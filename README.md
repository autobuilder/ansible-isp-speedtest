

# ansible-isp-speedtest


Ansible role for install [speedtest-cli][speedtestcli] using package manager or pip,
testspeed-cli outputs will be placed on dedicated directory as json files.

Currently this works on Debian and RedHat based linux systems.
**Tested platforms are:**

* Ubuntu 18.04



## Requirements

* Outbound network connectivity



## Dependencies

None



## Variables

| Variable Name | Default Vaule                             | Description               |
|:--------------|:------------------------------------------|:--------------------------|
|date           | ```Excution Date```                       | Excution date             |
|time           | ```Excution Time```                       | Excution time             |
|log_name       | ```speedtest-{{ date }}-{{ time }}.log``` | Logs name                 |
|log_path       | ```/tmp/speed_test_cli_logs```            | Logs path                 |
|output_type    | ```--json```                              | TestSpeed-cli output type |



## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
    - hosts: servers
      roles:
        - ansible-isp-speedtest
```


## Testing

This playbook uses [Kitchen][kitchenci] for CI and local testing.



## License

**This project is made available under the terms of the [Apache-2.0][apache2]. See the [LICENSE][license] file that accompanies this distribution for the full text of the license.**



## Author Information

**[Lior Lifshitz][liorlifshitz]**



[speedtestcli]: https://github.com/sivel/speedtest-cli
[kitchenci]: https://kitchen.ci
[apache2]: https://www.apache.org/licenses/LICENSE-2.0.html
[license]: https://github.com/liorlifshitz/ansible-isp-speedtest/blob/master/LICENSE
[liorlifshitz]: https://github.com/liorlifshitz
