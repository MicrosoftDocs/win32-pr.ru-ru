---
description: Область уведомлений — это часть панели задач, которая предоставляет временный источник уведомлений и состояния.
ms.assetid: D37E2BF7-1887-4780-81AD-85B2117321E4
title: Уведомления и область уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89af1d0b8af0b41674f79325f0eeb389cbc8f2c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344142"
---
# <a name="notifications-and-the-notification-area"></a><span data-ttu-id="19b36-103">Уведомления и область уведомлений</span><span class="sxs-lookup"><span data-stu-id="19b36-103">Notifications and the Notification Area</span></span>

<span data-ttu-id="19b36-104">Область уведомлений — это часть панели задач, которая предоставляет временный источник уведомлений и состояния.</span><span class="sxs-lookup"><span data-stu-id="19b36-104">The notification area is a portion of the taskbar that provides a temporary source for notifications and status.</span></span> <span data-ttu-id="19b36-105">Его также можно использовать для вывода значков для компонентов системы и программ, не имеющих присутствия на рабочем столе, таких как уровень аккумулятора, регулятор громкости и состояние сети.</span><span class="sxs-lookup"><span data-stu-id="19b36-105">It can also be used to display icons for system and program features that have no presence on the desktop, such as battery level, volume control, and network status.</span></span> <span data-ttu-id="19b36-106">Область уведомлений называлась журналом панели задач или областью состояния.</span><span class="sxs-lookup"><span data-stu-id="19b36-106">The notification area has been known historically as the system tray or status area.</span></span>

<span data-ttu-id="19b36-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="19b36-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="19b36-108">Рекомендации по уведомлениям и областям уведомлений</span><span class="sxs-lookup"><span data-stu-id="19b36-108">Notification and Notification Area Guidelines</span></span>](#notification-and-notification-area-guidelines)
-   [<span data-ttu-id="19b36-109">Создание и отображение уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-109">Creating and Displaying a Notification</span></span>](#notifications-and-the-notification-area)
    -   [<span data-ttu-id="19b36-110">Добавить значок уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-110">Add a Notification Icon</span></span>](#add-a-notification-icon)
    -   [<span data-ttu-id="19b36-111">Определение версии НОТИФИКОНДАТА</span><span class="sxs-lookup"><span data-stu-id="19b36-111">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
    -   [<span data-ttu-id="19b36-112">Определение вида и содержимого уведомлений</span><span class="sxs-lookup"><span data-stu-id="19b36-112">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
    -   [<span data-ttu-id="19b36-113">Проверка состояния пользователя</span><span class="sxs-lookup"><span data-stu-id="19b36-113">Check the User Status</span></span>](#check-the-user-status)
    -   [<span data-ttu-id="19b36-114">Отображение уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-114">Display the Notification</span></span>](#display-the-notification)
    -   [<span data-ttu-id="19b36-115">Удаление значка</span><span class="sxs-lookup"><span data-stu-id="19b36-115">Removing an Icon</span></span>](#removing-an-icon)
-   [<span data-ttu-id="19b36-116">Пример пакета SDK</span><span class="sxs-lookup"><span data-stu-id="19b36-116">SDK Sample</span></span>](#sdk-sample)
-   [<span data-ttu-id="19b36-117">См. также</span><span class="sxs-lookup"><span data-stu-id="19b36-117">Related topics</span></span>](#related-topics)

## <a name="notification-and-notification-area-guidelines"></a><span data-ttu-id="19b36-118">Рекомендации по уведомлениям и областям уведомлений</span><span class="sxs-lookup"><span data-stu-id="19b36-118">Notification and Notification Area Guidelines</span></span>

<span data-ttu-id="19b36-119">Рекомендации по использованию уведомлений и области уведомлений см. в разделах " [уведомления](../uxguide/mess-notif.md) и [область уведомлений](../uxguide/winenv-notification.md) " руководства по взаимодействию с пользователем Windows.</span><span class="sxs-lookup"><span data-stu-id="19b36-119">See the [Notifications](../uxguide/mess-notif.md) and [Notification Area](../uxguide/winenv-notification.md) sections of the Windows User Experience Interaction Guidelines for best practices in the use of notifications and the notification area.</span></span> <span data-ttu-id="19b36-120">Целью является предоставление пользователю преимуществ посредством соответствующего использования уведомлений, не заботясь об этом.</span><span class="sxs-lookup"><span data-stu-id="19b36-120">The goal is to provide user benefit through appropriate use of notifications, without being annoying or distracting.</span></span>

<span data-ttu-id="19b36-121">Область уведомлений не предназначена для критической информации, которая должна выполняться немедленно.</span><span class="sxs-lookup"><span data-stu-id="19b36-121">The notification area is not for critical information that must be acted on immediately.</span></span> <span data-ttu-id="19b36-122">Он также не предназначен для быстрого доступа к программе или командам.</span><span class="sxs-lookup"><span data-stu-id="19b36-122">It is also not intended for quick program or command access.</span></span> <span data-ttu-id="19b36-123">Начиная с Windows 7, большая часть этой функциональности лучше всего выполняется с помощью кнопки панели задач приложения.</span><span class="sxs-lookup"><span data-stu-id="19b36-123">As of Windows 7, much of that functionality is best accomplished through an application's taskbar button.</span></span>

<span data-ttu-id="19b36-124">Windows 7 позволяет пользователю подавлять все уведомления из приложения, если они выбраны, поэтому продуманное проектирование и использование занаклонируют пользователя, чтобы приложение продолжало отображать их.</span><span class="sxs-lookup"><span data-stu-id="19b36-124">Windows 7 allows a user to suppress all notifications from an application if they choose, so thoughtful notification design and use will incline the user to allow your application to continue to display them.</span></span> <span data-ttu-id="19b36-125">Уведомления являются прерываниями; Убедитесь, что они стоят.</span><span class="sxs-lookup"><span data-stu-id="19b36-125">Notifications are an interruption; ensure that they are worth it.</span></span>

<span data-ttu-id="19b36-126">В Windows 7 введено понятие "тихий срок".</span><span class="sxs-lookup"><span data-stu-id="19b36-126">Windows 7 introduces the concept of "quiet time".</span></span> <span data-ttu-id="19b36-127">Время молчания определяется как первый час после того, как новый пользователь войдет в свою учетную запись в первый раз или в первый раз после обновления операционной системы или чистой установки.</span><span class="sxs-lookup"><span data-stu-id="19b36-127">Quiet time is defined as the first hour after a new user logs into his or her account either for the first time or for the first time after an operating system upgrade or clean installation.</span></span> <span data-ttu-id="19b36-128">Это время не позволяет пользователю исследовать и изучать новую среду, не отвлекая уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-128">This time is set aside to allow the user to explore and familiarize themselves with the new environment without the distraction of notifications.</span></span> <span data-ttu-id="19b36-129">В течение этого времени большинство уведомлений не следует отправлять или показывать.</span><span class="sxs-lookup"><span data-stu-id="19b36-129">During this time, most notifications should not be sent or shown.</span></span> <span data-ttu-id="19b36-130">Исключения включают отзыв о том, что пользователь может видеть в ответ на действие пользователя, например, когда он подключается к USB-устройству или печатает документ.</span><span class="sxs-lookup"><span data-stu-id="19b36-130">Exceptions include feedback that the user would expect to see in response to a user action, such as when he or she plugs in a USB device or prints a document.</span></span> <span data-ttu-id="19b36-131">Особенности API, связанные со временем молчания, обсуждаются далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="19b36-131">API specifics of regarding quiet time are discussed later in this topic.</span></span>

## <a name="creating-and-displaying-a-notification"></a><span data-ttu-id="19b36-132">Создание и отображение уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-132">Creating and Displaying a Notification</span></span>

<span data-ttu-id="19b36-133">Остальные подразделы этого раздела описывают основную процедуру, которую необходимо выполнить для вывода уведомления от приложения к пользователю.</span><span class="sxs-lookup"><span data-stu-id="19b36-133">The remaining sections in this topic outline the basic procedure to follow to display a notification from your application to the user.</span></span>

1.  [<span data-ttu-id="19b36-134">Добавить значок уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-134">Add a Notification Icon</span></span>](#add-a-notification-icon)
2.  [<span data-ttu-id="19b36-135">Определение версии НОТИФИКОНДАТА</span><span class="sxs-lookup"><span data-stu-id="19b36-135">Define the NOTIFYICONDATA Version</span></span>](#define-the-notifyicondata-version)
3.  [<span data-ttu-id="19b36-136">Определение вида и содержимого уведомлений</span><span class="sxs-lookup"><span data-stu-id="19b36-136">Define the Notification Look and Contents</span></span>](#define-the-notification-look-and-contents)
4.  [<span data-ttu-id="19b36-137">Проверка состояния пользователя</span><span class="sxs-lookup"><span data-stu-id="19b36-137">Check the User Status</span></span>](#check-the-user-status)
5.  [<span data-ttu-id="19b36-138">Отображение уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-138">Display the Notification</span></span>](#display-the-notification)
6.  [<span data-ttu-id="19b36-139">Удаление значка</span><span class="sxs-lookup"><span data-stu-id="19b36-139">Removing an Icon</span></span>](#removing-an-icon)

### <a name="add-a-notification-icon"></a><span data-ttu-id="19b36-140">Добавить значок уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-140">Add a Notification Icon</span></span>

<span data-ttu-id="19b36-141">Для вывода уведомления в области уведомлений должен быть значок.</span><span class="sxs-lookup"><span data-stu-id="19b36-141">To display a notification, you must have an icon in the notification area.</span></span> <span data-ttu-id="19b36-142">В некоторых случаях, таких как Microsoft Communicator или уровень заряда батареи, этот значок уже существует.</span><span class="sxs-lookup"><span data-stu-id="19b36-142">In certain cases, such as Microsoft Communicator or battery level, that icon will already be present.</span></span> <span data-ttu-id="19b36-143">Однако во многих других случаях значок добавляется в область уведомлений только в том случае, если он необходим для отображения уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-143">In many other cases, however, you will add an icon to the notification area only as long as is needed to show the notification.</span></span> <span data-ttu-id="19b36-144">В любом случае это достигается с помощью функции [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .</span><span class="sxs-lookup"><span data-stu-id="19b36-144">In either case, this is accomplished using the [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) function.</span></span> <span data-ttu-id="19b36-145">**Оболочка \_ NotifyIcon** позволяет добавлять, изменять и удалять значки в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-145">**Shell\_NotifyIcon** allows you to add, modify, or delete an icon in the notification area.</span></span>

![область уведомлений, содержащая три значка](images/taskbar/notificationareaicons.png)

<span data-ttu-id="19b36-147">При добавлении значка в область уведомлений в Windows 7 он добавляется в раздел Overflow области уведомлений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19b36-147">When an icon is added to the notification area on Windows 7, it is added to the overflow section of the notification area by default.</span></span> <span data-ttu-id="19b36-148">Эта область содержит значки области уведомлений, которые активны, но не отображаются в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-148">This area contains notification area icons that are active, but not visible in the notification area.</span></span> <span data-ttu-id="19b36-149">Только пользователь может переместить значок из переполнения в область уведомлений, хотя в некоторых обстоятельствах система может временно переместить значок в область уведомлений в виде короткой предварительной версии (в течение одной минуты).</span><span class="sxs-lookup"><span data-stu-id="19b36-149">Only the user can promote an icon from the overflow to the notification area, although in certain circumstances the system can temporarily promote an icon into the notification area as a short preview (under one minute).</span></span>

> [!Note]  
> <span data-ttu-id="19b36-150">Пользователь должен иметь конечное мнение о том, какие значки должны отображаться в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-150">The user should have the final say on which icons they want to see in their notification area.</span></span> <span data-ttu-id="19b36-151">Перед установкой значка, не являющегося временным, в области уведомлений необходимо запросить разрешение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="19b36-151">Before installing a non-transient icon in the notification area, the user should be asked for permission.</span></span> <span data-ttu-id="19b36-152">Кроме того, следует указать параметр (как правило, хотя контекстное меню), чтобы удалить значок из области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-152">They should also be given the option (normally though its shortcut menu) to remove the icon from the notification area.</span></span>

 

<span data-ttu-id="19b36-153">Структура [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) , отправленная в вызове [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , содержит сведения, указывающие как значок области уведомлений, так и само уведомление.</span><span class="sxs-lookup"><span data-stu-id="19b36-153">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification itself.</span></span> <span data-ttu-id="19b36-154">Ниже перечислены элементы, относящиеся к самому значку области уведомлений, которые можно задать с помощью **нотификондата**.</span><span class="sxs-lookup"><span data-stu-id="19b36-154">The following are those items specific to the notification area icon itself that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="19b36-155">Ресурс, из которого берется значок.</span><span class="sxs-lookup"><span data-stu-id="19b36-155">The resource from which the icon is taken.</span></span>
-   <span data-ttu-id="19b36-156">Уникальный идентификатор значка.</span><span class="sxs-lookup"><span data-stu-id="19b36-156">A unique identifier for the icon.</span></span>
-   <span data-ttu-id="19b36-157">Стиль подсказки для значка.</span><span class="sxs-lookup"><span data-stu-id="19b36-157">The style of the icon's tooltip.</span></span>
-   <span data-ttu-id="19b36-158">Состояние значка (скрыто, Shared или Both) в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-158">The icon's state (hidden, shared, or both) in the notification area.</span></span>
-   <span data-ttu-id="19b36-159">Маркер окна приложения, связанный со значком.</span><span class="sxs-lookup"><span data-stu-id="19b36-159">The handle of an application window associated with the icon.</span></span>
-   <span data-ttu-id="19b36-160">Идентификатор сообщения обратного вызова, который позволяет значку передавать события, происходящие в ограничивающем прямоугольнике значка, и всплывающее уведомление с соответствующим окном приложения.</span><span class="sxs-lookup"><span data-stu-id="19b36-160">A callback message identifier that allows the icon to communicate events that occur within the icon's bounding rectangle and balloon notification with the associated application window.</span></span> <span data-ttu-id="19b36-161">Ограничивающий прямоугольник значка можно получить с помощью [**оболочки \_ нотификонжетрект**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span><span class="sxs-lookup"><span data-stu-id="19b36-161">The icon's bounding rectangle can be retrieved through [**Shell\_NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect).</span></span>

<span data-ttu-id="19b36-162">Каждый значок в области уведомлений может быть идентифицирован двумя способами:</span><span class="sxs-lookup"><span data-stu-id="19b36-162">Each icon in the notification area can be identified in two ways:</span></span>

-   <span data-ttu-id="19b36-163">Идентификатор GUID, с которым объявляется значок в реестре.</span><span class="sxs-lookup"><span data-stu-id="19b36-163">The GUID with which the icon is declared in the registry.</span></span> <span data-ttu-id="19b36-164">Этот метод является предпочтительным для Windows 7 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="19b36-164">This is the preferred method on Windows 7 and later.</span></span>
-   <span data-ttu-id="19b36-165">Маркер окна, связанный со значком области уведомлений, а также идентификатор значка, определяемый приложением.</span><span class="sxs-lookup"><span data-stu-id="19b36-165">The handle of a window associated with the notification area icon, plus an application-defined icon identifier.</span></span> <span data-ttu-id="19b36-166">Этот метод используется в Windows Vista и более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="19b36-166">This method is used on Windows Vista and earlier.</span></span>

<span data-ttu-id="19b36-167">Значки в области уведомлений могут содержать подсказку.</span><span class="sxs-lookup"><span data-stu-id="19b36-167">Icons in the notification area can have a tooltip.</span></span> <span data-ttu-id="19b36-168">Подсказка может быть либо стандартной подсказкой (предпочтительной), либо отображаемым приложением пользовательским интерфейсом всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="19b36-168">The tooltip can be either a standard tooltip (preferred) or an application-drawn, pop-up UI.</span></span> <span data-ttu-id="19b36-169">Хотя подсказка не является обязательной, ее рекомендуется использовать.</span><span class="sxs-lookup"><span data-stu-id="19b36-169">While a tooltip is not required, it is recommended.</span></span>

<span data-ttu-id="19b36-170">Для значков области уведомлений необходимо учитывать высокое разрешение DPI.</span><span class="sxs-lookup"><span data-stu-id="19b36-170">Notification area icons should be high-DPI aware.</span></span> <span data-ttu-id="19b36-171">Приложение должно предоставить как значок 16x16 пикселей, так и значок 32x32 в файле ресурсов, а затем использовать [**лоадиконметрик**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) , чтобы убедиться, что нужный значок загружен и правильно масштабируется.</span><span class="sxs-lookup"><span data-stu-id="19b36-171">An application should provide both a 16x16 pixel icon and a 32x32 icon in its resource file, and then use [**LoadIconMetric**](/windows/win32/api/commctrl/nf-commctrl-loadiconmetric) to ensure that the correct icon is loaded and scaled appropriately.</span></span>

<span data-ttu-id="19b36-172">Приложение, ответственное за значок области уведомлений, должно отреагировать на этот значок щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="19b36-172">The application responsible for the notification area icon should handle a mouse click for that icon.</span></span> <span data-ttu-id="19b36-173">Когда пользователь щелкает правой кнопкой мыши значок, он должен открыть обычное контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="19b36-173">When a user right-clicks the icon, it should bring up a normal shortcut menu.</span></span> <span data-ttu-id="19b36-174">Однако результат одного щелчка левой кнопкой мыши будет зависеть от функции значка.</span><span class="sxs-lookup"><span data-stu-id="19b36-174">However, the result of a single click with the left mouse button will vary with the function of the icon.</span></span> <span data-ttu-id="19b36-175">Он должен показать, что пользователь будет видеть в форме, которая лучше всего подходит для этого содержимого — всплывающее окно, диалоговое окно или само окно программы.</span><span class="sxs-lookup"><span data-stu-id="19b36-175">It should display what the user would expect to see in the form best suited to that content—a popup window, a dialog box or the program window itself.</span></span> <span data-ttu-id="19b36-176">Например, он может отображать текст состояния для значка состояния или ползунок для регулятора громкости.</span><span class="sxs-lookup"><span data-stu-id="19b36-176">For instance, it could show status text for a status icon, or a slider for the volume control.</span></span>

<span data-ttu-id="19b36-177">Расположение всплывающего окна или диалогового окна, которое появляется в результате щелчка, должно располагаться рядом с координатой щелчка в области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-177">The placement of a popup window or dialog box that results from the click should be placed near the coordinate of the click in the notification area.</span></span> <span data-ttu-id="19b36-178">Чтобы определить его расположение, используйте [**калкулатепопупвиндовпоситион**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) .</span><span class="sxs-lookup"><span data-stu-id="19b36-178">Use the [**CalculatePopupWindowPosition**](/windows/win32/api/winuser/nf-winuser-calculatepopupwindowposition) to determine its location.</span></span>

<span data-ttu-id="19b36-179">Значок можно добавить в область уведомлений без отображения уведомления, определив только элементы, относящиеся к значку [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (см. выше), и вызов [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="19b36-179">The icon can be added to the notification area without displaying a notification by defining only the icon-specific members of [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) (discussed above) and calling [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) as shown here:</span></span>


```
NOTIFYICONDATA nid = {};
// Do NOT set the NIF_INFO flag.
...                    
Shell_NotifyIcon(NIM_ADD, &nid);
```



<span data-ttu-id="19b36-180">Можно также добавить значок в область уведомлений и отобразить уведомление в одном вызове [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="19b36-180">You can also add the icon to the notification area and display a notification all in one call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="19b36-181">Для этого выполните инструкции, приведенные в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="19b36-181">To do so, continue with the instructions in this topic.</span></span>

### <a name="define-the-notifyicondata-version"></a><span data-ttu-id="19b36-182">Определение версии НОТИФИКОНДАТА</span><span class="sxs-lookup"><span data-stu-id="19b36-182">Define the NOTIFYICONDATA Version</span></span>

<span data-ttu-id="19b36-183">По мере выполнения Windows структура [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) расширяется и включает больше элементов для определения дополнительных функций.</span><span class="sxs-lookup"><span data-stu-id="19b36-183">As Windows has progressed, the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure has expanded to include more members to define more functionality.</span></span> <span data-ttu-id="19b36-184">Константы используются для объявления версии **нотификондата** , используемой с значком области уведомлений, для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="19b36-184">Constants are used to declare which version of **NOTIFYICONDATA** to use with your notification area icon, to allow for backward compatibility.</span></span> <span data-ttu-id="19b36-185">Если нет особой причины для этого, настоятельно рекомендуется использовать \_ версию NOTIFYICON версии \_ 4, появившуюся в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="19b36-185">Unless there is a compelling reason to do otherwise, it is strongly recommended that you use the NOTIFYICON\_VERSION\_4 version, introduced in Windows Vista.</span></span> <span data-ttu-id="19b36-186">Эта версия предоставляет все доступные функциональные возможности, в том числе предпочтительную возможность определять значок области уведомлений, хотя зарегистрированный GUID, старший механизм обратного вызова и улучшенный доступ.</span><span class="sxs-lookup"><span data-stu-id="19b36-186">This version provides the full available functionality, including the preferred ability to identify the notification area icon though a registered GUID, a superior callback mechanism, and better accessibility.</span></span>

<span data-ttu-id="19b36-187">Задайте версию, выполнив следующие вызовы:</span><span class="sxs-lookup"><span data-stu-id="19b36-187">Set the version through the following calls:</span></span>


```
NOTIFYICONDATA nid = {};
... 
nid.uVersion = NOTIFYICON_VERSION_4;
// Add the icon
Shell_NotifyIcon(NIM_ADD, &nid);
// Set the version
Shell_NotifyIcon(NIM_SETVERSION, &nid);
```



<span data-ttu-id="19b36-188">Обратите внимание, что этот вызов [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) не отображает уведомление.</span><span class="sxs-lookup"><span data-stu-id="19b36-188">Note that this call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) does not display a notification.</span></span>

### <a name="define-the-notification-look-and-contents"></a><span data-ttu-id="19b36-189">Определение вида и содержимого уведомлений</span><span class="sxs-lookup"><span data-stu-id="19b36-189">Define the Notification Look and Contents</span></span>

<span data-ttu-id="19b36-190">Уведомление — это специальный тип элемента управления всплывающей подсказки.</span><span class="sxs-lookup"><span data-stu-id="19b36-190">A notification is a special type of balloon tooltip control.</span></span> <span data-ttu-id="19b36-191">Он содержит заголовок, текст текста и значок.</span><span class="sxs-lookup"><span data-stu-id="19b36-191">It contains a title, body text, and an icon.</span></span> <span data-ttu-id="19b36-192">Как и окно, у него есть кнопка **Закрыть** в правом верхнем углу.</span><span class="sxs-lookup"><span data-stu-id="19b36-192">Like a window, it has a **Close** button in its upper right corner.</span></span> <span data-ttu-id="19b36-193">Он также содержит кнопку **Параметры** , которая открывает элемент значки области уведомлений на панели управления, что позволяет пользователю отображать или скрывать значок или отображать только уведомления без значка.</span><span class="sxs-lookup"><span data-stu-id="19b36-193">It also contains a **Options** button that opens the Notification Area Icons item in the Control Panel, which allows the user to show or hide the icon or show only notifications without an icon.</span></span>

![снимок экрана с всплывающим уведомлением о низком питании от аккумулятора](images/taskbar/notificationballoon.png)

<span data-ttu-id="19b36-195">Структура [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) , отправленная в вызове [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , содержит сведения, указывающие как значок области уведомлений, так и сам всплывающий элемент уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-195">The [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure sent in the call to [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) contains information that specifies both the notification area icon and the notification balloon itself.</span></span> <span data-ttu-id="19b36-196">Ниже перечислены элементы, относящиеся к уведомлению, которые можно задать с помощью **нотификондата**.</span><span class="sxs-lookup"><span data-stu-id="19b36-196">The following are those items specific to the notification that can be set through **NOTIFYICONDATA**.</span></span>

-   <span data-ttu-id="19b36-197">Значок, отображаемый в подсказке уведомления, которая указывается типом уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-197">An icon to display in the notification balloon, which is specified by the notification type.</span></span> <span data-ttu-id="19b36-198">Можно указать размер значка, а также настраиваемые значки.</span><span class="sxs-lookup"><span data-stu-id="19b36-198">The size of the icon can be specified, as well as custom icons.</span></span>
-   <span data-ttu-id="19b36-199">Заголовок уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-199">A notification title.</span></span> <span data-ttu-id="19b36-200">Этот заголовок должен содержать не более 48 символов на английском языке (для поддержки локализации).</span><span class="sxs-lookup"><span data-stu-id="19b36-200">This title should be a maximum of 48 characters long in English (to accommodate localization).</span></span> <span data-ttu-id="19b36-201">Заголовок — это первая строка уведомления, которая задается с помощью размера, цвета и веса шрифта.</span><span class="sxs-lookup"><span data-stu-id="19b36-201">The title is the first line of the notification, and set apart through the use of font size, color, and weight.</span></span>
-   <span data-ttu-id="19b36-202">Текст для использования в тексте уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-202">Text for use in the body of the notification.</span></span> <span data-ttu-id="19b36-203">Этот текст должен содержать не более 200 символов на английском языке (для поддержки локализации).</span><span class="sxs-lookup"><span data-stu-id="19b36-203">This text should be a maximum of 200 characters in English (to accommodate localization).</span></span>
-   <span data-ttu-id="19b36-204">Следует ли отменять уведомление, если оно не может быть отображено немедленно.</span><span class="sxs-lookup"><span data-stu-id="19b36-204">Whether the notification should be discarded if it cannot be displayed immediately.</span></span>
-   <span data-ttu-id="19b36-205">Время ожидания уведомления.</span><span class="sxs-lookup"><span data-stu-id="19b36-205">A timeout for the notification.</span></span> <span data-ttu-id="19b36-206">Этот параметр не учитывается в Windows Vista и более поздних системах в пользу параметра времени ожидания доступности в масштабе всей системы.</span><span class="sxs-lookup"><span data-stu-id="19b36-206">This setting is ignored in Windows Vista and later systems in favor of a system-wide accessibility timeout setting.</span></span>
-   <span data-ttu-id="19b36-207">Указывает, должно ли уведомление учитывать время молчания, задается с помощью флага [**\_ \_ \_ времени нииф "тихий**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) ".</span><span class="sxs-lookup"><span data-stu-id="19b36-207">Whether the notification should respect quiet time, set through the [**NIIF\_RESPECT\_QUIET\_TIME**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) flag.</span></span>

> [!Note]  
> <span data-ttu-id="19b36-208">Интерфейсы [**иусернотификатион**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) и [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) являются оболочками модели COM для [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="19b36-208">The [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification) and [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2) interfaces are Component Object Model (COM) wrappers for [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="19b36-209">Однако в настоящее время они не предоставляют полный \_ \_ набор функциональных возможностей NotifyIcon версии 4, доступных через **интерпретатор команд \_ NotifyIcon** напрямую, включая использование идентификатора GUID для указания значка области уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19b36-209">However, at this time, they do not provide the full NOTIFYICON\_VERSION\_4 functionality available through **Shell\_NotifyIcon** directly, including the use of a GUID to identify the notification area icon.</span></span>

 

### <a name="check-the-user-status"></a><span data-ttu-id="19b36-210">Проверка состояния пользователя</span><span class="sxs-lookup"><span data-stu-id="19b36-210">Check the User Status</span></span>

<span data-ttu-id="19b36-211">Система использует функцию [**шкуерюсернотификатионстате**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) для проверки того, находится ли пользователь в тихом режиме, от компьютера или в состоянии непрерывного состояния, такого как режим презентации.</span><span class="sxs-lookup"><span data-stu-id="19b36-211">The system uses the [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) function is used to check whether the user is in quiet time, away from the computer, or in an uninterruptable state such as Presentation mode.</span></span> <span data-ttu-id="19b36-212">Будет ли система отображать уведомление, зависит от этого состояния.</span><span class="sxs-lookup"><span data-stu-id="19b36-212">Whether the system displays your notification depends on this state.</span></span>

> [!Note]  
> <span data-ttu-id="19b36-213">Если приложение использует пользовательский метод уведомления, не использующий [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**иусернотификатион**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)или [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), он должен всегда явно вызывать [**шкуерюсернотификатионстате**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) , чтобы определить, должен ли он отображать пользовательский интерфейс уведомления в это время.</span><span class="sxs-lookup"><span data-stu-id="19b36-213">If your application is using a custom notification method that does not use [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), [**IUserNotification**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification), or [**IUserNotification2**](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2), it should always explicitly call [**SHQueryUserNotificationState**](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate) to determine whether it should display notification UI at that time.</span></span>

 

<span data-ttu-id="19b36-214">Уведомления, отправленные при отсутствии пользователя, помещаются в очередь для отображения, но из-за того, что пользователь не может получить сведения о том, когда будет возвращено это уведомление, можно будет повторно отправить уведомление позже.</span><span class="sxs-lookup"><span data-stu-id="19b36-214">Notifications sent when the user is away are queued for display, but because you cannot know when the user will return or whether the notification will still be valid at that time, you might consider resending the notification later.</span></span>

<span data-ttu-id="19b36-215">Уведомления, отправленные во время молчания, отбрасываются не отображаются.</span><span class="sxs-lookup"><span data-stu-id="19b36-215">Notifications sent during quiet time are discarded unshown.</span></span> <span data-ttu-id="19b36-216">Рекомендации по проектированию запрашивают, что все уведомления должны быть проигнорированы.</span><span class="sxs-lookup"><span data-stu-id="19b36-216">Design guidelines ask that all notifications be ignorable.</span></span> <span data-ttu-id="19b36-217">Они не должны требовать немедленного вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="19b36-217">They should not require immediate user action.</span></span> <span data-ttu-id="19b36-218">Поэтому уведомления не настолько важны, что оно должно переопределять время без вывода сообщений.</span><span class="sxs-lookup"><span data-stu-id="19b36-218">Therefore, no notification is so important that it should override quiet time.</span></span>

### <a name="display-the-notification"></a><span data-ttu-id="19b36-219">Отображение уведомления</span><span class="sxs-lookup"><span data-stu-id="19b36-219">Display the Notification</span></span>

<span data-ttu-id="19b36-220">После того как вы настроили версию [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) и определили уведомление в структуре **нотификондата** , вызовите [**оболочку \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) для вывода значка.</span><span class="sxs-lookup"><span data-stu-id="19b36-220">Once you have set the [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) version and defined the notification in a **NOTIFYICONDATA** structure, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to display the icon.</span></span>

-   <span data-ttu-id="19b36-221">Если значок области уведомлений отсутствует, вызовите [**оболочку \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , чтобы добавить значок.</span><span class="sxs-lookup"><span data-stu-id="19b36-221">If the notification area icon is not present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to add the icon.</span></span> <span data-ttu-id="19b36-222">Сделайте это как для временных, так и для невременных значков.</span><span class="sxs-lookup"><span data-stu-id="19b36-222">Do this for both transient and non-transient icons.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_ADD, &nid);
    ```

    

-   <span data-ttu-id="19b36-223">Если значок области уведомлений уже существует, вызовите [**оболочку \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , чтобы изменить значок.</span><span class="sxs-lookup"><span data-stu-id="19b36-223">If the notification area icon is already present, call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) to modify the icon.</span></span>
    ```
    NOTIFYICONDATA nid = {};
    ...                    
    Shell_NotifyIcon(NIM_MODIFY, &nid);
    ```

    

<span data-ttu-id="19b36-224">В следующем коде показан пример установки [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) данных и их отправки через [**оболочку \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span><span class="sxs-lookup"><span data-stu-id="19b36-224">The following code shows an example of setting [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) data and sending it through [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span> <span data-ttu-id="19b36-225">Обратите внимание, что этот пример определяет значок уведомления с помощью идентификатора GUID (предпочтительно в Windows 7).</span><span class="sxs-lookup"><span data-stu-id="19b36-225">Note that this example identifies the notification icon through a GUID (preferred in Windows 7).</span></span>


```
// Declare NOTIFYICONDATA details. 
    // Error handling is omitted here for brevity. Do not omit it in your code.
    
    NOTIFYICONDATA nid = {};
    nid.cbSize = sizeof(nid);
    nid.hWnd = hWnd;
    nid.uFlags = NIF_ICON | NIF_TIP | NIF_GUID;
    
    // Note: This is an example GUID only and should not be used.
    // Normally, you should use a GUID-generating tool to provide the value to
    // assign to guidItem.
    static const GUID myGUID = 
    {0x23977b55, 0x10e0, 0x4041, {0xb8, 0x62, 0xb1, 0x95, 0x41, 0x96, 0x36, 0x69}};
    nid.guidItem = myGUID;
    
    nid.guidItem = guid;
    
    // This text will be shown as the icon's tooltip.
    StringCchCopy(nid.szTip, ARRAYSIZE(nid.szTip), L"Test application");
    
    // Load the icon for high DPI.
    LoadIconMetric(hInst, MAKEINTRESOURCE(IDI_SMALL), LIM_SMALL, &(nid.hIcon));
    
    // Show the notification.
    Shell_NotifyIcon(NIM_ADD, &nid) ? S_OK : E_FAIL;
```



### <a name="removing-an-icon"></a><span data-ttu-id="19b36-226">Удаление значка</span><span class="sxs-lookup"><span data-stu-id="19b36-226">Removing an Icon</span></span>

<span data-ttu-id="19b36-227">Чтобы удалить значок, например, если вы временно добавили значок для рассылки уведомления, вызовите [**оболочку \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="19b36-227">To remove an icon—for instance, when you have only added the icon temporarily to broadcast a notification—call [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)as shown here.</span></span> <span data-ttu-id="19b36-228">В этом вызове требуется только минимальная структура [**нотификондата**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) , идентифицирующая значок.</span><span class="sxs-lookup"><span data-stu-id="19b36-228">Only a minimal [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) structure that identifies the icon is needed in this call.</span></span>


```
NOTIFYICONDATA nid = {};
...                    
Shell_NotifyIcon(NIM_DELETE, &nid);
```



> [!Note]  
> <span data-ttu-id="19b36-229">При удалении приложения его значок области уведомлений по-прежнему может отображаться для пользователя в виде параметра на странице значков области уведомлений на панели управления до семи дней.</span><span class="sxs-lookup"><span data-stu-id="19b36-229">When an application is uninstalled, its notification area icon can still appear to the user as an option in the Notification Area Icons page in the Control Panel for up to seven days.</span></span> <span data-ttu-id="19b36-230">Однако любые сделанные изменения не будут действовать.</span><span class="sxs-lookup"><span data-stu-id="19b36-230">However, any changes made there will have no effect.</span></span>

 

## <a name="sdk-sample"></a><span data-ttu-id="19b36-231">Пример пакета SDK</span><span class="sxs-lookup"><span data-stu-id="19b36-231">SDK Sample</span></span>

<span data-ttu-id="19b36-232">Полный пример применения [**оболочки \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)см. в образце примера [Нотификатионикон](samples-notificationicon.md) в пакете средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="19b36-232">See the [NotificationIcon Sample](samples-notificationicon.md) sample in the Windows Software Development Kit (SDK) for a full example of the use of [**Shell\_NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona).</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b36-233">См. также</span><span class="sxs-lookup"><span data-stu-id="19b36-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b36-234">**Значок \_ NotifyIcon**</span><span class="sxs-lookup"><span data-stu-id="19b36-234">**Shell\_NotifyIcon**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona)
</dt> <dt>

[<span data-ttu-id="19b36-235">**Оболочка \_ нотификонжетрект**</span><span class="sxs-lookup"><span data-stu-id="19b36-235">**Shell\_NotifyIconGetRect**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect)
</dt> <dt>

[<span data-ttu-id="19b36-236">**нотификондата**</span><span class="sxs-lookup"><span data-stu-id="19b36-236">**NOTIFYICONDATA**</span></span>](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa)
</dt> <dt>

[<span data-ttu-id="19b36-237">**шкуерюсернотификатионстате**</span><span class="sxs-lookup"><span data-stu-id="19b36-237">**SHQueryUserNotificationState**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate)
</dt> <dt>

[<span data-ttu-id="19b36-238">**иусернотификатион**</span><span class="sxs-lookup"><span data-stu-id="19b36-238">**IUserNotification**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification)
</dt> <dt>

[<span data-ttu-id="19b36-239">**IUserNotification2**</span><span class="sxs-lookup"><span data-stu-id="19b36-239">**IUserNotification2**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2)
</dt> <dt>

[<span data-ttu-id="19b36-240">Панель задач</span><span class="sxs-lookup"><span data-stu-id="19b36-240">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="19b36-241">Расширения панели задач</span><span class="sxs-lookup"><span data-stu-id="19b36-241">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
