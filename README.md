-------------------------------------------------------------------------------------------------------------------
Table structure: job_parameters
-------------------------------------------------------------------------------------------------------------------
JOB_ID  				: primary key Put the Job name 
FILE_GEN_PATH  			: Put the path where you want to generate the file after execution the job.
FILE_NAME				: Put file name like <file_name_DDMMYYYYHHMMSS>.txt or <file_name_DDMMYYYYHHMMSS>.csv
HEADER  				: Put like 'HRD' or blank if blank means, there is no header added in the first line of the prifix
FOOTER 					: Put like 'TRL' or blank if blank means, there is no footer added in the first line of the prifix along with date and time.
DATE_FORMAT				: Put the date format like "ddMMYYY HH:mm:ss" or you can add whatever you want date format.		 			  
APPLICATION_NAME 		: Put 'TRD' (Trade) or blank if blank means, there is no header added in the first line of the safix along with date and time.
EXECUTION_FREQUNCY  	: DAILY , INTRA DAY, MONTHLY AND QUATERLY (Just for the info)
CRONTAB_DTL  			: Put the crontab detail.
CHECKSUM_ALGO  			: Put "MD5" or "SHA-256" - if it's blank that meant checksum is not require.
PGP_ENCRYPTION			: Put flag Y/N If it Y then need to implement the pgp encryption
FILE_DATA_SEPERATION	: Put data saperation in the file like pipe or cumma ( | and , etc..)
FILE_TYPE				: Put txt, csv only.
DESCRIPTION  			: Put the detail information for the job 
-------------------------------------------------------------------------------------------------------------------
Table schema:
-------------------------------------------------------------------------------------------------------------------
CREATE TABLE `prepareexamdb`.`job_parameters` (
  `JOB_ID` VARCHAR(100) NOT NULL,
  `FILE_GEN_PATH` VARCHAR(100) NULL,
  `FILE_NAME` VARCHAR(100) NULL,
  `HEADER` VARCHAR(20) NULL,
  `FOOTER` VARCHAR(20) NULL,
  `DATE_FORMAT` VARCHAR(45) NULL,
  `APPLICATION_NAME` VARCHAR(45) NULL,
  `EXECUTION_FREQUNCY` VARCHAR(45) NULL,
  `CRONTAB_DTL` VARCHAR(45) NULL,
  `CHECKSUM_ALGO` VARCHAR(45) NULL,
  `PGP_ENCRYPTION` VARCHAR(45) NULL,
  `FILE_DATA_SEPERATION` VARCHAR(45) NULL,
  `FILE_TYPE` VARCHAR(45) NULL,
  `DATEMINUS1ORCURRENTDAY` VARCHAR(45) NULL,
  `CHECKSUM_FLAG` VARCHAR(1) NULL,
  PRIMARY KEY (`JOB_ID`));

  -------------------------------------------------------------------------------------------------------------------
