
Load balancing techniques:

    Round-Robin DNS-> asign one request to a server at a time

Sticky sessions:

    All requests from the same client always goes to the same backend server

perform server health check:

    incase of unhealthy server laodbalance does not send to sam server for requests

Access location and post to loadbalance:(Closes geographical load balancer)

    GeoDns
    
    GeoIP

CDNs (Content Delivery Networks):

    make up a network of physical hosts that are geographically located as close to the end users as possible

#### Change management:

Run tests:

    Unit test

    Integration test

Continous Integration (CI):

    Build and test our code everytime there is a change

Open source SI:

    Jenkins:

    Travis CI - by Github

Deploy changes:

    CD - Continous Deployment

    Build artifacts

Environmrnt:

    anything needed to run a service

        Test environment

        Production environment

A/B testing:

    some request are served using one set of code and configuration (A) and other requests are served using a different set of code and configuration B

#### Understanding Limitations

Rate Limits:

    revent one service from overloading the entire system

Utilization limit:

    Cap the total amount of a certain resource that you can provision

Use beta test to avoid system crash 

[Understanding VM CPU AND IP addresses ](https://cloud.google.com/compute/quotas#understanding_vm_cpu_and_ip_address_quotas)

[AWS service limits](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)

[Microsoft Azure service limits](https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#service-specific-limits)



### Monitoring and Alerting

Monitoring:

    Looking into the history and current status of a system

Monitoring systems:

    AWS CloudWatch
    
    Google Stack Driver

    Azure Metrics

Those that can be used across vendors

    prometheus

    DataDog

    Nagios

Pull model:

    monitoring infrastructure periodically queriesour service to get metric

Push model:

    our services needs to periodically connect to the system to send metrics

whitebox monitoring:

    collecting metrics from insdie a system like how much storage space the system is running and 
    how long it takes to process a request

    checks behaviour of a system from inside

blackbox monitoring:

    checks the behaviour of our system from outside


#### Getting notification alerts:

run job automation and  send status of a system:

    Linux --> cron

alert raising:

    pages:->those that need imeadiate attention
    
    non-urgent -> configured to create bugs/tickets for IT specialist
    

#### Service Level Object

Service-Level Objectives (SLOs):

    Pre-established performace goals for a specific service

Service Level Agreement (SLAs):

    a commitment between a provider and a client

#### Basic  Monitoring in GCP

using stackdriver:

has alerting policy

[datadog monitoring and data collection](https://www.datadoghq.com/blog/monitoring-101-collecting-data/)

[Introduction to metrics monitoring and alerting](https://www.digitalocean.com/community/tutorials/an-introduction-to-metrics-monitoring-and-alerting)

[High availablity](https://en.wikipedia.org/wiki/High_availability)

[SRE books refernces](https://landing.google.com/sre/books/)



### Troubleshooting and Debugging

#### off-premise troubleshoot

incase of failure due to upgrade, Rollback the changes

Mount disks of working and not working

isolate issues and problems 

or call the servce provider

run logs in the cloud server

#### Identiyfing root cause of failure

problems on provider side might be due to geographical regions

migrate to different regions 

resource issues, try running the services on a more powerful VM

do rollbacks for pieces that have recentlt changed

#### Recovering from failure

have backups and well documented recovery plan

keep secondary instances of your running apps

have different cloud providers

#### Debugging problems in the cloud readme

[Troubleshooting instances](https://cloud.google.com/compute/docs/troubleshooting/troubleshooting-instances)

[Virtual Machines Instances in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/)

[Amazon troubleshooting instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-troubleshoot.html)




