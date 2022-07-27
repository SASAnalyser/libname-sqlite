# This is SAS/ACCESS Interface to sqlite, let you read/write data from/to sqlite by using libname statement directly.
1. Installation:
just download the sqlite.zip and unzip it to <SASHome>\SASFoundation\9.4\core\sasexe

2. Usage:
/* write to sqlite database */
libname mylib sqlite "C:/temp/sample.db";
data mylib.air;
set sashelp.air;
run;

/* read from sqlite database */
libname mylib sqlite "C:/temp/sample.db";
data air;
set mylib.air;
run;

3. Limitation:
a. Not support bulkload.
b. Not support viewtable in Base Explorer.
c. Not support property in Base Explorer.
d. Only support Windows x64, may provide Linux version soon.
