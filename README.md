## Tunning postgresql is based on https://pgtune.leopard.in.ua/

#### Example playbook

```yaml
- hosts: example.host
  roles:
    - role: roles/pgtune
      pgtune_postgresql_version: 11
      pgtune_bind_ip: 0.0.0.0
      pgtune_bind_port: 5432
      pgtune_max_connection: 100
      pgtune_type_app: "oltp"
      pgtune_disks_type: "SSD"
```

*pgtune_postgresql_version* is the version of the postgresql.

*pgtune_bind_ip* is bind ip on host.

*pgtune_bind_port* is bind port on host.

*pgtune_max_connection* is count connection to database.

*pgtune_type_app* is the type of the application. Total five type applications: 
- **web** is the web applications
- **oltp** is the online transaction processing systems
- **dw** is the data warehouses
- **desktop** is the desktop applications
- **mixed** is the mixed type of applications

*pgtune_disks_type* is the type of disks. Total two type disks:
- **SSD** is the solid-state drive
- **HDD** is the hard (magnetic) disk drive