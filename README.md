# About-Me
....1
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="../public/contact.html">
  <title>About me</title>

  <script>
  (function () {
    // Скрываем контент как можно раньше
    var css = document.createElement('style');
    css.id = 'gate-css';
    css.textContent = 'body{visibility:hidden}';
    document.head.appendChild(css);

    // Запрашиваем пароль после загрузки DOM
    function ask() {
      var pass = prompt('Введите пароль для входа:');
      if (pass === null) {
        // Не пускаем без пароля
        ask();
        return;
      }
      if (pass === '123456') {
        // Показываем сайт
        document.body.style.visibility = 'visible';
        var el = document.getElementById('gate-css');
        if (el) el.remove();
      } else {
        alert('Неверный пароль. Попробуйте снова.');
        ask();
      }
    }

    window.addEventListener('DOMContentLoaded', ask);
  })();
  </script>
</head>
<body style="background-color: rgb(16, 16, 16);">
  <h1 style="color: rgb(0, 249, 5);">About me</h1>
  <hr>
  <p style="color: rgb(2, 245, 2);">Hi my Name is Asadbek Im 12 y old I can say i want to work in all works in the world!
    you can say it so strange but i want it and my second usually work is business
    I read a book how rich dad and poor dad there says what robert want to work 
    on differents works he says its so interesting And I also want to try it!
    <hr>
  </p>
  <img src="https://litmir.club/data/Author/272000/272964/%D0%A4%D0%BE%D1%82%D0%BE_%D0%9B%D0%BE%D1%85%D0%BC%D0%B0%D1%82%D1%8B%D0%B9_%D0%90%D0%BD%D0%BE%D0%BD%D0%B8%D0%BC_2c0e0.jpg" alt="Me">
  <br>
<p style="color: rgb(2, 248, 47);">I Have a question! Did you want to try Hacking 
  This Site can help with them!
  <hr>
</p>
<p style="color: rgb(4, 248, 28);">🔑 Взлом ≠ всегда преступление
Есть "чёрные" хакеры (Black Hat), которые нарушают закон ради выгоды, и "белые" (White Hat) — специалисты по кибербезопасности, которые ищут уязвимости, чтобы компании их исправили.

🛡️ Самая частая причина взломов — слабые пароли
Пароли типа 123456, qwerty, password ломаются за секунды.

📱 Фишинг опаснее, чем хакерские программы
В большинстве случаев люди сами "отдают" данные, переходя по поддельным ссылкам или скачивая вирусные файлы.

🌍 Первый вирус появился в 1986 году
Он назывался Brain, его написали два брата из Пакистана.

💻 Хакеры часто используют социальную инженерию
Это не только взлом компьютеров, но и манипуляции людьми (например, позвонить и представиться техподдержкой).

⚡ DDoS-атаки
Сайты иногда падают не из-за взлома базы данных, а потому что их "заваливают" миллионами запросов.

🚀 Хакерские атаки происходят каждую секунду
По статистике, в мире фиксируют тысячи попыток взлома ежесекундно.

🔒 Шифрование — главный враг хакеров
Чем лучше зашифрована информация (например, с помощью 2FA и современных алгоритмов), тем сложнее её украсть.</p>
<img src="https://d2qt3hjxf3fk7j.cloudfront.net/wp-content/uploads/2024/12/19181953/system-hacked-warning-alert-on-laptop1-1-400x200.jpg" alt="Hacking"><br>
<button><a href="http://abdumalikov.lunaweb.ru/">Hacking</a></button><br>
<hr>
<p style="color: rgb(0, 252, 84);">ТОП-10 самых известных взломов в истории:

Yahoo (2013–2014)
🔓 Самый большой взлом аккаунтов: украли данные более 3 миллиардов пользователей (логины, пароли, e-mail).

Equifax (2017)
📂 Утекли личные данные 147 миллионов американцев: номера соцстраховок, адреса, даты рождения.

Sony Pictures (2014)
🎬 Хакеры взломали студию, слили фильмы и переписку сотрудников. Атака приписывается группе из Северной Кореи.

PlayStation Network (2011)
🎮 Украдены данные 77 миллионов игроков (включая данные карт). Сеть была отключена почти на месяц.

Target (2013)
🛒 Взломали сеть супермаркетов Target. Украли данные 40 миллионов банковских карт.

Twitter (2020)
🐦 Взломали аккаунты Илона Маска, Барака Обамы, Билла Гейтса и других — для мошенничества с биткойнами.

Adult FriendFinder (2016)
🔥 Утекло более 400 миллионов аккаунтов с личными данными пользователей.

LinkedIn (2012)
👔 Украли около 165 миллионов паролей пользователей.

NASA (1999)
🚀 15-летний подросток взломал NASA и скачал исходный код, управляющий МКС. Ущерб оценили в 41 тысячу $.

WannaCry (2017)
🦠 Массовая атака вируса-шифровальщика, заразившего более 230 тысяч компьютеров в 150 странах.

⚡ Эти истории показывают, что взломы могут затронуть миллионы людей и даже правительства.</p>
<button><a href="../public/contact.html">My number</a></button>
<hr>
<p>My phone number </p>
</body>
</html>

