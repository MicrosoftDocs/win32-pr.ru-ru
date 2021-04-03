---
title: UI_PKEY_RecentColorsCategoryLabel
description: Определяет свойство UI \_ PKEY \_ рецентколорскатегорилабел.
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777567"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a><span data-ttu-id="02667-103">UI \_ PKEY \_ рецентколорскатегорилабел</span><span class="sxs-lookup"><span data-stu-id="02667-103">UI\_PKEY\_RecentColorsCategoryLabel</span></span>

<span data-ttu-id="02667-104">Определяет свойство UI \_ PKEY \_ рецентколорскатегорилабел.</span><span class="sxs-lookup"><span data-stu-id="02667-104">Identifies the UI\_PKEY\_RecentColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="02667-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02667-105">Remarks</span></span>

<span data-ttu-id="02667-106">UI \_ PKEY \_ рецентколорскатегорилабел используется приложением для запроса значения метки, связанной с категорией " **Последние цвета** " [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="02667-106">UI\_PKEY\_RecentColorsCategoryLabel is used by an application to query the value of the label associated with the **Recent Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="02667-107">UI \_ PKEY \_ рецентколорскатегорилабел допустим только для [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** (это единственный шаблон, содержащий помеченные категории).</span><span class="sxs-lookup"><span data-stu-id="02667-107">UI\_PKEY\_RecentColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="02667-108">На следующем снимке экрана показан `ThemeColors`  [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="02667-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![снимок экрана элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение семеколорс.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a><span data-ttu-id="02667-110">См. также</span><span class="sxs-lookup"><span data-stu-id="02667-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02667-111">Свойства выбора цвета</span><span class="sxs-lookup"><span data-stu-id="02667-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




