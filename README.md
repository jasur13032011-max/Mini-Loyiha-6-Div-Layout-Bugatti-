Mana berilgan yangi talablar asosida elementlarni position yordamida ustma-ust joylashtirish, doira shaklidagi profil rasmi, ikonkalarni joylashuvi va z-index boshqaruvi aks etgan to'liq kod strukturasi.

Bu misolda foydalanuvchi profil kartasi (Profile Card) yaratilgan:

1. HTML Tuzilmasi (index.html)
HTML
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profil Karta</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

    <div class="profile-card">
        
        <div class="card-badge">VIP</div>

        <div class="avatar-container">
            <img src="https://i.pravatar.cc/150?img=33" alt="Profil rasmi" class="profile-avatar">
        </div>
        
        <div class="profile-info">
            <h3 class="profile-name">Anvar Aliyev</h3>
            <p class="profile-job">Full-Stack Dasturchi</p>
        </div>

        <div class="social-icons">
            <a href="#" class="icon-link"><i class="fab fa-telegram"></i></a>
            <a href="#" class="icon-link"><i class="fab fa-instagram"></i></a>
            <a href="#" class="icon-link"><i class="fab fa-github"></i></a>
        </div>

    </div>

</body>
</html>
2. CSS Stil Formati (style.css)
CSS
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    /* Gradient fon */
    background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Profil kartasi - Asosiy konteyner */
.profile-card {
    position: relative; /* Ichki absolute elementlar uchun asos bo'ladi */
    width: 300px;
    height: 380px;
    background-color: #ffffff;
    border-radius: 20px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
    padding: 30px;
    text-align: center;
    
    /* Hover effekti uchun silliq o'tish */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

/* Hover: Element biroz yuqoriga ko'tariladi */
.profile-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.15);
}

/* Ustma-ust qo'yish va z-index boshqaruvi (Karta burchagidagi nishon) */
.card-badge {
    position: absolute;
    top: 15px;
    right: 15px;
    background: linear-gradient(135deg, #ff416c 0%, #ff4b2b 100%); /* Gradient fon */
    color: white;
    padding: 5px 12px;
    font-size: 12px;
    font-weight: bold;
    border-radius: 20px;
    z-index: 10; /* Rasm va matnlardan ustki qavatda turishi uchun */
}

/* Profil rasmi konteyneri */
.avatar-container {
    margin-top: 20px;
    margin-bottom: 15px;
}

/* Profil rasmi doira shaklida */
.profile-avatar {
    width: 120px;
    height: 120px;
    border-radius: 50%; /* Rasmni mukammal doira qiladi */
    object-fit: cover;
    border: 4px solid #f0f2f5;
}

/* Matnlar stili */
.profile-name {
    color: #2c3e50;
    font-size: 22px;
    margin-bottom: 5px;
}

.profile-job {
    color: #7f8c8d;
    font-size: 14px;
}

/* Ikonkalarni pastga absolute bilan joylashtirish */
.social-icons {
    position: absolute;
    bottom: 25px; /* Kartaning pastki qismidan masofa */
    left: 0;
    width: 100%; /* Ikonkalarni o'rtaga tekislash uchun kenglik */
    display: flex;
    justify-content: center;
    gap: 15px; /* Ikonkalar orasidagi masofa */
    z-index: 5;
}

/* Ikonka havolalari stili */
.icon-link {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    width: 40px;
    height: 40px;
    background-color: #f1f2f6;
    color: #2c3e50;
    border-radius: 50%;
    text-decoration: none;
    font-size: 18px;
    transition: all 0.2s ease;
}

/* Ikonkaga alohida hover bo'lgandagi effekt */
.icon-link:hover {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); /* Hoverda gradient */
    color: #ffffff;
    transform: translateY(-2px);
}
Kod qanday ishlamoqda (Talablar ijrosi):
position: relative va absolute: .profile-card elementiga relative berildi. Uning ichidagi .card-badge va .social-icons esa absolute orqali kartaning istalgan burchagiga mustaqil joylashtirildi.

Profil rasmi doira shaklida: .profile-avatar klassiga border-radius: 50% berilib, rasm to'liq aylana shakliga keltirildi.

Ikonkalar joylashuvi: .social-icons bloki position: absolute; bottom: 25px; yordamida kartaning eng pastki qismiga mahkamlandi.

Hover effekti: Asosiy kartaga sichqoncha olib borilganda .profile-card:hover orqali transform: translateY(-4px) finti bajarilib, karta silliq ko'tariladi.

z-index boshqaruvi: .card-badge elementiga z-index: 10 berildi, bu uning har qanday holatda boshqa kontentlardan ustki qavatda (oldinda) ko'rinishini ta'minlaydi.

Gradient fon: Ham body foniga, ham karta ichidagi kichik tugma (.card-badge) va ikonka hoverlariga chiroyli rangli gradientlar berildi.
