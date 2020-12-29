
## Automating with Configuration Management

#### configuration management with the Cloud

Scale:

    Achieving larger impact with same amount of effort

Configuration Management:

    using a management system to manage all configuration

Configuration Tools:

    Local management of servers and computer tools:

    Puppet

    Chef

    Ansible

    CFEngine

    Cloud Management tools include:

    Amazon EC2

    Microsoft Azure

    Google cloud platform

    Platform specific tools:

    SCCM

    Group policy-->windows

#### Infrastructure as code

IaC-->The paradigm of storing all configuration for managed devices in version controlled files.

Managing IaC provides systems that are :

    Consistent

    Versioned

    Reliable

    Repeatable

### Managing with PUppet

    its cross platform

    Open source

    Deployed using s client-server architecture

        client-puppet agent

        server-puppet master

Package management:

    Linux OS

        APT

        YUM

        DNF

    MAC OS

        Apple provider

        MAcPorts

    Windows:

        Locate the installer
        
        chocolatey

Puppet Resources

    Resources are the basic unit for modelling configuration that we want to manage

puppet code structure

    class sudo{
        package{ 'sudo':
        ensure=>present,
        }
    }

    class sysctl{
        # make sure the directory exists,some directories don't have it
        file{ '/etc/sysctl.d':
        ensure =>directory,
        }
    }

    class timezone{
        file{ '/etc/timezone':
         ensure => file,
         content => "UTC\n"
         replace => true
        }
    }

#### Puppet classes

Multiple classes

    class ntp{
        package{ 'ntp':
        ensure=>latest
        }
        file{ '/etc/ntp.conf':
            source=>'puppet:///modules/ntp/ntp.conf'
            replace=>true
        }
        service{ 'ntp':
            enable=>true
            ensure=>running
        }
    }

Multiple class 2 syntax

    class AutoConfig {
        package { 'Executable':
            ensure => latest,
            }
        file { 'executable.cfg':
            source => 'puppet:///modules/executable/Autoconfig/executable.cfg'
            replace => true,
            }
        service { 'executable.exe':
            enable  => true,
            ensure  => running,
            }
        }


[Checkout the latest Puppet and syntax](https://puppet.com/docs/puppet/latest/lang_resources.html)

[Deploy configuration across windows](https://puppet.com/blog/deploy-packages-across-your-windows-estate-with-bolt-and-chocolatey/)



