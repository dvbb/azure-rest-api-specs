

``` yaml

library-name: ArcScVmm
# default tag is a preview version
isAzureSpec: true
isArm: true
require: https://github.com/Azure/azure-rest-api-specs/blob/ba936cf8f3b4720dc025837281241fdc903f7e4d/specification/scvmm/resource-manager/readme.md
skip-csproj: true
modelerfour:
  flatten-payloads: false
use-model-reader-writer: true

format-by-name-rules:
  'tenantId': 'uuid'
  'etag': 'etag'
  'location': 'azure-location'
  '*Uri': 'Uri'
  '*Uris': 'Uri'

acronym-mapping:
  CPU: Cpu
  CPUs: Cpus
  Os: OS
  Ip: IP
  Ips: IPs|ips
  ID: Id
  IDs: Ids
  VMM: Vmm
  VM: Vm
  VMs: Vms
  VMScaleSet: VmScaleSet
  DNS: Dns
  VPN: Vpn
  NAT: Nat
  WAN: Wan
  Ipv4: IPv4|ipv4
  Ipv6: IPv6|ipv6
  Ipsec: IPsec|ipsec
  SSO: Sso
  URI: Uri
  Etag: ETag|etag

rename-mapping:
  AvailabilitySet: ScVmmAvailabilitySet
  Cloud: ScVmmCloud
  VMMServer: ScVmmServer
  VirtualMachine: ScVmmVirtualMachine
  VirtualMachineTemplate: ScVmmVirtualMachineTemplate
  VirtualNetwork: ScVmmVirtualNetwork

directive:
  - from: swagger-document
    where: $.definitions.InventoryItem.properties.properties
    transform: $["x-ms-client-flatten"] = false;
```