<script>
document.addEventListener('DOMContentLoaded', function () {
    const currentYear = new Date().getFullYear();
    const rows = document.querySelectorAll('table tr');

    rows.forEach(row => {
        const yearCell = row.querySelector('td, th');
        if (yearCell && parseInt(yearCell.innerText) === currentYear) {
            row.style.fontWeight = 'bolder';
            row.style.color = 'White';
            row.style.backgroundColor = 'DarkRed';
            row.style.fontSize = '1.1em';
            row.style.transform = 'scale(1.1)';
            row.style.transformOrigin = 'center';
        }
    });
});
</script>


| Year | Chuvash | Türkçe | English | Russian |
|------|---------------------|------------------|-----------------------------------|------------------|
| 2001 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2002 | Ут                  | At               | Horse                             | Конь             |
| 2003 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2004 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2005 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2006 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2007 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2008 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2009 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2010 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2011 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2012 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2013 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2014 | Ут                  | At               | Horse                             | Конь             |
| 2015 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2016 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2017 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2018 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2019 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2020 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2021 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2022 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2023 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2024 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2025 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2026 | Ут                  | At               | Horse                             | Конь             |
| 2027 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2028 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2029 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2030 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2031 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2032 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2033 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2034 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2035 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2036 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2037 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2038 | Ут                  | At               | Horse                             | Конь             |
| 2039 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2040 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2041 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2042 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2043 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2044 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2045 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2046 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2047 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2048 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2049 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2050 | Ут                  | At               | Horse                             | Конь             |
| 2051 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2052 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2053 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2054 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2055 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2056 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2057 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2058 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2059 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2060 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2061 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2062 | Ут                  | At               | Horse                             | Конь             |
| 2063 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2064 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2065 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2066 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2067 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2068 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2069 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2070 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2071 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2072 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2073 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2074 | Ут                  | At               | Horse                             | Конь             |
| 2075 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2076 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2077 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2078 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2079 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2080 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2081 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2082 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2083 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2084 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2085 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2086 | Ут                  | At               | Horse                             | Конь             |
| 2087 | Сурӑх               | Koyun            | Sheep                             | Овца             |
| 2088 | Пӗҫин               | Maymun           | Monkey                            | Обезьяна         |
| 2089 | Чӑх                 | Tavuk            | Chicken                           | Курица           |
| 2090 | Йытӑ                | Köpek            | Dog                               | Собака           |
| 2091 | Сысна               | Domuz            | Pig                               | Свинья           |
| 2092 | Кушаккайӑк          | Fare             | Mouse                             | Мышь             |
| 2093 | Ӗне                 | İnek             | Cow                               | Корова           |
| 2094 | Парӑс               | Pars             | Leopard                           | Барс             |
| 2095 | Мулкач              | Tavşan           | Rabbit                            | Заяц             |
| 2096 | Арӑслан             | Aslan            | Lion                              | Лев              |
| 2097 | Ҫӗлен               | Yılan            | Snake                             | Змея             |
| 2098 | Ут                  | At               | Horse                             | Конь             |
| 2099 | Сурӑх               | Koyun            | Sheep                             | Овца             |
