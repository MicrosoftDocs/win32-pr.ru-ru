---
title: Сообщение WM_MOUSEWHEEL (Winuser. h)
description: Посылается в окно фокуса при вращении колесика мыши.
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- WM_MOUSEWHEEL ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691805"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="28e45-104">\_Сообщение МАУСЕВХИЛ WM</span><span class="sxs-lookup"><span data-stu-id="28e45-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="28e45-105">Посылается в окно фокуса при вращении колесика мыши.</span><span class="sxs-lookup"><span data-stu-id="28e45-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="28e45-106">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) распространяет сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="28e45-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="28e45-107">Не должно быть внутренней пересылки сообщения, так как **дефвиндовпрок** распространяет его на родительскую цепочку, пока не обнаружит окно, которое его обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="28e45-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="28e45-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="28e45-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="28e45-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28e45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e45-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28e45-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28e45-111">Слово с высоким порядковым выражением указывает расстояние, на которое вращается колесико, выраженное в кратных или делениях от **\_ коэффициента наклона колесика**, то есть 120.</span><span class="sxs-lookup"><span data-stu-id="28e45-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="28e45-112">Положительное значение указывает, что колесико повернуто вперед, от пользователя; отрицательное значение указывает на то, что колесико повернуто назад, направлено к пользователю.</span><span class="sxs-lookup"><span data-stu-id="28e45-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="28e45-113">Слово низкого порядка показывает, не отключены ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="28e45-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="28e45-114">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="28e45-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="28e45-115">Значение</span><span class="sxs-lookup"><span data-stu-id="28e45-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="28e45-116">Значение</span><span class="sxs-lookup"><span data-stu-id="28e45-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="28e45-117"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="28e45-118">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="28e45-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="28e45-119"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="28e45-120">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="28e45-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="28e45-121"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="28e45-122">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="28e45-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="28e45-123"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="28e45-124">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="28e45-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="28e45-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="28e45-126">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="28e45-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="28e45-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="28e45-128">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="28e45-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="28e45-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="28e45-130">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="28e45-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="28e45-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28e45-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28e45-132">Слово нижнего порядка задает координату по оси x указателя относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="28e45-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="28e45-133">Слово в высоком порядке Указывает координату y указателя относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="28e45-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e45-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28e45-134">Return value</span></span>

<span data-ttu-id="28e45-135">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="28e45-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="28e45-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28e45-136">Remarks</span></span>

<span data-ttu-id="28e45-137">Используйте следующий код, чтобы получить сведения в параметре *wParam* :</span><span class="sxs-lookup"><span data-stu-id="28e45-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="28e45-138">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="28e45-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="28e45-139">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="28e45-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="28e45-140">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="28e45-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="28e45-141">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="28e45-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28e45-142">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="28e45-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="28e45-143">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="28e45-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="28e45-144">Поворот колесика будет кратным **\_ Дельта-кругу**, который устанавливается в 120.</span><span class="sxs-lookup"><span data-stu-id="28e45-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="28e45-145">Это пороговое значение для действия, которое необходимо выполнить, и одно из таких действий (например, прокрутка одного приращения) должно выполняться для каждой разностной разницы.</span><span class="sxs-lookup"><span data-stu-id="28e45-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="28e45-146">Дельта была установлена в 120, чтобы позволить корпорации Майкрософт или другим поставщикам создавать колеса с более высоким разрешением (с помощью свободного колесика без расхождений) для отправки большего количества сообщений на поворот, но с меньшим значением в каждом сообщении.</span><span class="sxs-lookup"><span data-stu-id="28e45-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="28e45-147">Чтобы использовать эту функцию, можно добавить входящие разностные значения до достижения **\_ Дельта** -угла (так что для сдвига изменений можно получить тот же ответ) или прокручивать частичные строки в ответ на более частые сообщения.</span><span class="sxs-lookup"><span data-stu-id="28e45-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="28e45-148">Можно также выбрать детализацию прокрутки и накапливать разности, пока она не будет достигнута.</span><span class="sxs-lookup"><span data-stu-id="28e45-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="28e45-149">Обратите внимание, что *фвкэйс* для **МШ \_ маусевхил** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="28e45-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="28e45-150">В противном случае параметры будут точно такими же, как для **WM \_ маусевхил**.</span><span class="sxs-lookup"><span data-stu-id="28e45-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="28e45-151">Приложение пересылает **МШ \_ маусевхил** всем внедренным объектам или элементам управления.</span><span class="sxs-lookup"><span data-stu-id="28e45-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="28e45-152">Приложение необходимо для отправки сообщения в активное внедренное приложение OLE.</span><span class="sxs-lookup"><span data-stu-id="28e45-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="28e45-153">Необязательно, чтобы приложение отправляло его в элемент управления с поддержкой колеса с фокусом.</span><span class="sxs-lookup"><span data-stu-id="28e45-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="28e45-154">Если приложение отправляет сообщение в элемент управления, оно может проверить возвращаемое значение, чтобы проверить, было ли сообщение обработано.</span><span class="sxs-lookup"><span data-stu-id="28e45-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="28e45-155">Элементы управления должны возвращать значение **true** , если они обрабатывают сообщение.</span><span class="sxs-lookup"><span data-stu-id="28e45-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e45-156">Требования</span><span class="sxs-lookup"><span data-stu-id="28e45-156">Requirements</span></span>



| <span data-ttu-id="28e45-157">Требование</span><span class="sxs-lookup"><span data-stu-id="28e45-157">Requirement</span></span> | <span data-ttu-id="28e45-158">Значение</span><span class="sxs-lookup"><span data-stu-id="28e45-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e45-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="28e45-159">Minimum supported client</span></span><br/> | <span data-ttu-id="28e45-160">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28e45-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="28e45-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="28e45-161">Minimum supported server</span></span><br/> | <span data-ttu-id="28e45-162">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="28e45-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28e45-163">Заголовок</span><span class="sxs-lookup"><span data-stu-id="28e45-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="28e45-164"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28e45-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e45-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="28e45-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="28e45-166">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="28e45-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28e45-167">**ПОЛУЧЕНИЕ \_ кэйстате \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="28e45-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="28e45-168">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="28e45-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="28e45-169">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="28e45-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="28e45-170">**ПОЛУЧИТЬ \_ \_ разностный \_ wParam для колеса**</span><span class="sxs-lookup"><span data-stu-id="28e45-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="28e45-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28e45-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="28e45-172">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28e45-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28e45-173">**\_событие мыши**</span><span class="sxs-lookup"><span data-stu-id="28e45-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="28e45-174">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="28e45-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28e45-175">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="28e45-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="28e45-176">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="28e45-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="28e45-177">**жетсистемметрикс**</span><span class="sxs-lookup"><span data-stu-id="28e45-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="28e45-178">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="28e45-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="28e45-179">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="28e45-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="28e45-180">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="28e45-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

