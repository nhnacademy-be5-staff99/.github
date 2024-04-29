# Store99
by Staff 99
nhnacademy

<br>

# Members


# Project Architecture
![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/4cce8cdb-b0ce-4b50-8575-285b1390f7be)
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
  - 늦을 거면 미리 말하기
  - 3번 늦으면 다과 돌리기
- TODO 관리 확실히 하기
- 스크럼 마스터는 일주일마다 돌아가면서 하고 회의록 정리하기
- 스크럼 참여 불가시
  1. 스크럼 마스터나 단톡을 통해서 스크럼 일정 변경 문의하기
  2. 온라인 참석(화면 O)
  3. 2번 불참시 개인프로젝트 전환

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

- 금요일마다 배포하고 github projects에 sonarqube 화면 올리기
    ![Untitled](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/c7e71132-068a-4930-8a96-6d39aa0afa98)

### 코드리뷰
- 코드 리뷰에 임하는 자세 [코드 리뷰에 임하는 자세](https://blog.banksalad.com/tech/banksalad-code-review-culture/#%EC%BD%94%EB%93%9C-%EB%A6%AC%EB%B7%B0%EC%97%90-%EC%9E%84%ED%95%98%EB%8A%94-%EC%9E%90%EC%84%B8)
  - 코드 리뷰 과정에서 이루어지는 것
  - 일관된 아키텍처를 유지하고 있는지
  - 다른 해결 방법에 대한 의견 제시
  - 버그가 발생할 수 있는 가능성 제시
  - 기술적인 지식, 노하우 공유
  - 히스토리 전달

- 리뷰의 5가지 규칙 [카카오 - 효과적인 코드리뷰를 위한 리뷰어의 자세](https://tech.kakao.com/2022/03/17/2022-newkrew-onboarding-codereview/)
  1. 왜 개선이 필요한지 이유를 충분한 설명해 주세요.
  2. 답을 알려주기보다는 스스로 고민하고 개선 방법을 선택할 수 있게 해주세요.
  3. 코드를 클린 하게 유지하고, 일관되게 구현하도록 안내해 주세요.
  4. 리뷰 과정이 숙제검사가 아닌 학습과정으로 느낄 수 있게 리뷰해 주세요.
  5. 리뷰를 위한 리뷰를 하지 마세요. 피드백 할 게 없으면 칭찬해 주세요.
     - LGTM, 수고하셨습니다. 등 금지 
  7. 리뷰도 하나의 업무입니다.
     - 구글은 작성된 모든 코드가 리뷰를 거치도록 하고 있으며, 마이크로소프트 역시 개발자들에게 실제 코드를 작성하는 시간 50%, 코드를 리뷰하는 시간 50%를 할당하도록 하고 있다.
     - 고찰 없이 대충 훑어보는 것은 전혀 도움이 되지 않습니다.
  8. 작은 PR 규칙
     ```
     Google의 코드 리뷰는 작은 변경은 1시간 이내, 규모가 큰 변경사항은 5시간 이내 검토가 완료됩니다. 평균적으로 4시간 이내에 완료된다고 하니 놀랍죠? (대기업의 경우 평균적으로 15시간 이상이 소요되는데 말이죠.)
     더 놀라운 것은 Google의 코드 리뷰의 90%는 10개 미만의 파일로 구성되어 있고, 리뷰의 75%는 리뷰어가 한 명뿐입니다. 변경 요구사항(Change List; CL)의 규모가 크고, 코드 리뷰 대상이 크면 클수록 코드 리뷰 시간은 길어지기 마련입니다. 그래서, Google에서는 변경사항의 전체를 조망해 보고, 주요 부분을 작게 나누어 리뷰할 수 있도록 CL을 여러 개의 CL로 분할한 다음 적절한 순서로 살펴보도록 권장하고 있죠.
     https://www.samsungsds.com/kr/insights/global_code_review.html
     ```

- Pn 룰 [커뮤니케이션 비용을 줄이기 위한 Pn 룰](https://blog.banksalad.com/tech/banksalad-code-review-culture/#%EC%BB%A4%EB%AE%A4%EB%8B%88%EC%BC%80%EC%9D%B4%EC%85%98-%EB%B9%84%EC%9A%A9%EC%9D%84-%EC%A4%84%EC%9D%B4%EA%B8%B0-%EC%9C%84%ED%95%9C-pn-%EB%A3%B0)
  - P1: 꼭 반영해주세요 (Request changes)
  - P2: 적극적으로 고려해주세요 (Request changes)
  - P3: 웬만하면 반영해 주세요 (Comment)
  - P4: 반영해도 좋고 넘어가도 좋습니다 (Approve)
  - P5: 그냥 사소한 의견입니다 (Approve)


- pull reqeust 지정 reviewer(2명) 승인 후 merge하기
    ![image](https://github.com/nhnacademy-be5-staff99/.github/assets/19241369/9eed4483-6ad7-4687-931b-a8120680d9f4)
    - 동영, 서연 -> 승규 -> 진규, 아현
    - 서연, 승규 -> 진규 -> 아현, 현철
    - 승규, 진규 -> 아현 -> 효겸, 동영
    - 진규, 아현 -> 효겸 -> 동영, 서연
    - 현쳘, 효겸 -> 동영 -> 서연, 승규
    - 효겸, 동영 -> 서연 -> 승규, 진규
    - 항상 push 전에 pull 먼저 하기
      
- 참고
  - [삼성SDS - 글로벌기업은 코드 리뷰를 어떻게 할까요?](https://www.samsungsds.com/kr/insights/global_code_review.html)
  - [카카오 - 효과적인 코드리뷰를 위한 리뷰어의 자세](https://tech.kakao.com/2022/03/17/2022-newkrew-onboarding-codereview/)
  - [뱅크샐러드 - 코드 리뷰 in 뱅크샐러드 개발 문화](https://blog.banksalad.com/tech/banksalad-code-review-culture/)
    
### 네이밍
- 클래스: PascalCase
- 변수: camelCase
- ENUM, 상수: UPPER_CASE
- 정적 파일: snake_case
- package: snake_case
- DB: snake_case
- branch명: kebab-case
- 변수명에 자료형 Optional, List 명시
    - memoOptional, memoList

### API
- API 명세
  - api/bookstore/v1/…
  - api/coupon/v1/…
  - open/bookstore/v1/…
  - open/coupon/v1/…
  - open
    - Front -> Gateway
      - url: /open/bookstore/v1/…
    - Gateway -> Bookstore
      - url: /v1/…
  - api
    - Front -> Gateway
      - url: /api/bookstore/v1/…
      - Hearder: X-USER-TOKEN : jwt token
    - Gateway -> Bookstore
      - url: /v1/…
      - Header: X-USER-ID : Long userId
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
 
[REST API 설계 원칙](https://kmkunk.tistory.com/139)

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
- Java Doc 사용
  ```
    /**
     * 한 줄 설명
     *
     * <p>상세한 설명
     *
     * @param
     * @return
     * @throws
     * @author
     * @see
     */
  ```
  - 참고
    ```
    /**
     * Enumeration of HTTP status codes.
     *
     * <p>The HTTP status code series can be retrieved via {@link #series()}.
     *
     * @author Arjen Poutsma
     * @author Sebastien Deleuze
     * @author Brian Clozel
     * @since 3.0
     * @see HttpStatus.Series
     * @see <a href="https://www.iana.org/assignments/http-status-codes">HTTP Status Code Registry</a>
     * @see <a href="https://en.wikipedia.org/wiki/List_of_HTTP_status_codes">List of HTTP status codes - Wikipedia</a>
     */
   ```

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
