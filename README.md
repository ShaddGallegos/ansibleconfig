# Ansible Config

**Created:** June 2024

## Synopsis

A comprehensive Ansible Automation Platform configuration and setup toolkit providing automated installation, configuration, and upgrade capabilities for Ansible AAP environments with Podman containerized deployments.

## Supported Operating Systems

- Red Hat Enterprise Linux 8/9
- CentOS Stream 8/9
- Rocky Linux 8/9
- AlmaLinux 8/9
- Fedora 35+

## Quick Usage

### Basic Configuration Setup

```bash
# Run the main configuration playbook
ansible-playbook config_ansible.yml

# Use the refactored configuration version
ansible-playbook config_ansible_refactored.yml

# Set up AAP environment
ansible-playbook aap_env_setup_playbook.yml
```

### AAP Bundle Management

```bash
# Download AAP bundle
ansible-playbook download_aap_bundle.yml

# Run all configuration tasks
ansible-playbook run_all.yml

# Execute site-wide configuration
ansible-playbook site.yml
```

### Requirements and Dependencies

```bash
# Install required collections and roles
ansible-galaxy install -r requirements.yml

# Check system requirements
ansible-playbook requirements_check.yml
```

### Available Configurations

1. **Basic Ansible Configuration** (config_ansible.yml)
2. **Advanced AAP Setup** (aap_env_setup_playbook.yml)
3. **Bundle Download and Setup** (download_aap_bundle.yml)
4. **Requirements Management** (requirements.yml, requirements_check.yml)
5. **Complete Site Configuration** (site.yml)

## Features and Capabilities

### Core Features

- Automated Ansible Automation Platform installation and configuration
- Containerized deployment with Podman integration
- Version upgrade management (2.4 to 2.5)
- Environment setup and validation
- Requirements checking and dependency management

### AAP Configuration

- Controller installation and configuration
- Hub installation and setup
- EDA (Event-Driven Ansible) configuration
- Gateway and proxy setup
- SSL certificate management
- Database configuration and optimization

### Containerized Deployment

- Podman container management
- Container image handling
- Network configuration for containers
- Volume and storage management
- Service orchestration
- Container security configuration

### Upgrade Management

- Version compatibility checking
- Backup creation before upgrades
- Step-by-step upgrade processes
- Configuration migration
- Post-upgrade validation
- Rollback procedures

### Environment Management

- Multi-environment support
- Inventory management with growth support
- Role-based configuration
- Variable management and templating
- Secret and credential management

## Documentation Resources

The project includes comprehensive documentation:

- **Ansible_AAP_2.4_to_2.5_Upgrade_Guide.docx** - Detailed upgrade procedures
- **Ansible_AAP_Podman_Config.docx** - Containerized deployment guide

## Limitations

- Requires Red Hat subscription for AAP components
- Minimum system requirements: 16GB RAM, 40GB storage
- Network connectivity required for bundle downloads
- Container runtime (Podman) required for deployment
- May require firewall configuration changes
- Some features require specific AAP version compatibility

## Getting Help

### Documentation

- Review the included Word documents for detailed procedures
- Check roles/ directory for specific role documentation
- Examine playbook variables for configuration options
- Review inventory files for environment setup examples

### Support Resources

- Red Hat Ansible Automation Platform documentation
- Podman documentation for container management
- Check logs and output for troubleshooting information
- Use ansible-playbook --check for dry-run validation

### Common Issues

- System requirements: Ensure sufficient resources for AAP deployment
- Network connectivity: Verify access to Red Hat repositories
- Container runtime: Ensure Podman is properly installed and configured
- Subscription access: Verify Red Hat subscription and entitlements
- Firewall configuration: Check required port accessibility
- Storage space: Monitor disk usage during installation

### Upgrade Considerations

- Always backup existing configurations before upgrades
- Test upgrades in development environment first
- Review compatibility matrices for version support
- Plan for service downtime during upgrade process
- Validate all services after upgrade completion

## Legal Disclaimer

This software is provided "as is" without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

Use this software at your own risk. No warranty is implied or provided.

**By Shadd**
