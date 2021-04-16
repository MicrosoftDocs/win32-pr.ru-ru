---
title: UI_PKEY_FontProperties_Family
description: Идентифицирует свойство UI \_ PKEY \_ фонтпропертиес \_ Family.
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7183e51105a397f14154639512ca11f7c03d44
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710293"
---
# <a name="ui_pkey_fontproperties_family"></a>\_Семейство UI PKEY \_ фонтпропертиес \_

Идентифицирует свойство UI \_ PKEY \_ фонтпропертиес \_ Family.

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Комментарии

\_Семейство UI PKEY \_ фонтпропертиес \_ используется приложением для запроса значения раскрывающейся коллекции **семейства шрифтов** .

Значение \_ семейства ФОНТПРОПЕРТИЕС UI PKEY \_ \_ соответствует имени [семейства шрифтов Windows GDI](../gdi/font-families.md) , полученному с помощью [функции EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) или [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).

Значение по умолчанию - пустая строка.

Если в качестве значения для семейства фонтпропертиес UI PKEY указана пустая строка \_ \_ \_ , выделение шрифта снимается.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 