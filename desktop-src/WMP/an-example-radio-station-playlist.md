---
title: Пример списка воспроизведения для радиостанции
description: Пример списка воспроизведения для радиостанции
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, примеры списков воспроизведения
- списки воспроизведения метафайлов, примеры списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, примеры списков воспроизведения
- списки воспроизведения, образцы списков воспроизведения
- списки воспроизведения метафайлов, образцы списков воспроизведения
- Списки воспроизведения метафайлов Windows Media, пример кода
- списки воспроизведения, пример кода
- списки воспроизведения метафайлов, пример кода
- Список воспроизведения метафайлов Windows Media, пример списка воспроизведения радиостанции
- списки воспроизведения, пример списка воспроизведения радиостанции
- списки воспроизведения метафайлов, пример списка воспроизведения радиостанции
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, примеры списков воспроизведения
- Проигрыватель Windows Media, образцы списков воспроизведения
- Проигрыватель Windows Media, пример списка воспроизведения радиостанции
- примеры списков воспроизведения
- примеры списков воспроизведения
- Образцы списков воспроизведения
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410828"
---
# <a name="an-example-radio-station-playlist"></a>Пример списка воспроизведения для радиостанции

В следующем примере кода показано, как создать список воспроизведения для сканирования трех радиостанций-переключателей. Вымышленная фирма Adventure Works Radio Марка находится в списке воспроизведения и всех отдельных потоках в списке воспроизведения. При написании кода измените все URL-адреса и имена файлов на допустимые имена файлов, доступные проигрывателю Windows Media.

Для каждой станции создается список воспроизведения. Четвертый список воспроизведения просматривает первые три. Списки воспроизведения создаются для ссылки на динамически создаваемые объявления и имеют фирменную символику Adventure Works Radio.

Один из списков воспроизведения, представляющих радиостанции, может выглядеть следующим образом.


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



Затем список воспроизведения может быть создан в виде ссылок на отдельные списки воспроизведения.

Пример кода


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



В этом примере воспроизводится рекламное объявление, за которым следует 30 секунд каждой из трех станций, на которые имеется ссылка, один за другим. Этот цикл будет повторяться в течение неограниченного времени, так как атрибут **Count** элемента **Repeat** не определен.

-   Названия организаций, предприятий и изделий, а также имена и события, используемые в качестве примеров, являются вымышленными. Возможное сходство с реально существующими организациями, предприятиями, изделиями, лицами и событиями следует рассматривать как случайное.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание списков воспроизведения метафайлов**](creating-metafile-playlists.md)
</dt> <dt>

[**Примеры списков воспроизведения**](example-playlists.md)
</dt> <dt>

[**Списки воспроизведения метафайлов**](metafile-playlists.md)
</dt> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Путеводитель по метафайлу Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




