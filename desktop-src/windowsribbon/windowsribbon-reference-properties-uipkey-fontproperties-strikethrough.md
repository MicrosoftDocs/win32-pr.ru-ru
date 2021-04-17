---
title: UI_PKEY_FontProperties_Strikethrough
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Зачеркнутый.
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b07804a74671bb219b34b1c67580af083fd5c34c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413498"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Зачеркнутый

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ Зачеркнутый.

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ Зачеркнутый используется приложением для запроса состояния кнопки **перечеркивания** .

Значение свойства находится в перечислении [**\_ Фонтпропертиес пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

Значение по умолчанию — `UI_FONTPROPERTIES_NOTSET`.

На следующем снимке экрана показана кнопка **зачеркивания** ленты [**фонтконтрол**](windowsribbon-element-fontcontrol.md).

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/markup/fontcontrol-strikethrough.png)

В следующей таблице описаны свойства и результат пользовательского интерфейса.



|                                  |                                                                              |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Кнопка **перечеркивания** отключена и может быть задана только приложением. |
| `UI_FONTPROPERTIES_NOTSET`       | Кнопка **перечеркивания** не выбрана.                                    |
| `UI_FONTPROPERTIES_SET`          | Кнопка **перечеркивания** выбрана.                                        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**фонтпропертиес пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 