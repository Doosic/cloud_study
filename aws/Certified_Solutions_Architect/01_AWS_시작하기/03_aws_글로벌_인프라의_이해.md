# aws 글로벌 인프라의 이해

- 글로벌 인프라는 aws의 솔루션을 설계할때 재해복구 시스템 설계 및 고가용성 시스템 설계시 매우 중요한 개념이다.
- 리전, 가용 영역, 엣지 네트워크 3가지의 분류로 나뉜다.

## aws 글로벌 인프라

- aws는 전 세계 수십개의 지리적 리전에 가용영역을 운영중

### 리전

- 데이터 센터를 클러스터링 하는 물리적 위치(서울리전, 홍콩리전 등)
- 전세계 주요국가에 위치
- 1개 AWS 리전 = 2개이상의 가용영역으로 구성
- 대부분의 aws 서비스는 리전을 선택 하여 시작(예, ec2 서비스)
- 리전을 선택하지 않는 글로벌 서비스도 있다(예, IAM서비스)
- 재해복구(DR) 설계 = 2개이상의 리전에 시스템을 배치

### 가용 영역(Availability Zone - AZ)

- 가용영역 = 하나 이상의 개별 데이터 센터
- 1개의 리전은 2개이상의 가용영역으로 구성 (보통 3~4개의 가용영역으로 구성)
- <img src="https://user-images.githubusercontent.com/82255957/229271965-728ac787-5305-401f-9fd7-2e14785a9757.png" width="400" height="250"/>
- 가용영역끼리는 물리적으로 떨어져 있고 고속 네트워크로 연결됨
- 고가용성 설계 = 다중 AZ (Multi-AZ), 2개이상의 가용영역에 시스템 배치

### 엣지 로케이션(Edge Location)

- 엣지 로케이션에 콘텐츠(데이터)를 캐싱하여 사용자에게 더 짧은 지연 시간으로 콘텐츠를 전송
- <img src="https://user-images.githubusercontent.com/82255957/229272166-7d6d22d8-c5cd-475c-bf33-c1d3b6f6e684.png" width="400" height="250"/>
- 전세계 수백개의 엣지 로케이션을 운영 중
- 엣지로케이션과 AWS 리전, 가용영역끼리는 고속 네트워크로 연결되어 있다.


