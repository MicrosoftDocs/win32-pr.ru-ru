---
UID: ''
title: Функция обратного вызова Кэйбоардпрок
description: Система вызывает эту функцию, которая получает функцию сообщения, и для обработки существует сообщение клавиатуры.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "105661685"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="ede64-103">Функция Кэйбоардпрок</span><span class="sxs-lookup"><span data-stu-id="ede64-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="ede64-104">Описание</span><span class="sxs-lookup"><span data-stu-id="ede64-104">Description</span></span>

<span data-ttu-id="ede64-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="ede64-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="ede64-106">Система вызывает эту функцию всякий раз, когда приложение вызывает функцию [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) [или сообщение](/windows/desktop/api/winuser/nf-winuser-getmessage) клавиатуры ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) или [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) для обработки.</span><span class="sxs-lookup"><span data-stu-id="ede64-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="ede64-107">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ede64-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="ede64-108">**Кэйбоардпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="ede64-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="ede64-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ede64-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="ede64-110">код [в]</span><span class="sxs-lookup"><span data-stu-id="ede64-110">code [in]</span></span>

<span data-ttu-id="ede64-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="ede64-111">Type: **int**</span></span>

<span data-ttu-id="ede64-112">Код, используемый процедурой-обработчиком для определения способа обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ede64-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="ede64-113">Если *код* меньше нуля, процедура обработчика должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="ede64-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="ede64-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="ede64-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="ede64-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ede64-115">Value</span></span> | <span data-ttu-id="ede64-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ede64-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="ede64-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="ede64-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="ede64-118">Параметры *wParam* и *lParam* содержат сведения о сообщении о нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="ede64-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="ede64-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="ede64-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="ede64-120">Параметры *wParam* и *lParam* содержат сведения о сообщении о нажатии клавиши, а сообщение о нажатии клавиши не было удалено из очереди сообщений.</span><span class="sxs-lookup"><span data-stu-id="ede64-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="ede64-121">(Приложение, именуемое функцией **PeekMessage** , с указанием флага **PM_NOREMOVE** .)</span><span class="sxs-lookup"><span data-stu-id="ede64-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="ede64-122">wParam [вход]</span><span class="sxs-lookup"><span data-stu-id="ede64-122">wParam [in]</span></span>

<span data-ttu-id="ede64-123">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="ede64-123">Type: **WPARAM**</span></span>

<span data-ttu-id="ede64-124">[Код виртуального ключа](/windows/desktop/inputdev/virtual-key-codes) для ключа, создавшего сообщение о нажатии клавиши.</span><span class="sxs-lookup"><span data-stu-id="ede64-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="ede64-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="ede64-125">lParam [in]</span></span>

<span data-ttu-id="ede64-126">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="ede64-126">Type: **LPARAM**</span></span>

<span data-ttu-id="ede64-127">Число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода.</span><span class="sxs-lookup"><span data-stu-id="ede64-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="ede64-128">Дополнительные сведения о параметре *lParam* см. в разделе [Флаги сообщения о нажатии клавиш](/windows/desktop/inputdev/about-keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="ede64-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="ede64-129">В следующей таблице описаны биты этого значения.</span><span class="sxs-lookup"><span data-stu-id="ede64-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="ede64-130">Bits</span><span class="sxs-lookup"><span data-stu-id="ede64-130">Bits</span></span> | <span data-ttu-id="ede64-131">Описание</span><span class="sxs-lookup"><span data-stu-id="ede64-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="ede64-132">0—15</span><span class="sxs-lookup"><span data-stu-id="ede64-132">0-15</span></span> | <span data-ttu-id="ede64-133">Число повторов.</span><span class="sxs-lookup"><span data-stu-id="ede64-133">The repeat count.</span></span> <span data-ttu-id="ede64-134">Значение — это количество повторений нажатия клавиши в результате того, как пользователь удерживает клавишу.</span><span class="sxs-lookup"><span data-stu-id="ede64-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="ede64-135">16—23</span><span class="sxs-lookup"><span data-stu-id="ede64-135">16-23</span></span> | <span data-ttu-id="ede64-136">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="ede64-136">The scan code.</span></span> <span data-ttu-id="ede64-137">Значение зависит от поставщика вычислительной техники.</span><span class="sxs-lookup"><span data-stu-id="ede64-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="ede64-138">24</span><span class="sxs-lookup"><span data-stu-id="ede64-138">24</span></span> | <span data-ttu-id="ede64-139">Указывает, является ли ключ расширенным ключом, таким как ключ функции или клавиша на цифровой клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="ede64-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="ede64-140">Значение равно 1, если ключ является расширенным ключом; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="ede64-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="ede64-141">25-28</span><span class="sxs-lookup"><span data-stu-id="ede64-141">25-28</span></span> | <span data-ttu-id="ede64-142">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="ede64-142">Reserved.</span></span> |
| <span data-ttu-id="ede64-143">29</span><span class="sxs-lookup"><span data-stu-id="ede64-143">29</span></span> | <span data-ttu-id="ede64-144">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="ede64-144">The context code.</span></span> <span data-ttu-id="ede64-145">Значение равно 1, если клавиша ALT не нажата; в противном случае — 0.</span><span class="sxs-lookup"><span data-stu-id="ede64-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="ede64-146">30</span><span class="sxs-lookup"><span data-stu-id="ede64-146">30</span></span> | <span data-ttu-id="ede64-147">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="ede64-147">The previous key state.</span></span> <span data-ttu-id="ede64-148">Значение равно 1, если ключ не работает до отправки сообщения; Если ключ работает, он равен 0.</span><span class="sxs-lookup"><span data-stu-id="ede64-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="ede64-149">31</span><span class="sxs-lookup"><span data-stu-id="ede64-149">31</span></span> | <span data-ttu-id="ede64-150">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="ede64-150">The transition state.</span></span> <span data-ttu-id="ede64-151">Значение равно 0, если клавиша нажата, и 1, если он освобождается.</span><span class="sxs-lookup"><span data-stu-id="ede64-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="ede64-152">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ede64-152">Returns</span></span>

<span data-ttu-id="ede64-153">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="ede64-153">Type: **LRESULT**</span></span>

<span data-ttu-id="ede64-154">Если *код* меньше нуля, процедура обработчика должна возвращать значение, возвращаемое функцией **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="ede64-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="ede64-155">Если *код* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_KEYBOARDные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.</span><span class="sxs-lookup"><span data-stu-id="ede64-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="ede64-156">Если процедура обработки сообщения обрабатывала сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение остальной части цепочки обработчиков или конечной процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="ede64-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede64-157">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ede64-157">Remarks</span></span>

<span data-ttu-id="ede64-158">Приложение устанавливает процедуру-обработчик, указывая тип обработчика **WH_KEYBOARD** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="ede64-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="ede64-159">Этот обработчик может быть вызван в контексте потока, установившего его.</span><span class="sxs-lookup"><span data-stu-id="ede64-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="ede64-160">Вызов осуществляется путем отправки сообщения в поток, устанавливающий обработчик.</span><span class="sxs-lookup"><span data-stu-id="ede64-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="ede64-161">Таким образом, поток, устанавливающий обработчик, должен иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="ede64-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="ede64-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ede64-162">See also</span></span>

[<span data-ttu-id="ede64-163">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="ede64-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="ede64-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="ede64-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="ede64-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="ede64-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="ede64-166">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="ede64-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="ede64-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="ede64-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="ede64-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="ede64-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="ede64-169">Обработчики</span><span class="sxs-lookup"><span data-stu-id="ede64-169">Hooks</span></span>](hooks.md)
