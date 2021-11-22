# DPM
Data Protection Manager SQL Scripts

I needed a way to track Tape and backup information outside of the DPM database.
I used these scripts to track the information I needed to conform to audit requirements in the event that our infrastructure went down.
I am not going to the actual process but I used these 3 scripts to help me with the information I needed to:
1. Track operations Jobs
2. Track recovery jobs for both tapes and disk then prove I was also testing backup media before it left the tape library.
3. Track Tape backups and what jobs were going to what tapes.
  - a sub point to this is I used Power BI to create a nice dashboard I could use to look up recovery points and use as a print to accompany tapes.

General Implementation
These scripts were run on a SQL Server Agent job with a schedule that worked with how jobs where scheduled.
From there the scripts would export data into a Data Warehouse on a difference instance using SSIS.
Then I used Power BI to create dashboards around the Data Warehouse.




