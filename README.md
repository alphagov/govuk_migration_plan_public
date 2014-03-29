# 2014 GOV.UK Platform Migration Overview

## Introduction

This is the plan for migrating the GOV.UK web stack from the Skyscape's **interim platform** to Skyscape's new **Platform 1**. The original plan is still held on our internal GitHub repo, however this version (with sanitised IPs, domains and GitHub repos) has been released publicly after the fact.

## Migration Plan

The migration plan is a series of [Markdown](https://help.github.com/articles/markdown-basics) documents. You can start by reading the [Overview](0_overview.md) or click on the linked sections below for more detail:

* [0. Overview](0_overview.md)
* [1. Pre-migration activity and communications](1_prior_activities.md)
* [2. Disable external publishing and licence applications](2_disable_external_access.md)
* [3. Synchronise data between the two platforms](3_synchronise_data.md)
* [4. Repoint to new platform](4_point_to_new_platform.md)
* [5. Conduct testing of content and publishing](5_test_all_the_things.md)
* [6. Enable external publishing and licence applications](6_enable_external_access.md)
* [7. Monitoring for regressions](7_monitor_for_regressions.md)
* [ANNEX A - List of DNS records](ANNEX_A_list_of_dns_records.md)

## Outstanding questions

* How do we synchronise web site support feedback tickets?
  * The `support_contacts` database is now part of the automated job.
* Do we accept that we might lose some end-user feedback during the migration?
  * We will only lose anonymous feedback statistics and Transaction Done surveys.
  * No Zendesk tickets will be lost.
