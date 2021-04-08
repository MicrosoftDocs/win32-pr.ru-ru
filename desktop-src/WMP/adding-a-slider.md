---
title: Добавление ползунка
description: Добавление ползунка
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Создание обложек, ползунков
- Обложки проигрывателя Windows Media, ползунки
- обложки, ползунки
- Ползунки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068228"
---
# <a name="adding-a-slider"></a>Добавление ползунка

Можно добавить ползунок для отображения текущего положения носителя, а также разрешить пользователю изменять положение в текущем файле мультимедиа.

Сначала необходимо добавить элемент **Slider** :


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



Это задает максимальное значение в зависимости от продолжительности текущего файла мультимедиа. При этом используется миниатюрное растровое изображение с незначительным размером в 10 пикселей на 10 пикселов зеленого квадрата. Фон ползунка будет красным, а передний цвет будет синим. Когда пользователь перетаскивает изображение бегунка в новую точку и позволяет нажать кнопку мыши, носитель изменится на эту точку.

Но ползунок не будет перемещаться сам по себе, если только не измеряется текущая позиция с помощью атрибута **CurrentPosition \_ onChange** элемента **Controls** , который внедряется в элемент **Player** .


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



При изменении положения носителя вызывается событие, которое затем запускает строку кода, которая изменяет значение ползунка на текущее положение носителя.

Аналогичную обложку рабочего ползунка можно увидеть в разделе примеров пакета SDK.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Руководством по созданию обложки**](skin-creation-guide.md)
</dt> </dl>

 

 




