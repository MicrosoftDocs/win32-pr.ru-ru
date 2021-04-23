---
title: Событие Медиаколлектионмедиаремовед объекта Аксвиндовсмедиаплайер
description: Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки. | Событие Медиаколлектионмедиаремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Событие Медиаколлектионмедиаремовед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699010"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d4958-105">Событие Медиаколлектионмедиаремовед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="d4958-105">MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d4958-106">Событие Медиаколлектионмедиаремовед возникает при удалении элемента мультимедиа из локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d4958-106">The MediaCollectionMediaRemoved event occurs when a media item is removed from the local library.</span></span>

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a><span data-ttu-id="d4958-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="d4958-107">Event Data</span></span>

<span data-ttu-id="d4958-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиаремоведевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="d4958-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEventHandler**.</span></span> <span data-ttu-id="d4958-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ медиаколлектионмедиаремоведевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="d4958-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaCollectionMediaRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="d4958-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="d4958-110">Property</span></span> | <span data-ttu-id="d4958-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d4958-111">Description</span></span>                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4958-112">пмедиа</span><span class="sxs-lookup"><span data-stu-id="d4958-112">pMedia</span></span>   | <span data-ttu-id="d4958-113">Элемент мультимедиа System. Обжектсе удален из локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d4958-113">System.ObjectThe media item removed from the local library.</span></span> <span data-ttu-id="d4958-114">Это можно привести к интерфейсу Ивмпмедиа для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="d4958-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4958-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d4958-115">Remarks</span></span>

<span data-ttu-id="d4958-116">Это событие возникает только для локальной библиотеки.</span><span class="sxs-lookup"><span data-stu-id="d4958-116">This event occurs only for the local library.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4958-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d4958-117">Requirements</span></span>



| <span data-ttu-id="d4958-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d4958-118">Requirement</span></span> | <span data-ttu-id="d4958-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d4958-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4958-120">Версия</span><span class="sxs-lookup"><span data-stu-id="d4958-120">Version</span></span><br/>   | <span data-ttu-id="d4958-121">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="d4958-121">Windows Media Player 11</span></span><br/>                                                                                         |
| <span data-ttu-id="d4958-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d4958-122">Namespace</span></span><br/> | <span data-ttu-id="d4958-123">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="d4958-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d4958-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="d4958-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d4958-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d4958-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4958-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d4958-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4958-127">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d4958-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d4958-128">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d4958-128">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





