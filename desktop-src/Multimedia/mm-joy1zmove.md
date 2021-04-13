---
title: Сообщение MM_JOY1ZMOVE (Ммсистем. h)
description: '\_Сообщение JOY1ZMOVE мм уведомляет окно с захваченным джойстиком, JOYSTICKID1, что расположение джойстика на оси z изменилось.'
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d4db3db8c1817f0502ce14cc5328ad666b32c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493275"
---
# <a name="mm_joy1zmove-message"></a><span data-ttu-id="18ac9-104">MM \_ JOY1ZMOVE, сообщение</span><span class="sxs-lookup"><span data-stu-id="18ac9-104">MM\_JOY1ZMOVE message</span></span>

<span data-ttu-id="18ac9-105">Сообщение **\_ JOY1ZMOVE мм** уведомляет окно с захваченным джойстиком, JOYSTICKID1, что расположение джойстика на оси z изменилось.</span><span class="sxs-lookup"><span data-stu-id="18ac9-105">The **MM\_JOY1ZMOVE** message notifies the window that has captured joystick JOYSTICKID1 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="18ac9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="18ac9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ac9-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*фвбуттонс*</span><span class="sxs-lookup"><span data-stu-id="18ac9-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="18ac9-108">Определяет нажатые кнопки.</span><span class="sxs-lookup"><span data-stu-id="18ac9-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="18ac9-109">Это может быть одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="18ac9-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="18ac9-110">Требование</span><span class="sxs-lookup"><span data-stu-id="18ac9-110">Requirement</span></span> | <span data-ttu-id="18ac9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="18ac9-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="18ac9-112">РАДОСТЬ \_</span><span class="sxs-lookup"><span data-stu-id="18ac9-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="18ac9-113">Нажата первая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="18ac9-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="18ac9-114">ДЖОЙСТИК ( \_ Button2)</span><span class="sxs-lookup"><span data-stu-id="18ac9-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="18ac9-115">Нажата вторая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="18ac9-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="18ac9-116">\_BUTTON3 радости</span><span class="sxs-lookup"><span data-stu-id="18ac9-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="18ac9-117">Нажата третья кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="18ac9-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="18ac9-118">\_BUTTON4 радости</span><span class="sxs-lookup"><span data-stu-id="18ac9-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="18ac9-119">Нажата четвертая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="18ac9-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="18ac9-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*зпос*</span><span class="sxs-lookup"><span data-stu-id="18ac9-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="18ac9-121">Z-координата джойстика.</span><span class="sxs-lookup"><span data-stu-id="18ac9-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18ac9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="18ac9-122">Requirements</span></span>



| <span data-ttu-id="18ac9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="18ac9-123">Requirement</span></span> | <span data-ttu-id="18ac9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="18ac9-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ac9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18ac9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="18ac9-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18ac9-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="18ac9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18ac9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="18ac9-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="18ac9-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="18ac9-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="18ac9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ac9-130"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="18ac9-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ac9-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18ac9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ac9-132">Джойстики</span><span class="sxs-lookup"><span data-stu-id="18ac9-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="18ac9-133">Мультимедийные сообщения джойстика</span><span class="sxs-lookup"><span data-stu-id="18ac9-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





