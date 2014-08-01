diagnostic-buildpack
====================

A sample buildpack which is used in diagnosing how cloudfoundry behaves w.r.t. buildpacks

In particular it produces output logs on stdout and stderr to help in diagnosting when a CF instance swallows them.

Usage:

```
 $cf push diag-buildpack -p ./bin -b https://github.com/gberche-orange/diagnostic-buildpack.git

 Updating app diag-buildpack in org myorg / space development as me@me.org...
 OK
 
 Uploading diag-buildpack...
 Uploading app files from: ./bin
 Uploading 1.7K, 3 files
 OK
 
 Stopping app diag-buildpack in org myorg / space development as me@me.org...
 OK
 
 Starting app diag-buildpack in org myorg / space development as me@me.org...
 OK
 -----> Downloaded app package (4.0K)
     Cloning into '/tmp/buildpacks/diagnostic-buildpack'...
     Compile echoing on stdout
 Fri Aug  1 13:07:15 UTC 2014
 Compile echoing on stderr
 Fri Aug  1 13:07:15 UTC 2014
 Compile echoing on stdout after waiting 1s
 -----> Uploading droplet (4.0K)
 
 1 of 1 instances running
 
 App started
 
 Showing health and status for app diag-buildpack in org myorg / space development as me@me.org...
 OK
 
 requested state: started
 instances: 1/1
 usage: 1G x 1 instances
 urls: diag-buildpack.cfapps.io
 
      state     since                    cpu    memory       disk
 #0   running   2014-08-01 03:07:22 PM   0.0%   552K of 1G   56K of 1G
 Endpoint deprecated
 ```
