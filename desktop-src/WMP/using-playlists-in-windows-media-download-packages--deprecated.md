---
title: Использование списков воспроизведения в пакетах загрузки Windows Media (устарело)
description: Использование списков воспроизведения в пакетах загрузки Windows Media (устарело)
ms.assetid: c40efe24-aaed-47fc-8a8a-f412dfc36af7
keywords:
- Метафайлы Windows Media, пакеты загрузки Windows Media
- Проигрыватель Windows Media, пакеты загрузки Windows Media
- Метафайлы, пакеты загрузки Windows Media
- Windows Media, Загрузка пакетов Windows Media
- списки воспроизведения, пакеты загрузки Windows Media
- списки воспроизведения метафайлов, пакеты загрузки Windows Media
- Списки воспроизведения метафайлов Windows Media, пакеты загрузки Windows Media
- Пакеты загрузки Windows Media, списки воспроизведения
- Пакеты загрузки Windows Media, списки воспроизведения метафайлов
- Пакеты загрузки Windows Media, списки воспроизведения метафайлов Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 00c4daa26d18294c00aad7b4926a017d2f3f6343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411208"
---
# <a name="using-playlists-in-windows-media-download-packages-deprecated"></a>Использование списков воспроизведения в пакетах загрузки Windows Media (устарело)

Эта страница описывает функцию, которая может быть недоступна в будущих версиях проигрывателя Windows Media и Windows Media Player SDK.

Списки воспроизведения — это метафайлы Windows Media с расширением. ASX, содержащие сведения о том, как воспроизвести упакованное содержимое в проигрывателе Windows Media. Объединяя несколько файлов содержимого в один пакет загрузки Windows Media, вы можете управлять пакетом загрузки Windows Media и настраивать его с помощью списка воспроизведения.

> [!Note]  
> Как правило, списки воспроизведения метафайлов используются пакетами загрузки Windows Media для ссылки на мультимедийное содержимое в пакете, а не на поток с сервера в интрасети или Интернете. Однако поддерживаются ссылки на URL-адреса в файле ASX.

 

С помощью XML метафайл предоставляет сведения, которые проигрыватель Windows Media использует для воспроизведения и вывода содержимого. Списки воспроизведения состоят из различных элементов кода XML со связанными тегами и атрибутами. Каждый элемент в списке воспроизведения метафайлов Windows Media определяет конкретный параметр или действие в проигрывателе Windows Media.

Компьютер пользователя связывает метафайл Windows Media с расширением файла. ASX с проигрывателем Windows Media. Проигрыватель Windows Media открывает и анализирует XML-код в метафайле, который содержит путь для поиска упакованных аудио-или видеофайлов. Затем сценарий метафайлов управляет аудио, видео и графическим интерфейсом. Метафайл также содержит сведения, которые проигрыватель Windows Media обрабатывает и отображает в раскрывающемся списке Список воспроизведения. Сразу после отображения списка выполняется воспроизведение первого элемента в списке.

Список воспроизведения метафайлов — это ярлык файлов, содержащих упакованное содержимое. Следующий код является примером метафайла, который задает границу для вывода с помощью элемента **Skin** , двух песен для воспроизведения и сведений о списках воспроизведения для каждой песни.


```XML
<ASX Version="3.0">
<AUTHOR>Name of content creator goes here</AUTHOR>
<TITLE>Album Title goes here</TITLE>
<PARAM name="Album" value="Album Title "/>
<PARAM name="Artist" value="Artist Name"/>
<PARAM name="Genre" value="Genre"/>
<SKIN HREF="myborder.wmz"/>
    <ENTRY>
        <REF HREF="song1.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #1 title</TITLE>
    </ENTRY>
    <ENTRY>
        <REF HREF="song2.wma"/>
        <AUTHOR>Creator's name</AUTHOR>
        <COPYRIGHT>Copyright information</COPYRIGHT>
        <TITLE>Song #2 name</TITLE>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Границы для проигрывателя Windows Media (не рекомендуется)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Пакеты загрузки Windows Media (устарели)**](windows-media-download-packages--deprecated.md)
</dt> <dt>

[**Метафайлы Windows Media**](windows-media-metafiles.md)
</dt> </dl>

 

 




