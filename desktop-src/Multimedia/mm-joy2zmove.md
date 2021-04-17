---
title: Сообщение MM_JOY2ZMOVE (Ммсистем. h)
description: '\_Сообщение JOY2ZMOVE мм уведомляет окно с захваченным джойстиком, JOYSTICKID2, что расположение джойстика на оси z изменилось.'
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682161"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="51387-104">MM \_ JOY2ZMOVE, сообщение</span><span class="sxs-lookup"><span data-stu-id="51387-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="51387-105">Сообщение **\_ JOY2ZMOVE мм** уведомляет окно с захваченным джойстиком, JOYSTICKID2, что расположение джойстика на оси z изменилось.</span><span class="sxs-lookup"><span data-stu-id="51387-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="51387-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51387-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51387-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*фвбуттонс*</span><span class="sxs-lookup"><span data-stu-id="51387-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="51387-108">Определяет нажатые кнопки.</span><span class="sxs-lookup"><span data-stu-id="51387-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="51387-109">Это может быть одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="51387-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="51387-110">Требование</span><span class="sxs-lookup"><span data-stu-id="51387-110">Requirement</span></span> | <span data-ttu-id="51387-111">Значение</span><span class="sxs-lookup"><span data-stu-id="51387-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="51387-112">РАДОСТЬ \_</span><span class="sxs-lookup"><span data-stu-id="51387-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="51387-113">Нажата первая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="51387-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="51387-114">ДЖОЙСТИК ( \_ Button2)</span><span class="sxs-lookup"><span data-stu-id="51387-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="51387-115">Нажата вторая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="51387-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="51387-116">\_BUTTON3 радости</span><span class="sxs-lookup"><span data-stu-id="51387-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="51387-117">Нажата третья кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="51387-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="51387-118">\_BUTTON4 радости</span><span class="sxs-lookup"><span data-stu-id="51387-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="51387-119">Нажата четвертая кнопка джойстика.</span><span class="sxs-lookup"><span data-stu-id="51387-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="51387-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*зпос*</span><span class="sxs-lookup"><span data-stu-id="51387-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="51387-121">Z-координата джойстика.</span><span class="sxs-lookup"><span data-stu-id="51387-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51387-122">Требования</span><span class="sxs-lookup"><span data-stu-id="51387-122">Requirements</span></span>



| <span data-ttu-id="51387-123">Требование</span><span class="sxs-lookup"><span data-stu-id="51387-123">Requirement</span></span> | <span data-ttu-id="51387-124">Значение</span><span class="sxs-lookup"><span data-stu-id="51387-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51387-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51387-125">Minimum supported client</span></span><br/> | <span data-ttu-id="51387-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51387-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="51387-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51387-127">Minimum supported server</span></span><br/> | <span data-ttu-id="51387-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51387-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="51387-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="51387-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="51387-130"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51387-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51387-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51387-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51387-132">Джойстики</span><span class="sxs-lookup"><span data-stu-id="51387-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="51387-133">Мультимедийные сообщения джойстика</span><span class="sxs-lookup"><span data-stu-id="51387-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





