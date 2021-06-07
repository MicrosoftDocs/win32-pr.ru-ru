---
title: UI_PKEY_ColorType
description: Определяет свойство UI \_ PKEY \_ колортипе.
ms.assetid: 7eaa9d8b-0c21-487c-9093-79ddffcae131
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9240d8c816adcf2674efcc2e7428d22b765f542
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443895"
---
# <a name="ui_pkey_colortype"></a>UI \_ PKEY \_ колортипе

Определяет свойство UI \_ PKEY \_ колортипе.

```
propertyDescription
   name = UI_PKEY_ColorType
   shellPKey = UI_PKEY_ColorType
   formatID = 00000401-7363-696e-8441798acf5aebb7
   propID = 401
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ колортипе используется приложением для запроса параметра Color элемента управления [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .

Значение свойства находится в перечислении [**\_ Сватчколортипе пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .



|    Свойство                            |    Описание                                                                                                                                                                             |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UI \_ СВАТЧКОЛОРТИПЕ \_ Color   | Приложение должно рассматривать параметр цвета как прозрачный. Обычно используется в сочетании с параметром **нет** цветового цвета.                                                   |
| Пользовательский интерфейс \_ сватчколортипе \_ автоматически | Приложение должно запрашивать [жетсисколор (цветная \_ WINDOWTEXT)](/windows/win32/api/winuser/nf-winuser-getsyscolor). Обычно используется в сочетании с параметром **автоматического** цвета. |
| сватчколортипе пользовательского интерфейса \_ \_ RGB       | Приложение должно запрашивать [ \_ \_ цвет пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-color.md) для параметра цвета.                                                          |



 

UI \_ PKEY \_ колортипе передается методу обратного вызова [**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выборе цветовой палитры в [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства выбора цвета](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 