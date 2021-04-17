---
title: Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер
description: Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения. | Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Событие Плайлистколлектионплайлистремовед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699080"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7c010-105">Событие Плайлистколлектионплайлистремовед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="7c010-105">PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7c010-106">Событие Плайлистколлектионплайлистремовед возникает при удалении списка воспроизведения из коллекции списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7c010-106">The PlaylistCollectionPlaylistRemoved event occurs when a playlist is removed from the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a><span data-ttu-id="7c010-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="7c010-107">Event Data</span></span>

<span data-ttu-id="7c010-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистремоведевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="7c010-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEventHandler**.</span></span> <span data-ttu-id="7c010-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистремоведевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="7c010-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistRemovedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7c010-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="7c010-110">Property</span></span>             | <span data-ttu-id="7c010-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7c010-111">Description</span></span>                                                                  |
|----------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="7c010-112">**бстрплайлистнаме**</span><span class="sxs-lookup"><span data-stu-id="7c010-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="7c010-113">System. СтрингспеЦифиес имя списка воспроизведения, который был удален.</span><span class="sxs-lookup"><span data-stu-id="7c010-113">System.StringSpecifies the name of the playlist that was removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c010-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7c010-114">Requirements</span></span>



| <span data-ttu-id="7c010-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7c010-115">Requirement</span></span> | <span data-ttu-id="7c010-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7c010-116">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c010-117">Версия</span><span class="sxs-lookup"><span data-stu-id="7c010-117">Version</span></span><br/>   | <span data-ttu-id="7c010-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="7c010-118">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7c010-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c010-119">Namespace</span></span><br/> | <span data-ttu-id="7c010-120">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="7c010-120">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7c010-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="7c010-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7c010-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7c010-122"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c010-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c010-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c010-124">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7c010-124">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7c010-125">**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="7c010-125">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





