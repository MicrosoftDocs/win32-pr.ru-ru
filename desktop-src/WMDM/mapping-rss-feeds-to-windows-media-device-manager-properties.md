---
title: сопоставление RSS-каналов с Windows свойствами диспетчер устройств мультимедиа
description: сопоставление RSS-каналов с Windows свойствами диспетчер устройств мультимедиа
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Диспетчер устройств мультимедиа, RSS-каналы
- Диспетчер устройств, RSS-каналы
- инструкции по программированию, RSS-каналы
- Классические приложения, RSS-каналы
- создание Windows мультимедиа диспетчер устройств приложений, rss-каналов
- RSS-каналы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355515217db31740603d5c6323ef8455da4b29ee80bec508897d2d4df5d59bde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031684"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a>сопоставление RSS-каналов с Windows свойствами диспетчер устройств мультимедиа

проигрыватель Windows Media 11 предоставляет функцию агрегатора RSS, которая позволяет пользователям хранить содержимое, полученное из подкастов, на своих компьютерах. В этом разделе описаны элементы XML, найденные в RSS-канале. кроме того, он сопоставляет эти элементы RSS со свойствами Windows мультимедиа диспетчер устройств.

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



в следующей таблице перечислены элементы канала в rss-канале и соответствующие свойства Windows Media диспетчер устройств.



| Элемент Channel | Состояние         | соответствующее свойство диспетчер устройств Windows мультимедиа   |
|-----------------|----------------|-------------------------------------------------------|
| категория        | Необязательный       | [g \_ всзвмдмженре](metadata-constants.md)             |
| cloud           | Неприменимо | Неприменимо                                        |
| авторские права       | Необязательный       | [g \_ всзвмдмпровидеркопиригхт](metadata-constants.md) |
| description     | Обязательно       | [g \_ всзвмдмдескриптион](metadata-constants.md)       |
| Документы            | Неприменимо | Неприменимо                                        |
| генератор       | Неприменимо | Неприменимо                                        |
| Язык        | Неприменимо | Неприменимо                                        |
| ластбуилддате   | Необязательный       | [g \_ всзвмдмластмодифиеддате](metadata-constants.md)  |
| link            | Обязательно       | [g \_ всзвмдмдестинатионурл](metadata-constants.md)    |
| managingEditor  | Необязательный       | [g \_ всзвмдмедитор](metadata-constants.md)            |
| pubDate         | Необязательный       | [g \_ всзвмдмеар](metadata-constants.md)              |
| рейтинг          | Неприменимо | Неприменимо                                        |
| скипдайс        | Неприменимо | Неприменимо                                        |
| скифаурс       | Неприменимо | Неприменимо                                        |
| textInput       | Неприменимо | Неприменимо                                        |
| title           | Обязательно       | [g \_ всзвмдмтитле](metadata-constants.md)             |
| ttl             | Необязательный       | [g \_ всзвмдмтиметоливе](metadata-constants.md)        |
| webMaster       | Необязательный       | [g \_ всзвмдмвебмастер](metadata-constants.md)         |



 

В следующей таблице перечислены элементы Image в RSS-канале и соответствующие свойства ВМДМ.



| Элемент Image | Состояние   | соответствующее свойство диспетчер устройств Windows мультимедиа |
|---------------|----------|-----------------------------------------------------|
| description   | Необязательный | [g \_ всзвмдмдескриптион](metadata-constants.md)     |
| рост        | Необязательный | [g \_ всзвмдмхеигхт](metadata-constants.md)          |
| link          | Необязательный | [g \_ всзвмдмдестинатионурл](metadata-constants.md)  |
| title         | Необязательный | [g \_ всзвмдмтитле](metadata-constants.md)           |
| url           | Необязательный | [g \_ всзвмдмсаурцеурл](metadata-constants.md)       |
| width         | Необязательный | [g \_ всзвмдмвидс](metadata-constants.md)           |



 

в следующей таблице перечислены элементы элементов в rss-канале и соответствующие свойства Windows Media диспетчер устройств.



| Элемент Item | attribute   | Состояние         | соответствующее свойство диспетчер устройств Windows мультимедиа            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| автор       |             | Необязательный       | [g \_ всзвмдмаусор](metadata-constants.md)                     |
| категория     |             | Необязательный       | [g \_ всзвмдмженре](metadata-constants.md)                      |
|              | домен      | Неприменимо | Неприменимо                                                 |
| description  |             | Необязательный       | [g \_ всзвмдмдескриптион](metadata-constants.md)                |
| корпуса    |             | Необязательный       | Неприменимо                                                 |
|              | length      | Обязательно       | [g \_ всзвмдмфилесизе](metadata-constants.md)                   |
|              | type        | Обязательно       | (Тип MIME должен быть сопоставлен с типом содержимого свойства.) |
|              | url         | Обязательно       | [g \_ всзвмдмсаурцеурл](metadata-constants.md)                  |
| guid         |             | Необязательный       | [g \_ всзвмдмедиагуид](metadata-constants.md)                   |
|              | подпостоянная | Неприменимо | Неприменимо                                                 |
| link         |             | Необязательный       | [g \_ всзвмдмдестинатионурл](metadata-constants.md)             |
| pubDate      |             | Необязательный       | [g \_ всзвмдмеар](metadata-constants.md)                       |
| source       |             | Неприменимо | Неприменимо                                                 |
| title        |             | Необязательный       | [g \_ всзвмдмтитле](metadata-constants.md)                      |



 

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



сопоставление элементов RSS-канала со значениями свойств Windows Media диспетчер устройств

в следующей таблице показано, как значения в элементах RSS-канала в предыдущем примере сопоставляются с определенными Windows мультимедиа диспетчер устройств свойства.



| Windows Свойство диспетчер устройств мультимедиа                    | Значение                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [g \_ всзвмдмаусордате](metadata-constants.md)           | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмдескриптион](metadata-constants.md)          | Исполнительный директор по компании Lucerne Питер банков, который просматривает последние тенденции в онлайн-публикациях. |
| [\_ \_ URL-адрес всзвмдмдестинатион g](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [g \_ всзвмдмедитор](metadata-constants.md)               | someone@example.com                                                                           |
| [g \_ всзвмдмфилекреатиондате](metadata-constants.md)     | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмфиленаме](metadata-constants.md)             | Цифровая публикация                                                                       |
| [g \_ всзвмдмфилесизе](metadata-constants.md)             | 13 790                                                                                        |
| [g \_ всзвмдмформаткоде](metadata-constants.md)           | ВМДМ \_ форматкоде \_ мультимедиа \_ -приведение                                                                 |
| [g \_ всзвмдмженре](metadata-constants.md)                | News                                                                                          |
| [\_ \_ Дата изменения всзвмдмласт \_](metadata-constants.md) | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмластмодифиеддате](metadata-constants.md)     | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [g \_ всзвмдмпровидеркопиригхт](metadata-constants.md)    | 2006. Публикация LP ЛЛЛП для компании Lucerne. All Rights Reserved.                                        |
| [g \_ всзвмдмтиметоливе](metadata-constants.md)           | 240                                                                                           |
| [g \_ всзвмдмтитле](metadata-constants.md)                | Цифровая публикация                                                                       |
| [g \_ всзвмдмвебмастер](metadata-constants.md)            | someone@example.com                                                                           |
| [g \_ всзвмдмеар](metadata-constants.md)                 | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |



 

сопоставление элементов изображения RSS с Windows медиа диспетчер устройств значений свойств

в следующей таблице описано, как значения в элементах изображения RSS в предыдущем примере сопоставляются с определенными Windows мультимедиа диспетчер устройств свойства.



| Windows Свойство диспетчер устройств мультимедиа                | Значение                                            |
|------------------------------------------------------|--------------------------------------------------|
| [g \_ всзвмдмалбумковерформат](metadata-constants.md) | \_Формат объекта \_ WPD \_ GIF                         |
| [g \_ всзвмдмалбумковерсизе](metadata-constants.md)   | 512                                              |
| [g \_ всзвмдмдескриптион](metadata-constants.md)      | Логотип компании Lucerne                                     |
| [g \_ всзвмдмдестинатионурл](metadata-constants.md)   | www.lucernepublishing.com/community/podcasts   |
| [g \_ всзвмдмхеигхт](metadata-constants.md)           | 300                                              |
| [g \_ всзвмдмсаурцеурл](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [g \_ всзвмдмтитле](metadata-constants.md)            | Публикация в компании Lucerne                               |
| [g \_ всзвмдмвидс](metadata-constants.md)            | 300                                              |



 

сопоставление элементов RSS-элемента со значениями свойств Windows Media диспетчер устройств

в следующей таблице описано, как значения в элементах элементов RSS в предыдущем примере сопоставляются с определенными Windows мультимедиа диспетчер устройств свойства.



| Windows Свойство диспетчер устройств мультимедиа                | Значение                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [g \_ всзвмдмаусор](metadata-constants.md)           | Компания                                                                                                                             |
| [g \_ всзвмдмаусордате](metadata-constants.md)       | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |
| [g \_ всзвмдмдескриптион](metadata-constants.md)      | Оперативные публикации быстро меняются. Генеральный директор по публикации изучает тенденции за последние пять лет и их последствия. |
| [g \_ всзвмдмдестинатионурл](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ всзвмдмдуратион](metadata-constants.md)         | 120325445                                                                                                                           |
| [g \_ всзвмдмфилекреатиондате](metadata-constants.md) | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |
| [g \_ всзвмдмфилесизе](metadata-constants.md)         | 10329011                                                                                                                            |
| [g \_ всзвмдмформаткоде](metadata-constants.md)       | ВМДМ \_ форматкоде \_ MP3                                                                                                               |
| [g \_ всзвмдмженре](metadata-constants.md)            | News                                                                                                                                |
| [g \_ всзвмдмластмодифиеддате](metadata-constants.md) | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |
| [g \_ всзвмдммедиагуид](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ всзвмдмсаурцеурл](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [g \_ всзвмдмтитле](metadata-constants.md)            | Цифровая публикация                                                                                                             |
| [g \_ всзвмдмеар](metadata-constants.md)             | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Константы метаданных**](metadata-constants.md)
</dt> </dl>

 

 




