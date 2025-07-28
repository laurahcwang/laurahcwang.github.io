# laurahcwang.github.io
<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NVIDIA 2026 研發替代役招募海報</title>
    <!-- 引入 Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- 引入 Inter 字體 -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #e6f7ff; /* 淺藍色背景，更繽紛 */
            color: #2c3e50; /* 深藍灰色文字 */
            line-height: 1.6;
        }
        .poster-container {
            max-width: 900px;
            margin: 3rem auto;
            background-color: #ffffff;
            border-radius: 1.5rem; /* 更圓潤的邊角 */
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15); /* 更明顯的陰影 */
            overflow: hidden;
            padding: 2rem;
            border: 2px solid #28a745; /* 綠色邊框 */
        }
        .header-section {
            /* Changed from linear-gradient to solid NVIDIA green */
            background-color: #76B900; /* NVIDIA Green */
            color: #ffffff;
            padding: 2.5rem 2rem;
            border-top-left-radius: 1.25rem;
            border-top-right-radius: 1.25rem;
            text-align: center;
            position: relative;
            overflow: hidden;
            border-bottom: 5px solid #28a745; /* 綠色底線 */
        }
        .header-section::before {
            content: '';
            position: absolute;
            top: -50px;
            left: -50px;
            width: 200px;
            height: 200px;
            background: rgba(102, 255, 102, 0.1); /* 亮綠色半透明裝飾 */
            border-radius: 50%;
            transform: rotate(45deg);
        }
        .header-section::after {
            content: '';
            position: absolute;
            bottom: -50px;
            right: -50px;
            width: 150px;
            height: 150px;
            background: rgba(102, 255, 102, 0.15); /* 亮綠色半透明裝飾 */
            border-radius: 50%;
            transform: rotate(-30deg);
        }
        .section-block {
            background-color: #f0fdf4; /* 淺綠色背景 */
            border-radius: 1rem;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            border-left: 5px solid #28a745; /* 左側綠色邊框 */
        }
        .section-block:hover {
            transform: translateY(-8px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.12);
        }
        .section-title {
            color: #004d40; /* 深綠色標題 */
            font-weight: 800; /* 更粗的字體 */
            margin-bottom: 1rem;
            position: relative;
            padding-bottom: 0.5rem;
            font-size: 1.8rem; /* 增大標題字體 */
        }
        .section-title::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 70px; /* 更長的底線 */
            height: 5px; /* 更粗的底線 */
            background-color: #28a745; /* 綠色底線 */
            border-radius: 2px;
        }
        .job-link {
            color: #007bff; /* 亮藍色連結 */
            font-weight: 700;
            text-decoration: none;
            transition: color 0.2s ease-in-out, text-decoration 0.2s ease-in-out;
        }
        .job-link:hover {
            color: #0056b3; /* 深藍色懸停 */
            text-decoration: underline;
        }
        .bullet-point {
            color: #28a745; /* 綠色項目符號 */
            font-weight: bold;
            margin-right: 0.5rem;
        }
        .footer-section {
            background-color: #004d40; /* 深綠色 */
            color: #e0e0e0;
            padding: 1.5rem 2rem;
            border-bottom-left-radius: 1.25rem;
            border-bottom-right-radius: 1.25rem;
            text-align: center;
            font-size: 0.9rem;
            border-top: 5px solid #28a745; /* 綠色頂線 */
        }

        /* NVIDIA Tile Styling */
        .nvidia-tile {
            background: linear-gradient(to bottom right, #004d40, #00796b); /* 綠色漸變背景 */
            color: #ffffff;
            padding: 2rem;
            border-radius: 1.5rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 2.5rem;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }
        .nvidia-tile::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://placehold.co/800x400/000000/ffffff?text=NVIDIA+Pattern') no-repeat center center; /* 抽象圖案 */
            background-size: cover;
            opacity: 0.1;
            z-index: 0;
        }
        .nvidia-tile > * {
            position: relative;
            z-index: 1;
        }
        .nvidia-tile img {
            width: 120px; /* 調整圖片大小 */
            height: auto;
            margin-bottom: 1.5rem;
            border-radius: 50%; /* 圓形圖片 */
            border: 5px solid #28a745; /* 綠色邊框 */
            box-shadow: 0 0 15px rgba(0, 255, 0, 0.5); /* 綠色發光效果 */
        }
        .nvidia-tile h3 {
            font-size: 1.8rem;
            font-weight: 800;
            margin-bottom: 0.75rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        .nvidia-tile p {
            font-size: 1.1rem;
            line-height: 1.6;
            margin-bottom: 1.5rem;
            max-width: 600px;
        }
        .nvidia-tile a {
            display: inline-block;
            background-color: #28a745; /* 綠色按鈕 */
            color: #ffffff;
            padding: 0.85rem 2rem;
            border-radius: 2rem; /* 更圓潤的按鈕 */
            text-decoration: none;
            font-weight: 700;
            letter-spacing: 0.05em;
            transition: background-color 0.3s ease-in-out, transform 0.2s ease-in-out, box-shadow 0.3s ease-in-out;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
        }
        .nvidia-tile a:hover {
            background-color: #218838; /* 深綠色懸停 */
            transform: translateY(-3px);
            box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
        }

        /* Job Categories Grid Styling */
        .job-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* 響應式網格 */
            gap: 1.5rem; /* 間距 */
            margin-top: 1.5rem;
        }
        .job-card {
            background-color: #ffffff;
            border-radius: 1rem;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            border: 1px solid #e0e0e0;
        }
        .job-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
            border-color: #28a745; /* 懸停時邊框變綠 */
        }
        .job-card .icon {
            font-size: 3rem; /* 圖標大小 */
            margin-bottom: 1rem;
            color: #007bff; /* 藍色圖標 */
            transition: color 0.3s ease-in-out;
        }
        .job-card:hover .icon {
            color: #28a745; /* 懸停時圖標變綠 */
        }
        .job-card h4 {
            font-size: 1.15rem;
            font-weight: 700;
            color: #2c3e50;
            margin-bottom: 1rem;
        }
        .job-card a {
            display: inline-block;
            background-color: #007bff; /* 藍色按鈕 */
            color: #ffffff;
            padding: 0.6rem 1.2rem;
            border-radius: 0.5rem;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s ease-in-out, transform 0.2s ease-in-out;
        }
        .job-card a:hover {
            background-color: #0056b3; /* 深藍色懸停 */
            transform: translateY(-2px);
        }

        /* Responsive adjustments for job grid */
        @media (max-width: 640px) {
            .job-grid {
                grid-template-columns: 1fr; /* 單列佈局 */
            }
        }
    </style>
</head>
<body>
    <div class="poster-container">
        <header class="header-section">
            <!-- NVIDIA Logo removed, using NVIDIA green background instead -->
            <h1 class="text-4xl font-extrabold mb-2 tracking-wide">NVIDIA 2026 研發替代役招募</h1>
            <p class="text-xl font-light opacity-90">引領人工智慧與高效能運算的未來</p>
        </header>

        <main class="p-6">
            <!-- NVIDIA Tile Section -->
            <section class="nvidia-tile">
                <!-- Placeholder for a more relevant AI/GPU icon if available, otherwise a generic one -->
                <img src="https://placehold.co/120x120/28a745/ffffff?text=AI+GPU" alt="NVIDIA AI Tile" class="rounded-full shadow-md">
                <h3>關於 NVIDIA</h3>
                <p>NVIDIA (輝達) 成立於 1993 年，是全球視覺運算技術的領導者，也是 GPU (繪圖處理器) 的發明者。我們的技術加速了科學研究、產品設計、遊戲體驗以及人工智慧的發展。</p>
                <a href="https://nvidia.wd5.myworkdayjobs.com/NVIDIAExternalCareerSite" target="_blank" class="job-link">了解更多 NVIDIA</a>
            </section>

            <!-- Recruitment Eligibility -->
            <section class="section-block">
                <h2 class="section-title">研發替代役申請資格</h2>
                <p class="mb-4 text-gray-700">申請 NVIDIA 2026 研發替代役，您必須符合以下兩項條件：</p>
                <ul class="list-none space-y-2 text-gray-700">
                    <li><span class="bullet-point">●</span> <strong class="text-gray-900">2026 年應屆畢業生</strong>：預計於 2026 年畢業的學士或碩士生。</li>
                    <li><span class="bullet-point">●</span> <strong class="text-gray-900">符合 2026 年研發替代役體位並與區公所確定資格</strong>：請務必提前向區公所確認您的研發替代役資格。</li>
                </ul>
            </section>

            <!-- Application Method -->
            <section class="section-block">
                <h2 class="section-title">應徵方式</h2>
                <p class="mb-4 text-gray-700">請準備以下資料，並透過 104 投遞履歷：</p>
                <ul class="list-none space-y-2 text-gray-700">
                    <li><span class="bullet-point">●</span> <strong class="text-gray-900">英文個人履歷</strong></li>
                    <li><span class="bullet-point">●</span> <strong class="text-gray-900">學士及碩士成績單</strong> (中英文皆可)</li>
                </ul>
            </section>

            <!-- Job Openings Grid -->
            <section class="section-block">
                <h2 class="section-title">職缺列表</h2>
                <p class="mb-4 text-gray-700">我們提供以下 9 個領域的研發替代役職缺，歡迎有志之士投遞履歷：</p>
                <div class="job-grid">
                    <!-- Job Card 1 -->
                    <div class="job-card">
                        <span class="icon">💻</span> <!-- Placeholder icon -->
                        <h4>Physical Design/EDA tools Design 數位 IC 設計工程師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 2 -->
                    <div class="job-card">
                        <span class="icon">🔌</span> <!-- Placeholder icon -->
                        <h4>Mixed Signal Design Engineer 類比設計工程師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 3 -->
                    <div class="job-card">
                        <span class="icon">⚡</span> <!-- Placeholder icon -->
                        <h4>Signal and Power Integrity Engineer</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 4 -->
                    <div class="job-card">
                        <span class="icon">🤖</span> <!-- Placeholder icon -->
                        <h4>軟體工程師 System Software/Android Software/AI Algorithm (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 5 -->
                    <div class="job-card">
                        <span class="icon">⚙️</span> <!-- Placeholder icon -->
                        <h4>Firmware Engineer 韌體工程師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 6 -->
                    <div class="job-card">
                        <span class="icon">💻</span> <!-- Changed from 🧪 to 💻 -->
                        <h4>Test Development Engineer 軟體測試開發工程師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 7 -->
                    <div class="job-card">
                        <span class="icon">🔬</span> <!-- Placeholder icon -->
                        <h4>Test Engineer/ Product Engineer/ Silicon Validation Engineer 測試/產品/驗證工程師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 8 -->
                    <div class="job-card">
                        <span class="icon">📊</span> <!-- Placeholder icon -->
                        <h4>System Analyst 系統分析師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                    <!-- Job Card 9 -->
                    <div class="job-card">
                        <span class="icon">⚡</span> <!-- Placeholder icon -->
                        <h4>System Power Validation/PCB Layout 系統電源驗證/佈線工程師 (多方向)</h4>
                        <a href="https://www.104.com.tw/company/1a2x6bm42t?job=RDSS&page=1&pageSize=20&order=8&asc=0#info06" target="_blank">立即應徵</a>
                    </div>
                </div>
            </section>

            <!-- Submission Instructions -->
            <section class="section-block text-center">
                <h2 class="section-title inline-block">提交申請</h2>
                <p class="mb-4 text-gray-700">
                    請將上述所需資料透過 104 連結投遞。我們將會審核您的申請，符合資格者將會收到進一步的聯繫通知。
                </p>
                <p class="text-xl font-bold text-gray-900 leading-relaxed mt-6">
                    期待您的加入，與 NVIDIA 一同開創無限可能！
                </p>
            </section>
        </main>

        <footer class="footer-section">
            <p>&copy; 2025 NVIDIA Corporation. All rights reserved.</p>
        </footer>
    </div>
</body>
</html>

