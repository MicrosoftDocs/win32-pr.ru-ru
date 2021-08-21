---
title: UI_PKEY_StandardColorsCategoryLabel
description: Определяет свойство UI \_ PKEY \_ стандардколорскатегорилабел.
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4301fe8874ef4eb3fae0ad931114a7ed305cbc4893ad12c58cf182babe8a16c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437931"
---
# <a name="ui_pkey_standardcolorscategorylabel"></a>UI \_ PKEY \_ стандардколорскатегорилабел

Определяет свойство UI \_ PKEY \_ стандардколорскатегорилабел.

```
propertyDescription
   name = UI_PKEY_StandardColorsCategoryLabel
   shellPKey = UI_PKEY_StandardColorsCategoryLabel
   formatID = 00000404-7363-696e-8441798acf5aebb7
   propID = 404
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ стандардколорскатегорилабел используется приложением для запроса значения метки, связанной со стандартной категорией **цветов** [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

UI \_ PKEY \_ стандардколорскатегорилабел допустим только для [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** (это единственный шаблон, содержащий помеченные категории).

На следующем снимке экрана показан `ThemeColors` [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

![снимок экрана элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение семеколорс.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




