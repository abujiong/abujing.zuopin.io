[未命名.html](https://github.com/user-attachments/files/26074426/default.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>视觉作品集 | 平面设计师</title>
    <style>
        /* 全局样式重置 & 基础变量 */
        :root {
            --primary: #ff3d00;
            --secondary: #212121;
            --light: #f5f5f5;
            --dark: #121212;
            --gray: #888888;
            --transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', 'Noto Sans SC', sans-serif;
        }

        body {
            background-color: var(--light);
            color: var(--secondary);
            overflow-x: hidden;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        .container {
            width: 90%;
            max-width: 1400px;
            margin: 0 auto;
        }

        /* 导航栏 - 极简悬浮设计 */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 2rem 0;
            z-index: 1000;
            transition: var(--transition);
        }

        nav.scrolled {
            background-color: rgba(255, 255, 255, 0.95);
            padding: 1rem 0;
            box-shadow: 0 2px 20px rgba(0, 0, 0, 0.05);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 800;
            letter-spacing: -1px;
            color: var(--primary);
        }

        .nav-links {
            display: flex;
            gap: 3rem;
            font-weight: 500;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-size: 0.9rem;
        }

        .nav-links a {
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -4px;
            left: 0;
            background-color: var(--primary);
            transition: var(--transition);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        /* 英雄区 - 设计师风格全屏展示 */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
        }

        .hero-content {
            flex: 1;
            z-index: 2;
            padding: 0 5rem;
        }

        .hero-title {
            font-size: clamp(3rem, 8vw, 6rem);
            line-height: 1.1;
            font-weight: 900;
            margin-bottom: 1.5rem;
            letter-spacing: -2px;
        }

        .hero-title span {
            color: var(--primary);
        }

        .hero-subtitle {
            font-size: clamp(1.2rem, 3vw, 1.8rem);
            color: var(--gray);
            max-width: 600px;
            margin-bottom: 2rem;
            line-height: 1.6;
        }

        .hero-cta {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: var(--transition);
            box-shadow: 0 10px 30px rgba(255, 61, 0, 0.3);
        }

        .hero-cta:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 30px rgba(255, 61, 0, 0.4);
        }

        .hero-img {
            flex: 1;
            height: 100%;
            position: relative;
        }

        .hero-img img {
            position: absolute;
            top: 50%;
            right: 0;
            transform: translateY(-50%);
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.15);
            z-index: 1;
        }

        /* 装饰元素 */
        .hero-decor {
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, var(--primary) 0%, rgba(255, 61, 0, 0.1) 70%);
            border-radius: 50%;
            filter: blur(80px);
            z-index: 0;
            right: 10%;
            top: 50%;
            transform: translateY(-50%);
            opacity: 0.5;
        }

        /* 通用板块样式 */
        section {
            padding: 8rem 0;
            position: relative;
        }

        .section-title {
            text-align: center;
            margin-bottom: 5rem;
        }

        .section-title h2 {
            font-size: clamp(2rem, 5vw, 3.5rem);
            font-weight: 800;
            position: relative;
            display: inline-block;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            width: 60%;
            height: 4px;
            background-color: var(--primary);
            bottom: -10px;
            left: 20%;
        }

        .section-title p {
            color: var(--gray);
            margin-top: 1.5rem;
            font-size: 1.1rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        /* 关于我 - 设计师风格 */
        .about {
            background-color: white;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-img {
            position: relative;
        }

        .about-img img {
            width: 100%;
            border-radius: 10px;
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
        }

        .about-img::after {
            content: '';
            position: absolute;
            width: 80%;
            height: 80%;
            border: 3px solid var(--primary);
            border-radius: 10px;
            top: -20px;
            left: -20px;
            z-index: -1;
        }

        .about-text h3 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
        }

        .about-text p {
            font-size: 1.1rem;
            line-height: 1.8;
            color: var(--gray);
            margin-bottom: 2rem;
        }

        .about-skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 2rem;
        }

        .skill-tag {
            background-color: var(--light);
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            font-weight: 500;
            transition: var(--transition);
        }

        .skill-tag:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-3px);
        }

        /* 作品展示 - 核心模块 */
        .portfolio {
            background-color: var(--light);
        }

        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }

        .portfolio-item {
            position: relative;
            border-radius: 10px;
            overflow: hidden;
            cursor: pointer;
            height: 400px;
        }

        .portfolio-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: var(--transition);
        }

        .portfolio-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(0,0,0,0) 0%, rgba(0,0,0,0.8) 100%);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            padding: 2rem;
            color: white;
            opacity: 0;
            transition: var(--transition);
            transform: translateY(20px);
        }

        .portfolio-item:hover .portfolio-overlay {
            opacity: 1;
            transform: translateY(0);
        }

        .portfolio-item:hover .portfolio-img {
            transform: scale(1.05);
        }

        .portfolio-category {
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }

        .portfolio-title {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        /* 服务板块 */
        .services {
            background-color: white;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            padding: 3rem 2rem;
            border-radius: 10px;
            background-color: var(--light);
            transition: var(--transition);
            text-align: center;
        }

        .service-card:hover {
            background-color: var(--primary);
            color: white;
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(255, 61, 0, 0.2);
        }

        .service-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
            transition: var(--transition);
        }

        .service-card:hover .service-icon {
            color: white;
            transform: scale(1.1);
        }

        .service-title {
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .service-desc {
            color: var(--gray);
            line-height: 1.7;
            transition: var(--transition);
        }

        .service-card:hover .service-desc {
            color: white;
        }

        /* 联系方式 */
        .contact {
            background-color: var(--dark);
            color: white;
            padding: 8rem 0 4rem;
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
        }

        .contact-info h3 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 2rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1.5rem;
            margin-bottom: 2rem;
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--primary);
        }

        .contact-text h4 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
        }

        .contact-text p {
            color: var(--gray);
        }

        .contact-social {
            display: flex;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .social-icon {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .social-icon:hover {
            background-color: var(--primary);
            transform: translateY(-5px);
        }

        /* 页脚 */
        footer {
            background-color: var(--dark);
            color: var(--gray);
            padding: 2rem 0;
            text-align: center;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* 响应式适配 */
        @media (max-width: 1024px) {
            .hero {
                flex-direction: column;
                height: auto;
                padding: 10rem 0 5rem;
            }
            
            .hero-content {
                padding: 0 2rem;
                margin-bottom: 3rem;
                text-align: center;
            }
            
            .hero-img img {
                position: static;
                transform: none;
                max-width: 100%;
            }
            
            .about-content, .contact-content {
                grid-template-columns: 1fr;
            }
            
            .about-img {
                max-width: 80%;
                margin: 0 auto;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                gap: 1.5rem;
            }
            
            section {
                padding: 5rem 0;
            }
            
            .portfolio-grid {
                grid-template-columns: 1fr;
            }
            
            .hero-decor {
                width: 300px;
                height: 300px;
            }
        }

        @media (max-width: 480px) {
            .nav-links {
                display: none;
            }
            
            .hero-title {
                font-size: clamp(2rem, 10vw, 4rem);
            }
            
            .section-title {
                margin-bottom: 3rem;
            }
            
            .portfolio-item {
                height: 300px;
            }
        }
    </style>
    <!-- 引入字体图标 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- 引入谷歌字体 -->
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700;800;900&family=Noto+Sans+SC:wght@400;500;700;900&display=swap" rel="stylesheet">
</head>
<body>
    <!-- 导航栏 -->
    <nav id="navbar">
        <div class="container nav-container">
            <div class="logo">DESIGNER</div>
            <ul class="nav-links">
                <li><a href="#home">首页</a></li>
                <li><a href="#about">关于我</a></li>
                <li><a href="#portfolio">作品集</a></li>
                <li><a href="#services">服务</a></li>
                <li><a href="#contact">联系我</a></li>
            </ul>
        </div>
    </nav>

    <!-- 英雄区 -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1 class="hero-title">
                    视觉<span>设计</span><br>
                    赋予品牌灵魂
                </h1>
                <p class="hero-subtitle">
                    专注品牌视觉设计、UI/UX设计、插画设计，用设计创造商业价值
                </p>
                <a href="#portfolio" class="hero-cta">查看作品集</a>
            </div>
            <div class="hero-img">
                <img src="https://images.unsplash.com/photo-1551434678-e076c223a692?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="设计师工作台">
                <div class="hero-decor"></div>
            </div>
        </div>
    </section>

    <!-- 关于我 -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>关于我</h2>
                <p>5年平面设计经验，专注于品牌视觉与商业设计，擅长将创意转化为有效的视觉语言</p>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80" alt="个人形象">
                </div>
                <div class="about-text">
                    <h3>用设计解决问题</h3>
                    <p>
                        我是一名资深平面设计师，毕业于XX设计学院视觉传达专业，拥有5年专业设计经验。曾服务于多家知名企业，涵盖电商、科技、文创等多个领域。
                    </p>
                    <p>
                        我的设计理念是：设计不仅是美学的表达，更是解决商业问题的工具。我擅长从品牌战略出发，结合用户体验，创造既有视觉冲击力又有商业价值的设计作品。
                    </p>
                    <div class="about-skills">
                        <span class="skill-tag">品牌设计</span>
                        <span class="skill-tag">LOGO设计</span>
                        <span class="skill-tag">画册设计</span>
                        <span class="skill-tag">包装设计</span>
                        <span class="skill-tag">UI设计</span>
                        <span class="skill-tag">插画设计</span>
                        <span class="skill-tag">海报设计</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 作品展示 -->
    <section id="portfolio" class="portfolio">
        <div class="container">
            <div class="section-title">
                <h2>精选作品</h2>
                <p>每一个作品都凝聚着创意与思考，用视觉语言讲述品牌故事</p>
            </div>
            <div class="portfolio-grid">
                <!-- 作品1 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1587614382346-4ec70e388b28?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="品牌VI设计" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <span class="portfolio-category">品牌设计</span>
                        <h3 class="portfolio-title">科技品牌VI全案设计</h3>
                    </div>
                </div>
                <!-- 作品2 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1622890866663-68fc77190547?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="包装设计" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <span class="portfolio-category">包装设计</span>
                        <h3 class="portfolio-title">食品品牌包装升级设计</h3>
                    </div>
                </div>
                <!-- 作品3 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1526506118085-60ce8714f8c5?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="海报设计" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <span class="portfolio-category">海报设计</span>
                        <h3 class="portfolio-title">文创产品推广海报设计</h3>
                    </div>
                </div>
                <!-- 作品4 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1547333590-47fae5f58975?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="UI设计" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <span class="portfolio-category">UI设计</span>
                        <h3 class="portfolio-title">电商APP界面设计</h3>
                    </div>
                </div>
                <!-- 作品5 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1619241638225-14d56e47ae64?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="画册设计" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <span class="portfolio-category">画册设计</span>
                        <h3 class="portfolio-title">企业年度画册设计</h3>
                    </div>
                </div>
                <!-- 作品6 -->
                <div class="portfolio-item">
                    <img src="https://images.unsplash.com/photo-1585386959984-a4155224a1ad?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="LOGO设计" class="portfolio-img">
                    <div class="portfolio-overlay">
                        <span class="portfolio-category">LOGO设计</span>
                        <h3 class="portfolio-title">餐饮品牌LOGO设计</h3>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 服务板块 -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-title">
                <h2>我的服务</h2>
                <p>提供全方位的视觉设计服务，满足不同场景的设计需求</p>
            </div>
            <div class="services-grid">
                <!-- 服务1 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-pen-fancy"></i>
                    </div>
                    <h3 class="service-title">品牌视觉设计</h3>
                    <p class="service-desc">LOGO设计、VI系统设计、品牌手册、品牌升级，打造独特的品牌视觉形象</p>
                </div>
                <!-- 服务2 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-box"></i>
                    </div>
                    <h3 class="service-title">包装设计</h3>
                    <p class="service-desc">产品包装、礼盒设计、标签设计，提升产品附加值和市场竞争力</p>
                </div>
                <!-- 服务3 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-desktop"></i>
                    </div>
                    <h3 class="service-title">UI/UX设计</h3>
                    <p class="service-desc">APP界面、网页设计、小程序设计，兼顾美观与用户体验</p>
                </div>
                <!-- 服务4 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-images"></i>
                    </div>
                    <h3 class="service-title">平面物料设计</h3>
                    <p class="service-desc">海报、画册、宣传单页、展架、名片等各类印刷物料设计</p>
                </div>
                <!-- 服务5 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h3 class="service-title">插画设计</h3>
                    <p class="service-desc">商业插画、品牌插画、包装插画、社交媒体插画，赋予品牌个性</p>
                </div>
                <!-- 服务6 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3 class="service-title">设计咨询</h3>
                    <p class="service-desc">品牌视觉诊断、设计策略规划、设计团队培训，提供专业建议</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 联系方式 -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>联系我</h2>
                <p>期待与您合作，共同创造有价值的设计作品</p>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>随时沟通</h3>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone"></i>
                        </div>
                        <div class="contact-text">
                            <h4>电话</h4>
                            <p>138-XXXX-XXXX</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h4>邮箱</h4>
                            <p>design@example.com</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h4>地址</h4>
                            <p>上海市XX区XX路XX号创意园A座501</p>
                        </div>
                    </div>
                    <div class="contact-social">
                        <a href="#" class="social-icon"><i class="fab fa-behance"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-dribbble"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-icon"><i class="fab fa-weixin"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 页脚 -->
    <footer>
        <div class="container">
            <p>&copy; 2026 平面设计师个人作品集 | 用设计创造价值</p>
        </div>
    </footer>

    <script>
        // 导航栏滚动效果
        window.addEventListener('scroll', function() {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // 平滑滚动
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
