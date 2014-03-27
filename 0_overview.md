# GOV.UK Platform Migration Overview

## Background

GOV.UK moved from Amazon AWS to a platform built by Skyscape Cloud Services in Q2 2012, known as the **Interim Platform**. That platform is fully accredited to the appropriate standards, however it was created at a time when cloud services for Government was an emerging market and was specifically built for GOV.UK.

In the past 12 months, Skyscape have created a multi-tenant Cloud Service, called **Platform 1**, which is built on newer technologies and should provide improved performance as compared to the Interim Platform. GDS will be migrating the GOV.UK web stack from the **Interim Platform** to **Platform 1** to take advantage of these improvements.

## Timeframe

The migration is expected to last 4 hours.

During the migration, GDS will:

1. Disable external publishing and licence applications
2. Synchronise data between the two platforms
3. Repoint our Content Delivery Network (CDN) to the new platform
4. Conduct testing of content and publishing
5. Enable external publishing and license applications
6. Monitor for regressions

## Impact on end users

The impact will be:

* **End Users (the public)** - low impact
  * License applications will not be available
  * Active content such as smart-answers and search may not be available for short periods.
  * The vast majority of content will be served from the CDN cache or our backup mirrors
* **Government users** - medium impact
  * Backend applications (e.g. publishing, licensing) will be unavailable; it will not be possible to edit or publish content.
  * Scheduled publishing may not happen at the configured time
    * Please let us know in advance if you have regulatory publishing needs that *MUST* be satisfied during the migration period.

## Activity overview

### [1. Pre-migration activity and communications](1_prior_activities.md)

Prior to the migration, GDS will:

* Communicate with affected government users
* Internally assess readiness for migration date
* Make technical changes to support the migration

### [2. Start migration: Disable external publishing and license applications](2_disable_external_access.md)

GDS controls the firewalls in front of our services and will use them to restrict access as follows:

* Access to backend applications on Interim Platform will be disabled
* Access to backend applications on Platform 1 will be restricted to GDS staff
* The License Application Tool will be shut down on Interim Platform

### [3. Synchronise data between the two platforms](3_synchronise_data.md)

Automated scripts run daily to copy databases and assets from the Interim Platform to Platform 1. Application versions are synchronised between the platforms such that an application deployment on the Interim Platform triggers an identical deployment to Platform 1. GDS will:

* Run the data sync scripts manually to ensure the latest data is on Platform 1
* Ensure that the application versions are correct
* Ensure that the Smoke Tests for each application pass
* Manually verify that recent publications have been copied

### [4. Repoint to the new platform](4_point_to_new_platform.md)

GDS controls the CDN configuration directly and will publish a new CDN configuration to direct user requests to the new platform.

GDS will also change the DNS entries for backend applications to point to Platform 1.

DNS TTL times will be set to short durations, but in the event of a failure to connect, users are advised to contact their local IT support to flush their DNS cache.

### [5. Conduct testing of content and publishing](5_test_all_the_things.md)

GDS will run a suite of automated tests against the new platform and ensure that these and external tests pass before opening up the platform for wider usage. The automated tests include content checks on a broad spectrum of GOV.UK pages (smoke tests).

Publishing via the Mainstream and Whitehall publishers will be manually checked (including scheduled publishing).

Applying for a test license will also be manually checked.

### [6. Enable external publishing and licence applications](6_enable_external_access.md)

* Access to backend applications on Interim Platform will remain disabled
* The License Application Tool will remain shut down on Interim Platform
* Access to backend applications on Platform 1 will be opened to the public

### [7. Monitor for regressions](7_monitor_for_regressions.md)

GDS will:

* Monitor our external checks and smoke tests
* Monitor user feedback submitted to our ticketing system (via report-a-problem)
* Monitor feedback from Government users via the Support Form

## Rollback plan

### Rollback prior to stage 5 (enable external access)

Depending how far the migration has progressed, GDS may opt to roll-back. Prior to stage 5, the rollback plan is to point our CDN back to the Interim Platform and re-enable firewall access to applications.

### Rollback after stage 5 (enable external access)

Depending on the amount of user activity, we may:

* Roll-back and perform manual data reconcilliation, or
* Continue with the migration and fix issues discovered

It is not possible to comprehensively outline the situations which would lead to each option, as it will depend on the degree of issues. The personnel involved will make a judgement according to the severity of any issues.
