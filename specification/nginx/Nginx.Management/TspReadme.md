

``` yaml

library-name: Nginx
isAzureSpec: true
isArm: true
require: https://github.com/Azure/azure-rest-api-specs/blob/4a361fccb94e82da94a239d3563f1e3e3b9d007d/specification/nginx/resource-manager/readme.md
#tag: package-2023-04-01
skip-csproj: true
modelerfour:
  flatten-payloads: false

#mgmt-debug:
#  show-serialized-names: true

rename-mapping:
  NginxNetworkInterfaceConfiguration.subnetId: -|arm-id
  NginxPrivateIPAddress.privateIPAddress: -|ip-address
  NginxPrivateIPAddress.subnetId: -|arm-id

prepend-rp-prefix:
  - ProvisioningState
  - ResourceSku

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
```