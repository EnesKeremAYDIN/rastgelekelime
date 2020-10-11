# rastgelekelime

## Bir (yada daha fazla) Türkçe kelime çıktısı alın.

random-words [GitHub](https://github.com/punkave/random-words) [NPM](https://www.npmjs.com/package/random-words) projesi düzenlenerek oluşturulmuştur.

[![Visitor](https://visitor-badge.laobi.icu/badge?page_id=EnesKeremAYDIN.rastgelekelime)](#)
[![Discord](https://discord.com/api/guilds/718831818589339701/widget.png)](https://discord.gg/wUP74GZ)
[![Steam](https://img.shields.io/badge/donate-steam-blue?logo=Steam&style=flat-square)](https://steamcommunity.com/tradeoffer/new/?partner=434566573&token=g789u6Uv)
[![Patreon](https://img.shields.io/badge/Donate-Patreon-red.svg)](https://discord.gg/wUP74GZ)
[![NPM Sürüm](https://img.shields.io/npm/v/rastgelekelime.svg?maxAge=3600)](https://www.npmjs.com/package/rastgelekelime)
[![NPM İndirme Sayısı](https://img.shields.io/npm/dt/rastgelekelime.svg?maxAge=3600)](https://www.npmjs.com/package/rastgelekelime)
[![Kod satırı sayısı](https://tokei.rs/b1/github/EnesKeremAYDIN/rastgelekelime)](https://github.com/EnesKeremAYDIN/rastgelekelime)
[![Dökümanlar](https://img.shields.io/badge/💡-docs-00ACD7.svg?style=flat)](https://github.com/EnesKeremAYDIN/rastgelekelime)
[![NPM Genel](https://nodei.co/npm/rastgelekelime.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/rastgelekelime)

Kurulum:

    npm install rastgelekelime

Örnek:

    var kelime = require('rastgelekelime');

    console.log(kelime()); // Bir adet çıktı almanızı sağlar.
    örnek

    console.log(kelime(5)); // Belirlediğiniz kadar (Örn:5) çıktı almanızı sağlar.
    ['örnek', 'örnek', 'örnek', 'örnek', 'örnek']

    console.log(kelime({ min: 3, max: 10 })); // Belirli sayı aralığı kadar (örn: 3-10 arası) çıktı almanızı sağlar.
    ['örnek', 'örnek', 'örnek', 'örnek', 'örnek', 'örnek', 'örnek']

    console.log(kelime({ exactly: 2 })); // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar.
    ['örnek', 'örnek']

    console.log(kelime({ exactly: 5, join: ' ' })) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. Çıktı alınan kelimelerin arasına belirlediğiniz karakteri (örn: boşluk) koyar.
    ['örnek örnek örnek örnek örnek']

    console.log(kelime({ exactly: 5, join: '' })) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. Çıktı alınan kelimelerin arasına bir şey koymaz, yapışık çıktı verir.
    ['örnekörnekörnekörnekörnek']

    console.log(kelime({exactly: 5, maxLength: 4})) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. En fazla belirlediğiniz uzunlukta (örn: 4) çıktı almanızı sağlar.
    ['örn', 'örnk', 'rnk', 'örnk', 'ör']

    console.log(kelime({exactly:5, wordsPerString:2})) // Kesinlikle belirlediğiniz kadar (örn: 5) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar.
    ['örnek örnek', 'örnek örnek', 'örnek örnek', 'örnek örnek', 'örnek örnek']

    console.log(kelime({exactly:5, wordsPerString:2, separator:'-'})) // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar. Çıktı alınan kelimelerin arasına belirlediğiniz karakteri (örn: -) koyar.
    ['örnek-örnek', 'örnek-örnek', 'örnek-örnek', 'örnek-örnek', 'örnek-örnek']

    console.log(kelime({exactly:5, wordsPerString:2, formatter: (word)=> word.toUpperCase()})) // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar. Çıktıların tüm harflerini büyük harfle yazdırır.
    ['ÖRNEK ÖRNEK', 'ÖRNEK ÖRNEK', 'ÖRNEK ÖRNEK', 'ÖRNEK ÖRNEK', 'ÖRNEK ÖRNEK']

    console.log(kelime({exactly:5, wordsPerString:2, formatter: (word, index)=> {return index === 0 ? word.slice(0,1).toUpperCase().concat(word.slice(1)) : word;}}))  // Kesinlikle belirlediğiniz kadar (örn: 2) çıktı almanızı sağlar. Alınan çıktının yanında kaç adet çıktı olmasını (örn: 2) seçmenizi sağlar. Çıktıların ilk harfini büyük yazdırır.
    ['Örnek örnek', 'Örnek örnek', 'Örnek örnek', 'Örnek örnek', 'Örnek örnek']
