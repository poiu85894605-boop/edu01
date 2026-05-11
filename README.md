<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>아름다운 우리 땅, 독도 (Dokdo)</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #004a99;
            --secondary-color: #007bff;
            --bg-light: #f8f9fa;
            --text-dark: #333;
        }

        body { font-family: 'Noto Sans KR', sans-serif; margin: 0; padding: 0; color: var(--text-dark); line-height: 1.6; word-break: keep-all; overflow-x: hidden; }
        
        /* 네비게이션 */
        nav { background: rgba(255, 255, 255, 0.95); padding: 1rem 5%; display: flex; justify-content: space-between; align-items: center; position: sticky; top: 0; box-shadow: 0 2px 10px rgba(0,0,0,0.1); z-index: 1000; }
        nav h1 { font-size: 1.5rem; color: var(--primary-color); margin: 0; cursor: pointer; }
        nav ul { list-style: none; display: flex; gap: 20px; margin: 0; }
        nav a { text-decoration: none; color: #555; font-weight: 500; transition: 0.3s; cursor: pointer; }
        nav a:hover { color: var(--primary-color); }

        /* 히로 섹션 */
        .hero { 
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1599395242603-90947604313d?auto=format&fit=crop&q=80&w=1600');
            height: 80vh; background-size: cover; background-position: center;
            display: flex; flex-direction: column; justify-content: center; align-items: center; color: white; text-align: center;
        }
        .hero h2 { font-size: 3.5rem; margin-bottom: 1rem; transform: translateY(30px); opacity: 0; transition: all 1s ease; }
        .hero.active h2 { transform: translateY(0); opacity: 1; }

        /* 섹션 공통 */
        section { padding: 100px 10%; opacity: 0; transform: translateY(50px); transition: all 0.8s ease-out; }
        section.reveal { opacity: 1; transform: translateY(0); }

        .section-title { text-align: center; margin-bottom: 50px; }
        .section-title h3 { font-size: 2.5rem; color: var(--primary-color); margin-bottom: 10px; }
        .section-title .bar { width: 60px; height: 4px; background: var(--secondary-color); margin: 0 auto; }

        /* 타임라인 스타일 */
        .timeline { position: relative; max-width: 1200px; margin: 0 auto; }
        .timeline::after { content: ''; position: absolute; width: 6px; background-color: #ddd; top: 0; bottom: 0; left: 50%; margin-left: -3px; }
        
        .t-container { padding: 10px 40px; position: relative; width: 50%; box-sizing: border-box; opacity: 0; transition: all 0.6s ease; }
        .t-container.show { opacity: 1; transform: translateX(0) !important; }
        
        .left { left: 0; text-align: right; transform: translateX(-50px); }
        .right { left: 50%; transform: translateX(50px); }
        
        .t-container::after { content: ''; position: absolute; width: 25px; height: 25px; right: -17px; background-color: white; border: 4px solid var(--secondary-color); top: 15px; border-radius: 50%; z-index: 1; }
        .right::after { left: -17px; }

        .content { padding: 20px; background: var(--bg-light); border-radius: 6px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); transition: 0.3s; }
        .content:hover { transform: scale(1.03); background: white; }
        .year { font-weight: bold; color: var(--secondary-color); font-size: 1.1rem; }

        footer { background: #222; color: white; text-align: center; padding: 40px 0; }

        @media screen and (max-width: 768px) {
            .timeline::after { left: 31px; }
            .t-container { width: 100%; padding-left: 70px; padding-right: 25px; text-align: left !important; transform: translateX(30px) !important; }
            .t-container::after { left: 15px; }
            .right { left: 0%; }
        }
    </style>
</head>
<body>

<nav id="navbar">
    <h1 onclick="window.scrollTo({top: 0, behavior: 'smooth'})"><i class="fa-solid fa-anchor"></i> DOKDO</h1>
    <ul>
        <li><a data-target="about">소개</a></li>
        <li><a data-target="history">역사</a></li>
    </ul>
</nav>

<section class="hero" id="home">
    <h2>대한민국의 아침이 시작되는 곳</h2>
    <p>우리 땅 독도의 숨겨진 이야기를 만나보세요.</p>
</section>

<section id="about">
    <div class="section-title">
        <h3>📍 독도 소개</h3>
        <div class="bar"></div>
    </div>
    <div style="text-align: center; max-width: 800px; margin: 0 auto;">
        <p>독도는 460만 년 전 화산 활동으로 탄생한 보물 같은 섬입니다. 동도와 서도를 중심으로 펼쳐진 천혜의 자연경관을 확인해 보세요.</p>
    </div>
</section>

<section id="history">
    <div class="section-title">
        <h3>📜 역사적 기록 10선</h3>
        <div class="bar"></div>
    </div>
    <div class="timeline" id="timeline">
        <!-- JS로 데이터가 들어갈 자리 또는 정적 유지 -->
        <div class="t-container left"><div class="content"><span class="year">512년</span><h4>우산국 귀속</h4><p>이사부의 정벌로 한국 역사 편입</p></div></div>
        <div class="t-container right"><div class="content"><span class="year">1454년</span><h4>세종실록지리지</h4><p>독도 영유권 명확히 기록</p></div></div>
        <div class="t-container left"><div class="content"><span class="year">1690년대</span><h4>안용복 사건</h4><p>일본으로부터 조선 땅 확약</p></div></div>
        <div class="t-container right"><div class="content"><span class="year">1877년</span><h4>태정관 지령</h4><p>일본 정부의 독도 제외 인정</p></div></div>
        <div class="t-container left"><div class="content"><span class="year">1900년</span><h4>칙령 제41호</h4><p>근대적 주권 공식 선포</p></div></div>
        <div class="t-container right"><div class="content"><span class="year">1905년</span><h4>시마네현 고시</h4><p>일본의 불법 영토 침탈</p></div></div>
        <div class="t-container left"><div class="content"><span class="year">1946년</span><h4>SCAPIN 677</h4><p>연합군의 한국 영토 분류</p></div></div>
        <div class="t-container right"><div class="content"><span class="year">1952년</span><h4>평화선 선포</h4><p>대한민국 해양 주권 확립</p></div></div>
        <div class="t-container left"><div class="content"><span class="year">1953년</span><h4>독도 수호</h4><p>의용수비대 활동 및 경비대 주둔</p></div></div>
        <div class="t-container right"><div class="content"><span class="year">1981년</span><h4>실거주 시작</h4><p>최초 주민 전입 및 관리</p></div></div>
    </div>
</section>

<footer>
    <p>&copy; 2026 독도 사랑 캠페인. 독도는 대한민국의 고유 영토입니다.</p>
</footer>

<script>
    /**
     * 바닐라 자바스크립트 기능 구현
     */
    document.addEventListener('DOMContentLoaded', () => {
        
        // 1. 히로 섹션 애니메이션
        setTimeout(() => {
            document.querySelector('.hero').classList.add('active');
        }, 300);

        // 2. 부드러운 스크롤 이동 (Smooth Scroll)
        const navLinks = document.querySelectorAll('nav a');
        navLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                const targetId = e.target.getAttribute('data-target');
                const targetSection = document.getElementById(targetId);
                window.scrollTo({
                    top: targetSection.offsetTop - 70,
                    behavior: 'smooth'
                });
            });
        });

        // 3. 스크롤 시 섹션 및 타임라인 카드 노출 (Intersection Observer)
        const observerOptions = {
            threshold: 0.1
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('reveal'); // 섹션 등장
                    
                    // 만약 타임라인 안의 카드들이라면 순차적으로 등장
                    if (entry.target.id === 'history') {
                        const cards = document.querySelectorAll('.t-container');
                        cards.forEach((card, index) => {
                            setTimeout(() => {
                                card.classList.add('show');
                            }, index * 150);
                        });
                    }
                }
            });
        }, observerOptions);

        // 감시 대상 설정
        document.querySelectorAll('section').forEach(section => {
            observer.observe(section);
        });
    });
</script>

</body>
</html>
