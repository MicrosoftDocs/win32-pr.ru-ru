---
title: Сообщение WM_POINTERWHEEL
description: Отправляется в окно с фокусом клавиатуры переднего плана при вращении колесика прокрутки.
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- WM_POINTERWHEEL сообщения и уведомления о входе
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ad1177b2e92e47ca40c745e6cd5f1ea2cf259215
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490029"
---
# <a name="wm_pointerwheel-message"></a><span data-ttu-id="a24a7-104">Сообщение WM_POINTERWHEEL</span><span class="sxs-lookup"><span data-stu-id="a24a7-104">WM_POINTERWHEEL message</span></span>

<span data-ttu-id="a24a7-105">Отправляется в окно с фокусом клавиатуры переднего плана при вращении колесика прокрутки.</span><span class="sxs-lookup"><span data-stu-id="a24a7-105">Posted to the window with foreground keyboard focus when a scroll wheel is rotated.</span></span>

<span data-ttu-id="a24a7-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a24a7-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="a24a7-107">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="a24a7-107">\[!Important\]</span></span>  
> <span data-ttu-id="a24a7-108">Для классических приложений следует учитывать DPI.</span><span class="sxs-lookup"><span data-stu-id="a24a7-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="a24a7-109">Если приложение не поддерживает DPI, экранные координаты, содержащиеся в сообщениях указателя и связанных структурах, могут выглядеть неточными из-за виртуализации DPI.</span><span class="sxs-lookup"><span data-stu-id="a24a7-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="a24a7-110">Виртуализация DPI обеспечивает автоматическую поддержку масштабирования для приложений, которые не поддерживают DPI и активны по умолчанию (пользователи могут отключить его).</span><span class="sxs-lookup"><span data-stu-id="a24a7-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="a24a7-111">Дополнительные сведения см. в статье [написание приложений Win32 с высоким разрешением](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a24a7-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a><span data-ttu-id="a24a7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a24a7-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a24a7-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a24a7-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24a7-114">Содержит идентификатор указателя и разницу в колесе.</span><span class="sxs-lookup"><span data-stu-id="a24a7-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="a24a7-115">Используйте следующие макросы для получения этих сведений.</span><span class="sxs-lookup"><span data-stu-id="a24a7-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="a24a7-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): идентификатор указателя.</span><span class="sxs-lookup"><span data-stu-id="a24a7-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="a24a7-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): Дельта с колесом прокрутки как короткое значение со знаком.</span><span class="sxs-lookup"><span data-stu-id="a24a7-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as a signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="a24a7-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a24a7-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a24a7-119">Содержит расположение точки указателя.</span><span class="sxs-lookup"><span data-stu-id="a24a7-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="a24a7-120">Так как указатель может установить связь с устройством в нетривиальной области, это расположение может быть упрощено более сложной областью указателя.</span><span class="sxs-lookup"><span data-stu-id="a24a7-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="a24a7-121">Когда это возможно, приложение должно использовать полные сведения об области указателя, а не расположение точки.</span><span class="sxs-lookup"><span data-stu-id="a24a7-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="a24a7-122">Используйте следующие макросы, чтобы получить физические экранные координаты точки.</span><span class="sxs-lookup"><span data-stu-id="a24a7-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="a24a7-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): координата X (горизонтальная точка).</span><span class="sxs-lookup"><span data-stu-id="a24a7-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="a24a7-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): координата Y (вертикальная точка).</span><span class="sxs-lookup"><span data-stu-id="a24a7-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a24a7-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a24a7-125">Return value</span></span>

<span data-ttu-id="a24a7-126">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="a24a7-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="a24a7-127">Если приложение не обрабатывает это сообщение, оно должно вызывать [**дефвиндовпрок**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a24a7-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="a24a7-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a24a7-128">Remarks</span></span>

<span data-ttu-id="a24a7-129">Чтобы получить единицы прокрутки колесика, используйте **inputData** , зафиксированную для структуры [**POINTER_INFO**](/previous-versions/windows/desktop/api) , возвращенной путем вызова функции [**жетпоинтеринфо**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="a24a7-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="a24a7-130">Это поле содержит значение со знаком и выражается в нескольких **WHEEL_DELTA**.</span><span class="sxs-lookup"><span data-stu-id="a24a7-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="a24a7-131">Положительное значение обозначает поворот вперед, а отрицательное значение — поворот назад.</span><span class="sxs-lookup"><span data-stu-id="a24a7-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="a24a7-132">Обратите внимание, что входные данные колеса могут доставляться, даже если курсор мыши находится за пределами окна приложения.</span><span class="sxs-lookup"><span data-stu-id="a24a7-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="a24a7-133">Сообщения колесика поставляются так же, как и входные данные клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a24a7-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="a24a7-134">Окно фокуса очереди сообщений форегаурнд получает сообщения колесика.</span><span class="sxs-lookup"><span data-stu-id="a24a7-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="a24a7-135">Требования</span><span class="sxs-lookup"><span data-stu-id="a24a7-135">Requirements</span></span>



| <span data-ttu-id="a24a7-136">Требование</span><span class="sxs-lookup"><span data-stu-id="a24a7-136">Requirement</span></span> | <span data-ttu-id="a24a7-137">Значение</span><span class="sxs-lookup"><span data-stu-id="a24a7-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a24a7-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a24a7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a24a7-139">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a24a7-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="a24a7-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a24a7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a24a7-141">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a24a7-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a24a7-142">Header</span><span class="sxs-lookup"><span data-stu-id="a24a7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a24a7-143"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a24a7-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a24a7-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a24a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a24a7-145">Сообщения</span><span class="sxs-lookup"><span data-stu-id="a24a7-145">Messages</span></span>](messages.md)
</dt> </dl>

 

