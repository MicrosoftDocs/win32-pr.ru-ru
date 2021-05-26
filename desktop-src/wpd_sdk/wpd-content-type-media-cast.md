---
description: '\_приведение \_ носителя типа содержимого \_ WPD \_'
ms.assetid: 368e7381-8978-421a-b450-59915f8e70e2
title: WPD_CONTENT_TYPE_MEDIA_CAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d45c9bc1e8e41bae526f02102d341ef00fad435
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423464"
---
# <a name="wpd_content_type_media_cast"></a>\_приведение \_ носителя типа содержимого \_ WPD \_

Объект, описывающий его тип как \_ тип содержимого \_ WPD \_ Cast, \_ представляет коллекцию связанных содержимого.

Объект Медиакаст можно рассматривать как объект-контейнер, группирующий связанное содержимое, как и список воспроизведения. Часто объект Медиакаст используется для группировки мультимедийного содержимого, опубликованного в сети. Например, RSS-канал может быть представлен как объект Медиакаст, объект которого ссылается на объекты содержимого, представляющие каждый элемент в канале.

Этот тип объекта поддерживает следующие свойства.



| Имя свойства             |  Обязательный или необязательный         |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [\_идентификатор объекта \_ WPD](object-properties.md)                                                                | Обязательный.                                                             |
| [\_ \_ идентификатор родительского объекта \_ WPD](object-properties.md)                                                 | Обязательный.                                                             |
| [\_имя объекта \_ WPD](object-properties.md)                                                            | Требуется, если объект представляет файл.                             |
| [\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD](object-properties.md)                          | Обязательный.                                                             |
| [\_Формат объекта \_ WPD](object-properties.md)                                                        | Обязательный.                                                             |
| [\_ \_ тип содержимого объекта \_ WPD](object-properties.md)                                           | Обязательный.                                                             |
| [\_объект WPD \_](object-properties.md)                                                    | Требуется, если объект скрыт.                                     |
| [\_система объектов \_ WPD](object-properties.md)                                                    | Требуется, если объект является системным объектом (представляет системный файл). |
| [\_размер объекта \_ WPD](object-properties.md)                                                            | Требуется, если у объекта есть по крайней мере один ресурс.                     |
| [\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD](object-properties.md)                              | Требуется, если объект представляет файл.                             |
| [\_объект WPD \_ не \_ поднимается](object-properties.md)                                       | Рекомендуется, если объект не предназначен для использования устройством. |
| [\_ \_ ссылки на объекты WPD](object-properties.md)                                                | Требуется, если объект содержит ссылки на другие объекты.               |
| [\_ \_ Ключевые слова объекта WPD](object-properties.md)                                                    | Необязательный элемент.                                                             |
| [\_ \_ идентификатор синхронизации объекта \_ WPD](object-properties.md)                                                     | Необязательный элемент.                                                             |
| [\_объект WPD \_ \_ защищен DRM \_](object-properties.md)                                  | Требуется, если объект защищен с помощью технологии DRM.                |
| [\_ \_ Дата создания объекта \_ WPD](object-properties.md)                                           | Необязательный элемент.                                                             |
| [\_ \_ Дата изменения объекта \_ WPD](object-properties.md)                                         | (рекомендуется).                                                          |
| [\_ \_ Дата создания объекта \_ WPD](object-properties.md)                                         | Необязательный элемент.                                                             |
| [\_ \_ обратные ссылки объекта WPD \_](object-properties.md)                                     | Рекомендуется, если на объект ссылается другой объект.            |
| [\_ \_ \_ идентификатор функционального \_ объекта контейнера объектов \_ WPD](object-properties.md)     | Необязательный элемент.                                                             |
| [Объект WPD, \_ \_ создающий \_ эскиз \_ из \_ ресурса](object-properties.md) | Необязательный элемент.                                                             |
| [\_объект WPD \_ может \_ удалить](object-properties.md)                                               | Требуется, если объект можно удалить.                                |
| [\_ \_ языковой стандарт объекта WPD \_](object-properties.md)                                                                | Требуется, если объект не может быть удален.                             |
| [устройство WPD, \_ \_ авторские права](media-properties.md)                                                     | Необязательный элемент.                                                             |
| [Возрастная \_ \_ Категория устройства WPD \_](media-properties.md)                                        | Необязательный элемент.                                                             |
| [\_ \_ мета жанр мультимедиа \_ WPD](media-properties.md)                                                  | Необязательный элемент.                                                             |
| [\_подзаголовок носителя WPD \_ \_](media-properties.md)                                                    | Необязательный элемент.                                                             |
| [\_ \_ Дата выпуска носителя \_ WPD](media-properties.md)                                              | (рекомендуется).                                                          |
| [\_заголовок носителя \_ WPD](media-properties.md)                                                             | (рекомендуется).                                                          |
| [\_владелец носителя \_ WPD](media-properties.md)                                                             | (рекомендуется).                                                          |
| [\_Редактор управления носителями WPD \_ \_](media-properties.md)                                        | (рекомендуется).                                                          |
| [\_Мастер мультимедиа \_ WPD](media-properties.md)                                                     | (рекомендуется).                                                          |
| [\_ \_ \_ URL-адрес источника мультимедиа WPD](media-properties.md)                                                  | (рекомендуется).                                                          |
| [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md)                                        | (рекомендуется).                                                          |
| [\_Описание носителя \_ WPD](media-properties.md)                                                 | Необязательный элемент.                                                             |
| [\_Жанр носителя \_ WPD](media-properties.md)                                                             | Необязательный элемент.                                                             |
| [\_Закладка \_ объекта мультимедиа WPD \_](media-properties.md)                                        | Рекомендуемая                                                           |
| [\_ \_ \_ Дата последней сборки \_ устройства WPD](media-properties.md)                                       | (рекомендуется).                                                          |
| [\_ \_ время \_ \_ жизни носителя (WPD)](media-properties.md)                                             | Необязательный элемент.                                                             |
| [Описание подпрограммы \_ типа WPD Media \_ \_](object-properties.md)                                                                 | Необязательный элемент.                                                             |



 

## <a name="typical-resources"></a>Типичные ресурсы

Эти объекты обычно включают в себя следующие ресурсы.



| Имя ресурса                                               | Обязательный или необязательный | Описание                                                                                                                 |
|-------------------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**\_ресурс \_ по умолчанию для WPD**](wpd-resource-default.md)      | Необязательный элемент.            | Содержит данные файла медиакаст. Например, если этот медиакаст представляет RSS-канал, это может быть документ RSS. |
| [**\_эскиз ресурса \_ WPD**](wpd-resource-thumbnail.md)  | Необязательный элемент.            | Содержит эскиз, представляющий этот медиакаст.                                                                         |
| [**\_ \_ Обложка ресурсов \_ WPD**](wpd-resource-album-art.md) | Необязательный элемент.            | Содержит иллюстрацию для этого медиакаст.                                                                                    |



 

## <a name="mapping-of-rss-elements-and-mediacast-properties"></a>Сопоставление элементов RSS и свойств Медиакаст

RSS-канал можно представить в виде объекта Медиакаст, ссылки на который указывает на объекты содержимого, представляющие каждый элемент в определенном канале.

Элементы в RSS-канале имеют следующие иерархию и атрибуты.


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



В следующей таблице перечислены элементы канала RSS-канала и соответствующие \_ \_ свойства типа содержимого WPD \_ \_ .



| Элемент Channel | Требование к RSS-каналу | Соответствующее свойство Медиакаст      |
|---------------------|--------------------------|---------------------------------------------------------------------------------|
| категория            | Необязательный элемент.                | [\_Жанр носителя \_ WPD](media-properties.md)                       |
| cloud               | Неприменимо.          | Неприменимо.                                                                 |
| авторские права           | Необязательный элемент.                | [устройство WPD, \_ \_ авторские права](media-properties.md)               |
| description         | Обязательный.                | [\_Описание носителя \_ WPD](media-properties.md)           |
| Документы                | Неприменимо.          | Неприменимо.                                                                 |
| генератор           | Неприменимо.          | Неприменимо.                                                                 |
| Язык            | Неприменимо.          | Неприменимо.                                                                 |
| ластбуилддате       | Необязательный элемент.                | [\_ \_ \_ Дата последней сборки \_ устройства WPD](media-properties.md) |
| link                | Обязательный.                | [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md)  |
| managingEditor      | Необязательный элемент.                | [\_Редактор управления носителями WPD \_ \_](media-properties.md)  |
| pubDate             | Необязательный элемент.                | [\_ \_ Дата выпуска носителя \_ WPD](media-properties.md)        |
| рейтинг              | Неприменимо.          | Неприменимо.                                                                 |
| скипдайс            | Неприменимо.          | Неприменимо.                                                                 |
| скифаурс           | Неприменимо.          | Неприменимо.                                                                 |
| textInput           | Неприменимо.          | Неприменимо.                                                                 |
| title               | Обязательный.                | [\_имя объекта \_ WPD](object-properties.md)                      |
| ttl                 | Необязательный элемент.                | [\_ \_ время \_ \_ жизни носителя (WPD)](media-properties.md)       |
| webMaster           | Необязательный элемент.                | [\_Мастер мультимедиа \_ WPD](media-properties.md)               |



 

В следующей таблице перечислены элементы изображения в RSS-канале и соответствующие \_ \_ свойства типа содержимого WPD \_ \_ .



| Элемент Image | Требование к RSS-каналу | Медиакаст, свойство                     |
|-------------------|--------------------------|--------------------------------------------------------------------------------|
| description       | Необязательный элемент.                | [\_Описание носителя \_ WPD](media-properties.md)          |
| рост            | Необязательный элемент.                | [\_Высота устройства \_ WPD](media-properties.md)                    |
| link              | Необязательный элемент.                | [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md) |
| title             | Необязательный элемент.                | [\_имя объекта \_ WPD](object-properties.md)                     |
| url               | Необязательный элемент.                | [\_ \_ \_ URL-адрес источника мультимедиа WPD](media-properties.md)           |
| width             | Необязательный элемент.                | [\_Ширина носителя \_ WPD](media-properties.md)                      |



 

В следующей таблице перечислены элементы элементов в RSS-канале и соответствующие \_ \_ свойства типа содержимого WPD \_ \_ .



| Элемент Item | attribute | Требование к RSS-каналу | Медиакаст, свойство  |
|------------------|---------------|--------------------------|--------------------------------------------------------------------------------|
| автор           |               | Необязательный элемент.                | [\_исполнитель мультимедиа \_ WPD](media-properties.md)                    |
| категория         |               | Необязательный элемент.                | [\_Жанр носителя \_ WPD](media-properties.md)                      |
|                  | домен        | Неприменимо.          | Неприменимо.                                                                |
| description      |               | Необязательный элемент.                | [\_Описание носителя \_ WPD](media-properties.md)          |
| корпуса        |               | Необязательный элемент.                |                                                                                |
|                  | url           | Обязательный.                | [\_ \_ \_ URL-адрес источника мультимедиа WPD](media-properties.md)           |
|                  | length        | Обязательный.                | [\_размер объекта \_ WPD](object-properties.md)                     |
|                  | тип          | Обязательный.                | (Тип MIME должен быть сопоставлен с типом содержимого свойства.)                 |
| guid             |               | Необязательный элемент.                | [\_GUID носителя \_ WPD](media-properties.md)                        |
|                  | подпостоянная   | Неприменимо.          | Неприменимо.                                                                |
| link             |               | Необязательный элемент.                | [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md) |
| pubDate          |               | Необязательный элемент.                | [\_ \_ Дата выпуска носителя \_ WPD](media-properties.md)       |
| source           |               | Неприменимо.          | Неприменимо.                                                                |
| title            |               | Необязательный элемент.                | [\_имя объекта \_ WPD](object-properties.md)                     |



 

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
    <link>https://www.lucernepublishing.com/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past 5 years and their implications.</description>
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



## <a name="mapping-rss-channel-elements-to-wpd-property-values"></a>Сопоставление элементов RSS-канала со значениями свойств WPD

В следующей таблице описано, как значения в элементах RSS-канала в предыдущем примере сопоставляются с определенными свойствами WPD.



| Свойство WPD | Значение |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [устройство WPD, \_ \_ авторские права](media-properties.md)                            | 2006. Публикация LP ЛЛЛП для компании Lucerne. All Rights Reserved.                                        |
| [\_Описание носителя \_ WPD](media-properties.md)                        | Исполнительный директор по компании Lucerne Питер банков, который просматривает последние тенденции в онлайн-публикациях. |
| [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md)               | https://www.lucernepublishing.com/services/podcasting                                          |
| [\_Жанр носителя \_ WPD](media-properties.md)                                    | Новости                                                                                          |
| [\_ \_ \_ Дата последней сборки \_ устройства WPD](media-properties.md)              | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [\_Редактор управления носителями WPD \_ \_](media-properties.md)               | someone@example.com                                                                           |
| [\_ \_ Дата выпуска носителя \_ WPD](media-properties.md)                     | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [\_ \_ время \_ \_ жизни носителя (WPD)](media-properties.md)                    | 240                                                                                           |
| [\_заголовок носителя \_ WPD](media-properties.md)                                    | Цифровая публикация                                                                       |
| [\_ \_ \_ URL-адрес источника мультимедиа WPD](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publication/rss.xml                  |
| [\_Мастер мультимедиа \_ WPD](media-properties.md)                            | someone@example.com                                                                           |
| [\_ \_ тип содержимого объекта \_ WPD](object-properties.md)                  | \_приведение \_ носителя типа содержимого \_ WPD \_                                                               |
| [\_ \_ Дата создания объекта \_ WPD](object-properties.md)                | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [\_ \_ Дата создания объекта \_ WPD](object-properties.md)                  | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [\_ \_ Дата изменения объекта \_ WPD](object-properties.md)                | Пятница, 9 июня 2006 14:00:28, EDT                                                                 |
| [\_Формат объекта \_ WPD](object-properties.md)                               | \_приведение \_ \_ абстрактного \_ носителя в формате \_ объекта WPD                                                    |
| [\_идентификатор объекта \_ WPD](object-properties.md)                                       | Зависящее от сеанса значение.                                                                      |
| [\_имя объекта \_ WPD](object-properties.md)                                   | Цифровая публикация                                                                       |
| [\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD](object-properties.md)     | Цифровая публикация                                                                       |
| [\_ \_ идентификатор родительского объекта \_ WPD](object-properties.md)                        | Миподкастс (вымышленная папка подкастов на устройстве). В этом примере предполагается "0A0".        |
| [\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD](object-properties.md) | Независимое от сеанса значение. (Для этого примера предполагается "0A1".)                                   |
| [\_ \_ ссылки на объекты WPD](object-properties.md)                       | 0A2 для N элементов<br/>                                                                   |
| [\_размер объекта \_ WPD](object-properties.md)                                   | 13 790                                                                                        |



 

## <a name="mapping-rss-image-elements-to-wpd-property-values"></a>Сопоставление элементов изображения RSS со значениями свойств WPD

В следующей таблице описано, как значения в элементах изображения RSS в предыдущем примере сопоставляются с определенными свойствами WPD.



| Свойство WPD               |                         Значение                                           |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [\_Описание носителя \_ WPD](media-properties.md)                                                   | Логотип компании Lucerne                                        |
| [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md)                                          | https://www.lucernepublishing.com/community/podcasts |
| [\_Высота устройства \_ WPD](media-properties.md)                                                             | 300                                                 |
| [\_ \_ \_ URL-адрес источника мультимедиа WPD](media-properties.md)                                                    | https://www.lucernepublishing.com/images/logo.gif    |
| [\_Ширина носителя \_ WPD](media-properties.md)                                                               | 300                                                 |
| [\_имя объекта \_ WPD](object-properties.md)                                                              | Публикация в компании Lucerne                                  |
| [\_атрибут ресурса \_ WPD \_ может быть \_ удален](attributes.md)                               | ВАРИАНТ \_ true                                       |
| [\_атрибут ресурса \_ WPD \_ может \_ читать](attributes.md)                                   | ВАРИАНТ \_ true                                       |
| [\_ \_ Формат атрибута ресурса \_ WPD](resource-attribute-properties.md)                     | \_Формат объекта \_ WPD \_ GIF                            |
| [\_ \_ \_ Размер неоптимального \_ \_ буфера чтения \_ для атрибута ресурса WPD](attributes.md) | 1024                                                |
| [\_ \_ \_ Общий \_ Размер атрибута ресурса WPD](resource-attribute-properties.md)            | 512                                                 |



 

## <a name="mapping-rss-item-elements-to-wpd-property-values"></a>Сопоставление элементов RSS-элементов со значениями свойств WPD

В следующей таблице описано, как значения в элементах элементов RSS в предыдущем примере сопоставляются с определенными свойствами WPD.



| Свойство WPD  | Значение                   |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [\_заголовок носителя \_ WPD](media-properties.md)                                    | Цифровая публикация                                                                                                          |
| [\_длительность носителя \_ WPD](media-properties.md)                              | 10329011                                                                                                                         |
| [\_исполнитель мультимедиа \_ WPD](media-properties.md)                                  | Компания                                                                                                                          |
| [\_Описание носителя \_ WPD](media-properties.md)                        | Оперативные публикации быстро меняются. Исполнительный директор по публикации изучает тенденции за последние 5 лет и их последствия. |
| [\_ \_ \_ URL-адрес назначения мультимедиа WPD](media-properties.md)               | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_Жанр носителя \_ WPD](media-properties.md)                                    | Новости                                                                                                                             |
| [\_GUID носителя \_ WPD](media-properties.md)                                      | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ Дата выпуска носителя \_ WPD](media-properties.md)                     | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                   |
| [\_ \_ \_ URL-адрес источника мультимедиа WPD](media-properties.md)                         | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                |
| [\_ \_ обратные ссылки объекта WPD \_](object-properties.md)            | 0A1                                                                                                                              |
| [\_ \_ тип содержимого объекта \_ WPD](object-properties.md)                  | \_тип содержимого WPD — \_ \_ \_ изображение носителя                                                                                                 |
| [\_ \_ Дата создания объекта \_ WPD](object-properties.md)                | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                   |
| [\_ \_ Дата создания объекта \_ WPD](object-properties.md)                  | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                   |
| [\_ \_ Дата изменения объекта \_ WPD](object-properties.md)                | "Чт, 1 июня 2006 14:00:28, EDT                                                                                                   |
| [\_Формат объекта \_ WPD](object-properties.md)                               | \_Формат объекта \_ WPD \_ MP3                                                                                                         |
| [\_идентификатор объекта \_ WPD](object-properties.md)                                       | Зависит от сеанса. (Для этого примера предполагается "0A2".)                                                                              |
| [\_имя объекта \_ WPD](object-properties.md)                                   | Цифровая публикация                                                                                                          |
| [\_ \_ \_ имя ИСХОДНОГО файла \_ объекта WPD](object-properties.md)     | digital0601.mp3                                                                                                                  |
| [\_ \_ идентификатор родительского объекта \_ WPD](object-properties.md)                        | 0A0                                                                                                                              |
| [\_ \_ Постоянный \_ уникальный идентификатор объекта \_ WPD](object-properties.md) | Независимый от сеанса.                                                                                                             |
| [\_размер объекта \_ WPD](object-properties.md)                                   | 10329011                                                                                                                         |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Требования к объектам**](requirements-for-objects.md)
</dt> </dl>

 

 




