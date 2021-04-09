---
title: Полный код для простой обложки
description: Полный код для простой обложки
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- Создание обложек, примеры кода
- Обложки проигрывателя Windows Media, примеры кода
- обложки, примеры кода
- файлы определения обложки, примеры кода
- Создание обложек, примеры
- Обложки проигрывателя Windows Media, примеры
- обложки, примеры
- файлы определения обложки, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888679"
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

Создайте сжатый файл с расширением ZIP. Этот сжатый файл содержит файл определения обложки, растровые изображения и любые цифровые файлы мультимедиа, которые необходимо включить. Переименуйте файл, чтобы он был иметь расширение WMZ. Затем дважды щелкните сжатую обложку, чтобы начать играть.

Аналогичные работающие простые обложки можно увидеть в разделе Samples пакета SDK.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Создание файла определения обложки**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




