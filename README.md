<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Эвакуатор - Быстрая помощь на дороге</title>
    <style>
        /* Общие стили */
        body, html {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background: url('https://raw.githubusercontent.com/username/repository-name/main/images/XXL_height.webp') no-repeat center center fixed;
            background-size: cover;
            color: #333;
        }

        /* Шапка */
        header {
            background-color: rgba(255, 255, 0, 0.9);
            padding: 20px;
            text-align: center;
            font-size: 24px;
            font-weight: bold;
        }

        /* Контейнер услуг */
        section {
            padding: 20px;
            background: rgba(255, 255, 255, 0.9);
            margin: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        }

        .services {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }

        .service {
            background-color: white;
            padding: 20px;
            width: 30%;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            margin: 10px;
            text-align: center;
        }

        /* Форма связи */
        .contact-form {
            display: flex;
            flex-direction: column;
            width: 300px;
            margin: 20px auto;
        }

        .contact-form input, .contact-form textarea {
            margin-bottom: 10px;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        .contact-form button {
            background-color: yellow;
            border: none;
            padding: 10px;
            cursor: pointer;
            font-size: 16px;
        }

        /* Подвал */
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 20px;
        }

        /* Слайдер */
        .slider {
            position: relative;
            max-width: 600px;
            margin: 20px auto;
            overflow: hidden;
            border-radius: 10px;
        }

        .slides {
            display: flex;
            transition: transform 0.5s ease-in-out;
        }

        .slides img {
            width: 100%;
            border-radius: 10px;
        }

        .prev, .next {
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
            background: rgba(0, 0, 0, 0.5);
            color: white;
            border: none;
            padding: 10px;
            cursor: pointer;
            font-size: 20px;
        }

        .prev { left: 10px; }
        .next { right: 10px; }
    </style>
</head>
<body>

<header>
    Эвакуатор - Быстрая помощь на дороге
</header>

<section>
    <h2>Наши услуги</h2>
    <div class="services">
        <div class="service">
            <h3>Стандартная эвакуация</h3>
            <p>Перевозка автомобиля на стандартных условиях по городу или региону.</p>
        </div>
        <div class="service">
            <h3>Экстренная эвакуация</h3>
            <p>Быстрая помощь в случае аварии или поломки автомобиля.</p>
        </div>
        <div class="service">
            <h3>Перевозка автомобилей</h3>
            <p>Перевозка автомобилей с любых типов дорог и условий.</p>
        </div>
    </div>
</section>

<!-- Слайдер изображений -->
<div class="slider">
    <button class="prev" onclick="prevSlide()">&#10094;</button>
    <div class="slides">
        <img src="https://raw.githubusercontent.com/username/repository-name/main/images/image1.jpg" alt="Эвакуатор">
        <img src="https://raw.githubusercontent.com/username/repository-name/main/images/image2.jpg" alt="Помощь на дороге">
        <img src="https://raw.githubusercontent.com/username/repository-name/main/images/image3.jpg" alt="Автоэвакуация">
    </div>
    <button class="next" onclick="nextSlide()">&#10095;</button>
</div>

<footer>
    <p>&copy; Все права защищены.</p>
</footer>

<script>
    let currentIndex = 0;
    
    function showSlide(index) {
        const slides = document.querySelector('.slides');
        const totalSlides = document.querySelectorAll('.slides img').length;
        
        if (index >= totalSlides) currentIndex = 0;
        else if (index < 0) currentIndex = totalSlides - 1;
        else currentIndex = index;
        
        slides.style.transform = `translateX(${-currentIndex * 100}%)`;
    }

    function nextSlide() {
        showSlide(currentIndex + 1);
    }

    function prevSlide() {
        showSlide(currentIndex - 1);
    }
</script>

</body>
</html>
