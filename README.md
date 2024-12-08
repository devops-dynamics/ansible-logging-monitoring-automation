# Ansible Logging & Monitoring Automation

## Overview
This project contains Ansible playbooks and roles for automated deployment and configuration of various logging and monitoring solutions including ELK Stack, EFK Stack, Prometheus/Grafana, Graylog, and Splunk.

## Prerequisites
- Ansible 2.9 or higher
- Python 3.x
- SSH access to target hosts
- Sufficient permissions to install and configure monitoring tools

## Directory Structure
```
ansible-logging-monitoring-automation/
├── ansible.cfg                # Ansible configuration
├── inventory/                 # Environment-specific inventories
├── playbooks/                 # Main playbooks
├── roles/                     # Individual role definitions
├── vars/                      # Variable definitions
└── docs/                      # Documentation
```

## Quick Start
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd ansible-logging-monitoring-automation
   ```

2. Update inventory:
   ```bash
   # Edit the appropriate inventory file
   vim inventory/dev.yml
   ```

3. Configure variables:
   ```bash
   # Update global variables
   vim vars/global.yml
   ```

4. Run playbook:
   ```bash
   ansible-playbook -i inventory/dev.yml playbooks/elk_stack.yml
   ```

## Available Playbooks
- `elk_stack.yml`: Deploys ELK (Elasticsearch, Logstash, Kibana) stack
- `efk_stack.yml`: Deploys EFK (Elasticsearch, Fluentd, Kibana) stack
- `prometheus_grafana.yml`: Deploys Prometheus and Grafana
- `graylog.yml`: Deploys Graylog
- `splunk.yml`: Deploys Splunk

## Role Documentation
Detailed documentation for each role is available in the `docs/role_guides/` directory.

## Testing
```bash
# Run molecule tests
molecule test

# Run integration tests
./tests/integration/run_tests.sh
```

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Troubleshooting
See `docs/troubleshooting.md` for common issues and solutions.
