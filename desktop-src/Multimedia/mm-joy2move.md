---
title: Сообщение MM_JOY2MOVE (Ммсистем. h)
description: '\_Сообщение JOY2MOVE mm уведомляет окно с захваченным джойстиком, JOYSTICKID2, что расположение джойстика изменилось.'
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- MM_JOY2MOVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135270"
---
# <a name="mm_joy2move-message"></a><span data-ttu-id="a9899-104">MM \_ JOY2MOVE, сообщение</span><span class="sxs-lookup"><span data-stu-id="a9899-104">MM\_JOY2MOVE message</span></span>

<span data-ttu-id="a9899-105">Сообщение **\_ JOY2MOVE mm** уведомляет окно с захваченным джойстиком, JOYSTICKID2, что расположение джойстика изменилось.</span><span class="sxs-lookup"><span data-stu-id="a9899-105">The **MM\_JOY2MOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position has changed.</span></span>


```C++
MM_JOY2MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="a9899-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9899-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9899-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*фвбуттонс*</span><span class="sxs-lookup"><span data-stu-id="a9899-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="a9899-108">Определяет нажатые кнопки.</span><span class="sxs-lookup"><span data-stu-id="a9899-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="a9899-109">Это может быть одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a9899-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="a9899-110">Требование</span><span class="sxs-lookup"><span data-stu-id="a9899-110">Requirement</span></span> | <span data-ttu-id="a9899-111">Значение</span><span class="sxs-lookup"><span data-stu-id="a9899-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="a9899-112">РАДОСТЬ \_</span><span class="sxs-lookup"><span data-stu-id="a9899-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="a9899-113">Нажата первая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="a9899-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="a9899-114">ДЖОЙСТИК ( \_ Button2)</span><span class="sxs-lookup"><span data-stu-id="a9899-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="a9899-115">Нажата вторая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="a9899-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="a9899-116">\_BUTTON3 радости</span><span class="sxs-lookup"><span data-stu-id="a9899-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="a9899-117">Нажата третья кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="a9899-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="a9899-118">\_BUTTON4 радости</span><span class="sxs-lookup"><span data-stu-id="a9899-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="a9899-119">Нажата четвертая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="a9899-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a9899-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*кспос*</span><span class="sxs-lookup"><span data-stu-id="a9899-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="a9899-121">Координаты x джойстика относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="a9899-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="a9899-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*ипос*</span><span class="sxs-lookup"><span data-stu-id="a9899-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="a9899-123">Координата по оси y джойстика относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="a9899-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9899-124">Требования</span><span class="sxs-lookup"><span data-stu-id="a9899-124">Requirements</span></span>



| <span data-ttu-id="a9899-125">Требование</span><span class="sxs-lookup"><span data-stu-id="a9899-125">Requirement</span></span> | <span data-ttu-id="a9899-126">Значение</span><span class="sxs-lookup"><span data-stu-id="a9899-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9899-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9899-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a9899-128">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9899-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9899-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9899-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a9899-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9899-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9899-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9899-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9899-132"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9899-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9899-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9899-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9899-134">Джойстики</span><span class="sxs-lookup"><span data-stu-id="a9899-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="a9899-135">Мультимедийные сообщения джойстика</span><span class="sxs-lookup"><span data-stu-id="a9899-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





