## [![Nabla](https://debops.org/images/debops-small.png)](https://github.com/AlbanAndrieu) roles/alban_andrieu_synergy

This file was generated by Ansigenome. Do not edit this file directly but instead have a look at the files in the ./meta/ directory.

[![License](http://img.shields.io/:license-apache-blue.svg?style=flat-square)](http://www.apache.org/licenses/LICENSE-2.0.html)
[![Travis CI](https://img.shields.io/travis/AlbanAndrieu/ansible-synergy.svg?style=flat)](https://travis-ci.org/AlbanAndrieu/ansible-synergy)
[![Branch](http://img.shields.io/github/tag/AlbanAndrieu/ansible-synergy.svg?style=flat-square)](https://github.com/AlbanAndrieu/ansible-synergy/tree/master)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-alban.andrieu.synergy-660198.svg?style=flat)](https://galaxy.ansible.com/alban.andrieu/synergy)
[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)

This ``Simple`` role allows you to install [synergy](http://fr.wikipedia.org/wiki/Synergy_(logiciel)) service
which can be share your keyboard and mouse across computer.

Official website is [synergy](https://symless.com/synergy/downloads)

### Installation

This role requires at least Ansible `v2.3.0.0`. To install it, run:

Using `ansible-galaxy`:
```shell
$ ansible-galaxy install alban.andrieu.synergy
```

Using `arm` ([Ansible Role Manager](https://github.com/mirskytech/ansible-role-manager/)):
```shell
$ arm install alban.andrieu.synergy
```

Using `git`:
```shell
$ git clone https://github.com/AlbanAndrieu/ansible-synergy.git
```

### Role variables

List of default variables available in the inventory:

```YAML
synergy_enabled: yes                       # Enable module

#synergy_listen_ip: "127.0.0.1"
#synergy_port: "8090"

#user: 'albandri' #please override me
user: "{{ lookup('env','USER') }}"
synergy_owner: "{{ user }}"
synergy_group: "{{ synergy_owner }}"
#home: '~' #please override me
home: "{{ lookup('env','HOME') }}"
synergy_owner_home: "{{ home }}"
#synergy_home: "{{ synergy_owner_home }}.synergy"
synergy_base_dir: "/usr/local/synergy"
synergy_dir_tmp: "/tmp" # or override with "{{ tempdir.stdout }} in order to have be sure to download the file"
synergy_user_state: present
#synergy_pkg_state: present

## Most likely you dont need to edit
#todo synergy_service_enabled   : 'yes'
synergy_major: "1"
#synergy_minor: "8.2"
synergy_minor: "4.18"
#synergy_number: "rc1-f4510c7"
synergy_number: "r2250"
synergy_architecture: "Linux-x86_64"
synergy_version: "{{synergy_major}}.{{synergy_minor}}-{{synergy_number}}-{{synergy_architecture}}"
synergy_package_deb: "synergy-{{synergy_version}}.deb"
synergy_name: "synergy-{{synergy_major}}.{{synergy_minor}}"
#synergy_archive_extracted: "synergy_{{synergy_package_deb}}"
synergy_archive_extracted: "{{synergy_package_deb}}"
synergy_archive: "{{synergy_archive_extracted}}"
#synergy_url: "https://symless.com/files/nightly/{{synergy_package_deb}}"
synergy_url: "http://symless.com/download/free/{{synergy_package_deb}}"
#synergy_home_dir: "{{synergy_base_dir}}/{{synergy_name}}"
synergy_server: "127.0.0.1"
synergy_configuration: '.synergy.conf'
synergy_server_main: "nabla-main"
synergy_server_desktop: "nabla-desktop"
synergy_server_laptop: "nabla-laptop"

# Place to get apt repository key
apt_key_url: https://symless.com/gpg
# apt repository key signature
apt_key_sig: "Free download"
```


### Detailed usage guide

Describe how to use in more detail...

### Testing
```shell
$ ansible-galaxy install alban.andrieu.synergy
$ vagrant up
```

### Contributing

The [issue tracker](https://github.com/AlbanAndrieu/ansible-synergy/issues) is the preferred channel for bug reports, features requests and submitting pull requests.

For pull requests, editor preferences are available in the [editor config](.editorconfig) for easy use in common text editors. Read more and download plugins at <http://editorconfig.org>.

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests and examples for any new or changed functionality.

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

### Authors and license

`roles/alban_andrieu_synergy` role was written by:

- [Alban Andrieu](fr.linkedin.com/in/nabla/) | [e-mail](mailto:alban.andrieu@free.fr) | [Twitter](https://twitter.com/AlbanAndrieu) | [GitHub](https://github.com/AlbanAndrieu)

License
-------

- License: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-%28gpl-3%29)

### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/AlbanAndrieu/ansible-synergy/issues)!

***

This role is part of the [Nabla](https://github.com/AlbanAndrieu) project.
README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).

***

Alban Andrieu

[linkedin](fr.linkedin.com/in/nabla/)
