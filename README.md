Resource
==========

### Nbe resource tool

### Usage:

    $ res [OPTIONS] COMMAND [ARGS]...

#### Add Influxdb:

    $ res add_influxdb marco --length 9 --admin false

Options are:

* `--length`, `-l`: the length of the password
* `--admin`, `-a`: admin for user

#### Add Sentry:

    $ res add_sentry marco --platform python --namespace platform

Options are:

* `--platform`, `-p`: the language of the project
* `--namespace`, `-n`: the group in sentry
    
#### Nginx Reload:

    $ res nginx_reload /tmp/marco.conf /etc/nginx/conf.d/marco.conf --nginx-list nginx.sample --key-file armin.pub --user armin

Arguments are:

* `local_path`: local nginx conf path 
* `remote_path`: remote nginx conf path, e.g. /etc/nginx/conf.d/marco.conf

Options are:

* `--nginx-list`, `-l`: file that contains nginx server list
* `--key-file`, `-k`: SSH public key
* `--user`, `-u`: user to login

#### Command Options are:

* `--config-path`: path for root config in etcd, which stores mysql/influxdb/sentry key information 
