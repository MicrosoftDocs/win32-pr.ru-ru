---
title: Событие Куррентмедиаитемаваилабле объекта Аксвиндовсмедиаплайер
description: Событие Куррентмедиаитемаваилабле возникает при доступности элемента метаданных изображения в текущем элементе мультимедиа. | Событие Куррентмедиаитемаваилабле объекта Аксвиндовсмедиаплайер
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Событие Куррентмедиаитемаваилабле в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699030"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="cf2ac-105">Событие Куррентмедиаитемаваилабле объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="cf2ac-105">CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="cf2ac-106">Событие Куррентмедиаитемаваилабле возникает при доступности элемента метаданных изображения в текущем элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-106">The CurrentMediaItemAvailable event occurs when a graphic metadata item in the current media item becomes available.</span></span>

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a><span data-ttu-id="cf2ac-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="cf2ac-107">Event Data</span></span>

<span data-ttu-id="cf2ac-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ куррентмедиаитемаваилабливенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEventHandler**.</span></span> <span data-ttu-id="cf2ac-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ куррентмедиаитемаваилабливент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentMediaItemAvailableEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="cf2ac-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="cf2ac-110">Property</span></span>     | <span data-ttu-id="cf2ac-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cf2ac-111">Description</span></span>                                                 |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="cf2ac-112">бстритемнаме</span><span class="sxs-lookup"><span data-stu-id="cf2ac-112">bstrItemName</span></span> | <span data-ttu-id="cf2ac-113">Имя System. Стрингсе текущего элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-113">System.StringThe name of the current media item.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf2ac-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf2ac-114">Remarks</span></span>

<span data-ttu-id="cf2ac-115">Так как воспроизведение может начаться до полной загрузки элемента мультимедиа, все метаданные, содержащиеся в элементе мультимедиа (например, обложку альбома), могут быть недоступны при начале воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-115">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="cf2ac-116">Это событие предупреждает о завершении загрузки графического элемента метаданных.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-116">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="cf2ac-117">Затем можно получить интерфейс **ивмпмедиа** , передав значение **бстритемнаме** в *ивмпмедиаколлектион*. метод **жетбинаме** , после которого можно получить доступ к графическому элементу метаданных с помощью *IWMPMedia3*. **жетитеминфобитипе** и укажите **WM/Picture** в качестве имени атрибута.</span><span class="sxs-lookup"><span data-stu-id="cf2ac-117">You can then retrieve the **IWMPMedia** interface by passing the value of **bstrItemName** to the *IWMPMediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *IWMPMedia3*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf2ac-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cf2ac-118">Requirements</span></span>



| <span data-ttu-id="cf2ac-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cf2ac-119">Requirement</span></span> | <span data-ttu-id="cf2ac-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cf2ac-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf2ac-121">Версия</span><span class="sxs-lookup"><span data-stu-id="cf2ac-121">Version</span></span><br/>   | <span data-ttu-id="cf2ac-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="cf2ac-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="cf2ac-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf2ac-123">Namespace</span></span><br/> | <span data-ttu-id="cf2ac-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="cf2ac-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="cf2ac-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="cf2ac-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cf2ac-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cf2ac-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf2ac-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf2ac-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf2ac-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cf2ac-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf2ac-129">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cf2ac-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf2ac-130">**IWMPMedia3. Жетитеминфобитипе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cf2ac-130">**IWMPMedia3.getItemInfoByType (VB and C#)**</span></span>](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cf2ac-131">**Ивмпмедиаколлектион. Жетбинаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cf2ac-131">**IWMPMediaCollection.getByName (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





