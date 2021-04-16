---
description: Публикуется в приложении, когда пользователь отменяет действия по записи в журнал. Сообщение публикуется с нулевым маркером окна.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Сообщение WM_CANCELJOURNAL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702583"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="0a39d-104">\_Сообщение КАНЦЕЛЖАУРНАЛ WM</span><span class="sxs-lookup"><span data-stu-id="0a39d-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="0a39d-105">Публикуется в приложении, когда пользователь отменяет действия по записи в журнал.</span><span class="sxs-lookup"><span data-stu-id="0a39d-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="0a39d-106">Сообщение публикуется с **нулевым** маркером окна.</span><span class="sxs-lookup"><span data-stu-id="0a39d-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="0a39d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0a39d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a39d-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a39d-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a39d-109">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="0a39d-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0a39d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a39d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0a39d-111">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="0a39d-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a39d-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0a39d-112">Return value</span></span>

<span data-ttu-id="0a39d-113">Тип: **void**</span><span class="sxs-lookup"><span data-stu-id="0a39d-113">Type: **void**</span></span>

<span data-ttu-id="0a39d-114">Это сообщение не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0a39d-114">This message does not return a value.</span></span> <span data-ttu-id="0a39d-115">Она должна обрабатываться из главного цикла приложения или процедуры обработки [**сообщений**](/windows/win32/api/winuser/nf-winuser-getmessage) , а не из оконной процедуры.</span><span class="sxs-lookup"><span data-stu-id="0a39d-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a39d-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a39d-116">Remarks</span></span>

<span data-ttu-id="0a39d-117">Записи журнала и режимы воспроизведения — это режимы, установленные в системе, позволяющие приложению последовательно записывать или воспроизводить ввод данных пользователем.</span><span class="sxs-lookup"><span data-stu-id="0a39d-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="0a39d-118">Система переходит в эти режимы, когда приложение устанавливает процедуру-обработчик [*жаурналрекордпрок*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) или [*жаурналплайбаккпрок*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0a39d-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="0a39d-119">Если система находится в одном из этих режимов ведения журнала, приложения должны переключаться на чтение входных данных из очереди ввода.</span><span class="sxs-lookup"><span data-stu-id="0a39d-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="0a39d-120">Если какое-либо приложение прекращает чтение входных данных, пока система находится в режиме ведения журнала, другие приложения вынуждены ожидать.</span><span class="sxs-lookup"><span data-stu-id="0a39d-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="0a39d-121">Чтобы обеспечить надежную систему, которая не может быть недоступна для какого-либо приложения, система автоматически отменяет все действия по внесению в журнал, когда пользователь нажимает клавиши CTRL + ESC или CTRL + ALT + DEL.</span><span class="sxs-lookup"><span data-stu-id="0a39d-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="0a39d-122">Затем система отсоединяет все процедуры-обработчики ведения журнала и отправляет сообщение **\_ канцелжаурнал WM** с **нулевым** маркером окна в приложение, которое устанавливает обработчик ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="0a39d-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="0a39d-123">Сообщение **WM \_ Канцелжаурнал** имеет **нулевой** обработчик окна, поэтому его нельзя отправить в оконную процедуру.</span><span class="sxs-lookup"><span data-stu-id="0a39d-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="0a39d-124">Существует два способа, с помощью которых приложение может видеть **сообщение \_ канцелжаурнал WM** : Если приложение выполняется в собственном главном цикле, оно должно перехватить сообщение между вызовом метода [**или**](/windows/win32/api/winuser/nf-winuser-getmessage) [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) и его вызовом [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span><span class="sxs-lookup"><span data-stu-id="0a39d-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="0a39d-125">Если приложение не выполняется в собственном главном цикле, оно должно установить процедуру-обработчик [*жетмсгпрок*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (с помощью вызова [**сетвиндовшукекс**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) , указывающего тип обработчика **\_ сообщений** , который отслеживает сообщение).</span><span class="sxs-lookup"><span data-stu-id="0a39d-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="0a39d-126">Когда приложение видит сообщение **WM \_ канцелжаурнал** , оно может предположить две вещи: пользователь намеренно отменил запись журнала или режим воспроизведения, и система уже отключила какие-либо процедуры записи журнала или обработчика воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0a39d-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="0a39d-127">Обратите внимание, что сочетания клавиш, упомянутые выше (CTRL + ESC или CTRL + ALT + DEL), приводят к отмене ведения журнала системой.</span><span class="sxs-lookup"><span data-stu-id="0a39d-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="0a39d-128">Если какое-либо приложение не отвечает, они дают пользователю возможность восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a39d-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="0a39d-129">Код виртуального ключа [**VK \_ Cancel**](../inputdev/virtual-key-codes.md) (обычно реализованный в виде сочетания клавиш Ctrl + Break) — это то, что должно отслеживать приложение, настоящее в режиме записи в журнале, в качестве сигнала, который пользователь хочет отменить действие ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="0a39d-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="0a39d-130">Разница заключается в том, что наблюдение за **VK \_ Cancel** является рекомендуемым поведением для ведения журнала приложений, в то время как CTRL + ESC или Ctrl + Alt + Del приводит к отмене ведения журнала независимо от поведения приложения журнала.</span><span class="sxs-lookup"><span data-stu-id="0a39d-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a39d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0a39d-131">Requirements</span></span>



| <span data-ttu-id="0a39d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0a39d-132">Requirement</span></span> | <span data-ttu-id="0a39d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0a39d-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a39d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a39d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0a39d-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0a39d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0a39d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a39d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0a39d-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0a39d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0a39d-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0a39d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a39d-139"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a39d-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a39d-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a39d-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a39d-141">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="0a39d-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="0a39d-142">[*жаурналплайбаккпрок*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a39d-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0a39d-143">[*жаурналрекордпрок*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a39d-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="0a39d-144">[*жетмсгпрок*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0a39d-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0a39d-145">**сетвиндовшукекс**</span><span class="sxs-lookup"><span data-stu-id="0a39d-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="0a39d-146">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0a39d-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a39d-147">Обработчики</span><span class="sxs-lookup"><span data-stu-id="0a39d-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
