
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
