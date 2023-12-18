# Using the Mathrutech system 

When your userid was set up on Mathrutech's system they sent an email containing details of sample programs, files, databases, and JCL members that they define to help you get started. The information includes the following. Note that several of these values will be unique per user. 

IP Address: 23.229.8.213  
Port: 8723

User Id: [provided]  	MATEVA
Password: [provided]  	RAK734
DB2 Database: DBMATE1  
Tablespace: TSMATEVA  
DB2 Plans: MATEVAA, MATEVAB, MATEVAC, MATEVAD  

Sample CICS resources: 

Program: MVAPGM1  
Mapset: MVAMPS1  
Transaction: MVA1  
File: MVAFIL1  
DB2Entry: MVAENT1  
DB2Tran: MVATRN1  
TDQueue: MVAT  
Group: Your Mateva ID  

Mappings: 

MVA1 -> MVAPGM1  
MVAENT1 -> MATEVAA  
MVATRN1 -> MVAENT1 & MVA1 

Dataset allocation:

Use volume DEVHD3  
Specify tracks, max 12 tracks primary and secondary  
Use your ID as the high level qualifier   

## Connecting to Mathrutech 

Mathrutech does not provide a front-end for accessing z/OS. You can use any 3270 terminal emulator. Use the IP address and port provided in your sign-up email.

## Connecting with x3270 

If you are using x3270 on OS X (Mac) and you installed x3270 as documented in [Using x3270 with Mateva](Using_x3270_with-Mateva.md), you can create a shell script to start ```c3270``` and get you to the Mateva log on screen:

```shell 
/opt/homebrew/Cellar/x3270/4.3ga4/bin/c3270 23.229.8.213:8723
```

In my case, I put the script in a directory that is already on the path, and named it ```mateva```.

### File transfer 

IND$FILE is not available to us on the host system. The c3270 file transfer features will not work. 

ISPF option 3.7.2 (file transfer) is not available to us on the host system. 

If you want to provide sample code for your students, you will have to type it in by hand each time you set up a class. 

If you want to keep a copy of files you create on the Mateva system, you will have to type them in by hand on your local system. 

## TSO/ISPF 

