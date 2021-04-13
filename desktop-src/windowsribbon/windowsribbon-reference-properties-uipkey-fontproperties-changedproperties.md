---
title: UI_PKEY_FontProperties_ChangedProperties
description: Определяет свойство UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413414"
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

## <a name="remarks"></a>Комментарии

UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес используется приложением для запроса только измененных свойств из [UI \_ PKEY \_ фонтпропертиес](windowsribbon-reference-properties-uipkey-fontproperties.md).

Вызов метода [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) для этого объекта [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) возвращает [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore).

UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес передается как последний параметр вызова [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) в ведущее приложение ленты.

Этот ключ свойства доступен только для чтения.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 