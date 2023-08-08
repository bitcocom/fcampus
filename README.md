# Open API를 이용하여 책 검색 및 데이터베이스 저장 프로그램 자바 애플리케이션 개발

이 프로그램은 Kakao Book Open API를 활용하여 책을 검색하고, 검색한 책 데이터를 데이터베이스에 저장하는 기능을 제공합니다.

## 문제 설명

### 단계 1: Kakao API 키 획득

1. [Kakao Developers](https://developers.kakao.com)에 로그인합니다.

2. 로그인 후, [시작 가이드](https://developers.kakao.com/docs/latest/ko/getting-started/app)에 따라 자신만의 애플리케이션을 생성합니다.

3. 애플리케이션 생성 시, 각 플랫폼별로 앱 키가 발급됩니다. 나중 사용을 위해 REST API 키를 메모해두세요.

### 단계 2: 책 검색 API 사용

1. [다음 검색 REST API 문서](https://developers.kakao.com/docs/latest/ko/daum-search/dev-guide)를 참고하여 책 검색 REST API를 확인합니다.

2. 문서에서 제공된 책 검색 예제 코드를 확인하여 요청과 응답 구조를 이해합니다.

### 단계 3: Java 애플리케이션 구현

1. Kakao Book Open API와 상호작용하는 Java 애플리케이션을 설계합니다.

2. 입력으로 책 제목을 제공하고 API에서 받아온 책 데이터를 JSON 형식으로 파싱합니다.

3. 검색한 책에 관한 정보를 도서 제목, 가격, 출판사, 저자, 할인 가격 및 ISBN과 같이 적절한 정보로 출력합니다.

4. 책 데이터는 기본 10개를 출력하면 된다.

### 단계 4: 데이터베이스 저장

1. 검색 결과를 출력한 후, 사용자에게 데이터베이스에 저장할지 여부를 선택하도록 안내합니다.

2. 사용자가 저장을 선택한 경우 (Y), 관련 책 정보를 데이터베이스에 저장하는 로직을 구현합니다.

3. 데이터베이스에 저장된 책 목록을 다시 불러오는 로직을 구현합니다.

## 입력 및 출력 예시

### [입력 화면]

도서를 검색할 제목을 입력하세요: 자바의 정석

### [출력 결과]

| 도서 제목           | 가격   | 출판사            | 작가              | 할인 가격      | ISBN       |
|---------------------|--------|-------------------|------------------|----------------|------------|
| 자바의 표준          | 30000  | 도울               | 남궁성            |   26000       |  98210011  |
| ...                 |        |                  |                   |                |            |

데이터베이스에 저장하시겠습니까? Y/N
저장성공

[TABLE LIST]

| 도서 제목           | 가격   | 출판사            | 작가              | 할인 가격      | ISBN       |
|---------------------|--------|-------------------|------------------|----------------|------------|
| 자바의 표준          | 30000  | 도울               | 남궁성            |   26000       |  98210011  |
| ...                 |        |                  |                   |                |            |


## 의존성

- Java 8 이상
- 데이터베이스 라이브러리 (예: JDBC) 데이터베이스 상호작용을 위해

## 평가기준
1. 입출력 화면이 잘 설계 되었는가?
2. JSON 책 데이터 잘 파싱하여 목록을 출력하였는가?
3. 책 데이터를 데이터베이스에 잘 저장 하였는가?
4. 데이터베이스에 저장된 책 목록을 잘 불러 왔는가?

