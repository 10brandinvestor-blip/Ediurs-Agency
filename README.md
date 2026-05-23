<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome To Ediurs Agency</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            background-color: #0b4a4f; /* Agency Teal Color */
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-family: sans-serif;
            overflow-x: hidden;
        }
        .site-container {
            position: relative;
            width: 100%;
            max-width: 1440px;
            height: auto;
        }
        .canva-design {
            width: 100%;
            height: auto;
            display: block;
        }
        /* Invisible Clickable Links Over the Image */
        .invisible-link {
            position: absolute;
            cursor: pointer;
            background: rgba(255, 255, 255, 0);
        }
        .link-home { top: 0.4%; left: 58%; width: 4.5%; height: 1.2%; }
        .link-contact { top: 0.4%; left: 63%; width: 5.5%; height: 1.2%; }
        .link-overview { top: 0.4%; left: 69.5%; width: 6%; height: 1.2%; }
        .link-services { top: 0.4%; left: 76.5%; width: 5.5%; height: 1.2%; }
        .link-login { top: 0.35%; left: 84.5%; width: 6.5%; height: 1.5%; border-radius: 20px; }
        .main-overview-btn { top: 12.8%; left: 43.8%; width: 11.5%; height: 1.8%; border-radius: 25px; }

        /* FLOATING BLUE ROBOT */
        #ediurs-chatbot-container {
            position: fixed;
            bottom: 30px; 
            right: 30px;
            z-index: 999999 !important;
            display: flex;
            flex-direction: column;
            align-items: flex-end;
        }
        #robot-speech-bubble {
            background: #0b4a4f;
            color: #ffffff;
            padding: 10px 16px;
            border-radius: 18px 18px 2px 18px;
            font-size: 14px;
            font-weight: 600;
            margin-bottom: 12px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.15);
            white-space: nowrap;
            animation: fadeOutSequence 5s forwards;
            animation-delay: 3s;
        }
        #robot-trigger { width: 70px; height: 70px; cursor: pointer; transition: transform 0.3s ease; }
        #robot-trigger:hover { transform: scale(1.1) translateY(-3px); }
        #robot-avatar { width: 100%; height: 100%; object-fit: contain; }

        @keyframes fadeOutSequence {
            0% { opacity: 1; transform: scale(1); }
            100% { opacity: 0; transform: scale(0); display: none; }
        }
        .tawk-minified, #tawk-chat-container, iframe[name^="tawkChatWidget"] {
            display: none !important;
            visibility: hidden !important;
            opacity: 0 !important;
        }
    </style>
</head>
<body>

    <div class="site-container">
        <img src="https://framerusercontent.com/images/egYYOJBqIIcl27XlkyjkNM5nrSg.jpg?scale-down-to=2048&width=8192&height=4672" alt="Ediurs Agency Website" class="canva-design">

        <a href="index.html" class="invisible-link link-home" title="Home"></a>
        <a href="contact.html" class="invisible-link link-contact" title="Contact"></a>
        <a href="overview.html" class="invisible-link link-overview" title="Overview"></a>
        <a href="services.html" class="invisible-link link-services" title="Services"></a>
        <a href="login.html" class="invisible-link link-login" title="Login"></a>
        <a href="overview.html" class="invisible-link main-overview-btn" title="Go to Overview"></a>
    </div>

    <div id="ediurs-chatbot-container">
        <div id="robot-speech-bubble">Hi everyone! 👋</div>
        <div id="robot-trigger" onclick="toggleTawkChat()">
            <img id="robot-avatar" src="https://framerusercontent.com/images/3HBp9bWuNPXdUmznW7zOw3oVp8.png?width=512&height=488" alt="EDIURS Robot Button">
        </div>
    </div>

    <script type="text/javascript">
    var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
    Tawk_API.onLoad = function(){ Tawk_API.hideWidget(); };
    Tawk_API.onChatMinimized = function(){ Tawk_API.hideWidget(); };

    (function(){
    var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
    s1.async=true; s1.src='https://embed.tawk.to/6a0760b558927f1c34944c43/1jomd3i8e';
    s1.charset='UTF-8'; s1.setAttribute('crossorigin','*'); s0.parentNode.insertBefore(s1,s0);
    })();

    function toggleTawkChat() {
        if (window.Tawk_API) {
            if (window.Tawk_API.isChatMaximized()) {
                window.Tawk_API.minimize(); window.Tawk_API.hideWidget();
            } else {
                window.Tawk_API.showWidget(); window.Tawk_API.maximize();
            }
        }
    }
    </script>
</body>
</html>
