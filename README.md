# README

In order to run this application in Azure Web App Linux you need the following steps:

1. Create a Ruby 2.7.3 web app
2. Add this app setting **`ASSETS_PRECOMPILE=true`**
3. Fork this repository to your account and then set up deployment center with the forked repository.

To run this app locally, make sure you have 2.7.3 installed and then run `bundle install` to install gems, finally use `rails server -b 0.0.0.0` to run the app.

## Troubleshooting
If profiler is not being loaded, review the following:

* SSH into the container using `https://<sitename>.scm.azurewebsites.net/webssh/host` and cd into /home/site/wwwroot/log, cat production.log to check for any exception.
* Request a couple of times to load the speed badge in home page.
* Cd into /home/site/wwwroot/tmp and delete miniprofiler folder with rm -rf miniprofiler/, then stop and start the site from the azure portal.

