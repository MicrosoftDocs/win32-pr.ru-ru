---
title: Сообщение WM_LBUTTONUP (Winuser. h)
description: Публикуется, когда пользователь отпускает левую кнопку мыши, когда курсор находится в клиентской области окна.
ms.assetid: 6efa298f-85f7-40ab-a64b-16b5071f2437
keywords:
- WM_LBUTTONUP ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_LBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe921ffe68359efe15aa0782c5c8543fd0870fa
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335398"
---
# <a name="wm_lbuttonup-message"></a><span data-ttu-id="33c06-104">\_Сообщение ЛБУТТОНУП WM</span><span class="sxs-lookup"><span data-stu-id="33c06-104">WM\_LBUTTONUP message</span></span>

<span data-ttu-id="33c06-105">Публикуется, когда пользователь отпускает левую кнопку мыши, когда курсор находится в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="33c06-105">Posted when the user releases the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="33c06-106">Если мышь не захвачена, сообщение отправляется в окно под курсором.</span><span class="sxs-lookup"><span data-stu-id="33c06-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="33c06-107">В противном случае сообщение отправляется в окно, которое захватывает мышь.</span><span class="sxs-lookup"><span data-stu-id="33c06-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="33c06-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="33c06-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONUP                    0x0202
```



## <a name="parameters"></a><span data-ttu-id="33c06-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="33c06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c06-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33c06-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33c06-111">Указывает, работают ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="33c06-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="33c06-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="33c06-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="33c06-113">Значение</span><span class="sxs-lookup"><span data-stu-id="33c06-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="33c06-114">Значение</span><span class="sxs-lookup"><span data-stu-id="33c06-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="33c06-115"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="33c06-116">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="33c06-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="33c06-117"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="33c06-118">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="33c06-118">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="33c06-119"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="33c06-120">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="33c06-120">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="33c06-121"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="33c06-122">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="33c06-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="33c06-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="33c06-124">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="33c06-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="33c06-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="33c06-126">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="33c06-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="33c06-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33c06-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33c06-128">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="33c06-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="33c06-129">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="33c06-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="33c06-130">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="33c06-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="33c06-131">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="33c06-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c06-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="33c06-132">Return value</span></span>

<span data-ttu-id="33c06-133">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="33c06-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c06-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33c06-134">Remarks</span></span>

<span data-ttu-id="33c06-135">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="33c06-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="33c06-136">Как отмечалось выше, координата x находится **в низком порядке значения** lParam; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="33c06-136">As noted above, the x-coordinate is in the low-order **short** of the lParam value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="33c06-137">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="33c06-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="33c06-138">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="33c06-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="33c06-139">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="33c06-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="33c06-140">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="33c06-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33c06-141">Требования</span><span class="sxs-lookup"><span data-stu-id="33c06-141">Requirements</span></span>



| <span data-ttu-id="33c06-142">Требование</span><span class="sxs-lookup"><span data-stu-id="33c06-142">Requirement</span></span> | <span data-ttu-id="33c06-143">Значение</span><span class="sxs-lookup"><span data-stu-id="33c06-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c06-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33c06-144">Minimum supported client</span></span><br/> | <span data-ttu-id="33c06-145">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33c06-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="33c06-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33c06-146">Minimum supported server</span></span><br/> | <span data-ttu-id="33c06-147">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="33c06-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="33c06-148">Заголовок</span><span class="sxs-lookup"><span data-stu-id="33c06-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="33c06-149"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33c06-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c06-150">См. также</span><span class="sxs-lookup"><span data-stu-id="33c06-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="33c06-151">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="33c06-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33c06-152">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="33c06-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="33c06-153">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="33c06-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="33c06-154">**Захват**</span><span class="sxs-lookup"><span data-stu-id="33c06-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="33c06-155">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="33c06-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="33c06-156">**WM \_ лбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="33c06-156">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="33c06-157">**WM \_ лбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="33c06-157">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

<span data-ttu-id="33c06-158">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="33c06-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="33c06-159">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="33c06-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="33c06-160">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="33c06-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="33c06-161">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="33c06-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="33c06-162">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33c06-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

