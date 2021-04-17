---
title: Событие Плайлистколлектионплайлистсетасделетед объекта Аксвиндовсмедиаплайер
description: Событие Плайлистколлектионплайлистсетасделетед зарезервировано для будущего использования.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Событие Плайлистколлектионплайлистсетасделетед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf432ede40298abed98cdf0c5b02b0a192f7b3a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699078"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="14c54-104">Событие Плайлистколлектионплайлистсетасделетед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="14c54-104">PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="14c54-105">Событие Плайлистколлектионплайлистсетасделетед зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="14c54-105">The PlaylistCollectionPlaylistSetAsDeleted event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a><span data-ttu-id="14c54-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="14c54-106">Event Data</span></span>

<span data-ttu-id="14c54-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистсетасделетедевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="14c54-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEventHandler**.</span></span> <span data-ttu-id="14c54-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистсетасделетедевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="14c54-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistSetAsDeletedEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="14c54-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="14c54-109">Property</span></span>         | <span data-ttu-id="14c54-110">Описание</span><span class="sxs-lookup"><span data-stu-id="14c54-110">Description</span></span>                                 |
|------------------|---------------------------------------------|
| <span data-ttu-id="14c54-111">бстрплайлистнаме</span><span class="sxs-lookup"><span data-stu-id="14c54-111">bstrPlaylistName</span></span> | <span data-ttu-id="14c54-112">**System. String** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="14c54-112">**System.String** Not supported.</span></span><br/>  |
| <span data-ttu-id="14c54-113">варфисделетед</span><span class="sxs-lookup"><span data-stu-id="14c54-113">varfIsDeleted</span></span>    | <span data-ttu-id="14c54-114">**System. Boolean** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="14c54-114">**System.Boolean** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14c54-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14c54-115">Remarks</span></span>

<span data-ttu-id="14c54-116">Это событие зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="14c54-116">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="14c54-117">Требования</span><span class="sxs-lookup"><span data-stu-id="14c54-117">Requirements</span></span>



| <span data-ttu-id="14c54-118">Требование</span><span class="sxs-lookup"><span data-stu-id="14c54-118">Requirement</span></span> | <span data-ttu-id="14c54-119">Значение</span><span class="sxs-lookup"><span data-stu-id="14c54-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c54-120">Версия</span><span class="sxs-lookup"><span data-stu-id="14c54-120">Version</span></span><br/>   | <span data-ttu-id="14c54-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="14c54-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="14c54-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="14c54-122">Namespace</span></span><br/> | <span data-ttu-id="14c54-123">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="14c54-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="14c54-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="14c54-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="14c54-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="14c54-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c54-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14c54-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c54-127">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="14c54-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





