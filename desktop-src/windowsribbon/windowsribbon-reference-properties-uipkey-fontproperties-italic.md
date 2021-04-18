---
title: UI_PKEY_FontProperties_Italic
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413103"
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

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ Italic используется приложением для запроса состояния кнопки **курсив** .

Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Кнопка с **курсивом** отключена и может быть установлена только приложением. |
| `UI_FONTPROPERTIES_NOTSET`       | Кнопка с **курсивом** не выбрана.                                    |
| `UI_FONTPROPERTIES_SET`          | Выбрана **курсивная** кнопка.                                        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтпропертиес пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 