![image](https://user-images.githubusercontent.com/103885741/231492566-95f5b064-3346-48a6-972d-a228e3995f0f.png)

Amazon Virtual Private Cloud(VPC)

- 정의 및 특징

사용자의 AWS 계정 전용 가상 네트워크이다.

VPC는 AWS 클라우드에서 다른 가상 네트워크와 논리적으로 분리되어 있다.

EC2 인스턴스와 같은 AWS 리소스를 VPC에서 실행할 수 있다.

IP 주소 범위와 VPC 범위를 설정하고 서브넷을 추가하고 보안 그룹을 연결한 다음 라우팅 테이블을 구성한다.

- 구조

Internet -> Internet gateway -> Router <-> Route table <-> NACL -> security group -> EC2(bastion) -> nat gateway

- 구성 요소

Subnet

Internet gateway

NACL/보안그룹

Route table

Nat Instance/Nat Gateway

- 특성

가상의 데이터 센터이다.

외부와 격리된 네트워크 컨테이너 구성 가능(원하는 대로 사설망 구축가능, 부여된 IP 대역을 분할하여 사용 가능)

리전 단위이다.

-사용 사례

EC2, RDS, Lambda등의 AWS의 컴퓨팅 서비스 실행

다양한 서브넷 구성

보안 설정(IP Block, 인터넷에 노출되지 않는 EC2등 구성)



* NACL(Network ACL)은 다른 서브넷끼리 통신할 때 사용자가 직접 정책을 설정하여 유입되는 트래픽을 제어한다.
