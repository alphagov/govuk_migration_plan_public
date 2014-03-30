## Synchronise Data

### Run the Jenkins Job:

* https://deploy.jenkins/job/Copy_Data_to_P1_Production/

### Ensure that the following jobs complete without errors:

* Copy of MySQL databases for Backend Applications
* Copy of Mongo databases for Backend Applications
* Copy of MySQL whitehall_production DB from Interim Production to P1 Whitehall MySQL servers
* Copy of Mongo databases for Router
* Copy of EFG MySQL databases
* Copy of Errbit MongoDB database
* Copy of Support Contacts MySQL database
* Copy of ElasticSearch Indices
* Syncing Assets/Uploads

### Disable the job to sync from Interim to Platform 1

* This MUST be disabled from this point forward so we don't risk overwriting data

Next Steps: [4_point_to_new_platform.md](4_point_to_new_platform.md)
