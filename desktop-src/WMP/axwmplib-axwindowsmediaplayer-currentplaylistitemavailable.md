---
title: Событие Куррентплайлиститемаваилабле объекта Аксвиндовсмедиаплайер
description: Событие Куррентплайлиститемаваилабле возникает, когда текущий список воспроизведения станет доступным. | Событие Куррентплайлиститемаваилабле объекта Аксвиндовсмедиаплайер
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Событие Куррентплайлиститемаваилабле в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694409"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9eff9-105">Событие Куррентплайлиститемаваилабле объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="9eff9-105">CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9eff9-106">Событие Куррентплайлиститемаваилабле возникает, когда текущий список воспроизведения станет доступным.</span><span class="sxs-lookup"><span data-stu-id="9eff9-106">The CurrentPlaylistItemAvailable event occurs when the current playlist becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="9eff9-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="9eff9-107">Event Data</span></span>

<span data-ttu-id="9eff9-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ куррентплайлиститемаваилабливенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="9eff9-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEventHandler**.</span></span> <span data-ttu-id="9eff9-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ куррентплайлиститемаваилабливент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="9eff9-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentPlaylistItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9eff9-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="9eff9-110">Property</span></span>         | <span data-ttu-id="9eff9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9eff9-111">Description</span></span>                                                    |
|------------------|----------------------------------------------------------------|
| <span data-ttu-id="9eff9-112">**бстритемнаме**</span><span class="sxs-lookup"><span data-stu-id="9eff9-112">**bstrItemName**</span></span> | <span data-ttu-id="9eff9-113">Имя System. Стрингсе текущего элемента списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9eff9-113">System.StringThe name of the current playlist item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9eff9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9eff9-114">Remarks</span></span>

<span data-ttu-id="9eff9-115">Имя текущего списка воспроизведения можно использовать для получения соответствующего интерфейса **ивмпплайлист** из интерфейса ивмпплайлистаррай, возвращаемого методом Ивмпплайлистколлектион. жетбинаме.</span><span class="sxs-lookup"><span data-stu-id="9eff9-115">The name of the current playlist can be used to retrieve the corresponding **IWMPPlaylist** interface from the IWMPPlaylistArray interface that is returned from the IWMPPlaylistCollection.getByName method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eff9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9eff9-116">Requirements</span></span>



| <span data-ttu-id="9eff9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9eff9-117">Requirement</span></span> | <span data-ttu-id="9eff9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9eff9-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eff9-119">Версия</span><span class="sxs-lookup"><span data-stu-id="9eff9-119">Version</span></span><br/>   | <span data-ttu-id="9eff9-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="9eff9-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9eff9-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9eff9-121">Namespace</span></span><br/> | <span data-ttu-id="9eff9-122">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="9eff9-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9eff9-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="9eff9-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9eff9-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9eff9-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9eff9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9eff9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eff9-126">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9eff9-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9eff9-127">**Интерфейс Ивмпплайлист (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9eff9-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9eff9-128">**Интерфейс Ивмпплайлистаррай (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9eff9-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9eff9-129">**Ивмпплайлистколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="9eff9-129">**IWMPPlaylistCollection.getByName (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





