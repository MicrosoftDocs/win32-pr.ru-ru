---
title: Событие MouseUp объекта Аксвиндовсмедиаплайер
description: Событие MouseUp возникает, когда пользователь отпускает кнопку мыши. | Событие MouseUp объекта Аксвиндовсмедиаплайер
ms.assetid: 26bb6e82-d744-4770-b4de-07c9f52b76ec
keywords:
- Событие MouseUp объекта Аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- MouseUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2bf9c209b4fa263eb0a6cbcba2a32b0b1c46fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695168"
---
# <a name="mouseup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="33ec8-105">Событие MouseUp объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="33ec8-105">MouseUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="33ec8-106">Событие MouseUp возникает, когда пользователь отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="33ec8-106">The MouseUp event occurs when the user releases a mouse button.</span></span>

``` syntax
[C#]
private void player_MouseUpEvent(
  object sender,
  _WMPOCXEvents_MouseUpEvent e
)

[Visual Basic]
Private Sub player_MouseUpEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseUpEvent
) Handles player.MouseUpEvent
```

## <a name="event-data"></a><span data-ttu-id="33ec8-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="33ec8-107">Event Data</span></span>

<span data-ttu-id="33ec8-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ маусеупевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="33ec8-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEventHandler**.</span></span> <span data-ttu-id="33ec8-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ маусеупевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="33ec8-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MouseUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="33ec8-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="33ec8-110">Property</span></span>    | <span data-ttu-id="33ec8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="33ec8-111">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ec8-112">нбуттон</span><span class="sxs-lookup"><span data-stu-id="33ec8-112">nButton</span></span>     | <span data-ttu-id="33ec8-113">System. Int16-битовые биты с битами, соответствующими левой кнопке (бит 0), правой кнопке (бит 1) и средней кнопке (бит 2).</span><span class="sxs-lookup"><span data-stu-id="33ec8-113">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="33ec8-114">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="33ec8-114">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="33ec8-115">Задан только один из битов, указывающий кнопку, вызвавшую событие.</span><span class="sxs-lookup"><span data-stu-id="33ec8-115">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="33ec8-116">ншифтстате</span><span class="sxs-lookup"><span data-stu-id="33ec8-116">nShiftState</span></span> | <span data-ttu-id="33ec8-117">System. Int16 — битовые биты с наименее значащими битами, соответствующими клавише SHIFT (бит 0), клавишей CTRL (бит 1) и клавишей ALT (бит 2).</span><span class="sxs-lookup"><span data-stu-id="33ec8-117">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="33ec8-118">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="33ec8-118">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="33ec8-119">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="33ec8-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="33ec8-120">fX</span><span class="sxs-lookup"><span data-stu-id="33ec8-120">fX</span></span>          | <span data-ttu-id="33ec8-121">Координата по оси System. Int32The x указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="33ec8-121">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="33ec8-122">Обозначения</span><span class="sxs-lookup"><span data-stu-id="33ec8-122">fY</span></span>          | <span data-ttu-id="33ec8-123">Координата y System. Int32The указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="33ec8-123">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="33ec8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="33ec8-124">Requirements</span></span>



| <span data-ttu-id="33ec8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="33ec8-125">Requirement</span></span> | <span data-ttu-id="33ec8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="33ec8-126">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ec8-127">Версия</span><span class="sxs-lookup"><span data-stu-id="33ec8-127">Version</span></span><br/>   | <span data-ttu-id="33ec8-128">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="33ec8-128">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="33ec8-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="33ec8-129">Namespace</span></span><br/> | <span data-ttu-id="33ec8-130">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="33ec8-130">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="33ec8-131">Сборка</span><span class="sxs-lookup"><span data-stu-id="33ec8-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="33ec8-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="33ec8-132"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ec8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33ec8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ec8-134">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="33ec8-134">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





