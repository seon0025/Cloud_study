![image](https://user-images.githubusercontent.com/103885741/232380891-968a0271-4b94-4c9f-bdaa-5a5451a1c128.png)

AWS ELB(Elastic Load Balancer)

들어오는 애플리케이션 트래픽을 Amazon EC2 인스턴스 , 컨테이너, IP 주소, Lambda 함수와 같은 여러 대상에 자동으로 분산시킨다
ELB는 단일 가용 영역 또는 여러 가용 영역에서 다양한 애플리케이션 부하를 처리할 수 있다

ELB에서 제공하는 로드 밸런서는 애플리케이션 내결함성에 필요한 고가용성, 자동 확장/축소, 강력한 보안을 갖추고 있다

Health Check : 직접 트래픽을 발생시켜 Instance가 살아있는지 체크

지속적으로 IP 주소가 바뀌며 IP 고정이 불가능하다(항상 도메인 기반으로 사용)

http에서 https로 리디렉션을 처리한다

- Elastic Load Balancing 로드 밸런서 유형

Application Load Balancers

Network Load Balancer

Gateway Load Balancer

Classic Load Balancer
