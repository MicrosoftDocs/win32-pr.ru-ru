---
title: Событие Плайлистколлектионплайлистаддед объекта Аксвиндовсмедиаплайер
description: Событие Плайлистколлектионплайлистаддед возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения. | Событие Плайлистколлектионплайлистаддед объекта Аксвиндовсмедиаплайер
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Событие Плайлистколлектионплайлистаддед в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b019e58ae8955f6df894101956e4776c2cd71626
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699082"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="43cba-105">Событие Плайлистколлектионплайлистаддед объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="43cba-105">PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="43cba-106">Событие Плайлистколлектионплайлистаддед возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="43cba-106">The PlaylistCollectionPlaylistAdded event occurs when a playlist is added to the playlist collection.</span></span>

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a><span data-ttu-id="43cba-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="43cba-107">Event Data</span></span>

<span data-ttu-id="43cba-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистаддедевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="43cba-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEventHandler**.</span></span> <span data-ttu-id="43cba-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ плайлистколлектионплайлистаддедевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="43cba-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlaylistCollectionPlaylistAddedEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="43cba-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="43cba-110">Property</span></span>             | <span data-ttu-id="43cba-111">Описание</span><span class="sxs-lookup"><span data-stu-id="43cba-111">Description</span></span>                                                                |
|----------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="43cba-112">**бстрплайлистнаме**</span><span class="sxs-lookup"><span data-stu-id="43cba-112">**bstrPlaylistName**</span></span> | <span data-ttu-id="43cba-113">System. СтрингспеЦифиес. имя добавленного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="43cba-113">System.StringSpecifies the name of the playlist that was added.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="43cba-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43cba-114">Remarks</span></span>

<span data-ttu-id="43cba-115">Имя добавленного списка воспроизведения можно использовать для получения соответствующего списка воспроизведения с помощью Ивмпплайлистколлектион. метод **жетбинаме** .</span><span class="sxs-lookup"><span data-stu-id="43cba-115">The name of the playlist that was added can be used to retrieve the corresponding playlist by using the IWMPPlaylistCollection.**getByName** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="43cba-116">Требования</span><span class="sxs-lookup"><span data-stu-id="43cba-116">Requirements</span></span>



| <span data-ttu-id="43cba-117">Требование</span><span class="sxs-lookup"><span data-stu-id="43cba-117">Requirement</span></span> | <span data-ttu-id="43cba-118">Значение</span><span class="sxs-lookup"><span data-stu-id="43cba-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cba-119">Версия</span><span class="sxs-lookup"><span data-stu-id="43cba-119">Version</span></span><br/>   | <span data-ttu-id="43cba-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="43cba-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="43cba-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43cba-121">Namespace</span></span><br/> | <span data-ttu-id="43cba-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="43cba-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="43cba-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="43cba-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="43cba-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="43cba-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43cba-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43cba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cba-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="43cba-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="43cba-127">**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="43cba-127">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





