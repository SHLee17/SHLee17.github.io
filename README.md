<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>나의 포트폴리오</title>
  <style>
    /* 기본 스타일 */
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      scroll-behavior: smooth;
      line-height: 1.6;
    }
    h1, h2, h3 {
      margin: 0;
    }

  </style>
</head>
<body>

  <!-- 첫 화면 -->
  <header>
    <img src="profile.jpg" alt="내 사진">
    <h1>홍길동</h1>
    <nav>
      <a href="#career">경력</a>
      <a href="#skills">스킬</a>
      <a href="#portfolio">포트폴리오</a>
      <a href="#about">자기소개</a>
    </nav>
  </header>

  <!-- 경력 -->
  <section id="career">
    <h2>경력</h2>
    <div class="card">
      <h3>○○ 회사 (2020 - 현재)</h3>
      <p>웹 개발자로 근무하며 프론트엔드 및 백엔드 프로젝트를 담당</p>
    </div>
    <div class="card">
      <h3>△△ 스타트업 (2018 - 2020)</h3>
      <p>프론트엔드 엔지니어로 React 기반 서비스 개발</p>
    </div>
  </section>

  <!-- 스킬 -->
  <section id="skills">
    <h2>스킬</h2>
    <ul class="skills">
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
      <li>React</li>
      <li>Node.js</li>
      <li>Git/GitHub</li>
    </ul>
  </section>

  <!-- 포트폴리오 -->
  <section id="portfolio">
    <h2>포트폴리오</h2>
    <div class="card">
      <h3>프로젝트 A</h3>
      <p>React 기반 웹앱, 사용자 인증 및 데이터 시각화 기능 구현</p>
    </div>
    <div class="card">
      <h3>프로젝트 B</h3>
      <p>Node.js API 서버, RESTful 엔드포인트 설계 및 배포</p>
    </div>
  </section>

  <!-- 자기소개 -->
  <section id="about">
    <h2>자기소개</h2>
    <div class="card">
      <p>안녕하세요! 저는 웹 개발자 홍길동입니다.  
      새로운 기술을 배우고 적용하는 것을 좋아하며, 사용자 경험을 개선하는 데 관심이 많습니다.  
      앞으로도 다양한 프로젝트를 통해 성장하고 싶습니다.</p>
    </div>
  </section>

</body>
</html>
