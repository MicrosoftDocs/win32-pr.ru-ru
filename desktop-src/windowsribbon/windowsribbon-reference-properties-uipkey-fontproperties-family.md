---
title: UI_PKEY_FontProperties_Family
description: Идентифицирует свойство UI \_ PKEY \_ фонтпропертиес \_ Family.
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0574ea4fb104cff29b58c8b1f649bd9287672acef677e3ea4cdc6ad5f91367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438663"
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

## <a name="remarks"></a>Remarks

\_Семейство UI PKEY \_ фонтпропертиес \_ используется приложением для запроса значения раскрывающейся коллекции **семейства шрифтов** .

значение \_ семейства фонтпропертиес UI PKEY \_ \_ соответствует имени [семейства шрифтов GDI Windows](../gdi/font-families.md) , полученного с помощью [функции EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) или [EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).

Значение по умолчанию — пустая строка.

Если в качестве значения для семейства фонтпропертиес UI PKEY указана пустая строка \_ \_ \_ , выделение шрифта снимается.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 