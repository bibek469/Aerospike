Role Name
=========

This role will launch the aerossipkes cluster in debian and redhat family Linux environment.


Role Variables
--------------
All the role variable is mentioned in the defults folder.

```
aerospike_boot_enabled: true
aerospike_source_directory: "/usr/local/src"
aerospike_log_directory: "/var/log/aerospike"
aerospike_config_destination: "/etc/aerospike/aerospike.conf"
amc_version: "4.0.27"

# Aerospike configuration Vars
aerospike_cluster_size: 1
aerospike_service_threads: 4
aerospike_transaction_queues: 4
aerospike_transaction_threads: 4

# Heartbeat configuration Vars
aerospike_mesh_seed_addresses:
  - 127.0.0.1

## Namespace configuration Vars
aerospike_namespaces:
  - name: default
```

Example Playbook
----------------

Including an example of how to run the playbook 

```
- hosts: all
   gather_facts: true 
   become : true
   remote_user: root 
   roles:
    - aerospikes
```

License
-------

MIT License

Author Information
------------------

This role is maintained by @bibek469
