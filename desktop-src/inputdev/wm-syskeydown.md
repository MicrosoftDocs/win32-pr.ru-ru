---
title: Сообщение WM_SYSKEYDOWN (Winuser. h)
description: Отправляется в окно с фокусом клавиатуры, когда пользователь нажимает клавишу F10 (активирует строку меню) или удерживает клавишу ALT, а затем нажимает другой ключ.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691845"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="f5a5f-104">\_Сообщение СИСКЭЙДОВН WM</span><span class="sxs-lookup"><span data-stu-id="f5a5f-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="f5a5f-105">Отправляется в окно с фокусом клавиатуры, когда пользователь нажимает клавишу F10 (активирует строку меню) или удерживает клавишу ALT, а затем нажимает другой ключ.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="f5a5f-106">Это также происходит, когда ни один из окон в данный момент не имеет фокуса клавиатуры. в этом случае сообщение **WM \_ сискэйдовн** отправляется в активное окно.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="f5a5f-107">Окно, получающее сообщение, может различать эти контексты путем проверки кода контекста в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f5a5f-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="f5a5f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5a5f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a5f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5a5f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a5f-110">Код виртуального ключа нажатой клавиши.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="f5a5f-111">См. раздел [**коды виртуальных клавиш**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f5a5f-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5a5f-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5a5f-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a5f-113">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="f5a5f-114">Bits</span><span class="sxs-lookup"><span data-stu-id="f5a5f-114">Bits</span></span>  | <span data-ttu-id="f5a5f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f5a5f-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a5f-116">0—15</span><span class="sxs-lookup"><span data-stu-id="f5a5f-116">0-15</span></span>  | <span data-ttu-id="f5a5f-117">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-117">The repeat count for the current message.</span></span> <span data-ttu-id="f5a5f-118">Значение — это число повторных попыток нажатия клавиши в результате, когда пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="f5a5f-119">Если нажатие клавиши удерживается достаточно долго, отправляется несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="f5a5f-120">Однако число повторов не является накопительным.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="f5a5f-121">16—23</span><span class="sxs-lookup"><span data-stu-id="f5a5f-121">16-23</span></span> | <span data-ttu-id="f5a5f-122">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-122">The scan code.</span></span> <span data-ttu-id="f5a5f-123">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="f5a5f-124">24</span><span class="sxs-lookup"><span data-stu-id="f5a5f-124">24</span></span>    | <span data-ttu-id="f5a5f-125">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="f5a5f-126">Значение равно 1, если это расширенный ключ; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="f5a5f-127">25-28</span><span class="sxs-lookup"><span data-stu-id="f5a5f-127">25-28</span></span> | <span data-ttu-id="f5a5f-128">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f5a5f-129">29</span><span class="sxs-lookup"><span data-stu-id="f5a5f-129">29</span></span>    | <span data-ttu-id="f5a5f-130">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-130">The context code.</span></span> <span data-ttu-id="f5a5f-131">Значение равно 1, если при нажатии клавиши ALT клавиша SHIFT не нажата. он равен 0, если сообщение **WM \_ сискэйдовн** отправляется в активное окно, так как ни одно окно не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="f5a5f-132">30</span><span class="sxs-lookup"><span data-stu-id="f5a5f-132">30</span></span>    | <span data-ttu-id="f5a5f-133">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-133">The previous key state.</span></span> <span data-ttu-id="f5a5f-134">Значение равно 1, если ключ не работает до отправки сообщения, или 0, если ключ работает.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="f5a5f-135">31</span><span class="sxs-lookup"><span data-stu-id="f5a5f-135">31</span></span>    | <span data-ttu-id="f5a5f-136">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-136">The transition state.</span></span> <span data-ttu-id="f5a5f-137">Значение всегда равно 0 для сообщения **WM \_ сискэйдовн** .</span><span class="sxs-lookup"><span data-stu-id="f5a5f-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="f5a5f-138">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="f5a5f-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a5f-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5a5f-139">Return value</span></span>

<span data-ttu-id="f5a5f-140">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a5f-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5a5f-141">Remarks</span></span>

<span data-ttu-id="f5a5f-142">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) проверяет указанный ключ и создает сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) , если ключ является либо TAB, либо Enter.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="f5a5f-143">Если код контекста равен нулю, сообщение может быть передано функции [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , которое будет обрабатывать его так, как будто оно было обычным ключевым сообщением, а не сообщением с символьным ключом.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="f5a5f-144">Это позволяет использовать сочетания клавиш с активным окном, даже если активное окно не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="f5a5f-145">Из-за автоматической повторной операции может произойти несколько сообщений **\_ сискэйдовн WM** , прежде чем будет отправлено сообщение [**\_ сискэйуп WM**](wm-syskeyup.md) .</span><span class="sxs-lookup"><span data-stu-id="f5a5f-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="f5a5f-146">Предыдущее состояние ключа (бит 30) можно использовать для определения того, указывает ли сообщение **WM \_ сискэйдовн** на первый переход или повторный переход.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="f5a5f-147">Для расширенных клавиш с 101 и 102, расширенными ключами являются сочетания клавиш ALT и CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, КОНЕЧная страница вверх, PAGE DOWN и стрелка в кластерах слева от цифровой клавиатуры; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="f5a5f-148">Другие клавиатуры могут поддерживать бит расширенного ключа в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f5a5f-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="f5a5f-149">Это сообщение также отправляется каждый раз, когда пользователь нажимает клавишу F10 без клавиши ALT.</span><span class="sxs-lookup"><span data-stu-id="f5a5f-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a5f-150">Требования</span><span class="sxs-lookup"><span data-stu-id="f5a5f-150">Requirements</span></span>



| <span data-ttu-id="f5a5f-151">Требование</span><span class="sxs-lookup"><span data-stu-id="f5a5f-151">Requirement</span></span> | <span data-ttu-id="f5a5f-152">Значение</span><span class="sxs-lookup"><span data-stu-id="f5a5f-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a5f-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5a5f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a5f-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5a5f-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f5a5f-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5a5f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a5f-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f5a5f-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5a5f-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f5a5f-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a5f-158"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a5f-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a5f-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5a5f-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5a5f-160">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="f5a5f-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5a5f-161">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="f5a5f-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f5a5f-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="f5a5f-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="f5a5f-163">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="f5a5f-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="f5a5f-164">**WM \_ сискэйуп**</span><span class="sxs-lookup"><span data-stu-id="f5a5f-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="f5a5f-165">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="f5a5f-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5a5f-166">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="f5a5f-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

