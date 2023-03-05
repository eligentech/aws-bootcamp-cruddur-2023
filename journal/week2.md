# Week 2 — Distributed Tracing

## Required Homework / Tasks

### Instrument Honeycomb.io with (OTEL) into the backend-flask application
I followed along with Andrew's Week 2 class, signed up for Honeycomb.io and added the Honeycomb.io code to connect it to my backend-flask/app.py file:
![Added Honeycomb.io code to app.py)](assets/04-proof-add-honeycomb-updates-for-tracer-and-flask-instrumentation-to-app-dot-py.png)

### Run queries to explore traces within Honeycomb.io
I followed along, created a trace, and added the multispan trace as Jessica Kerr suggested:
![Honeycomb.io trace with 2 spans)](assets/15-proof-trace-results-with-2-spans.png)

### Added npm i to gitpod.yml for frontend-flask-js
I had wondered why we hadn't done this before so I'm glad we added it to gitpod.yml
![Add npm i to gitpod.yml for frontend-flask-js)](assets/20-proof-add-npm-i-to-gitpod-dot-yml-file.png)

### Instrument AWS X-Ray into backend flask application
I watched and followed along with Andrew's follow-up video on X-Ray, created the required xray-json file.....
![Create xray-json file](assets/22-proof-create-xray-json-file.png)

...and created a crudder group in X-Ray from the Terminal
![Create xray cruddur group from terminal](assets/24-proof-create-cruddur-group-in-xray-from-terminal.png)

### Configure and provision X-Ray daemon within docker-compose and send data back to X-Ray API
I added the x-ray Daemon code into docker-compose to provision the X-Ray daemon:
![Add code to docker-compose to conig and provision X-Ray Daemon](assets/27-proof-add-xray-daemon-and-xray-env-vars-to-docker-compose.png)

### Observe X-Ray traces within the AWS Console
After running Compose UP on docker-compose, opening up the backend in my browser, and hitting refresh a few times I started to see data coming through into the AWS X-Ray Console.
![X-Ray console showing data from backend-flask)](assets/28-proof-aws-xray-traces-showing-data.png)

Tracet map of data:
![Trace Map](assets/29-proof-instument-xray.png)

After we added code to track subsegment activity it started to show up in the console to:
![Traces showing subsegment activity](assets/30-proof-segments-and-subsegments-aws-xray.png)

### Integrate Rollbar for Error Logging
I followed Andrew's follow-up Rollbar video and add the rollbar instrumentation to backend-flask app.py
![Add Rollbar integration to app.py](assets/52-proof-add-rollbar-instrumentation-to-app-dot-py.png)

Initially, Rollbar did not connect to my backend-flask instance and after investigation I saw that when docker-compose was running there was a warning about the not receiving a value for the rollbar_access_token even though I set the env vars..and that the value was set to the default which was blank.  

I didn't take a screenshot of that, but when I attached terminal to the backend-flask docker container "env | grep ROLL" didn't show the rollbar token.  After committing and deleting my gitpod workspace and starting a new one, the env vars were passed and Rollbar connected.  

![Proof that rollbar/test works)](assets/54-proof-rollbar-test-page-works.png)

Once the env vars were being passed, rollbar started receiving data and showing stats:
![Rollbar connected and showing data](assets/55-proof-rollbar-stats.png)

### Trigger an error an observe an error with Rollbar
After confirming that Rollbar was connected and receiving data, we janked the code by removing code from home_activities.py
![Error in Rollbar after janking the code)](assets/57-proof-rollbar-error-from-home-activities-dot-py.png)

Clicking the error showed more detail:
![Detail of error that Rollbar reported)](assets/58-proof-rollbar-trace-of-error.png)

I also received an email from Rollbar with an alert regarding the error:
![Email notificatoin from Rollbar](assets/60-proof-email-from-rollbar-error-notification.png)

### Install WatchTower and write a custom logger to send application log data to CloudWatch Log group
Following Andrew's Cloudwatch video I was able to install and configure Watchtower, and send data to the AWS Cloudwatch.
![Cloudwatch Configuration proof](assets/47-proof-that-logs-are-being-sent-to-cloudwatch-for-cruddur-group.png)
