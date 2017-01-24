# Host variables

The following server variables are provided to Ansible from the Memset API:

| Variable Name | Type | Description |
| ------------- | ---- | ----------- |
| memset_backups | Boolean | Whether this server has a backup service |
| memset_control_panel | String | describing the control panel, e.g. “none”, or “cpanel”. |
| memset_data_zone | String | The name of the data zone this service is in (if applicable). Some services that don’t have data at rest are data zone independent and this field will be empty. |
| memset_expiry_date | Date | The end date of the service. |
| memset_firewall_rule_group_name | String | The unique identifier for this rule group. |
| memset_firewall_rule_group_nickname | String | The nickname of this rule group. |
| memset_firewall_type | String | Describes the firewall type, e.g. “none”, “basic”, “self_managed” or “managed”. |
| memset_ignore_monitoring_off | Boolean | Whether the customer has acknowledged that they aren’t being monitored. |
| memset_monitor | Boolean | Whether we are monitoring this server |
| memset_monitoring_level | String | Describes the monitoring level, “basic”, “advanced” or “managed”|
| memset_network_zone | String | The name of the network zone this server is associated with |
| memset_nickname | String | The friendly 'nickname' of this server, set in the Control Panel |
| memset_no_auto_reboot | Boolean | Whether this server will be automatically rebooted by the Monitoring service|
| memset_os | String | Describes the Operating System installed, e.g. “debian_wheezy_64”, “win2012serverstd_r2_64”. |
| memset_penetration_patrol | String | The intrusion detection support level for this server e.g. “none”, “basic” = Self-monitored, “monitored” = Memset-monitored or “protected” = Memset-protected |
| memset_penetration_patrol_alert_level | Integer | The alert level that is set for Penetration Patrol intrusion detection (1-15) or 0 (penetration_patrol=”none”) |
| memset_renewal_price_amount | Float | The monetary amount for the monthly renewal including VAT |
| memset_renewal_price_currency | String | The currency for the renewal, e.g. “GBP”. |
| memset_renewal_price_vat | Float | The monetary amount for VAT on the monthly renewal |
| memset_start_date | Date | The start date of the service |
| memset_support_level | String | The support level of the server |
| memset_type | String | The type of server: server / miniserver |
| memset_vulnscan | String | whether this server is vulnerability scanned, ‘none’ = no scanning, ‘basic’ = Self-monitored, ‘managed’ = Memset-monitored. |
