# Microsoft Defender Integration with Corelight

The integration between Microsoft Defender and Corelight is designed to enhance your security logs by adding valuable host information and CVE (Common Vulnerabilities and Exposures) vulnerability data. This integration utilizes the Machines API and the Vulnerabilities by Machine and Software API to enrich specific logs, providing a more comprehensive view of your network's security posture.

## Log Enrichment Details

- **Enriched Logs**: The integration specifically enriches the `known_hosts.log` and `suricata_corelight.log` files. These logs are augmented with additional details such as:
  - **IP Address**: The network address of the host.
  - **Hostname**: The name assigned to the host.
  - **OS Version**: The operating system version running on the host.
  - **Known CVE List**: A list of known vulnerabilities associated with the host.

- **Non-Enriched Logs**: It is important to note that while the `conn.log` is ingested by Microsoft Defender for IoT, it does not receive enrichment from this integration.

This integration helps in providing a more detailed and actionable insight into your network's security, allowing for better threat detection and response.