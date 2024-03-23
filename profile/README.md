# Store99
by Staff 99
nhnacademy

<br>

# Members


# Project Architecture
![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/4cce8cdb-b0ce-4b50-8575-285b1390f7be)
| 리포지토리 | Public IP (플로팅 IP) | Private IP (사설 IP) | PORT (포트) | 인스턴스 이름 | CI/CD 환경 | Login User 이름 | 서버 접속 명령어 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| store99-front | 180.210.83.229 | 192.168.0.65 | 8080 | store99-front | Github Action | store99 | ssh -i github_rsa store99@180.210.83.229 |
| store99-front | 133.186.247.247 | 192.168.0.74 | 8080 | store99-front2 | Github Action | store99 | ssh -i github_rsa store99@133.186.247.247 |
| store99-gateway | 125.6.38.50 | 192.168.0.93 | 8080 | store99-gateway | Github Action | store99 | ssh -i github_rsa store99@125.6.38.50 |
| store99-auth | 125.6.38.50 | 192.168.0.93 | 8081 | store99-gateway | Github Action | store99 | ssh -i github_rsa store99@125.6.38.50 |
| store99-eureka | 125.6.38.50 | 192.168.0.93 | 8082 | store99-gateway | Github Action | store99 | ssh -i github_rsa store99@125.6.38.50 |
| store99-bookstore | 133.186.159.71 | 192.168.0.96 | 8080 | store99-bookstore | Jenkins | store99 | ssh -i github_rsa store99@133.186.159.71 |
| store99-coupon | 180.210.83.81 | 192.168.0.32 | 8080 | store99-coupon | Jenkins | store99 | ssh -i github_rsa store99@133.186.159.71180.210.83.81 |
| store99-batch | 133.186.212.35 | 192.168.0.130 | 8080 | store99-batch | Jenkins | store99 | ssh -i github_rsa store99@133.186.159.71133.186.212.35 |
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
- package: kebab-case
- DB: snake_case
- branch명: kebab-case
- 변수명에 자료형 Optional, List 명시
    - memoOptional, memoList

  
### API
- REST API 원칙 지키기
- 중첩은 3단계까지
- API 명세 Gihub Projects 이용하여 공유
- 후에 Spring Rest Doc 사용하여 명세
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
  
**요청 메시지**
- 모든 요청에 'Authorization' 헤더를 포함하여 요청합니다.
- json body 를 포함하여 보내야 하는 메시지의 경우, `Content-Type` 헤더를 명시하여야 합니다.
```
    Content-Type: application/json
```

**응답 메시지**
- 응답결과 json에 스펙에 명시되지 않은 추가 필드가 응답될 수 있습니다.
    - 클라이언트에서는 스펙에 명시되지 않은 추가 필드는 무시합니다.

**응답 결과 해석**
- HTTP Status 응답 코드와 Body 내의 `header` 블럭을 사용하여 기본 결과를 표시합니다.
- 사용하는 HTTP Status 응답코드는 다음과 같습니다.
    - 200: 성공
    - 301: 리소스의 위치가 다른 곳인 경우
    - 302: 리소스의 위치가 다른 곳인 경우
    - 303: 리소스의 위치가 다른 곳인 경우
    - 307: 리소스의 위치가 다른 곳인 경우
    - 400: 사용자 입력 오류
    - 401: 인증되지 않은 요청인 경우 (예, Authorization 헤더가 없는 경우, 토큰이 폐기된 경우, 잘못된 토큰을 보낸 경우)
    - 403: 권한이 없는 경우(예, 프로젝트 어드민만 할 수 있는 작업을 일반 멤버가 하는 경우)
    - 404: 존재하지 않는 리소스를 요청하는 경우. (예외적으로 권한이 없는 리소스의 경우에도 404가 나오는 경우가 있음)
    - 409: 중복되는 리소스 생성 요청의 경우
    - 415: Content-Type 이 맞지 않는 경우
    - 429: 너무 많은 요청을 보내는 경우
    - 500: 서버에서 작업에 실패한 경우
- 그 외 상세한 정보가 필요한 경우 응답 body 내의 `header.resultCode, header.resultMessage` 를 사용합니다.
    - `header.resultMessage` 는 사람을 위해 제공되는 필드입니다.
    - `header.resultMessage` 는 이해하기 쉬운 형태로 예고 없이 변경될 수 있습니다.
    - `header.resultMessage` 는 적절한 응답인지 확인을 위해 프로그램 로직에서 사용하는 것을 지양해야합니다.

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
- view랑 관련된 내용만 처리

### Service
- 서비스 레이어는 반드시 사용
- transaction 관리 철저히 하기
- dto 구성은 Service에서 처리
- 여러 리포지토리 호출 가능
- 서비스에서 서비스 호출은 지양
 
### Repository
- 리포지토리 findOne의 경우 Optional로 반환
- 조회 시 dto projection 사용
- 리스트 조회 시 pagable 사용

### 어댑터
- FeignClient 사용

### 참고
