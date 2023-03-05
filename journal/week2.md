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
![Proof)](assets/22-proof-create-xray-json file.png)
![Proof)](assets/24-proof-create-cruddur-group-in-xray-from-terminal.png)

### Configure and provision X-Ray daemon within docker-compose and send data back to X-Ray API
![Proof)](assets/27-proof-add-xray-daemon-and-xray-env-vars-to-docker-compose.png)

### Observe X-Ray traces within the AWS Console
![Proof)](assets/28-proof-aws-xray-traces-showing-data.png)
![Proof)](assets/29-proof-instument-xray.png)
![Proof)](assets/30-proof-segments-and-subsegments-aws-xray.png)

### Integrate Rollbar for Error Logging
![Proof)](assets/)

### Trigger an error an observe an error with Rollbar
![Proof)](assets/)


### Install WatchTower and write a custom logger to send application log data to CloudWatch Log group
![Proof)](assets/)
