# DataBase_IBM
creating a database in mysql and performing operations in iib ace toolkit


configuring the DSN

-->search for odbc datasource 64 bit
-->go to system dsn
-->click on add and select mysql odbc ansi driver
-->provide the username password,datasource name
-->test the connection

mqsi command for connecting to db
mqsisetdpparms DBNode -n ibmNodeODBC -u root -p root
mqsicvp DBNode -n MYSQLIIBM_ODBC
mqsireload DBNode
mqsichangeproperties DBNode -e server -o ComIbmJVMManager -n jvmDebugPort -v 3999

-->provide the same dsn name in compute node
