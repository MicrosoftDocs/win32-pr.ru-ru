---
title: Сообщение WM_UNICHAR (Winuser. h)
description: Сообщение WM \_ уничар может использоваться приложением для передачи входных данных в другие окна.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- WM_UNICHAR ввода сообщений с клавиатуры и мыши
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691844"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="19202-104">\_Сообщение УНИЧАР WM</span><span class="sxs-lookup"><span data-stu-id="19202-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="19202-105">Сообщение **WM \_ уничар** может использоваться приложением для передачи входных данных в другие окна.</span><span class="sxs-lookup"><span data-stu-id="19202-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="19202-106">Это сообщение содержит код символа нажатой клавиши.</span><span class="sxs-lookup"><span data-stu-id="19202-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="19202-107">(Проверьте, может ли целевое приложение обрабатывать сообщения **WM \_ уничар** , отправив сообщение с параметром *wParam* в **Unicode без \_ знака**.)</span><span class="sxs-lookup"><span data-stu-id="19202-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="19202-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="19202-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19202-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19202-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19202-110">Код символа ключа.</span><span class="sxs-lookup"><span data-stu-id="19202-110">The character code of the key.</span></span>

<span data-ttu-id="19202-111">Если параметр *wParam* имеет значение **Unicode No \_ char** и приложение обрабатывает это сообщение, возвращается **значение true**.</span><span class="sxs-lookup"><span data-stu-id="19202-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="19202-112">Функция [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) вернет **значение false** (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="19202-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="19202-113">Если аргумент *wParam* не является символом **Юникода \_**, возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="19202-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="19202-114">[**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) в Юникоде отправляет сообщение [**WM \_ char**](wm-char.md) с теми же параметрами, а функция **дефвиндовпрок** ANSI отправляет одно или два сообщения **WM \_ char** с соответствующими символами ANSI.</span><span class="sxs-lookup"><span data-stu-id="19202-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="19202-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19202-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19202-116">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="19202-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="19202-117">Bits</span><span class="sxs-lookup"><span data-stu-id="19202-117">Bits</span></span>  | <span data-ttu-id="19202-118">Значение</span><span class="sxs-lookup"><span data-stu-id="19202-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19202-119">0—15</span><span class="sxs-lookup"><span data-stu-id="19202-119">0-15</span></span>  | <span data-ttu-id="19202-120">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="19202-120">The repeat count for the current message.</span></span> <span data-ttu-id="19202-121">Значение — это число повторных попыток нажатия клавиши в результате, когда пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="19202-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="19202-122">Если нажатие клавиши удерживается достаточно долго, отправляется несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="19202-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="19202-123">Однако число повторов не является накопительным.</span><span class="sxs-lookup"><span data-stu-id="19202-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="19202-124">16—23</span><span class="sxs-lookup"><span data-stu-id="19202-124">16-23</span></span> | <span data-ttu-id="19202-125">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="19202-125">The scan code.</span></span> <span data-ttu-id="19202-126">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="19202-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="19202-127">24</span><span class="sxs-lookup"><span data-stu-id="19202-127">24</span></span>    | <span data-ttu-id="19202-128">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="19202-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="19202-129">Значение равно 1, если это расширенный ключ; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="19202-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="19202-130">25-28</span><span class="sxs-lookup"><span data-stu-id="19202-130">25-28</span></span> | <span data-ttu-id="19202-131">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="19202-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="19202-132">29</span><span class="sxs-lookup"><span data-stu-id="19202-132">29</span></span>    | <span data-ttu-id="19202-133">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="19202-133">The context code.</span></span> <span data-ttu-id="19202-134">Значение равно 1, если клавиша ALT удерживается при нажатии клавиши; в противном случае значение равно 0.</span><span class="sxs-lookup"><span data-stu-id="19202-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="19202-135">30</span><span class="sxs-lookup"><span data-stu-id="19202-135">30</span></span>    | <span data-ttu-id="19202-136">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="19202-136">The previous key state.</span></span> <span data-ttu-id="19202-137">Значение равно 1, если ключ не работает до отправки сообщения, или 0, если ключ работает.</span><span class="sxs-lookup"><span data-stu-id="19202-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="19202-138">31</span><span class="sxs-lookup"><span data-stu-id="19202-138">31</span></span>    | <span data-ttu-id="19202-139">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="19202-139">The transition state.</span></span> <span data-ttu-id="19202-140">Значение равно 1, если ключ освобождается, или 0, если клавиша нажата.</span><span class="sxs-lookup"><span data-stu-id="19202-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="19202-141">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="19202-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19202-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="19202-142">Return value</span></span>

<span data-ttu-id="19202-143">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="19202-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="19202-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19202-144">Remarks</span></span>

<span data-ttu-id="19202-145">Сообщение **WM \_ уничар** похоже на [**WM \_ char**](wm-char.md), но использует формат преобразования Юникода (UTF)-32, тогда как **WM \_ char** использует UTF-16.</span><span class="sxs-lookup"><span data-stu-id="19202-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="19202-146">Это сообщение предназначено для отправки или публикации символов Юникода в окнах ANSI и может работать с символами вспомогательной плоскости Юникода.</span><span class="sxs-lookup"><span data-stu-id="19202-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="19202-147">Так как не обязательно однозначное соответствие между нажатием клавиш и сообщениями о символах, сведения в слове с высоким приоритетом параметра *lParam* обычно не используются для приложений.</span><span class="sxs-lookup"><span data-stu-id="19202-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="19202-148">Информация в слове высокого порядка применяется только к последнему сообщению [**WM \_ KeyDown**](wm-keydown.md) , которое предшествует отправке сообщения **WM \_ уничар** .</span><span class="sxs-lookup"><span data-stu-id="19202-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="19202-149">Для улучшенных клавиатуры с 101-и 102-клавишами расширенными ключами являются права ALT и right CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, конец, страница вверх, страница вниз и стрелка в кластерах слева от цифровой клавиатуры; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="19202-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="19202-150">Некоторые другие клавиатуры могут поддерживать бит расширенного ключа в параметре *lParam* .</span><span class="sxs-lookup"><span data-stu-id="19202-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="19202-151">Требования</span><span class="sxs-lookup"><span data-stu-id="19202-151">Requirements</span></span>



| <span data-ttu-id="19202-152">Требование</span><span class="sxs-lookup"><span data-stu-id="19202-152">Requirement</span></span> | <span data-ttu-id="19202-153">Значение</span><span class="sxs-lookup"><span data-stu-id="19202-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19202-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19202-154">Minimum supported client</span></span><br/> | <span data-ttu-id="19202-155">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="19202-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="19202-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19202-156">Minimum supported server</span></span><br/> | <span data-ttu-id="19202-157">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="19202-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19202-158">Header</span><span class="sxs-lookup"><span data-stu-id="19202-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="19202-159"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19202-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19202-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19202-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="19202-161">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="19202-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19202-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="19202-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="19202-163">**WM \_ char**</span><span class="sxs-lookup"><span data-stu-id="19202-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="19202-164">**WM \_ KeyDown**</span><span class="sxs-lookup"><span data-stu-id="19202-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="19202-165">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="19202-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="19202-166">Ввод с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="19202-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

