---
title: Сообщение WM_KEYUP (Winuser. h)
description: Отправляется в окно с фокусом клавиатуры при освобождении несистемного ключа. Несистемный ключ — это ключ, который нажимается, когда клавиша ALT не нажата, или клавиша, которая нажата, когда окно имеет фокус клавиатуры.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- WM_KEYUP ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415293"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="fc72c-105">\_Сообщение с KEYUP</span><span class="sxs-lookup"><span data-stu-id="fc72c-105">WM\_KEYUP message</span></span>

<span data-ttu-id="fc72c-106">Отправляется в окно с фокусом клавиатуры при освобождении несистемного ключа.</span><span class="sxs-lookup"><span data-stu-id="fc72c-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="fc72c-107">Несистемный ключ — это ключ, который нажимается, когда клавиша ALT *не* нажата, или клавиша, которая нажата, когда окно имеет фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="fc72c-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="fc72c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc72c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc72c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc72c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc72c-110">Код виртуального ключа несистемного ключа.</span><span class="sxs-lookup"><span data-stu-id="fc72c-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="fc72c-111">См. раздел [коды виртуальных клавиш](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fc72c-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="fc72c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc72c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc72c-113">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="fc72c-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="fc72c-114">Bits</span><span class="sxs-lookup"><span data-stu-id="fc72c-114">Bits</span></span>  | <span data-ttu-id="fc72c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fc72c-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc72c-116">0—15</span><span class="sxs-lookup"><span data-stu-id="fc72c-116">0-15</span></span>  | <span data-ttu-id="fc72c-117">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="fc72c-117">The repeat count for the current message.</span></span> <span data-ttu-id="fc72c-118">Значение — это число повторных попыток нажатия клавиши в результате, когда пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="fc72c-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="fc72c-119">Число повторов всегда равно 1 для сообщения **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="fc72c-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="fc72c-120">16—23</span><span class="sxs-lookup"><span data-stu-id="fc72c-120">16-23</span></span> | <span data-ttu-id="fc72c-121">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="fc72c-121">The scan code.</span></span> <span data-ttu-id="fc72c-122">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="fc72c-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="fc72c-123">24</span><span class="sxs-lookup"><span data-stu-id="fc72c-123">24</span></span>    | <span data-ttu-id="fc72c-124">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="fc72c-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="fc72c-125">Значение равно 1, если это расширенный ключ; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="fc72c-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="fc72c-126">25-28</span><span class="sxs-lookup"><span data-stu-id="fc72c-126">25-28</span></span> | <span data-ttu-id="fc72c-127">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="fc72c-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="fc72c-128">29</span><span class="sxs-lookup"><span data-stu-id="fc72c-128">29</span></span>    | <span data-ttu-id="fc72c-129">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="fc72c-129">The context code.</span></span> <span data-ttu-id="fc72c-130">Значение всегда равно 0 для сообщения **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="fc72c-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="fc72c-131">30</span><span class="sxs-lookup"><span data-stu-id="fc72c-131">30</span></span>    | <span data-ttu-id="fc72c-132">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="fc72c-132">The previous key state.</span></span> <span data-ttu-id="fc72c-133">Значение всегда равно 1 для сообщения **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="fc72c-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="fc72c-134">31</span><span class="sxs-lookup"><span data-stu-id="fc72c-134">31</span></span>    | <span data-ttu-id="fc72c-135">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="fc72c-135">The transition state.</span></span> <span data-ttu-id="fc72c-136">Значение всегда равно 1 для сообщения **WM \_ KEYUP** .</span><span class="sxs-lookup"><span data-stu-id="fc72c-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="fc72c-137">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="fc72c-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc72c-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc72c-138">Return value</span></span>

<span data-ttu-id="fc72c-139">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="fc72c-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc72c-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc72c-140">Remarks</span></span>

<span data-ttu-id="fc72c-141">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно верхнего уровня, если была снята клавиша F10 или ALT.</span><span class="sxs-lookup"><span data-stu-id="fc72c-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="fc72c-142">Параметр *wParam* сообщения имеет значение SC \_ кэймену.</span><span class="sxs-lookup"><span data-stu-id="fc72c-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="fc72c-143">Для расширенных клавиш с 101 и 102, расширенными ключами являются сочетания клавиш ALT и CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, КОНЕЧная страница вверх, PAGE DOWN и стрелка в кластерах слева от цифровой клавиатуры; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="fc72c-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="fc72c-144">Другие клавиатуры могут поддерживать бит расширенного ключа в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="fc72c-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="fc72c-145">Приложения должны передавать *wParam* в [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , не изменяя его вообще.</span><span class="sxs-lookup"><span data-stu-id="fc72c-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc72c-146">Требования</span><span class="sxs-lookup"><span data-stu-id="fc72c-146">Requirements</span></span>



| <span data-ttu-id="fc72c-147">Требование</span><span class="sxs-lookup"><span data-stu-id="fc72c-147">Requirement</span></span> | <span data-ttu-id="fc72c-148">Значение</span><span class="sxs-lookup"><span data-stu-id="fc72c-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc72c-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc72c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fc72c-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc72c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fc72c-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc72c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fc72c-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc72c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc72c-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc72c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc72c-154"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc72c-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc72c-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc72c-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc72c-156">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="fc72c-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fc72c-157">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="fc72c-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="fc72c-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="fc72c-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="fc72c-159">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="fc72c-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="fc72c-160">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="fc72c-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="fc72c-161">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="fc72c-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fc72c-162">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="fc72c-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

