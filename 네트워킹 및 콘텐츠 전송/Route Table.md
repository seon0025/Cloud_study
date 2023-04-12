Route table

- 정의 및 특징

트래픽이 어디로 가야 할지 알려주는 이정표

VPC 생성시 기본으로 하나 제공

- 특성

VPC 내부에 대해서는 자동으로 라우팅이 생성되기 떄문에 별다른 설정 없이 한 Subnet에서 다른 Subnet으로 통신이 가능하다. 

이는 보이지 않는 암시적 라우터인 VPC Router를 통해 가능하게 된다. 

Subnet은 자신이 아닌 다른 Subnet 으로 리소스를 보낼떄 이 VPC Router를 거쳐야 한다.

 
