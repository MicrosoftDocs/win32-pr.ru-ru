---
title: Добавление ползунка
description: Добавление ползунка
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Создание обложек, ползунков
- обложки проигрыватель Windows Media, ползунки
- обложки, ползунки
- Ползунки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c3644e1b243188664295bbc00101a74377cbef17632217ff0a81dac0d377a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004384"
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

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Руководством по созданию обложки**](skin-creation-guide.md)
</dt> </dl>

 

 




