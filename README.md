# Ansible Role: ntpd

Installs NTP Server on RedHat/CentOS servers.

## Requirements

None.

## Role Variables

### `defaults/main.yml`

* `ntpd_ipv6_enable: true`
* `ntpd_logfile: /var/log/ntp.log`
* `ntpd_ntp_servers:`
    ```
      - ntp.fudan.edu.cn prefer
      - ntp.api.bz
      - 127.127.1.0  
    ```
* `ntpd_restrict_net: []`

## Dependencies

None.

## Example Playbook

    - hosts: servers
      vars:
        ntpd_restrict_net:
          - { net: "192.168.1.0", mask: "255.255.255.0" }
      roles:
         - ntpd

## License

MIT / BSD

## Author Information

z@zstack.net
