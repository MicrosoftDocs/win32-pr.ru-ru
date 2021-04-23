---
description: Панель инструментов рабочего стола приложения (также называемая панель приложений) — это окно, похожее на панель задач Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Использование панелей инструментов рабочего стола приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140ef94c1daeb571cd0d766dfbd4dc28b7991efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143981"
---
# <a name="using-application-desktop-toolbars"></a><span data-ttu-id="5af6b-103">Использование панелей инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-103">Using Application Desktop Toolbars</span></span>

<span data-ttu-id="5af6b-104">*Панель инструментов рабочего стола приложения* (также называемая панель приложений) — это окно, похожее на панель задач Windows.</span><span class="sxs-lookup"><span data-stu-id="5af6b-104">An *application desktop toolbar* (also called an appbar) is a window that is similar to the Windows taskbar.</span></span> <span data-ttu-id="5af6b-105">Он привязан к границе экрана, и обычно содержит кнопки, предоставляющие пользователю быстрый доступ к другим приложениям и окнам.</span><span class="sxs-lookup"><span data-stu-id="5af6b-105">It is anchored to an edge of the screen, and it typically contains buttons that give the user quick access to other applications and windows.</span></span> <span data-ttu-id="5af6b-106">Система не позволяет другим приложениям использовать область рабочего стола, используемую панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-106">The system prevents other applications from using the desktop area used by an appbar.</span></span> <span data-ttu-id="5af6b-107">Любое количество AppBar может существовать на рабочем столе в любое заданное время.</span><span class="sxs-lookup"><span data-stu-id="5af6b-107">Any number of appbars can exist on the desktop at any given time.</span></span>

<span data-ttu-id="5af6b-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="5af6b-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5af6b-109">О панелях инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-109">About Application Desktop Toolbars</span></span>](#about-application-desktop-toolbars)
    -   [<span data-ttu-id="5af6b-110">Отправка сообщений</span><span class="sxs-lookup"><span data-stu-id="5af6b-110">Sending Messages</span></span>](#sending-messages)
    -   [<span data-ttu-id="5af6b-111">Регистрация</span><span class="sxs-lookup"><span data-stu-id="5af6b-111">Registration</span></span>](#registration)
    -   [<span data-ttu-id="5af6b-112">Панель приложений размер и расположение</span><span class="sxs-lookup"><span data-stu-id="5af6b-112">Appbar Size and Position</span></span>](#appbar-size-and-position)
    -   [<span data-ttu-id="5af6b-113">Автоматически скрывать панели инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-113">Autohide Application Desktop Toolbars</span></span>](#autohide-application-desktop-toolbars)
    -   [<span data-ttu-id="5af6b-114">Сообщения уведомления панель приложений</span><span class="sxs-lookup"><span data-stu-id="5af6b-114">Appbar Notification Messages</span></span>](#appbar-notification-messages)
-   [<span data-ttu-id="5af6b-115">Регистрация панели инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-115">Registering an Application Desktop Toolbar</span></span>](#registering-an-application-desktop-toolbar)
-   [<span data-ttu-id="5af6b-116">Установка размера и расположения панель приложений</span><span class="sxs-lookup"><span data-stu-id="5af6b-116">Setting the Appbar Size and Position</span></span>](#setting-the-appbar-size-and-position)
-   [<span data-ttu-id="5af6b-117">Обработка сообщений уведомлений панель приложений</span><span class="sxs-lookup"><span data-stu-id="5af6b-117">Processing Appbar Notification Messages</span></span>](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a><span data-ttu-id="5af6b-118">О панелях инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-118">About Application Desktop Toolbars</span></span>

<span data-ttu-id="5af6b-119">Windows предоставляет API, позволяющий использовать преимущества панель приложений служб, предоставляемых системой.</span><span class="sxs-lookup"><span data-stu-id="5af6b-119">Windows provides an API that lets you take advantage of appbar services provided by the system.</span></span> <span data-ttu-id="5af6b-120">Службы помогают обеспечить плавность работы определяемых приложением AppBar, а также с панелью задач.</span><span class="sxs-lookup"><span data-stu-id="5af6b-120">The services help ensure that application-defined appbars operate smoothly with one another and with the taskbar.</span></span> <span data-ttu-id="5af6b-121">Система сохраняет сведения о каждом панель приложений и отправляет сообщения AppBar, чтобы уведомить их о событиях, которые могут повлиять на их размер, расположение и внешний вид.</span><span class="sxs-lookup"><span data-stu-id="5af6b-121">The system maintains information about each appbar and sends the appbars messages to notify them about events that can affect their size, position, and appearance.</span></span>

### <a name="sending-messages"></a><span data-ttu-id="5af6b-122">отправка сообщений</span><span class="sxs-lookup"><span data-stu-id="5af6b-122">Sending Messages</span></span>

<span data-ttu-id="5af6b-123">Приложение использует специальный набор сообщений, называемых панель приложений сообщениями, для добавления или удаления панель приложений, установки размера и расположения панель приложений и получения сведений о размере, положении и состоянии панели задач.</span><span class="sxs-lookup"><span data-stu-id="5af6b-123">An application uses a special set of messages, called appbar messages, to add or remove an appbar, set an appbar's size and position, and retrieve information about the size, position, and state of the taskbar.</span></span> <span data-ttu-id="5af6b-124">Чтобы отправить сообщение панель приложений, приложение должно использовать функцию [**шаппбармессаже**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-124">To send an appbar message, an application must use the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function.</span></span> <span data-ttu-id="5af6b-125">Параметры функции включают идентификатор сообщения, например [**АБМ \_ New**](abm-new.md), и адрес структуры [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-125">The function's parameters include a message identifier, such as [**ABM\_NEW**](abm-new.md), and the address of an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="5af6b-126">Члены структуры содержат сведения, необходимые системе для обработки данного сообщения.</span><span class="sxs-lookup"><span data-stu-id="5af6b-126">The structure members contain information that the system needs to process the given message.</span></span>

<span data-ttu-id="5af6b-127">Для любого заданного сообщения панель приложений система использует некоторые члены структуры [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) и игнорирует другие.</span><span class="sxs-lookup"><span data-stu-id="5af6b-127">For any given appbar message, the system uses some members of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure and ignores the others.</span></span> <span data-ttu-id="5af6b-128">Однако система всегда использует элементы **кбсизе** и **HWND** , поэтому приложение должно заполнить эти члены для каждого сообщения панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-128">However, the system always uses the **cbSize** and **hWnd** members, so an application must fill these members for every appbar message.</span></span> <span data-ttu-id="5af6b-129">Элемент **кбсизе** задает размер структуры, а элемент **HWND** — дескриптор окна Панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-129">The **cbSize** member specifies the size of the structure, and the **hWnd** member is the handle to the appbar's window.</span></span>

<span data-ttu-id="5af6b-130">Некоторые сообщения панель приложений запрашивают информацию из системы.</span><span class="sxs-lookup"><span data-stu-id="5af6b-130">Some appbar messages request information from the system.</span></span> <span data-ttu-id="5af6b-131">При обработке этих сообщений система копирует запрошенные сведения в структуру [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-131">When processing these messages, the system copies the requested information into the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

### <a name="registration"></a><span data-ttu-id="5af6b-132">Регистрация</span><span class="sxs-lookup"><span data-stu-id="5af6b-132">Registration</span></span>

<span data-ttu-id="5af6b-133">Система сохраняет внутренний список AppBar и сохраняет информацию о каждой строке в списке.</span><span class="sxs-lookup"><span data-stu-id="5af6b-133">The system keeps an internal list of appbars and maintains information about each bar in the list.</span></span> <span data-ttu-id="5af6b-134">Система использует информацию для управления AppBar, выполнения для них служб и отправки сообщений с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="5af6b-134">The system uses the information to manage appbars, perform services for them, and send them notification messages.</span></span>

<span data-ttu-id="5af6b-135">Приложение должно зарегистрировать панель приложений (то есть добавить его во внутренний список), прежде чем оно сможет получить от системы панель приложений Services.</span><span class="sxs-lookup"><span data-stu-id="5af6b-135">An application must register an appbar (that is, add it to the internal list) before it can receive appbar services from the system.</span></span> <span data-ttu-id="5af6b-136">Чтобы зарегистрировать панель приложений, приложение отправляет [**\_ новое сообщение АБМ**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-136">To register an appbar, an application sends the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="5af6b-137">Сопутствующая структура [**аппбардата**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) включает в себя обработчик для окна Панель приложений и идентификатор сообщения, определяемый приложением.</span><span class="sxs-lookup"><span data-stu-id="5af6b-137">The accompanying [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure includes the handle to the appbar's window and an application-defined message identifier.</span></span> <span data-ttu-id="5af6b-138">Система использует идентификатор сообщения для отправки сообщений уведомления в процедуру окна Панель приложений окна.</span><span class="sxs-lookup"><span data-stu-id="5af6b-138">The system uses the message identifier to send notification messages to the window procedure of the appbar window.</span></span> <span data-ttu-id="5af6b-139">Дополнительные сведения см. в разделе Панель приложений Notification messages.</span><span class="sxs-lookup"><span data-stu-id="5af6b-139">For more information, see Appbar Notification Messages.</span></span>

<span data-ttu-id="5af6b-140">Приложение отменяет регистрацию панель приложений, отправляя сообщение [**об \_ удалении АБМ**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-140">An application unregisters an appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="5af6b-141">При отмене регистрации панель приложений удаляется из внутреннего списка AppBar системы.</span><span class="sxs-lookup"><span data-stu-id="5af6b-141">Unregistering an appbar removes it from the system's internal list of appbars.</span></span> <span data-ttu-id="5af6b-142">Система больше не отправляет сообщения уведомления панель приложений или не позволяет другим приложениям использовать область экрана, используемую панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-142">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span> <span data-ttu-id="5af6b-143">Приложение всегда должно отправить **АБМ \_ Remove** перед уничтожением панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-143">An application should always send **ABM\_REMOVE** before destroying an appbar.</span></span>

### <a name="appbar-size-and-position"></a><span data-ttu-id="5af6b-144">Панель приложений размер и расположение</span><span class="sxs-lookup"><span data-stu-id="5af6b-144">Appbar Size and Position</span></span>

<span data-ttu-id="5af6b-145">Приложение должно установить размер и положение панель приложений, чтобы оно не влияло на другие AppBar или панель задач.</span><span class="sxs-lookup"><span data-stu-id="5af6b-145">An application should set an appbar's size and position so that it does not interfere with any other appbars or the taskbar.</span></span> <span data-ttu-id="5af6b-146">Каждый панель приложений должен быть привязан к определенной границе экрана, а несколько AppBar могут быть привязаны к границе.</span><span class="sxs-lookup"><span data-stu-id="5af6b-146">Every appbar must be anchored to a particular edge of the screen, and multiple appbars can be anchored to an edge.</span></span> <span data-ttu-id="5af6b-147">Однако если панель приложений привязан к тому же самому, что и панель задач, система гарантирует, что панель задач всегда находится на внешнем крае.</span><span class="sxs-lookup"><span data-stu-id="5af6b-147">However, if an appbar is anchored to the same edge as the taskbar, the system ensures that the taskbar is always on the outermost edge.</span></span>

<span data-ttu-id="5af6b-148">Чтобы задать размер и расположение панель приложений, приложение сначала предложит границу экрана и ограничивающий прямоугольник для панель приложений, отправив сообщение [**АБМ \_ куерипос**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-148">To set the size and position of an appbar, an application first proposes a screen edge and bounding rectangle for the appbar by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="5af6b-149">Система определяет, используется ли какая-либо часть экранной области в предложенном прямоугольнике панелью задач или другой панель приложений, корректирует прямоугольник (при необходимости) и возвращает измененный прямоугольник в приложение.</span><span class="sxs-lookup"><span data-stu-id="5af6b-149">The system determines whether any part of the screen area within the proposed rectangle is used by the taskbar or another appbar, adjusts the rectangle (if necessary), and returns the adjusted rectangle to the application.</span></span>

<span data-ttu-id="5af6b-150">Затем приложение отправляет сообщение [**АБМ \_ сетпос**](abm-setpos.md) , чтобы установить новый ограничивающий прямоугольник для панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-150">Next, the application sends the [**ABM\_SETPOS**](abm-setpos.md) message to set the new bounding rectangle for the appbar.</span></span> <span data-ttu-id="5af6b-151">Опять же, система может настроить прямоугольник перед возвратом в приложение.</span><span class="sxs-lookup"><span data-stu-id="5af6b-151">Again, the system may adjust the rectangle before returning it to the application.</span></span> <span data-ttu-id="5af6b-152">По этой причине приложение должно использовать скорректированный прямоугольник, возвращенный **АБМ \_ сетпос** для установки окончательного размера и расположения.</span><span class="sxs-lookup"><span data-stu-id="5af6b-152">For this reason, the application should use the adjusted rectangle returned by **ABM\_SETPOS** to set the final size and position.</span></span> <span data-ttu-id="5af6b-153">Приложение может использовать функцию [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) для перемещения панель приложений в положение.</span><span class="sxs-lookup"><span data-stu-id="5af6b-153">The application can use the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="5af6b-154">Используя двухэтапный процесс для установки размера и положения, система позволяет приложению предоставлять пользователю промежуточный отзыв во время операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="5af6b-154">By using a two-step process to set the size and position, the system enables the application to provide intermediate feedback to the user during the move operation.</span></span> <span data-ttu-id="5af6b-155">Например, если пользователь перетаскивает панель приложений, приложение может отобразить затененный прямоугольник, указывающий на новую точку перед тем, как панель приложений перемещается.</span><span class="sxs-lookup"><span data-stu-id="5af6b-155">For example, if the user drags an appbar, the application might display a shaded rectangle indicating the new position before the appbar actually moves.</span></span>

<span data-ttu-id="5af6b-156">Приложение должно задать размер и расположение его панель приложений после его регистрации и всякий раз, когда панель приложений получит сообщение уведомления [**АБН \_ посчанжед**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-156">An application should set the size and position of its appbar after registering it and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="5af6b-157">Панель приложений получает это уведомление каждый раз, когда происходит изменение размера, расположения или видимости панели задач, а также при каждом изменении размера, добавления или удаления другого панель приложений на той же стороне экрана.</span><span class="sxs-lookup"><span data-stu-id="5af6b-157">An appbar receives this notification message whenever a change occurs in the taskbar's size, position, or visibility state and whenever another appbar on the same side of the screen is resized, added, or removed.</span></span>

<span data-ttu-id="5af6b-158">Всякий раз, когда панель приложений получает \_ сообщение активации WM, оно должно отправить сообщение о [**\_ активации АБМ**](abm-activate.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-158">Whenever an appbar receives the WM\_ACTIVATE message, it should send the [**ABM\_ACTIVATE**](abm-activate.md) message.</span></span> <span data-ttu-id="5af6b-159">Аналогично, когда панель приложений получает сообщение WM \_ виндовпосчанжед, оно должно вызывать [**АБМ \_ виндовпосчанжед**](abm-windowposchanged.md).</span><span class="sxs-lookup"><span data-stu-id="5af6b-159">Similarly, when an appbar receives a WM\_WINDOWPOSCHANGED message, it must call [**ABM\_WINDOWPOSCHANGED**](abm-windowposchanged.md).</span></span> <span data-ttu-id="5af6b-160">Отправка этих сообщений гарантирует, что система правильно устанавливает z-порядок любых appbarов автоскрытия на одном и том же крае.</span><span class="sxs-lookup"><span data-stu-id="5af6b-160">Sending these messages ensures that the system properly sets the z-order of any autohide appbars on the same edge.</span></span>

### <a name="autohide-application-desktop-toolbars"></a><span data-ttu-id="5af6b-161">Автоматически скрывать панели инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-161">Autohide Application Desktop Toolbars</span></span>

<span data-ttu-id="5af6b-162">Панель приложений автоматически скрывается, но становится видимым, когда пользователь перемещает курсор мыши к границе экрана, с которой связана панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-162">An autohide appbar is one that is normally hidden but becomes visible when the user moves the mouse cursor to the screen edge with which the appbar is associated.</span></span> <span data-ttu-id="5af6b-163">Панель приложений скрывает себя снова, когда пользователь перемещает указатель мыши за пределы ограничивающего прямоугольника на панели.</span><span class="sxs-lookup"><span data-stu-id="5af6b-163">The appbar hides itself again when the user moves the mouse cursor out of the bar's bounding rectangle.</span></span>

<span data-ttu-id="5af6b-164">Несмотря на то, что система допускает несколько различных AppBar в любой момент времени, она позволяет только одному элементу автоскрытия панель приложений в каждый момент времени для каждого края экрана на основе первых поступающих.</span><span class="sxs-lookup"><span data-stu-id="5af6b-164">Although the system allows a number of different appbars at any given time, it allows only one autohide appbar at a time for each screen edge on a first-come, first-served basis.</span></span> <span data-ttu-id="5af6b-165">Система автоматически сохраняет z-порядок панель приложений автоскрытия (только в пределах своей группы z-порядка).</span><span class="sxs-lookup"><span data-stu-id="5af6b-165">The system automatically maintains the z-order of an autohide appbar (within its z-order group only).</span></span>

<span data-ttu-id="5af6b-166">Приложение использует сообщение [**АБМ \_ сетаутохидебар**](abm-setautohidebar.md) для регистрации или отмены регистрации панель приложенийа автоскрытия.</span><span class="sxs-lookup"><span data-stu-id="5af6b-166">An application uses the [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) message to register or unregister an autohide appbar.</span></span> <span data-ttu-id="5af6b-167">В сообщении указывается ребро для панель приложений и флаг, указывающий, следует ли регистрировать или отменять регистрацию панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-167">The message specifies the edge for the appbar and a flag that specifies whether the appbar is to be registered or unregistered.</span></span> <span data-ttu-id="5af6b-168">Сообщение завершается ошибкой, если регистрируется панель приложений, но она уже связана с заданным ребром.</span><span class="sxs-lookup"><span data-stu-id="5af6b-168">The message fails if an autohide appbar is being registered but one is already associated with the specified edge.</span></span> <span data-ttu-id="5af6b-169">Приложение может получить маркер для панель приложенийа автоскрытия, связанного с ребром, отправив [**сообщение \_ жетаутохидебар АБМ**](abm-getautohidebar.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-169">An application can retrieve the handle to the autohide appbar associated with an edge by sending the [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) message.</span></span>

<span data-ttu-id="5af6b-170">Панель приложений для автоскрытия не требуется регистрировать как обычную панель приложений; то есть его не нужно регистрировать, отправляя [**\_ новое сообщение АБМ**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-170">An autohide appbar does not need to register as a normal appbar; that is, it does not need to be registered by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="5af6b-171">Панель приложений, который не зарегистрирован **АБМ \_ New** , перекрывает все AppBar, привязанные к одному и тому же краям экрана.</span><span class="sxs-lookup"><span data-stu-id="5af6b-171">An appbar that is not registered by **ABM\_NEW** overlaps any appbars anchored on the same edge of the screen.</span></span>

### <a name="appbar-notification-messages"></a><span data-ttu-id="5af6b-172">Сообщения уведомления панель приложений</span><span class="sxs-lookup"><span data-stu-id="5af6b-172">Appbar Notification Messages</span></span>

<span data-ttu-id="5af6b-173">Система отправляет сообщения для уведомления панель приложений о событиях, которые могут повлиять на его расположение и внешний вид.</span><span class="sxs-lookup"><span data-stu-id="5af6b-173">The system sends messages to notify an appbar about events that can affect its position and appearance.</span></span> <span data-ttu-id="5af6b-174">Сообщения отправляются в контексте определяемого приложением сообщения.</span><span class="sxs-lookup"><span data-stu-id="5af6b-174">The messages are sent in the context of an application-defined message.</span></span> <span data-ttu-id="5af6b-175">Приложение указывает идентификатор сообщения при отправке [**\_ нового сообщения АБМ**](abm-new.md) для регистрации панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-175">The application specifies the identifier of the message when it sends the [**ABM\_NEW**](abm-new.md) message to register the appbar.</span></span> <span data-ttu-id="5af6b-176">Код уведомления находится в параметре *wParam* сообщения, определяемого приложением.</span><span class="sxs-lookup"><span data-stu-id="5af6b-176">The notification code is in the *wParam* parameter of the application-defined message.</span></span>

<span data-ttu-id="5af6b-177">Панель приложений получает уведомление о [**АБН \_ посчанжед**](abn-poschanged.md) , когда изменяется размер, положение или состояние видимости панели задач, когда на тот же край экрана добавляется другой панель приложений или изменяется размер или удаление другого панель приложений на том же крае экрана.</span><span class="sxs-lookup"><span data-stu-id="5af6b-177">An appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message when the taskbar's size, position, or visibility state changes, when another appbar is added to the same edge of the screen, or when another appbar on the same edge of the screen is resized or removed.</span></span> <span data-ttu-id="5af6b-178">Панель приложений должен ответить на это сообщение уведомления, отправив сообщения [**АБМ \_ Куерипос**](abm-querypos.md) и [**АБМ \_ сетпос**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-178">An appbar should respond to this notification message by sending [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="5af6b-179">Если положение панель приложений изменилось, оно должно вызвать функцию [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) , чтобы переместить себя в новое положение.</span><span class="sxs-lookup"><span data-stu-id="5af6b-179">If an appbar's position has changed, it should call the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

<span data-ttu-id="5af6b-180">Система отправляет сообщение уведомления [**АБН \_ STATECHANGE**](abn-statechange.md) всякий раз, когда изменяется Автоскрытие или постоянное состояние панели задач, то есть когда пользователь устанавливает или снимает флажок **всегда включено** или **автоматически скрывать** окно на странице свойств панели задач.</span><span class="sxs-lookup"><span data-stu-id="5af6b-180">The system sends the [**ABN\_STATECHANGE**](abn-statechange.md) notification message whenever the taskbar's autohide or always-on-top state has changed—that is, when the user selects or clears the **Always on top** or **Auto hide** check box on the taskbar's property sheet.</span></span> <span data-ttu-id="5af6b-181">Панель приложений может использовать это сообщение уведомления, чтобы установить его состояние в соответствии с соответствующими настройками панели задач (при необходимости).</span><span class="sxs-lookup"><span data-stu-id="5af6b-181">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

<span data-ttu-id="5af6b-182">При запуске полноэкранного приложения или закрытии последнего полноэкранного приложения панель приложений получает сообщение уведомления о [**АБН \_ фуллскринапп**](abn-fullscreenapp.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-182">When a full-screen application is started or when the last full-screen application is closed, an appbar receives the [**ABN\_FULLSCREENAPP**](abn-fullscreenapp.md) notification message.</span></span> <span data-ttu-id="5af6b-183">Параметр *lParam* указывает, будет ли полноэкранное приложение открываться или закрываться.</span><span class="sxs-lookup"><span data-stu-id="5af6b-183">The *lParam* parameter indicates whether the full-screen application is opening or closing.</span></span> <span data-ttu-id="5af6b-184">Если он открывается, панель приложений должен быть направлен в нижнюю часть z-порядка.</span><span class="sxs-lookup"><span data-stu-id="5af6b-184">If it is opening, the appbar must drop to the bottom of the z-order.</span></span> <span data-ttu-id="5af6b-185">При закрытии последнего полноэкранного приложения панель приложений должен восстановить свою координату z-порядка.</span><span class="sxs-lookup"><span data-stu-id="5af6b-185">The appbar should restore its z-order position when the last full-screen application has closed.</span></span>

<span data-ttu-id="5af6b-186">Панель приложений получает уведомление о [**АБН \_ виндоварранже**](abn-windowarrange.md) , когда пользователь выбирает команду каскадная, мозаичная или плитка по вертикали в контекстном меню панели задач.</span><span class="sxs-lookup"><span data-stu-id="5af6b-186">An appbar receives the [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) notification message when the user selects the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span> <span data-ttu-id="5af6b-187">Система отправляет сообщение два раза — перед изменением окна (*lParam* имеет **значение true**) и после расположения окна (*lParam* имеет **значение false**).</span><span class="sxs-lookup"><span data-stu-id="5af6b-187">The system sends the message two times—before rearranging the windows (*lParam* is **TRUE**) and after arranging the windows (*lParam* is **FALSE**).</span></span>

<span data-ttu-id="5af6b-188">Панель приложений может использовать сообщения [**АБН \_ виндоварранже**](abn-windowarrange.md) , чтобы исключить себя из операции каскада или плитки.</span><span class="sxs-lookup"><span data-stu-id="5af6b-188">An appbar can use [**ABN\_WINDOWARRANGE**](abn-windowarrange.md) messages to exclude itself from the cascade or tile operation.</span></span> <span data-ttu-id="5af6b-189">Чтобы исключить себя, панель приложений должен скрывать себя, когда параметр *lParam* имеет **значение true** , и показывать себя, когда параметр *lParam* имеет **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5af6b-189">To exclude itself, the appbar should hide itself when *lParam* is **TRUE** and show itself when *lParam* is **FALSE**.</span></span> <span data-ttu-id="5af6b-190">Если панель приложений скрывает себя в ответ на это сообщение, ему не нужно отсылать сообщения [**АБМ \_ Куерипос**](abm-querypos.md) и [**АБМ \_ сетпос**](abm-setpos.md) в ответ на операцию Cascade или Tile.</span><span class="sxs-lookup"><span data-stu-id="5af6b-190">If an appbar hides itself in response to this message, it does not need to send the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages in response to the cascade or tile operation.</span></span>

## <a name="registering-an-application-desktop-toolbar"></a><span data-ttu-id="5af6b-191">Регистрация панели инструментов рабочего стола приложения</span><span class="sxs-lookup"><span data-stu-id="5af6b-191">Registering an Application Desktop Toolbar</span></span>

<span data-ttu-id="5af6b-192">Приложение должно зарегистрировать панель приложений, отправив новое сообщение [**АБМ \_**](abm-new.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-192">An application must register an appbar by sending the [**ABM\_NEW**](abm-new.md) message.</span></span> <span data-ttu-id="5af6b-193">Регистрация панель приложений добавляет его во внутренний список системы и предоставляет системе идентификатор сообщения, который будет использоваться для отправки сообщений уведомлений в панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-193">Registering an appbar adds it to the system's internal list and provides the system with a message identifier to use to send notification messages to the appbar.</span></span> <span data-ttu-id="5af6b-194">Перед выходом приложение должно отменить регистрацию панель приложений, отправив сообщение об [**\_ удалении АБМ**](abm-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-194">Before exiting, an application must unregister the appbar by sending the [**ABM\_REMOVE**](abm-remove.md) message.</span></span> <span data-ttu-id="5af6b-195">При отмене регистрации панель приложений удаляется из внутреннего списка системы и предотвращает получение сообщений уведомления панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-195">Unregistering removes the appbar from the system's internal list and prevents the bar from receiving appbar notification messages.</span></span>

<span data-ttu-id="5af6b-196">Функция в следующем примере либо регистрирует, либо отменяет регистрацию панель приложений в зависимости от значения параметра логического флага.</span><span class="sxs-lookup"><span data-stu-id="5af6b-196">The function in the following example either registers or unregisters an appbar, depending on the value of a Boolean flag parameter.</span></span>


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a><span data-ttu-id="5af6b-197">Установка размера и расположения панель приложений</span><span class="sxs-lookup"><span data-stu-id="5af6b-197">Setting the Appbar Size and Position</span></span>

<span data-ttu-id="5af6b-198">Приложение должно задать размер и расположение панель приложений после регистрации панель приложений, после того как пользователь переместит или изменит размер панель приложений и каждый раз, когда панель приложений получит сообщение с уведомлением [**АБН \_ посчанжед**](abn-poschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-198">An application should set an appbar's size and position after registering the appbar, after the user user moves or sizes the appbar, and whenever the appbar receives the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message.</span></span> <span data-ttu-id="5af6b-199">Перед установкой размера и расположения панель приложений приложение запрашивает в системе утвержденный ограничивающий прямоугольник, отправляя сообщение [**\_ куерипос АБМ**](abm-querypos.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-199">Before setting the size and position of the appbar, the application queries the system for an approved bounding rectangle by sending the [**ABM\_QUERYPOS**](abm-querypos.md) message.</span></span> <span data-ttu-id="5af6b-200">Система возвращает ограничивающий прямоугольник, который не влияет на панель задач или другие панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-200">The system returns a bounding rectangle that does not interfere with the taskbar or any other appbar.</span></span> <span data-ttu-id="5af6b-201">Система настраивает прямоугольник исключительно на вычитание прямоугольника; Сохранение исходного размера прямоугольника не дает никаких усилий.</span><span class="sxs-lookup"><span data-stu-id="5af6b-201">The system adjusts the rectangle purely by rectangle subtraction; it makes no effort to preserve the rectangle's initial size.</span></span> <span data-ttu-id="5af6b-202">По этой причине при необходимости панель приложений должен перенастроить прямоугольник после отправки **АБМ \_ куерипос**.</span><span class="sxs-lookup"><span data-stu-id="5af6b-202">For this reason, the appbar should readjust the rectangle, as necessary, after sending **ABM\_QUERYPOS**.</span></span>

<span data-ttu-id="5af6b-203">Затем приложение передает ограничивающий прямоугольник обратно в систему, используя сообщение [**АБМ \_ сетпос**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="5af6b-203">Next, the application passes the bounding rectangle back to the system by using the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span> <span data-ttu-id="5af6b-204">Затем вызывается функция [**мовевиндов**](/windows/win32/api/winuser/nf-winuser-movewindow) для перемещения панель приложений в положение.</span><span class="sxs-lookup"><span data-stu-id="5af6b-204">Then it calls the [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) function to move the appbar into position.</span></span>

<span data-ttu-id="5af6b-205">В следующем примере показано, как задать размер и расположение панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-205">The following example shows how to set an appbar's size and position.</span></span>


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a><span data-ttu-id="5af6b-206">Обработка сообщений уведомлений панель приложений</span><span class="sxs-lookup"><span data-stu-id="5af6b-206">Processing Appbar Notification Messages</span></span>

<span data-ttu-id="5af6b-207">Панель приложений получает сообщение уведомления при изменении состояния панели задач, при запуске полноэкранного приложения (или при закрытии последнего) или при возникновении события, которое может повлиять на размер и положение панель приложений.</span><span class="sxs-lookup"><span data-stu-id="5af6b-207">An appbar receives a notification message when the state of the taskbar changes, when a full-screen application starts (or the last one closes), or when an event occurs that can affect the appbar's size and position.</span></span> <span data-ttu-id="5af6b-208">В следующем примере показано, как обрабатывать различные сообщения уведомления.</span><span class="sxs-lookup"><span data-stu-id="5af6b-208">The following example shows how to process the various notification messages.</span></span>


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



<span data-ttu-id="5af6b-209">Следующая функция корректирует ограничивающий прямоугольник панель приложений, а затем вызывает определяемую приложением функцию Аппбаркуерисетпос (включена в предыдущий раздел), чтобы соответствующим образом задать размер и расположение панели.</span><span class="sxs-lookup"><span data-stu-id="5af6b-209">The following function adjusts an appbar's bounding rectangle and then calls the application-defined AppBarQuerySetPos function (included in the previous section) to set the bar's size and position accordingly.</span></span>


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
