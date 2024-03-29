---

# ansible-isp-speedtest

<img src="https://www.ansible.com/hubfs/2016_Images/Assets/Ansible-Mark-Large-RGB-Pool.png?hsLang=en-us" width="10%" height="10%" alt="Ansible logo" align="right"/>

[![License](https://img.shields.io/github/license/autobuilder/ansible-isp-speedtest)](https://opensource.org/licenses/MIT)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/autobuilder/ansible-isp-speedtest/issues)
[![Build Status](https://travis-ci.org/autobuilder/ansible-isp-speedtest.svg?branch=master)](https://github.com/autobuilder/ansible-isp-speedtest)

![Platform](https://img.shields.io/badge/platform-ubuntu-dd4814.svg?style=flat) 
![Platform](https://img.shields.io/badge/platform-debian-a80030.svg?style=flat) 
![Platform](https://img.shields.io/badge/platform-centos-932279.svg?style=flat)

Ansible role for install [speedtest-cli][speedtestcli] using package manager or pip.

Speedtest-cli outputs will be placed on dedicated directory as json files.

---

### Requirements:

* Outbound network connectivity

### Dependencies:

* None

---

### Variables:

| Variable Name | Default Vaule                             | Description               |
|:--------------|:------------------------------------------|:--------------------------|
|date           | ```Excution Date```                       | Excution date             |
|time           | ```Excution Time```                       | Excution time             |
|log_name       | ```speedtest-{{ date }}-{{ time }}.log``` | Logs name                 |
|log_path       | ```/tmp/speed_test_cli_logs```            | Logs path                 |
|output_type    | ```json```                                | Speedtest-cli output type |
|use_get_url    | ```true```                                | Download  Speedtest-cli   |

---

### Example Playbook:

```yaml
- hosts: servers
  roles:
    - ansible-isp-speedtest
```

---

### Test Automation:

Automated tests run with [Kitchen-CI][kitchenci] and [Ansible Lint][ansiblelint].
Tested platforms are the below linux-based distros:

* Ubuntu 16.04
* Ubuntu 18.04
* Debian 9
* Centos 7

---

#### License:

This project is made available under the terms of the [MIT][mit].

See the [LICENSE][license] file that accompanies this distribution for the full text of the license.

---

#### Author Information:

[AutoBuilder][autobuilder]

[autobuilder]: https://github.com/autobuilder
[mit]: https://opensource.org/licenses/MIT
[license]: https://github.com/autobuilder/ansible-isp-speedtest/blob/master/LICENSE
[ansiblelint]: https://docs.ansible.com/ansible-lint/
[kitchenci]: https://kitchen.ci
[speedtestcli]: https://github.com/sivel/speedtest-cli