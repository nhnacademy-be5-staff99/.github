# Store99
by Staff 99
nhnacademy

<br>

# Members


# Project Architecture
![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/4cce8cdb-b0ce-4b50-8575-285b1390f7be)
| 리포지토리 | Public IP (플로팅 IP) | Private IP (사설 IP) | PORT (포트) | 인스턴스 이름 | CI/CD 환경 | Login User 이름 | 서버 접속 명령어 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| store99-front | 180.210.83.229 | 192.168.0.65 | 8080 | store99-front | Github Action | store99 | ssh -i github_rsa mailto:store99@180.210.83.229 |
| store99-gateway | 125.6.38.50 | 192.168.0.93 | 8080 | store99-gateway | Github Action | store99 | ssh -i github_rsa mailto:store99@125.6.38.50 |
| store99-auth | 125.6.38.50 | 192.168.0.93 | 8081 | store99-gateway | Github Action | store99 | ssh -i github_rsa mailto:store99@125.6.38.50 |
| store99-eureka | 125.6.38.50 | 192.168.0.93 | 8082 | store99-gateway | Github Action | store99 | ssh -i github_rsa mailto:store99@125.6.38.50 |
| store99-bookstore | 133.186.159.71 | 192.168.0.96 | 8080 | store99-bookstore | Jenkins | store99 | ssh -i github_rsa mailto:store99@133.186.159.71 |
| store99-coupon | 180.210.83.81 | 192.168.0.32 | 8080 | store99-coupon | Jenkins | store99 | ssh -i github_rsa mailto:store99@133.186.159.71180.210.83.81 |
| store99-batch | 133.186.212.35 | 192.168.0.130 | 8080 | store99-batch | Jenkins | store99 | ssh -i github_rsa mailto:store99@133.186.159.71133.186.212.35 |
| store99-elk |  |  |  | store99-elk | Jenkins | store99 |  |

# 컨벤션 & 팀 규칙
### 공통

- 필요한 검사나 검증은 프론트, 백, DB 모두 하기
- 사용하지 않는 메소드 지우기
- 무분별한 Lombok 사용하지 않기(Data, Value, Constructor ...)
    - 커버리지
    - 가독성
    - 디버깅
- 9 - 18시 메신저 잘 확인하고 답변 잘하기

### Scrum

- 매일 9시 지각하지 않기
- TODO 관리 확실히 하기
- 스크럼 마스터는 일주일마다 돌아가면서 하고 회의록 정리하기

### GIT

- git flow 따르기
    - 메인 브랜치: main, develop
    - 서포팅 브랜치: feature/{{개발하는 기능 이름}}
        - fast-forward 사용하지 않기(git merge —no-ff)
- commit message 사용
    
    ```
    type(타입): title(제목)
    
    body(본문, 생략 가능)
    
    Resolves: #issueNo, ...(해결한 이슈 , 생략 가능)
    
    See also: #issueNo, ...(참고 이슈, 생략 가능)
    ```
    
    - 타입 종류
        
        ```
        feat : 새로운 기능에 대한 커밋
        fix : 버그 수정에 대한 커밋
        build : 빌드 관련 파일 수정에 대한 커밋
        chore : 빌드 업무 수정, 패키지 매니저 수정(gitignore), 그 외 자잘한 수정에 대한 커밋
        ci : CI관련 설정 수정에 대한 커밋
        docs : 문서 수정에 대한 커밋
        style : 코드 스타일 혹은 포맷 등에 관한 커밋
        refactor :  코드 리팩토링에 대한 커밋
        test : 테스트 코드 수정에 대한 커밋
        rename : 파일 혹은 폴더 이름만 변경한 경우에 대한 커밋
        remove : 파일을 삭제만 한 경우에 대한 커밋
        perf : 성능 개선
        add : 코드나 테스트, 예제, 문서등의 추가 생성이 있는경우
        improve : 호환성, 검증 기능, 접근성 향상에 대한 커밋
        implement : 구현체 완성에 대한 커밋
        move : 코드 이동에 대한 커밋
        updated : 계정이나 버전 업데이트가 있을 때 사용. 주로 코드보다는 문서나, 리소스, 라이브러리등에 사용합니다.
        comment : 필요한 주석 추가 및 변경에 대한 커밋
        ```
        
- pull reqeust 지정 reviewer(2명) 승인 후 merge하기
    ![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/2e6b79f8-9580-4bac-8dae-db2068a78495)
    - 동영, 서연 -> 승규 -> 진규, 아현
    - 서연, 승규 -> 진규 -> 아현, 현철
    - 승규, 진규 -> 아현 -> 현철, 효겸
    - 진규, 아현 -> 현철 -> 효겸, 동영
    - 아현, 현철 -> 효겸 -> 동영, 서연
    - 현쳘, 효겸 -> 동영 -> 서연, 승규
    - 효겸, 동영 -> 서연 -> 승규, 진규
    - 항상 push 전에 pull 먼저 하기
      
- 금요일마다 배포하고 github projects에 sonarqube 화면 올리기
    ![Untitled](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/c7e71132-068a-4930-8a96-6d39aa0afa98)


### 네이밍

- 클래스: PascalCase
- 변수: camelCase
- ENUM, 상수: UPPER_CASE
- 정적 파일: snake_case
- package kebab-case
- 변수명에 자료형 Optional, List 명시
    - memoOptional, memoList
- DB: snake_case

### API

- REST API 원칙 지키기
- 중첩은 3단계까지
- API 명세 Gihub Projects 이용하여 공유
- 후에 Spring Rest Doc 사용하여 명세

[[네트워크] REST API / Restful API란?(feat. 원칙과 네이밍 규칙)](https://ziszini.tistory.com/91)

[웹 API 디자인 모범 사례 - Azure Architecture Center](https://learn.microsoft.com/ko-kr/azure/architecture/best-practices/api-design)

[Dooray!](https://helpdesk.dooray.com/share/pages/9wWo-xwiR66BO5LGshgVTg/2937064454837487755)

### Spring

- osiv 끄기
- ddl-auto 는 validate
- package
    
    ```java
    config
    {{domain}}
    ┕ controller
    ┕ service
    	┕ impl
    ┕ repository
    ┕ dto
    	┕ request (class MemoRegisterRequest.java)
    	┕ response (class MemoRegisterResponse.java)
    ┕ entity
    ┕ exception
    ┕ advice
    ```
    
- 프론트는 부트 스트랩 사용하여 반응형
- properties의 DB 정보는 암호화

### 테스트

- 테스트는 h2 사용
- 커버리지 80퍼 이상 맞추기

### Controller

- 도메인 넘기지 말고 dto 사용
- Map 사용하여 값 받거나 반환하지 말기
- 공통 응답 ResponseEntity 사용
    
    ```json
    // 단 건
    {
        "header": {
            "isSuccessful":true,
    		    "resultCode":200,
    	      "resultMessage":"Success"
        },
        "result": {
    		    ...
        }
    }
    
    // 리스트
    {
        "header": {
            "isSuccessful":true,
    	      "resultCode":200,
    	      "resultMessage":"Success"
        },
        "result": [ ... ],
        "totalCount": 0
    }
    
    // 에러
    {
        "header": {
            "isSuccessful":false,
    		    "resultCode":401,
    	      "resultMessage":"잘못된 비밀번호 입니다."
        },
        "result": null
    }
    ```
    
- HTTP 응답코드
    - 200
    - 400
    - 401
    - 403
    - 404
    - 409

### Service

- 서비스 레이어는 반드시 사용
- transaction 관리 철저히 하기

### Repository

- 리포지토리 findOne의 경우 Optional로 반환
- 조회 시 dto projection 사용
- 리스트 조회 시 pagable 사용

### 어댑터

- 

### 참고
