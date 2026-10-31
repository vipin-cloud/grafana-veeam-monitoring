# Grafana Monitoring for Veeam Backup & Replication

## Overview

This project demonstrates the deployment and configuration of Grafana for monitoring Veeam Backup & Replication environments. It provides visibility into backup performance, job status, repository usage, and infrastructure health through interactive dashboards.

The solution is designed for backup administrators, infrastructure engineers, and IT operations teams who need centralized monitoring and reporting for Veeam workloads.

---

## Features

✅ Real-time backup job monitoring

✅ Backup success and failure tracking

✅ Backup duration and throughput analysis

✅ Repository capacity monitoring

✅ Restore point visibility

✅ Infrastructure health dashboards

✅ Customizable alerts and notifications

✅ Historical trend analysis

---

## Technology Stack

| Component | Version |
|------------|----------|
| Grafana | Latest Stable |
| Veeam Backup & Replication | v12.x |
| RHEL | 10.2 |
| Linux Firewall | firewalld |
| Data Source | Veeam / Prometheus |

---

## Environment Details

### Operating System

```bash
Red Hat Enterprise Linux 10.2
```

### Grafana Service

```bash
grafana-server
```

### Default Grafana URL

```text
http://<server-ip>:3000
```

Example:

```text
http://192.168.56.101:3000
```

---

## Installation

### Install Grafana

```bash
dnf install grafana -y
```

### Start Grafana Service

```bash
systemctl enable --now grafana-server
```

### Verify Service Status

```bash
systemctl status grafana-server
```

### Open Firewall Port

```bash
firewall-cmd --permanent --add-port=3000/tcp
firewall-cmd --reload
```

---

## Dashboard Metrics

The following metrics are monitored:

- Backup Job Status
- Backup Success Rate
- Failed Jobs
- Repository Capacity
- Restore Points
- Backup Throughput
- Session Duration
- Protected Workloads
- Backup Infrastructure Health

---

## Screenshots

### Grafana Dashboard

Place dashboard screenshots inside:

```text
screenshots/
```

Example:

```text
screenshots/dashboard-overview.png
screenshots/backup-status.png
screenshots/repository-utilization.png
```

---

## Project Structure

```text
grafana-veeam-monitoring/
│
├── README.md
├── dashboards/
│   ├── veeam-overview.json
│   ├── backup-health.json
│
├── screenshots/
│   ├── dashboard-overview.png
│
├── grafana/
│   └── grafana.ini
│
└── docs/
    └── installation-guide.md
```

---

## Useful Commands

### Check Grafana Logs

```bash
journalctl -u grafana-server -f
```

### Restart Grafana

```bash
systemctl restart grafana-server
```

### Verify Port

```bash
ss -tulpn | grep 3000
```

---

## Future Enhancements

- Email Alerting
- Microsoft Teams Integration
- ServiceNow Incident Integration
- Capacity Forecasting
- Multi-Site Backup Monitoring
- Veeam ONE Integration
- Prometheus Exporter Support

---

## Author

**Vipin Tanwar**

Backup Engineer - L2

Technologies:

- Veeam Backup & Replication
- Commvault
- Grafana
- Linux Administration
- Backup Monitoring
- Disaster Recovery

---

## License

This project is published for educational and demonstration purposes.

MIT License
