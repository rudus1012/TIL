# SPOF(Single Point Of Failure)
SPOF란, 단일 장애점으로, 시스템 구성요소 중 동작하지 않으면 전체 시스템이 중단되는 요소를 말한다.

서버, 디스크, 네트워크장치, 케이블 등 SPOF 가능성이 있는 모든 요소들은 찾아서 시스템 장애를 방지해야 한다.

## SPOF 방지

* High Availability(HA)
많은 고객사의 IT관리자 분들은 현재의 IT서비스의 연속성을 지속적으로 유지하는 방안에 대한 고민을 한번쯤 하게 된다. 그에 따라, 서버 다운타임 최소화, 백업, 가용성 유지 등으로 정보 검색을 하다 보면, 마지막에 만나게 되는 단어가 “서버 이중화”, “서버 HA”등이 될 것이다. HA(High Availability)를 간단히 한국어로 직역을 하자면 “고가용성” 이라고 말하기도 하는데, Wiki의 정리 내용은 아래와 같다.

“고가용성(高可用性, HA, High Availability)이란 서버와 네트워크, 프로그램 등의 정보 시스템이 상당히 오랜 기간 동안 지속적으로 정상 운영이 가능한 성질을 말한다. 고(高)가용성이란 “가용성이 높다”는 뜻으로서, “절대 고장 나지 않음”을 의미한다. 고가용성은 흔히 가용한 시간의 비율을 99%, 99.9% 등과 같은 퍼센티지로 표현하는데, 1년에 계획 된 것 제외 5분 15초 이하의 장애시간을 허용한다는 의미의 파이브 나인스(5 nines), 즉 99.999%는 매우 높은 수준으로 고품질의 데이터센터에서 목표로 한다고 알려져 있다. 하나의 정보 시스템에 고가용성이 요구된다면, 그 시스템의 모든 부품과 구성 요소들은 미리 잘 설계되어야 하며, 실제로 사용되기 전에 완전하게 시험되어야 한다.”

“고가용성 솔루션을 이용하면, 각 시스템 간에 공유 디스크를 중심으로 집단화 하여 클러스터로 엮어지게 만들 수 있다. 동시에 다수의 시스템을 클러스터로 연결할 수 있지만 주로 2개의 서버를 연결하는 방식을 많이 사용한다. 만약 클러스터로 묶인 2개의 서버 중 1대의 서버에서 장애가 발생할 경우, 다른 서버가 즉시 그 업무를 대신 수행하므로, 시스템 장애를 불과 수 초에서 수 분 안에 복구할 수 있다.”

위의 내용으로 간단히 HA솔루션을 설명하면, 서버 2대를 통해 한쪽 서버가 장애 시 다른 한쪽 서버가 해당 서비스를 대신 운영하여 가용성을 높이는 솔루션이라고 생각 하면 된다.

* Fault Tolerant(FT)
시스템을 구성하는 부품의 일부에서 결함 또는 고장이 발생하여도 정상적 혹은 부분적으로 기능을 수행할 수 있는 시스템이다. 결함감내 시스템은 부품의 고장이 발생하면 부분적인 기능을 사용할 수 없게되며, 계속적으로 부품의 결함이나 고장이 발생하면 부분적인 기능을 사용할 수 없게되며, 계속적으로 부품의 결함이나 고장이 발생하면 점진적으로 사용할 수 없는 기능이 증가하며, 치명적인 결함이나 고장이 발생하면 시스템이 정지한다.

* Load Balancing
하나의 인터넷 서비스가 발생하는 트래픽이 많을 때 여러 대의 서버가 분산처리하여 서버의 로드율 증가, 부하량, 속도저하 등을 고려하여 적절히 분산처리하여 해결해주는 서비스입니다.

* RAID(redundant array of independent disks)
여러개의 디스크를 묶어 하나의 디스크 처럼 사용하는 기술
    - RAID Level : RAID 0 ~ RAID 6까지 있지만, 최근 출시되는 RAID 컨트롤러에서 사용 가능 한 RAID Level은 RAID 0, RAID 1, RAID 5, RAID 6 입니다.

