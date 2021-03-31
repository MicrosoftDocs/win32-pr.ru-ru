---
title: Сообщение WM_XBUTTONDBLCLK (Winuser. h)
description: Посылается, когда пользователь дважды щелкает первую или вторую кнопку X, пока курсор находится в клиентской области окна.
ms.assetid: 68f7abaf-cf6d-499a-957f-3c4d73cdbdee
keywords:
- WM_XBUTTONDBLCLK ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_XBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed0612c2850f784901f01313935145fc9d3d7910
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802908"
---
# <a name="wm_xbuttondblclk-message"></a><span data-ttu-id="8d30a-104">\_Сообщение КСБУТТОНДБЛКЛК WM</span><span class="sxs-lookup"><span data-stu-id="8d30a-104">WM\_XBUTTONDBLCLK message</span></span>

<span data-ttu-id="8d30a-105">Посылается, когда пользователь дважды щелкает первую или вторую кнопку X, пока курсор находится в клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="8d30a-105">Posted when the user double-clicks the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="8d30a-106">Если мышь не захвачена, сообщение отправляется в окно под курсором.</span><span class="sxs-lookup"><span data-stu-id="8d30a-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="8d30a-107">В противном случае сообщение отправляется в окно, которое захватывает мышь.</span><span class="sxs-lookup"><span data-stu-id="8d30a-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="8d30a-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8d30a-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONDBLCLK                0x020D
```



## <a name="parameters"></a><span data-ttu-id="8d30a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8d30a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d30a-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d30a-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d30a-111">Слово низкого порядка показывает, не отключены ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="8d30a-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="8d30a-112">Это может быть одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8d30a-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="8d30a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="8d30a-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="8d30a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8d30a-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="8d30a-115"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="8d30a-116">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="8d30a-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="8d30a-117"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="8d30a-118">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="8d30a-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="8d30a-119"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="8d30a-120">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="8d30a-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="8d30a-121"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="8d30a-122">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="8d30a-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="8d30a-123"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="8d30a-124">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="8d30a-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="8d30a-125"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="8d30a-126">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="8d30a-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="8d30a-127"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="8d30a-128">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="8d30a-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="8d30a-129">Слово в высоком порядке указывает на то, какая кнопка была двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="8d30a-129">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="8d30a-130">Может быть одним из указанных далее.</span><span class="sxs-lookup"><span data-stu-id="8d30a-130">It can be one of the following values.</span></span>



| <span data-ttu-id="8d30a-131">Значение</span><span class="sxs-lookup"><span data-stu-id="8d30a-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="8d30a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8d30a-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="8d30a-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="8d30a-134">Первая кнопка X была двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="8d30a-134">The first X button was double-clicked.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="8d30a-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="8d30a-136">Вторая кнопка X была двойным щелчком.</span><span class="sxs-lookup"><span data-stu-id="8d30a-136">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8d30a-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d30a-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d30a-138">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="8d30a-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="8d30a-139">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="8d30a-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="8d30a-140">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="8d30a-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="8d30a-141">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="8d30a-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d30a-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8d30a-142">Return value</span></span>

<span data-ttu-id="8d30a-143">Если приложение обрабатывает это сообщение, оно должно возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="8d30a-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="8d30a-144">Дополнительные сведения об обработке возвращаемого значения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="8d30a-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d30a-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d30a-145">Remarks</span></span>

<span data-ttu-id="8d30a-146">Используйте следующий код, чтобы получить сведения в параметре *wParam* :</span><span class="sxs-lookup"><span data-stu-id="8d30a-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="8d30a-147">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="8d30a-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="8d30a-148">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="8d30a-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="8d30a-149">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="8d30a-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="8d30a-150">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="8d30a-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d30a-151">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="8d30a-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="8d30a-152">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="8d30a-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="8d30a-153">Только окна с стилем **CS \_ дблклкс** могут получить сообщения **WM \_ ксбуттондблклк** , которые система создает каждый раз, когда пользователь нажимает, отпускает и снова нажимает кнопку X в пределах времени двойного щелчка системы.</span><span class="sxs-lookup"><span data-stu-id="8d30a-153">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_XBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="8d30a-154">Двойной щелчок одной из этих кнопок на самом деле приводит к созданию четырех сообщений: [**WM \_ ксбуттондовн**](wm-xbuttondown.md), [**WM \_ Ксбуттонуп**](wm-xbuttonup.md), **WM \_ ксбуттондблклк** и **WM \_ ксбуттонуп** .</span><span class="sxs-lookup"><span data-stu-id="8d30a-154">Double-clicking one of these buttons actually generates four messages: [**WM\_XBUTTONDOWN**](wm-xbuttondown.md), [**WM\_XBUTTONUP**](wm-xbuttonup.md), **WM\_XBUTTONDBLCLK**, and **WM\_XBUTTONUP** again.</span></span>

<span data-ttu-id="8d30a-155">В отличие от [**сообщений \_ WM лбуттондблклк**](wm-lbuttondblclk.md), [**WM \_ мбуттондблклк**](wm-mbuttondblclk.md)и [**WM \_ рбуттондблклк**](wm-rbuttondblclk.md) , приложение должно вернуть **значение true** из этого сообщения, если оно обрабатывает его.</span><span class="sxs-lookup"><span data-stu-id="8d30a-155">Unlike the [**WM\_LBUTTONDBLCLK**](wm-lbuttondblclk.md), [**WM\_MBUTTONDBLCLK**](wm-mbuttondblclk.md), and [**WM\_RBUTTONDBLCLK**](wm-rbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="8d30a-156">Это позволит программному обеспечению имитировать это сообщение в системах Windows более ранних, чем Windows 2000, чтобы определить, обрабатывало ли это сообщение процедура окна или вызываемая [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для его обработки.</span><span class="sxs-lookup"><span data-stu-id="8d30a-156">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d30a-157">Требования</span><span class="sxs-lookup"><span data-stu-id="8d30a-157">Requirements</span></span>



| <span data-ttu-id="8d30a-158">Требование</span><span class="sxs-lookup"><span data-stu-id="8d30a-158">Requirement</span></span> | <span data-ttu-id="8d30a-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8d30a-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d30a-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d30a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8d30a-161">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d30a-161">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8d30a-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d30a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8d30a-163">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d30a-163">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8d30a-164">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8d30a-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d30a-165"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d30a-165"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d30a-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d30a-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d30a-167">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="8d30a-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d30a-168">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="8d30a-168">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="8d30a-169">**ПОЛУЧЕНИЕ \_ кэйстате \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="8d30a-169">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="8d30a-170">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="8d30a-170">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="8d30a-171">**ПОЛУЧЕНИЕ \_ ксбуттон \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="8d30a-171">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="8d30a-172">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="8d30a-172">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="8d30a-173">**Захват**</span><span class="sxs-lookup"><span data-stu-id="8d30a-173">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="8d30a-174">**жетдаублекликктиме**</span><span class="sxs-lookup"><span data-stu-id="8d30a-174">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="8d30a-175">**сетдаублекликктиме**</span><span class="sxs-lookup"><span data-stu-id="8d30a-175">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="8d30a-176">**WM \_ ксбуттондовн**</span><span class="sxs-lookup"><span data-stu-id="8d30a-176">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

[<span data-ttu-id="8d30a-177">**WM \_ ксбуттонуп**</span><span class="sxs-lookup"><span data-stu-id="8d30a-177">**WM\_XBUTTONUP**</span></span>](wm-xbuttonup.md)
</dt> <dt>

<span data-ttu-id="8d30a-178">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8d30a-178">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d30a-179">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="8d30a-179">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="8d30a-180">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="8d30a-180">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8d30a-181">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="8d30a-181">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="8d30a-182">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8d30a-182">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

