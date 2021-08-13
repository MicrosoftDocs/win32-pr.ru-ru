---
title: UI_PKEY_RecentItems
description: Определяет свойство UI \_ PKEY \_ рецентитемс.
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437960"
---
# <a name="ui_pkey_recentitems"></a>UI \_ PKEY \_ рецентитемс

Определяет свойство UI \_ PKEY \_ рецентитемс.

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Remarks

[Пользовательский интерфейс \_ \_Подкрепленный PKEY](windowsribbon-reference-properties-uipkey-pinned.md) используется приложением для запроса массива элементов в коллекции последних использованных элементов [меню приложения](windowsribbon-controls-applicationmenu.md). Сведения для каждого MRU-элемента инкапсулированы в объекте [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) и включают следующие три ключа свойств:

-   [\_Метка PKEY пользовательского интерфейса \_](windowsribbon-reference-properties-uipkey-label.md)
-   [UI \_ PKEY \_ лабелдескриптион](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [Пользовательский интерфейс \_ PKEY \_ закреплен](windowsribbon-reference-properties-uipkey-pinned.md)

Список MRU-элементов передается в ведущее приложение ленты в виде **массива SafeArray** [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) указателей на соответствующие реализации в ведущем приложении.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства состояния](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 