# Jenkins Error 페이지 설정

## 목적
Jenkins를 사용할 때 내장되어 있는 웹서버를 사용할 경우 (tomcat과 같은 다른 WAS사용 없이), 403/404와 같은 에러페이지 발생 시 Jetty의 버전 정보가 노출되어 해당 정보가 출력되지 않도록 수정이 필요했다.

## 조치방법
### web 설정 경로
웹설정관련 파일이 위치한 경로   
CentOS 7 : /var/cache/war (관련 설정이 없을 경우 default 경로)

### error page 생성
mkdir $WEB_HOME/error_page
vi error_page.html

### error page 설정
vi web.xml
error 추가

### Jenkins 재기동
