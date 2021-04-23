---
title: UI_PKEY_RecentItems
description: Определяет свойство UI \_ PKEY \_ рецентитемс.
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710307"
---
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="955fd-103">UI \_ PKEY \_ рецентитемс</span><span class="sxs-lookup"><span data-stu-id="955fd-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="955fd-104">Определяет свойство UI \_ PKEY \_ рецентитемс.</span><span class="sxs-lookup"><span data-stu-id="955fd-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="955fd-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="955fd-105">Remarks</span></span>

<span data-ttu-id="955fd-106">[Пользовательский интерфейс \_ \_Подкрепленный PKEY](windowsribbon-reference-properties-uipkey-pinned.md) используется приложением для запроса массива элементов в коллекции последних использованных элементов [меню приложения](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="955fd-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="955fd-107">Сведения для каждого MRU-элемента инкапсулированы в объекте [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) и включают следующие три ключа свойств:</span><span class="sxs-lookup"><span data-stu-id="955fd-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="955fd-108">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="955fd-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="955fd-109">UI \_ PKEY \_ лабелдескриптион</span><span class="sxs-lookup"><span data-stu-id="955fd-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="955fd-110">Пользовательский интерфейс \_ PKEY \_ закреплен</span><span class="sxs-lookup"><span data-stu-id="955fd-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="955fd-111">Список MRU-элементов передается в ведущее приложение ленты в виде **массива SafeArray** [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) указателей на соответствующие реализации в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="955fd-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="955fd-112">См. также</span><span class="sxs-lookup"><span data-stu-id="955fd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="955fd-113">Свойства состояния</span><span class="sxs-lookup"><span data-stu-id="955fd-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 