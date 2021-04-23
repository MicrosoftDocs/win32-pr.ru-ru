---
title: Сообщение WM_LBUTTONDBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды щелкает левую кнопку мыши, когда курсор находится в клиентской области окна.
ms.assetid: 370aa19e-4939-4ac3-9c0b-137a9792e52a
keywords:
- WM_LBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_LBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd91eef026ae027e183b4f304211915e7bbbd95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691812"
---
# <a name="wm_lbuttondblclk-message"></a><span data-ttu-id="0691c-104">\_Сообщение ЛБУТТОНДБЛКЛК WM</span><span class="sxs-lookup"><span data-stu-id="0691c-104">WM\_LBUTTONDBLCLK message</span></span>

<span data-ttu-id="0691c-105">Посылается, когда пользователь дважды щелкает левую кнопку мыши, когда курсор находится в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="0691c-105">Posted when the user double-clicks the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="0691c-106">Если мышь не захвачена, сообщение отправляется в окно под курсором.</span><span class="sxs-lookup"><span data-stu-id="0691c-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="0691c-107">В противном случае сообщение отправляется в окно, которое захватывает мышь.</span><span class="sxs-lookup"><span data-stu-id="0691c-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="0691c-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0691c-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDBLCLK                0x0203
```



## <a name="parameters"></a><span data-ttu-id="0691c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0691c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0691c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0691c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0691c-111">Указывает, работают ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="0691c-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="0691c-112">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0691c-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="0691c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="0691c-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="0691c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0691c-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="0691c-115"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="0691c-116">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="0691c-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="0691c-117"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="0691c-118">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="0691c-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="0691c-119"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="0691c-120">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="0691c-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="0691c-121"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="0691c-122">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="0691c-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="0691c-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="0691c-124">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="0691c-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="0691c-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="0691c-126">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="0691c-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="0691c-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="0691c-128">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="0691c-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="0691c-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0691c-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0691c-130">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="0691c-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="0691c-131">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="0691c-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="0691c-132">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="0691c-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="0691c-133">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="0691c-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0691c-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0691c-134">Return value</span></span>

<span data-ttu-id="0691c-135">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="0691c-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="0691c-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0691c-136">Remarks</span></span>

<span data-ttu-id="0691c-137">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="0691c-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="0691c-138">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="0691c-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="0691c-139">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0691c-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="0691c-140">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="0691c-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0691c-141">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="0691c-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="0691c-142">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="0691c-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="0691c-143">Только окна, имеющие стиль **CS \_ дблклкс** , могут получить сообщения **WM \_ лбуттондблклк** , которые система создает каждый раз, когда пользователь нажимает, отпускает и снова нажимает левую кнопку мыши в пределах времени двойного щелчка системы.</span><span class="sxs-lookup"><span data-stu-id="0691c-143">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_LBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="0691c-144">Двойной щелчок левой кнопки мыши на самом деле создает последовательность из четырех сообщений: [**WM \_ лбуттондовн**](wm-lbuttondown.md), [**WM \_ Лбуттонуп**](wm-lbuttonup.md), **WM \_ лбуттондблклк** и **WM \_ лбуттонуп**.</span><span class="sxs-lookup"><span data-stu-id="0691c-144">Double-clicking the left mouse button actually generates a sequence of four messages: [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_LBUTTONUP**](wm-lbuttonup.md), **WM\_LBUTTONDBLCLK**, and **WM\_LBUTTONUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0691c-145">Требования</span><span class="sxs-lookup"><span data-stu-id="0691c-145">Requirements</span></span>



| <span data-ttu-id="0691c-146">Требование</span><span class="sxs-lookup"><span data-stu-id="0691c-146">Requirement</span></span> | <span data-ttu-id="0691c-147">Значение</span><span class="sxs-lookup"><span data-stu-id="0691c-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0691c-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0691c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0691c-149">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0691c-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0691c-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0691c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0691c-151">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0691c-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0691c-152">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0691c-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="0691c-153"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0691c-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0691c-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0691c-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="0691c-155">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="0691c-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0691c-156">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="0691c-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="0691c-157">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="0691c-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="0691c-158">**Захват**</span><span class="sxs-lookup"><span data-stu-id="0691c-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="0691c-159">**жетдаублекликктиме**</span><span class="sxs-lookup"><span data-stu-id="0691c-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="0691c-160">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="0691c-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="0691c-161">**сетдаублекликктиме**</span><span class="sxs-lookup"><span data-stu-id="0691c-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="0691c-162">**WM \_ лбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="0691c-162">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="0691c-163">**WM \_ лбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="0691c-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="0691c-164">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0691c-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0691c-165">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="0691c-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="0691c-166">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="0691c-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0691c-167">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="0691c-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="0691c-168">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0691c-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

