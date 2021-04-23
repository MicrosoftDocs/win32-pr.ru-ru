---
title: Событие Стрингколлектиончанже объекта Аксвиндовсмедиаплайер
description: Событие Стрингколлектиончанже возникает при изменении коллекции строк. | Событие Стрингколлектиончанже объекта Аксвиндовсмедиаплайер
ms.assetid: 21b66882-bff9-4482-b56c-32c9df0bc02f
keywords:
- Событие Стрингколлектиончанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- StringCollectionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5182352f7f18727a1c11e9a0ef49e8141000d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694408"
---
# <a name="stringcollectionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="78fd1-105">Событие Стрингколлектиончанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="78fd1-105">StringCollectionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="78fd1-106">Событие Стрингколлектиончанже возникает при изменении коллекции строк.</span><span class="sxs-lookup"><span data-stu-id="78fd1-106">The StringCollectionChange event occurs when a string collection changes.</span></span>

``` syntax
[C#]
private void player_StringCollectionChange(
  object sender,
  _WMPOCXEvents_StringCollectionChangeEvent e
)

[Visual Basic]
Private Sub player_StringCollectionChange(
  sender As Object,
  e As _WMPOCXEvents_StringCollectionChangeEvent
) Handles player.StringCollectionChange
```

## <a name="event-data"></a><span data-ttu-id="78fd1-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="78fd1-107">Event Data</span></span>

<span data-ttu-id="78fd1-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ стрингколлектиончанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="78fd1-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEventHandler**.</span></span> <span data-ttu-id="78fd1-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ стрингколлектиончанжеевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="78fd1-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_StringCollectionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="78fd1-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="78fd1-110">Property</span></span>              | <span data-ttu-id="78fd1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="78fd1-111">Description</span></span>                                                                                                                           |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fd1-112">пдиспстрингколлектион</span><span class="sxs-lookup"><span data-stu-id="78fd1-112">pdispStringCollection</span></span> | <span data-ttu-id="78fd1-113">Измененный элемент коллекции строк System. Обжектсе.</span><span class="sxs-lookup"><span data-stu-id="78fd1-113">System.ObjectThe string collection item that changed.</span></span> <span data-ttu-id="78fd1-114">Это можно привести к интерфейсу Ивмпстрингколлектион для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="78fd1-114">You can cast this to an IWMPStringCollection interface to access it.</span></span><br/> |
| <span data-ttu-id="78fd1-115">лколлектиониндекс</span><span class="sxs-lookup"><span data-stu-id="78fd1-115">lCollectionIndex</span></span>      | <span data-ttu-id="78fd1-116">Индекс System. Int32The элемента коллекции строк, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="78fd1-116">System.Int32The index of the string collection item that changed.</span></span><br/>                                                          |
| <span data-ttu-id="78fd1-117">Изменить</span><span class="sxs-lookup"><span data-stu-id="78fd1-117">change</span></span>                | <span data-ttu-id="78fd1-118">Значение перечисления Вмплиб. Вмпстрингколлектиончанжеевенттипеан, указывающее тип произошедшего изменения.</span><span class="sxs-lookup"><span data-stu-id="78fd1-118">WMPLib.WMPStringCollectionChangeEventTypeAn enumeration value indicating the type of change that occurred.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="78fd1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="78fd1-119">Requirements</span></span>



| <span data-ttu-id="78fd1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="78fd1-120">Requirement</span></span> | <span data-ttu-id="78fd1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="78fd1-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78fd1-122">Версия</span><span class="sxs-lookup"><span data-stu-id="78fd1-122">Version</span></span><br/>   | <span data-ttu-id="78fd1-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="78fd1-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="78fd1-124">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78fd1-124">Namespace</span></span><br/> | <span data-ttu-id="78fd1-125">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="78fd1-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="78fd1-126">Сборка</span><span class="sxs-lookup"><span data-stu-id="78fd1-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="78fd1-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="78fd1-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78fd1-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78fd1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78fd1-129">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="78fd1-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="78fd1-130">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="78fd1-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="78fd1-131">**вмпстрингколлектиончанжеевенттипе**</span><span class="sxs-lookup"><span data-stu-id="78fd1-131">**WMPStringCollectionChangeEventType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpstringcollectionchangeeventtype)
</dt> </dl>

 

 





