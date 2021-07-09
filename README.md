# O11y Pipeline Demo

This demo application shows that how to use an Observability Pipeline in a sample java application architecture.

The java application has been instrumented by OpenTelemetry Java Auto Instrumentation.
You can reach the Application UI with 80 port from the server which you have installed the demo app.
"Traces" page of the application gives you all the ready links of the observability tools;

- SignalFx
- Splunk
- Grafana
- Google Stackdriver
- Jeager
- Zipkin

### O11y Pipeline Demo Architecture

![image](/etc/nginx/html/architecture.png)

## Installation Options

### Install The Demo App & Pipeline & Observability Tools (All In One)

Installation steps:

```
git clone <git_repo_url>
cd oi-observability-pipeline-demo
#update the envrioenment variables of SFX & Splunk on .env file
vi .env
docker-compose up -d
```

### Install Only The Demo App

Installation steps:

```
git clone <git_repo_url>
cd oi-observability-pipeline-demo
#update the envrioenment variables of SFX & Splunk on .env file
vi .env
docker-compose -f docker-compose-java.yml up -d
```

### Install Only O11y Pipeline & Observability Tools

Installation steps:

```
git clone <git_repo_url>
cd oi-observability-pipeline-demo
#update the envrioenment variables of SFX & Splunk on .env file
vi .env
docker-compose -f docker-compose-pipeline.yml up -d
```

## O11y Pipeline Demo Environment

Demo environment has been created under "ingka-itoi-explore-dev" GCP project with the name of:

- observability-pipeline-demo (Primary)
- observability-pipeline-demo-backup (Secondary)
  These are Ubuntu instances which are installed docker engine and compose.

Current installation directory:

```
/home/o11y/
```

Installation steps:

```
git clone <git_repo_url>
cd oi-observability-pipeline-demo
#update the envrioenment variables of SFX & Splunk on .env file
vi .env
docker-compose up -d
```

After the first deployment, you can move deployDemoApp.sh to parent folder and just need to execute the following command to update the demo app with the latest version:

```
./deployDemoApp.sh
```

## Work Instructions

Before doing any work you need to run the Makefile to setup the project settings for git.

```
make init
```
