# ansible-role-win-features

Role to add, remove Windows Features

## Table of content

- [Default Variables](#default-variables)
  - [win_feature_list_add](#win_feature_list_add)
  - [win_feature_list_remove](#win_feature_list_remove)
  - [win_feature_post_reboot_delay](#win_feature_post_reboot_delay)
  - [win_feature_pre_reboot_delay](#win_feature_pre_reboot_delay)
  - [win_feature_reboot_when_required](#win_feature_reboot_when_required)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### win_feature_list_add

list of windows features to be installed

#### Default value

```YAML
win_feature_list_add: []
```

#### Example usage

```YAML
win_feature_list_add
  - name: "AD-Domain-Services"
    include_management_tools: true
    include_sub_features: true
  - name: "FS-FileServer"
```

### win_feature_list_remove

list of windows features to be uninstalled

#### Default value

```YAML
win_feature_list_remove: []
```

#### Example usage

```YAML
win_feature_list_remove
  - "AD-Domain-Services"
  - "FS-FileServer"
```

### win_feature_post_reboot_delay

Wait number of seconds after reboot to continue

#### Default value

```YAML
win_feature_post_reboot_delay: 30
```

### win_feature_pre_reboot_delay

Wait number of seconds before rebooting

#### Default value

```YAML
win_feature_pre_reboot_delay: 5
```

### win_feature_reboot_when_required

Automatically reboot when a Windows feature requires it

#### Default value

```YAML
win_feature_reboot_when_required: true
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
