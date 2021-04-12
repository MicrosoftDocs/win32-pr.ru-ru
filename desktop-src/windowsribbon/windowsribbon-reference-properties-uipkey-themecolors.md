---
title: UI_PKEY_ThemeColors
description: Определяет свойство UI \_ PKEY \_ семеколорс.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5991ce5058de5a6f49ca8929de02e19657a610
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337772"
---
# <a name="ui_pkey_themecolors"></a>UI \_ PKEY \_ семеколорс

Определяет свойство UI \_ PKEY \_ семеколорс.

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ семеколорс используется приложением для запроса значений цветовой палитры [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

Каждое значение [COLORREF](../gdi/colorref.md) соответствует образцу цвета в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** .

Значение свойства представляет собой массив значений [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 