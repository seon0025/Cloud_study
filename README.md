# VPC

### VPC는 네트워크 환경을 가상으로 구성하여, 리소스 배치, 연결 및 보안을 포함해서 완벽하게 제어할 수 있도록 도와주는 역할을 하고 있다

VPC는 노드 간에 여러 개의 병렬 경로를 사용하고 트래픽 로드 밸런싱을 허용하여, 이중화 및 양방향 대역 폭을 늘릴 수 있는 Layer 2 Multipath를 제공한다

사용자가 정의한 가상 네트워크로 AWS 리소스를 사용할 수 있다

VPC는 자체 데이터 센터에서 운영하는 기존 네트워크와 아주 유사한 가상 네트워크이다

VPC는 VPC Domain을 통해서 장비 간 연결을 하며, 단일 VDC(Virtual Device Context)에서만 동작하기 때문에 반드시 동일한 VDC에서 VPC domain을 정의해야 한다

### vpc 장점

단일 장비에서 두 대의 장비간 Port-Channel 제공

사용 가능한 모든 업링크 대역 폭 사용

링크 또는 장비에 장애가 발생할 경우 신속한 Convergence 제공

링크 레벨의 복구 기능 제공

고가용성 제공

### VPC 구성요소

subnet : VPC를 특정 범위로 나눈 범위

RouteTable : 네트워크 트래픽을 전달할 위치가 명시된 규칙 집합 테이블

Internet GW : VPC의 리소스에서의 인터넷 통신을 활성하기 위한 게이트웨이

NAT GW : 네트워크 주소 변환을 통해 private subnet 에서 인터넷 통신을 연결하는 게이트웨이

VPC endpoint : NAT, IGW 등을 통하지 않고 AWS의 서비스를 비공개로 연결 가능하게 하는 서비스


# VPN

VPN(Virtual Private Network, 가상 사설망)은 인터넷을 통해 장치 간 사설 네트워크 연결을 생성하는 서비스이다. 

VPN은 장치의 실제 IP 주소를 가상 IP 주소로 대체하고, 데이터를 암호화하고, 데이터를 전 세계 보안 네트워크로 라우팅함으로써 정보를 보호한다

따라서 VPN 다운로드를 통해 익명성을 확보한 상태에서 안전하게 인터넷을 이용할 수 있다


### vpn 취약점

MITM / 도청

비 허용 접속

이동 중 데이터 도난

S/W 패치




# Subnet

서브넷은 VPC의 IP 주소 범위이다 

서브넷은 단일 가용 영역에 상주해야 한다 

서브넷을 추가한 후에는 VPC에 AWS 리소스 배포할 수 있다




# AWS ELB(Elastic Load Balancer)

### 들어오는 애플리케이션 트래픽을 Amazon EC2 인스턴스 ,  컨테이너, IP 주소, Lambda 함수와 같은 여러 대상에 자동으로 분산시킨다

ELB는 단일 가용 영역 또는 여러 가용 영역에서 다양한 애플리케이션 부하를 처리할 수 있다 

ELB에서 제공하는 로드 밸런서는 애플리케이션 내결함성에 필요한 고가용성, 자동 확장/축소, 강력한 보안을 갖추고 있다

Health Check : 직접 트래픽을 발생시켜 Instance가 살아있는지 체크

지속적으로 IP 주소가 바뀌며 IP 고정이 불가능하다(항상 도메인 기반으로 사용)

http에서 https로 리디렉션을 처리한다

### Elastic Load Balancing 로드 밸런서 유형

Application Load Balancers

Network Load Balancer

Gateway Load Balancer

Classic Load Balancer



# private subnet

### 외부에서 직접적으로 접근이 불가능한 네트워크 영역이다.

Internet Gateway에 연결되어 있지 않은 Subnet이다.

Private Subnet 은 외부 인터넷과 연결이 안되기 때문에 Private Subnet 인스턴스에 접속하고 제어하고 Private Subnet 의 인스턴스들이 인터넷연결을 위한 NAT 인스턴스가 필요하다.

### 프라이빗 서브넷을 사용하는 이유

중요한 리소스들을 안전하게 관리하기 위함이다.

DB를 프라이빗 서브넷에 위치시킨다던가, ELB만 퍼블릭영역에 두고 실제 WAS는 프라이빗영역에 배치하여 보다 안전하게 관리할 수 있다.
