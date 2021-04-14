---
title: Сообщение WM_MOUSEMOVE (Winuser. h)
description: Отправляется в окно при перемещении курсора. Если мышь не захвачена, сообщение отправляется в окно, содержащее курсор. В противном случае сообщение отправляется в окно, которое захватывает мышь.
ms.assetid: 9b99387e-e176-4b20-a05a-bc75928a1367
keywords:
- WM_MOUSEMOVE ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_MOUSEMOVE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d61ffd10edbd58d11c5667fbda9dc0408ea1d72a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533992"
---
# <a name="wm_mousemove-message"></a><span data-ttu-id="5933d-106">\_Сообщение WM MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="5933d-106">WM\_MOUSEMOVE message</span></span>

<span data-ttu-id="5933d-107">Отправляется в окно при перемещении курсора.</span><span class="sxs-lookup"><span data-stu-id="5933d-107">Posted to a window when the cursor moves.</span></span> <span data-ttu-id="5933d-108">Если мышь не захвачена, сообщение отправляется в окно, содержащее курсор.</span><span class="sxs-lookup"><span data-stu-id="5933d-108">If the mouse is not captured, the message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="5933d-109">В противном случае сообщение отправляется в окно, которое захватывает мышь.</span><span class="sxs-lookup"><span data-stu-id="5933d-109">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="5933d-110">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5933d-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEMOVE                    0x0200
```



## <a name="parameters"></a><span data-ttu-id="5933d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5933d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5933d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5933d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5933d-113">Указывает, работают ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="5933d-113">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="5933d-114">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5933d-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="5933d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5933d-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="5933d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5933d-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="5933d-117"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="5933d-118">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="5933d-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="5933d-119"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="5933d-120">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="5933d-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="5933d-121"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="5933d-122">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="5933d-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="5933d-123"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="5933d-124">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="5933d-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="5933d-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="5933d-126">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="5933d-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="5933d-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="5933d-128">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="5933d-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="5933d-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="5933d-130">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="5933d-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="5933d-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5933d-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5933d-132">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="5933d-132">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="5933d-133">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="5933d-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="5933d-134">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="5933d-134">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="5933d-135">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="5933d-135">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5933d-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5933d-136">Return value</span></span>

<span data-ttu-id="5933d-137">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="5933d-137">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5933d-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5933d-138">Remarks</span></span>

<span data-ttu-id="5933d-139">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="5933d-139">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="5933d-140">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="5933d-140">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="5933d-141">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="5933d-141">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="5933d-142">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="5933d-142">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5933d-143">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="5933d-143">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="5933d-144">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="5933d-144">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5933d-145">Требования</span><span class="sxs-lookup"><span data-stu-id="5933d-145">Requirements</span></span>



| <span data-ttu-id="5933d-146">Требование</span><span class="sxs-lookup"><span data-stu-id="5933d-146">Requirement</span></span> | <span data-ttu-id="5933d-147">Значение</span><span class="sxs-lookup"><span data-stu-id="5933d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5933d-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5933d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="5933d-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5933d-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5933d-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5933d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="5933d-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5933d-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5933d-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="5933d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="5933d-153"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5933d-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5933d-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5933d-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="5933d-155">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="5933d-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5933d-156">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="5933d-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="5933d-157">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="5933d-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="5933d-158">**Захват**</span><span class="sxs-lookup"><span data-stu-id="5933d-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="5933d-159">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="5933d-159">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

<span data-ttu-id="5933d-160">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="5933d-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5933d-161">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="5933d-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="5933d-162">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="5933d-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5933d-163">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="5933d-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="5933d-164">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5933d-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

