---
title: Сообщение WM_CHAR (Winuser. h)
description: Отправляется в окно с фокусом клавиатуры, когда \_ сообщение WM KeyDown преобразуется функцией TranslateMessage. Сообщение WM \_ Char содержит код символа нажатой клавиши.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- WM_CHAR ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717917"
---
# <a name="wm_char-message"></a><span data-ttu-id="604e5-105">\_Сообщение WM char</span><span class="sxs-lookup"><span data-stu-id="604e5-105">WM\_CHAR message</span></span>

<span data-ttu-id="604e5-106">Отправляется в окно с фокусом клавиатуры, когда сообщение [**WM \_ KeyDown**](wm-keydown.md) преобразуется функцией [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="604e5-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="604e5-107">Сообщение **WM \_ char** содержит код символа нажатой клавиши.</span><span class="sxs-lookup"><span data-stu-id="604e5-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="604e5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="604e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="604e5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="604e5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="604e5-110">Код символа ключа.</span><span class="sxs-lookup"><span data-stu-id="604e5-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="604e5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="604e5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="604e5-112">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="604e5-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="604e5-113">Bits</span><span class="sxs-lookup"><span data-stu-id="604e5-113">Bits</span></span>  | <span data-ttu-id="604e5-114">Значение</span><span class="sxs-lookup"><span data-stu-id="604e5-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="604e5-115">0—15</span><span class="sxs-lookup"><span data-stu-id="604e5-115">0-15</span></span>  | <span data-ttu-id="604e5-116">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="604e5-116">The repeat count for the current message.</span></span> <span data-ttu-id="604e5-117">Значение — это число повторных попыток нажатия клавиши в результате, когда пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="604e5-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="604e5-118">Если нажатие клавиши удерживается достаточно долго, отправляется несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="604e5-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="604e5-119">Однако число повторов не является накопительным.</span><span class="sxs-lookup"><span data-stu-id="604e5-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="604e5-120">16—23</span><span class="sxs-lookup"><span data-stu-id="604e5-120">16-23</span></span> | <span data-ttu-id="604e5-121">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="604e5-121">The scan code.</span></span> <span data-ttu-id="604e5-122">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="604e5-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="604e5-123">24</span><span class="sxs-lookup"><span data-stu-id="604e5-123">24</span></span>    | <span data-ttu-id="604e5-124">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="604e5-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="604e5-125">Значение равно 1, если это расширенный ключ; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="604e5-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="604e5-126">25-28</span><span class="sxs-lookup"><span data-stu-id="604e5-126">25-28</span></span> | <span data-ttu-id="604e5-127">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="604e5-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="604e5-128">29</span><span class="sxs-lookup"><span data-stu-id="604e5-128">29</span></span>    | <span data-ttu-id="604e5-129">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="604e5-129">The context code.</span></span> <span data-ttu-id="604e5-130">Значение равно 1, если клавиша ALT удерживается при нажатии клавиши; в противном случае значение равно 0.</span><span class="sxs-lookup"><span data-stu-id="604e5-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="604e5-131">30</span><span class="sxs-lookup"><span data-stu-id="604e5-131">30</span></span>    | <span data-ttu-id="604e5-132">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="604e5-132">The previous key state.</span></span> <span data-ttu-id="604e5-133">Значение равно 1, если ключ не работает до отправки сообщения, или 0, если ключ работает.</span><span class="sxs-lookup"><span data-stu-id="604e5-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="604e5-134">31</span><span class="sxs-lookup"><span data-stu-id="604e5-134">31</span></span>    | <span data-ttu-id="604e5-135">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="604e5-135">The transition state.</span></span> <span data-ttu-id="604e5-136">Значение равно 1, если ключ освобождается, или 0, если клавиша нажата.</span><span class="sxs-lookup"><span data-stu-id="604e5-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="604e5-137">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="604e5-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="604e5-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="604e5-138">Return value</span></span>

<span data-ttu-id="604e5-139">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="604e5-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="604e5-140">Пример</span><span class="sxs-lookup"><span data-stu-id="604e5-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="604e5-141">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="604e5-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="604e5-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="604e5-142">Remarks</span></span>

<span data-ttu-id="604e5-143">В сообщении **WM \_ char** используется формат преобразования Юникода (UTF)-16.</span><span class="sxs-lookup"><span data-stu-id="604e5-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="604e5-144">Не обязательно однозначное соответствие между нажатием клавиш и сообщениями о символах, поэтому сведения в слове с высоким приоритетом параметра *lParam* обычно не используются для приложений.</span><span class="sxs-lookup"><span data-stu-id="604e5-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="604e5-145">Информация в слове высокого порядка применяется только к последнему сообщению [**WM \_ KeyDown**](wm-keydown.md) , которое предшествует отправке сообщения **WM \_ char** .</span><span class="sxs-lookup"><span data-stu-id="604e5-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="604e5-146">Для улучшенных клавиатуры с 101-и 102-клавишами расширенными ключами являются права ALT и right CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, конец, страница вверх, страница вниз и стрелка в кластерах слева от цифровой клавиатуры; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="604e5-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="604e5-147">Некоторые другие клавиатуры могут поддерживать бит расширенного ключа в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="604e5-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="604e5-148">Сообщение [**WM \_ уничар**](wm-unichar.md) такое же, как **WM \_ char**, за исключением того, что он использует UTF-32.</span><span class="sxs-lookup"><span data-stu-id="604e5-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="604e5-149">Она предназначена для отправки или публикации символов Юникода в окнах ANSI, а также для управления символами вспомогательной плоскости Юникода.</span><span class="sxs-lookup"><span data-stu-id="604e5-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="604e5-150">Требования</span><span class="sxs-lookup"><span data-stu-id="604e5-150">Requirements</span></span>



| <span data-ttu-id="604e5-151">Требование</span><span class="sxs-lookup"><span data-stu-id="604e5-151">Requirement</span></span> | <span data-ttu-id="604e5-152">Значение</span><span class="sxs-lookup"><span data-stu-id="604e5-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="604e5-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="604e5-153">Minimum supported client</span></span><br/> | <span data-ttu-id="604e5-154">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="604e5-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="604e5-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="604e5-155">Minimum supported server</span></span><br/> | <span data-ttu-id="604e5-156">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="604e5-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="604e5-157">Заголовок</span><span class="sxs-lookup"><span data-stu-id="604e5-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="604e5-158"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="604e5-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="604e5-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="604e5-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="604e5-160">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="604e5-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="604e5-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="604e5-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="604e5-162">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="604e5-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="604e5-163">**WM \_ уничар**</span><span class="sxs-lookup"><span data-stu-id="604e5-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="604e5-164">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="604e5-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="604e5-165">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="604e5-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

