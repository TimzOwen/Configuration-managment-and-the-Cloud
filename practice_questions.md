


## Interview quick recap quizes:

What is IaC (Infrastructure as Code)

    Using a version control system to deploy and manage node configurations

What is the principle called when you think of networked machines as interchangeable resources instead of individual machines

    Treating computers like "cattle instead of pets"

What benefits can we gain by using automation to manage our configuration

    Reliability

    consistency

    scalability

state some of the best tools used for configuration management

    Ansible

    CFEngiene

    Chef

    Puppet

Whats the most basic modeling unit in a puppet

    resource

What is the advantage of grouping related resources into a single class

    To ensure efficiency and convenience for future changes

What is the benefit of grouping resources into classes when using Puppet

    Configuration management is simplified

What defines which provider will be used for a particular resource

    Puppet assigns providers based on the resource type and data collected from the system.

In Puppet’s file resource type, which attribute overwrites content that already exists

    Replace

A Puppet agent inspects /etc/conf.d, determines the OS to be Gentoo Linux, then activates the Portage package manager. What is the provider in this scenario

    Portage

How is a declarative language different from a procedural language

    A declarative language defines the goal; a procedural language defines the steps to achieve a goal

Puppet facts are stored in hashes. If we wanted to use a conditional statement to perform a specific action based on a fact value, what symbol must precede the facts variable for the Puppet DSL to recognize it

    $

What does it mean that Puppet is stateless

    There is no state being kept between runs of the agent

What does the "test and repair" paradigm mean in practice

    We should only take actions when testing determines they need to be done to reach the requested state

Where, in Puppet syntax, are the attributes of a resource found

    Inside the curly braces after the resource type
