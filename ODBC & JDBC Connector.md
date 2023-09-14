**ODBC & JDBC Connector:**

** TNS entry **

Path: cd $ORACLE_HOME or /opt or chdbclients/oracle/product/12.1.0/network/admin
File: tnsnames.ora

Syntax:
DNS name =
   (DESCRIPTION = (Enable=broken) 
     (ADDRESS_LIST =
       (ADDRESS =
         (PROTOCOL = TCP)
          (HOST = hostname)
         (PORT = port number)
       )
     )
     (CONNECT_DATA =
        (SERVICE_NAME = Service name)
       (INSTANCE_NAME = PV)
     )
   )`

To test the connectivity: tnsping (DNS name)

Note: Oracle connections are timing out when connecting from DataStage. Hence Enable=broken will help to keep the connection intact.

** DNS Entry **

Path: cd $DSHOME or /opt or chdba/IBM/InformationServer/Server/DSEngine/sample/
File: .odbc.ini

Syntax:
[DNS name]
Driver=/chdba/IBM/InformationServer/Server/branded_odbc/lib/VMsqls00.so 
Description=DataDirect SQL Server Native Wire Protocol
AlternateServers=
AlwaysReportTriggerResults=0
AnsiNPW=1
ApplicationName=
ApplicationUsingThreads=1
AuthenticationMethod=1
BulkBinaryThreshold=32
BulkCharacter Threshold=-1
BulkLoadBatchSize=1024
BulkLoadOptions=2
ConnectionReset=0
ConnectionRetryCount=5
ConnectionRetryDelay=5
Database=(DB name)
EnableBulkLoad=0
EnableQuotedidentifiers=0
EncryptionMethod=1
FailoverGranularity=0
FailoverMode=0
FailoverPreconnect=0 
FetchTSWTZasTimestamp=0
FetchTWFSasTime=1 
GSSClient-native
HostName=(Servername/hostname)
HostNameInCertificate= 
InitializationString=
Language=
LoadBalanceTimeout=0
LoadBalancing=0
LoginTimeout=180
LogonID=
MaxPoolSize=100
MinPoolSize=0
PacketSize=0
Password=
Pooling=0
MinPoolSize=0
PacketSize=0
Password=
Pooling=0
PortNumber=(Portnumber)
QueryTimeout=0
ReportCodePageConversionErrors=0
SnapshotSerializable=0
TrustStore=
TrustStorePassword= 
ValidateServerCertificate=0
WorkStationID=
XML Describe Type=-10
SeedBeforeConnect=1
MultiSubnetFailover=True

To Test the connectivity: 

Step 1: Use the path /chdba/IBM/InformationServer/Server/branded_odbc/samples/example
Step 2: run the script ./example
Step 3: Enter the DataSourcename(DSN), Username & Password

Note: If Servers are HA enabled, then we should use MultiSubnetFailover.

** Interfaces **

Path: cd $SYBASE or /opt/sybase 
File: interfaces

Syntax:
DSN name

         master tcp ether (hostname) (port number)

         query tcp ether (hostname) (port number)
ODBC & JDBC Connector.txt
Displaying ODBC & JDBC Connector.txt.
