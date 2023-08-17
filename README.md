# spreadcat.vscodium

Ansible role for inststalling [VScodium](https://vscodium.com/) and Extensions.

## Requirements

* The role requires `gathered_facts: true` to be set.

## Role Variables

See `./defaults/main.yml` for a detailed explanation on how to use the variables.

```yaml
vscodium_extensions: []
```

* List of extensions that will be installed.

## Other variables

```yaml
vscodium_apt_gpg_key: ""
```

* URL to the GPG key for the APT repository.

```yaml
vscodium_rpm_gpg_key: ""
```

* URL to the GPG key for the RPM repository.

```yaml
vscodium_package_name: ""
```

* String with the name of the package to install.

```yaml
vscodium_package_state: ""
```

* String with the package state.

```yaml
vscodium_user_home: ""
```

* Homedirectory of the user who should use VSCodium.

```yaml
vscodium_user_name: ""

* Username for which to set permissions and extensions.

```

## Dependencies

None

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
---
- hosts: all
  gather_facts: true
  roles:
     - role: spreadcat.vscodium
       vars:
         vscodium_extensions:
           - vscodevim.vim
```

## License

BSD

## Author Information

This role is written an maintained by DBV.
