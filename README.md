# Ansible Role macOS Hostname

A simple Ansible role to set HostName, LocalHostName, and ComputerName on macOS.

## Requirements

No special requirements.

## Role Variables

### Notes

- The output column of the following table assumes the role is being run on a MacBookPro 14.1.
- The properties `HostName`, `LocalHostName`, and `ComputerName` referred to in the table are keywords used with the `scutil` command on macOS.

| Variable name      | Default value | Output | Description |
|--------------------|---------------|--------|-------------|
| `mh_domain`        | `example.com` | -      | Network domain for use in automatic HostName. |
| `mh_hostname`      | `auto`        | `macbookpro14-1.example.com` | The HostName to set or `auto` (see "Output" column). |
| `mh_localhostname` | `auto`        | `MacBookPro14-1` | The LocalHostName to set or `auto` (see "Output" column). |
| `mh_computername`  | `auto`        | `MacBookPro14-1` | The ComputerName to set or `auto` (see "Output" column). |

## Example Playbook

    - hosts: servers
      roles:
         - role: ansible-role-macos-hostname

## License

GPLv3

## Author Information

Christopher Torgalson
