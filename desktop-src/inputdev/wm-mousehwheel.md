---
title: Сообщение WM_MOUSEHWHEEL (Winuser. h)
description: Отправляется в активное окно, когда колесо горизонтальной прокрутки мыши вращается или поворачивается.
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- WM_MOUSEHWHEEL ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1f3b1690ad39919e2a62b50ba6eacec8348e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691806"
---
# <a name="wm_mousehwheel-message"></a><span data-ttu-id="3c830-104">\_Сообщение МАУСЕХВХИЛ WM</span><span class="sxs-lookup"><span data-stu-id="3c830-104">WM\_MOUSEHWHEEL message</span></span>

<span data-ttu-id="3c830-105">Отправляется в активное окно, когда колесо горизонтальной прокрутки мыши вращается или поворачивается.</span><span class="sxs-lookup"><span data-stu-id="3c830-105">Sent to the active window when the mouse's horizontal scroll wheel is tilted or rotated.</span></span> <span data-ttu-id="3c830-106">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) распространяет сообщение родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="3c830-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="3c830-107">Не должно быть внутренней пересылки сообщения, так как **дефвиндовпрок** распространяет его на родительскую цепочку, пока не обнаружит окно, которое его обрабатывает.</span><span class="sxs-lookup"><span data-stu-id="3c830-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="3c830-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3c830-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a><span data-ttu-id="3c830-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c830-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c830-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c830-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c830-111">Слово в высоком порядке указывает расстояние, на которое вращается колесико, выраженное в множителях или множителях от наклона **колесика \_**, для которого задано значение 120.</span><span class="sxs-lookup"><span data-stu-id="3c830-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or factors of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="3c830-112">Положительное значение указывает, что колесо поворачивается вправо; отрицательное значение указывает, что колесико мыши было повернуто влево.</span><span class="sxs-lookup"><span data-stu-id="3c830-112">A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left.</span></span>

<span data-ttu-id="3c830-113">Слово низкого порядка показывает, не отключены ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="3c830-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="3c830-114">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3c830-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="3c830-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3c830-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="3c830-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3c830-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="3c830-117"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="3c830-118">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="3c830-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="3c830-119"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="3c830-120">Левая кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="3c830-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="3c830-121"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="3c830-122">Средняя кнопка мыши не работает.</span><span class="sxs-lookup"><span data-stu-id="3c830-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="3c830-123"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="3c830-124">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="3c830-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="3c830-125"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="3c830-126">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="3c830-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="3c830-127"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="3c830-128">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="3c830-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="3c830-129"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="3c830-130">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="3c830-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="3c830-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c830-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c830-132">Слово нижнего порядка задает координату по оси x указателя относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="3c830-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="3c830-133">Слово в высоком порядке Указывает координату y указателя относительно левого верхнего угла экрана.</span><span class="sxs-lookup"><span data-stu-id="3c830-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c830-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c830-134">Return value</span></span>

<span data-ttu-id="3c830-135">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3c830-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c830-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c830-136">Remarks</span></span>

<span data-ttu-id="3c830-137">Используйте следующий код для получения сведений в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="3c830-137">Use the following code to obtain the information in the *wParam* parameter.</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="3c830-138">Используйте следующий код, чтобы получить горизонтальное и вертикальное расположение.</span><span class="sxs-lookup"><span data-stu-id="3c830-138">Use the following code to obtain the horizontal and vertical position.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="3c830-139">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="3c830-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="3c830-140">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="3c830-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="3c830-141">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="3c830-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c830-142">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="3c830-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="3c830-143">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="3c830-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="3c830-144">Вращение колесика является кратным для **\_ разницы колеса**, для которой задано значение 120.</span><span class="sxs-lookup"><span data-stu-id="3c830-144">The wheel rotation is a multiple of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="3c830-145">Это пороговое значение для действия, которое необходимо выполнить, и одно из таких действий (например, прокрутка одного приращения) должно выполняться для каждой разностной разницы.</span><span class="sxs-lookup"><span data-stu-id="3c830-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="3c830-146">Дельта была задана как 120, чтобы позволить корпорации Майкрософт или другим поставщикам создавать колеса с более высоким разрешением (например, свободно вращающееся колесо, без выпусков) для отправки дополнительных сообщений на смену, но с меньшим значением в каждом сообщении.</span><span class="sxs-lookup"><span data-stu-id="3c830-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (for example, a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="3c830-147">Чтобы использовать эту функцию, можно добавить входящие разностные значения, пока не будет достигнуто значение наклона **колесика \_** (так что для сдвига изменений можно получить тот же ответ) или прокручивать частичные строки в ответ на более частые сообщения.</span><span class="sxs-lookup"><span data-stu-id="3c830-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to more frequent messages.</span></span> <span data-ttu-id="3c830-148">Можно также выбрать детализацию прокрутки и накапливать разности, пока она не будет достигнута.</span><span class="sxs-lookup"><span data-stu-id="3c830-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c830-149">Требования</span><span class="sxs-lookup"><span data-stu-id="3c830-149">Requirements</span></span>



| <span data-ttu-id="3c830-150">Требование</span><span class="sxs-lookup"><span data-stu-id="3c830-150">Requirement</span></span> | <span data-ttu-id="3c830-151">Значение</span><span class="sxs-lookup"><span data-stu-id="3c830-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c830-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c830-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3c830-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c830-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3c830-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c830-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3c830-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c830-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c830-156">Header</span><span class="sxs-lookup"><span data-stu-id="3c830-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c830-157"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c830-157"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c830-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c830-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c830-159">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="3c830-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3c830-160">**ПОЛУЧЕНИЕ \_ кэйстате \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="3c830-160">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="3c830-161">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="3c830-161">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="3c830-162">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="3c830-162">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="3c830-163">**ПОЛУЧИТЬ \_ \_ разностный \_ wParam для колеса**</span><span class="sxs-lookup"><span data-stu-id="3c830-163">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="3c830-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c830-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3c830-165">[**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c830-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3c830-166">**\_событие мыши**</span><span class="sxs-lookup"><span data-stu-id="3c830-166">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="3c830-167">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="3c830-167">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3c830-168">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="3c830-168">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="3c830-169">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="3c830-169">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="3c830-170">**жетсистемметрикс**</span><span class="sxs-lookup"><span data-stu-id="3c830-170">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="3c830-171">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="3c830-171">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="3c830-172">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3c830-172">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3c830-173">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="3c830-173">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

