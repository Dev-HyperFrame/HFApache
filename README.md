# Apache

세계에서 가장 널리 사용되는 웹 서버 소프트웨어로, 웹 서비스를 제공하는 데에 주로 사용된다.

## 1. 주요 기능 및 특징

### 확장성

다양한 모듈과 플러그인 시스템을 통해 기능을 확장할 수 있으며, 다중 프로세스나 다중 스레드로 동작하여 동시에 여러 요청을 처리할 수 있다.

### 모듈화 구조

모듈화 구조를 갖추고 있어 다양한 기능을 추가하거나 수정할 수 있다. 사용자는 필요한 모듈을 선택하고 활성화하여 웹 서버에 원하는 기능을 추가할 수 있다.

### 보안 기능

다양한 인증 및 암호화 프로토콜을 지원하며, 웹 애플리케이션 취약점을 방어하기 위한 보안 모듈과 기능을 제공한다. 또한, 액세스 제어 및 사용자 인증과 같은 기능을 설정하여 웹 서버의 보안을 강화할 수 있다.

### 유연한 구성

설정 파일을 통해 유연하게 웹 서버를 구성할 수 있다. 가상 호스트(Virtual Hosts)를 설정하거나 URL 리다이렉션, 로깅, 캐싱, 압축 등의 기능을 조정할 수 있다.

## 2. 설치 및 사용 방법
1. httpd Version 설정 및 설치 파일 다운로드
```
export VERSION=2.4.63
```
```
$ wget https://github.com/Dev-HyperFrame/HFApache/releases/download/${VERSION}/hf-apache-${VERSION}.tar.gz
```
2. .bash_profile 및 .profile에서 env.sh 읽도록 설정
```
. ~/env.sh
```
3. 다운로드 한 설치 파일 압축 해제 <br>
3-1. env.sh에서 httpd 설치 대상 디렉터리 설정
   ```
   export HF_HOME="/sw/web" # 설치 디렉터리에 맞게 수정
   ```
3-2. install.sh 스크립트 실행
설치 결과 디렉터리
```
|- TestPage #Apache 설치시 생성되는 Test Page
|- apache2.4 # Apache Home 디렉터리
|- check-package.sh # Apache 설치 시 필요한 package check 스크립트
|- env.sh # Apache에서 사용되는 기본 환경 변수
|- haconfig # Apache 기본 Config, set-config.sh 기동 후 삭제 해도 됨
|- install.sh # install 스크립트, 설치 후 삭제 해도 됨
|- install_modules # apr, apr-util, pcre, openssl 설치 모듈 
|- set-config.sh # 기본 설정 설정하는 스크립트, 실행 후 삭제 해도 됨
|- source # apr, apr-util, pcre, openssl, httpd 소스 디렉터리
```
3-3. set-config.sh 스크립트 실행 <br>
hfapache 기본 컨피그 설정

## 3. Apache Image Build

https://github.com/Dev-HyperFrame/K8S/tree/main/apache#2-Apache-image-build

## 4. Apache in K8S

https://github.com/Dev-HyperFrame/K8S/tree/main/apache#3-Apache-in-K8S

## 5. 참고 URL

- Apache 공식 문서: https://httpd.apache.org/docs/
- Apache 공식 Github: https://github.com/apache/httpd
- HF Apache 공식 Github: https://github.com/TmaxSoftOfficial/HyperFrame-Apache
- Apache K8S 환경 Github: https://github.com/Dev-HyperFrame/K8S/tree/main/apache
