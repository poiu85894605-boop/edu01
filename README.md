<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>우리 땅, 아름다운 독도 교육 포털</title>
    <style>
        /* 기본 스타일 초기화 */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Pretendard', sans-serif; line-height: 1.6; color: #333; background-color: #f4f7f9; }
        a { text-decoration: none; color: inherit; }

        /* 헤더 스타일 */
        header { background: #fff; border-bottom: 2px solid #0056b3; padding: 1rem 5%; display: flex; justify-content: space-between; align-items: center; sticky: top; }
        .logo { font-size: 1.5rem; font-weight: bold; color: #0056b3; }
        nav ul { display: flex; list-style: none; }
        nav ul li { margin-left: 20px; font-weight: 600; }
        nav ul li:hover { color: #007bff; cursor: pointer; }

        /* 히어로 섹션 */
        .hero { 
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.3)), url('https://images.unsplash.com/photo-1599420186946-7b6fb4e297f0?auto=format&fit=crop&q=80&w=1000') no-repeat center/cover;
            height: 400px; display: flex; flex-direction: column; justify-content: center; align-items: center; color: #fff; text-align: center;
        }
        .hero h1 { font-size: 3rem; margin-bottom: 10px; text-shadow: 2px 2px 4px rgba(0,0,0,0.5); }

        /* 메인 컨텐츠 레이아웃 */
        .container { display: flex; padding: 40px 5%; max-width: 1200px; margin: 0 auto; gap: 30px; }
        
        /* 사이드바 */
        aside { flex: 1; background: #fff; padding: 20px; border-radius: 8px; box-shadow: 0 2px 10px rgba(0,0,0,0.05); height: fit-content; }
        aside ul { list-style: none; }
        aside ul li { padding: 12px 0; border-bottom: 1px solid #eee; }
        aside ul li:last-child { border: none; }
        aside ul li.active { color: #0056b3; font-weight: bold; }

        /* 본문 섹션 */
        section { flex: 3; }
        .card-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; margin-top: 20px; }
        .card { background: #fff; padding: 20px; border-radius: 8px; border-top: 4px solid #0056b3; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        .card h3 { margin-bottom: 15px; color: #0056b3; }
        .card p { font-size: 0.9rem; color: #666; }

        /* 푸터 */
        footer { background: #333; color: #fff; text-align: center; padding: 20px; margin-top: 40px; font-size: 0.8rem; }
    </style>
</head>
<body>

    <header>
        <div class="logo">독도 교육 포털</div>
        <nav>
            <ul>
                <li>독도 소개</li>
                <li>독도 역사</li>
                <li>생태계</li>
                <li>참여마당</li>
            </ul>
        </nav>
    </header>

    <div class="hero">
        <h1>우리 땅, 아름다운 독도</h1>
        <p>대한민국의 소중한 영토, 독도의 이야기를 만나보세요.</p>
    </div>

    <div class="container">
        <aside>
            <ul>
                <li class="active">Home</li>
                <li>독도란?</li>
                <li>역사 속 독도</li>
                <li>생태 이야기</li>
                <li>자료실 (PDF)</li>
                <li>실시간 영상</li>
            </ul>
        </aside>

        <section>
            <h2>주요 학습 내용</h2>
            <div class="card-grid">
                <div class="card">
                    <h3>1. 독도의 역사</h3>
                    <p>신라 지증왕 13년(512년) 이사부의 우산국 정복부터 대한제국 칙령 제41호까지, 역사적 문헌이 증명하는 독도.</p>
                </div>
                <div class="card">
                    <h3>2. 자연과 생태</h3>
                    <p>괭이갈매기, 강치(강치 복원 노력), 그리고 독도 주변 해역의 풍부한 해양 생태계 자원을 알아봅니다.</p>
                </div>
                <div class="card">
                    <h3>3. 교육 자료실</h3>
                    <p>학생들을 위한 독도 퀴즈와 선생님들을 위한 수업용 활동지를 다운로드할 수 있습니다.</p>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>Copyright © 2026 Dokdo Education Portal. All Rights Reserved.</p>
        <p>개인정보처리방침 | 이용약관</p>
    </footer>

</body>
</html>
