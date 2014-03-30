## Disable external access

### Stop applications on both platforms

* `Apply for a Licence` frontend
  * This can't be done using firewall rules, because as the service can be accessed via GOV.UK

### Block access via the vSE Firewall to Interim Platform

* [Backend Load Balancer](https://internal.github/gds/vcloud-provisioner/blob/master/edgegateway/production/firewall.rb#L21-L29)
* [EFG](https://internal.github/gds/vcloud-provisioner/blob/master/edgegateway/production/firewall.rb#L36-L44)
* [Licensify Admin](https://internal.github/gds/vcloud-provisioner/blob/master/edgegateway/production/firewall.rb#L46-L54)
* [Licensify Upload](https://internal.github/gds/vcloud-provisioner/blob/master/edgegateway/production/firewall.rb#L46-L54)

### Block access via the vSE Firewall to Platform 1

* [Backend Load Balancer](https://internal.github/gds/govuk-provisioning/blob/master/networking/common/firewall.rb#L40-L48)
* [EFG](https://internal.github/gds/govuk-provisioning/blob/master/networking/common/firewall.rb#L55-L63)
* [Licensify Admin/Upload](https://internal.github/gds/govuk-provisioning/blob/master/networking/common/firewall.rb#L65-L73)

### Allow access from GDS

* Add a rule to allow GDS to access port 80 and 443 on any Interim Platform IP
* Add a rule to allow GDS to access port 80 and 443 on any Platform 1 IP

Next Steps [3_synchronise_data.md](3_synchronise_data.md)
