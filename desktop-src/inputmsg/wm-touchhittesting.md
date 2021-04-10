---
title: Сообщение WM_TOUCHHITTESTING
description: Отправляются в окно касанием, чтобы определить наиболее вероятную цель касания.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136483"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="76fe3-104">Сообщение WM_TOUCHHITTESTING</span><span class="sxs-lookup"><span data-stu-id="76fe3-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="76fe3-105">Отправляются в окно касанием, чтобы определить наиболее вероятную цель касания.</span><span class="sxs-lookup"><span data-stu-id="76fe3-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="76fe3-106">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="76fe3-106">\[!Important\]</span></span>  
> <span data-ttu-id="76fe3-107">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="76fe3-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="76fe3-108">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="76fe3-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="76fe3-109">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="76fe3-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="76fe3-110">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76fe3-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="76fe3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="76fe3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76fe3-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76fe3-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe3-113">Не используется.</span><span class="sxs-lookup"><span data-stu-id="76fe3-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="76fe3-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76fe3-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe3-115">Указатель на структуру [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) , содержащую данные контактной зоны касания.</span><span class="sxs-lookup"><span data-stu-id="76fe3-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76fe3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="76fe3-116">Return value</span></span>

<span data-ttu-id="76fe3-117">Если один или несколько элементов находятся в области контактного лица, приложение должно вернуть результат [**пакктаучхиттестингпроксимитевалуатион**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span><span class="sxs-lookup"><span data-stu-id="76fe3-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="76fe3-118">Если в области контактного лица нет элементов, приложение должно задать значение **Score** в [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) для [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) и вызвать метод [**ПАККТАУЧХИТТЕСТИНГПРОКСИМИТЕВАЛУАТИОН**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) , чтобы получить возвращаемое значение LRESULT.</span><span class="sxs-lookup"><span data-stu-id="76fe3-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="76fe3-119">Если приложение не обрабатывает это сообщение, оно должно вызвать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="76fe3-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="76fe3-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76fe3-120">Remarks</span></span>

<span data-ttu-id="76fe3-121">Это сообщение отправляется в Windows, которые регистрируются с помощью функции [**регистертаучхиттестингвиндов**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="76fe3-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="76fe3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="76fe3-122">Requirements</span></span>



| <span data-ttu-id="76fe3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="76fe3-123">Requirement</span></span> | <span data-ttu-id="76fe3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="76fe3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76fe3-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76fe3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="76fe3-126">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="76fe3-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="76fe3-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76fe3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="76fe3-128">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="76fe3-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="76fe3-129">Header</span><span class="sxs-lookup"><span data-stu-id="76fe3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="76fe3-130"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="76fe3-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fe3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76fe3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fe3-132">Сообщения</span><span class="sxs-lookup"><span data-stu-id="76fe3-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="76fe3-133">**Оценки проверки попадания касания**</span><span class="sxs-lookup"><span data-stu-id="76fe3-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

