---
title: Добавление визуализаций
description: Добавление визуализаций
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Создание обложек, визуализаций
- Обложки проигрывателя Windows Media, визуализации
- обложки, визуализации
- визуализации, обложки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9750b114d99af8c59777ea28ff4dab85a56dd229
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776322"
---
# <a name="adding-visualizations"></a>Добавление визуализаций

Окно визуализации можно добавить так же, как вы добавили видеоокно. Можно использовать одну и ту же обложку, однако используется элемент **Effects** .

Сначала необходимо добавить элемент **Effects** и присвоить ему идентификатор и размер:


```C++
       <EFFECTS
            id = "myeffects"
            top = "25"
            left = "88"
            width = "180"
            height = "150"/>

```



Затем можно назначить две кнопки в следующей строке кода визуализации:


```C++
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Next"
            onClick = "JScript:myeffects.next(); " />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Previous"
            onClick = "JScript:myeffects.previous(); " />

```



Слои и точечные рисунки были такими же, как в примере с видео, за исключением того, что стрелка воспроизведения была скопирована и отражена по горизонтали.

Наконец, был добавлен простой элемент **игрока** с атрибутом **URL** , чтобы выбрать композицию для воспроизведения.


```C++
      <PLAYER
          URL = "https://proseware.com/mellow.wma">
      </PLAYER>

```



Похожая Рабочая оболочка визуализации отображается в разделе примера пакета SDK.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Руководством по созданию обложки**](skin-creation-guide.md)
</dt> </dl>

 

 




