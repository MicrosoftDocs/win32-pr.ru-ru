---
title: Событие Маркерхит объекта Аксвиндовсмедиаплайер
description: Событие Маркерхит возникает при достижении маркера. | Событие Маркерхит объекта Аксвиндовсмедиаплайер
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Событие Маркерхит в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699022"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="efed6-105">Событие Маркерхит объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="efed6-105">MarkerHit Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="efed6-106">Событие Маркерхит возникает при достижении маркера.</span><span class="sxs-lookup"><span data-stu-id="efed6-106">The MarkerHit event occurs when a marker is reached.</span></span>

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a><span data-ttu-id="efed6-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="efed6-107">Event Data</span></span>

<span data-ttu-id="efed6-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ маркерхитевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="efed6-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEventHandler**.</span></span> <span data-ttu-id="efed6-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ маркерхитевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="efed6-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MarkerHitEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="efed6-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="efed6-110">Property</span></span>      | <span data-ttu-id="efed6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="efed6-111">Description</span></span>                                                             |
|---------------|-------------------------------------------------------------------------|
| <span data-ttu-id="efed6-112">**маркернум**</span><span class="sxs-lookup"><span data-stu-id="efed6-112">**MarkerNum**</span></span> | <span data-ttu-id="efed6-113">System. Int32Indicates — номер маркера, который был достигнут.</span><span class="sxs-lookup"><span data-stu-id="efed6-113">System.Int32Indicates the number of the marker that was hit.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="efed6-114">Требования</span><span class="sxs-lookup"><span data-stu-id="efed6-114">Requirements</span></span>



| <span data-ttu-id="efed6-115">Требование</span><span class="sxs-lookup"><span data-stu-id="efed6-115">Requirement</span></span> | <span data-ttu-id="efed6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="efed6-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efed6-117">Версия</span><span class="sxs-lookup"><span data-stu-id="efed6-117">Version</span></span><br/>   | <span data-ttu-id="efed6-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="efed6-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="efed6-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="efed6-119">Namespace</span></span><br/> | <span data-ttu-id="efed6-120">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="efed6-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="efed6-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="efed6-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="efed6-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="efed6-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efed6-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efed6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efed6-124">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="efed6-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





