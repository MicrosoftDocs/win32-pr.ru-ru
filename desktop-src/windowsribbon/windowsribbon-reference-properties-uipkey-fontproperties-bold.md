---
title: UI_PKEY_FontProperties_Bold
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Bold.
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68800d3cfed72382f3576edfc01272c82b46c825
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444385"
---
# <a name="ui_pkey_fontproperties_bold"></a>Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Bold

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Bold.

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ фонтпропертиес \_ Bold используется приложением для запроса состояния кнопки **полужирный** .

Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|      Свойство                    |    Результат пользовательского интерфейса                                                        |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Кнопка **полужирного начертания** отключена и может быть установлена только приложением. |
| `UI_FONTPROPERTIES_NOTSET`       | Кнопка **полужирного шрифта** не выбрана.                                    |
| `UI_FONTPROPERTIES_SET`          | Выбрана **Полужирная** кнопка.                                        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтпропертиес пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 