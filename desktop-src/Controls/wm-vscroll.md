---
title: Сообщение WM_VSCROLL (Winuser. h)
description: Сообщение WM \_ VSCROLL отправляется в окно при возникновении события прокрутки в стандартной вертикальной полосе прокрутки окна.
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- Элементы управления Windows для WM_VSCROLL сообщений
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137547"
---
# <a name="wm_vscroll-message"></a><span data-ttu-id="abcc5-104">\_Сообщение VSCROLL WM</span><span class="sxs-lookup"><span data-stu-id="abcc5-104">WM\_VSCROLL message</span></span>

<span data-ttu-id="abcc5-105">Сообщение **WM \_ VSCROLL** отправляется в окно при возникновении события прокрутки в стандартной вертикальной полосе прокрутки окна.</span><span class="sxs-lookup"><span data-stu-id="abcc5-105">The **WM\_VSCROLL** message is sent to a window when a scroll event occurs in the window's standard vertical scroll bar.</span></span> <span data-ttu-id="abcc5-106">Это сообщение также отправляется владельцу вертикальной полосы прокрутки, когда в элементе управления возникает событие прокрутки.</span><span class="sxs-lookup"><span data-stu-id="abcc5-106">This message is also sent to the owner of a vertical scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="abcc5-107">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="abcc5-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="abcc5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="abcc5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abcc5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="abcc5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abcc5-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает текущее расположение поля прокрутки, если [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) является SB \_ сумбпоситион или SB \_ сумбтракк; в противном случае это слово не используется.</span><span class="sxs-lookup"><span data-stu-id="abcc5-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="abcc5-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает значение полосы прокрутки, которое указывает на запрос прокрутки пользователя.</span><span class="sxs-lookup"><span data-stu-id="abcc5-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="abcc5-112">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="abcc5-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="abcc5-113">Значение</span><span class="sxs-lookup"><span data-stu-id="abcc5-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="abcc5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="abcc5-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="abcc5-115"><dt>**SB \_ снизу**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-115"><dt>**SB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="abcc5-116">Прокручивает вниз до нижнего правого.</span><span class="sxs-lookup"><span data-stu-id="abcc5-116">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="abcc5-117"><dt>**SB \_ ендскролл**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-117"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="abcc5-118">Завершает прокрутку.</span><span class="sxs-lookup"><span data-stu-id="abcc5-118">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="abcc5-119"><dt>**SB \_ линедовн**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-119"><dt>**SB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="abcc5-120">Прокручивает по одной строке вниз.</span><span class="sxs-lookup"><span data-stu-id="abcc5-120">Scrolls one line down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="abcc5-121"><dt>**построителя \_**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-121"><dt>**SB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="abcc5-122">Выполняет прокрутку на одну строку вверх.</span><span class="sxs-lookup"><span data-stu-id="abcc5-122">Scrolls one line up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="abcc5-123"><dt>**SB \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-123"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="abcc5-124">Прокручивает одну страницу вниз.</span><span class="sxs-lookup"><span data-stu-id="abcc5-124">Scrolls one page down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="abcc5-125"><dt>**SB \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-125"><dt>**SB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="abcc5-126">Прокручивает на одну страницу вверх.</span><span class="sxs-lookup"><span data-stu-id="abcc5-126">Scrolls one page up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="abcc5-127"><dt>**SB \_ сумбпоситион**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-127"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="abcc5-128">Пользователь переместил бегунок (бегунок) и отпустил кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="abcc5-128">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="abcc5-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на позиции ползунка в конце операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="abcc5-129">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="abcc5-130"><dt>**SB \_ сумбтракк**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-130"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="abcc5-131">Пользователь перетаскивает полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="abcc5-131">The user is dragging the scroll box.</span></span> <span data-ttu-id="abcc5-132">Это сообщение отправляется повторно, пока пользователь не отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="abcc5-132">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="abcc5-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на то, куда переместился ползунок полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="abcc5-133">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="abcc5-134"><dt>**SB \_ сверху**</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-134"><dt>**SB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="abcc5-135">Выполняет прокрутку к верхнему левому краю.</span><span class="sxs-lookup"><span data-stu-id="abcc5-135">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="abcc5-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="abcc5-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="abcc5-137">Если сообщение отправляется элементом управления "полоса прокрутки", этот параметр является маркером элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="abcc5-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="abcc5-138">Если сообщение отправляется стандартной полосой прокрутки, этот параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="abcc5-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abcc5-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abcc5-139">Return value</span></span>

<span data-ttu-id="abcc5-140">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="abcc5-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="abcc5-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abcc5-141">Remarks</span></span>

<span data-ttu-id="abcc5-142">\_Код запроса SB сумбтракк обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.</span><span class="sxs-lookup"><span data-stu-id="abcc5-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="abcc5-143">Если приложение прокручивает содержимое окна, оно также должно сбрасывать в качестве значения поля прокрутки с помощью функции [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="abcc5-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="abcc5-144">Обратите внимание, что сообщение **WM \_ VSCROLL** содержит только 16 бит данных о положении поля прокрутки.</span><span class="sxs-lookup"><span data-stu-id="abcc5-144">Note that the **WM\_VSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="abcc5-145">Поэтому приложения, которые используют только **WM \_ VSCROLL** (и [**WM \_ HSCROLL**](wm-hscroll.md)) для данных о положении прокрутки, имеют практически максимальное значение 65 535.</span><span class="sxs-lookup"><span data-stu-id="abcc5-145">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="abcc5-146">Однако, поскольку функции [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**сетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**жетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)и [**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) поддерживают 32-битные данные о положении полосы прокрутки, существует способ обойти 16-разрядное препятствие сообщений [**WM \_ HSCROLL**](wm-hscroll.md) и **WM \_ VSCROLL** .</span><span class="sxs-lookup"><span data-stu-id="abcc5-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the [**WM\_HSCROLL**](wm-hscroll.md) and **WM\_VSCROLL** messages.</span></span> <span data-ttu-id="abcc5-147">Описание метода см. в разделе **жетскроллинфо** .</span><span class="sxs-lookup"><span data-stu-id="abcc5-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="abcc5-148">Требования</span><span class="sxs-lookup"><span data-stu-id="abcc5-148">Requirements</span></span>



| <span data-ttu-id="abcc5-149">Требование</span><span class="sxs-lookup"><span data-stu-id="abcc5-149">Requirement</span></span> | <span data-ttu-id="abcc5-150">Значение</span><span class="sxs-lookup"><span data-stu-id="abcc5-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abcc5-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="abcc5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="abcc5-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="abcc5-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="abcc5-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="abcc5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="abcc5-154">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="abcc5-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="abcc5-155">Header</span><span class="sxs-lookup"><span data-stu-id="abcc5-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="abcc5-156"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abcc5-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abcc5-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abcc5-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="abcc5-158">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="abcc5-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="abcc5-159">**жетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="abcc5-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="abcc5-160">**жетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="abcc5-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="abcc5-161">**жетскроллранже**</span><span class="sxs-lookup"><span data-stu-id="abcc5-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="abcc5-162">**сетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="abcc5-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="abcc5-163">**сетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="abcc5-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="abcc5-164">**сетскроллранже**</span><span class="sxs-lookup"><span data-stu-id="abcc5-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="abcc5-165">**WM \_ HSCROLL**</span><span class="sxs-lookup"><span data-stu-id="abcc5-165">**WM\_HSCROLL**</span></span>](wm-hscroll.md)
</dt> <dt>

[<span data-ttu-id="abcc5-166">**WM \_ VSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="abcc5-166">**WM\_VSCROLL (Trackbar)**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

