---
title: Сообщение MM_JOY2BUTTONDOWN (Ммсистем. h)
description: '\_Сообщение JOY2BUTTONDOWN mm уведомляет окно с захваченным джойстиком JOYSTICKID2, что была нажата кнопка.'
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672493"
---
# <a name="mm_joy2buttondown-message"></a><span data-ttu-id="6d13a-104">MM \_ JOY2BUTTONDOWN, сообщение</span><span class="sxs-lookup"><span data-stu-id="6d13a-104">MM\_JOY2BUTTONDOWN message</span></span>

<span data-ttu-id="6d13a-105">Сообщение **\_ JOY2BUTTONDOWN mm** уведомляет окно с захваченным джойстиком JOYSTICKID2, что была нажата кнопка.</span><span class="sxs-lookup"><span data-stu-id="6d13a-105">The **MM\_JOY2BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID2 that a button has been pressed.</span></span>


```C++
MM_JOY2BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="6d13a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d13a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d13a-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*фвбуттонс*</span><span class="sxs-lookup"><span data-stu-id="6d13a-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="6d13a-108">Определяет кнопку, которая имеет измененное состояние и нажатые кнопки.</span><span class="sxs-lookup"><span data-stu-id="6d13a-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="6d13a-109">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6d13a-109">It can be one of the following:</span></span>



| <span data-ttu-id="6d13a-110">Требование</span><span class="sxs-lookup"><span data-stu-id="6d13a-110">Requirement</span></span> | <span data-ttu-id="6d13a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="6d13a-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="6d13a-112">\_BUTTON1CHG радости</span><span class="sxs-lookup"><span data-stu-id="6d13a-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="6d13a-113">Первая кнопка джойстика изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="6d13a-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="6d13a-114">\_BUTTON2CHG радости</span><span class="sxs-lookup"><span data-stu-id="6d13a-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="6d13a-115">Вторая кнопка джойстика изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="6d13a-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="6d13a-116">\_BUTTON3CHG радости</span><span class="sxs-lookup"><span data-stu-id="6d13a-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="6d13a-117">Третья кнопка игрового состояния изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="6d13a-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="6d13a-118">\_BUTTON4CHG радости</span><span class="sxs-lookup"><span data-stu-id="6d13a-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="6d13a-119">Четвертая кнопка джойстика изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="6d13a-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="6d13a-120">и один или несколько из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="6d13a-120">and one or more of the following:</span></span>



| <span data-ttu-id="6d13a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6d13a-121">Requirement</span></span> | <span data-ttu-id="6d13a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6d13a-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="6d13a-123">РАДОСТЬ \_</span><span class="sxs-lookup"><span data-stu-id="6d13a-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="6d13a-124">Нажата первая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="6d13a-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="6d13a-125">ДЖОЙСТИК ( \_ Button2)</span><span class="sxs-lookup"><span data-stu-id="6d13a-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="6d13a-126">Нажата вторая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="6d13a-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="6d13a-127">\_BUTTON3 радости</span><span class="sxs-lookup"><span data-stu-id="6d13a-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="6d13a-128">Нажата третья кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="6d13a-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="6d13a-129">\_BUTTON4 радости</span><span class="sxs-lookup"><span data-stu-id="6d13a-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="6d13a-130">Нажата четвертая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="6d13a-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6d13a-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*</span><span class="sxs-lookup"><span data-stu-id="6d13a-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="6d13a-132">Координаты x джойстика относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="6d13a-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="6d13a-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*</span><span class="sxs-lookup"><span data-stu-id="6d13a-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="6d13a-134">Координата по оси y джойстика относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="6d13a-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d13a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="6d13a-135">Requirements</span></span>



| <span data-ttu-id="6d13a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="6d13a-136">Requirement</span></span> | <span data-ttu-id="6d13a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="6d13a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d13a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d13a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6d13a-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d13a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6d13a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d13a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6d13a-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d13a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6d13a-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6d13a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d13a-143"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d13a-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d13a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d13a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d13a-145">Джойстики</span><span class="sxs-lookup"><span data-stu-id="6d13a-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="6d13a-146">Мультимедийные сообщения джойстика</span><span class="sxs-lookup"><span data-stu-id="6d13a-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





