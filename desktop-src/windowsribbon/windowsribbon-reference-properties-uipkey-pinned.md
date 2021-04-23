---
title: UI_PKEY_Pinned
description: Идентифицирует \_ \_ закрепленное свойство UI PKEY.
ms.assetid: 906b2ab9-1ed7-46a6-88bc-e8f9160ab60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8637f11404090313751647058ee41acbad3d9bf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258723"
---
# <a name="ui_pkey_pinned"></a><span data-ttu-id="9949f-103">Пользовательский интерфейс \_ PKEY \_ закреплен</span><span class="sxs-lookup"><span data-stu-id="9949f-103">UI\_PKEY\_Pinned</span></span>

<span data-ttu-id="9949f-104">Идентифицирует \_ \_ закрепленное свойство UI PKEY.</span><span class="sxs-lookup"><span data-stu-id="9949f-104">Identifies the UI\_PKEY\_Pinned property.</span></span>

```
propertyDescription
   name = UI_PKEY_Pinned
   shellPKey = UI_PKEY_Pinned
   formatID = 00000351-7363-696e-8441798acf5aebb7
   propID = 351
   typeInfo
      type = VT_BOOL
   booleanFormat
      formatAs = VARIANT_TRUE=-1, VARIANT_FALSE=0
```

## <a name="remarks"></a><span data-ttu-id="9949f-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9949f-105">Remarks</span></span>

<span data-ttu-id="9949f-106">\_ \_ Закрепленный пользовательский интерфейс (PKEY) используется приложением для запроса, является ли элемент в [меню "приложение](windowsribbon-controls-applicationmenu.md) " закрепленным или постоянным, между экземплярами приложения.</span><span class="sxs-lookup"><span data-stu-id="9949f-106">UI\_PKEY\_Pinned is used by an application to query whether an item in the [Application Menu](windowsribbon-controls-applicationmenu.md) is "pinned", or persistent, across application instances.</span></span> <span data-ttu-id="9949f-107">Например, элемент в списке недавно использовавшихся элементов доступен и не удаляет список MRU-элементов, пока не будет снят закрепление.</span><span class="sxs-lookup"><span data-stu-id="9949f-107">For example, an item in the most recently used (MRU) items list is accessible and does not drop off the MRU items list until it is "unpinned".</span></span>

## <a name="related-topics"></a><span data-ttu-id="9949f-108">См. также</span><span class="sxs-lookup"><span data-stu-id="9949f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9949f-109">Свойства состояния</span><span class="sxs-lookup"><span data-stu-id="9949f-109">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> <dt>

[<span data-ttu-id="9949f-110">UI \_ PKEY \_ рецентитемс</span><span class="sxs-lookup"><span data-stu-id="9949f-110">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md)
</dt> <dt>

[<span data-ttu-id="9949f-111">Недавние элементы</span><span class="sxs-lookup"><span data-stu-id="9949f-111">Recent Items</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 




