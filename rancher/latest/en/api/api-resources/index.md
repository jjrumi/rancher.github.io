---
title: API
layout: rancher-api-default
version: latest
lang: en
---

## Resource Types


<br>

[Account]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/account/)|
---|
All resources in Rancher are owned or created by an account. |

<br>

[Amazonec2Config]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/amazonec2Config/)|
---|
The configuration to launch an EC2 instance in Amazon Web Services using [machine]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/machine). Rancher is calling `docker-machine`, so any available options in `docker-machine` for specific drivers are exposed in Rancher. The default fields from `docker-machine` are not listed in the Rancher API, and they can be found in the `docker-machine` documentation. The notes on which fields are **required** are from the `docker-machine` documentation. |

<br>

[ApiKey]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/apiKey/)|
---|
An API Key provides access to the Rancher API if access control has been turned on. The access key and secret key pair are created per environment and can be used to directly call the API or used with [rancher-compose]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/rancher-compose). |

<br>

[AuditLog]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/auditLog/)|
---|
 |

<br>

[AzureConfig]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/azureConfig/)|
---|
The configuration to launch an instance in Microsoft Azure. For all cloud providers, Rancher is calling `docker-machine`, so any available options in `docker-machine` are exposed in Rancher. The default fields from `docker-machine` are not listed in the Rancher API, and they can be found in the `docker-machine` documentation. |

<br>

[Backup]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/backup/)|
---|
 |

<br>

[BackupTarget]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/backupTarget/)|
---|
 |

<br>

[Certificate]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/certificate/)|
---|
A certificate is used to add in SSL termination to load balancers. |

<br>

[Container]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/container/)|
---|
A container is a representation of a Docker container on a host. |

<br>

[Credential]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/credential/)|
---|
 |

<br>

[DigitaloceanConfig]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/digitaloceanConfig/)|
---|
The configuration to launch a droplet in DigitalOcean using [machine]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/machine). Rancher is calling `docker-machine`, so any available options in `docker-machine` for specific drivers are exposed in Rancher. The default fields from `docker-machine` are not listed in the Rancher API, and they can be found in the `docker-machine` documentation. |

<br>

[DnsService]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/dnsService/)|
---|
A "dnsService" in the API is referred to as a Service Alias in the UI and the Rancher documentation. In the API documentation, we'll use the UI terminology. A service alias allows the ability to add a DNS record for your services to be discovered. |

<br>

[Environment]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/environment/)|
---|
An "environment" in the API is referred to as a stack in the UI and the Rancher documentation. In the API documentation, we'll use the UI terminology. A Rancher stack mirrors the same concept as a docker-compose project.  It represents a group of services that make up a typical application or workload. |

<br>

[ExternalService]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/externalService/)|
---|
An external service allows the ability to add any IP or hostname as a service to be discovered as a service. |

<br>

[HealthcheckInstanceHostMap]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/healthcheckInstanceHostMap/)|
---|
 |

<br>

[Host]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/host/)|
---|
Hosts are the most basic unit of resource within Rancher and is represented as any Linux server, virtual or physical, with the following minimum requirements. <br> <br> * Any modern Linux distribution that supports Docker 1.10.3+. <br> * Must be able to communicate with the Rancher server via http or https through the pre-configured port (Default is 8080). <br> * Must be routable to any other hosts belonging to the same environment to leverage Rancher's cross-host networking for Docker containers.<br> <br> Rancher also supports Docker Machine and allows you to add your host via any of its supported drivers. |

<br>

[Identity]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/identity/)|
---|
An identity is Rancher's representation of an object(i.e. `ldap_group`, `github_user`) when Rancher has turned on [access control]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/configuration/access-control/). The `externalId` in an identity is the unique identifier in the authentication system that represents the object. The role of an identity is always null unless it is being returned as the identity of a [projectMember]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/projectMember/). |

<br>

[Image]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/image/)|
---|
 |

<br>

[Instance]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/instance/)|
---|
 |

<br>

[IpAddress]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/ipAddress/)|
---|
 |

<br>

[KubernetesStack]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/kubernetesStack/)|
---|
 |

<br>

[KubernetesStackUpgrade]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/kubernetesStackUpgrade/)|
---|
 |

<br>

[LoadBalancerService]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/loadBalancerService/)|
---|
Rancher implements a managed load balancer using HAProxy that can be manually scaled to multiple hosts.  A load balancer can be used to distribute network and application traffic to individual containers by directly adding them or "linked" to a basic service.  A basic service that is "linked" will have all its underlying containers automatically registered as load balancer targets by Rancher. |

<br>

[Machine]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/machine/)|
---|
Machines are created whenever Rancher uses `docker-machine` to create hosts in Rancher. Adding any type of host through the UI that is not the custom command option is calling `docker-machine` and a machine entry will be created as well as a [host]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/host). |

<br>

[MachineDriver]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/machineDriver/)|
---|
 |

<br>

[PacketConfig]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/packetConfig/)|
---|
The configuration to launch an instance in Packet. |

<br>

[Project]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/project/)|
---|
A "project" in the API is referred to as an environment in the UI and Rancher documentation. In the API documentation, we'll use the UI terminology.  All hosts and any Rancher resources (i.e. containers, load balancers, etc.) are created and belong to an [environment]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/configuration/environments/).  Access control to who can view and manage these resources are then defined by the owner of the environment.  Rancher currently supports the capability for each user to manage and invite other users to their environment and allows for the ability to create multiple environments for different workloads.  For example, you may want to create a "dev" environment and a separate "production" environment with its own set of resources and limited user access for your application deployment. |

<br>

[ProjectMember]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/projectMember/)|
---|
A "project member" in the API is referred to as an environment members in the UI and Rancher documentation. An environment member is a list of all of the members of the  environment. An environment member is an [identity]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/identity). |

<br>

[PullTask]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/pullTask/)|
---|
 |

<br>

[RegistrationToken]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/registrationToken/)|
---|
 |

<br>

[Registry]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/registry/)|
---|
A registry is where image repositories are hosted. The repository can be either from DockerHub, Quay.io, or a custom private registry. |

<br>

[RegistryCredential]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/registryCredential/)|
---|
A registry credential is used to authenticate against a [registry]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/registry). |

<br>

[Service]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/service/)|
---|
Rancher adopts the standard Docker Compose terminology for services and defines a basic service as one or more containers created from the same Docker image.  Once a service (consumer) is linked to another service (producer) within the same stack, a DNS record mapped to each container instance is automatically created and discoverable by containers from the "consuming" service. Other benefits of creating a service under Rancher include":" <br><br> * Service HA - the ability to have Rancher automatically monitor container states and maintain a service's desired scale. <br> * Health Monitoring - the ability to set basic monitoring thresholds for container health. |

<br>

[ServiceConsumeMap]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/serviceConsumeMap/)|
---|
 |

<br>

[ServiceExposeMap]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/serviceExposeMap/)|
---|
 |

<br>

[ServiceProxy]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/serviceProxy/)|
---|
 |

<br>

[Setting]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/setting/)|
---|
 |

<br>

[Snapshot]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/snapshot/)|
---|
 |

<br>

[StoragePool]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/storagePool/)|
---|
A storage pool is a list of hosts that can participate in shared storage. |

<br>

[Subscribe]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/subscribe/)|
---|
 |

<br>

[Volume]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/volume/)|
---|
A volume can be associated to containers or storage pools. <br><br> * A container can have many volumes and containers are mapped to volumes the [mount]({{site.baseurl}}/rancher/{{page.version}}/{{page.lang}}/api/api-resources/mount/) link on a container. <br> * A storage pool owns many volues. The volume is only available to containers deployed on hostst that are part of the storage pool. When a volume is being created, you do not directly associate it to a storage pool. You will only need to specify a driver and during allocation, Rancher will resolve it to a storage pool. |

