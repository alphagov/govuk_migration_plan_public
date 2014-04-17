## Disable external access

### Stop applications on both platforms

* Licensify Frontend
  * This can't be done via Firewalling, because Licensify can be accessed via GOV.UK

### Block access via the VSE Firewall to Interim Platform

* Backend Load Balancer
* EFG
* Licensify Admin
* Licensify Upload

### Block access via the VSE Firewall to Platform 1

* Backend Load Balancer
* EFG
* Licensify Admin/Upload

### Allow access from GDS

* Add a rule to allow GDS to access port 80 and 443 on any Interim Platform IP
* Add a rule to allow GDS to access port 80 and 443 on any Platform 1 IP

Next Steps [3_synchronise_data.md](3_synchronise_data.md)
