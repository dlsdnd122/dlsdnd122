<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=0:1e3c72,100:2a5298&height=180&section=header&text=Jung%20InWoong&fontSize=42&fontColor=ffffff&desc=Backend%20Developer&descAlignY=72&descSize=18)

</div>

## 👋 About Me

Spring Boot 기반 백엔드 개발자 **정인웅**입니다.
<br>
실제 팀 프로젝트를 통해 **API 설계, 인증 구현, AWS 배포** 경험을 쌓았습니다.

- 🔐 JWT · OAuth2(카카오/구글) 소셜 로그인 구현 및 인증 트러블슈팅 경험
- ☁️ AWS(EC2, RDS) + GitHub Actions를 활용한 배포 경험
- 🧩 Spring Bean 의존성, 프록시 환경의 요청 처리 등 **"왜 안 되는지"를 끝까지 파고드는 것**을 좋아합니다

<br>

## 🛠 Tech Stack

**Backend**
<br>
![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white)

**Database**
<br>
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

**Infra / DevOps**
<br>
![AWS EC2](https://img.shields.io/badge/AWS%20EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)
![AWS RDS](https://img.shields.io/badge/AWS%20RDS-527FFF?style=for-the-badge&logo=amazonrds&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)

**Frontend**
<br>
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-005F0F?style=for-the-badge&logo=thymeleaf&logoColor=white)

**Collaboration**
<br>
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)

<br>

## 🚀 Projects

### 🏋️ Muscle Market — 운동용품 중고거래 플랫폼
> AI 추천, 지도 기반 운동장 검색, 커뮤니티 기능을 갖춘 운동용품 중고거래 서비스

`Java` `Spring Boot` `Spring Security` `JPA` `PostgreSQL` `AWS` `GitHub Actions`

**담당 역할**
- 🔐 JWT 기반 로그인 / 회원가입 구현
- 🔑 카카오 소셜 로그인(OAuth2) 인증 구현
- 🤖 앨런 AI 기반 운동용품 추천 시스템 개발
- 🗺 카카오 지도 API 기반 운동장 검색 기능 개발
- 🧭 온보딩 페이지 및 사용자 흐름 설계

**트러블슈팅**
- **순환 참조 해결**: OAuth2 구현 중 `SecurityConfig → OAuth2SuccessHandler → UserService` 간 Bean 순환 참조 발생 → `@Lazy`로 생성 시점을 지연시켜 해소
- **redirect_uri mismatch 해결**: HTTPS 배포 환경에서 서버가 baseUrl을 HTTP로 인식 → `ForwardedHeaderFilter`와 forward-headers 설정으로 프록시 뒤 HTTPS 요청을 올바르게 인식하도록 수정

🔗 [GitHub](https://github.com/team-muscle-market/MuscleMarket) · [Notion](https://www.notion.so/oreumi/Muscle-Market-2aeebaa8982b80c2953cfec28e27769d)

<br>

### 🛵 Dev의 민족 — 배민 사업자용 페이지 클론
> 동네 사장님들이 매출 관리, 프로모션, 커뮤니티 활동을 한 곳에서 할 수 있는 서비스

`Java` `Spring Boot` `Spring Security` `JPA` `PostgreSQL` `AWS`

**담당 역할**
- 🍽️ 식당 등록 / 수정 / 삭제 CRUD API 개발
- 📊 관리자 페이지 통계 기능 개발

**트러블슈팅**
- **CSRF 403 오류 해결**: API 요청 시 CSRF 토큰 누락으로 403 발생 → 메타 태그와 JS 요청 헤더에 토큰을 실어 보내도록 수정

🔗 [GitHub](https://github.com/Autopopcornshooter/EST_Second_Proj) · [Notion](https://www.notion.so/oreumi/2-Dev-277ebaa8982b807687d7eb999fd2431c)

<br>

## 💡 Activity

- 🧮 백준 알고리즘 문제 풀이 (Java) — 코딩테스트 단계별 문제 풀이

<!-- solved.ac 티어 뱃지를 넣고 싶다면 아래 주석을 풀고 YOUR_ID를 백준 아이디로 바꿔 주세요 -->
<!-- [![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=YOUR_ID)](https://solved.ac/YOUR_ID) -->

<br>

## 📊 GitHub Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=dlsdnd122&show_icons=true&hide_border=true&count_private=true" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=dlsdnd122&layout=compact&hide_border=true" />

</div>

<br>

## 📫 Contact

<!-- 사용하는 것만 남기고 링크를 채워 주세요 -->
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:your@email.com)
[![Notion](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](https://your-notion-portfolio-link)
