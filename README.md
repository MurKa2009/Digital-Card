<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MurKa - Мои контакты</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            color: #f1f1f1;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            background-color: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.5);
            border: 1px solid rgba(255, 255, 255, 0.1);
            text-align: center;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 25px;
            border: 5px solid #58a6ff;
            box-shadow: 0 0 25px rgba(88, 166, 255, 0.5);
        }
        
        h1 {
            font-size: 2.8rem;
            margin-bottom: 10px;
            background: linear-gradient(to right, #58a6ff, #8b949e);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .username {
            font-weight: bold;
            color: #58a6ff;
            font-size: 1.2rem;
            margin-bottom: 5px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            color: #8b949e;
            margin-bottom: 40px;
        }
        
        .contacts-container {
            display: flex;
            flex-direction: column;
            gap: 25px;
            margin: 40px 0;
        }
        
        .contact-card {
            background: rgba(255, 255, 255, 0.1);
            border-radius: 15px;
            padding: 25px;
            display: flex;
            align-items: center;
            text-align: left;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
            cursor: pointer;
        }
        
        .contact-card:hover {
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.15);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .icon {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
            margin-right: 25px;
            flex-shrink: 0;
        }
        
        .github .icon {
            background: linear-gradient(135deg, #333, #6e5494);
            color: white;
        }
        
        .telegram .icon {
            background: linear-gradient(135deg, #0088cc, #34aadc);
            color: white;
        }
        
        .discord .icon {
            background: linear-gradient(135deg, #5865F2, #7289da);
            color: white;
        }
        
        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 8px;
        }
        
        .contact-info p {
            color: #8b949e;
            font-size: 1.1rem;
            margin-bottom: 5px;
        }
        
        .user-id {
            font-weight: bold;
            color: #58a6ff;
            font-size: 1.3rem;
            background: rgba(88, 166, 255, 0.1);
            padding: 5px 10px;
            border-radius: 8px;
            display: inline-block;
            margin-top: 5px;
        }
        
        .copy-btn {
            background: rgba(88, 166, 255, 0.2);
            border: 1px solid #58a6ff;
            color: #58a6ff;
            border-radius: 8px;
            padding: 8px 15px;
            margin-top: 10px;
            cursor: pointer;
            font-size: 0.9rem;
            transition: all 0.3s ease;
        }
        
        .copy-btn:hover {
            background: rgba(88, 166, 255, 0.3);
        }
        
        .copied {
            background: rgba(46, 160, 67, 0.2);
            border-color: #2ea043;
            color: #2ea043;
        }
        
        .footer {
            margin-top: 40px;
            color: #8b949e;
            font-size: 0.9rem;
        }
        
        .stats {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 20px;
            margin-bottom: 30px;
        }
        
        .stat-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 15px 25px;
            border-radius: 12px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .stat-number {
            font-size: 2rem;
            font-weight: bold;
            color: #58a6ff;
        }
        
        .stat-label {
            font-size: 0.9rem;
            color: #8b949e;
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 25px;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            .contact-card {
                flex-direction: column;
                text-align: center;
                padding: 20px;
            }
            
            .icon {
                margin-right: 0;
                margin-bottom: 15px;
            }
            
            .contact-info h3 {
                font-size: 1.3rem;
            }
            
            .stats {
                flex-direction: column;
                gap: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="profile-header">
            <img src="https://avatars.githubusercontent.com/u/110113489?v=4" alt="Фото профиля MurKa" class="profile-img">
            
            <h1>MurKa</h1>
            <div class="username">@MurKa2009</div>
            <p class="subtitle">Разработчик | Программист | Технический энтузиаст</p>
        </div>
        
        <div class="stats">
            <div class="stat-item">
                <div class="stat-number">2015</div>
                <div class="stat-label">Год регистрации</div>
            </div>
         </div>
        
        <div class="contacts-container">
            <!-- GitHub -->
            <div class="contact-card github" onclick="window.open('https://github.com/MurKa2009', '_blank')">
                <div class="icon">
                    <i class="fab fa-github"></i>
                </div>
                <div class="contact-info">
                    <h3>GitHub</h3>
                    <p>Мои проекты и репозитории</p>
                    <div class="user-id">MurKa2009</div>
                    <button class="copy-btn" onclick="copyToClipboard('MurKa2009', this)">Копировать</button>
                </div>
            </div>
            
            <!-- Telegram -->
            <div class="contact-card telegram" onclick="window.open('https://t.me/murka_toper', '_blank')">
                <div class="icon">
                    <i class="fab fa-telegram"></i>
                </div>
                <div class="contact-info">
                    <h3>Telegram</h3>
                    <p>Напишите мне в Telegram</p>
                    <div class="user-id">@murka_toper</div>
                    <button class="copy-btn" onclick="copyToClipboard('@murka_toper', this)">Копировать</button>
                </div>
            </div>
            
            <!-- Discord -->
            <div class="contact-card discord">
                <div class="icon">
                    <i class="fab fa-discord"></i>
                </div>
                <div class="contact-info">
                    <h3>Discord</h3>
                    <p>Свяжитесь со мной в Discord</p>
                    <div class="user-id">murka2009</div>
                    <button class="copy-btn" onclick="copyToClipboard('murka2009', this)">Копировать</button>
                </div>
            </div>
        </div>
        
        <p class="footer">
            Нажмите на карточку для перехода на GitHub или Telegram. Нажмите "Копировать" для копирования username.<br>
            Страница обновлена: сентябрь 2023
        </p>
    </div>

    <script>
        function copyToClipboard(text, button) {
            // Используем современный API для копирования в буфер обмена
            navigator.clipboard.writeText(text).then(() => {
                // Меняем текст кнопки
                const originalText = button.textContent;
                button.textContent = 'Скопировано!';
                button.classList.add('copied');
                
                // Возвращаем исходный текст через 2 секунды
                setTimeout(() => {
                    button.textContent = originalText;
                    button.classList.remove('copied');
                }, 2000);
            }).catch(err => {
                console.error('Не удалось скопировать текст: ', err);
                alert('Не удалось скопировать текст. Попробуйте еще раз.');
            });
            
            // Останавливаем всплытие события, чтобы не срабатывал click на родительском элементе
            event.stopPropagation();
        }
        
        // Обработчик для клика по карточке Discord (без ссылки)
        document.querySelector('.discord').addEventListener('click', function(event) {
            // Если клик был не по кнопке копирования
            if (!event.target.classList.contains('copy-btn')) {
                copyToClipboard('murka2009', this.querySelector('.copy-btn'));
            }
        });
        
        // Динамическая статистика (для демонстрации)
        document.addEventListener('DOMContentLoaded', function() {
            const statNumbers = document.querySelectorAll('.stat-number');
            
            statNumbers.forEach(stat => {
                const target = parseInt(stat.textContent);
                let current = 0;
                const increment = target / 50;
                const timer = setInterval(() => {
                    current += increment;
                    if (current >= target) {
                        current = target;
                        clearInterval(timer);
                    }
                    stat.textContent = Math.floor(current);
                }, 30);
            });
        });
    </script>
</body>
</html>
