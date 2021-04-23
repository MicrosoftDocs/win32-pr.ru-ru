---
title: Сообщение WM_CTLCOLORSCROLLBAR (Winuser. h)
description: Сообщение WM \_ ктлколорскроллбар отправляется в родительское окно элемента управления "полоса прокрутки", когда элемент управления собирается для рисования.
ms.assetid: 35832a23-96f1-42cb-a986-06726bf2a124
keywords:
- Элементы управления Windows для WM_CTLCOLORSCROLLBAR сообщений
topic_type:
- apiref
api_name:
- WM_CTLCOLORSCROLLBAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f8282e8e15bf1d1a668e1f57e17048f0babac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988591"
---
# <a name="wm_ctlcolorscrollbar-message"></a><span data-ttu-id="e7ba4-104">\_Сообщение КТЛКОЛОРСКРОЛЛБАР WM</span><span class="sxs-lookup"><span data-stu-id="e7ba4-104">WM\_CTLCOLORSCROLLBAR message</span></span>

<span data-ttu-id="e7ba4-105">Сообщение **WM \_ ктлколорскроллбар** отправляется в родительское окно элемента управления "полоса прокрутки", когда элемент управления собирается для рисования.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-105">The **WM\_CTLCOLORSCROLLBAR** message is sent to the parent window of a scroll bar control when the control is about to be drawn.</span></span> <span data-ttu-id="e7ba4-106">При ответе на это сообщение родительское окно может использовать маркер контекста отображения, чтобы задать цвет фона для элемента управления полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-106">By responding to this message, the parent window can use the display context handle to set the background color of the scroll bar control.</span></span>

<span data-ttu-id="e7ba4-107">Окно получает это сообщение через функцию [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7ba4-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_CTLCOLORSCROLLBAR

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e7ba4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7ba4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ba4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7ba4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ba4-110">Обработайте с контекстом устройства для элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="e7ba4-110">Handle to the device context for the scroll bar control.</span></span>

</dd> <dt>

<span data-ttu-id="e7ba4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7ba4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ba4-112">Маркер полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-112">Handle to the scroll bar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ba4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7ba4-113">Return value</span></span>

<span data-ttu-id="e7ba4-114">Если приложение обрабатывает это сообщение, оно должно вернуть дескриптор в кисть.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-114">If an application processes this message, it must return the handle to a brush.</span></span> <span data-ttu-id="e7ba4-115">Система использует кисть для рисования фона элемента управления полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-115">The system uses the brush to paint the background of the scroll bar control.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ba4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7ba4-116">Remarks</span></span>

<span data-ttu-id="e7ba4-117">Если приложение возвращает созданную кисть (например, с помощью функции [**креатесолидбруш**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) или [**креатебрушиндирект**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) ), приложение должно освободить кисть.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-117">If the application returns a brush that it created (for example, by using the [**CreateSolidBrush**](/windows/desktop/api/wingdi/nf-wingdi-createsolidbrush) or [**CreateBrushIndirect**](/windows/desktop/api/wingdi/nf-wingdi-createbrushindirect) function), the application must free the brush.</span></span> <span data-ttu-id="e7ba4-118">Если приложение возвращает системную кисть (например, которая была получена функцией [**жетстоккобжект**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) или [**жетсисколорбруш**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) ), приложению не нужно освобождать эту кисть.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-118">If the application returns a system brush (for example, one that was retrieved by the [**GetStockObject**](/windows/desktop/api/wingdi/nf-wingdi-getstockobject) or [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) function), the application does not need to free the brush.</span></span>

<span data-ttu-id="e7ba4-119">По умолчанию функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) выбирает системные цвета по умолчанию для элемента управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="e7ba4-119">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the scroll bar control.</span></span>

<span data-ttu-id="e7ba4-120">Сообщение **WM \_ ктлколорскроллбар** никогда не отправляется между потоками; оно отправляется только в том же потоке.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-120">The **WM\_CTLCOLORSCROLLBAR** message is never sent between threads; it is only sent within the same thread.</span></span>

<span data-ttu-id="e7ba4-121">Если процедура диалогового окна обрабатывает это сообщение, необходимо привести требуемое возвращаемое значение к типу **int \_ ptr** и вернуть значение напрямую.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-121">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="e7ba4-122">Если процедура диалогового окна возвращает **значение false**, выполняется обработка сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-122">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="e7ba4-123">\_Значение МСГРЕСУЛТ DWL, заданное функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-123">The DWL\_MSGRESULT value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

<span data-ttu-id="e7ba4-124">Сообщение **WM \_ ктлколорскроллбар** используется только дочерними элементами управления "полоса прокрутки".</span><span class="sxs-lookup"><span data-stu-id="e7ba4-124">The **WM\_CTLCOLORSCROLLBAR** message is used only by child scroll bar controls.</span></span> <span data-ttu-id="e7ba4-125">Полосы прокрутки, присоединенные к окну (WS \_ Scroll и WS \_ VSCROLL), не создают это сообщение.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-125">Scrollbars attached to a window (WS\_SCROLL and WS\_VSCROLL) do not generate this message.</span></span> <span data-ttu-id="e7ba4-126">Чтобы настроить внешний вид полос прокрутки, присоединенных к окну, используйте функции плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="e7ba4-126">To customize the appearance of scrollbars attached to a window, use the flat scroll bar functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ba4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e7ba4-127">Requirements</span></span>



| <span data-ttu-id="e7ba4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e7ba4-128">Requirement</span></span> | <span data-ttu-id="e7ba4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e7ba4-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ba4-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7ba4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ba4-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e7ba4-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e7ba4-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7ba4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ba4-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e7ba4-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7ba4-134">Header</span><span class="sxs-lookup"><span data-stu-id="e7ba4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ba4-135"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7ba4-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ba4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7ba4-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="e7ba4-137">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e7ba4-138">**WM \_ ктлколорбтн**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-138">**WM\_CTLCOLORBTN**</span></span>](wm-ctlcolorbtn.md)
</dt> <dt>

[<span data-ttu-id="e7ba4-139">**WM \_ ктлколоредит**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-139">**WM\_CTLCOLOREDIT**</span></span>](wm-ctlcoloredit.md)
</dt> <dt>

[<span data-ttu-id="e7ba4-140">**WM \_ ктлколорлистбокс**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-140">**WM\_CTLCOLORLISTBOX**</span></span>](wm-ctlcolorlistbox.md)
</dt> <dt>

[<span data-ttu-id="e7ba4-141">**WM \_ ктлколорстатик**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-141">**WM\_CTLCOLORSTATIC**</span></span>](wm-ctlcolorstatic.md)
</dt> <dt>

<span data-ttu-id="e7ba4-142">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e7ba4-143">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e7ba4-144">**реализепалетте**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-144">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="e7ba4-145">**селектпалетте**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-145">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="e7ba4-146">**WM \_ ктлколордлг**</span><span class="sxs-lookup"><span data-stu-id="e7ba4-146">**WM\_CTLCOLORDLG**</span></span>](/windows/desktop/dlgbox/wm-ctlcolordlg)
</dt> </dl>

 

