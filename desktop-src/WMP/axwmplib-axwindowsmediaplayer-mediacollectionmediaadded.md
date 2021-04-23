---
title: Событие Медиаколлектионмедиааддед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионмедиааддед возникает при добавлении элемента мультимедиа в локальную библиотеку. | Событие Медиаколлектионмедиааддед объекта Аксвиндовсмедиаплайер
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Событие Медиаколлектионмедиааддед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb839fccf9a5048b5647480eca36fcfcaeb904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699011"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="b8d22-105">Событие Медиаколлектионмедиааддед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="b8d22-105">MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="b8d22-106">Событие Медиаколлектионмедиааддед возникает при добавлении элемента мультимедиа в локальную библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b8d22-106">The MediaCollectionMediaAdded event occurs when a media item is added to the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a><span data-ttu-id="b8d22-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="b8d22-107">Event Data</span></span>

<span data-ttu-id="b8d22-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиааддедевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="b8d22-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEventHandler**.</span></span> <span data-ttu-id="b8d22-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиааддедевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="b8d22-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="b8d22-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="b8d22-110">Property</span></span> | <span data-ttu-id="b8d22-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b8d22-111">Description</span></span>                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d22-112">пмедиа</span><span class="sxs-lookup"><span data-stu-id="b8d22-112">pMedia</span></span>   | <span data-ttu-id="b8d22-113">Элемент мультимедиа System. Обжектсе добавлен в локальную библиотеку.</span><span class="sxs-lookup"><span data-stu-id="b8d22-113">System.ObjectThe media item added to the local library.</span></span> <span data-ttu-id="b8d22-114">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="b8d22-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8d22-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8d22-115">Remarks</span></span>

<span data-ttu-id="b8d22-116">Это событие возникает только для локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="b8d22-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d22-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b8d22-117">Requirements</span></span>



| <span data-ttu-id="b8d22-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b8d22-118">Requirement</span></span> | <span data-ttu-id="b8d22-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b8d22-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d22-120">Версия</span><span class="sxs-lookup"><span data-stu-id="b8d22-120">Version</span></span><br/>   | <span data-ttu-id="b8d22-121">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="b8d22-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="b8d22-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b8d22-122">Namespace</span></span><br/> | <span data-ttu-id="b8d22-123">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="b8d22-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="b8d22-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="b8d22-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8d22-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b8d22-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8d22-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b8d22-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8d22-127">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b8d22-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8d22-128">**Аксвиндовсмедиаплайер. Медиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b8d22-128">**AxWindowsMediaPlayer.mediaCollection (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8d22-129">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b8d22-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8d22-130">**Интерфейс Ивмпмедиаколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b8d22-130">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





