---
title: Событие DoubleClick объекта Аксвиндовсмедиаплайер
description: Событие DoubleClick возникает, когда пользователь дважды щелкает кнопку мыши в элементе управления проигрывателя Windows Media.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Событие DoubleClick в проигрывателе Windows Media объекта Аксвиндовсмедиаплайер
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694962"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="96f2b-104">Событие DoubleClick объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="96f2b-104">DoubleClick Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="96f2b-105">Событие DoubleClick возникает, когда пользователь дважды щелкает кнопку мыши в элементе управления проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="96f2b-105">The DoubleClick event occurs when the user double-clicks a mouse button on a Windows Media Player control.</span></span>

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a><span data-ttu-id="96f2b-106">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="96f2b-106">Event Data</span></span>

<span data-ttu-id="96f2b-107">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ даублекликкевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="96f2b-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEventHandler**.</span></span> <span data-ttu-id="96f2b-108">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ даублекликкевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="96f2b-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_DoubleClickEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="96f2b-109">Свойство</span><span class="sxs-lookup"><span data-stu-id="96f2b-109">Property</span></span>    | <span data-ttu-id="96f2b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="96f2b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96f2b-111">нбуттон</span><span class="sxs-lookup"><span data-stu-id="96f2b-111">nButton</span></span>     | <span data-ttu-id="96f2b-112">System. Int16-битовые биты с битами, соответствующими левой кнопке (бит 0), правой кнопке (бит 1) и средней кнопке (бит 2).</span><span class="sxs-lookup"><span data-stu-id="96f2b-112">System.Int16A bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="96f2b-113">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="96f2b-113">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="96f2b-114">Задан только один из битов, указывающий кнопку, вызвавшую событие.</span><span class="sxs-lookup"><span data-stu-id="96f2b-114">Only one of the bits is set, indicating the button that caused the event.</span></span><br/>                                                |
| <span data-ttu-id="96f2b-115">ншифтстате</span><span class="sxs-lookup"><span data-stu-id="96f2b-115">nShiftState</span></span> | <span data-ttu-id="96f2b-116">System. Int16 — битовые биты с наименее значащими битами, соответствующими клавише SHIFT (бит 0), клавишей CTRL (бит 1) и клавишей ALT (бит 2).</span><span class="sxs-lookup"><span data-stu-id="96f2b-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="96f2b-117">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="96f2b-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="96f2b-118">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="96f2b-118">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |
| <span data-ttu-id="96f2b-119">fX</span><span class="sxs-lookup"><span data-stu-id="96f2b-119">fX</span></span>          | <span data-ttu-id="96f2b-120">Координата по оси System. Int32The x указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="96f2b-120">System.Int32The x-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |
| <span data-ttu-id="96f2b-121">Обозначения</span><span class="sxs-lookup"><span data-stu-id="96f2b-121">fY</span></span>          | <span data-ttu-id="96f2b-122">Координата y System. Int32The указателя мыши относительно левого верхнего угла элемента управления.</span><span class="sxs-lookup"><span data-stu-id="96f2b-122">System.Int32The y-coordinate of the mouse pointer relative to the upper-left corner of the control.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="96f2b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="96f2b-123">Requirements</span></span>



| <span data-ttu-id="96f2b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="96f2b-124">Requirement</span></span> | <span data-ttu-id="96f2b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="96f2b-125">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96f2b-126">Версия</span><span class="sxs-lookup"><span data-stu-id="96f2b-126">Version</span></span><br/>   | <span data-ttu-id="96f2b-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="96f2b-127">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="96f2b-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="96f2b-128">Namespace</span></span><br/> | <span data-ttu-id="96f2b-129">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="96f2b-129">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="96f2b-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="96f2b-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="96f2b-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="96f2b-131"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96f2b-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96f2b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f2b-133">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="96f2b-133">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





