# openstack-ansible-os_horizon_metadatasearch

## Important Variables To Set

The following variables must be set for your environment before running the playbook.

```yaml
# Found in defaults/main.yml
# For Liberty this should be stable/liberty (that is default)
# stable/mitaka is also supported.
horizon_metadatasearch_git_install_branch: ""
# This must match the OSA version
openstack_release: 12.0.14
# This will only need to be changed if for some reason you are not using a venv
horizon_venv_bin: "/openstack/venvs/horizon-{{ openstack_release }}/bin"
# This should not need to be changed but in some cases the package might end up in dist-packages
horizon_venv_lib_dir: "{{ horizon_venv_bin | dirname }}/lib/python2.7/site-packages"

# Found in group_vars/all.yml
# This is the location where the rpc repository was checked out
osa_roles_path: /opt/openstack-ansible/playbooks/roles
osa_inventory_path: /opt/openstack-ansible/playbooks
```

## Usage

```bash
openstack-ansible os_horizon_metadatasearch.yml
```
