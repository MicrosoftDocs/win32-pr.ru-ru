---
title: UI_PKEY_StandardColors
description: Определяет свойство UI \_ PKEY \_ стандардколорс.
ms.assetid: fbdce7ba-4417-4f7f-928b-fba6af6eb396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc3c3b991e798406736e87d594d09be92d89512
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700875"
---
# <a name="ui_pkey_standardcolors"></a>UI \_ PKEY \_ стандардколорс

Определяет свойство UI \_ PKEY \_ стандардколорс.

```
propertyDescription
   name = UI_PKEY_StandardColors
   shellPKey = UI_PKEY_StandardColors
   formatID = 00000410-7363-696e-8441798acf5aebb7
   propID = 410
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ стандардколорс используется приложением для запроса значений цветовой палитры [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

Каждое значение [COLORREF](../gdi/colorref.md) соответствует цветовой палитре в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) независимо от значения, указанного для атрибута **колортемплате** .

Значение свойства представляет собой массив значений [COLORREF](../gdi/colorref.md) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 