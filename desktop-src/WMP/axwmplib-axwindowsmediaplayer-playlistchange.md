---
title: Событие Плайлистчанже объекта Аксвиндовсмедиаплайер
description: Событие Плайлистчанже возникает при изменении списка воспроизведения. | Событие Плайлистчанже объекта Аксвиндовсмедиаплайер
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Событие Плайлистчанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9989b303d8e9077c158fd844c93431100205d9f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699085"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d1c5a-105">Событие Плайлистчанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="d1c5a-105">PlaylistChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d1c5a-106">Событие Плайлистчанже возникает при изменении списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d1c5a-106">The PlaylistChange event occurs when a playlist changes.</span></span>

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a><span data-ttu-id="d1c5a-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="d1c5a-107">Event Data</span></span>

<span data-ttu-id="d1c5a-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистчанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="d1c5a-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEventHandler**.</span></span> <span data-ttu-id="d1c5a-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистчанжеевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="d1c5a-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="d1c5a-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="d1c5a-110">Property</span></span>     | <span data-ttu-id="d1c5a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d1c5a-111">Description</span></span>                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c5a-112">**список воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="d1c5a-112">**playlist**</span></span> | <span data-ttu-id="d1c5a-113">Измененный объект System. Обжектсе.</span><span class="sxs-lookup"><span data-stu-id="d1c5a-113">System.ObjectThe object which changed.</span></span> <span data-ttu-id="d1c5a-114">Это можно привести к интерфейсу Ивмпплайлист для доступа к нему.</span><span class="sxs-lookup"><span data-stu-id="d1c5a-114">You can cast this to an IWMPPlaylist interface to access it.</span></span><br/>                |
| <span data-ttu-id="d1c5a-115">**change**</span><span class="sxs-lookup"><span data-stu-id="d1c5a-115">**change**</span></span>   | <span data-ttu-id="d1c5a-116">Значение перечисления Вмплиб. Вмпплайлистчанжеевенттипеан, указывающее тип изменения, произошедшего в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d1c5a-116">WMPLib.WMPPlaylistChangeEventTypeAn enumeration value indicating the type of change that occurred to the playlist.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1c5a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d1c5a-117">Requirements</span></span>



| <span data-ttu-id="d1c5a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d1c5a-118">Requirement</span></span> | <span data-ttu-id="d1c5a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d1c5a-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c5a-120">Версия</span><span class="sxs-lookup"><span data-stu-id="d1c5a-120">Version</span></span><br/>   | <span data-ttu-id="d1c5a-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d1c5a-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d1c5a-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1c5a-122">Namespace</span></span><br/> | <span data-ttu-id="d1c5a-123">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="d1c5a-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d1c5a-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="d1c5a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d1c5a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d1c5a-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1c5a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1c5a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c5a-127">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d1c5a-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d1c5a-128">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d1c5a-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





