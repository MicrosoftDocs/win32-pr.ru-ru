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

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ рецентколорскатегорилабел используется приложением для запроса значения метки, связанной с категорией " **Последние цвета** " [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

UI \_ PKEY \_ рецентколорскатегорилабел допустим только для [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** (это единственный шаблон, содержащий помеченные категории).

На следующем снимке экрана показан `ThemeColors`  [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

![снимок экрана элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение семеколорс.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




