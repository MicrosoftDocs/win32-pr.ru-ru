---
title: Сообщение MM_JOY2BUTTONUP (Ммсистем. h)
description: '\_Сообщение JOY2BUTTONUP mm уведомляет окно с захваченным джойстиком, JOYSTICKID2, что кнопка была снята.'
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682162"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="4310a-104">MM \_ JOY2BUTTONUP, сообщение</span><span class="sxs-lookup"><span data-stu-id="4310a-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="4310a-105">Сообщение **\_ JOY2BUTTONUP mm** уведомляет окно с захваченным джойстиком, JOYSTICKID2, что кнопка была снята.</span><span class="sxs-lookup"><span data-stu-id="4310a-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="4310a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4310a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4310a-107">**фвбуттонс**</span><span class="sxs-lookup"><span data-stu-id="4310a-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="4310a-108">Определяет кнопку, которая имеет измененное состояние и нажатые кнопки.</span><span class="sxs-lookup"><span data-stu-id="4310a-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="4310a-109">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="4310a-109">It can be one of the following:</span></span>



| <span data-ttu-id="4310a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="4310a-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="4310a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4310a-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="4310a-112"><dt>**\_BUTTON1CHG радости**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="4310a-113">Первая кнопка джойстика изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="4310a-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="4310a-114"><dt>**\_BUTTON2CHG радости**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="4310a-115">Вторая кнопка джойстика изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="4310a-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="4310a-116"><dt>**\_BUTTON3CHG радости**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="4310a-117">Третья кнопка игрового состояния изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="4310a-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="4310a-118"><dt>**\_BUTTON4CHG радости**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="4310a-119">Четвертая кнопка джойстика изменила состояние.</span><span class="sxs-lookup"><span data-stu-id="4310a-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="4310a-120">и один или несколько из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="4310a-120">and one or more of the following:</span></span>



| <span data-ttu-id="4310a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4310a-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="4310a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4310a-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="4310a-123"><dt>**РАДОСТЬ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="4310a-124">Нажата первая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="4310a-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="4310a-125"><dt>**ДЖОЙСТИК ( \_ Button2)**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="4310a-126">Нажата вторая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="4310a-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="4310a-127"><dt>**\_BUTTON3 радости**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="4310a-128">Нажата третья кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="4310a-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="4310a-129"><dt>**\_BUTTON4 радости**</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="4310a-130">Нажата четвертая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="4310a-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4310a-131">**кспос**</span><span class="sxs-lookup"><span data-stu-id="4310a-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="4310a-132">Координаты x джойстика относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="4310a-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="4310a-133">**ипос**</span><span class="sxs-lookup"><span data-stu-id="4310a-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="4310a-134">Координата по оси y джойстика относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="4310a-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4310a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="4310a-135">Requirements</span></span>



| <span data-ttu-id="4310a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="4310a-136">Requirement</span></span> | <span data-ttu-id="4310a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4310a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4310a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4310a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4310a-139">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4310a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4310a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4310a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4310a-141">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4310a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4310a-142">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4310a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="4310a-143"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4310a-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4310a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4310a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4310a-145">Джойстики</span><span class="sxs-lookup"><span data-stu-id="4310a-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="4310a-146">Мультимедийные сообщения джойстика</span><span class="sxs-lookup"><span data-stu-id="4310a-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





