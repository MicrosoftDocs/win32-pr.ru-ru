---
title: Полный код для простой обложки
description: Полный код для простой обложки
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Создание обложек, примеры кода
- обложки проигрыватель Windows Media, примеры кода
- обложки, примеры кода
- файлы определения обложки, примеры кода
- Создание обложек, примеры
- обложки проигрыватель Windows Media, примеры
- обложки, примеры
- файлы определения обложки, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b4d4380c6d7fb44290e8faff26bf5cb84dae552d09fe13594402dbe434ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135797"
---
# <a name="complete-code-for-simple-skin"></a>Полный код для простой обложки

Ниже приведен полный код для первого примера обложки:


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



Теперь все части объединены.

Создайте сжатый файл с расширением имени файла .zip. Этот сжатый файл содержит файл определения обложки, растровые изображения и любые цифровые файлы мультимедиа, которые необходимо включить. Переименуйте файл, чтобы он был иметь расширение WMZ. Затем дважды щелкните сжатую обложку, чтобы начать играть.

Аналогичные работающие простые обложки можно увидеть в разделе Samples пакета SDK.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Создание файла определения обложки**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




