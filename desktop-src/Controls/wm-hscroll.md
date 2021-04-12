---
title: Сообщение WM_HSCROLL (Winuser. h)
description: Сообщение WM \_ HSCROLL отправляется в окно при возникновении события прокрутки в стандартной горизонтальной полосе прокрутки окна.
ms.assetid: 197e522f-defd-4356-8521-5b5dfda596da
keywords:
- Элементы управления Windows для WM_HSCROLL сообщений
topic_type:
- apiref
api_name:
- WM_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f26eec697e91ee8862912c0f93bcd6e8c4e5c56e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136394"
---
# <a name="wm_hscroll-message"></a><span data-ttu-id="10d31-104">\_Сообщение HSCROLL WM</span><span class="sxs-lookup"><span data-stu-id="10d31-104">WM\_HSCROLL message</span></span>

<span data-ttu-id="10d31-105">Сообщение **WM \_ HSCROLL** отправляется в окно при возникновении события прокрутки в стандартной горизонтальной полосе прокрутки окна.</span><span class="sxs-lookup"><span data-stu-id="10d31-105">The **WM\_HSCROLL** message is sent to a window when a scroll event occurs in the window's standard horizontal scroll bar.</span></span> <span data-ttu-id="10d31-106">Это сообщение также отправляется владельцу горизонтальной полосы прокрутки при возникновении события прокрутки в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="10d31-106">This message is also sent to the owner of a horizontal scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="10d31-107">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="10d31-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_HSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="10d31-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="10d31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d31-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="10d31-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10d31-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает текущее расположение поля прокрутки, если [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) является SB \_ сумбпоситион или SB \_ сумбтракк; в противном случае это слово не используется.</span><span class="sxs-lookup"><span data-stu-id="10d31-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="10d31-111">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает значение полосы прокрутки, которое указывает на запрос прокрутки пользователя.</span><span class="sxs-lookup"><span data-stu-id="10d31-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="10d31-112">Это слово может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="10d31-112">This word can be one of the following values.</span></span>



| <span data-ttu-id="10d31-113">Значение</span><span class="sxs-lookup"><span data-stu-id="10d31-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="10d31-114">Значение</span><span class="sxs-lookup"><span data-stu-id="10d31-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="10d31-115"><dt>**SB \_ ендскролл**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-115"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="10d31-116">Завершает прокрутку.</span><span class="sxs-lookup"><span data-stu-id="10d31-116">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <span data-ttu-id="10d31-117"><dt>**поsb, \_ слева**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-117"><dt>**SB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="10d31-118">Выполняет прокрутку к верхнему левому краю.</span><span class="sxs-lookup"><span data-stu-id="10d31-118">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <span data-ttu-id="10d31-119"><dt>**SB \_ right**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-119"><dt>**SB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="10d31-120">Прокручивает вниз до нижнего правого.</span><span class="sxs-lookup"><span data-stu-id="10d31-120">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <span data-ttu-id="10d31-121"><dt>**SB \_ линелефт**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-121"><dt>**SB\_LINELEFT**</dt></span></span> </dl>                | <span data-ttu-id="10d31-122">Прокрутка влево на одну единицу.</span><span class="sxs-lookup"><span data-stu-id="10d31-122">Scrolls left by one unit.</span></span><br/>                                                                                                                                                                                      |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <span data-ttu-id="10d31-123"><dt>**SB \_ линеригхт**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-123"><dt>**SB\_LINERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="10d31-124">Выполняет прокрутку вправо на одну единицу.</span><span class="sxs-lookup"><span data-stu-id="10d31-124">Scrolls right by one unit.</span></span><br/>                                                                                                                                                                                     |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <span data-ttu-id="10d31-125"><dt>**SB \_ пажелефт**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-125"><dt>**SB\_PAGELEFT**</dt></span></span> </dl>                | <span data-ttu-id="10d31-126">Прокрутка влево по ширине окна.</span><span class="sxs-lookup"><span data-stu-id="10d31-126">Scrolls left by the width of the window.</span></span><br/>                                                                                                                                                                       |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <span data-ttu-id="10d31-127"><dt>**SB \_ пажеригхт**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-127"><dt>**SB\_PAGERIGHT**</dt></span></span> </dl>             | <span data-ttu-id="10d31-128">Прокрутка вправо по ширине окна.</span><span class="sxs-lookup"><span data-stu-id="10d31-128">Scrolls right by the width of the window.</span></span><br/>                                                                                                                                                                      |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="10d31-129"><dt>**SB \_ сумбпоситион**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-129"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="10d31-130">Пользователь переместил бегунок (бегунок) и отпустил кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="10d31-130">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="10d31-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на позиции ползунка в конце операции перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="10d31-131">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="10d31-132"><dt>**SB \_ сумбтракк**</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-132"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="10d31-133">Пользователь перетаскивает полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="10d31-133">The user is dragging the scroll box.</span></span> <span data-ttu-id="10d31-134">Это сообщение отправляется повторно, пока пользователь не отпускает кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="10d31-134">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="10d31-135">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает на то, куда переместился ползунок полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="10d31-135">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="10d31-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10d31-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10d31-137">Если сообщение отправляется элементом управления "полоса прокрутки", этот параметр является маркером элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="10d31-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="10d31-138">Если сообщение отправляется стандартной полосой прокрутки, этот параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="10d31-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d31-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="10d31-139">Return value</span></span>

<span data-ttu-id="10d31-140">Если приложение обрабатывает это сообщение, оно должно вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="10d31-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="10d31-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10d31-141">Remarks</span></span>

<span data-ttu-id="10d31-142">\_Код запроса SB сумбтракк обычно используется приложениями, которые предоставляют отзыв по мере того, как пользователь перетаскивает ползунок.</span><span class="sxs-lookup"><span data-stu-id="10d31-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="10d31-143">Если приложение прокручивает содержимое окна, оно также должно сбрасывать в качестве значения поля прокрутки с помощью функции [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="10d31-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="10d31-144">Обратите внимание, что сообщение **WM \_ HSCROLL** содержит только 16 бит данных о положении поля прокрутки.</span><span class="sxs-lookup"><span data-stu-id="10d31-144">Note that the **WM\_HSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="10d31-145">Поэтому приложения, которые используют только **WM \_ HSCROLL** (и [**WM \_ VSCROLL**](wm-vscroll.md)) для данных о положении прокрутки, имеют практически максимальное значение 65 535.</span><span class="sxs-lookup"><span data-stu-id="10d31-145">Thus, applications that rely solely on **WM\_HSCROLL** (and [**WM\_VSCROLL**](wm-vscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="10d31-146">Однако, поскольку функции [**сетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**сетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**сетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**жетскроллинфо**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**жетскроллпос**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)и [**жетскроллранже**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) поддерживают 32-битные данные о положении полосы прокрутки, существует способ обойти 16-разрядное препятствие сообщений **WM \_ HSCROLL** и [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="10d31-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the **WM\_HSCROLL** and [**WM\_VSCROLL**](wm-vscroll.md) messages.</span></span> <span data-ttu-id="10d31-147">Описание метода см. в разделе **жетскроллинфо** .</span><span class="sxs-lookup"><span data-stu-id="10d31-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d31-148">Требования</span><span class="sxs-lookup"><span data-stu-id="10d31-148">Requirements</span></span>



| <span data-ttu-id="10d31-149">Требование</span><span class="sxs-lookup"><span data-stu-id="10d31-149">Requirement</span></span> | <span data-ttu-id="10d31-150">Значение</span><span class="sxs-lookup"><span data-stu-id="10d31-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d31-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10d31-151">Minimum supported client</span></span><br/> | <span data-ttu-id="10d31-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10d31-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="10d31-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10d31-153">Minimum supported server</span></span><br/> | <span data-ttu-id="10d31-154">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10d31-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="10d31-155">Header</span><span class="sxs-lookup"><span data-stu-id="10d31-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="10d31-156"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="10d31-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10d31-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10d31-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="10d31-158">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="10d31-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="10d31-159">**жетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="10d31-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="10d31-160">**жетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="10d31-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="10d31-161">**жетскроллранже**</span><span class="sxs-lookup"><span data-stu-id="10d31-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="10d31-162">**сетскроллинфо**</span><span class="sxs-lookup"><span data-stu-id="10d31-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="10d31-163">**сетскроллпос**</span><span class="sxs-lookup"><span data-stu-id="10d31-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="10d31-164">**сетскроллранже**</span><span class="sxs-lookup"><span data-stu-id="10d31-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="10d31-165">**WM \_ HSCROLL (TrackBar)**</span><span class="sxs-lookup"><span data-stu-id="10d31-165">**WM\_HSCROLL (trackbar)**</span></span>](wm-hscroll--trackbar-.md)
</dt> <dt>

[<span data-ttu-id="10d31-166">**WM \_ VSCROLL**</span><span class="sxs-lookup"><span data-stu-id="10d31-166">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

