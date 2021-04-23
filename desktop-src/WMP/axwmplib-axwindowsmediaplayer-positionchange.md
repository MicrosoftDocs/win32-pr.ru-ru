---
title: Событие Поситиончанже объекта Аксвиндовсмедиаплайер
description: Событие Поситиончанже возникает при изменении текущей позиции воспроизведения в элементе мультимедиа.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Событие Поситиончанже в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694800"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="61eec-104">Событие Поситиончанже объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="61eec-104">PositionChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="61eec-105">Событие Поситиончанже возникает при изменении текущей позиции воспроизведения в элементе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="61eec-105">The PositionChange event occurs when the current playback position within the media item has been changed.</span></span>

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a><span data-ttu-id="61eec-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="61eec-106">Event Data</span></span>

<span data-ttu-id="61eec-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ поситиончанжеевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="61eec-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEventHandler**.</span></span> <span data-ttu-id="61eec-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ поситиончанжеевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="61eec-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PositionChangeEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="61eec-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="61eec-109">Property</span></span>    | <span data-ttu-id="61eec-110">Описание</span><span class="sxs-lookup"><span data-stu-id="61eec-110">Description</span></span>                                         |
|-------------|-----------------------------------------------------|
| <span data-ttu-id="61eec-111">олдпоситион</span><span class="sxs-lookup"><span data-stu-id="61eec-111">oldPosition</span></span> | <span data-ttu-id="61eec-112">Старое расположение System. ДаублеспеЦифиес.</span><span class="sxs-lookup"><span data-stu-id="61eec-112">System.DoubleSpecifies the old position.</span></span><br/> |
| <span data-ttu-id="61eec-113">невпоситион</span><span class="sxs-lookup"><span data-stu-id="61eec-113">newPosition</span></span> | <span data-ttu-id="61eec-114">System. ДаублеспеЦифиес новое расположение.</span><span class="sxs-lookup"><span data-stu-id="61eec-114">System.DoubleSpecifies the new position.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="61eec-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61eec-115">Remarks</span></span>

<span data-ttu-id="61eec-116">Это событие не вызывается во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="61eec-116">This event is not raised routinely during playback.</span></span> <span data-ttu-id="61eec-117">Это происходит только тогда, когда что-то активно изменяет текущее положение воспроизводимого элемента мультимедиа, например, когда пользователь перемещает маркер поиска или когда выполняется код, указывающий значение для Ивмпконтролс. **CurrentPosition**.</span><span class="sxs-lookup"><span data-stu-id="61eec-117">It only occurs when something actively changes the current position of the playing media item, such as when the user moves the seek handle or when code is executed that specifies a value for IWMPControls.**currentPosition**.</span></span>

## <a name="requirements"></a><span data-ttu-id="61eec-118">Требования</span><span class="sxs-lookup"><span data-stu-id="61eec-118">Requirements</span></span>



| <span data-ttu-id="61eec-119">Требование</span><span class="sxs-lookup"><span data-stu-id="61eec-119">Requirement</span></span> | <span data-ttu-id="61eec-120">Значение</span><span class="sxs-lookup"><span data-stu-id="61eec-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61eec-121">Версия</span><span class="sxs-lookup"><span data-stu-id="61eec-121">Version</span></span><br/>   | <span data-ttu-id="61eec-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="61eec-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="61eec-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="61eec-123">Namespace</span></span><br/> | <span data-ttu-id="61eec-124">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="61eec-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="61eec-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="61eec-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="61eec-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="61eec-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61eec-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61eec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61eec-128">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="61eec-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="61eec-129">**Ивмпконтролс. currentPosition (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="61eec-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





