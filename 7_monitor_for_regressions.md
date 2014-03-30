## Monitor for regressions / follow-up

### Review monitoring alerts

* Smokey should stay green
* Nimsoft should not raise alerts
* Icinga should not raise unexpected alerts

### Sync P1 Staging from P1 Production

* We should kick off the platform sync job

### Ensure that Deploy jobs from Interim are disabled

* Consider disabling Jenkins on Interim Production

### Ensure that Platform 1 is running off the right code branches of repos

* `application-deployment-repo`: release
* `infrastructure-deployment-repo`: master
* `infrastructure-puppet-repo`: release
