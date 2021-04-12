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
# <a name="ui_pkey_themecolors"></a><span data-ttu-id="03fc5-103">UI \_ PKEY \_ семеколорс</span><span class="sxs-lookup"><span data-stu-id="03fc5-103">UI\_PKEY\_ThemeColors</span></span>

<span data-ttu-id="03fc5-104">Определяет свойство UI \_ PKEY \_ семеколорс.</span><span class="sxs-lookup"><span data-stu-id="03fc5-104">Identifies the UI\_PKEY\_ThemeColors property.</span></span>

```
propertyDescription
   name = UI_PKEY_ThemeColors
   shellPKey = UI_PKEY_ThemeColors
   formatID = 00000409-7363-696e-8441798acf5aebb7
   propID = 409
   typeInfo
      type = VT_VECTOR | VT_UI4
```

## <a name="remarks"></a><span data-ttu-id="03fc5-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03fc5-105">Remarks</span></span>

<span data-ttu-id="03fc5-106">UI \_ PKEY \_ семеколорс используется приложением для запроса значений цветовой палитры [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="03fc5-106">UI\_PKEY\_ThemeColors is used by an application to query the color swatch values of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="03fc5-107">Каждое значение [COLORREF](../gdi/colorref.md) соответствует образцу цвета в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** .</span><span class="sxs-lookup"><span data-stu-id="03fc5-107">Each [COLORREF](../gdi/colorref.md) value corresponds to a color swatch in a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute.</span></span>

<span data-ttu-id="03fc5-108">Значение свойства представляет собой массив значений [COLORREF](../gdi/colorref.md) .</span><span class="sxs-lookup"><span data-stu-id="03fc5-108">The property value is an array of [COLORREF](../gdi/colorref.md) values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03fc5-109">См. также</span><span class="sxs-lookup"><span data-stu-id="03fc5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03fc5-110">Свойства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="03fc5-110">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 