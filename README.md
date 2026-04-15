<!DOCTYPE html>
<html lang="vi">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <meta name="description" content="Thiết kế web chuyên nghiệp - Ngoc Minh Web Design">
    <meta name="keywords" content="web design, professional web design, thiet ke web, thiet ke web chuyen nghiep">
    <meta name="author" content="Ngoc Minh">
    <title>Ngoc Minh Web Design | Trang chủ</title>
    <style>
        /* ========== RESET & GLOBAL ========== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Arial, Helvetica, sans-serif;
            background: #fff7ed;
            color: #222;
            line-height: 1.5;
        }

        .container {
            width: 85%;
            max-width: 1200px;
            margin: auto;
            overflow: hidden;
        }

        ul {
            list-style: none;
            padding: 0;
        }

        .button_1 {
            background: #f97316;
            color: #fff;
            border: 0;
            padding: 10px 20px;
            border-radius: 40px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
            display: inline-block;
            border: none;
        }

        .button_1:hover {
            background: #ea580c;
            transform: scale(1.02);
        }

        .dark {
            background: #7c2d12;
            color: #fff;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
        }

        /* ========== HEADER ========== */
        header {
            background: #fb923c;
            color: #fff;
            padding: 20px 0;
            border-bottom: 4px solid #f97316;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        header .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }

        header #branding h1 {
            margin: 0;
            font-size: 1.9rem;
            letter-spacing: 1px;
        }

        header .highlight {
            color: #4c1d95;
            background: rgba(255, 255, 240, 0.2);
            padding: 0 5px;
            border-radius: 12px;
        }

        header nav ul {
            display: flex;
            gap: 20px;
        }

        header nav ul li a {
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            padding: 8px 12px;
            border-radius: 30px;
            transition: 0.2s;
        }

        header nav ul li.current a,
        header nav ul li a:hover {
            background: #4c1d95;
            color: #fff;
        }

        /* ========== SHOWCASE (HOME) ========== */
        #showcase {
            background: linear-gradient(135deg, #f97316, #ec4899, #8b5cf6);
            color: white;
            text-align: center;
            padding: 80px 20px;
            border-radius: 0 0 40px 40px;
            margin-bottom: 30px;
        }

        #showcase h1 {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        #showcase p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
        }

        /* ========== NEWSLETTER ========== */
        #newsletter {
            background: #ffe4e6;
            padding: 30px 20px;
            border-radius: 28px;
            margin: 30px 0;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
        }

        #newsletter .container {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 20px;
        }

        #newsletter h1 {
            font-size: 1.5rem;
            color: #4c1d95;
        }

        #newsletter form {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
        }

        #newsletter input[type="email"] {
            padding: 12px 18px;
            border-radius: 50px;
            border: 1px solid #f97316;
            width: 260px;
            font-size: 1rem;
            outline: none;
        }

        /* ========== MAIN LAYOUT (dynamic pages) ========== */
        .main-col {
            width: 65%;
            float: left;
            margin-bottom: 30px;
        }

        .sidebar {
            width: 30%;
            float: right;
            margin-bottom: 30px;
        }

        .sidebar .quote input,
        .sidebar .quote textarea {
            width: 100%;
            padding: 10px;
            margin: 8px 0;
            border-radius: 20px;
            border: 1px solid #f97316;
            font-family: inherit;
        }

        .sidebar .quote button {
            margin-top: 10px;
            width: 100%;
        }

        /* clearfix */
        .clearfix::after {
            content: "";
            display: table;
            clear: both;
        }

        /* ========== BOXES (home) ========== */
        #boxes {
            display: flex;
            flex-wrap: wrap;
            gap: 2%;
            margin-top: 30px;
        }

        #boxes .box {
            flex: 1;
            min-width: 250px;
            background: white;
            padding: 25px 15px;
            text-align: center;
            border-radius: 28px;
            border: 2px solid #f97316;
            transition: 0.2s;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.05);
        }

        #boxes .box img {
            width: 70px;
            height: auto;
            margin-bottom: 15px;
        }

        #boxes .box h3 {
            margin: 15px 0 10px;
            color: #4c1d95;
        }

        /* ========== SERVICES LIST (dịch vụ) ========== */
        ul#services {
            list-style: none;
            padding: 0;
        }

        ul#services li {
            background: white;
            margin-bottom: 20px;
            padding: 20px;
            border-left: 8px solid #ec4899;
            border-radius: 20px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
        }

        ul#services li h3 {
            color: #f97316;
            margin-bottom: 8px;
        }

        /* ========== PAGE CONTAINERS (toggling) ========== */
        .page {
            display: none;
            animation: fade 0.25s ease;
        }

        .page.active-page {
            display: block;
        }

        @keyframes fade {
            from {
                opacity: 0;
                transform: translateY(8px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ========== FOOTER ========== */
        footer {
            background: #4c1d95;
            color: white;
            text-align: center;
            padding: 22px;
            margin-top: 40px;
            border-radius: 30px 30px 0 0;
            font-weight: 500;
        }

        /* ========== RESPONSIVE ========== */
        @media (max-width: 850px) {
            .container {
                width: 92%;
            }

            header .container {
                flex-direction: column;
                gap: 15px;
            }

            .main-col,
            .sidebar {
                width: 100%;
                float: none;
            }

            #boxes {
                flex-direction: column;
            }

            #newsletter .container {
                flex-direction: column;
                text-align: center;
            }

            #showcase h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>

<body>

    <header>
        <div class="container">
            <div id="branding">
                <h1><span class="highlight">Ngoc Minh</span> Web Design</h1>
            </div>
            <nav>
                <ul>
                    <li id="nav-home" class="current"><a href="#" data-page="home">Trang chủ</a></li>
                    <li id="nav-about"><a href="#" data-page="about">Thông tin</a></li>
                    <li id="nav-services"><a href="#" data-page="services">Dịch vụ</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- NEWSLETTER (common section) -->
    <section id="newsletter">
        <div class="container">
            <h1>📧 Đăng ký để nhận thông báo mới từ chúng tôi</h1>
            <form id="newsletterForm">
                <input type="email" placeholder="Nhập Email..." required>
                <button type="submit" class="button_1">Đăng ký</button>
            </form>
        </div>
    </section>

    <!-- ========== DYNAMIC PAGES CONTAINER ========== -->
    <div class="container clearfix" id="pageContainer">
        <!-- TRANG CHỦ (HOME) -->
        <div id="homePage" class="page active-page">
            <section id="showcase">
                <div class="container">
                    <h1>🚀 Thiết kế website chuyên nghiệp.</h1>
                    <p>Chúng tôi cung cấp các dịch vụ thiết kế website chuyên nghiệp, giá cả hợp lý theo yêu cầu khách
                        hàng.</p>
                </div>
            </section>

            <section id="boxes">
                <div class="box">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%23E44D26'/%3E%3Ctext x='50' y='67' font-size='28' text-anchor='middle' fill='white' font-weight='bold'%3EHTML5%3C/text%3E%3C/svg%3E"
                        alt="HTML5">
                    <h3>Ngôn ngữ HTML5</h3>
                    <p>HTML5 là ngôn ngữ cấu trúc và trình bày nội dung cho World Wide Web, công nghệ cốt lõi của
                        Internet hiện đại.</p>
                </div>
                <div class="box">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect width='100' height='100' fill='%23264de4'/%3E%3Ctext x='50' y='67' font-size='28' text-anchor='middle' fill='white' font-weight='bold'%3ECSS3%3C/text%3E%3C/svg%3E"
                        alt="CSS3">
                    <h3>Ngôn ngữ CSS3</h3>
                    <p>CSS3 là phiên bản nâng cao của CSS, tạo kiểu và định dạng trang web chuyên nghiệp, hỗ trợ bởi mọi
                        trình duyệt.</p>
                </div>
                <div class="box">
                    <img src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Ccircle cx='50' cy='50' r='48' fill='%23f97316'/%3E%3Ctext x='50' y='67' font-size='34' text-anchor='middle' fill='white' font-weight='bold'%3E✎%3C/text%3E%3C/svg%3E"
                        alt="Đồ họa">
                    <h3>Thiết kế đồ họa</h3>
                    <p>Thiết kế đồ họa sáng tạo, trực quan, đẳng cấp — giúp thương hiệu của bạn bùng nổ.</p>
                </div>
            </section>
        </div>

        <!-- THÔNG TIN (ABOUT) -->
        <div id="aboutPage" class="page">
            <article class="main-col">
                <h1 class="page-title" style="color:#4c1d95;">📌 Về chúng tôi</h1>
                <p style="font-size:1.05rem;">Chúng tôi luôn lắng nghe nhu cầu, tạo ra những ý tưởng đột phá mới giúp
                    hơn 2.300 khách hàng thành công.</p>
                <div class="dark" style="margin-top:20px;">
                    Về sáng tạo, chúng tôi có hơn 10 năm kinh nghiệm xây dựng chiến lược web cho công ty, thương mại
                    điện tử và tập đoàn. Về công nghệ, chúng tôi phát triển những trang web vượt trội, giải pháp
                    e-commercial, quảng cáo web, dịch vụ web…
                </div>
            </article>

            <aside class="sidebar">
                <div class="dark">
                    <h3>✨ Dịch vụ chúng tôi</h3>
                    <p>Chúng tôi cam kết cung cấp dịch vụ tin cậy, chuyên nghiệp, giá cả phải chăng. Đội ngũ giàu đam
                        mê, hỗ trợ 24/7.</p>
                </div>
            </aside>
            <div style="clear:both"></div>
        </div>

        <!-- DỊCH VỤ (SERVICES) -->
        <div id="servicesPage" class="page">
            <article class="main-col">
                <h1 class="page-title" style="color:#4c1d95;">⚙️ Các dịch vụ</h1>
                <ul id="services">
                    <li>
                        <h3>🌐 Thiết kế Website</h3>
                        <p>Tạo website chuyên nghiệp, giá cả phải chăng cho cá nhân, công ty, doanh nghiệp hoặc tổ chức.
                        </p>
                        <p><strong>Giá: $1,000 - $3,000</strong></p>
                    </li>
                    <li>
                        <h3>🛠️ Bảo trì Website</h3>
                        <p>Bảo trì website chuyên nghiệp, cập nhật an ninh, hiệu suất cao.</p>
                        <p><strong>Giá: $250 mỗi tháng</strong></p>
                    </li>
                    <li>
                        <h3>☁️ Web Hosting</h3>
                        <p>Cung cấp hosting tốc độ cao, bảo mật, hỗ trợ 24/7.</p>
                        <p><strong>Giá: $25 mỗi tháng</strong></p>
                    </li>
                </ul>
            </article>

            <aside class="sidebar">
                <div class="dark">
                    <h3>📩 Liên hệ tư vấn</h3>
                    <form class="quote" id="contactForm">
                        <div>
                            <label>Tên</label><br>
                            <input type="text" placeholder="Tên của bạn" required>
                        </div>
                        <div>
                            <label>Email</label><br>
                            <input type="email" placeholder="Email liên hệ" required>
                        </div>
                        <div>
                            <label>Nội dung</label><br>
                            <textarea placeholder="Yêu cầu dịch vụ..." rows="3"></textarea>
                        </div>
                        <button class="button_1" type="submit">Gửi yêu cầu</button>
                    </form>
                    <p style="margin-top: 12px; font-size: 0.85rem;">🌟 Phản hồi trong 24h</p>
                </div>
            </aside>
            <div style="clear:both"></div>
        </div>
    </div>

    <footer>
        <p>Ngoc Minh Web Design, Copyright &copy; 2025 | Thiết kế bởi Ngoc Minh Team</p>
    </footer>

    <script>
        (function () {
            // Lấy các phần tử trang
            const homePage = document.getElementById('homePage');
            const aboutPage = document.getElementById('aboutPage');
            const servicesPage = document.getElementById('servicesPage');
            const pages = [homePage, aboutPage, servicesPage];

            // Lấy các nút điều hướng
            const navHome = document.getElementById('nav-home');
            const navAbout = document.getElementById('nav-about');
            const navServices = document.getElementById('nav-services');
            const navLinks = [navHome, navAbout, navServices];

            // Hàm chuyển đổi trang
            function switchPage(pageId) {
                // Ẩn tất cả các page
                pages.forEach(page => {
                    page.classList.remove('active-page');
                });
                // Hiện page được chọn
                if (pageId === 'home') homePage.classList.add('active-page');
                if (pageId === 'about') aboutPage.classList.add('active-page');
                if (pageId === 'services') servicesPage.classList.add('active-page');

                // Cập nhật class current trên menu
                navLinks.forEach(link => link.classList.remove('current'));
                if (pageId === 'home') navHome.classList.add('current');
                if (pageId === 'about') navAbout.classList.add('current');
                if (pageId === 'services') navServices.classList.add('current');

                // Thay đổi title trang cho trải nghiệm tốt
                if (pageId === 'home') document.title = "Ngoc Minh Web Design | Trang chủ";
                if (pageId === 'about') document.title = "Ngoc Minh Web Design | Thông tin";
                if (pageId === 'services') document.title = "Ngoc Minh Web Design | Dịch vụ";
            }

            // Xử lý sự kiện click menu
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const page = this.getAttribute('data-page');
                    if (page) switchPage(page);
                });
            });

            // Newsletter form (chỉ thông báo demo)
            const newsletterForm = document.getElementById('newsletterForm');
            if (newsletterForm) {
                newsletterForm.addEventListener('submit', function (e) {
                    e.preventDefault();
                    const emailInput = this.querySelector('input[type="email"]');
                    if (emailInput.value.trim() !== "") {
                        alert(`📧 Cảm ơn ${emailInput.value} đã đăng ký! Chúng tôi sẽ gửi thông báo mới nhất.`);
                        emailInput.value = "";
                    } else {
                        alert("Vui lòng nhập email hợp lệ.");
                    }
                });
            }

            // Contact form (dịch vụ sidebar)
            const contactForm = document.getElementById('contactForm');
            if (contactForm) {
                contactForm.addEventListener('submit', function (e) {
                    e.preventDefault();
                    const name = this.querySelector('input[placeholder="Tên của bạn"]').value;
                    const email = this.querySelector('input[type="email"]').value;
                    if (name && email) {
                        alert(`✅ Cảm ơn ${name}, chúng tôi sẽ liên hệ qua ${email} trong thời gian sớm nhất!`);
                        this.reset();
                    } else {
                        alert("Vui lòng nhập đầy đủ tên và email.");
                    }
                });
            }

            // Mặc định hiển thị trang chủ (đã active class từ đầu)
            // Đảm bảo nếu có hash thì xử lý nhưng không bắt buộc
            const currentActive = document.querySelector('.page.active-page');
            if (!currentActive) {
                switchPage('home');
            }
        })();
    </script>
</body>

</html>
