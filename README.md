<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>未来科技教育 | FunMA & STEAM</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+SC:wght@300;400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            /* 品牌色系定义 */
            --primary: #2563EB;      /* 科技蓝：主色调 */
            --secondary: #0F172A;    /* 深邃黑：文字与背景 */
            --accent-funma: #F59E0B; /* 活力橙：FunMA */
            --accent-steam: #10B981; /* 探索绿：STEAM */
            --accent-custom: #8B5CF6;/* 智慧紫：客制化 */
            --bg-light: #F8FAFC;
            --white: #FFFFFF;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Noto Sans SC', sans-serif;
            color: var(--secondary);
            line-height: 1.6;
            background-color: var(--white);
        }

        /* 导航栏 */
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.5rem 5%;
            background: rgba(255, 255, 255, 0.95);
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            text-decoration: none;
            color: var(--secondary);
            font-weight: 500;
            transition: color 0.3s;
        }

        nav a:hover {
            color: var(--primary);
        }

        .btn {
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: transform 0.2s, box-shadow 0.2s;
            display: inline-block;
        }

        .btn-primary {
            background-color: var(--primary);
            color: var(--white);
        }

        .btn-outline {
            border: 2px solid var(--primary);
            color: var(--primary);
            margin-left: 10px;
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(37, 99, 235, 0.3);
        }

        /* Hero 区域 */
        .hero {
            padding: 6rem 5% 4rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: linear-gradient(135deg, #EFF6FF 0%, #FFFFFF 100%);
            min-height: 80vh;
        }

        .hero-text {
            flex: 1;
            max-width: 600px;
        }

        .hero h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            color: var(--secondary);
        }

        .hero h1 span {
            color: var(--primary);
        }

        .hero p {
            font-size: 1.2rem;
            color: #64748B;
            margin-bottom: 2rem;
        }

        .hero-image {
            flex: 1;
            display: flex;
            justify-content: center;
            position: relative;
        }

        /* 模拟软件界面的占位符 */
        .mockup {
            width: 90%;
            height: 400px;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 50px rgba(0,0,0,0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            border: 1px solid #E2E8F0;
            position: relative;
            overflow: hidden;
        }
        
        /* 简单的装饰性背景圆 */
        .blob {
            position: absolute;
            width: 300px;
            height: 300px;
            background: rgba(37, 99, 235, 0.1);
            border-radius: 50%;
            z-index: -1;
            right: 0;
            top: 0;
        }

        /* 服务板块 */
        .services {
            padding: 5rem 5%;
            background-color: var(--bg-light);
        }

        .section-title {
            text-align: center;
            margin-bottom: 4rem;
        }

        .section-title h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .cards-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: white;
            padding: 3rem 2rem;
            border-radius: 16px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
            border: 1px solid #F1F5F9;
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.08);
        }

        .service-card::top {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 6px;
        }

        .card-funma { border-top: 6px solid var(--accent-funma); }
        .card-steam { border-top: 6px solid var(--accent-steam); }
        .card-custom { border-top: 6px solid var(--accent-custom); }

        .icon-box {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .bg-funma { background: #FEF3C7; color: var(--accent-funma); }
        .bg-steam { background: #D1FAE5; color: var(--accent-steam); }
        .bg-custom { background: #EDE9FE; color: var(--accent-custom); }

        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }

        .service-card ul {
            list-style: none;
            margin-top: 1.5rem;
        }

        .service-card li {
            margin-bottom: 0.8rem;
            display: flex;
            align-items: center;
            gap: 10px;
            color: #64748B;
        }

        /* FunMA 特色展示区 */
        .feature-split {
            padding: 5rem 5%;
            display: flex;
            align-items: center;
            gap: 4rem;
        }

        .feature-content h2 {
            font-size: 2.2rem;
            margin-bottom: 1rem;
        }

        .stats-bar {
            background: var(--secondary);
            color: white;
            padding: 3rem 5%;
            display: flex;
            justify-content: space-around;
            text-align: center;
        }

        .stat-item h4 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        footer {
            background: #F1F5F9;
            padding: 2rem 5%;
            text-align: center;
            color: #64748B;
            font-size: 0.9rem;
        }

        /* 移动端适配 */
        @media (max-width: 768px) {
            .hero {
                flex-direction: column;
                text-align: center;
                padding-top: 3rem;
            }
            
            .hero-image {
                margin-top: 3rem;
                width: 100%;
            }

            .feature-split {
                flex-direction: column-reverse;
            }
            
            nav { display: none; } /* 简化演示，隐藏导航 */
            
            .stats-bar {
                flex-direction: column;
                gap: 2rem;
            }
        }
    </style>
</head>
<body>

    <header>
        <div class="logo">
            <i class="fa-solid fa-shapes"></i> TechEdu
        </div>
        <nav>
            <ul>
                <li><a href="#">首页</a></li>
                <li><a href="#">FunMA软件</a></li>
                <li><a href="#">STEAM课程</a></li>
                <li><a href="#">企业定制</a></li>
            </ul>
        </nav>
        <a href="#" class="btn btn-primary">免费试用</a>
    </header>

    <section class="hero">
        <div class="hero-text">
            <h1>用科技点燃好奇心<br><span>定义未来学习方式</span></h1>
            <p>我们提供个性化数学软件、沉浸式 STEAM 课程以及专业的教育定制服务，赋能每一位学生与教育者。</p>
            <div>
                <a href="#" class="btn btn-primary">体验 FunMA</a>
                <a href="#" class="btn btn-outline">了解课程</a>
            </div>
        </div>
        <div class="hero-image">
            <div class="blob"></div>
            <div class="mockup">
                <div style="text-align:center;">
                    <i class="fa-solid fa-chart-pie" style="font-size: 4rem; color: var(--primary); margin-bottom: 1rem;"></i>
                    <h3 style="color: #64748B;">FunMA 智能分析界面</h3>
                </div>
            </div>
        </div>
    </section>

    <section class="stats-bar">
        <div class="stat-item">
            <h4>10,000+</h4>
            <p>服务学生</p>
        </div>
        <div class="stat-item">
            <h4>95%</h4>
            <p>成绩提升率</p>
        </div>
        <div class="stat-item">
            <h4>50+</h4>
            <p>合作学校</p>
        </div>
    </section>

    <section class="services">
        <div class="section-title">
            <h2>全方位的科技教育解决方案</h2>
            <p>针对不同需求，提供最专业的教育产品与服务</p>
        </div>

        <div class="cards-container">
            <div class="service-card card-funma">
                <div class="icon-box bg-funma">
                    <i class="fa-solid fa-calculator"></i>
                </div>
                <h3>FunMA 数学软件</h3>
                <p>专为 K-12 设计的互动式数学学习平台，利用 AI 算法实现真正的千人千面。</p>
                <ul>
                    <li><i class="fa-solid fa-check"></i> AI 智能诊断薄弱点</li>
                    <li><i class="fa-solid fa-check"></i> 游戏化闯关机制</li>
                    <li><i class="fa-solid fa-check"></i> 实时生成学习报告</li>
                </ul>
            </div>

            <div class="service-card card-steam">
                <div class="icon-box bg-steam">
                    <i class="fa-solid fa-flask"></i>
                </div>
                <h3>STEAM 课程</h3>
                <p>融合科学、技术、工程、艺术与数学，在动手实践中培养解决问题的能力。</p>
                <ul>
                    <li><i class="fa-solid fa-check"></i> 跨学科项目制学习</li>
                    <li><i class="fa-solid fa-check"></i> 丰富的实验教具包</li>
                    <li><i class="fa-solid fa-check"></i> 定期举办科创竞赛</li>
                </ul>
            </div>

            <div class="service-card card-custom">
                <div class="icon-box bg-custom">
                    <i class="fa-solid fa-handshake"></i>
                </div>
                <h3>B2B 客制化服务</h3>
                <p>为学校和教育机构提供从课程开发到数字化转型的一站式解决方案。</p>
                <ul>
                    <li><i class="fa-solid fa-check"></i> 校本课程定制开发</li>
                    <li><i class="fa-solid fa-check"></i> 师资培训与认证</li>
                    <li><i class="fa-solid fa-check"></i> 校园创客空间建设</li>
                </ul>
            </div>
        </div>
    </section>

    <section class="feature-split">
        <div class="hero-image">
            <div class="mockup" style="border-radius: 30px; border: 8px solid #333; height: 350px;">
                <div style="display:flex; align-items:center; justify-content:center; height:100%; flex-direction:column; background:#f0f9ff;">
                    <i class="fa-solid fa-rocket" style="font-size: 3rem; color: var(--accent-funma);"></i>
                    <p style="margin-top:10px; font-weight:bold;">闯关成功！</p>
                </div>
            </div>
        </div>
        <div class="feature-content">
            <span style="color: var(--primary); font-weight: bold; text-transform: uppercase; letter-spacing: 1px;">FunMA Highlight</span>
            <h2>让数学不再枯燥</h2>
            <p>FunMA 不仅仅是一个题库，它是孩子的私人数学教练。通过独特的互动界面和即时反馈机制，我们帮助孩子建立数学自信。</p>
            <br>
            <p style="color: #64748B;">“使用 FunMA 后，孩子第一次主动要求做数学题。” —— 来自一位小学家长的反馈</p>
            <br>
            <a href="#" class="btn btn-primary" style="background-color: var(--secondary);">查看产品演示 <i class="fa-solid fa-arrow-right"></i></a>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 TechEdu Inc. All Rights Reserved. 科技点亮教育未来。</p>
    </footer>

</body>
</html>
