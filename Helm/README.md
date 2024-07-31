# Solution Kubernetes Helm

1. How Prometheus works
   Prometheus collects logs/data from configured targets at given intervals and store locally. Also it can runs rules over this data to generate alerts.

2. Creating custom Prometheus alerts
   Here's an example of an alert rule configuration:

```
groups:
  - name: example
    rules:
      - alert: HighCPUUsage
        expr: rate(container_cpu_usage_seconds_total[5m]) > 0.9
        for: 5m
        labels:
          severity: critical
        annotations:
          summary: "High CPU usage detected"
          description: "CPU usage is above 90% for more than 5 minutes."
```
