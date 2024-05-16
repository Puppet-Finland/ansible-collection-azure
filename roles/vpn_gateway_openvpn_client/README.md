# vpn_gateway_openvpn_client

An Ansible role to configure Azure VPN Gateway OpenVPN clients. Includes
support for adding the VPN IP to Azure Private DNS.

## Requirements

Currently this role only supports RHEL 9 and derivatives.

## Dependencies

This role depends on the following external collections:

* ansible.posix
* community.general

## Role Variables

Role variables are listed in [tasks/main.yml](tasks/main.yml).

## License

BSD-2-Clause
