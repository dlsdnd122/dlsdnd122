<div align="center">

<h1>정인웅 · Jung InWoong</h1>

<p><b>Java · Spring Boot 백엔드 개발자</b><br>
문제가 생기면 "왜 안 되는지"를 로그와 실행 흐름으로 끝까지 추적합니다.</p>

<a href="mailto:dlsdnd122@naver.com"><img src="https://img.shields.io/badge/Email-dlsdnd122@naver.com-1A1D21?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://app.notion.com/p/331530ef640e805ebd54e8cc4db7c16b"><img src="https://img.shields.io/badge/Portfolio-Notion-1A1D21?style=flat-square&logo=notion&logoColor=white" alt="Portfolio"></a>

</div>

<br>

### About

- 토목공학에서 컴퓨터SW로 전과해, 이스트소프트 백엔드 과정에서 두 번의 팀 프로젝트를 진행했습니다.
- 인증(JWT · OAuth2), REST API 설계, AWS 배포까지 서비스 하나가 사용자에게 닿는 전 과정을 경험했습니다.
- 영어학원에서 반복 업무를 생성형 AI로 자동화한 경험을 바탕으로, 강사용 AI 자동화 서비스 **EduDesk**를 만들고 있습니다.

<br>

### Featured Projects

| 프로젝트 | 한 줄 소개 | 내가 맡은 일 | 링크 |
| :-- | :-- | :-- | :-- |
| **Muscle Market** | 운동용품 중고거래 · AI 추천 · 운동시설 검색 플랫폼 | 인증/보안, Google OAuth2, 앨런 AI 추천, 카카오맵 연동 | [Repo](https://github.com/team-muscle-market/MuscleMarket) · [Site](https://muscle-market.duckdns.org/) |
| **Dev의 민족** | 동네 사장님을 위한 매장 관리 · 커뮤니티 서비스 | 식당 CRUD API, 관리자 통계, CSRF 이슈 해결 | [Repo](https://github.com/Autopopcornshooter/EST_Second_Proj) · [Demo](https://www.youtube.com/watch?v=BJOcfJpIQDo) |
| **EduDesk** `진행 중` | 학원 강사용 AI 시험 자료 자동화 플랫폼 | LLM 기반 PDF 파싱 파이프라인, 멀티테넌시 설계 | [Org](https://github.com/team-edudesk) |

<br>

### Troubleshooting

<details>
<summary><b>배포 후에만 실패한 구글 소셜 로그인</b> · Muscle Market</summary>
<br>

- **문제** 로컬에서는 정상이던 로그인이 Nginx 리버스 프록시 뒤 배포 환경에서 `redirect_uri_mismatch`로 실패
- **원인** 외부 HTTPS / 내부 HTTP 구조에서 `X-Forwarded-Proto` 헤더를 인식하지 못해 baseUrl을 http로 계산
- **해결** `ForwardedHeaderFilter` 등록 + `server.forward-headers-strategy: native` 적용

</details>

<details>
<summary><b>긴 AI 답변에서만 화면이 비던 추천 기능</b> · Muscle Market</summary>
<br>

- **문제** 서버 로그에는 AI 응답이 찍히는데 긴 답변일 때만 화면에 표시되지 않음
- **원인** 지연 로딩(`FetchType.LAZY`) 필드를 DB 세션이 닫힌 뒤 JSON 직렬화 과정에서 접근
- **해결** 필요한 필드만 담은 응답 DTO를 만들고, 트랜잭션 안의 서비스 계층에서 변환해 반환

</details>

<details>
<summary><b>OAuth2 구현 중 발생한 Bean 순환 참조</b> · Muscle Market</summary>
<br>

- **문제** `SecurityConfig → OAuth2SuccessHandler → UserService` 사이에 순환 참조가 발생해 애플리케이션 기동 실패
- **해결** `@Lazy`로 Bean 생성 시점을 지연시켜 순환 고리를 끊음

</details>

<details>
<summary><b>관리자 API 요청마다 반복된 403</b> · Dev의 민족</summary>
<br>

- **문제** 관리자 페이지에서 JavaScript로 API를 호출할 때마다 403 Forbidden
- **원인** CSRF 보호가 켜진 상태에서 요청에 CSRF 토큰이 빠져 있음
- **해결** 메타 태그에 토큰을 넣고 요청 헤더에 함께 전송. 보안 기능을 끄지 않고 해결

</details>

<br>

### Tech Stack

| 분야 | 기술 |
| :-- | :-- |
| Backend | Java 17, Spring Boot 3, Spring Security, Spring Data JPA, REST API |
| Database | PostgreSQL, MySQL |
| Infra | AWS EC2 · RDS · S3, Nginx, GitHub Actions |
| Frontend | Thymeleaf, JavaScript, HTML / CSS |
| AI | LLM API 연동, 생성형 AI 기반 업무 자동화 |
| Collaboration | Git, GitHub Flow, Notion |
