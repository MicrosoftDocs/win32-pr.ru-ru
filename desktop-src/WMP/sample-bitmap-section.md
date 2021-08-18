---
title: Пример раздела точечного рисунка
description: Пример раздела точечного рисунка
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- проигрыватель Windows Media Обложки для мобильных устройств, точечные рисунки
- обложки, точечные рисунки
- Справочник по обложкам, точечным рисункам
- точечные рисунки в обложках, раздел точечных рисунков
- файлы определения обложки, раздел растровых изображений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de401906896abcdda4728ff0984871ef4a399d3e223b36afd9d585eb0e4fce76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833398"
---
# <a name="sample-bitmap-section"></a>Пример раздела точечного рисунка

В следующих строках показан типичный раздел точечных рисунков в файле определения обложки:


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



Он определяет пять растровых изображений, которые используются для создания фонового изображения, изображения для отключенных и отправленных кнопок, изображение региона для кнопок области и супер-изображение для значений TrackBar.

> [!Note]  
> в обложках для проигрыватель Windows Media 10 Mobile или более поздней версии не рекомендуется использовать область и супер bitmap.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Растровые изображения**](bitmaps.md)
</dt> </dl>

 

 




