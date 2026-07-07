<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HOMEPAGE - 我的可爱个人主页</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "PingFang SC",

                "HarmonyOS Sans",

                "MiSans",

                "Microsoft YaHei",

                sans-serif
        }

        :root {
            --main-blue: #84b8f0;
            --word-yellow: #ffd370;
            --soft-pink: #ffb8c2;
            --apple-red: #ff7b86;
            --white: #ffffff;
            --text-dark: #304a7a;
            --light-blue: #e8f2ff;
            --soft-gray: #fcf4f8;
            --cream: #fff9ef;
        }

        body {
            overflow: hidden;
        }

        /* 全局可爱动画 */
        @keyframes floatUpDown {

            0%,
            100% {
                transform: translateY(0px);
            }

            50% {
                transform: translateY(-12px);
            }
        }

        @keyframes slowWave {
            0% {
                transform: translateX(-30px);
            }

            50% {
                transform: translateX(30px);
            }

            100% {
                transform: translateX(-30px);
            }
        }

        @keyframes appleFall {
            0% {
                top: 30%;
                opacity: 0;
            }

            30% {
                opacity: 1;
            }

            80% {
                top: 44%;
                opacity: 1;
            }

            100% {
                top: 46%;
                opacity: 0;
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes textPop {
            0% {
                transform: scale(0.8);
                opacity: 0;
            }

            70% {
                transform: scale(1.05);
            }

            100% {
                transform: scale(1);
                opacity: 1;
            }
        }

        @keyframes navSlide {
            from {
                opacity: 0;
                transform: translateY(-10px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes cardShine {
            0% {
                box-shadow: 0 0 5px rgba(132, 184, 240, 0.2);
            }

            50% {
                box-shadow: 0 0 18px rgba(132, 184, 240, 0.45);
            }

            100% {
                box-shadow: 0 0 5px rgba(132, 184, 240, 0.2);
            }
        }

        @keyframes floatShape {

            0%,
            100% {
                transform: translate(0, 0) rotate(0deg);
            }

            25% {
                transform: translate(15px, -20px) rotate(8deg);
            }

            50% {
                transform: translate(-10px, -30px) rotate(15deg);
            }

            75% {
                transform: translate(-20px, 10px) rotate(-8deg);
            }
        }

        @keyframes twinkle {

            0%,
            100% {
                opacity: 0.3;
            }

            50% {
                opacity: 1;
            }
        }

        @keyframes heartBeat {

            0%,
            100% {
                transform: scale(1);
            }

            50% {
                transform: scale(1.1);
            }
        }

        /* 证件照样式 —— 已删除动画 + 放大 + 米白色细边框 */
        .id-card-box {
            position: absolute;
            top: 80px;
            right: 4%;
            z-index: 8;
            width: 150px;
            height: 180px;
        }

        .id-photo {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 16px;
            border: 2px solid #f9f9f9;
            /* 米白色细边框 */
            box-shadow: 0 6px 16px rgba(132, 184, 240, 0.25);
        }

        /* 顶部导航栏 */
        header {
            background-color: var(--white);
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 16px 4%;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 999;
            animation: navSlide 1s ease forwards;
            box-shadow: 0 3px 12px rgba(132, 184, 240, 0.15);
            border-bottom-left-radius: 20px;
            border-bottom-right-radius: 20px;
            max-width: 100%;
            height: auto;
            max-width: 100%;
            height: auto;
        }

        header {
            background: rgba(255, 255, 255, .65);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);

            border: 1px solid rgba(255, 255, 255, .4);

            box-shadow:
                0 10px 35px rgba(0, 0, 0, .08);

            transition: .4s;
            max-width: 100%;
            height: auto;
            max-width: 100%;
            height: auto;
        }

        nav a:hover {

            background: white;

            transform: translateY(-3px);

            box-shadow:
                0 8px 18px rgba(132, 184, 240, .25);

        }


        .logo {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 28px;
            font-weight: 900;
            color: #5b5b5b;
            /* 纯黑色文字 */
            letter-spacing: 4px;
            /* 文字间距1.5px */
        }

        .logo-img {
            width: 36px;
            height: 36px;
            max-width: 100%;
            height: auto;
            border-radius: 50%;
            object-fit: cover;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .logo-img:hover {
            transform: scale(1.15) rotate(6deg);
            box-shadow: 0 0 10px rgba(255, 123, 134, 0.4);
        }

        nav ul {
            display: flex;
            gap: 28px;
            list-style: none;
        }

        nav a {
            text-decoration: none;
            color: #333;
            text-align: center;
            display: block;
            cursor: pointer;
            transition: all 0.3s ease;
            padding: 4px 8px;
            border-radius: 12px;
        }

        nav a:hover {
            background: var(--light-blue);
        }

        nav a:hover p:first-child {
            color: var(--main-blue);
            transform: scale(1.08);
        }

        nav a p:first-child {
            font-size: 17px;
            font-weight: 600;
            transition: transform 0.3s ease;
        }

        nav a p:last-child {
            font-size: 12px;
            color: #777;
        }


        /* 横向滑动容器核心 */
        .page-wrapper {
            display: flex;
            width: 600vw;
            height: 100vh;
            transition: transform 0.9s cubic-bezier(0.22, 1, 0.36, 1);
            padding-top: 70px;
        }

        .slide-page {
            width: 100vw;
            height: 100vh;
            overflow-y: auto;
            position: relative;
        }

        /* 除封面外所有页面共用全屏背景图 */
        .page-biography,
        .page-hobby,
        .page-portfolio,
        .page-award,
        .page-contact {
            background-image: url('wwwwpic/888.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;
        }



        /* 左右通用箭头按钮样式 */
        .arrow-btn {
            position: absolute;
            bottom: 30px;
            font-size: 40px;
            cursor: pointer;
            transition: all 0.3s ease;
            animation: fadeInUp 1.5s ease forwards;
            animation-delay: 0.8s;
            opacity: 0;
            z-index: 99;
            user-select: none;
        }

        .arrow-left {
            left: 6%;
        }

        .arrow-right {
            right: 6%;
        }

        .dark-arrow {
            color: rgba(255, 255, 255, 0.7);
        }

        .arrow-btn:hover {

            transform: scale(1.12);

            background: white;

        }

        .dark-arrow.arrow-right:hover {
            transform: translateX(8px);
        }

        .light-arrow {
            color: rgba(48, 74, 122, 0.6);
        }

        .light-arrow:hover {
            color: var(--text-dark);
            transform: translateX(-8px);
        }

        .light-arrow.arrow-right:hover {
            transform: translateX(8px);
        }

        /* 首页气泡文字可点击跳转 */
        .talk-bubble {
            position: absolute;
            right: 6%;
            bottom: 30px;
            cursor: pointer;
            background: rgba(255, 255, 255, 0.85);
            padding: 14px 30px;
            border-radius: 18px 18px 18px 0;
            font-size: 32px;
            color: var(--text-dark);
            font-weight: 600;
            width: fit-content;
            animation: floatUpDown 4s ease-in-out infinite;
            transition: all 0.3s;
            z-index: 100;
        }

        .talk-bubble:hover {
            background: rgba(255, 255, 255, 1);
            transform: scale(1.03);
        }

        /* 首页封面 */
        .page-home {
            background-image: url('wwwwpic/88.jpg');
            background-size: cover;
            background-position: 50% 30%;
            background-repeat: no-repeat;
            background-attachment: fixed;
            width: 100vw;
            height: 100vh;
            padding: 40px 4%;
            overflow: hidden;
        }

        .page-home::before {

            content: "";

            position: absolute;

            left: 0;
            top: 0;

            width: 100%;
            height: 100%;


        }

        .welcome-title,
        .hero-text-left {

            position: relative;
            z-index: 5;

        }

        .decor-shape {
            position: absolute;
            pointer-events: none;
            animation: floatShape 12s ease-in-out infinite;
        }

        .shape1 {
            width: 90px;
            height: 90px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.18);
            top: 12%;
            left: 8%;
            animation-delay: 0s;
        }

        .shape2 {
            width: 55px;
            height: 55px;
            background: rgba(255, 211, 112, 0.22);
            border-radius: 16px;
            top: 22%;
            right: 12%;
            animation-delay: 2s;
        }

        .shape3 {
            width: 130px;
            height: 130px;
            border: 2px solid rgba(255, 255, 255, 0.25);
            border-radius: 50%;
            bottom: 25%;
            left: 5%;
            animation-delay: 4s;
        }

        .heart-decor {
            position: absolute;
            width: 40px;
            height: 40px;
            background: var(--soft-pink);
            border-radius: 50%;
            top: 40%;
            right: 10%;
            animation: heartBeat 3s infinite;
            opacity: 0.6;
        }

        .star-dot {
            position: absolute;
            width: 7px;
            height: 7px;
            background: #fff;
            border-radius: 50%;
            animation: twinkle 3s infinite;
        }

        .star1 {
            top: 18%;
            left: 30%;
            animation-delay: 0.5s;
        }

        .star2 {
            top: 35%;
            right: 25%;
            animation-delay: 1s;
        }

        .star3 {
            bottom: 40%;
            left: 15%;
            animation-delay: 1.8s;
        }

        .wave-line {
            position: absolute;
            stroke: #fff;
            stroke-width: 1.4;
            fill: transparent;
            pointer-events: none;
            animation: slowWave 8s ease-in-out infinite;
        }

        .wave1 {
            top: 26%;
            left: 2%;
            width: 96%;
            animation-delay: 0s;
        }

        .wave2 {
            bottom: 0;
            left: 0;
            width: 100%;
            animation-delay: 1s;
        }

        .welcome-title {
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 120px;
            font-weight: bold;
            color: var(--word-yellow);
            letter-spacing: 10px;
            margin-top: 30px;
            animation: textPop 2s ease forwards;
            /* 刚进入页面自动播放 */
        }

        .apple-icon {
            width: 130px;
            height: 130px;
            background: var(--apple-red);
            border-radius: 52% 52% 48% 48%;
            position: relative;
            margin: 0 -8px;
            animation: floatUpDown 3s ease-in-out infinite;
        }

        .apple-icon::after {
            content: "";
            width: 12px;
            height: 24px;
            background: #663322;
            position: absolute;
            top: -12px;
            left: 50%;
            transform: translateX(-50%);
            border-radius: 4px;
        }

        .fall-apple {
            width: 75px;
            height: 75px;
            background: var(--apple-red);
            border-radius: 52% 52% 48% 48%;
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            animation: appleFall 6s ease-in-out infinite;
        }

        .hero-text-left {
            position: absolute;
            left: 6%;
            top: 54%;
            color: var(--text-dark);
            animation: fadeInUp 1.5s ease forwards;
            animation-delay: 0.4s;
            opacity: 0;
        }

        .hero-text-left p.cn {
            font-size: 22px;
            line-height: 1.8;
        }

        .hero-text-left p.en {
            font-size: 16px;
            margin-top: 8px;
        }

        /* 通用板块 */
        .page-inner-wrap {
            max-width: 1280px;
            margin: 90px auto 0;
            padding: 70px 50px;
        }

        .two-col-row {
            gap: 50px;
        }

        .sub-block {
            padding: 40px;
            margin-bottom: 45px;
            border-radius: 28px;
        }

        .edu-item,
        .exp-item {
            padding: 22px 0;
        }

        .section-main-title {
            text-align: center;
            font-size: 40px;
            color: var(--white);
            margin-bottom: 50px;
            position: relative;
        }

        .section-main-title::after {
            content: "";
            width: 100px;
            height: 4px;
            background: var(--apple-red);
            position: absolute;
            left: 50%;
            transform: translateX(-50%);
            bottom: -12px;
            border-radius: 4px;
        }



        .sub-block {

            background: rgba(255, 255, 255, .72);

            backdrop-filter: blur(18px);

            border: 1px solid rgba(255, 255, 255, .5);

            border-radius: 30px;

            box-shadow:
                0 15px 45px rgba(60, 90, 140, .08);

        }

        .sub-block p {
            text-indent: 2em;
            /* 2个汉字宽度首行缩进 */
            line-height: 1.8;
        }

        .sub-block:hover {

            transform:
                translateY(-8px) scale(1.05);

        }


        .sub-block h3 {
            font-size: 24px;
            color: var(--text-dark);
            margin-bottom: 18px;
            display: flex;
            align-items: center;
            gap: 10px;
        }




        .sub-block h3::before {
            content: "";
            width: 6px;
            height: 24px;
            background: var(--apple-red);
            border-radius: 3px;
        }

        /* 1.自我介绍页面 */
        .two-col-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }

        .edu-item,
        .exp-item {
            padding: 14px 0;
            border-bottom: 1px solid #ccd6e6;
            display: flex;
            justify-content: space-between;
            transition: padding-left 0.3s;
        }

        .edu-item:hover,
        .exp-item:hover {
            padding-left: 10px;
            color: var(--main-blue);
        }

        /* 2.兴趣爱好页面 */
        .hobby-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 18px;
        }

        .hobby-tag {
            background: rgba(255, 255, 255, 0.9);
            padding: 14px;
            border-radius: 16px;
            text-align: center;
            border: 1px solid var(--main-blue);
            transition: all 0.3s ease;
            font-size: 16px;
        }

        .hobby-tag:hover {
            background: var(--main-blue);
            color: white;
            transform: scale(1.06);
        }

        .daily-card {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        .daily-item {
            flex: 1;
            min-width: 220px;
            background: rgba(255, 255, 255, 0.9);
            padding: 22px;
            border-radius: 18px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .daily-item:hover {
            background: var(--main-blue);
            color: white;
        }

        /* 4.作品展示 */
        .port-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 22px;
        }

        .port-item {
            height: 260px;
            background: rgba(212, 231, 255, 0.9);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-dark);
            font-size: 20px;
            transition: all 0.3s ease;
        }

        .port-item:hover {
            transform: scale(1.04);
            background: var(--main-blue);
            color: white;
        }

        /* 5.荣誉收获 */
        .award-item {
            padding: 16px 0;
            border-bottom: 1px solid #ccd6e6;
            font-size: 18px;
        }

        /* 6.联系方式 */
        .contact-box {
            max-width: 700px;
            margin: 0 auto;
        }

        .contact-item {
            font-size: 20px;
            padding: 18px;
            margin: 14px 0;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 16px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .contact-item:hover {
            background: var(--main-blue);
            color: white;
            letter-spacing: 1px;
        }

        /* 弹窗遮罩通用样式 */
        .mask {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            background: rgba(0, 0, 0, 0.7);
            z-index: 9999;
            align-items: center;
            justify-content: center;
        }

        .mask.show {
            display: flex;
        }

        .qr-img {
            max-width: 70%;
            max-height: 80vh;
            border-radius: 12px;
        }

        /* 移动端适配 */
        @media (max-width:768px) {

            header {
                padding: 12px 18px;
                max-width: 100%;
                height: auto;
            }

            .logo {
                font-size: 22px;
            }

            .logo-img {
                width: 28px;
                height: 28px;
            }

            nav ul {
                gap: 6px;
            }

            nav a p:first-child {
                font-size: 12px;
            }

            nav a p:last-child {
                display: none;
            }

            .welcome-title {
                font-size: 60px;
                letter-spacing: 4px;
            }

            .hero-text-left {
                left: 8%;
                top: 60%;
            }

            .hero-text-left p.cn {
                font-size: 18px;
            }

            .hero-text-left p.en {
                font-size: 13px;
            }

            .page-inner-wrap {
                padding: 30px 18px;
            }

            .two-col-row {
                grid-template-columns: 1fr;
            }

            .port-grid {
                grid-template-columns: 1fr;
            }

            .port-item {
                height: 240px;
            }

            .port-item video {
                width: 100%;
                height: 100%;
                object-fit: cover;

                @media (max-width:768px) {

                    header {
                        padding: 12px 18px;
                        max-width: 100%;
                        height: auto;
                    }

                    .logo {
                        font-size: 22px;
                    }

                    .logo-img {
                        width: 28px;
                        height: 28px;
                    }

                    nav ul {
                        gap: 6px;
                    }

                    nav a p:first-child {
                        font-size: 12px;
                    }

                    nav a p:last-child {
                        display: none;
                    }

                    .welcome-title {
                        font-size: 60px;
                        letter-spacing: 4px;
                    }

                    .hero-text-left {
                        left: 8%;
                        top: 60%;
                    }

                    .hero-text-left p.cn {
                        font-size: 18px;
                    }

                    .hero-text-left p.en {
                        font-size: 13px;
                    }

                    .page-inner-wrap {
                        padding: 30px 18px;
                    }

                    .two-col-row {
                        grid-template-columns: 1fr;
                    }

                    .port-grid {
                        grid-template-columns: 1fr;
                    }

                    .port-item {
                        height: 240px;
                    }

                    .port-item video {
                        width: 100%;
                        height: 100%;
                        object-fit: cover;
                    }

                    .section-main-title {
                        font-size: 28px;
                    }

                    .sub-block {
                        padding: 22px;
                    }

                    .contact-item {
                        font-size: 16px;
                    }

                    .arrow-btn {
                        display: none;
                    }

                }
            }

            .section-main-title {
                font-size: 28px;
            }

            .sub-block {
                padding: 22px;
            }

            .contact-item {
                font-size: 16px;
            }

            .arrow-btn {
                display: none;
            }

        }
    </style>
</head>

<body>
    <header>
        <div class="logo">
            <img class="logo-img" src="wwwwpic/44.png" alt="头像logo">
            徐燕云

        </div>
        <nav>
            <ul>
                <li>
                    <a data-target="0">
                        <p>封面</p>
                        <p>Home</p>
                    </a>
                </li>
                <li>
                    <a data-target="1">
                        <p>自我介绍</p>
                        <p>About Me</p>
                    </a>
                </li>
                <li>
                    <a data-target="2">
                        <p>兴趣爱好</p>
                        <p>Hobbies</p>
                    </a>
                </li>
                <li>
                    <a data-target="3">
                        <p>作品展示</p>
                        <p>Works</p>
                    </a>
                </li>
                <li>
                    <a data-target="4">
                        <p>荣誉收获</p>
                        <p>Awards</p>
                    </a>
                </li>
                <li>
                    <a data-target="5">
                        <p>联系方式</p>
                        <p>Contact</p>
                    </a>
                </li>
            </ul>
        </nav>
    </header>

    <div class="page-wrapper" id="slideContainer">
        <!-- 第0页：封面 -->
        <div class="slide-page page-home" data-index="0">
            <div class="decor-shape shape1"></div>
            <div class="decor-shape shape2"></div>
            <div class="decor-shape shape3"></div>
            <div class="heart-decor"></div>
            <div class="star-dot star1"></div>
            <div class="star-dot star2"></div>
            <div class="star-dot star3"></div>

            <svg class="wave-line wave1" viewBox="0 0 1200 300">
                <path d="M20,150 Q200,30 400,140 T800,130 T1200,150" />
            </svg>
            <svg class="wave-line wave2" viewBox="0 0 1200 180">
                <path d="M0,90 Q150,170 300,80 T600,90 T900,70 T1200,90" />
            </svg>
            <div class="fall-apple"></div>

            <div class="welcome-title" id="welcomeText">
                WELCOME
                <div class="apple-icon"></div>
            </div>

            <div class="hero-text-left">
                <p class="cn">每个人都有无限可能</p>
                <p class="en">Everyone has infinite possibilities</p>
            </div>
            <div class="talk-bubble" data-next="1">THIS IS MY CHANNEL!</div>
        </div>

        <!-- 第1页：自我介绍 -->
        <div class="slide-page page-biography" data-index="1">
            <div class="id-card-box">
                <img class="id-photo" src="wwwwpic/zjz.jpg" alt="个人证件照">
            </div>

            <div class="page-inner-wrap">
                <h2 class="section-main-title">自我介绍 About Me</h2>
                <div class="two-col-row">
                    <div>
                        <div class="sub-block">
                            <h3>个人概述</h3>
                            <p>大家好，我是徐燕云，或者你可以叫我SOOKU。</p>
                            <p>如果要用几个关键词来概括自己，我会选：温和、敏感、有耐心、有计划。</p>

                            <p> 我性格偏内向，不是那种一见面就能迅速热络起来的人。刚接触时我可能话不多，显得有些安静——但这绝不是冷淡，只是需要一点时间去适应和观察。熟悉我的朋友都知道，我其实挺爱笑的，笑起来也没什么包袱，聊开了之后说话也挺直接。和人相处，我的习惯是先释放善意，不喜欢摆出攻击性或距离感。无论是小组作业还是日常社交，我都会尽量让身边人觉得舒服、放松。在团队里，我更像一个“黏合剂”而不是“指挥者”，更愿意先倾听、理解，再表达。
                            </p>

                            <p>
                                文学是我最大的爱好，这些年读过的书塑造了我对文字和情绪的敏感度。
                                除此之外，我也喜欢听歌——音乐和文学一样，是我理解世界的另一扇窗。旋律里的情绪、歌词中的叙事，常常能给我带来灵感和共鸣。我偏爱短途旅行，去附近的城市走走、看看不同的风景和人文，那种短暂抽离的感觉能让我重新充电。而且我做这件事很有计划性——出发前会查好路线、天气、想逛的小店，甚至连吃饭的时段都会考虑进去。这种习惯也延续到了学习和工作中：我不太喜欢临时抱佛脚，更倾向于提前规划好节奏，一步步稳扎稳打地推进。
                            </p>
                            <p>也正因为有计划，我在做事时特别在意细节和质感。一个标题、一张画面的色调、一句话的语气，我愿意花时间反复调整，不急着交差。同时我也不排斥新事物，看到有意思的工具或技能，会主动去尝试，哪怕一开始并不熟练。
                            </p>
                            <p>我学广告，是希望成为一个能理解人、也能打动人的表达者。我相信好的沟通不是靠音量，而是靠共情和洞察。我希望未来能用自己的文字和创意，去连接品牌与人、内容与内心。</p>

                            <p>这就是我，不算耀眼，但足够真诚。很高兴认识你。</p>
                        </div>
                        <div class="sub-block">
                            <h3>个性签名</h3>
                            <p>“孤独是关上灯，与发光的灵魂为伴。”</p>
                            <p>“凡是过往，皆为序章。”</p>
                        </div>
                        <div class="sub-block">
                            <h3>人生格言</h3>
                            <p>种一棵树最好的时间是十年前，其次是现在。</p>
                        </div>
                    </div>
                    <div>
                        <div class="sub-block">
                            <h3>学历履历</h3>
                            <div class="edu-list">
                                <div class="edu-item">
                                    <div>
                                        <strong>安徽师范大学 | 本科</strong> 广告学专业
                                        <p style="margin-top:8px; font-weight:normal; font-size:16px; line-height:1.7;">
                                            主修课程与专业能力：系统修读《广告策划与创意》《品牌管理与整合营销传播》《消费者行为与心理洞察》《数字营销与社交媒体策略》《市场调研与数据分析》《广告文案与内容创作》等核心课程，建立起从策略规划到落地执行、从传统媒介到数字生态的完整广告知识体系，具备将理论灵活应用于实践项目的能力。
                                        </p>
                                        <p>大二学年我注重理论结合实践，踊跃参与专业创意竞赛锻炼实操能力，先后参加大学生创意广告比赛与2025年秋季中国广告节学院奖；与组员分工协作完成原创广告视频创作，凭借完整的创意策划与视听呈现，作品顺利斩获学院奖入围奖。
                                        </p>
                                    </div>
                                    <div>2023.09 - 2027.06</div>
                                </div>
                                <div class="edu-item">
                                    <div><strong>郎溪高级中学</strong> 重点高中
                                        <p style="margin-top:8px; font-weight:normal; font-size:16px; line-height:1.7;">
                                            本人高中就读于郎溪高级中学。在三年的学习生活中，我不仅在学业上刻苦钻研，更注重通过班级工作提升自身的综合能力。
                                        </p>
                                        <p>在班级职务方面，我长期担任纪律委员与劳动委员。作为纪律委员，我严于律己，协助班主任维持班级秩序，营造了良好的学习氛围；作为劳动委员，我以身作则，带领同学做好卫生保洁工作，增强了班级的凝聚力与责任感。这些干部经历锻炼了我的组织协调能力与沟通能力，也让我深刻理解了“责任”二字的含义。
                                        </p>
                                        <p>在学习上，我始终保持端正的态度，勤奋努力，不断突破自我，成绩稳步提升。同时，我热衷于参与学校各类文体与社团活动，力求在德、智、体、美、劳各方面均衡发展。高中三年，我不仅收获了知识，更磨砺了踏实肯干、勇于担当的品格。
                                        </p>
                                    </div>
                                    <div>2020.09 - 2023.06</div>
                                </div>
                            </div>
                        </div>
                        <div class="sub-block">
                            <h3>个人经历</h3>
                            <div class="exp-list">
                                <div class="exp-item">
                                    <div>枣红波光梦影梳乡
                                        宣城项目实践</div>
                                    <div>2024.09-2024.10</div>
                                    <p style="margin-top:8px; font-weight:normal; font-size:16px; line-height:1.7;">
                                        在参与当地文旅宣传项目中，我主要负责实地采访与新闻内容编写。通过深入村落调研，我与团队成员完成三篇文旅主题报道，其中以传统工艺活化与生态旅游发展为主线的内容，完成文化叙事，将农产品推荐出去。这些内容成为项目申报“百瑞德奖学金”的核心材料支撑，最终助力团队获得该项荣誉。

                                        项目后期，我们团队持续跟进文旅发展动态，几篇报道被地方媒体采
                                        用，累计获得破万的阅读量，有效提升了当地文旅资源的公众关注度，为宣城文旅宣传提供了持续的内容支持。</p>
                                </div>
                                <div class="exp-item">
                                    <div>兴乡图鉴融媒焕彩
                                        实践队</div>
                                    <div>2025.07-2025.08</div>
                                    <p style="margin-top:8px; font-weight:normal; font-size:16px; line-height:1.7;">
                                        在旌德农文旅推广项目中，我作为文创设计的主要成员，主导了当地特色农产品包装体系的视觉设计。通过深入调研特色农产品与传统红色文化，我将文化元素转化为系列包装方案，并为其设计出IP形象，并推动设计落地生产，实际应用于农产品。包装投入使用后，有效提升了产品市场辨识度。我同时参与文旅宣传片视觉策划，相关成果获省级媒体刊发，共同提升了旌德文旅品牌影响力。
                                    </p>
                                </div>
                                <div class="exp-item">
                                    <div>外卖员</div>
                                    <div>2024.09-2024.11</div>
                                    <p style="margin-top:8px; font-weight:normal; font-size:16px; line-height:1.7;">
                                        在外卖担任配送员期间，我日均完成30单以上的配送任务，准时率达到99.2%。为提升配送效率，我通过分析订单分布和路况信息，自主优化配送路线，使平均配送时长缩短15%，单日最高完成50单。异常订单均在30分钟内解决。凭借细致服务和积极沟通，我获得用户好评率
                                        98%，累计收获点赞超2000次，并多次获评“服务之星”。这段经历让我在高压环境下培养了高效执行、快速应变和持续优化的工作能力。
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="arrow-btn arrow-left light-arrow" data-next="0">◀</div>
            <div class="arrow-btn arrow-right light-arrow" data-next="2">▷</div>
        </div>

        <!-- 第2页：兴趣爱好 -->
        <div class="slide-page page-hobby" data-index="2">
            <div class="page-inner-wrap">
                <h2 class="section-main-title">兴趣爱好 Hobbies</h2>
                <div class="sub-block">
                    <h3>日常爱好清单</h3>
                    <div class="hobby-grid">
                        <div class="hobby-tag">📖 阅读</div>
                        <div class="hobby-tag">🎬 观影放松</div>
                        <div class="hobby-tag">✍️ 写作</div>
                        <div class="hobby-tag">📷 摄影</div>
                        <div class="hobby-tag">🎵 听歌</div>
                        <div class="hobby-tag">🚶 短途旅行</div>
                        <div class="hobby-tag">🍰 美食探店</div>
                    </div>
                </div>
                <div class="sub-block">
                    <h3>我的日常节奏</h3>
                    <div class="daily-card">
                        <div class="daily-item">上午<br>学习专业知识</div>
                        <div class="daily-item">下午<br>设计/文案创作</div>
                        <div class="daily-item">夜晚<br>阅读+观影放松</div>
                    </div>
                </div>
            </div>
            <div class="arrow-btn arrow-left light-arrow" data-next="1">◀</div>
            <div class="arrow-btn arrow-right light-arrow" data-next="3">▷</div>
        </div>

        <!-- 第3页：作品展示 -->
        <div class="slide-page page-portfolio" data-index="3">
            <div class="page-inner-wrap">
                <h2 class="section-main-title">作品展示 Works</h2>
                <div class="port-grid">
                    <!-- 广告海报设计 带双图预览+标题+点击弹窗 -->
                    <div class="port-item" onclick="openPoster()">
                        <div
                            style="display:flex; flex-direction:column; gap:10px; align-items:center; justify-content:center; height:100%; padding:10px;">
                            <div style="display:flex; gap:8px; align-items:center;">
                                <img src="wwwwpic/广告设计.jpg" style="height:140px; border-radius:8px; object-fit:cover;">
                                <img src="wwwwpic/广告设计2.jpg" style="height:140px; border-radius:8px; object-fit:cover;">
                            </div>
                            <span style="font-size:18px; font-weight:600; color:var(--text-dark);">广告海报设计</span>
                        </div>
                    </div>
                    <div class="port-item" onclick="openVideo()">
                        <div
                            style="display:flex;flex-direction:column;gap:10px;align-items:center;justify-content:center;height:100%;padding:10px;">
                            <video src="wwwwpic/44444444.mp4" muted autoplay loop playsinline
                                style="width:100%;height:100%;object-fit:cover;border-radius:10px;">
                            </video>


                        </div>
                    </div>
                    <div class="port-item">
                        <video controls autoplay muted loop playsinline controlsList="nodownload"
                            disablePictureInPicture preload="metadata"
                            style="width:100%;height:100%;object-fit:cover;border-radius:20px;background:#000;">
                            <source src="wwwwpic/动画.mp4" type="video/mp4">

                        </video>
                    </div>
                </div>
            </div>
            <div class="arrow-btn arrow-left light-arrow" data-next="2">◀</div>
            <div class="arrow-btn arrow-right light-arrow" data-next="4">▷</div>
        </div>

        <!-- 第4页：荣誉收获 -->
        <div class="slide-page page-award" data-index="4">
            <div class="page-inner-wrap">
                <h2 class="section-main-title">荣誉收获 Awards</h2>
                <div class="sub-block">
                    <h3>赛事与奖项</h3>
                    <div class="award-list">

                        <div class="award-item">学院奖入围奖</div>
                    </div>
                </div>
                <div class="sub-block">
                    <h3>证书资质</h3>
                    <div class="award-list">
                        <div class="award-item">新媒体运营相关实训证书</div>
                        <div class="award-item">普通话二级甲等证书</div>
                        <div class="award-item">英语四级证书</div>
                    </div>
                </div>
            </div>
            <div class="arrow-btn arrow-left light-arrow" data-next="3">◀</div>
            <div class="arrow-btn arrow-right light-arrow" data-next="5">▷</div>
        </div>

        <!-- 第5页：联系方式（已排序） -->
        <div class="slide-page page-contact" data-index="5">
            <div class="page-inner-wrap">
                <h2 class="section-main-title">联系方式 Contact</h2>
                <div class="contact-box">
                    <div class="contact-item">📍 所在地：安徽省芜湖市</div>
                    <div class="contact-item">📧 邮箱：sooku_2023@qq.com</div>
                    <!-- QQ点击弹窗 -->
                    <div class="contact-item" onclick="showQQ()">
                        QQ：1336588755
                    </div>
                    <!-- 微信点击弹窗 -->
                    <div class="contact-item" onclick="showWX()">
                        📱 微信：wide_wind979904
                    </div>
                </div>
            </div>
            <div class="arrow-btn arrow-left light-arrow" data-next="4">◀</div>
        </div>
    </div>

    <!-- 全局共用弹窗遮罩（只保留一个） -->
    <div class="mask" id="maskWrap" onclick="closeMask()">
        <img class="qr-img" id="qrImgBox" src="">
    </div>

    <script>
        const container = document.getElementById('slideContainer');
        const navLinks = document.querySelectorAll('nav a[data-target]');
        const allBtns = document.querySelectorAll('.arrow-btn, .talk-bubble');
        const welcome = document.getElementById('welcomeText');
        const mask = document.getElementById('maskWrap');
        const qrImg = document.getElementById('qrImgBox');

        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                const targetIdx = link.dataset.target;
                slideTo(targetIdx);
            })
        })
        allBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                const nextIdx = btn.dataset.next;
                slideTo(nextIdx);
            })
        })

        function slideTo(index) {
            const offset = index * -100;
            container.style.transform = `translateX(${offset}vw)`;
            // 每次回到封面，重新播放 WELCOME 动画
            if (index == 0) {
                welcome.style.animation = 'none';
                welcome.offsetHeight;
                welcome.style.animation = 'textPop 2s ease forwards';
            }
        }

        // 广告海报弹窗：同时展示两张海报
        function openPoster() {
            mask.innerHTML = `
        <div style="display:flex; flex-direction:column; gap:20px; align-items:center; max-width:92vw; max-height:90vh;">
            <h3 style="color:#fff; font-size:26px; margin:0;">广告海报设计</h3>
            <div style="display:flex; gap:24px; align-items:center;">
                <img src="wwwwpic/广告设计.jpg" style="max-height:88vh; max-width:44vw; border-radius:10px;">
                <img src="wwwwpic/广告设计2.jpg" style="max-height:88vh; max-width:44vw; border-radius:10px;">
            </div>
        </div>
    `;
            mask.classList.add("show");

        }


        // 打开QQ二维码
        function showQQ() {
            mask.innerHTML = `<img class="qr-img" id="qrImgBox" src="wwwwpic/qq.png">`;
            mask.classList.add("show");
        }
        // 打开微信二维码
        function showWX() {
            mask.innerHTML = `<img class="qr-img" id="qrImgBox" src="wwwwpic/wx.png">`;
            mask.classList.add("show");
        }
        // 关闭弹窗，重置内容
        function closeMask() {
            mask.classList.remove("show");
            mask.innerHTML = `<img class="qr-img" id="qrImgBox" src="">`;
        }
        function openVideo() {
            mask.innerHTML = `
    <div style="display:flex;flex-direction:column;gap:16px;align-items:center;">
        <h3 style="color:#fff;font-size:26px;">短视频剪辑</h3>

        <video
            controls
            autoplay
            playsinline
            style="max-width:90vw;max-height:85vh;border-radius:12px;background:#000;">
            <source src="wwwwpic/44444444.mp4" type="video/mp4">
        </video>
    </div>
    `;
            mask.classList.add("show");
        }
    </script>
</body>

</html># my-website
