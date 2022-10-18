# ZNS 상에서 Zone 분리를 통한 성능 개선 연구, EXT4, dm-zoned


## 1. 프로젝트 소개

본 프로젝트는 ZNS 상에서 EXT4 file system을 타겟으로 하여 Zone 분리를 통해 성능을 개선을 목표로 한다.

block I/O가 file system을 거쳐 ZNS의 Zone으로 내려올 때 journal data와 file data의 비율을 측정 및 분석.

Zone reclaim이 발생했을 시, valid data의 copy양을 측정 및 분석

EXT4 file system journaling의 특성과 ZNS상에서의 Zone reclaim 특성의 충돌로 인한 Write Amplification이 발생 즉 Overhead로 인한 Performance 저하

Journal data를 위한 별도의 Random Zone을 만들어 준다면 이러한 Amplification을 피할 수 있고 그러므로 Performance 향상을 목표로 본 프로젝트를 진행한다.

## 2. 팀 소개

#### 19학번 임경민(gyoung01145@gmail.com)

#### 18학번 이선후(seonhu04@naver.com)
#### 16학번 김상현(sh333kkk@naver.com)




<!--[![영상 이름](유튜브 영상 썸네일 URL)](유투브 영상 URL)-->
[![부산대학교 정보컴퓨터공학부 소개](http://img.youtube.com/vi/zh_gQ_lmLqE/0.jpg)](https://www.youtube.com/watch?v=zh_gQ_lmLqE)    
