## Activities to be completed prior to the migration day

### T-14 Days

* Assess the state of the project - will we be ready?
* Decide on the people we need to do the migration - are they available?
* Do we have reasonable backup people in place (or necessary redundancy)?
* Communicate to GDS
* Communicate to Departments (via SPoCs)

### T-7 Days

* Assess the state of the project - will we still be ready?
* Confirm that we have the necessary people in place
* Communicate to GDS (again)
* Communicate to Departments (again) - via SPoCs
* Block out the release calendar for:
 * T-1 Days
 * T-0 Days
 * T+1 Days

### T-3 Days

* Assess the state of the project - will we really be ready to go in 3 days?
* Assess the Data Replication - is it running reliably?
* Lower DNS TTLs on the DNS records listed as changing here: [ANNEX_A_list_of_dns_records.md](ANNEX_A_list_of_dns_records.md)
* Change A records to CNAMEs as listed here: [ANNEX_A_list_of_dns_records.md](ANNEX_A_list_of_dns_records.md)
* Review application versions - are they in sync across platforms?

### T-1 Days

* Final reminder to GDS
* Final reminder to Departments
* Review application versions - are they in sync across platforms?
* Review data sync - how long did it take, are we confident it will succeed tonight?
* Review Smokey and Nagios on Platform 1 - is everything green?

### T-0 Days

* Prepare merge pull requests on any out of sync repository branches.
* Confirm that all the people are ready to go

Next Steps: [2_disable_external_access.md](2_disable_external_access.md)
