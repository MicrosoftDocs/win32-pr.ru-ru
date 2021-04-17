---
title: Буферизация события объекта Аксвиндовсмедиаплайер
description: Событие буферизации возникает, когда элемент управления проигрывателя Windows Media начинает или заканчивается буферизацией или загружается. | Буферизация события объекта Аксвиндовсмедиаплайер
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Буферизация события объекта Аксвиндовсмедиаплайер проигрывателя Windows Media
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694392"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="97ccc-105">Буферизация события объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="97ccc-105">Buffering Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="97ccc-106">Событие буферизации возникает, когда элемент управления проигрывателя Windows Media начинает или заканчивается буферизацией или загружается.</span><span class="sxs-lookup"><span data-stu-id="97ccc-106">The Buffering event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a><span data-ttu-id="97ccc-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="97ccc-107">Event Data</span></span>

<span data-ttu-id="97ccc-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ буфферинжевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="97ccc-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_BufferingEventHandler**.</span></span> <span data-ttu-id="97ccc-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ буфферинжевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="97ccc-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_BufferingEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="97ccc-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="97ccc-110">Property</span></span> | <span data-ttu-id="97ccc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="97ccc-111">Description</span></span>                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ccc-112">Запуск</span><span class="sxs-lookup"><span data-stu-id="97ccc-112">Start</span></span>    | <span data-ttu-id="97ccc-113">System. БулеанспеЦифиес, начало или окончание буферизации.</span><span class="sxs-lookup"><span data-stu-id="97ccc-113">System.BooleanSpecifies whether buffering has begun or ended.</span></span> <span data-ttu-id="97ccc-114">Значение true указывает, что оно началось; значение false указывает, что оно завершено.</span><span class="sxs-lookup"><span data-stu-id="97ccc-114">A value of true indicates that it has begun; a value of false indicates that it has ended.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="97ccc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97ccc-115">Remarks</span></span>

<span data-ttu-id="97ccc-116">Это событие используется для определения времени, в течение которого буферизация или загрузка начинается или останавливается.</span><span class="sxs-lookup"><span data-stu-id="97ccc-116">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="97ccc-117">Один и тот же блок событий можно использовать в обоих случаях и в Test *ивмпнетворк*. **буфферингпрогресс** и *ивмпнетворк*. **довнлоадпрогресс** , чтобы определить, является ли проигрыватель Windows Media в данный момент буферизацией или загрузкой содержимого.</span><span class="sxs-lookup"><span data-stu-id="97ccc-117">You can use the same event block for both cases and test *IWMPNetwork*.**bufferingProgress** and *IWMPNetwork*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ccc-118">Требования</span><span class="sxs-lookup"><span data-stu-id="97ccc-118">Requirements</span></span>



| <span data-ttu-id="97ccc-119">Требование</span><span class="sxs-lookup"><span data-stu-id="97ccc-119">Requirement</span></span> | <span data-ttu-id="97ccc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="97ccc-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ccc-121">Версия</span><span class="sxs-lookup"><span data-stu-id="97ccc-121">Version</span></span><br/>   | <span data-ttu-id="97ccc-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="97ccc-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="97ccc-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97ccc-123">Namespace</span></span><br/> | <span data-ttu-id="97ccc-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="97ccc-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="97ccc-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="97ccc-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="97ccc-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="97ccc-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97ccc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97ccc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ccc-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="97ccc-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="97ccc-129">**Ивмпнетворк. Буфферингпрогресс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="97ccc-129">**IWMPNetwork.bufferingProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="97ccc-130">**Ивмпнетворк. Довнлоадпрогресс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="97ccc-130">**IWMPNetwork.downloadProgress (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





