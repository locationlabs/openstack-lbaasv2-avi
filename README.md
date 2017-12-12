# TripleO Avi Integration

This Ansible role installs Avi's
* LBaaS V2 driver for Neutron
* Heat resources
* Optional dashboard Integration

# Requirements

It is expected that the Avi controllers and their OpenStack integration has
already been completed, see this [heat template][avi-heat] as an example. Avi's
LBaaS driver files must first be obtained from their customer portal and
extracted on the ansible host.

Currently this role was developed to target the Ocata release of TripleO and Avi
version 17.1.x.

By default, this role will configure Avi-OpenStack integration in OpenStack
managed mode, where Neutron handles LBaaS API requests and the dashboard. The
role variables can then be used to:
* Enable heat resources for Avi managed LBaaS
* Replace LBaaS dashboard with Avi's

**NOTE:** While it is possible to use both Neutron LBaaS V2 API and Avi's API
within the same OpenStack cluster, do not mix these approaches within a project.

# Role Variables

Required:
* `avi_driver_package_dir`: Path to the unarchived Avi driver package
 * Example: `~/Downloads/avi/openstack_lbplugin`
* `avi_controller_ip`: IP address to the Avi controller
* `avi_controller_admin_password`: Admin password
* `avi_heat_pip_package`
* `avi_dashboard_pip_package`
* `avi_dashboard_code_specific`

Optional:
* `avi_controller_admin_user`: Admin user name, default: admin
* `avi_controller_cloud`: Cloud name, default: Default-Cloud

# Dependencies

None

# License

Apache License 2.0

# Author Information

Location Labs by Avast

[avi-heat]:https://github.com/avinetworks/devops/tree/master/openstack/heat_templates
