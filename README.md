# Tomcat package

Tomcat is an open-source web server designed to host and run Java-based web applications. It is a lightweight server with a good performance for applications running in production environments

## Parameters
Configuration Reference

### Tomcat parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|pullPolicy|Tomcat image pull policy|String|IfNotPresent| 
|Replicas|Specify number of Tomcat replicas|integer|1|
|containerPorts.http|HTTP port to expose at container level|integer|8080|
|containerSecurityContext.runAsUser|User ID for the Tomcat container|integer|1001|
|containerSecurityContext.runAsNonRoot|Force user to be root in Tomcat container|String|TRUE|
|livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe|integer|120|
|livenessProbe.periodSeconds|Period seconds for livenessProbe|integer|10|
|livenessProbe.failureThreshold|Failure threshold for livenessProbe|integer|5|
|livenessProbe.successThreshold|Success threshold for livenessProbe|integer|1|
|readinessProbe.enabled|Enable readinessProbe|String|TRUE|
|readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe|integer|30|
|readinessProbe.periodSeconds|Period seconds for readinessProbe|integer|5|
|readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe|integer|3|
|readinessProbe.failureThreshold|Failure threshold for readinesStringsFALSEProbe|integer|3|
|readinessProbe.successThreshold|Success threshold for readinessProbe|integer|1|

### Traffic Exposure parameters

|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|ingress.enabled|Enable ingress controller resource|String|FALSE
|ingress.pathType|Ingress path type|string|ImplementationSpecific|

### Metrics parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|metrics.podMonitor.enabled|Create PodMonitor Resource for scraping metrics using PrometheusOperator|String|FALSE|
|metrics.podMonitor.interval|Specify the interval at which metrics should be scraped|integer|30s|
|metrics.podMonitor.scrapeTimeout|Specify the timeout after which the scrape is ended|integer|30s|
|metrics.prometheusRule.enabled|Set this to true to create prometheusRules for Prometheus operator|String|FALSE|
|metrics.prometheusRule.additionalLabels|Additional labels that can be used so prometheusRules will be discovered by Prometheus|String|{}|
