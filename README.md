# README

In order to run this application in Azure Web App Linux you need the following steps:

* Select Ruby 2.6 
* Add this app setting ASSETS_PRECOMPILE=true

## Troubleshooting
If profiler is not being loaded, review the following:

* SSH into the container using `https://<sitename>.scm.azurewebsites.net/webssh/host` and cd into /home/site/wwwroot/log, cat production.log to check for any exception.
* Request a couple of times to load the speed badge in home page.
* Cd into /home/site/wwwroot/tmp and delete miniprofiler folder with rm -rf miniprofiler/, then stop and start the site from the azure portal.

