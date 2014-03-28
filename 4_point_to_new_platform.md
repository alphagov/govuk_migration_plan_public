## Point DNS to new platform

### Switch Fastly to new platform

* Change DNS for ip-d.production (192.0.2.4) to 198.51.100.4
* Wait for Fastly CDN to pick up the DNS change
* If DNS change fails to pick up, consider switching to IP instead of hostname temporarily
* Confirm that user requests are hitting new platform
* Confirm that user requests are not hitting old platform

### Switch DNS for backend apps

* Make all the remaining changes as outlined in [ANNEX_A_list_of_dns_records.md]
* Confirm that backend traffic reaches new platform from GDS

Next Steps: [5_test_all_the_things.md](5_test_all_the_things.md) 




