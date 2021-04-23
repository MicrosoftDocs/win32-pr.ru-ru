---
title: Событие EndOfStream объекта Аксвиндовсмедиаплайер
description: Событие EndOfStream зарезервировано для будущего использования.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Событие EndOfStream в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694457"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="3d1c1-104">Событие EndOfStream объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="3d1c1-104">EndOfStream Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="3d1c1-105">Событие EndOfStream зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="3d1c1-105">The EndOfStream event is reserved for future use.</span></span>

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a><span data-ttu-id="3d1c1-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="3d1c1-106">Event Data</span></span>

<span data-ttu-id="3d1c1-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ ендофстреамевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="3d1c1-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEventHandler**.</span></span> <span data-ttu-id="3d1c1-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ ендофстреамевент**, который содержит следующее свойство, связанное с этим событием.</span><span class="sxs-lookup"><span data-stu-id="3d1c1-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_EndOfStreamEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="3d1c1-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="3d1c1-109">Property</span></span> | <span data-ttu-id="3d1c1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3d1c1-110">Description</span></span>                           |
|----------|---------------------------------------|
| <span data-ttu-id="3d1c1-111">result</span><span class="sxs-lookup"><span data-stu-id="3d1c1-111">result</span></span>   | <span data-ttu-id="3d1c1-112">System. Int32Not поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3d1c1-112">System.Int32Not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d1c1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d1c1-113">Remarks</span></span>

<span data-ttu-id="3d1c1-114">Это событие зарезервировано для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="3d1c1-114">This event is reserved for future use.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1c1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3d1c1-115">Requirements</span></span>



| <span data-ttu-id="3d1c1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3d1c1-116">Requirement</span></span> | <span data-ttu-id="3d1c1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3d1c1-117">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1c1-118">Версия</span><span class="sxs-lookup"><span data-stu-id="3d1c1-118">Version</span></span><br/>   | <span data-ttu-id="3d1c1-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3d1c1-119">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="3d1c1-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3d1c1-120">Namespace</span></span><br/> | <span data-ttu-id="3d1c1-121">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="3d1c1-121">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="3d1c1-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="3d1c1-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3d1c1-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3d1c1-123"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d1c1-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d1c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1c1-125">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3d1c1-125">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





