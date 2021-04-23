---
UID: ''
title: Функция обратного вызова Ловлевелкэйбоардпрок
description: Система вызывает эту функцию каждый раз, когда будет отправлено новое событие ввода с клавиатуры в очередь входных потоков.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "104069726"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="de738-103">Функция Ловлевелкэйбоардпрок</span><span class="sxs-lookup"><span data-stu-id="de738-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="de738-104">Описание</span><span class="sxs-lookup"><span data-stu-id="de738-104">Description</span></span>

<span data-ttu-id="de738-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="de738-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="de738-106">Система вызывает эту функцию каждый раз, когда будет отправлено новое событие ввода с клавиатуры в очередь входных потоков.</span><span class="sxs-lookup"><span data-stu-id="de738-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="de738-107">**Примечание.**  При вызове этой функции обратного вызова в ответ на изменение в состоянии ключа функция обратного вызова вызывается до обновления асинхронного состояния ключа.</span><span class="sxs-lookup"><span data-stu-id="de738-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="de738-108">Следовательно, асинхронное состояние ключа не может быть определено путем вызова [жетасинккэйстате](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) из функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="de738-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="de738-109">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="de738-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="de738-110">**Ловлевелкэйбоардпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="de738-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="de738-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="de738-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="de738-112">код [в]</span><span class="sxs-lookup"><span data-stu-id="de738-112">code [in]</span></span>

<span data-ttu-id="de738-113">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="de738-113">Type: **int**</span></span>

<span data-ttu-id="de738-114">Код, используемый процедурой-обработчиком для определения способа обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="de738-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="de738-115">Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="de738-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="de738-116">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="de738-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="de738-117">Значение</span><span class="sxs-lookup"><span data-stu-id="de738-117">Value</span></span> | <span data-ttu-id="de738-118">Значение</span><span class="sxs-lookup"><span data-stu-id="de738-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="de738-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="de738-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="de738-120">Параметры *wParam* и *lParam* содержат сведения о сообщении клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="de738-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="de738-121">wParam [вход]</span><span class="sxs-lookup"><span data-stu-id="de738-121">wParam [in]</span></span>

<span data-ttu-id="de738-122">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="de738-122">Type: **WPARAM**</span></span>

<span data-ttu-id="de738-123">Идентификатор сообщения клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="de738-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="de738-124">Этот параметр может принимать одно из следующих сообщений: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)или [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span><span class="sxs-lookup"><span data-stu-id="de738-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="de738-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="de738-125">lParam [in]</span></span>

<span data-ttu-id="de738-126">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="de738-126">Type: **LPARAM**</span></span>

<span data-ttu-id="de738-127">Указатель на структуру [кбдллхукструкт](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="de738-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="de738-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de738-128">Returns</span></span>

<span data-ttu-id="de738-129">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="de738-129">Type: **LRESULT**</span></span>

<span data-ttu-id="de738-130">Если *нкоде* меньше нуля, процедура-обработчик должна возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="de738-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="de738-131">Если *нкоде* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать метод **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_KEYBOARD_LLные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.</span><span class="sxs-lookup"><span data-stu-id="de738-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="de738-132">Если процедура обработки сообщения обрабатывала сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение остальной части цепочки обработчиков или конечной процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="de738-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="de738-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de738-133">Remarks</span></span>

<span data-ttu-id="de738-134">Приложение устанавливает процедуру-обработчик, указывая тип обработчика **WH_KEYBOARD_LL** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="de738-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="de738-135">Этот обработчик вызывается в контексте потока, установившего его.</span><span class="sxs-lookup"><span data-stu-id="de738-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="de738-136">Вызов осуществляется путем отправки сообщения в поток, устанавливающий обработчик.</span><span class="sxs-lookup"><span data-stu-id="de738-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="de738-137">Таким образом, поток, устанавливающий обработчик, должен иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="de738-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="de738-138">Ввод с клавиатуры может быть получен от локального драйвера клавиатуры или из вызовов функции [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .</span><span class="sxs-lookup"><span data-stu-id="de738-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="de738-139">Если входные данные поступают из вызова функции **keybd_event**, входные данные были «добавлены».</span><span class="sxs-lookup"><span data-stu-id="de738-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="de738-140">Однако обработчик WH_KEYBOARD_LL не внедряется в другой процесс.</span><span class="sxs-lookup"><span data-stu-id="de738-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="de738-141">Вместо этого контекст переключается в процесс, который установил обработчик, и вызывается в исходном контексте.</span><span class="sxs-lookup"><span data-stu-id="de738-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="de738-142">Затем контекст переключается обратно в приложение, создавшее событие.</span><span class="sxs-lookup"><span data-stu-id="de738-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="de738-143">Процедура-ловушка должна обрабатывать сообщение меньше времени, чем запись данных, указанная в значении **ловлевелхукстимеаут** в следующем разделе реестра: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="de738-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="de738-144">Значение указывается в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="de738-144">The value is in milliseconds.</span></span>
<span data-ttu-id="de738-145">Если превышено время ожидания для процедуры-обработчика, система передает сообщение следующему обработчику.</span><span class="sxs-lookup"><span data-stu-id="de738-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="de738-146">Однако в Windows 7 и более поздних версиях обработчик автоматически удаляется без вызова.</span><span class="sxs-lookup"><span data-stu-id="de738-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="de738-147">Для приложения нет способа определить, удален ли обработчик.</span><span class="sxs-lookup"><span data-stu-id="de738-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="de738-148">Примечание. ловушки отладки не могут контролировать этот тип перехватчиков клавиатуры низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="de738-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="de738-149">Если приложение должно использовать перехватчики низкого уровня, оно должно запускать обработчики в выделенном потоке, который передает работу в рабочий поток, а затем немедленно возвращает.</span><span class="sxs-lookup"><span data-stu-id="de738-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="de738-150">В большинстве случаев, когда приложению требуется использовать низкоуровневые обработчики, вместо него следует отслеживать необработанные данные.</span><span class="sxs-lookup"><span data-stu-id="de738-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="de738-151">Это обусловлено тем, что необработанные входные данные могут асинхронно отслеживать сообщения мыши и клавиатуры, предназначенные для других потоков более эффективно, чем низкоуровневые обработчики.</span><span class="sxs-lookup"><span data-stu-id="de738-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="de738-152">Дополнительные сведения о необработанных входных данных см. в разделе [необработанные входные](/windows/desktop/inputdev/raw-input)данные.</span><span class="sxs-lookup"><span data-stu-id="de738-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="de738-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de738-153">See also</span></span>

[<span data-ttu-id="de738-154">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="de738-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="de738-155">кбдллхукструкт</span><span class="sxs-lookup"><span data-stu-id="de738-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="de738-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="de738-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="de738-157">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="de738-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="de738-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="de738-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="de738-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="de738-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="de738-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="de738-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="de738-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="de738-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="de738-162">Обработчики</span><span class="sxs-lookup"><span data-stu-id="de738-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="de738-163">О обработчиках</span><span class="sxs-lookup"><span data-stu-id="de738-163">About Hooks</span></span>](about-hooks.md)
