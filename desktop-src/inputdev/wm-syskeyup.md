---
title: Сообщение WM_SYSKEYUP (Winuser. h)
description: Передается в окно с фокусом клавиатуры, когда пользователь отпускает клавишу, которая была нажата во время удержания клавиши ALT.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352055"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="9bcce-104">\_Сообщение СИСКЭЙУП WM</span><span class="sxs-lookup"><span data-stu-id="9bcce-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="9bcce-105">Передается в окно с фокусом клавиатуры, когда пользователь отпускает клавишу, которая была нажата во время удержания клавиши ALT.</span><span class="sxs-lookup"><span data-stu-id="9bcce-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="9bcce-106">Это также происходит, когда ни один из окон в данный момент не имеет фокуса клавиатуры. в этом случае сообщение **WM \_ сискэйуп** отправляется в активное окно.</span><span class="sxs-lookup"><span data-stu-id="9bcce-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="9bcce-107">Окно, получающее сообщение, может различать эти контексты путем проверки кода контекста в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9bcce-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="9bcce-108">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9bcce-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="9bcce-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9bcce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcce-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bcce-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcce-111">Код виртуального ключа для освобожденного ключа.</span><span class="sxs-lookup"><span data-stu-id="9bcce-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="9bcce-112">См. раздел [**коды виртуальных клавиш**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9bcce-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="9bcce-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bcce-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcce-114">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9bcce-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="9bcce-115">Bits</span><span class="sxs-lookup"><span data-stu-id="9bcce-115">Bits</span></span>  | <span data-ttu-id="9bcce-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9bcce-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcce-117">0—15</span><span class="sxs-lookup"><span data-stu-id="9bcce-117">0-15</span></span>  | <span data-ttu-id="9bcce-118">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="9bcce-118">The repeat count for the current message.</span></span> <span data-ttu-id="9bcce-119">Значение — это число повторных попыток нажатия клавиши в результате, когда пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="9bcce-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="9bcce-120">Число повторов всегда равно единице для сообщения **WM \_ сискэйуп** .</span><span class="sxs-lookup"><span data-stu-id="9bcce-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="9bcce-121">16—23</span><span class="sxs-lookup"><span data-stu-id="9bcce-121">16-23</span></span> | <span data-ttu-id="9bcce-122">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="9bcce-122">The scan code.</span></span> <span data-ttu-id="9bcce-123">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="9bcce-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="9bcce-124">24</span><span class="sxs-lookup"><span data-stu-id="9bcce-124">24</span></span>    | <span data-ttu-id="9bcce-125">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="9bcce-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="9bcce-126">Значение равно 1, если это расширенный ключ; в противном случае он равен нулю.</span><span class="sxs-lookup"><span data-stu-id="9bcce-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="9bcce-127">25-28</span><span class="sxs-lookup"><span data-stu-id="9bcce-127">25-28</span></span> | <span data-ttu-id="9bcce-128">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="9bcce-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="9bcce-129">29</span><span class="sxs-lookup"><span data-stu-id="9bcce-129">29</span></span>    | <span data-ttu-id="9bcce-130">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="9bcce-130">The context code.</span></span> <span data-ttu-id="9bcce-131">Значение равно 1, если при отпускании клавиши клавиша ALT не нажата; он равен нулю, если сообщение **WM \_ сискэйуп** отправляется в активное окно, так как ни одно окно не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="9bcce-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="9bcce-132">30</span><span class="sxs-lookup"><span data-stu-id="9bcce-132">30</span></span>    | <span data-ttu-id="9bcce-133">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="9bcce-133">The previous key state.</span></span> <span data-ttu-id="9bcce-134">Значение всегда равно 1 для сообщения **WM \_ сискэйуп** .</span><span class="sxs-lookup"><span data-stu-id="9bcce-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="9bcce-135">31</span><span class="sxs-lookup"><span data-stu-id="9bcce-135">31</span></span>    | <span data-ttu-id="9bcce-136">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="9bcce-136">The transition state.</span></span> <span data-ttu-id="9bcce-137">Значение всегда равно 1 для сообщения **WM \_ сискэйуп** .</span><span class="sxs-lookup"><span data-stu-id="9bcce-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="9bcce-138">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="9bcce-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bcce-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9bcce-139">Return value</span></span>

<span data-ttu-id="9bcce-140">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="9bcce-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bcce-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9bcce-141">Remarks</span></span>

<span data-ttu-id="9bcce-142">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно верхнего уровня, если была снята клавиша F10 или ALT.</span><span class="sxs-lookup"><span data-stu-id="9bcce-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="9bcce-143">Параметр *wParam* сообщения имеет значение **SC \_ кэймену**.</span><span class="sxs-lookup"><span data-stu-id="9bcce-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="9bcce-144">Если код контекста равен нулю, сообщение может быть передано функции [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , которое будет обрабатывать его так, как будто оно было обычным ключевым сообщением, а не сообщением с символьным ключом.</span><span class="sxs-lookup"><span data-stu-id="9bcce-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="9bcce-145">Это позволяет использовать сочетания клавиш с активным окном, даже если активное окно не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="9bcce-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="9bcce-146">Для расширенных клавиш с 101 и 102, расширенными ключами являются сочетания клавиш ALT и CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, КОНЕЧная страница вверх, PAGE DOWN и стрелка в кластерах слева от цифровой клавиатуры; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="9bcce-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="9bcce-147">Другие клавиатуры могут поддерживать бит расширенного ключа в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="9bcce-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="9bcce-148">Для не-U. S. Улучшенная клавиатура с 102 клавиша, правая клавиша ALT обрабатываются как клавиши CTRL + ALT.</span><span class="sxs-lookup"><span data-stu-id="9bcce-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="9bcce-149">В следующей таблице показана последовательность сообщений, которые отображаются, когда пользователь нажимает и отпускает этот ключ.</span><span class="sxs-lookup"><span data-stu-id="9bcce-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="9bcce-150">Сообщение</span><span class="sxs-lookup"><span data-stu-id="9bcce-150">Message</span></span>                           | <span data-ttu-id="9bcce-151">Код виртуального ключа</span><span class="sxs-lookup"><span data-stu-id="9bcce-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="9bcce-152">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="9bcce-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="9bcce-153">**\_элемент управления VK**</span><span class="sxs-lookup"><span data-stu-id="9bcce-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="9bcce-154">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="9bcce-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="9bcce-155">**\_меню VK**</span><span class="sxs-lookup"><span data-stu-id="9bcce-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="9bcce-156">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="9bcce-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="9bcce-157">**\_элемент управления VK**</span><span class="sxs-lookup"><span data-stu-id="9bcce-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="9bcce-158">**WM \_ сискэйуп**</span><span class="sxs-lookup"><span data-stu-id="9bcce-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="9bcce-159">**\_меню VK**</span><span class="sxs-lookup"><span data-stu-id="9bcce-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="9bcce-160">Требования</span><span class="sxs-lookup"><span data-stu-id="9bcce-160">Requirements</span></span>



| <span data-ttu-id="9bcce-161">Требование</span><span class="sxs-lookup"><span data-stu-id="9bcce-161">Requirement</span></span> | <span data-ttu-id="9bcce-162">Значение</span><span class="sxs-lookup"><span data-stu-id="9bcce-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcce-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9bcce-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9bcce-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bcce-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9bcce-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9bcce-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9bcce-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9bcce-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9bcce-167">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9bcce-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bcce-168"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bcce-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcce-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9bcce-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="9bcce-170">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="9bcce-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9bcce-171">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="9bcce-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="9bcce-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="9bcce-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="9bcce-173">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="9bcce-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="9bcce-174">**WM \_ сискэйдовн**</span><span class="sxs-lookup"><span data-stu-id="9bcce-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="9bcce-175">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="9bcce-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9bcce-176">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="9bcce-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

