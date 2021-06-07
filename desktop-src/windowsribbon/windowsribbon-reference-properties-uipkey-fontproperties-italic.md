---
title: UI_PKEY_FontProperties_Italic
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Italic.
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443815"
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

Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|    Свойство                      |       Результат пользовательского интерфейса                                                       |
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

 

 