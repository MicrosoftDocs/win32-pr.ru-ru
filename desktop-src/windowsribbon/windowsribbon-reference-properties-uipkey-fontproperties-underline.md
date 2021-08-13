---
title: UI_PKEY_FontProperties_Underline
description: Определяет \_ \_ \_ свойство подчеркивания UI PKEY фонтпропертиес.
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75142e08549c2084ebcd37e82943ed63fdfb5b278faef01c4ad79441fa36915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706728"
---
# <a name="ui_pkey_fontproperties_underline"></a>Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_

Определяет \_ \_ \_ свойство подчеркивания UI PKEY фонтпропертиес.

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Remarks

Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_ используется приложением для запроса состояния кнопки **подчеркивания** .

Значение свойства находится в перечислении [**\_ Фонтундерлине пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .

Значение по умолчанию — `UI_FONTUNDERLINE_NOTSET`.

На следующем снимке экрана показана кнопка **подчеркивания** ленты [**фонтконтрол**](windowsribbon-element-fontcontrol.md).

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-underline.png)

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|      Свойство                   |       Результат пользовательского интерфейса                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | Кнопка **подчеркивания** отключена и может быть задана только приложением. |
| `UI_FONTUNDERLINE_NOTSET`       | Кнопка **подчеркивания** не выбрана.                                    |
| `UI_FONTUNDERLINE_SET`          | Кнопка **подчеркивания** выбрана.                                        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтундерлине пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 