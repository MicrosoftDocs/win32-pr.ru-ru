---
UID: ''
title: Функция обратного вызова Жаурналрекордпрок
description: Функция записывает сообщения, которые система удаляет из очереди системных сообщений.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2020
ms.locfileid: "103987299"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="ca40b-103">Функция Жаурналрекордпрок</span><span class="sxs-lookup"><span data-stu-id="ca40b-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="ca40b-104">Описание</span><span class="sxs-lookup"><span data-stu-id="ca40b-104">Description</span></span>

<span data-ttu-id="ca40b-105">Определяемая приложением или библиотекой функция обратного вызова, используемая с функцией [сетвиндовшукекс](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="ca40b-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="ca40b-106">Функция записывает сообщения, которые система удаляет из очереди системных сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca40b-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="ca40b-107">Позже приложение может использовать процедуру-обработчик [жаурналплайбаккпрок](journalplaybackproc.md) для воспроизведения сообщений.</span><span class="sxs-lookup"><span data-stu-id="ca40b-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="ca40b-108">Тип **хукпрок** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ca40b-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="ca40b-109">**Жаурналрекордпрок** — это заполнитель для определяемого приложением или библиотечного имени функции.</span><span class="sxs-lookup"><span data-stu-id="ca40b-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="ca40b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca40b-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="ca40b-111">код [в]</span><span class="sxs-lookup"><span data-stu-id="ca40b-111">code [in]</span></span>

<span data-ttu-id="ca40b-112">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="ca40b-112">Type: **int**</span></span>

<span data-ttu-id="ca40b-113">Указывает способ обработки сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca40b-113">Specifies how to process the message.</span></span>
<span data-ttu-id="ca40b-114">Если *код* меньше нуля, процедура обработчика должна передать сообщение в функцию [каллнекссукекс](/windows/desktop/api/winuser/nf-winuser-callnexthookex) без дальнейшей обработки и возвращать значение, возвращенное **каллнекссукекс**.</span><span class="sxs-lookup"><span data-stu-id="ca40b-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="ca40b-115">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="ca40b-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="ca40b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ca40b-116">Value</span></span> | <span data-ttu-id="ca40b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ca40b-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="ca40b-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="ca40b-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="ca40b-119">Параметр *lParam* является указателем на структуру [евентмсг](/windows/desktop/api/winuser/ns-winuser-eventmsg) , содержащую сведения об сообщении, удаленном из системной очереди.</span><span class="sxs-lookup"><span data-stu-id="ca40b-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="ca40b-120">Процедура-обработчик должна записать содержимое структуры, скопировав их в буфер или файл.</span><span class="sxs-lookup"><span data-stu-id="ca40b-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="ca40b-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="ca40b-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="ca40b-122">Удалено Системное модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ca40b-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="ca40b-123">Процедура обработчика должна возобновить запись.</span><span class="sxs-lookup"><span data-stu-id="ca40b-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="ca40b-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="ca40b-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="ca40b-125">Отображается Системное модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="ca40b-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="ca40b-126">Пока диалоговое окно не будет уничтожено, процедура обработчика должна закончить запись.</span><span class="sxs-lookup"><span data-stu-id="ca40b-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="ca40b-127">wParam</span><span class="sxs-lookup"><span data-stu-id="ca40b-127">wParam</span></span>

<span data-ttu-id="ca40b-128">Тип: **wParam**</span><span class="sxs-lookup"><span data-stu-id="ca40b-128">Type: **WPARAM**</span></span>

<span data-ttu-id="ca40b-129">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="ca40b-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="ca40b-130">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="ca40b-130">lParam [in]</span></span>

<span data-ttu-id="ca40b-131">Тип: **lParam** .</span><span class="sxs-lookup"><span data-stu-id="ca40b-131">Type: **LPARAM**</span></span>

<span data-ttu-id="ca40b-132">Указатель на структуру **евентмсг** , содержащую записываемое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ca40b-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="ca40b-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca40b-133">Returns</span></span>

<span data-ttu-id="ca40b-134">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="ca40b-134">Type: **LRESULT**</span></span>

<span data-ttu-id="ca40b-135">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="ca40b-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca40b-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca40b-136">Remarks</span></span>

<span data-ttu-id="ca40b-137">Процедура-обработчик **жаурналрекордпрок** должна копировать, но не изменять сообщения.</span><span class="sxs-lookup"><span data-stu-id="ca40b-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="ca40b-138">После того как процедура подключения вернет управление в систему, сообщение будет продолжать обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="ca40b-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="ca40b-139">Установите процедуру-обработчик **жаурналрекордпрок** , указав тип [WH_JOURNALRECORD](about-hooks.md) и указатель на процедуру обработчика в вызове функции **сетвиндовшукекс** .</span><span class="sxs-lookup"><span data-stu-id="ca40b-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="ca40b-140">Процедура обработчика **жаурналрекордпрок** не обязательно должна находиться в библиотеке динамической компоновки.</span><span class="sxs-lookup"><span data-stu-id="ca40b-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="ca40b-141">Процедура-обработчик **жаурналрекордпрок** может находиться в самом приложении.</span><span class="sxs-lookup"><span data-stu-id="ca40b-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="ca40b-142">В отличие от большинства других процедур глобального обработчика процедуры-обработчики **жаурналрекордпрок** и [жаурналплайбаккпрок](journalplaybackproc.md) всегда вызываются в контексте потока, который задает обработчик.</span><span class="sxs-lookup"><span data-stu-id="ca40b-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="ca40b-143">Приложение, в котором установлена процедура-обработчик **жаурналрекордпрок** , должно отслеживать [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) код виртуального ключа (который реализуется как сочетание клавиш CTRL + BREAK на большинстве клавиатур).</span><span class="sxs-lookup"><span data-stu-id="ca40b-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="ca40b-144">Этот код виртуального ключа должен интерпретироваться приложением как сигнал о том, что пользователь хочет отключить запись журнала.</span><span class="sxs-lookup"><span data-stu-id="ca40b-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="ca40b-145">Приложение должно ответить, завершая последовательность записи и удаляя процедуру обработчика **жаурналрекордпрок** .</span><span class="sxs-lookup"><span data-stu-id="ca40b-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="ca40b-146">Удаление важно.</span><span class="sxs-lookup"><span data-stu-id="ca40b-146">Removal is important.</span></span>
<span data-ttu-id="ca40b-147">Это предотвращает блокировку системы приложением ведения журнала путем зависания внутри процедуры-ловушки.</span><span class="sxs-lookup"><span data-stu-id="ca40b-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="ca40b-148">Эта роль как сигнал для остановки записи жаурнл означает, что сочетание клавиш CTRL + BREAK не может быть записано самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="ca40b-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="ca40b-149">Поскольку сочетание клавиш CTRL + C не имеет такой роли, как сигнал ведения журнала, его можно записать.</span><span class="sxs-lookup"><span data-stu-id="ca40b-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="ca40b-150">Существует два других сочетания клавиш, которые не могут быть записаны: CTRL + ESC и CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="ca40b-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="ca40b-151">Эти два сочетания клавиш приводят к тому, что система останавливает все операции ведения журнала (запись или воспроизведение), удаляет все обработчики ведения журнала и записывает [WM_CANCELJOURNAL](wm-canceljournal.md) сообщение в приложение ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="ca40b-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca40b-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca40b-152">See also</span></span>

[<span data-ttu-id="ca40b-153">каллнекссукекс</span><span class="sxs-lookup"><span data-stu-id="ca40b-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="ca40b-154">евентмсг</span><span class="sxs-lookup"><span data-stu-id="ca40b-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="ca40b-155">жаурналплайбаккпрок</span><span class="sxs-lookup"><span data-stu-id="ca40b-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="ca40b-156">сетвиндовшукекс</span><span class="sxs-lookup"><span data-stu-id="ca40b-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="ca40b-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="ca40b-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="ca40b-158">Обработчики</span><span class="sxs-lookup"><span data-stu-id="ca40b-158">Hooks</span></span>](hooks.md)
