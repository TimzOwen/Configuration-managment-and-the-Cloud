
## Deploying Puppet

#### Applying Rules locally

    Puppet deployed on client-server architecture

    Also use as stand alone run from command line

Installing:

    sudo apt install puppet-master

    vim tools.pp ------> cmd to create a file where the rules are stored

    # ensure puppet is installed
    package{ 'htop' :
        ensure => present,
    }

    sudo puppet apply -v tools.pp -------> install htop

Catalog --> List of rules that are generated for once specific computer once the server has evaluated all   variables, conditionals and functions

#### Managing Resources in Relationships


Resource start with First later in Capital for reference from other resources

    class ntp{
        package { 'ntp':
            ensure=>latest,
        }
        file { '/etc/ntp.conf ':
            source => '/home/user/ntp.conf'
            replace => true
            require=> Package['ntp'],               # is capitilized
            notify=>Service['ntp],
            }
        service{ 'ntp'
            enable=> true,
            ensure=>running,
            require => File['/home/user/ntp.conf'],            # Also first later capitalized
        }
    }
    include ntp

#### Organizing your puppet module

Module--> Collection of manifest and associated data

start with 'init.pp'

tree modules/      ---------> checking tree module branching

include :: apache  ----> used to make sure init.pp is included

metadata.json --->contain additional data about module

lib --> holds new module developed and shared by others

[Puppet guide](https://puppet.com/docs/puppet/latest/style_guide.html)

[Puppet server package installers](https://puppet.com/docs/puppetserver/latest/install_from_packages.html)

