---
title: Сообщение WM_LBUTTONDOWN (Winuser. h)
description: Посылается, когда пользователь нажимает левую кнопку мыши, когда курсор находится в клиентской области окна.
ms.assetid: 2e43720a-98e6-407a-9430-34c288c3da51
keywords:
- WM_LBUTTONDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_LBUTTONDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: c8ac54e813d622f47462b73b763534977ba0932f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698823"
---
# <a name="wm_lbuttondown-message"></a><span data-ttu-id="4240b-104">\_Сообщение ЛБУТТОНДОВН WM</span><span class="sxs-lookup"><span data-stu-id="4240b-104">WM\_LBUTTONDOWN message</span></span>

<span data-ttu-id="4240b-105">Посылается, когда пользователь нажимает левую кнопку мыши, когда курсор находится в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="4240b-105">Posted when the user presses the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="4240b-106">Если мышь не захвачена, сообщение отправляется в окно под курсором.</span><span class="sxs-lookup"><span data-stu-id="4240b-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="4240b-107">В противном случае сообщение отправляется в окно, которое захватывает мышь.</span><span class="sxs-lookup"><span data-stu-id="4240b-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="4240b-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4240b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDOWN                  0x0201
```



## <a name="parameters"></a><span data-ttu-id="4240b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4240b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4240b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4240b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4240b-111">Указывает, работают ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="4240b-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="4240b-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4240b-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="4240b-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4240b-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="4240b-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4240b-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="4240b-115"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="4240b-116">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="4240b-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="4240b-117"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="4240b-118">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="4240b-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="4240b-119"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="4240b-120">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="4240b-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="4240b-121"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="4240b-122">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="4240b-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="4240b-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="4240b-124">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="4240b-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="4240b-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="4240b-126">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="4240b-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="4240b-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="4240b-128">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="4240b-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="4240b-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4240b-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4240b-130">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="4240b-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="4240b-131">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="4240b-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="4240b-132">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="4240b-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="4240b-133">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="4240b-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4240b-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4240b-134">Return value</span></span>

<span data-ttu-id="4240b-135">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="4240b-135">If an application processes this message, it should return zero.</span></span>

## <a name="example"></a><span data-ttu-id="4240b-136">Пример</span><span class="sxs-lookup"><span data-stu-id="4240b-136">Example</span></span>


```cpp
LRESULT CALLBACK WndProc(_In_ HWND hWnd, _In_ UINT msg, _In_ WPARAM wParam, _In_ LPARAM lParam)
{
    POINT pt;

    switch (msg)
    {

    case WM_LBUTTONDOWN:
            {
                pt.x = GET_X_LPARAM(lParam);
                pt.y = GET_Y_LPARAM(lParam);
            }
        }
        break;

    default:
        return DefWindowProc(hWnd, msg, wParam, lParam);
    }
    return 0;
}
```

<span data-ttu-id="4240b-137">Дополнительные примеры см. в разделе [классические примеры Windows](https://github.com/microsoft/Windows-classic-samples) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="4240b-137">For more examples see [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="4240b-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4240b-138">Remarks</span></span>

<span data-ttu-id="4240b-139">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="4240b-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="4240b-140">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="4240b-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="4240b-141">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="4240b-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4240b-142">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="4240b-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="4240b-143">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="4240b-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="4240b-144">Чтобы обнаружить, что нажата клавиша ALT, проверьте, < ли в **\_ меню** " [**жеткэйстате**](/windows/win32/api/winuser/nf-winuser-getkeystate) " VK "0".</span><span class="sxs-lookup"><span data-stu-id="4240b-144">To detect that the ALT key was pressed, check whether [**GetKeyState**](/windows/win32/api/winuser/nf-winuser-getkeystate) with **VK\_MENU** < 0.</span></span> <span data-ttu-id="4240b-145">Обратите внимание, что это не должно быть [**жетасинккэйстате**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="4240b-145">Note, this must not be [**GetAsyncKeyState**](/windows/win32/api/winuser/nf-winuser-getasynckeystate).</span></span>

## <a name="requirements"></a><span data-ttu-id="4240b-146">Требования</span><span class="sxs-lookup"><span data-stu-id="4240b-146">Requirements</span></span>



| <span data-ttu-id="4240b-147">Требование</span><span class="sxs-lookup"><span data-stu-id="4240b-147">Requirement</span></span> | <span data-ttu-id="4240b-148">Значение</span><span class="sxs-lookup"><span data-stu-id="4240b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4240b-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4240b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="4240b-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4240b-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4240b-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4240b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="4240b-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4240b-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4240b-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4240b-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="4240b-154"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4240b-154"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4240b-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4240b-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="4240b-156">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="4240b-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4240b-157">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="4240b-157">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="4240b-158">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="4240b-158">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="4240b-159">**Захват**</span><span class="sxs-lookup"><span data-stu-id="4240b-159">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="4240b-160">**жеткэйстате**</span><span class="sxs-lookup"><span data-stu-id="4240b-160">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
</dt> <dt>

[<span data-ttu-id="4240b-161">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="4240b-161">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="4240b-162">**WM \_ лбуттондблклк**</span><span class="sxs-lookup"><span data-stu-id="4240b-162">**WM\_LBUTTONDBLCLK**</span></span>](wm-lbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="4240b-163">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="4240b-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="4240b-164">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="4240b-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4240b-165">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="4240b-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="4240b-166">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="4240b-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4240b-167">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="4240b-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="4240b-168">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4240b-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

