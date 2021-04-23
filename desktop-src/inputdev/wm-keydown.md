---
title: Сообщение WM_KEYDOWN (Winuser. h)
description: Отправляется в окно с фокусом клавиатуры при нажатии несистемного ключа. Несистемный ключ — это ключ, который нажимается, когда клавиша ALT не нажата.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699113"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="69bf5-105">\_Сообщение WM KeyDown</span><span class="sxs-lookup"><span data-stu-id="69bf5-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="69bf5-106">Отправляется в окно с фокусом клавиатуры при нажатии несистемного ключа.</span><span class="sxs-lookup"><span data-stu-id="69bf5-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="69bf5-107">Несистемный ключ — это ключ, который нажимается, когда клавиша ALT не нажата.</span><span class="sxs-lookup"><span data-stu-id="69bf5-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="69bf5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="69bf5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69bf5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="69bf5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf5-110">Код виртуального ключа несистемного ключа.</span><span class="sxs-lookup"><span data-stu-id="69bf5-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="69bf5-111">См. раздел [коды виртуальных клавиш](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="69bf5-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="69bf5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="69bf5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="69bf5-113">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="69bf5-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="69bf5-114">Bits</span><span class="sxs-lookup"><span data-stu-id="69bf5-114">Bits</span></span>  | <span data-ttu-id="69bf5-115">Значение</span><span class="sxs-lookup"><span data-stu-id="69bf5-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bf5-116">0—15</span><span class="sxs-lookup"><span data-stu-id="69bf5-116">0-15</span></span>  | <span data-ttu-id="69bf5-117">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="69bf5-117">The repeat count for the current message.</span></span> <span data-ttu-id="69bf5-118">Значение — это число повторных попыток нажатия клавиши в результате, когда пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="69bf5-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="69bf5-119">Если нажатие клавиши удерживается достаточно долго, отправляется несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="69bf5-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="69bf5-120">Однако число повторов не является накопительным.</span><span class="sxs-lookup"><span data-stu-id="69bf5-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="69bf5-121">16—23</span><span class="sxs-lookup"><span data-stu-id="69bf5-121">16-23</span></span> | <span data-ttu-id="69bf5-122">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="69bf5-122">The scan code.</span></span> <span data-ttu-id="69bf5-123">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="69bf5-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="69bf5-124">24</span><span class="sxs-lookup"><span data-stu-id="69bf5-124">24</span></span>    | <span data-ttu-id="69bf5-125">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="69bf5-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="69bf5-126">Значение равно 1, если это расширенный ключ; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="69bf5-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="69bf5-127">25-28</span><span class="sxs-lookup"><span data-stu-id="69bf5-127">25-28</span></span> | <span data-ttu-id="69bf5-128">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="69bf5-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="69bf5-129">29</span><span class="sxs-lookup"><span data-stu-id="69bf5-129">29</span></span>    | <span data-ttu-id="69bf5-130">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="69bf5-130">The context code.</span></span> <span data-ttu-id="69bf5-131">Значение всегда равно 0 для сообщения **WM \_ KeyDown** .</span><span class="sxs-lookup"><span data-stu-id="69bf5-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="69bf5-132">30</span><span class="sxs-lookup"><span data-stu-id="69bf5-132">30</span></span>    | <span data-ttu-id="69bf5-133">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="69bf5-133">The previous key state.</span></span> <span data-ttu-id="69bf5-134">Значение равно 1, если ключ не работает до отправки сообщения, или равен нулю, если ключ работает.</span><span class="sxs-lookup"><span data-stu-id="69bf5-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="69bf5-135">31</span><span class="sxs-lookup"><span data-stu-id="69bf5-135">31</span></span>    | <span data-ttu-id="69bf5-136">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="69bf5-136">The transition state.</span></span> <span data-ttu-id="69bf5-137">Значение всегда равно 0 для сообщения **WM \_ KeyDown** .</span><span class="sxs-lookup"><span data-stu-id="69bf5-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="69bf5-138">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="69bf5-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69bf5-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="69bf5-139">Return value</span></span>

<span data-ttu-id="69bf5-140">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="69bf5-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="69bf5-141">Пример</span><span class="sxs-lookup"><span data-stu-id="69bf5-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="69bf5-142">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="69bf5-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="69bf5-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="69bf5-143">Remarks</span></span>

<span data-ttu-id="69bf5-144">Если нажата клавиша F10, функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) устанавливает внутренний флаг.</span><span class="sxs-lookup"><span data-stu-id="69bf5-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="69bf5-145">Когда **дефвиндовпрок** получает сообщение [**WM \_ KEYUP**](wm-keyup.md) , функция проверяет, установлен ли внутренний флаг, и, если это так, отправляет сообщение [**WM \_ сискомманд**](/windows/desktop/menurc/wm-syscommand) в окно верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="69bf5-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="69bf5-146">Параметр **WM \_ сискомманд** сообщения имеет значение SC \_ кэймену.</span><span class="sxs-lookup"><span data-stu-id="69bf5-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="69bf5-147">Из-за функции автоповтора может быть отправлено более одного сообщения **WM \_ KeyDown** , прежде чем будет отправлено сообщение [**WM \_ KEYUP**](wm-keyup.md) .</span><span class="sxs-lookup"><span data-stu-id="69bf5-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="69bf5-148">Предыдущее состояние ключа (бит 30) можно использовать, чтобы определить, указывает ли сообщение **WM \_ KeyDown** на первый переход или повторный переход.</span><span class="sxs-lookup"><span data-stu-id="69bf5-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="69bf5-149">Для расширенных клавиш с 101 и 102, расширенными ключами являются сочетания клавиш ALT и CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, КОНЕЧная страница вверх, PAGE DOWN и стрелка в кластерах слева от цифровой клавиатуры; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="69bf5-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="69bf5-150">Другие клавиатуры могут поддерживать бит расширенного ключа в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="69bf5-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="69bf5-151">Приложения должны передавать *wParam* в [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , не изменяя его вообще.</span><span class="sxs-lookup"><span data-stu-id="69bf5-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="69bf5-152">Требования</span><span class="sxs-lookup"><span data-stu-id="69bf5-152">Requirements</span></span>



| <span data-ttu-id="69bf5-153">Требование</span><span class="sxs-lookup"><span data-stu-id="69bf5-153">Requirement</span></span> | <span data-ttu-id="69bf5-154">Значение</span><span class="sxs-lookup"><span data-stu-id="69bf5-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bf5-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="69bf5-155">Minimum supported client</span></span><br/> | <span data-ttu-id="69bf5-156">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69bf5-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="69bf5-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="69bf5-157">Minimum supported server</span></span><br/> | <span data-ttu-id="69bf5-158">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="69bf5-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="69bf5-159">Заголовок</span><span class="sxs-lookup"><span data-stu-id="69bf5-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="69bf5-160"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="69bf5-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69bf5-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="69bf5-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="69bf5-162">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="69bf5-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="69bf5-163">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="69bf5-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="69bf5-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="69bf5-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="69bf5-165">**WM \_ char**</span><span class="sxs-lookup"><span data-stu-id="69bf5-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="69bf5-166">**WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="69bf5-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="69bf5-167">**WM \_ сискомманд**</span><span class="sxs-lookup"><span data-stu-id="69bf5-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="69bf5-168">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="69bf5-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="69bf5-169">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="69bf5-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

