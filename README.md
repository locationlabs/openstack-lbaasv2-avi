# TripleO Avi LB Plugin role

This Ansible role installs the Avi LBaaS V2 driver for Neutron.

# Requirements

It is expected that the Avi controllers and their OpenStack integration has
already been completed, and the driver files have been downloaded from the
customer portal.

Currently this role was developed to target the Ocata release of TripleO and Avi
version 17.1.x.

# Role Variables

* `avi_driver_package_dir`: Path to the unarchived Avi driver package
 * Example: `~/Downloads/avi/openstack_lbplugin`
* `avi_controller_ip`: IP address to the Avi controller
* `avi_controller_admin_user`: Admin user name, default: admin
* `avi_controller_admin_password`: Admin password
* `avi_controller_cloud`: Cloud name, default: Default-Cloud

# Dependencies

None

# License

MIT

# Author Information

Location Labs by Avast
