---
title: UI_PKEY_ThemeColors
description: Определяет свойство UI \_ PKEY \_ семеколорс.
ms.assetid: d539cbaa-45dc-4f9e-830e-e81fb289b4ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5c4582561e3c86ba19b2821cf600d0a1da614cfc9fc7144b935665c8af7f14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437799"
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

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ семеколорс используется приложением для запроса значений цветовой палитры [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

Каждое значение [COLORREF](../gdi/colorref.md) соответствует образцу цвета в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** .

Значение свойства представляет собой массив значений [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 