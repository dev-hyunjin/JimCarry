# JimCarry - <a href="http://www.jimcarry.site">바로가기</a>
스프링 부트 : 공유 창고 중개 서비스

## :desktop_computer: 프로젝트 소개
개개인의 창고에 다른 사람의 짐을 보관할 수 있는 서비스 창고 제공자는 방치된 빈 방을 경제적이고 활용성 있게 만들 수 있으며, 창고 사용자는 집의 여유공간을 확보할 수 있다.
<br>

## :mantelpiece_clock: 개발 기간
* 23.03.13일 - 23.04.07일

### :people_holding_hands: 맴버구성 - 백엔드 업무
 - 팀장  : 황자현 - 관리자페이지
 - 부팀장 : 문은서 - 창고등록, 문의하기, 공지사항
 - 팀원1 : 강민구 - 마이페이지
 - 팀원2 : 김주연 - 검색 및 상세페이지
 - 팀원3 : 김서현 - 메인페이지, 결제페이지
 - 팀원4 : 정현진 - 로그인, 회원가입, ID찾기, PW찾기
 
 ### 프로젝트 목적
 창고 제공자와 창고 사용자 간의 새로운 사회적 연결망이 형성하여, 창고제공자와, 사용자의 경제성과 공간 효율성을 확보하여 사람들의 삶의 질을 향상시킬 수 있는 서비스 기획
 
 # 기획배경
현대 사회에서 많은 사람들이 도시에 살며 작은 공간에서 살아가고 있음에 따라 집안에 물건을 보관하는 것도 쉽지 않은 문제가 되고 있다. 이러한 문제점을 해결하기 위해, 창고 제공자와 창고 사용자를 연결해주는 서비스를 만들어 창고 제공자는 방치된 빈 방을 경제적이고 활용성 있게 만들 수 있고, 창고 사용자는 집의 여유공간을 확보하여 더 편안한 생활을 할 수 있도록 기획하였습니다.

# 목적 및 기대 효과
- 창고 제공자 : 방치된 빈 방을 경제적으로 활용 가능
- 창고 사용자 : 협소한 주거공간 확보 가능
- 1인 가구 및 이삿짐, 취미용품 등 창고 보관을 통해 공간성 확보

# 프로젝트에서 맡은 역할
- 서비스 기획 및 전반적인 구성,
- 프론트 업무 : header, footer, 메인페이지, 검색결과 페이지, 공지사항 목록페이지, 공지사항 상세페이지, 오류페이지(400, 404, 405, 500)
- 백엔드 업무 : 회원가입, 로그인, 아이디 찾기, 비밀번호 찾기
- DB 설계 및 구축
- AWS 서버 배포

### :gear: 개발 환경
- java
- jQuery
- Thymeleaf
- Spring Boot
- HTML, CSS, JS
- MySQL
- JDK 11.0.15
- YAML
- JSON
- REST:API
- Sourcetree
- DBeaver
- IntelliJ IDEA
- git, gitHub
- JUnit5
- POSTMAN
- Lombok
- Boot pay
- Naver OAuth
- Kakao OAuth
- Cool SMS API
- SMTP API

## :pushpin: 맡은 역할

#### 프론트 진행 - <a href="https://github.com/dev-hyunjin/JimCarry/wiki/맡은-기능-소개-(퍼블리싱)" > 상세보기 - WIKI 이동</a>

##### 메인페이지, 검색결과 페이지, 공지사항, 오류페이지
- 헤더
- 푸터
- 메인페이지
- 검색 결과 페이지
- 공지사항 목록페이지
- 공지사항 상세페이지
- 오류페이지(400, 404, 405, 500)


#### 백엔드 진행 - <a href="https://github.com/dev-hyunjin/JimCarry/wiki/맡은-기능-소개-(백엔드)" > 상세보기 - WIKI 이동</a>

##### 회원가입, 로그인, 아이디 찾기, 비밀번호 찾기
- 회원가입
- 로그인
- 아이디 찾기 - 핸드폰
- 아이디 찾기 - 이메일
- 비밀번호 찾기 - 핸드폰
- 비밀번호 찾기 - 이메일
- 비밀번호 변경


# ERD
![짐캐리 포토폴리오 drawio](https://user-images.githubusercontent.com/122762367/233571878-705a5117-3b1e-4b33-aaaa-46514db16b89.png)

# 프로젝트에서 느낀점
## 어려웠던 부분
 : 카카오, 네이버로 Oauth 로그인, 회원가입을 구현할 때 처음 해보는 것이어서 어려웠다. 다른 팀의 
## 문제를 해결했던 부분 
#### 문제상황
 네이버 간편로그인을 할 경우, 로그인 토큰을 인식하고 자동 로그인이 되는 과정에서 흰 화면(callback.html)이 1~2초가량 무조건 노출되었다.
 기능 구현에는 문제가 없었으나, 서버 구동 속도가 느릴 경우 callback.html 화면이 비춰지며 보이는 현상이었다.
 
#### 해결방법
 네이버 로그인 API 설명 페이지에서는 로그인 페이지에서 데이터 이동 시 post로 callback.html로 이동시킨 후 로그인 컨트롤러로 이동할 수 있도록 설명되어 있었다. 그러나 로그인.html에서 바로 데이터를 넘겨받아 메인으로 이동하도록 하였다. 따라서 페이지 이동이 한 번 줄어들어 해당 증상이 없어졌다. 아주 간단한 생각의 전환이었지만 기다리는 사용자의 입장에서 생각해본 해결방법이었다.
 
## 협업의 중요성
 활발하게 소통을 하지 않으면 잘못된 방향으로 프로젝트가 진행된다는 것을 느꼈다. 프로젝트를 할 때 기획단계에서 자세하게 기획을 했다고 생각을 했었는데 각자 이해한 점이 달랐던 적이 있다. 개발 도중 팀원들과 얘기를 해봤을 때 되서야 각자 이해한 점이 다르단 것을 알았고 결국 개발을 중단하고 기획단계로 돌아가 시간이 약간이지만 허비되었다. 그러면서 개발 시간이 결국 줄어든거나 마찬가지였기 때문에 그 점에서 협업의 중요성을 느꼈다.

## 총평
 처음 백엔드 업무를 받았을 때 속으로는 다른 기능들보다 로그인, 회원가입쪽이 비교적 쉽다고 생각했다. 그러나 그 기능조차도 완벽하게 구현하려면 QA작업을 모든 상황을 생각하며 꼼꼼하게 하는 등 엄청난 노력이 필요하다는 것을 깨달았다. 그래도 다음 프로젝트에서는 회원 관련 쪽이 아닌 다른 파트를 맡아서 CRUD를 모두 경험할 수 있는 업무를 받아보고싶다.
