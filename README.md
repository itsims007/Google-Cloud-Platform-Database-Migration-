# Steps in Google Cloud Platform (Database Migration)

- Connect to Google Cloud Shell
- **Download** the dump using wget

  - cd ~
  - wget https://tcb-public-events.s3.amazonaws.com/icp/mission3.zip
  - unzip mission3.zip
 
Connect to MySQL DB running on Cloud SQL (once it prompts for the password, provide welcome123456). Don’t forget to replace the placeholder with your Cloud SQL Public IP.

    - mysql --host=<replace_with_public_ip_cloudsql> --port=3306 -u app -p

Import the dump on Cloud SQL

    - use dbcovidtesting;
    - source ~/mission3/en/db/db_dump.sql

Check if the data got imported correctly
  
    - select * from records;
    - exit;
