# Ansible role `bertvv.pulp`

An Ansible role for setting up and managint Pulp. Specifically, the responsibilities of this role are to:

- Install Pulp and its dependencies
- Manage Pulp configuration

**Remark** that this role is far from production ready. At this time, it will automate the installation, as described in the [Pulp documentation](https://pulp-user-guide.readthedocs.org/en/2.5-release/installation.html), up to the heading "Admin client".

## Requirements

No specific requirements

## Role Variables

You can set all variables in the [`/etc/pulp/server.conf`](https://github.com/pulp/pulp/blob/master/server/etc/pulp/server.conf) configuration file by adding prefix `pulp`. E.g. to change setting `server_name`, set a variable `pulp_server_name`. When not set, the default values will be applied.

## Dependencies

No dependencies.

## Example Playbook

See the [test playbook](tests/test.yml)

## Testing

The `tests` directory contains tests for this role in the form of a Vagrant environment. The directory `tests/roles/pulp` is a symbolic link that should point to the root of this project in order to work. To create it, do

```ShellSession
$ cd tests/
$ mkdir roles
$ ln -frs ../../PROJECT_DIR roles/pulp
```

You may want to change the base box into one that you like. The current one is based on Box-Cutter's [CentOS Packer template](https://github.com/boxcutter/centos).

The playbook [`test.yml`](tests/test.yml) applies the role to a VM, setting role variables.

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Preferably, create a topic branch and when submitting, squash your commits into one (with a descriptive message).

## License

BSD

## Author Information

Bert Van Vreckem (bert.vanvreckem@gmail.com)

