---
layout: default
title: Troubleshooting
nav_order: 8
has_children: true
has_toc: false
---

## Troubleshooting

This is our general overview on SLA Standards when submitting a service request and weekend support. 

### Getting Support
<a href="https://support.cloudm.io/hc/en-us/requests/new">Contact our 24/7 support team.</a>

### Service Level Agreement & Response Times

It is the responsibility of the CloudM Product Support Engineer to determine an appropriate priority and action based on business impact. For urgent issues our response time is 4 hours from the initial receipt of the issue and all other issues is 8 hours.

| Priority level | Response Time| Update Schedule |
| --- | --- | --- |
| High | 2 Hours |  24 Hours |
| Medium | 4 Hours |  36 Hours |
| Low| 8 Hours |  48 Hours |

### 24-hour Weekend Support 

-  Weekend support for P1 issues is a 4-hour response SLA.
-  Support accessible 24/7. 
-  Engineers are located in US, Singapore, UK and utilizes a follow the sun model.

### Sending Traces and Project Configs to Support

To expedite the request please fill out the support ticket with the relevent information about the issue that is occuring. Providing screenshots, trace logs, and configuration files can assist us with providing answers faster. There is not an option to export the configuration from the hosted version of the tool, Support already has access to this information.

**NOTE:**  If using CloudM Migrate SAAS, please open a support ticket via our Help Center and inform support of the destination migration domain.

#### How to Export Configuration File 

To export your Logging and Trace Files:

- Go to the Projects page with in CloudM Migrate. 
- Click the Gear Cog icon in the upper right. 
- Select the Export Configuration icon.
 
#### How to Locate Traces 

When running a self hosted migration the locatation of a trace logs is the C:\ProgramData\Cloud Technology Solutions folder on the primary server.

### Exceptions 

If migrating from Lotus Notes, GroupWise, Zimbra, Box, Dropbox, PST and Windows File System, select General Migration Settings > Advanced Settings > System > Trace Level to TRACE instead, this will gather additional tracing for those platforms.

### Generating a Debug Level Trace

In order to generate a trace file with full visibility on how the tool is handling data another pass is required please follow the steps on how to set the tool to debug level.  Select Step 4 - **Config Settings** > **Advanced Settings** > **System** and set **Trace Level** to **Debug**  within CloudM Migrate.

### Cluster Logs 

When running CloudM Migrate in a Cluster, different log files are written to a few different locations. The configurable storage location does not apply to clustered migrations, and logs are always written to the following locations:

Migration logs are written to the secondary node on which the migration occurred. To determine which secondary node performed a migration for a user, refer to the progress tab or the CSV report files generated at the end of a migration.

### Primary Node

- User interface logs - C:\ProgramData\Cloud Technology Solutions\CloudMigrator\CloudMigrator.UI.Trace.txt
- User interface logs store information about the user interface and can be used to help troubleshoot any issues with it
- User interface logs are kept on a rolling basis, the latest has no number
- Migration logs - C:\ProgramData\Cloud Technology Solutions\CloudMigrator\CloudMigrator.Trace.txt
- Migration logs contain detailed information about what happened during a migration and can be used to help diagnose issues with user migrations.
- The 10 most recent migration logs are kept, the latest log file is always that without a number
- Service logs - C:\ProgramData\Cloud Technology Solutions\CloudMigrator.Service.Trace.txt
- Service logs provide information about the management of migrations and communication between system components
- Service logs are kept on a rolling basis, the latest has no number.

### Secondary Node 

- Migration logs - C:\ProgramData\Cloud Technology Solutions\CloudMigrator\CloudMigrator.Trace.txt
- Migration logs contain detailed information about what happened during a migration and can be used to help diagnose issues with user migrations.
- The 10 most recent migration logs are kept, the latest log file is always that without a number.
- Service logs - C:\ProgramData\Cloud Technology Solutions\CloudMigrator.Service.Trace.txt.
- Service logs provide information about the management of migrations and communication between system components.
- Service logs are kept on a rolling basis, the latest has no number.
 

