---
UID: ''
title: Функция обратного вызова Ловлевелмаусепрок
description: Система вызывает эту функцию каждый раз, когда будет отправлено новое событие ввода-вывода мыши в очередь входных потоков.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2020
ms.locfileid: "104070807"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="be744-103">Функция Ловлевелмаусепрок</span><span class="sxs-lookup"><span data-stu-id="be744-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="be744-104">Описание</span><span class="sxs-lookup"><span data-stu-id="be744-104">Description</span></span>

<span data-ttu-id="be744-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="be744-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="be744-106">Система вызывает эту функцию каждый раз, когда будет отправлено новое событие ввода-вывода мыши в очередь входных потоков.</span><span class="sxs-lookup"><span data-stu-id="be744-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="be744-107">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="be744-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="be744-108">**Ловлевелмаусепрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="be744-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="be744-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="be744-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="be744-110">Нкоде [in]</span><span class="sxs-lookup"><span data-stu-id="be744-110">nCode [in]</span></span>

<span data-ttu-id="be744-111">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="be744-111">Type: **int**</span></span>

<span data-ttu-id="be744-112">Код, используемый процедурой-обработчиком для определения способа обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="be744-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="be744-113">Если *нкоде* меньше нуля, процедура-обработчик должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="be744-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="be744-114">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="be744-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="be744-115">Значение</span><span class="sxs-lookup"><span data-stu-id="be744-115">Value</span></span> | <span data-ttu-id="be744-116">Значение</span><span class="sxs-lookup"><span data-stu-id="be744-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="be744-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="be744-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="be744-118">Параметры *wParam* и *lParam* содержат сведения о сообщении мыши.</span><span class="sxs-lookup"><span data-stu-id="be744-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="be744-119">wParam [вход]</span><span class="sxs-lookup"><span data-stu-id="be744-119">wParam [in]</span></span>

<span data-ttu-id="be744-120">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="be744-120">Type: **WPARAM**</span></span>

<span data-ttu-id="be744-121">Идентификатор сообщения мыши.</span><span class="sxs-lookup"><span data-stu-id="be744-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="be744-122">Этот параметр может принимать одно из следующих сообщений: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) или [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span><span class="sxs-lookup"><span data-stu-id="be744-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="be744-123">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="be744-123">lParam [in]</span></span>

<span data-ttu-id="be744-124">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="be744-124">Type: **LPARAM**</span></span>

<span data-ttu-id="be744-125">Указатель на структуру [мсллхукструкт](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="be744-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="be744-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be744-126">Returns</span></span>

<span data-ttu-id="be744-127">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="be744-127">Type: **LRESULT**</span></span>

<span data-ttu-id="be744-128">Если *нкоде* меньше нуля, процедура-обработчик должна возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="be744-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="be744-129">Если *нкоде* больше или равен нулю и процедура обработчика не обработала сообщение, настоятельно рекомендуется вызвать метод **каллнекссукекс** и вернуть возвращаемое значение. в противном случае другие приложения, которые установили [WH_MOUSE_LLные](about-hooks.md) обработчики, не будут получать уведомления о ловушках и могут вести себя неправильно.</span><span class="sxs-lookup"><span data-stu-id="be744-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="be744-130">Если процедура обработки сообщения обрабатывала сообщение, она может вернуть ненулевое значение, чтобы система не могла передать сообщение остальной части цепочки обработчиков или конечной процедуры окна.</span><span class="sxs-lookup"><span data-stu-id="be744-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="be744-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be744-131">Remarks</span></span>

<span data-ttu-id="be744-132">Приложение устанавливает процедуру-обработчик, указывая тип обработчика **WH_MOUSE_LL** и указатель на процедуру-обработчик в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="be744-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="be744-133">Этот обработчик вызывается в контексте потока, установившего его.</span><span class="sxs-lookup"><span data-stu-id="be744-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="be744-134">Вызов осуществляется путем отправки сообщения в поток, устанавливающий обработчик.</span><span class="sxs-lookup"><span data-stu-id="be744-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="be744-135">Таким образом, поток, устанавливающий обработчик, должен иметь цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="be744-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="be744-136">Входные данные мыши могут поступать от локального драйвера мыши или из вызовов функции [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .</span><span class="sxs-lookup"><span data-stu-id="be744-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="be744-137">Если входные данные поступают из вызова функции **mouse_event**, входные данные были «добавлены».</span><span class="sxs-lookup"><span data-stu-id="be744-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="be744-138">Однако обработчик **WH_MOUSE_LL** не внедряется в другой процесс.</span><span class="sxs-lookup"><span data-stu-id="be744-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="be744-139">Вместо этого контекст переключается в процесс, который установил обработчик, и вызывается в исходном контексте.</span><span class="sxs-lookup"><span data-stu-id="be744-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="be744-140">Затем контекст переключается обратно в приложение, создавшее событие.</span><span class="sxs-lookup"><span data-stu-id="be744-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="be744-141">Процедура-ловушка должна обрабатывать сообщение меньше времени, чем запись данных, указанная в значении **ловлевелхукстимеаут** в следующем разделе реестра: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="be744-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="be744-142">Значение указывается в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="be744-142">The value is in milliseconds.</span></span>
<span data-ttu-id="be744-143">Если превышено время ожидания для процедуры-обработчика, система передает сообщение следующему обработчику.</span><span class="sxs-lookup"><span data-stu-id="be744-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="be744-144">Однако в Windows 7 и более поздних версиях обработчик автоматически удаляется без вызова.</span><span class="sxs-lookup"><span data-stu-id="be744-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="be744-145">Для приложения нет способа определить, удален ли обработчик.</span><span class="sxs-lookup"><span data-stu-id="be744-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="be744-146">**Примечание.**  Ловушки отладки не могут контролировать этот тип обработчиков мыши низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="be744-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="be744-147">Если приложение должно использовать перехватчики низкого уровня, оно должно запускать обработчики в выделенном потоке, который передает работу в рабочий поток, а затем немедленно возвращает.</span><span class="sxs-lookup"><span data-stu-id="be744-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="be744-148">В большинстве случаев, когда приложению требуется использовать низкоуровневые обработчики, вместо него следует отслеживать необработанные данные.</span><span class="sxs-lookup"><span data-stu-id="be744-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="be744-149">Это обусловлено тем, что необработанные входные данные могут асинхронно отслеживать сообщения мыши и клавиатуры, предназначенные для других потоков более эффективно, чем низкоуровневые обработчики.</span><span class="sxs-lookup"><span data-stu-id="be744-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="be744-150">Дополнительные сведения о необработанных входных данных см. в разделе [необработанные входные](/windows/desktop/inputdev/raw-input)данные.</span><span class="sxs-lookup"><span data-stu-id="be744-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="be744-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be744-151">See also</span></span>

[<span data-ttu-id="be744-152">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="be744-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="be744-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="be744-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="be744-154">кбдллхукструкт</span><span class="sxs-lookup"><span data-stu-id="be744-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="be744-155">мсллхукструкт</span><span class="sxs-lookup"><span data-stu-id="be744-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="be744-156">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="be744-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="be744-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="be744-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="be744-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="be744-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="be744-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="be744-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="be744-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="be744-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="be744-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="be744-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="be744-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="be744-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="be744-163">Обработчики</span><span class="sxs-lookup"><span data-stu-id="be744-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="be744-164">О обработчиках</span><span class="sxs-lookup"><span data-stu-id="be744-164">About Hooks</span></span>](about-hooks.md)
