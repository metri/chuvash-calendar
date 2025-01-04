<div id="flip-calendar" style="display: flex; gap: 20px;">
    <div class="flip-block" id="year-block" style="text-align: center;">
        <h2 id="year-number">2024</h2>
        <p id="year-name" style="font-size: smaller;">Арӑслан <br> Aslan <br> Lion 🦁</p>
    </div>
    <div class="flip-block" id="month-block" style="text-align: center;">
        <h2 id="month-name">Кӑрлач</h2>
        <p style="font-size: smaller;">Ocak <br> January</p>
    </div>
    <div class="flip-block" id="day-block" style="text-align: center;">
        <h2 id="day-number">4</h2>
        <p id="weekday-name" style="font-size: smaller;">Тунти кун <br> Pazartesi <br> Monday</p>
    </div>
</div>

<style>
@keyframes flip {
    0% {
        transform: rotateX(0deg);
    }
    50% {
        transform: rotateX(90deg);
    }
    100% {
        transform: rotateX(180deg);
    }
}

.flip-container {
    perspective: 1000px;
}

.flip-card {
    width: 60px;
    height: 60px;
    position: relative;
    transform-style: preserve-3d;
    animation: flip 1s infinite;
}

.flip-card .front, .flip-card .back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 20px;
    font-weight: bold;
}

.flip-card .back {
    transform: rotateX(180deg);
    background-color: #f0f0f0;
}

.flip-card .front {
    background-color: #4CAF50;
    color: white;
}
</style>

<script>
    // dog-nail
    const yearNames = {
     2001: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2002: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2003: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2004: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2005: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2006: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2007: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2008: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2009: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2010: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2011: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2012: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2013: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2014: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2015: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2016: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2017: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2018: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2019: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2020: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2021: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2022: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2023: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2024: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2025: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2026: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2027: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2028: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2029: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2030: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2031: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2032: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2033: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2034: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2035: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2036: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2037: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2038: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2039: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2040: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2041: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2042: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2043: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2044: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2045: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2046: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2047: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2048: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2049: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2050: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2051: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2052: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2053: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2054: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2055: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2056: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2057: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2058: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2059: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2060: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2061: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2062: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2063: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2064: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2065: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2066: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2067: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2068: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2069: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2070: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2071: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2072: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2073: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2074: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2075: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2076: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2077: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2078: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2079: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2080: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2081: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2082: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2083: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2084: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" },
     2085: { Chuvash: "Ҫӗлен", Türkçe: "Yılan", English: "Snake" },
     2086: { Chuvash: "Ут", Türkçe: "At", English: "Horse" },
     2087: { Chuvash: "Сурӑх", Türkçe: "Koyun", English: "Sheep" },
     2088: { Chuvash: "Пӗҫин", Türkçe: "Maymun", English: "Monkey" },
     2089: { Chuvash: "Чӑх", Türkçe: "Tavuk", English: "Chicken" },
     2090: { Chuvash: "Йытӑ", Türkçe: "Köpek", English: "Dog" },
     2091: { Chuvash: "Сысна", Türkçe: "Domuz", English: "Pig" },
     2092: { Chuvash: "Кушаккайӑк", Türkçe: "Fare", English: "Mouse" },
     2093: { Chuvash: "Ӗне", Türkçe: "İnek", English: "Cow" },
     2094: { Chuvash: "Парӑс", Türkçe: "Pars", English: "Leopard" },
     2095: { Chuvash: "Мулкач", Türkçe: "Tavşan", English: "Rabbit" },
     2096: { Chuvash: "Арӑслан", Türkçe: "Aslan", English: "Lion" }
    ;

    };
    
    const months = {
        1: { chuvash: "Кӑрлач", turkish: "Ocak", english: "January" },
        2: { chuvash: "Нарӑс", turkish: "Şubat", english: "February" },
        3: { chuvash: "Пуш", turkish: "Mart", english: "March" },
        4: { chuvash: "Ака", turkish: "Nisan", english: "April" },
        5: { chuvash: "Ҫу", turkish: "Mayıs", english: "May" },
        6: { chuvash: "Ҫӗртме", turkish: "Haziran", english: "June" },
        7: { chuvash: "Утӑ", turkish: "Temmuz", english: "July" },
        8: { chuvash: "Ҫурла", turkish: "Ağustos", english: "August" },
        9: { chuvash: "Авӑн", turkish: "Eylül", english: "September" },
        10: { chuvash: "Юпа", turkish: "Ekim", english: "October" },
        11: { chuvash: "Чӳк", turkish: "Kasım", english: "November" },
        12: { chuvash: "Раштав", turkish: "Aralık", english: "December" }
    };
    
    const daysOfWeek = {
        0: { chuvash: "Тунти кун", turkish: "Pazar", english: "Monday" },
        1: { chuvash: "Ытлари кун", turkish: "Pazartesi", english: "Tuesday" },
        2: { chuvash: "Юн кун", turkish: "Salı", english: "Wednesday" },
        3: { chuvash: "Кӗҫнерни кун", turkish: "Çarşamba", english: "Thursday" },
        4: { chuvash: "Эрне кун", turkish: "Perşembe", english: "Friday" },
        5: { chuvash: "Шӑмат кун", turkish: "Cuma", english: "Saturday" },
        6: { chuvash: "Вырсарни кун", turkish: "Cumartesi", english: "Sunday" }
    };

    function createFlipClock(value, lang) {
        return `<div class="flip-container">
                    <div class="flip-card">
                        <div class="front">${daysOfWeek[value][lang]}</div>
                        <div class="back">${daysOfWeek[value][lang]}</div>
                    </div>
                </div>`;
    }

    let currentDay = new Date().getDay();
    let currentHour = new Date().getHours();

    document.getElementById('chuvash-day').innerHTML = createFlipClock(currentDay, 'chuvash');
    document.getElementById('english-day').innerHTML = createFlipClock(currentDay, 'english');
    document.getElementById('turkish-day').innerHTML = createFlipClock(currentDay, 'turkish');

    setInterval(() => {
        currentDay = (currentDay + 1) % 7;
        document.getElementById('chuvash-day').innerHTML = createFlipClock(currentDay, 'chuvash');
        document.getElementById('english-day').innerHTML = createFlipClock(currentDay, 'english');
        document.getElementById('turkish-day').innerHTML = createFlipClock(currentDay, 'turkish');
    }, 1000); // Обновление каждую секунду для анимации
</script>
