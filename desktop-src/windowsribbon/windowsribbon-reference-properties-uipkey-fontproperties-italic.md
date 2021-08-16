---
title: UI_PKEY_FontProperties_Italic
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bb72e1ba43b29f5e3815fe42d0ace454ff0219a188a128b422e4a621af210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438539"
---
# <a name="ui_pkey_fontproperties_italic"></a>Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ курсивом

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Italic.

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ фонтпропертиес \_ Italic используется приложением для запроса состояния кнопки **курсив** .

Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|    Свойство.                      |       Результат пользовательского интерфейса                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Кнопка с **курсивом** отключена и может быть установлена только приложением. |
| `UI_FONTPROPERTIES_NOTSET`       | Кнопка с **курсивом** не выбрана.                                    |
| `UI_FONTPROPERTIES_SET`          | Выбрана **курсивная** кнопка.                                        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтпропертиес пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 