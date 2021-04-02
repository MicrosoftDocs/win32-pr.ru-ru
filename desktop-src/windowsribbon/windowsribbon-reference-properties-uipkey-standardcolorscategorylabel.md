---
title: UI_PKEY_StandardColorsCategoryLabel
description: Определяет свойство UI \_ PKEY \_ стандардколорскатегорилабел.
ms.assetid: 59452d4b-acc9-4a5f-a06c-a67b0e676a57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcaecc19213ab82ebafaa76dc2e88a0db836a97a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777561"
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

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ стандардколорскатегорилабел используется приложением для запроса значения метки, связанной со стандартной категорией **цветов** [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

UI \_ PKEY \_ стандардколорскатегорилабел допустим только для [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) , где `ThemeColors` указывается как значение атрибута **колортемплате** (это единственный шаблон, содержащий помеченные категории).

На следующем снимке экрана показан `ThemeColors`  [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

![снимок экрана элемента дропдовнколорпиккер с атрибутом колортемплате, для которого задано значение семеколорс.](images/markup/colortemplate.themedcolors.1.png)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




