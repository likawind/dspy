# Configuring Metrics Logging Through Zeek Log Streams

## Overview

Metrics and stats logging through Zeek log streams is a feature that is **enabled by default** on Corelight Sensors. This functionality allows you to monitor various metrics such as CPU, memory, and disk usage, which are crucial for maintaining optimal sensor performance.

## Disabling Metrics Logging

If you wish to disable metrics logging, you can do so through the Fleet Manager. This can be configured as a sensor configuration option and applied either to a **Policy** or to individual sensors.

## Enabling and Adjusting Metrics Logging

To enable or adjust metrics logging, follow these steps:

1. Navigate to **Sensor > Statistics** in the sensor UI.
2. Enable the setting for **Enable Reporting Through Zeek Log Streams**.
3. Set the **Reporting Interval** to your desired frequency.

Once configured, metrics logs such as `metrics_cpu`, `metrics_memory`, and `metrics_disk` will be exported alongside other Zeek logs using your configured export mechanisms. These mechanisms can include HEC, Kafka, Splunk, JSON, Elasticsearch, or Syslog.

## Granular Control

For more granular control over your metrics logging, ensure that you configure the settings based on your specific logging requirements. This will help you tailor the logging to suit your operational needs and ensure that you are capturing the necessary data for analysis and monitoring.

By following these steps, you can effectively manage and configure metrics logging on your Corelight Sensors, ensuring that you have the necessary insights into your system's performance.