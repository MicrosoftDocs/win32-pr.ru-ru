---
title: TEXT. Value
description: Атрибут value указывает или получает текст, отображаемый в элементе управления "текст".
ms.assetid: dbc50be2-ee18-4661-a343-9e906879aba0
keywords:
- ТЕКСТОВЫЙ. Value — проигрыватель Windows Media
topic_type:
- apiref
api_name:
- TEXT.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d87f688f7afffeb588a37ac13ebff4cdc7cc105
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648679"
---
# <a name="textvalue"></a>TEXT. Value

Атрибут **value** указывает или получает текст, отображаемый в элементе управления "текст".

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Возможные значения

Этот атрибут является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Если ширина текстового элемента управления недостаточно для того, чтобы вместить указанный текст, текст обрезается, а для демонстрации факта отображается многоточие. Если атрибут **ToolTip** не задан, то полный текст будет отображаться в виде подсказки при наведении курсора мыши на элемент управления.

Если ширина не указана, по умолчанию ширина элемента управления равна ширине строки.

Если высота элемента управления не задана, высота по умолчанию — одна строка.

Если атрибут **WordWrap** имеет значение true и высота элемента достаточно велика для размещения другой строки текста, текст переносится на следующую строку. Заключение происходит только между словами. Разрывы строк также могут быть принудительно применены, как описано в разделе **WordWrap**.

## <a name="examples"></a>Примеры

Следующий пример представляет собой полный файл определения обложки, иллюстрирующий использование атрибутов **текстового** элемента. Его можно найти в каталоге Samples, который был установлен вместе с пакетом SDK.


```C++
<THEME>
  <VIEW
    height = "175"
  >
    <TEXT 
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Play"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.play"
      onClick = "JScript: player.URL='https://proseware.com/laure.wma';"
    />
    <TEXT
      top = "50"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      disabledForegroundColor = "#CCCCCC"
      justification = "Center"
      value = "Stop"
      cursor = "hand"
      enabled = "wmpenabled:player.controls.stop"
      onClick = "JScript: player.controls.stop();"
    />
    <TEXT
      top = "100"
      width = "150"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "Close"
      cursor = "hand"
      onClick = "JScript: view.close();"
    />
    <TEXT
      top = "30"
      left = "120"
      width = "200"
      fontSize = "20"
      fontStyle = "Underline"
      justification = "Center"
      value = "Volume"
    />
    <TEXT
      top = "60"
      left = "120"
      width = "200"
      fontSize = "40"
      justification = "Center"
      value = "wmpprop:player.settings.volume"
    />
    <TEXT
      top = "65"
      left = "142"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "-"
      cursor = "hand"
      toolTip = "decrease volume"
      onClick = "player.settings.volume = player.settings.volume - 5"
    />
    <TEXT
      top = "65"
      left = "260"
      width = "40"
      fontSize = "30"
      hoverFontStyle = "Bold"
      hoverForegroundColor = "red"
      justification = "Center"
      value = "+"
      cursor = "hand"
      toolTip = "increase volume"
      onClick = "player.settings.volume = player.settings.volume + 5"
    />
    <TEXT
      top = "155"
      width = "300"
      height = "30"
      fontFace = "System"
      backgroundColor = "blue"
      foregroundColor = "white"
      justification = "Center"
      scrolling = "true"
      scrollingAmount = "1"
      scrollingDelay = "50"
      value = "wmpprop:player.status"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**TEXT, элемент**](text-element.md)
</dt> <dt>

[**TEXT. toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT. wordWrap**](text-wordwrap.md)
</dt> </dl>

 

 





