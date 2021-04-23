---
UID: ''
title: Функция обратного вызова Жаурналплайбаккпрок
description: Воспроизводит серию сообщений мыши и клавиатуры, записанных ранее.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "104412752"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="0028d-103">Функция Жаурналплайбаккпрок</span><span class="sxs-lookup"><span data-stu-id="0028d-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="0028d-104">Описание</span><span class="sxs-lookup"><span data-stu-id="0028d-104">Description</span></span>

<span data-ttu-id="0028d-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="0028d-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="0028d-106">Как правило, приложение использует эту функцию для воспроизведения ряда сообщений мыши и клавиатуры, записанных ранее с помощью процедуры-обработчика **жаурналрекордпрок** .</span><span class="sxs-lookup"><span data-stu-id="0028d-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="0028d-107">При условии, что процедура обработчика **жаурналплайбаккпрок** установлена, обычная мышь и ввод с клавиатуры отключаются.</span><span class="sxs-lookup"><span data-stu-id="0028d-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="0028d-108">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0028d-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="0028d-109">**Жаурналплайбаккпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="0028d-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="0028d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0028d-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="0028d-111">код [в]</span><span class="sxs-lookup"><span data-stu-id="0028d-111">code [in]</span></span>

<span data-ttu-id="0028d-112">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="0028d-112">Type: **int**</span></span>

<span data-ttu-id="0028d-113">Код, используемый процедурой-обработчиком для определения способа обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="0028d-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="0028d-114">Если *код* меньше нуля, процедура обработчика должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="0028d-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="0028d-115">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="0028d-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="0028d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0028d-116">Value</span></span> | <span data-ttu-id="0028d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0028d-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="0028d-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="0028d-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="0028d-119">Процедура-обработчик должна скопировать текущее сообщение мыши или клавиатуры в структуру [евентмсг](/windows/desktop/api/winuser/ns-winuser-eventmsg) , на которую указывает параметр *lParam* .</span><span class="sxs-lookup"><span data-stu-id="0028d-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="0028d-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="0028d-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="0028d-121">Приложение вызвало функцию [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) с параметром времовемсг, для которого задано значение **PM_NOREMOVE**, что означает, что сообщение не удаляется из очереди сообщений после обработки **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="0028d-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="0028d-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="0028d-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="0028d-123">Процедура-обработчик должна подготовиться к копированию следующего сообщения мыши или клавиатуры в структуру **евентмсг** , на которую указывает *lParam*.</span><span class="sxs-lookup"><span data-stu-id="0028d-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="0028d-124">После получения кода **HC_GETNEXT** процедура обработчика должна скопировать сообщение в структуру.</span><span class="sxs-lookup"><span data-stu-id="0028d-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="0028d-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="0028d-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="0028d-126">Удалено Системное модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0028d-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="0028d-127">Процедура-обработчик должна возобновить воспроизведение сообщений.</span><span class="sxs-lookup"><span data-stu-id="0028d-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="0028d-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="0028d-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="0028d-129">Отображается Системное модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="0028d-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="0028d-130">Пока диалоговое окно не будет уничтожено, процедура обработчика должна прекращать воспроизведение сообщений.</span><span class="sxs-lookup"><span data-stu-id="0028d-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="0028d-131">wParam</span><span class="sxs-lookup"><span data-stu-id="0028d-131">wParam</span></span>

<span data-ttu-id="0028d-132">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="0028d-132">Type: **WPARAM**</span></span>

<span data-ttu-id="0028d-133">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="0028d-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="0028d-134">lParam</span><span class="sxs-lookup"><span data-stu-id="0028d-134">lParam</span></span>

<span data-ttu-id="0028d-135">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="0028d-135">Type: **LPARAM**</span></span>

<span data-ttu-id="0028d-136">Указатель на структуру **евентмсг** , представляющую сообщение, обрабатываемое процедурой-обработчиком.</span><span class="sxs-lookup"><span data-stu-id="0028d-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="0028d-137">Этот параметр допустим только в том случае, если параметр *Code* имеет значение **HC_GETNEXT**.</span><span class="sxs-lookup"><span data-stu-id="0028d-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="0028d-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0028d-138">Returns</span></span>

<span data-ttu-id="0028d-139">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="0028d-139">Type: **LRESULT**</span></span>

<span data-ttu-id="0028d-140">Чтобы система ожидала перед обработкой сообщения, возвращаемое значение должно быть временем ожидания (в тактах), которое система должна ожидать.</span><span class="sxs-lookup"><span data-stu-id="0028d-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="0028d-141">(Это значение можно вычислить, вычисляя разницу между элементами времени в текущем и предыдущем входных сообщениях.)</span><span class="sxs-lookup"><span data-stu-id="0028d-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="0028d-142">Для немедленной обработки сообщения возвращаемое значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="0028d-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="0028d-143">Возвращаемое значение используется только в том случае, если код обработчика имеет **HC_GETNEXT**; в противном случае он игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0028d-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="0028d-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0028d-144">Remarks</span></span>

<span data-ttu-id="0028d-145">Процедура-обработчик **жаурналплайбаккпрок** должна скопировать входное сообщение в параметр *lParam* .</span><span class="sxs-lookup"><span data-stu-id="0028d-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="0028d-146">Сообщение должно быть ранее записано с помощью процедуры-обработчика **жаурналрекордпрок** , которая не должна изменять сообщение.</span><span class="sxs-lookup"><span data-stu-id="0028d-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="0028d-147">Для получения одного и того же сообщения процедура обработки может вызываться несколько раз с параметром *Code* , для которого задано **HC_GETNEXT** без промежуточного вызова с *кодом* , равным **HC_SKIP**.</span><span class="sxs-lookup"><span data-stu-id="0028d-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="0028d-148">Если *код* **HC_GETNEXT** и возвращаемое значение больше нуля, система приостанавливается на число миллисекунд, указанное возвращаемым значением.</span><span class="sxs-lookup"><span data-stu-id="0028d-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="0028d-149">При продолжении система снова вызывает процедуру-обработчик с *кодом* , имеющим значение **HC_GETNEXT** , чтобы получить то же сообщение.</span><span class="sxs-lookup"><span data-stu-id="0028d-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="0028d-150">Возвращаемое значение этого нового вызова **жаурналплайбаккпрок** должно равняться нулю; в противном случае система вернется в спящий режим на число миллисекунд, указанное возвращаемым значением, вызовите **жаурналплайбаккпрок** еще раз и так далее.</span><span class="sxs-lookup"><span data-stu-id="0028d-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="0028d-151">Система не отвечает.</span><span class="sxs-lookup"><span data-stu-id="0028d-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="0028d-152">В отличие от большинства других процедур глобального обработчика процедуры-обработчики **жаурналрекордпрок** и **жаурналплайбаккпрок** всегда вызываются в контексте потока, который задает обработчик.</span><span class="sxs-lookup"><span data-stu-id="0028d-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="0028d-153">После того как процедура подключения вернет управление в систему, сообщение будет продолжать обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="0028d-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="0028d-154">Если *код* **HC_SKIP**, процедура обработчика должна подготовиться к возврату следующего записанного сообщения о событии при следующем вызове.</span><span class="sxs-lookup"><span data-stu-id="0028d-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="0028d-155">Установите процедуру-обработчик **жаурналплайбаккпрок** , указав тип [WH_JOURNALPLAYBACK](about-hooks.md) и указатель на процедуру обработчика в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="0028d-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="0028d-156">Если пользователь нажимает клавиши CTRL + ESC или CTRL + ALT + DEL во время воспроизведения журнала, система останавливает воспроизведение, отсоединяет процедуру воспроизведения журнала и отправляет сообщение [WM_CANCELJOURNAL](wm-canceljournal.md) в приложение ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="0028d-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="0028d-157">Если процедура-обработчик возвращает сообщение в диапазоне **WM_KEYFIRST** для **WM_KEYLAST**, применяются следующие условия.</span><span class="sxs-lookup"><span data-stu-id="0028d-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="0028d-158">Элемент **param** структуры **евентмсг** указывает виртуальный код клавиши, который был нажат.</span><span class="sxs-lookup"><span data-stu-id="0028d-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="0028d-159">Элемент **парамх** структуры **евентмсг** указывает код сканирования.</span><span class="sxs-lookup"><span data-stu-id="0028d-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="0028d-160">Невозможно указать число повторов.</span><span class="sxs-lookup"><span data-stu-id="0028d-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="0028d-161">Событие всегда принимается для представления одного ключевого события.</span><span class="sxs-lookup"><span data-stu-id="0028d-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="0028d-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0028d-162">See also</span></span>

[<span data-ttu-id="0028d-163">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="0028d-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="0028d-164">евентмсг</span><span class="sxs-lookup"><span data-stu-id="0028d-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="0028d-165">жаурналрекордпрок</span><span class="sxs-lookup"><span data-stu-id="0028d-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="0028d-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="0028d-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="0028d-167">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="0028d-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="0028d-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="0028d-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="0028d-169">Обработчики</span><span class="sxs-lookup"><span data-stu-id="0028d-169">Hooks</span></span>](hooks.md)
