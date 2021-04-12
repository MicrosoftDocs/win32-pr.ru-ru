---
description: Отправляется в приложение, когда редактор IME возвращает символ результата преобразования. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Сообщение WM_IME_CHAR (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424045"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="d88f7-104">\_Сообщение IME редактора WM \_</span><span class="sxs-lookup"><span data-stu-id="d88f7-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="d88f7-105">Отправляется в приложение, когда редактор IME возвращает символ результата преобразования.</span><span class="sxs-lookup"><span data-stu-id="d88f7-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="d88f7-106">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d88f7-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="d88f7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d88f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88f7-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d88f7-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d88f7-109">Маркер для окна.</span><span class="sxs-lookup"><span data-stu-id="d88f7-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="d88f7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d88f7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d88f7-111">**DBCS:** Однобайтовое или двойное значение символа.</span><span class="sxs-lookup"><span data-stu-id="d88f7-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="d88f7-112">Для двухбайтовых символов (BYTE) (wParam >> 8) содержит старший байт.</span><span class="sxs-lookup"><span data-stu-id="d88f7-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="d88f7-113">Обратите внимание, что круглые скобки необходимы, поскольку оператор CAST имеет более высокий приоритет, чем оператор сдвига.</span><span class="sxs-lookup"><span data-stu-id="d88f7-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="d88f7-114">**Юникод:** Значение символа Юникода.</span><span class="sxs-lookup"><span data-stu-id="d88f7-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="d88f7-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d88f7-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d88f7-116">Число повторов, код сканирования, флаг расширенного ключа, код контекста, флаг предыдущего состояния ключа и флаг состояния перехода со значениями, указанными ниже.</span><span class="sxs-lookup"><span data-stu-id="d88f7-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="d88f7-117">bit</span><span class="sxs-lookup"><span data-stu-id="d88f7-117">Bit</span></span>   | <span data-ttu-id="d88f7-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d88f7-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d88f7-119">0—15</span><span class="sxs-lookup"><span data-stu-id="d88f7-119">0-15</span></span>  | <span data-ttu-id="d88f7-120">Число повторов.</span><span class="sxs-lookup"><span data-stu-id="d88f7-120">Repeat count.</span></span> <span data-ttu-id="d88f7-121">Поскольку первый байт и второй байт непрерывны, это всегда 1.</span><span class="sxs-lookup"><span data-stu-id="d88f7-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="d88f7-122">16—23</span><span class="sxs-lookup"><span data-stu-id="d88f7-122">16-23</span></span> | <span data-ttu-id="d88f7-123">Код проверки для полного азиатского символа.</span><span class="sxs-lookup"><span data-stu-id="d88f7-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="d88f7-124">24</span><span class="sxs-lookup"><span data-stu-id="d88f7-124">24</span></span>    | <span data-ttu-id="d88f7-125">Расширенный ключ.</span><span class="sxs-lookup"><span data-stu-id="d88f7-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="d88f7-126">25-28</span><span class="sxs-lookup"><span data-stu-id="d88f7-126">25-28</span></span> | <span data-ttu-id="d88f7-127">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d88f7-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="d88f7-128">29</span><span class="sxs-lookup"><span data-stu-id="d88f7-128">29</span></span>    | <span data-ttu-id="d88f7-129">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="d88f7-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="d88f7-130">30</span><span class="sxs-lookup"><span data-stu-id="d88f7-130">30</span></span>    | <span data-ttu-id="d88f7-131">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="d88f7-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="d88f7-132">31</span><span class="sxs-lookup"><span data-stu-id="d88f7-132">31</span></span>    | <span data-ttu-id="d88f7-133">Переходное состояние.</span><span class="sxs-lookup"><span data-stu-id="d88f7-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d88f7-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d88f7-134">Remarks</span></span>

<span data-ttu-id="d88f7-135">В отличие от сообщения [**WM \_ char**](../inputdev/wm-char.md) для окна, не поддерживающего Юникод, это сообщение может содержать двухбайтовые и однобайтовые значения.</span><span class="sxs-lookup"><span data-stu-id="d88f7-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="d88f7-136">Для окна Юникода это сообщение будет таким же, как WM \_ char.</span><span class="sxs-lookup"><span data-stu-id="d88f7-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="d88f7-137">Если в окне, не поддерживающем Юникод, в \_ сообщении IME редактора WM \_ содержится двухбайтовый символ, а приложение передает это сообщение в [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), IME преобразует это сообщение в два \_ сообщения WM char, каждый из которых содержит один байт двухбайтовых символов.</span><span class="sxs-lookup"><span data-stu-id="d88f7-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="d88f7-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d88f7-138">Requirements</span></span>



| <span data-ttu-id="d88f7-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d88f7-139">Requirement</span></span> | <span data-ttu-id="d88f7-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d88f7-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88f7-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d88f7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d88f7-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d88f7-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d88f7-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d88f7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d88f7-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d88f7-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d88f7-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d88f7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88f7-146"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d88f7-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88f7-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d88f7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88f7-148">Диспетчер метода ввода</span><span class="sxs-lookup"><span data-stu-id="d88f7-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="d88f7-149">Сообщения диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="d88f7-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
