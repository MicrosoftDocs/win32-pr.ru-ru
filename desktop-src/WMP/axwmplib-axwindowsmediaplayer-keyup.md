---
title: Событие KeyUp объекта Аксвиндовсмедиаплайер
description: Событие KeyUp возникает при отпускании клавиши. | Событие KeyUp объекта Аксвиндовсмедиаплайер
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Событие KeyUp объекта Аксвиндовсмедиаплайер проигрыватель Windows Media
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509f520ff7624b0b29302d7bf5cd825cd45b4254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698771"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="e901e-105">Событие KeyUp объекта Аксвиндовсмедиаплайер</span><span class="sxs-lookup"><span data-stu-id="e901e-105">KeyUp Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="e901e-106">Событие KeyUp возникает при отпускании клавиши.</span><span class="sxs-lookup"><span data-stu-id="e901e-106">The KeyUp event occurs when a key is released.</span></span>

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a><span data-ttu-id="e901e-107">Данные о событиях</span><span class="sxs-lookup"><span data-stu-id="e901e-107">Event Data</span></span>

<span data-ttu-id="e901e-108">Обработчик, связанный с этим событием, имеет тип **аксвмплиб. \_ Вмпокксевентс \_ кэйупевенсандлер**.</span><span class="sxs-lookup"><span data-stu-id="e901e-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEventHandler**.</span></span> <span data-ttu-id="e901e-109">Этот обработчик получает аргумент типа **аксвмплиб. \_ Вмпокксевентс \_ кэйупевент**, который содержит следующие свойства, связанные с этим событием.</span><span class="sxs-lookup"><span data-stu-id="e901e-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_KeyUpEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="e901e-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="e901e-110">Property</span></span>    | <span data-ttu-id="e901e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="e901e-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e901e-112">нкэйкоде</span><span class="sxs-lookup"><span data-stu-id="e901e-112">nKeyCode</span></span>    | <span data-ttu-id="e901e-113">System. Int16Specifies, на котором нажата физическая клавиша.</span><span class="sxs-lookup"><span data-stu-id="e901e-113">System.Int16Specifies which physical key is pressed.</span></span> <span data-ttu-id="e901e-114">Возможные значения см. в разделе "Примечания" события KeyDown.</span><span class="sxs-lookup"><span data-stu-id="e901e-114">For possible values, see the Remarks section of the KeyDown event.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="e901e-115">ншифтстате</span><span class="sxs-lookup"><span data-stu-id="e901e-115">nShiftState</span></span> | <span data-ttu-id="e901e-116">System. Int16 — битовые биты с наименее значащими битами, соответствующими клавише SHIFT (бит 0), клавишей CTRL (бит 1) и клавишей ALT (бит 2).</span><span class="sxs-lookup"><span data-stu-id="e901e-116">System.Int16A bitfield with the least significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="e901e-117">Эти биты соответствуют значениям 1, 2 и 4 соответственно.</span><span class="sxs-lookup"><span data-stu-id="e901e-117">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="e901e-118">Аргумент shift указывает состояние этих ключей.</span><span class="sxs-lookup"><span data-stu-id="e901e-118">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="e901e-119">Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.</span><span class="sxs-lookup"><span data-stu-id="e901e-119">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e901e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e901e-120">Requirements</span></span>



| <span data-ttu-id="e901e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e901e-121">Requirement</span></span> | <span data-ttu-id="e901e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e901e-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e901e-123">Версия</span><span class="sxs-lookup"><span data-stu-id="e901e-123">Version</span></span><br/>   | <span data-ttu-id="e901e-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e901e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="e901e-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e901e-125">Namespace</span></span><br/> | <span data-ttu-id="e901e-126">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="e901e-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e901e-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="e901e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e901e-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e901e-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e901e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e901e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e901e-130">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e901e-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





