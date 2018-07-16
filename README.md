telegraf
=========

This role attempts to install and configure telegraf, a monitoring agent written in Go.

Requirements
------------

* Tested on Ansible 2.6 or higher.

Role Variables
--------------

#### `telegraf_agent_output`
Output target for data gathered by telegraf. See defaults/main.yml for an example.

#### `telegraf_plugins`
Additional input plugins to be configured.
This is a list containing unnamed dictionaries with the following keys:

  - `plugin` -- name of the plugin
  - `config` -- list of lines that will be put in the config file for the plugin

See Example Playbook below.

Dependencies
------------

None.

Example Playbook
----------------

This example installs an additional input plugin `ping` with a configuration option.

    - hosts: servers
      tasks:
        - import_role:
            name: jniewt.telegraf
          vars:
            telegraf_plugins:
              - plugin: ping
                config:
                  - 'urls = ["www.google.com", "1.2.3.4"] # required'

License
-------

MIT

Author Information
------------------

jniewt | [jniewt@gmail.com](jniewt@gmail.com)
