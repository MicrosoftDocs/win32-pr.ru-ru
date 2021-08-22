---
title: Использование пользовательских параметров и команд
description: Использование пользовательских параметров и команд
ms.assetid: 6b0bfd19-1672-41e3-9b7f-c8d541168c0e
keywords:
- Windows Списки воспроизведения мультимедийных метафайлов, пользовательские параметры
- списки воспроизведения, пользовательские параметры
- списки воспроизведения метафайлов, пользовательские параметры
- Windows Списки воспроизведения мультимедийных метафайлов, пользовательские команды
- списки воспроизведения, пользовательские команды
- списки воспроизведения метафайлов, пользовательские команды
- Windows Списки воспроизведения мультимедийных метафайлов, параметры
- списки воспроизведения, параметры
- списки воспроизведения метафайлов, параметры
- пользовательские параметры
- пользовательские команды
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6848131c58dabfa465a202bd39b061997e2a9bbda3e8004133f1ef1ce1d2d12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830940"
---
# <a name="using-custom-parameters-and-commands"></a>Использование пользовательских параметров и команд

Можно создать пользовательские параметры для передачи дополнительных метаданных в список воспроизведения метафайлов с помощью элемента **param** . Используйте атрибут **Name** элемента **param** , чтобы определить имя настраиваемого параметра. Используйте атрибут **value** , чтобы определить значение для именованного настраиваемого параметра.

Получите метаданные **param** с помощью методов **getItemInfo** объектов **мультимедиа** и **списков воспроизведения** . Пример использования этих методов для получения метаданных см. в описании метода [аттрибутекаунт](playlist-attributecount.md) объекта **списка воспроизведения** .

В следующем примере списка воспроизведения метафайла показано использование элемента **param** для определения пользовательских параметров.


```XML
<ASX version="3.0" BANNERBAR="auto" >
    <TITLE>Example Media Player Show</TITLE>
    <PARAM NAME="Director" VALUE="Jane D." />

    <ENTRY>
        <TITLE>Example Clip</TITLE>
        <REF HREF="https://www.proseware.com/media.wma" />
        <PARAM NAME="Title" VALUE="Example Clip" />
        <PARAM NAME="Location" VALUE="North America" />
        <PARAM NAME="Release Date" VALUE="March 1998" />
    </ENTRY>

    <ENTRY>
        <TITLE>Another Clip</TITLE>
        <REF HREF="https://www.proseware.com/more_media.wma" />
        <PARAM NAME="Title" VALUE="Another Clip" />
        <PARAM NAME="Location" VALUE="Japan" />
        <PARAM NAME="Release Date" VALUE="December 2000" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Использование списков воспроизведения метафайлов**](using-metafile-playlists.md)
</dt> </dl>

 

 




