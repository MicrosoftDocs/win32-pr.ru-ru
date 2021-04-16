---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе.
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568898cb2706eb932ea708f929aa4791f0643c74
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487796"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе.

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе используется приложением в сочетании с [UI \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor)для запроса параметров коллекции **цветов выделения текста** .

Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

Значение по умолчанию — `UI_SWATCHCOLORTYPE_RGB`.

В следующей таблице описаны значения свойств.



|                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Приложение должно запрашивать соответствующую метрику системы для значения цвета, как правило, текущего **цвета фона окна** темы Windows, получаемого с помощью жетсисколор ( \_ окно цвета).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Не поддерживается [**фонтконтрол**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | Приложение должно запрашивать [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) для значения цвета. Значение цвета [UI \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) отображается на кнопке **Цвет выделения текста** и выбрано в коллекции **цветов выделения текста** .<br/> |



 

UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе передается методу обратного вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цвета в коллекции **цветов подсветки текста** [**фонтконтрол**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> Настоятельно рекомендуется, чтобы приложение задали только исходное значение **цвета выделения текста** и не задали его повторно при перемещении курсора в пределах документа. Последний выбор должен поддерживаться, чтобы избежать необходимости повторно выбирать нужный цвет.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**сватчколортипе пользовательского интерфейса \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

