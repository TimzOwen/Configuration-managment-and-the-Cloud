## Cloud Automation

#### Cloud services

services:

    SaaS (Software as a service):->When a cloud provider delivers an entire progam/application to a user

    PaaS (Platform as a Service):->cloud provider offering preconfigured platform to a customer

    IaaS (Infrastructure as a service):->Cloud provider only provieds the bare-bones computing experience
        Amazon's EC2
        Google Cloud Compute Engiene
        Microsfot Azure 

#### Scaling in the Cloud


Capacity:

    How much the service can deliver

QPS:

    server reponse in one second to certain number of queiries 

scaling:

    Horizontally --> adding morenodes to the main server

    Vertically --> Making nodes bigger (CPU, Memory, Disk space)

    Automatically -->uses metrics to automatically increase/decrease the capacity of a system

    Manually--changes controlled by humans instead of software

#### Evaluating the Cloud

security certificate:

    SOC
    
    ISO 27001

Choose the right service to be offered to by the cloud  provider

#### Migrating to the Cloud

lift and shift:

    moving servers from premise one to another

PaaS: give ofer management of an application to the cloud provider

web application platform:

    Amazon Elastic BeanStalk

    Microsoft App Service

    Google App Engiene

Containers:

    Applications that are packaged together with their configurations and dependecies

Clouds:

    public clouds -- >services provided to you by third-party

    private clouds -->a company owns the services and rest of infrastructure wether onsite/remote

    hybrid clouds--> both private and public

    Multi-clouds -- Mixture of public and/or private clouds across venders


### Managing instances in the CLoud


#### Spinning up VMs in the cloud

Options to choose when selecting VMS:

    Name
    region & Zone
    bootdisk

Reference images:

    Store the contents of a machine in a reusable format

Templating:

    The process of capturing all of the system configuration to let us create VMs in a repeatable way

Disk image:

    a snapshot of virtual machine's disk at a given point name
    
    

#### Creating a New VM using GCP web UI

Used google GCP.

curl wttr.in --> cmd used to check the weather on the command line

#### Customizing VMs in GCP

steps:

    connect to ssh of the VM

    clone the repo you want ot deploy

    run the ./app as sudo

    check the ip before the shh connection

    locate the services and run them as cloud

    check for running services --> (ps as | grep hello)

#### Templating a customized VM

steps:

    stop the VM

    click machine name

    chekc boot disk name

    Then create Image/template 

    Follow the command cand crate from the template

#### Creating from GCP cmd

    gcloud init ---> authenticates google to VM Gcloud

    selecect default project

    select region and zone

    gcloud compute instances create --source-instance-template webserver-template ws1 ws2 ws3 ws4 ws5 

[Compute Linux GCP](https://cloud.google.com/compute/docs/quickstart-linux)

[create VM from instance template](https://cloud.google.com/compute/docs/instances/create-vm-from-instance-template)

[Google sdk docs](https://cloud.google.com/sdk/docs)



### Automating CLoud Deployments

#### Cloud scale Deployments

Load balancer:

    Ensures that each node receives a balanced number of requests

Round Robin--> Givining each node one request

Varnish & Nginx ---> Cashing technologies used

Database caching:

    Memcached

    Redis

#### Using orchestration

The automated configuration and coordination of complex IT systems and services

CLoud APIs allows you to habdle communication between cloud servers services and applications managed

#### Cloud Infrastructure as Code

Tools to manage services as Code:

    Amazon- Cloud formation
    Google - Cloud Deployment manager
    Microsoft - Azure Resource Manager
    Openstack - Heat Orchestration Templates

Terraform:

    uses domain-specific language to specify what the cloud infrastructure would look like

Cloud nodes:

    Long-lived -->Long lasting
    short-lived--> can be deleted

[Getting Started with GCP on Terraform](https://cloud.google.com/community/tutorials/getting-started-on-gcp-with-terraform)

[Creating groups of unmanaged instances](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-unmanaged-instances)

[Load balancing requests](https://cloud.google.com/load-balancing/docs/https/)

[Gcp Load balancer](https://geekflare.com/gcp-load-balancer/)

#### Hybrid setup

[Terraform template](https://blog.inkubate.io/create-a-centos-7-terraform-template-for-vmware-vsphere/)

[Terraform enterprise reference](https://www.terraform.io/docs/enterprise/before-installing/reference-architecture/gcp.html)

[Terraform on-premise hybrid](https://www.hashicorp.com/resources/terraform-on-premises-hybrid-cloud-wayfair)

