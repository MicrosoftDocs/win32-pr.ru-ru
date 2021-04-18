---
title: Событие Дуратионунитчанже объекта Аксвиндовсмедиаплайер
description: Событие Дуратионунитчанже зарезервировано для будущего использования.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Событие Дуратионунитчанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f90aa052c61893d83683d10f482cd05841a49fab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694462"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="f48ea-104">Событие Дуратионунитчанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="f48ea-104">DurationUnitChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="f48ea-105">Событие Дуратионунитчанже зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="f48ea-105">The DurationUnitChange event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a><span data-ttu-id="f48ea-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="f48ea-106">Event Data</span></span>

<span data-ttu-id="f48ea-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ дуратионунитчанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="f48ea-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEventHandler**.</span></span> <span data-ttu-id="f48ea-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ дуратионунитчанжеевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="f48ea-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DurationUnitChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="f48ea-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="f48ea-109">Property</span></span>        | <span data-ttu-id="f48ea-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f48ea-110">Description</span></span>                               |
|-----------------|-------------------------------------------|
| <span data-ttu-id="f48ea-111">невдуратионунит</span><span class="sxs-lookup"><span data-stu-id="f48ea-111">newDurationUnit</span></span> | <span data-ttu-id="f48ea-112">**System. Int32** Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f48ea-112">**System.Int32** Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f48ea-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f48ea-113">Remarks</span></span>

<span data-ttu-id="f48ea-114">Это событие зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="f48ea-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="f48ea-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f48ea-115">Requirements</span></span>



| <span data-ttu-id="f48ea-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f48ea-116">Requirement</span></span> | <span data-ttu-id="f48ea-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f48ea-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48ea-118">Версия</span><span class="sxs-lookup"><span data-stu-id="f48ea-118">Version</span></span><br/>   | <span data-ttu-id="f48ea-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f48ea-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="f48ea-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f48ea-120">Namespace</span></span><br/> | <span data-ttu-id="f48ea-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="f48ea-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="f48ea-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="f48ea-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f48ea-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f48ea-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f48ea-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f48ea-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48ea-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f48ea-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





