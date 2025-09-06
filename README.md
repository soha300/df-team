df team
programing team
[soha.html.html](https://github.com/user-attachments/files/22191829/soha.html.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>soha</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #D291BC; /* لافندر فاتح */
            --secondary-color: #F7D6E0; /* بينك */
            --accent-color: #9C89B8; /* لافندر غامق */
            --text-color: #333;
            --light-text: #fff;
            --background: #F8F9FA;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--background);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* زر تبديل اللغة */
        .language-switcher {
            position: fixed;
            top: 20px;
            left: 20px;
            z-index: 1000;
        }

        .language-switcher button {
            background: var(--accent-color);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            font-weight: bold;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .language-switcher button:hover {
            background: var(--primary-color);
            transform: translateY(-2px);
        }

        /* الهيدر والصورة الشخصية */
        header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--accent-color) 100%);
            color: var(--light-text);
            padding: 60px 0 30px;
            text-align: center;
            border-bottom-left-radius: 50% 20%;
            border-bottom-right-radius: 50% 20%;
        }

        .profile-img {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid var(--secondary-color);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            margin-bottom: 20px;
        }

        .header-content h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .header-content p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto;
        }

        /* أقسام الموقع */
        section {
            padding: 60px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 40px;
            color: var(--accent-color);
            position: relative;
            font-size: 2rem;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--primary-color);
            margin: 10px auto;
            border-radius: 2px;
        }

        /* قسم عني */
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 30px;
            justify-content: center;
        }

        .about-text {
            flex: 1;
            min-width: 300px;
            padding: 20px;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .about-images {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
            justify-content: center;
            margin-top: 20px;
        }

        .about-img {
            width: 100%;
            max-width: 400px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        /* قسم الأعمال */
        .projects {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
        }

        .project-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .project-info {
            padding: 20px;
        }

        .project-info h3 {
            color: var(--accent-color);
            margin-bottom: 10px;
        }

        /* قسم الفريق */
        .team {
            background: linear-gradient(135deg, var(--secondary-color) 0%, #ffffff 100%);
            border-radius: 15px;
            padding: 40px;
            text-align: center;
            margin-top: 40px;
        }

        .team-images {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            justify-content: center;
            margin: 30px 0;
        }

        .team-img {
            width: 100%;
            max-width: 500px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .team-logos {
            display: flex;
            justify-content: center;
            gap: 40px;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .logo {
            width: 120px;
            height: 120px;
            object-fit: contain;
            background: white;
            padding: 15px;
            border-radius: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        /* قسم التواصل */
        .contact {
            background: linear-gradient(135deg, var(--accent-color) 0%, var(--primary-color) 100%);
            color: var(--light-text);
            text-align: center;
            padding: 60px 0;
            border-top-left-radius: 50% 20%;
            border-top-right-radius: 50% 20%;
        }

        .contact-info {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 40px;
            margin-top: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.1rem;
        }

        .contact-icon {
            font-size: 1.5rem;
        }

        /* الفوتر */
        footer {
            background: var(--text-color);
            color: var(--light-text);
            text-align: center;
            padding: 20px 0;
            font-size: 0.9rem;
        }

        /* التكيف مع الشاشات الصغيرة */
        @media (max-width: 768px) {
            .header-content h1 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 1.8rem;
            }
            
            .team {
                padding: 30px 20px;
            }
            
            .contact-info {
                flex-direction: column;
                gap: 20px;
            }
            
            .team-images {
                gap: 20px;
            }
        }
    </style>
</head>
<body>
    <!-- زر تبديل اللغة -->
    <div class="language-switcher">
        <button id="language-btn">EN</button>
    </div>

    <!-- الهيدر -->
    <header>
        <div class="container">
            <img src="WhatsApp Image 2025-09-02 at 7.08.48 AM (1).jpeg" alt="صورة سهى الشخصية" class="profile-img">
            <div class="header-content">
                <h1>سهى سامح</h1>
                <p>أنا سها سامح، عضوة في فريق "الأنامل الرقمية" في مدرسة الشهيد مدحت طلعت. أتعلم البرمجة، وأعمل بشكل خاص على تعلم HTML و CSS.</p>
            </div>
        </div>
    </header>

    <!-- قسم عني -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">about</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>أنا طالبة متحمسة في مجال البرمجة وتطوير الويب. انضممت إلى فريق الأنامل الرقمية لاكتساب الخبرة العملية والعمل على مشاريع حقيقية.</p>
                    <p>أتمتع بشغف كبير للتعلم وأطمح لأن أصبح مطورة ويب محترفة في المستقبل. أحب العمل الجمعى</p>
                     
                </div>
            
            </div>
            <div class="about-images">
                <img src="WhatsApp Image 2025-09-04 at 2.54.19 AM.jpeg" alt="صورة عن سهى" class="about-img">
            </div>
        </div>
    </section>

    <!-- قسم الأعمال -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">أعمالي</h2>
            <div class="projects">
                <div class="project-card">
                    <img src="WhatsApp Image 2025-09-06 at 2.46.14 AM.jpeg" alt="مشروع HTML و CSS" class="project-img">
                    <div class="project-info">
                        <h3>موقع شخصي بتصميم مبتكر</h3>
                        <p>قمت بتصميم وتنفيذ موقع شخصي باستخدام HTML و CSS فقط، مع التركيز على التصميم المتجاوب.</p>
                    </div>
                </div>
    
                <div class="الفريق">
                    <img width="200" height="250"
                     src="WhatsApp Image 2025-09-05 at 2.44.13 PM.jpeg" alt="الفريق" class=" فريق">
                    <div class="project-info">
                        <h3>فريق الانامل الرقميه</h3>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- قسم الفريق -->
    <section id="team">
        <div class="container">
            <h2 class="section-title">فريقي البرمجي</h2>
            <div class="team">
                <h3>فريق الأنامل الرقمية</h3>
                <p>نحن فريق من الطلاب المتحمسين للبرمجة والتكنولوجيا، نعمل معًا على تطوير مشاريع برمجية مبتكرة وتنمية مهاراتنا في مجال تطوير الويب.</p>
                
                <div class="team-images">
                    <img  width="200" height="250"
                    src="WhatsApp Image 2025-09-06 at 3.02.24 AM.jpeg" alt="صورة الفريق " class="team-img">
        
                </div>
                
                <div class="team-logos">
                    <img width="200" height="250"
                     src="WhatsApp Image 2025-09-06 at 3.12.38 AM.jpeg" alt="شعار مدرسة الشهيد مدحت طلعت" class="logo">
                    <img src="WhatsApp Image 2025-09-03 at 4.57.05 AM (1).jpeg" alt="شعار فريق الأنامل الرقمية" class="logo">
                </div>
                <a href="#" style="display: inline-block; margin-top: 20px; padding: 10px 20px; background: var(--primary-color); color: white; text-decoration: none; border-radius: 30px;">صفحة الفيسبوك</a>
            </div>
        </div>
    </section>

    <!-- قسم التواصل -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">تواصل معي</h2>
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-phone contact-icon"></i>
                    <span>+20 XXX XXX XXXX</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope contact-icon"></i>
                    <span>sohasameh41@gmail.com</span>
                </div>
            </div>
        </div>
    </section>

    <!-- الفوتر -->
    <footer>
        <div class="container">
            <p>© 2025 جميع الحقوق محفوظة | تصميم وتطوير سهى سامح</p>
        </div>
    </footer>

    <!-- JavaScript لتبديل اللغة -->
    <script>
        document.getElementById('language-btn').addEventListener('click', function() {
            const currentLang = document.documentElement.lang;
            if (currentLang === 'ar') {
                document.documentElement.lang = 'en';
                document.documentElement.dir = 'ltr';
                this.textContent = 'AR';
                // هنا يمكن إضافة ترجمة للمحتوى
            } else {
                document.documentElement.lang = 'ar';
                document.documentElement.dir = 'rtl';
                this.textContent = 'EN';
                // هنا يمكن إعادة المحتوى للعربية
            }
        });
    </script>
</body>
</html>
