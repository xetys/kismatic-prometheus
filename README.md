# Kismatic prometheus operator

This project contains a deployment bundle to install prometheus operator to a kubernetes cluster, provisioned by kismatic enterprise toolkit. It's based on the contrib scripts for cluster monitoring from the prometheus operator.

> why not using the original contrib scripts from prometheus operator project?

* the current version (v1.6.1) has an issue in the scraping progress
* the controller manager and scheduler are not properly set up, so alerts are comming

## What's in the box?

* a prometheus operator, which automatically can spawn new prometheus instances
* new TRPs: `Prometheus`, `ServiceMonitor`, `AlertMananger`, see [documentation](https://coreos.com/operators/prometheus/docs/latest) and [GitHub Project](https://github.com/coreos/prometheus-operator/) for further info
* a monitoring interface including node exporters, kube-state-metrics and prometheus for cluster-monitoring
* a prometheus instance on http://<NODE_IP>:30900 for cluster monitoring
* a grafana instance on http://<NODE_IP>:30902 (user: admin, password: admin
* a alert manager instance on http://<NODE_IP>:30903

## Requirements

* existence of `kubectl`
* cluster context set up for your KET cluster

## Install & Teardown

Run

```
$ ./deploy
```

to install all what's in the box to the namespace "monitoring", and 

```
$ ./teardown
```
to remove the workloads
