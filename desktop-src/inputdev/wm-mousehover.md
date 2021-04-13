---
title: Сообщение WM_MOUSEHOVER (Winuser. h)
description: Отправляется в окно при наведении курсора на клиентскую область окна в течение периода времени, указанного в предыдущем вызове метода TrackMouseEven.
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- WM_MOUSEHOVER ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490038"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="24501-104">\_Сообщение МАУСЕХОВЕР WM</span><span class="sxs-lookup"><span data-stu-id="24501-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="24501-105">Отправляется в окно при наведении курсора на клиентскую область окна в течение периода времени, указанного в предыдущем вызове метода [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span><span class="sxs-lookup"><span data-stu-id="24501-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="24501-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="24501-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="24501-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="24501-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24501-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24501-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24501-109">Указывает, работают ли различные виртуальные ключи.</span><span class="sxs-lookup"><span data-stu-id="24501-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="24501-110">Этот параметр может принимать одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="24501-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="24501-111">Значение</span><span class="sxs-lookup"><span data-stu-id="24501-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="24501-112">Значение</span><span class="sxs-lookup"><span data-stu-id="24501-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="24501-113"><dt>**MK \_ Управление**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="24501-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="24501-114">Нажата клавиша CTRL.</span><span class="sxs-lookup"><span data-stu-id="24501-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="24501-115"><dt>**MK \_ ЛБУТТОН**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="24501-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="24501-116">Нажата левая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="24501-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="24501-117"><dt>**MK \_ МБУТТОН**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="24501-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="24501-118">Нажата средняя кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="24501-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="24501-119"><dt>**MK \_ РБУТТОН**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="24501-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="24501-120">Нажата правая кнопка мыши.</span><span class="sxs-lookup"><span data-stu-id="24501-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="24501-121"><dt>**MK \_ SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="24501-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="24501-122">Нажата клавиша SHIFT.</span><span class="sxs-lookup"><span data-stu-id="24501-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="24501-123"><dt>**MK \_ XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="24501-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="24501-124">Первая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="24501-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="24501-125"><dt>**MK \_ XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="24501-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="24501-126">Вторая кнопка X не работает.</span><span class="sxs-lookup"><span data-stu-id="24501-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="24501-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24501-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24501-128">Слово нижнего порядка Указывает координату x курсора.</span><span class="sxs-lookup"><span data-stu-id="24501-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="24501-129">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="24501-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="24501-130">Слово в высоком порядке Указывает координату y курсора.</span><span class="sxs-lookup"><span data-stu-id="24501-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="24501-131">Координата задается относительно левого верхнего угла клиентской области.</span><span class="sxs-lookup"><span data-stu-id="24501-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24501-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="24501-132">Return value</span></span>

<span data-ttu-id="24501-133">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="24501-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24501-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24501-134">Remarks</span></span>

<span data-ttu-id="24501-135">Отслеживание наведения при наведении останавливается при создании **\_ маусеховер WM** .</span><span class="sxs-lookup"><span data-stu-id="24501-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="24501-136">Приложение должно вызвать [**TrackMouseEven**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) еще раз, если требуется дальнейшее отслеживание поведения при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="24501-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="24501-137">Чтобы получить горизонтальное и вертикальное расположение, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="24501-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="24501-138">Как отмечалось выше, координата x находится в низком порядке в **коротком** значении возвращаемого значения; Координата y находится в **высоком порядке (** оба представляют значения *со знаком* , так как они могут принимать отрицательные значения в системах с несколькими мониторами).</span><span class="sxs-lookup"><span data-stu-id="24501-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="24501-139">Если возвращаемое значение присваивается переменной, можно использовать макрос [**макепоинтс**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) для получения структуры [**points**](/previous-versions//dd162808(v=vs.85)) из возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="24501-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="24501-140">Для извлечения координат x или y можно также использовать макрос [**Get \_ x \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) или [**Get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) .</span><span class="sxs-lookup"><span data-stu-id="24501-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24501-141">Не используйте макросы [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) или [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) для извлечения координат x и y позиции курсора, так как эти макросы возвращают неверные результаты в системах с несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="24501-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="24501-142">Системы с несколькими мониторами могут иметь отрицательные координаты x и y, а **ловорд** и **HIWORD** обрабатывают координаты как неподписанные количества.</span><span class="sxs-lookup"><span data-stu-id="24501-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24501-143">Требования</span><span class="sxs-lookup"><span data-stu-id="24501-143">Requirements</span></span>



| <span data-ttu-id="24501-144">Требование</span><span class="sxs-lookup"><span data-stu-id="24501-144">Requirement</span></span> | <span data-ttu-id="24501-145">Значение</span><span class="sxs-lookup"><span data-stu-id="24501-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24501-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24501-146">Minimum supported client</span></span><br/> | <span data-ttu-id="24501-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24501-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="24501-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24501-148">Minimum supported server</span></span><br/> | <span data-ttu-id="24501-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="24501-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="24501-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="24501-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="24501-151"><dt>Winuser. h (включение Виндовскс. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24501-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24501-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24501-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="24501-153">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="24501-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24501-154">**ПОЛУЧИТЬ \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="24501-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="24501-155">**ПОЛУЧИТЬ \_ lParam для Y \_**</span><span class="sxs-lookup"><span data-stu-id="24501-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="24501-156">**Захват**</span><span class="sxs-lookup"><span data-stu-id="24501-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="24501-157">**сеткаптуре**</span><span class="sxs-lookup"><span data-stu-id="24501-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="24501-158">**TrackMouseEven**</span><span class="sxs-lookup"><span data-stu-id="24501-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="24501-159">**TRACKMOUSEEVEN**</span><span class="sxs-lookup"><span data-stu-id="24501-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="24501-160">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="24501-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24501-161">Ввод с помощью мыши</span><span class="sxs-lookup"><span data-stu-id="24501-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="24501-162">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="24501-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="24501-163">**макепоинтс**</span><span class="sxs-lookup"><span data-stu-id="24501-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="24501-164">[**ТОЧКИ**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24501-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

