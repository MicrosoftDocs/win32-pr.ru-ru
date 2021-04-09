---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг.
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b67e2a099b7ce02b3c94f7c9d799fcdda5e881
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070472"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг.

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг используется приложением для запроса значения элементов управления " **надстрочный** " и " **индекс** ".

Значение свойства находится в перечислении [**\_ Фонтвертикалпоситион пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .

Значение по умолчанию — `UI_FONTVERTICALPOSITION_NOTSET`.

На следующем снимке экрана показаны кнопки **надстрочных** и **подстрочных индексов** на ленте [**фонтконтрол**](windowsribbon-element-fontcontrol.md).

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-subsuper.png)

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|                                        |                                                                                                |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | **Верхние** и нижние **индексы** отключены и могут быть установлены только приложением. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | Кнопки **надстрочных** и **подстрочных индексов** не выбраны.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | Выбрана кнопка **надстрочных знаков** .                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | Выбрана кнопка **подстрочных индексов** .                                                              |



 

> [!Note]  
> Невозможно одновременно выбрать **надстрочные** и **подстрочные** кнопки.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтвертикалпоситион пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 