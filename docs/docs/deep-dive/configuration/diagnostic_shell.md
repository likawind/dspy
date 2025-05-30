# Accessing Diagnostic Shell for Configuration

### Running `broala-config` Commands from the Diagnostic Shell

To execute `broala-config` commands, you must access the Corelight Sensor's diagnostic shell. This provides direct interaction with the sensor for configuration management. Use the following steps:

1. **Access the Diagnostic Shell**: Connect to the Corelight Sensor's diagnostic shell to begin the configuration process.
2. **Run Commands**: Use the command `sudo broala-config` to view or modify key-value pairs within the sensor's configuration.
3. **Apply Changes**: After making the necessary modifications, apply the changes by executing `sudo broala-config apply`.

This method ensures manual control over sensor configurations, complementing automated processes like Kubernetes-based management. It allows for precise adjustments and troubleshooting directly on the sensor.