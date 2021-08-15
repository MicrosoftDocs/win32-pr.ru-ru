---
title: UI_PKEY_RecentColorsCategoryLabel
description: Определяет свойство UI \_ PKEY \_ рецентколорскатегорилабел.
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f3a7a513afb50f01ee3a03c3a3240a2eae7a6ed7b6b8228c4a49e7343e052e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118031482"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a>UI \_ PKEY \_ рецентколорскатегорилабел

Определяет свойство UI \_ PKEY \_ рецентколорскатегорилабел.

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ рецентколорскатегорилабел используется приложением для запроса значения метки, связанной с категорией " **Последние цвета** " [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

UI \_ PKEY \_ рецентколорскатегорилабел допустим только для [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** (это единственный шаблон, содержащий помеченные категории).

На следующем снимке экрана показан `ThemeColors` [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

![снимок экрана элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение семеколорс.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




