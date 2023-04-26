# Data Project Example

This is an example template to use for research classroom studies in my SQL training.


### Assumptions

All projects will use Postgresql as an SQL RDBMS and it will need to be
installed. Instructions for installation of Postgresql will not be covered in
this document.

All projects will be based on a POSIX operating system. If you are using
Windows, this will mean instructions may not directly relate to what programs
and commands available on your computer. MacOS and Unix operating systems
should be covered.


### File Structure

<pre>
/
|- data (data files related to the project)
|- sql (sql scripts related to the project)
</pre>


##### Data directory

Copy all your data files in to this directory. It will make future referencing
of the files easier. Keep in mind, you can renaming the files to whatever is
easier to remember or type once they are copied to this directory.


##### SQL scripts directory

A few SQL scripts have been created in this folder. They related to creation
of tables and importing of data into those tables. You can create any scripts
in this directory that may be repetitve commands. Once scripted, it is quicker
to rebuild your table(s) and import data from these files than to retype the
commands in the psql client directly.


##### SQL scripts execution

To execute SQL, it is necessary to use the psql client manually or reference a
script file with existing SQL inside the file. The commands that follow
describe how to execute SQL script files from a unix command line prompt. They
are split out by creating and importing, but you can create your own scripts
and execute those in whatever manner you wish.


**Creating Tables**
```sh
psql -d <database-name> -f ./sql/create.sql
```

**Importing Data**
```sh
psql -d <database-name> -f ./sql/import.sql
```

