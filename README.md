# Grafana-tracker
My project for Quarqs test case 

Main targer was to create Dashboard using Grafana for visualisation,
Prometheus for reciving data and BlackBox exporter for tracking and expoting data + all ofit must be containerized in docker.

## **Scope of tasks** 

1) Grafana

Build a graph based on metrics
probe_http_duration_seconds.
This graph should show the difference
current phase values and values that were yesterday at that time
same time


Visualization:
write labels in the graphic legend in the format: phase – target,
display values on the graph on the right, with a table.
Enable stack series of values on the graph


2) Prometheus

Create an Alert

Condition:
if the average value of the probe_duration_seconds metric
within one minute for more than 2 seconds


3) Blackbox exporter

Configuration tasks:
consider the probe result unsuccessful if on the site which
we want to monitor through the http_2xx module
ssl is disabled



## How to run it

1) Import code and configs
2) ``` docker-compose build ```
3) ``` docker-compose up -d ```
4) Enter to the localhost:3000 and enter ``` admin``` as login and pass (you may skip changing password)
5) In Grafana enter here


![Screenshot_20220923_161615](https://user-images.githubusercontent.com/69244449/191981291-589b5f4c-d1d4-487f-bf7d-3cca8ba27c89.png)

6) Press on `Add data sources` and select Prometheus
7) In URL enter `http://prometheus:9090`,scroll down till the end and press on `save & test`
8) Enter here


![Screenshot_20220923_161508](https://user-images.githubusercontent.com/69244449/191981019-47165cbd-db4c-437f-9972-ab7dd96cb30d.png)

9) You can export my dashboard by Uploading JSON file or create a new one by youre self entering ID `7587` and pressing load
