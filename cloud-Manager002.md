
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


