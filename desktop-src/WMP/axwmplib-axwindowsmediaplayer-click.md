---
title: Событие Click объекта Аксвиндовсмедиаплайер
description: Событие Click возникает, когда пользователь нажимает кнопку мыши в элементе управления проигрывателя Windows Media.
ms.assetid: 41a719a2-103a-46b5-806d-5c21c4a09e00
keywords:
- Событие Click объекта Аксвиндовсмедиаплайер проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- Click Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d316e5dc4c12e75d75dd0b292c1df6db974bc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694379"
---
# <a name="click-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e3744-104">Событие Click объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="e3744-104">Click Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e3744-105">Событие Click возникает, когда пользователь нажимает кнопку мыши в элементе управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e3744-105">The Click event occurs when the user clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_OnClick(
  object  sender,
  _WMPOCXEvents_ClickEvent e
);

[Visual Basic]
Private Sub player_OnClick(  
  sender As Object,
  e As WMPOCXEvents_ClickEvent
) Handles player.ClickEvent
```

## <a name="event-data"></a><span data-ttu-id="e3744-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="e3744-106">Event Data</span></span>

<span data-ttu-id="e3744-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кликкевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="e3744-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ClickEventHandler**.</span></span> <span data-ttu-id="e3744-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кликкевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="e3744-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="e3744-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="e3744-109">Property</span></span>    | <span data-ttu-id="e3744-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e3744-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3744-111">нбуттон</span><span class="sxs-lookup"><span data-stu-id="e3744-111">nButton</span></span>     | <span data-ttu-id="e3744-112">System. Int16-битовые биты с битами, соответствующими левой кнопке (бит 0), правой кнопке (бит 1) и средней кнопке (бит 2).</span><span class="sxs-lookup"><span data-stu-id="e3744-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="e3744-113">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="e3744-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="e3744-114">Задан только один из битов, указывающий кнопку, вызвавшую событие.</span><span class="sxs-lookup"><span data-stu-id="e3744-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="e3744-115">ншифтстате</span><span class="sxs-lookup"><span data-stu-id="e3744-115">nShiftState</span></span> | <span data-ttu-id="e3744-116">System. Int16 — битовые биты с наименее значащими битами, соответствующими клавише SHIFT (бит 0), клавишей CTRL (бит 1) и клавишей ALT (бит 2).</span><span class="sxs-lookup"><span data-stu-id="e3744-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="e3744-117">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="e3744-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="e3744-118">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="e3744-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="e3744-119">fX</span><span class="sxs-lookup"><span data-stu-id="e3744-119">fX</span></span>          | <span data-ttu-id="e3744-120">Координата по оси System. Int32The x указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e3744-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="e3744-121">Обозначения</span><span class="sxs-lookup"><span data-stu-id="e3744-121">fY</span></span>          | <span data-ttu-id="e3744-122">Координата y System. Int32The указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="e3744-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="e3744-123">Требования</span><span class="sxs-lookup"><span data-stu-id="e3744-123">Requirements</span></span>



| <span data-ttu-id="e3744-124">Требование</span><span class="sxs-lookup"><span data-stu-id="e3744-124">Requirement</span></span> | <span data-ttu-id="e3744-125">Значение</span><span class="sxs-lookup"><span data-stu-id="e3744-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3744-126">Версия</span><span class="sxs-lookup"><span data-stu-id="e3744-126">Version</span></span><br/>   | <span data-ttu-id="e3744-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e3744-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e3744-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e3744-128">Namespace</span></span><br/> | <span data-ttu-id="e3744-129">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="e3744-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e3744-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="e3744-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e3744-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e3744-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3744-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e3744-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3744-133">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e3744-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





