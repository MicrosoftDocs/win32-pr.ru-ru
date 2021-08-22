---
title: Добавление визуализаций
description: Добавление визуализаций
ms.assetid: adb5d10b-070c-426c-a74a-8d4881d9acbf
keywords:
- Создание обложек, визуализаций
- обложки проигрыватель Windows Media, визуализации
- обложки, визуализации
- визуализации, обложки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d236990d3e29cf4e51dbb46e8e1269b0c8a50ccaf205940a6f34b97c89fa6e62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619154"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Руководством по созданию обложки**](skin-creation-guide.md)
</dt> </dl>

 

 




