

``` yaml

library-name: HealthBot
isAzureSpec: true
isArm: true
require: https://github.com/Azure/azure-rest-api-specs/blob/6b08774c89877269e73e11ac3ecbd1bd4e14f5a0/specification/healthbot/resource-manager/readme.md
tag: package-2021-08-24
skip-csproj: true
modelerfour:
  flatten-payloads: false

rename-mapping:
  HealthBotProperties.botManagementPortalLink: -|uri
  HealthBotProperties: HealthBotProperties
  KeyVaultProperties: HealthBotKeyVaultProperties

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