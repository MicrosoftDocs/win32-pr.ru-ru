---
title: UI_PKEY_FontProperties_ChangedProperties
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36262a9acf217e448956f108b68cb0716b5b5080c71f6a2a8e305c9e59478c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028662"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес

Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес.

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Remarks

UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес используется приложением для запроса только измененных свойств из [UI \_ PKEY \_ фонтпропертиес](windowsribbon-reference-properties-uipkey-fontproperties.md).

Вызов метода [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) для этого объекта [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) возвращает [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore).

UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес передается как последний параметр вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) в ведущее приложение ленты.

Этот ключ свойства доступен только для чтения.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 