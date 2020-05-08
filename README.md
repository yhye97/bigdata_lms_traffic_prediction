# LMS Traffic Prediction using Big Data

## 빅데이터를 활용한 LMS 트래픽 예측

### Motivation:
코로나 19사태로 인하여 초중고등학교들이 온라인 개학을 하는 초유의 사태가 벌어졌다. 트래픽이 급증에 대한 대비가 미흡하여 LMS(학습관리시스템)에 접속이 안되거나 영상 다운로드 및 스트리밍이 끊기는 문제들이 발생하였다. 이로 인하여, 학생들은 보장 받아야할 학습권과, 교사들은 교육권을 보장 받지 못하였다.</br>

***어떤한 상황에서도 학생들의 학습권과 교사들의 교육권을 보장할 수 있는 LMS가 없을까?

### Requirement:
Dataset:</br>
공공데이터포털, 나이스 교육정보 개방 포털 </br>
* 학교기본정보 </br>
*  학사일정 </br>
*  초등학교, 중학교, 고등학교 각 학교, 학급, 반, 교시, 수업 정보가 있는 시간표(https://open.neis.go.kr/hub/elsTimetable 크롤링할 예정) </br>
*  학년별 학급수 및 학생수</br>
* 전국초중/고등학교위치표준데이터</br>

=> 학생들이 LMS를 정확히 어느 위치에서 접속하는지에 관한 데이터가 없고, 사회적 거리두기로 인하여 이동하면서 접속할 경우가 적기 때문에 아래와 같은 항목들을 가정하여 프로젝트를 진행한다 </br>
1.  학생들은 학교 주변에서 강의를 듣는다 </br>
2.  학생들은 각 학교 시간표에 맞게 LMS를 접속한다 </br>


### Background:
* Data Storage:</br>
HDFS </br>

* Data Analysis: </br>
Python 3.7 </br>
Spark 2.4.5</br>
Jupyter Notebook </br>

<img width="1146" alt="Screen Shot 2020-05-08 at 2 07 57 PM" src="https://user-images.githubusercontent.com/17666783/81372892-69f2c200-9136-11ea-928a-be8b1a4f0e9c.png">

</br>
=> 현재 진행상황: </br>
 find_location.ipynb : 도로명 주소 => 위도, 경도 확인 </br>
 students_num.ipynb : 초중고등학교 기본 정보 구한 테이블 (데이터 부족시 더 크롤링하여 추가할 예정)</br>
   

* Data Visualization:</br>
Express Framework </br>
BackEnd: Node JS </br>

### Milestone:
***SCRUM***<br>
5개의  Sprint : Data Acquistion, Storage, Analysis, Visualization, QA </br>
각 2주 동안 진행 </br>

### Desired Outcomes:
1. 언제, 어디서, 특정 학년 학생들이 입력하면 해당 상황의 LMS 접속 트래픽을 예측하여 트래픽 과부화로 인한 문제를 대비할 수 있을 것이다 (e.g. 클라우드 컴퓨팅 자원 할당, CDN 서비스에서 캐시 스토리지 어느 지역에 많이 확보해야될지 여부 등) </br>

2. 직방과 같이 지도에 트래픽 부화도 나타내면 데이터를 보다 직관적으로 이해하기 쉽게 한다 </br>
https://www.zigbang.com/home/apt/map 



