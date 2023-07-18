# Table of contents

* [SDDC Platform](README.md)
* [Tenant 권한 관리](tenant-member.md)

## 💻 Compute

* [Server](compute/server.md)
* [Init Script](compute/init-script.md)
* [Key Pair](compute/key-pair.md)
* [Security Group](compute/security-group/README.md)
  * [Security Rule](compute/security-group/security-rule.md)
* [Network Interface](compute/network-interface.md)
* [Server Snapshot](compute/server-snapshot.md)

## Storage

* [Block Storage](storage/block/README.md)
  * [Volume](storage/block/volume.md)
  * [Volume Snapshot](storage/block-snapshot.md)

## 🔗 Network

* [VPC](network/vpc.md)
* [Subnet](network/subnet.md)
* [Routing](network/routing/README.md)
  * [Subnet Routing](network/subnet-routing.md)
  * [VPC Peering](network/vpc-routing.md)
  * [Gateway 연결](network/external-gateway.md)
  * [Cloud Connect 연결](network/routing/cloud-connect-routing.md)
* [Gateway](network/external-gateway-1.md)
* [Cloud Connect](network/cloud-connect.md)

## NFV

* [vFW](nfv/device.md)

## VNF관리 <a href="#vnf-mgmt" id="vnf-mgmt"></a>

* [VNF](vnf-mgmt/vnf/README.md)
  * [VNF Package](vnf-mgmt/vnf/vnf-package.md)
  * [NS Package](vnf-mgmt/vnf/ns-package.md)
  * [NFV Subnet](vnf-mgmt/vnf/nfv-subnet.md)
  * [NFV Instance](vnf-mgmt/vnf/nfv-instance.md)
  * [Device](vnf-mgmt/vnf/device.md)
  * [Service Graph](vnf-mgmt/vnf/service-graph.md)
  * [Static Route](vnf-mgmt/vnf/static-route.md)
* [기준 정보](vnf-mgmt/etc/README.md)
  * [Spec](vnf-mgmt/etc/spec.md)
  * [License](vnf-mgmt/etc/license.md)
  * [NFV Farm](vnf-mgmt/etc/nfv-farm.md)
  * [VIM](vnf-mgmt/etc/vim.md)
  * [NFV Address Pool](vnf-mgmt/etc/nfv-address-pool.md)

## ⚙ SDN 관리 <a href="#fabric" id="fabric"></a>

* [PathGroup](fabric/pathgroup.md)
* [Gateway Info](fabric/gateway-info.md)
* [Policy Group](fabric/policy-group.md)
* [Domain](fabric/domain.md)
* [PathEndpoint](fabric/pathendpoint.md)

## 🗒 Common

* [사용자 관리](common/user/README.md)
  * [사용자 관리](common/user/auth-user.md)
  * [미승인 사용자 관리](common/user/unauth-user.md)
* [공통코드 관리](common/code.md)
* [CIDR 관리](common/cidr-block.md)
* [Quota 관리](common/quota/README.md)
  * [플랫폼 기본 Quota 관리](common/quota/default.md)
* [이력 관리](common/history/README.md)
  * [Access History](common/history/access.md)
  * [SAGA Transaction](common/history/saga.md)

## 관리 기능 <a href="#management" id="management"></a>

* [Tenant 관리](management/system-tenant.md)
* [OpenStack 관리](management/openstack/README.md)
  * [Image 관리](management/openstack/image.md)
  * [Flavor 관리](management/openstack/flavor.md)
  * [Volume 관리](management/openstack/volume.md)
  * [OpenStack 연결 관리](management/openstack/osp-connect.md)
* [Network 관리](management/network/README.md)
  * [VPC 전체 현황](management/network/system-vpc.md)
  * [Subnet 전체 현황](management/network/system-subnet.md)
  * [Gateway 관리](management/network/gateway.md)
  * [Cloud Connect 관리](management/network/cloud-connect.md)
  * [Cloud Connect 사용 신청 관리](management/network/cloud-connect-ask.md)

## 💡 튜토리얼 <a href="#tutorial" id="tutorial"></a>

* [단일 네트워크 서버 환경 구성](tutorial/undefined.md)
* [다른 네트워크(Subnet) 서버 환경 구성](tutorial/subnet.md)
* [On-Premise와 연결 구성](tutorial/on-premise.md)
* [접근 제어 설정 방법](tutorial/undefined-1.md)
