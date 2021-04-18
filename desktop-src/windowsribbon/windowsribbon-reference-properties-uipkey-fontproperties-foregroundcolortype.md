---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе.
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5589e9b21fc7ab0884a3cac51eba114ee77036b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413219"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе.

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе используется приложением в сочетании с [UI \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md)для запроса параметров коллекции **цветов текста** .

Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

Значение по умолчанию — `UI_SWATCHCOLORTYPE_RGB`.

В следующей таблице описаны значения свойств.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Не поддерживается [**фонтконтрол**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Приложение должно запрашивать соответствующую метрику системы для значения цвета, как правило, текущего **цвета текста** темы Windows, получаемого с помощью ЖЕТСИСКОЛОР (цветная \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | Приложение должно запрашивать [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) для значения цвета. Значение цвета [UI \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) отображается на кнопке **Цвет текста** и выбирается в коллекции **цветов текста** .<br/> |



 

UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе передается методу обратного вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цвета в коллекции **цветов текста** [**фонтконтрол**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> Настоятельно рекомендуется, чтобы приложение задали только исходное значение **цвета текста** и не задали его повторно при перемещении курсора в пределах документа. Последний выбор должен поддерживаться, чтобы избежать необходимости повторно выбирать нужный цвет.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**сватчколортипе пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

