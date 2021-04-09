---
title: Сопоставление RSS-каналов со свойствами диспетчер устройств Windows Media
description: Сопоставление RSS-каналов со свойствами диспетчер устройств Windows Media
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Диспетчер устройств Windows Media, RSS-каналы
- Диспетчер устройств, RSS-каналы
- инструкции по программированию, RSS-каналы
- Классические приложения, RSS-каналы
- Создание приложений диспетчер устройств Windows Media, RSS-каналов
- RSS-каналы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887808"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>Сопоставление RSS-каналов со свойствами диспетчер устройств Windows Media

Проигрыватель Windows Media 11 предоставляет функцию агрегатора RSS, которая позволяет пользователям хранить содержимое, полученное из подкастов, на своих компьютерах. В этом разделе описаны элементы XML, найденные в RSS-канале. Кроме того, он сопоставляет эти элементы RSS со свойствами диспетчер устройств Windows Media.

Элементы в RSS-канале имеют следующие иерархию и атрибуты:


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



В следующей таблице перечислены элементы канала в RSS-канале и соответствующие свойства Windows Media диспетчер устройств.



| Элемент Channel | Состояние         | Соответствующее свойство диспетчер устройств Windows Media   |
|-----------------|----------------|-------------------------------------------------------|
| категория        | Необязательно       | [g \_ всзвмдмженре](metadata-constants.md)             |
| cloud           | Неприменимо | Неприменимо                                        |
| авторские права       | Необязательно       | [g \_ всзвмдмпровидеркопиригхт](metadata-constants.md) |
| description;     | Обязательно       | [g \_ всзвмдмдескриптион](metadata-constants.md)       |
| Документы            | Неприменимо | Неприменимо                                        |
| генератор       | Неприменимо | Неприменимо                                        |
| Язык        | Неприменимо | Неприменимо                                        |
| ластбуилддате   | Необязательно       | [g \_ всзвмдмластмодифиеддате](metadata-constants.md)  |
| link            | Обязательно       | [g \_ всзвмдмдестинатионурл](metadata-constants.md)    |
| managingEditor  | Необязательно       | [g \_ всзвмдмедитор](metadata-constants.md)            |
| pubDate         | Необязательно       | [g \_ всзвмдмеар](metadata-constants.md)              |
| рейтинг          | Неприменимо | Неприменимо                                        |
| скипдайс        | Неприменимо | Неприменимо                                        |
| скифаурс       | Неприменимо | Неприменимо                                        |
| textInput       | Неприменимо | Неприменимо                                        |
| title           | Обязательно       | [g \_ всзвмдмтитле](metadata-constants.md)             |
| ttl             | Необязательно       | [g \_ всзвмдмтиметоливе](metadata-constants.md)        |
| webMaster       | Необязательно       | [g \_ всзвмдмвебмастер](metadata-constants.md)         |



 

В следующей таблице перечислены элементы Image в RSS-канале и соответствующие свойства ВМДМ.



| Элемент Image | Состояние   | Соответствующее свойство диспетчер устройств Windows Media |
|---------------|----------|-----------------------------------------------------|
| description;   | Необязательно | [g \_ всзвмдмдескриптион](metadata-constants.md)     |
| рост        | Необязательно | [g \_ всзвмдмхеигхт](metadata-constants.md)          |
| link          | Необязательно | [g \_ всзвмдмдестинатионурл](metadata-constants.md)  |
| title         | Необязательно | [g \_ всзвмдмтитле](metadata-constants.md)           |
| url           | Необязательно | [g \_ всзвмдмсаурцеурл](metadata-constants.md)       |
| width         | Необязательно | [g \_ всзвмдмвидс](metadata-constants.md)           |



 

В следующей таблице перечислены элементы элементов в RSS-канале и соответствующие свойства Windows Media диспетчер устройств.



| Элемент Item | attribute   | Состояние         | Соответствующее свойство диспетчер устройств Windows Media            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| автор       |             | Необязательно       | [g \_ всзвмдмаусор](metadata-constants.md)                     |
| категория     |             | Необязательно       | [g \_ всзвмдмженре](metadata-constants.md)                      |
|              | домен      | Неприменимо | Неприменимо                                                 |
| description;  |             | Необязательно       | [g \_ всзвмдмдескриптион](metadata-constants.md)                |
| корпуса    |             | Необязательно       | Неприменимо                                                 |
|              | length      | Обязательно       | [g \_ всзвмдмфилесизе](metadata-constants.md)                   |
|              | type        | Обязательно       | (Тип MIME должен быть сопоставлен с типом содержимого свойства.) |
|              | url         | Обязательно       | [g \_ всзвмдмсаурцеурл](metadata-constants.md)                  |
| guid         |             | Необязательно       | [g \_ всзвмдмедиагуид](metadata-constants.md)                   |
|              | подпостоянная | Неприменимо | Неприменимо                                                 |
| link         |             | Необязательно       | [g \_ всзвмдмдестинатионурл](metadata-constants.md)             |
| pubDate      |             | Необязательно       | [g \_ всзвмдмеар](metadata-constants.md)                       |
| source       |             | Неприменимо | Неприменимо                                                 |
| title        |             | Необязательно       | [g \_ всзвмдмтитле](metadata-constants.md)                      |



 

Пример

В следующем примере показан полный RSS-канал для вымышленной подкаста, предоставляемого Генеральным директором компании для публикации.


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



Сопоставление элементов RSS-канала со значениями свойств диспетчер устройств Windows Media

В следующей таблице показано, как значения в элементах RSS-канала в предыдущем примере сопоставляются с определенными свойствами Windows Media диспетчер устройств.



| Свойство диспетчер устройств Windows Media                    | Значение                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ всзвмдмаусордате](metadata-constants.md)           | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмдескриптион](metadata-constants.md)          | Исполнительный директор по компании Lucerne Питер банков, который просматривает последние тенденции в онлайн-публикациях. |
| [\_ \_ URL-адрес всзвмдмдестинатион g](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ всзвмдмедитор](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ всзвмдмфилекреатиондате](metadata-constants.md)     | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмфиленаме](metadata-constants.md)             | Цифровая публикация                                                                       |
| [g \_ всзвмдмфилесизе](metadata-constants.md)             | 13 790                                                                                        |
| [g \_ всзвмдмформаткоде](metadata-constants.md)           | ВМДМ \_ форматкоде \_ мультимедиа \_ -приведение                                                                 |
| [g \_ всзвмдмженре](metadata-constants.md)                | Новости                                                                                          |
| [\_ \_ Дата изменения всзвмдмласт \_](metadata-constants.md) | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмластмодифиеддате](metadata-constants.md)     | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмпровидеркопиригхт](metadata-constants.md)    | 2006. Публикация LP ЛЛЛП для компании Lucerne. All Rights Reserved.                                        |
| [g \_ всзвмдмтиметоливе](metadata-constants.md)           | 240                                                                                           |
| [g \_ всзвмдмтитле](metadata-constants.md)                | Цифровая публикация                                                                       |
| [g \_ всзвмдмвебмастер](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ всзвмдмеар](metadata-constants.md)                 | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |



 

Сопоставление элементов изображения RSS со значениями свойств диспетчер устройств Windows Media

В следующей таблице показано, как значения в элементах изображения RSS в предыдущем примере сопоставляются с определенными свойствами Windows Media диспетчер устройств.



| Свойство диспетчер устройств Windows Media                | Значение                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ всзвмдмалбумковерформат](metadata-constants.md) | \_Формат объекта \_ WPD \_ GIF                         |
| [g \_ всзвмдмалбумковерсизе](metadata-constants.md)   | 512                                              |
| [g \_ всзвмдмдескриптион](metadata-constants.md)      | Логотип компании Lucerne                                     |
| [g \_ всзвмдмдестинатионурл](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ всзвмдмхеигхт](metadata-constants.md)           | 300                                              |
| [g \_ всзвмдмсаурцеурл](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ всзвмдмтитле](metadata-constants.md)            | Публикация в компании Lucerne                               |
| [g \_ всзвмдмвидс](metadata-constants.md)            | 300                                              |



 

Сопоставление элементов RSS-элемента со значениями свойств диспетчер устройств Windows Media

В следующей таблице описано, как значения в элементах элементов RSS в предыдущем примере сопоставляются с определенными свойствами Windows Media диспетчер устройств.



| Свойство диспетчер устройств Windows Media                | Значение                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ всзвмдмаусор](metadata-constants.md)           | Компания                                                                                                                             |
| [g \_ всзвмдмаусордате](metadata-constants.md)       | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |
| [g \_ всзвмдмдескриптион](metadata-constants.md)      | Оперативные публикации быстро меняются. Генеральный директор по публикации изучает тенденции за последние пять лет и их последствия. |
| [g \_ всзвмдмдестинатионурл](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ всзвмдмдуратион](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ всзвмдмфилекреатиондате](metadata-constants.md) | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |
| [g \_ всзвмдмфилесизе](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ всзвмдмформаткоде](metadata-constants.md)       | ВМДМ \_ форматкоде \_ MP3                                                                                                               |
| [g \_ всзвмдмженре](metadata-constants.md)            | Новости                                                                                                                                |
| [g \_ всзвмдмластмодифиеддате](metadata-constants.md) | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |
| [g \_ всзвмдммедиагуид](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ всзвмдмсаурцеурл](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ всзвмдмтитле](metadata-constants.md)            | Цифровая публикация                                                                                                             |
| [g \_ всзвмдмеар](metadata-constants.md)             | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Константы метаданных**](metadata-constants.md)
</dt> </dl>

 

 




