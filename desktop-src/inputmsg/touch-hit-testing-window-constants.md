---
title: Константы окна проверки нажатия касания
description: Указывает, как сообщения для проверки попадания касания обрабатываются окнами, зарегистрированными с помощью функции Регистертаучхиттестингвиндов.
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415908"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="97868-103">Константы окна проверки нажатия касания</span><span class="sxs-lookup"><span data-stu-id="97868-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="97868-104">Указывает, как сообщения для проверки попадания касания обрабатываются окнами, зарегистрированными с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="97868-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="97868-105">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="97868-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="97868-106">Описание</span><span class="sxs-lookup"><span data-stu-id="97868-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="97868-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="97868-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="97868-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) сообщения не отправляются в целевое окно, но отправляются в дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="97868-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="97868-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="97868-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="97868-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) сообщения отправляются в целевое окно.</span><span class="sxs-lookup"><span data-stu-id="97868-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="97868-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="97868-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="97868-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) сообщения не отправляются в целевое окно или дочерние окна.</span><span class="sxs-lookup"><span data-stu-id="97868-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="97868-113">Требования</span><span class="sxs-lookup"><span data-stu-id="97868-113">Requirements</span></span>



| <span data-ttu-id="97868-114">Требование</span><span class="sxs-lookup"><span data-stu-id="97868-114">Requirement</span></span> | <span data-ttu-id="97868-115">Значение</span><span class="sxs-lookup"><span data-stu-id="97868-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97868-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97868-116">Minimum supported client</span></span><br/> | <span data-ttu-id="97868-117">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="97868-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97868-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97868-118">Minimum supported server</span></span><br/> | <span data-ttu-id="97868-119">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="97868-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97868-120">Header</span><span class="sxs-lookup"><span data-stu-id="97868-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="97868-121"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="97868-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97868-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97868-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97868-123">Константы</span><span class="sxs-lookup"><span data-stu-id="97868-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="97868-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="97868-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

