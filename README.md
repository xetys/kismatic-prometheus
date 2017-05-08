# Kismatic prometheus operator

    This project contains a deployment bundle to install prometheus operator to a kubernetes cluster, provisioned by kismatic enterprise toolkit.

    ## What's in the box?

    * a prometheus operator, which automatically can spawn new prometheus instances
* new TRPs: `Prometheus`, `ServiceMonitor`, `AlertMananger`, see (documentation)[https://coreos.com/operators/prometheus/docs/latest] and (GitHub Project)[https://github.com/coreos/prometheus-operator/] for further info

## Requirements

* existence of `kubectl`
* cluster context set up for your KET cluster

## Install
