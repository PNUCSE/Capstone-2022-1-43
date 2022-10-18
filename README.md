# ZNS 상에서 Zone 분리를 통한 성능 개선 연구, EXT4, dm-zoned


## 1. 프로젝트 소개

본 프로젝트는 ZNS 상에서 EXT4 file system을 타겟으로 하여 Zone 분리를 통해 성능을 개선을 목표로 한다.

[1] block I/O가 file system을 거쳐 ZNS의 Zone으로 내려올 때 journal data와 file data의 비율을 측정 및 분석.

[2] Zone reclaim이 발생했을 시, valid data의 copy양을 측정 및 분석

[3] EXT4 file system journaling의 특성과 ZNS상에서의 Zone reclaim 특성의 충돌로 인한 Write Amplification이 발생 즉 Overhead로 인한 Performance 저하

[4] Journal data를 위한 별도의 Random Zone을 만들어 준다면 이러한 Amplification을 피할 수 있고 그러므로 Performance 향상을 목표로 본 프로젝트를 진행한다.

## 2. 팀 소개

#### 19학번 임경민(gyoung01145@gmail.com)
###### 역할 : ZNS 논문 분석, 보고서 및 포스터 제작, Kernel 분석, 작업 환경 구축 및 개발

#### 18학번 이선후(seonhu04@naver.com)
###### 역할 : ZNS 논문 분석, 보고서 및 포스터 제작, Kernel 분석, 작업 환경 구축 및 개발

#### 16학번 김상현(sh333kkk@naver.com)
###### 역할 : ZNS 논문 분석, kernel 분석


## 3. 프로젝트 진행 과정

[1] block I/O가 EXT4 file system을 거쳐 ZNS의 Zone으로 내려올 때 journal data와 file data의 비율을 측정 및 분석

<  Amount of File Data in each Zone >
<img src = "https://user-images.githubusercontent.com/65112294/196332247-b97c93fd-5757-4d81-989f-3a70e59c41a5.png" width = "90%">
<  Amount of Journal Data in each Zone > 
<img src = "https://user-images.githubusercontent.com/65112294/196332937-823b2c04-1ecc-402e-bbd3-c56d7baa2614.png" width = "90%">

< Amount of Journal/File data from LBA Chunk Number 14 in Zone
<img src = "https://user-images.githubusercontent.com/65112294/196333122-0ac56f37-2446-4b20-a8c9-19c2179852a4.png" width = "90%">


















[![부산대학교 정보컴퓨터공학부 소개](http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg)](https://www.youtube.com/watch?v=zh_gQ_lmLqE)    
