

``` yaml
library-name: GraphServices
isAzureSpec: true
isArm: true
require: https://github.com/Azure/azure-rest-api-specs/blob/fe056966cf070be84e92dd2dc1b566bae35002cf/specification/graphservicesprod/resource-manager/readme.md
skip-csproj: true
modelerfour:
  flatten-payloads: false

format-by-name-rules:
  'tenantId': 'uuid'
  'ETag': 'etag'
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
  VM: Vm
  VMs: Vms
  Vmos: VmOS
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

rename_mapping:
  AccountResourceProperties.appId: -|uuid
  AccountResourceProperties.billingPlanId: -|uuid

prepend-rp-prefix:
    - ProvisioningState
    - AccountResource
    - AccountResourceList
    - AccountPatchResource
    - AccountResourceProperties
    - TagUpdate
    
directive:
    - remove-operation: 'Operation_List'

```