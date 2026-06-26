<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>나의 포트폴리오</title>
  <style>
    html, body {
      margin: 0;
      height: 100%;
      scroll-snap-type: y mandatory;
      overflow-y: scroll;
      font-family: 'Segoe UI', sans-serif;
    }

    section {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      scroll-snap-align: start;
      transition: opacity 1s ease, transform 1s ease;
      opacity: 0;
      transform: translateY(50px);
    }

    section.visible {
      opacity: 1;
      transform: translateY(0);
    }

    header {
      background: linear-gradient(135deg, #667eea, #764ba2);
      color: white;
      text-align: center;
    }
    header img {
      width: 160px;
      height: 160px;
      border-radius: 50%;
      border: 4px solid white;
      margin-bottom: 20px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.3);
    }
    nav a {
      margin: 0 15px;
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    nav a:hover {
      color: #ffd700;
    }

    #career { background: #f9f9f9; }
    #skills { background: #e3f2fd; }
    #portfolio { background: #fff3e0; }
    #about { background: #f0f0f0; }

    .card {
      background: white;
      margin: 20px;
      padding: 20px;
      max-width: 600px;
      border-radius: 12px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    ul.skills {
      list-style: none;
      padding: 0;
    }
    ul.skills li {
      display: inline-block;
      margin: 10px;
      padding: 10px 20px;
      background: #667eea;
      color: white;
      border-radius: 20px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <!-- 첫 화면 -->
  <section id="home" class="visible">
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
  </section>

  <!-- 경력 -->
  <section id="career">
    <h2>경력</h2>
    <div class="card">
      <h3>○○ 회사 (2020 - 현재)</h3>
      <p>웹 개발자로 근무하며 프론트엔드 및 백엔드 프로젝트 담당</p>
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

  <script>
    // 스크롤 시 애니메이션 효과
    const sections = document.querySelectorAll("section");
    const options = { threshold: 0.3 };

    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add("visible");
        }
      });
    }, options);

    sections.forEach(section => {
      observer.observe(section);
    });
  </script>

</body>
</html>
