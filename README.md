# Practical Issues in Data Engineering
## 실습환경 구축 후 이미지
![ssm-seoul](2022-03-26-과제완료-화면캡처.png)

## 2022-03-26 1일차 내용
### 실습환경 구축
* 링크참조 [[GitHub Page]](https://github.com/psyoblade/docker-for-dummies/tree/master/wsl)
 * 설치요류시 아래 내용 참고
   * Windows 재시작
   * WSL2 버전 업그레이드 [[Microsoft]](https://docs.microsoft.com/ko-kr/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)
### 데이터 엔지니어링 소개
#### 목차
* 데이터 엔지니어링
* 데이터 엔지니어링의 역사
* Q&A

### Data Engineering
* '데이터 엔지니어링' 이란?
  * Data Scientist vs Data Engineer
    * "Data Scientist" 라는 직군은 여기에서는 아래의 직군(역할)을 통칭하여 일컫기로 함
      * System Engineer: 인프라, 네트워크, 시스템 및 플랫폼을 구축 
      * Data Engineer  : 시스템 아키텍처의 설계, 데이터의 수집, 가공 및 서비스를 위한 데이터 파이프라인의 설계 및 구축
      * Data Analysis  : 데이터를 모델링하고, 탐색하고, 예측 및 처방적인 분석을 수행
    * "Data Scientist"는 기업 내의 가치를 창출하고 서비스의 품질을 향상 시키기 위한 데이터 플랫폼의 설계, 구축 및 고도화를 위한 엔지니어라고 할 수 있음

### 데이터 엔지니어링의 역사
* 데이터 엔지니어링은 현재 Hadoop을 둘러싼 에코시스템의 발전으로 설명하여도 무리가 없을 것이다.
  * 참고 [MAD(Machine Learning, Artificial Intelligence, Data) Landscape 2021](http://46eybw2v1nh52oe80d3bi91u-wpengine.netdna-ssl.com/wp-content/uploads/2021/12/2021-MAD-Landscape-v3.pdf)

### 하둡 시스템소개
#### 목차
* 하둡 시스템
  * 하둡 1.
  * 하둡 2.
    * 분산저장 엔진 - HDFS(Hadoop Distributed File System)
    * 분산처리 엔진 - YARN(Yet Another Resource Negotiator)
* Q&A

### 하둡 1.
* 하둡 1.0 - MapReduce(이하 M/R) 기반 분산 저장, 처리 엔진
  * Map 과 Reduce 함수를 통해 분산 환경에서 다양한 애플리케이션을 구현할 수 있도록 하둡 과 함께 제공 되었던 Java 기반의 프레임워크
  * 구글이 정보 검색을 위해 데이터 처리(색인어 추출, 역색인 등)를 목적으로 개발된 분산 환경에서의 병렬 데이터 처리 기법이자 프로그래밍 모델
  * 병렬 처리가 가능한 Map 함수와 집계를 위한 Reduce 함수를 구현하고 이를 조합하여 다양한 애플리케이션을 구현하는 기법
* 전통적인 데이터 처리방법
  * 데이터를 직접 가져와서 분할 및 처리한 이후에 모든 데이터를 집계하는 과정을 매번 처리
* M/R을 이용한 처리방법
  * 프로그램을 데이터가 있는 각 분산 저장소에 전송하여 Map 과 Reduce 함수를 수행할 수 있는 엔진을 제공
* Hadoop v1.0은 전통적인 방법에 비해 100% 완전하지는 않지만 분산처리방식의 가능성을 보여줌

### 하둡 2 (HDFS, YARN)
* 하둡 2.0에서 가장 큰 변화는 HDFS Federation, NameNode HA 그리고 YARN 이라는 리소스 관리 프레임워크의 등장. HDFS, M/R 모두 하나의 어플리케이션으로 기동할 수 있게 됨
* M/R외에 Graph, MPP 등 다양한 알고리즘 지원
* 참고 ![[Hadoop v1. vs Haddop v.2]](2022-03-26-Hadoop-2.png)
* 출처 [[!Edureka]](https://www.edureka.co/blog/hadoop-yarn-tutorial/)
