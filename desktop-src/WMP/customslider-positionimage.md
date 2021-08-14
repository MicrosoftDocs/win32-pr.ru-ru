---
title: КУСТОМСЛИДЕР. Поситионимаже
description: Атрибут Поситионимаже указывает или получает карту изображения, используемую для определения того, какое изображение должно быть отображено из файла изображения.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- кустомслидер. поситионимаже проигрыватель Windows Media
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727601ceb7ed078e40a284ab291f2e182a4270682b5f1db104515e31d3dbe2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749999"
---
# <a name="customsliderpositionimage"></a>КУСТОМСЛИДЕР. Поситионимаже

Атрибут **поситионимаже** указывает или получает карту изображения, используемую для определения того, какое изображение должно быть отображено из файла изображения.

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.

## <a name="remarks"></a>Remarks

Этот атрибут является обязательным и должен быть указан.

**Поситионимаже** не отображается. Вместо этого он выступает в качестве схемы, определяющей щелчки отображаемых областей изображения. Отображаемое изображение является одним из подизображений файла изображения и представляет фактическое состояние ползунка. **Поситионимаже** содержит несколько серых регионов масштабирования, равных количеству этих подобразов. Подизображения должны иметь те же размеры, что и **поситионимаже** , или пользовательский ползунок будет работать неправильно.

Любой регион, не являющийся серой шкалой, не будет щелкать. Для областей, используемых для щелчков, должно быть задано цветовое значение, которое равномерно распределяется между черным спектром в оттенках серого, а первый регион — чистым черным, а последний регион — чистым белым. Значения цвета каждой последующей области должны увеличиваться на величину, равную 255, деленную на общее число регионов минус единица, округление до ближайшего целого числа.

Например, если имеется шесть регионов, то приращение будет 51 (255, деленное на 5), а шесть значений оттенков серого — 0, 51, 102, 153, 204 и 255. Затем шестнадцатеричные значения цвета для шести регионов будут \# 000000, \# 333333, \# 666666, \# 999999, \# кккккк и \# FFFFFF.

Таким образом, регионы будут иметь последовательность, определяемую значениями цвета серого масштаба, и эта последовательность будет соответствовать последовательности подизображений в файле изображения. При щелчке по одному из регионов отображается соответствующее подизображение, а **значение** настраиваемого ползунка соответствующим образом обновляется.

Поддерживаются следующие типы файлов изображений: BMP, JPG, PNG и GIF (не включая анимированные GIF).

## <a name="examples"></a>Примеры

Ниже приведен пример настраиваемого ползунка **поситионимаже**. Соответствующее изображение показано в разделе "пример" свойства **Image** .

![Образец графика поситионимаже](images/dialmap.png)

В следующем коде показано использование атрибутов **кустомслидер** .


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

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
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**КУСТОМСЛИДЕР, элемент**](customslider-element.md)
</dt> <dt>

[**КУСТОМСЛИДЕР. Image**](customslider-image.md)
</dt> </dl>

 

 





