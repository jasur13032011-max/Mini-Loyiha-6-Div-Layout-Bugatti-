# Mini-Loyiha-6-Div-Layout-Bugatti-

Conversation with Gemini
 Требования

✅ <div> larni to'g'ri tuzilmada joylashtiring

✅ Fon rangi yoki gradient

✅ Shrift va matn rangini belgilang

✅ Rasmni CSS bilan boshqaring (max-width, object-fit)

✅ margin va padding

✅ Hover effekti

Mana berilgan talablarga to'liq javob beradigan, toza va zamonaviy tuzilmaga ega HTML va CSS kodlari. Bu misolda chiroyli rasm kartasi (Card component) yaratilgan:

1. HTML Tuzilmasi (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zamonaviy Karta</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="card-container">
        
        <div class="card-image-wrapper">
            <img src="https://picsum.photos/600/400" alt="Tabiat rasmi" class="card-img">
        </div>
        
        <div class="card-content">
            <h2 class="card-title">Gofret va Sayohat</h2>
            <p class="card-text">
                Ushbu karta zamonaviy CSS metodlari yordamida yaratildi. Hover effekti, to'g'ri padding va margin o'lchamlari hamda chiroyli gradient fonga ega.
            </p>
            <button class="card-btn">Batafsil</button>
        </div>

    </div>

</body>
</html>
2. CSS Stil Formati (style.css)
CSS
/* Umumiy sozlamalar va Shrift */
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    /* Fon uchun chiroyli gradient */
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

/* Karta konteyneri */
.card-container {
    background-color: #ffffff;
    border-radius: 15px;
    overflow: hidden;
    max-width: 350px;
    width: 100%;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.15);
    
    /* Margin: kartani atrofdan masofalash uchun */
    margin: 20px; 
    
    /* Hover effekti uchun silliq o'tish */
    transition: transform 0.3s ease, box-shadow 0.3s ease; 
}

/* Rasm qismi (CSS bilan boshqarish) */
.card-image-wrapper {
    width: 100%;
    height: 200px;
    overflow: hidden;
}

.card-img {
    width: 100%;
    height: 100%;
    max-width: 100%; /* Rasmni CSS bilan chegaralash */
    object-fit: cover; /* Rasm cho'zilib ketmasligi uchun */
    transition: transform 0.5s ease;
}

/* Matn qismi va Padding */
.card-content {
    padding: 25px; /* Ichki masofa */
}

/* Shrift va matn ranglari */
.card-title {
    font-size: 1.5rem;
    font-weight: 600;
    color: #2d3748; /* To'q rangli matn */
    margin-bottom: 12px; /* Pastki masofa */
}

.card-text {
    font-size: 0.95rem;
    color: #718096; /* Ochroq matn rangi */
    line-height: 1.6;
    margin-bottom: 20px;
}

/* Tugma stili */
.card-btn {
    padding: 10px 20px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: #ffffff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s ease;
}

/* --- Hover Effektlari --- */

/* Kartaning o'ziga hover bo'lganda */
.card-container:hover {
    transform: translateY(-10px); /* Tepaga biroz ko'tariladi */
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.25);
}

/* Karta ustiga borganda rasmning yaqinlashishi */
.card-container:hover .card-img {
    transform: scale(1.1);
}

/* Tugmaga alohida hover */
.card-btn:hover {
    opacity: 0.9;
}
Kod qanday talablarni bajardi:
divlar mantiqiy ravishda card-container → card-image-wrapper va card-content qismlariga ajratildi.

body qismida zamonaviy binafsha-ko'k gradient ishlatildi.

Google Fonts orqali Poppins shrifti ulandi, sarlavha va matnga alohida ranglar berildi.

Rasm uchun max-width: 100% va object-fit: cover xususiyatlari qo'llanildi.

margin va padding o'lchamlari elementlar siqilib qolmasligi uchun to'g'ri taqsimlandi.

.card-container:hover orqali karta yuqoriga siljiydi, soyasi kattalashadi va ichidagi rasm biroz yaqinlashadi (scale).




Gemini isn’t human. It can make mistakes, so double-check it.

