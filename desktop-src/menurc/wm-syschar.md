---
title: Сообщение WM_SYSCHAR (Winuser. h)
description: Отправляется в окно с фокусом клавиатуры, когда \_ сообщение WM сискэйдовн преобразуется функцией TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535546"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="a38f0-104">\_Сообщение СИСЧАР WM</span><span class="sxs-lookup"><span data-stu-id="a38f0-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="a38f0-105">Отправляется в окно с фокусом клавиатуры, когда сообщение [**WM \_ сискэйдовн**](/windows/desktop/inputdev/wm-syskeydown) преобразуется функцией [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) .</span><span class="sxs-lookup"><span data-stu-id="a38f0-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="a38f0-106">Он задает код символа системного символа, который нажат, когда клавиша ALT не работает.</span><span class="sxs-lookup"><span data-stu-id="a38f0-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="a38f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a38f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a38f0-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a38f0-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a38f0-109">Код символа раздела меню "окно".</span><span class="sxs-lookup"><span data-stu-id="a38f0-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="a38f0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a38f0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a38f0-111">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a38f0-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="a38f0-112">Bits</span><span class="sxs-lookup"><span data-stu-id="a38f0-112">Bits</span></span>                                                                             | <span data-ttu-id="a38f0-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a38f0-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a38f0-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="a38f0-115">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="a38f0-115">The repeat count for the current message.</span></span> <span data-ttu-id="a38f0-116">Значение — это число повторных нажатий клавиш, выполненных пользователем в результате нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="a38f0-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="a38f0-117">Если нажатие клавиши удерживается достаточно долго, отправляется несколько сообщений.</span><span class="sxs-lookup"><span data-stu-id="a38f0-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="a38f0-118">Однако число повторов не является накопительным.</span><span class="sxs-lookup"><span data-stu-id="a38f0-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="a38f0-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="a38f0-120">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="a38f0-120">The scan code.</span></span> <span data-ttu-id="a38f0-121">Это значение зависит от изготовителя оборудования (OEM).</span><span class="sxs-lookup"><span data-stu-id="a38f0-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a38f0-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="a38f0-123">Указывает, является ли ключ расширенным ключом, таким как правая клавиша ALT и CTRL, которые появляются на клавиатуре с 101 или 102.</span><span class="sxs-lookup"><span data-stu-id="a38f0-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="a38f0-124">Значение равно 1, если это расширенный ключ; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="a38f0-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a38f0-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="a38f0-126">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="a38f0-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="a38f0-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="a38f0-128">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="a38f0-128">The context code.</span></span> <span data-ttu-id="a38f0-129">Значение равно 1, если клавиша ALT удерживается при нажатии клавиши; в противном случае значение равно 0.</span><span class="sxs-lookup"><span data-stu-id="a38f0-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="a38f0-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="a38f0-131">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="a38f0-131">The previous key state.</span></span> <span data-ttu-id="a38f0-132">Значение равно 1, если ключ не работает до отправки сообщения, или 0, если ключ работает.</span><span class="sxs-lookup"><span data-stu-id="a38f0-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="a38f0-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="a38f0-134">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="a38f0-134">The transition state.</span></span> <span data-ttu-id="a38f0-135">Значение равно 1, если ключ освобождается, или 0, если клавиша нажата.</span><span class="sxs-lookup"><span data-stu-id="a38f0-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="a38f0-136">Дополнительные сведения см. в разделе [Флаги сообщения о нажатии клавиш](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="a38f0-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a38f0-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a38f0-137">Return value</span></span>

<span data-ttu-id="a38f0-138">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="a38f0-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a38f0-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a38f0-139">Remarks</span></span>

<span data-ttu-id="a38f0-140">Если код контекста равен нулю, сообщение может быть передано функции [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , которое будет обрабатывать его так, как если бы оно было стандартным, а не системным символьным сообщением.</span><span class="sxs-lookup"><span data-stu-id="a38f0-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="a38f0-141">Это позволяет использовать сочетания клавиш с активным окном, даже если активное окно не имеет фокуса клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="a38f0-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="a38f0-142">Для расширенных клавиш с 101 и 102, расширенными ключами являются сочетания клавиш ALT и CTRL в основном разделе клавиатуры. клавиши INS, DEL, ДОМАШНяя, конец, страница вверх, страница вниз и стрелка в кластерах слева от цифровой клавиатуры; Клавиша PRINT СКРН; ключ РАЗРЫВа; Клавиша NUMLOCK; и клавиши деления (/) и ENTER на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="a38f0-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="a38f0-143">Другие клавиатуры могут поддерживать бит расширенного ключа в параметре.</span><span class="sxs-lookup"><span data-stu-id="a38f0-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a38f0-144">Требования</span><span class="sxs-lookup"><span data-stu-id="a38f0-144">Requirements</span></span>



| <span data-ttu-id="a38f0-145">Требование</span><span class="sxs-lookup"><span data-stu-id="a38f0-145">Requirement</span></span> | <span data-ttu-id="a38f0-146">Значение</span><span class="sxs-lookup"><span data-stu-id="a38f0-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38f0-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a38f0-147">Minimum supported client</span></span><br/> | <span data-ttu-id="a38f0-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a38f0-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a38f0-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a38f0-149">Minimum supported server</span></span><br/> | <span data-ttu-id="a38f0-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a38f0-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a38f0-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a38f0-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="a38f0-152"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a38f0-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38f0-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a38f0-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="a38f0-154">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="a38f0-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a38f0-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="a38f0-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="a38f0-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="a38f0-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="a38f0-157">**WM \_ сискэйдовн**</span><span class="sxs-lookup"><span data-stu-id="a38f0-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="a38f0-158">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a38f0-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a38f0-159">Сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="a38f0-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

