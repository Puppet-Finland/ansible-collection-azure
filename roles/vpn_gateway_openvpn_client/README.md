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

This role accepts the following variables:

- *vpn_gateway_openvpn_client_name:* Basename for the VPN client configuration
- *vpn_gateway_openvpn_client_remote:* DNS name of the Azure VPN Gateway instance
- *vpn_gateway_openvpn_client_x509_name:* Name of the Azure VPN Gateway - seems to be the hostname part of DNS name
- *vpn_gateway_openvpn_client_tenant:* Azure tenant name (e.g. *acme.org*) for Azure Private DNS
- *vpn_gateway_openvpn_client_rg:* Resource group for Azure Private DNS
- *vpn_gateway_openvpn_client_zone_name:* Zone name for Azure Private DNS
- *vpn_gateway_openvpn_client_sp_username:* Azure Service Principal username (used to authenticate to Azure)
- *vpn_gateway_openvpn_client_sp_password:* Azure Service Principal password (used to authenticate to Azure)
- *vpn_gateway_openvpn_client_ca:* Azure VPN Gateway's CA certificate
- *vpn_gateway_openvpn_client_tls_key:* OpenVPN client's TLS auth key
- *vpn_gateway_openvpn_client_cert:* OpenVPN client's certificate
- *vpn_gateway_openvpn_client_key:* OpenVPN client's private key

Many of these parameters are required for
[update-azure-private-dns.sh](https://github.com/Puppet-Finland/openvpn-update-azure-private-dns),
a script that is responsible for adding the VPN client's IP address to Azure Private DNS.

## License

BSD-2-Clause
