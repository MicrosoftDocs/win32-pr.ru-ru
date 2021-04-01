---
title: Управляющие сообщения
description: В этом разделе содержатся сведения о том, как сообщения Windows используются для взаимодействия с элементами управления.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103891297"
---
# <a name="control-messages"></a><span data-ttu-id="14d97-103">Управляющие сообщения</span><span class="sxs-lookup"><span data-stu-id="14d97-103">Control Messages</span></span>

<span data-ttu-id="14d97-104">В этом разделе содержатся сведения о том, как сообщения Windows используются для взаимодействия с элементами управления.</span><span class="sxs-lookup"><span data-stu-id="14d97-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="14d97-105">Обсуждаются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="14d97-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="14d97-106">Сообщения для стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="14d97-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="14d97-107">Уведомления из элементов управления</span><span class="sxs-lookup"><span data-stu-id="14d97-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="14d97-108">См. также</span><span class="sxs-lookup"><span data-stu-id="14d97-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="14d97-109">Сообщения для стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="14d97-109">Messages to Common Controls</span></span>

<span data-ttu-id="14d97-110">Так как стандартные элементы управления — Windows, приложение может взаимодействовать с ними с помощью общих сообщений Microsoft Win32, таких как [**WM- \_ Font**](/windows/desktop/winmsg/wm-getfont) или [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="14d97-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="14d97-111">Кроме того, класс окон для каждого стандартного элемента управления поддерживает набор сообщений, относящихся к конкретному элементу управления.</span><span class="sxs-lookup"><span data-stu-id="14d97-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="14d97-112">Как правило, приложение использует [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) или [**сенддлгитеммессаже**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) для передачи сообщений элементу управления (часто получение сведений в возвращаемом значении).</span><span class="sxs-lookup"><span data-stu-id="14d97-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="14d97-113">Некоторые стандартные элементы управления также имеют набор макросов, которые приложение может использовать вместо [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="14d97-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="14d97-114">Как правило, макросы проще использовать, чем функции.</span><span class="sxs-lookup"><span data-stu-id="14d97-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="14d97-115">Следующий пример кода извлекает текст выбранного элемента представления дерева, сначала с помощью необработанных сообщений, а второй — с помощью эквивалентных макросов.</span><span class="sxs-lookup"><span data-stu-id="14d97-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="14d97-116">Предположим, *HWND* является дескриптором окна управления.</span><span class="sxs-lookup"><span data-stu-id="14d97-116">Assume that *hwnd* is the handle of the control window.</span></span>


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



<span data-ttu-id="14d97-117">При внесении изменений в параметры системного цвета Windows отправляет сообщение [**WM \_ сисколорчанже**](/windows/desktop/gdi/wm-syscolorchange) всем окнам верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="14d97-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="14d97-118">Окно верхнего уровня должно пересылать сообщение **\_ сисколорчанже WM** в общие элементы управления. в противном случае элементы управления не будут уведомлены об изменении цвета.</span><span class="sxs-lookup"><span data-stu-id="14d97-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="14d97-119">Пересылка сообщения гарантирует, что цвета, используемые общими элементами управления, будут соответствовать значениям, используемым другими объектами пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="14d97-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="14d97-120">Например, элемент управления ToolBar использует цвет "трехмерные объекты" для рисования своих кнопок.</span><span class="sxs-lookup"><span data-stu-id="14d97-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="14d97-121">Если пользователь изменяет цвет трехмерного объекта, но сообщение **WM \_ сисколорчанже** не пересылается на панель инструментов, кнопки панели инструментов останутся в исходном цвете (или даже меняются на сочетание старого и нового цветов), а цвет других кнопок в системе изменится.</span><span class="sxs-lookup"><span data-stu-id="14d97-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="14d97-122">Уведомления из элементов управления</span><span class="sxs-lookup"><span data-stu-id="14d97-122">Notifications from Controls</span></span>

<span data-ttu-id="14d97-123">Элементы управления являются дочерними окнами, которые отправляют сообщения уведомления родительскому окну, когда события, обычно активируемые вводом от пользователя, происходят в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="14d97-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="14d97-124">Приложение использует эти уведомления для определения действия, которое пользователь хочет предпринять.</span><span class="sxs-lookup"><span data-stu-id="14d97-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="14d97-125">За исключением TrackBar, использующих [**сообщения \_ WM HSCROLL**](wm-hscroll.md) и [**WM \_ VSCROLL**](wm-vscroll.md) для уведомления родительского элемента об изменениях, общие элементы управления отправляют уведомления в виде [**\_ команды WM**](/windows/desktop/menurc/wm-command) или [**\_ уведомления WM notify**](wm-notify.md) , как указано в справочном разделе по уведомлению.</span><span class="sxs-lookup"><span data-stu-id="14d97-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="14d97-126">Как правило, более старые уведомления (те, которые были в API в течение длительного времени) используют **\_ команду WM**.</span><span class="sxs-lookup"><span data-stu-id="14d97-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="14d97-127">Параметр *lParam* для [**WM \_ Notify**](wm-notify.md) является адресом структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) или адресом более крупной структуры, включающей **NMHDR** в качестве первого элемента.</span><span class="sxs-lookup"><span data-stu-id="14d97-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="14d97-128">Структура содержит код уведомления и определяет общий элемент управления, который отправил сообщение уведомления.</span><span class="sxs-lookup"><span data-stu-id="14d97-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="14d97-129">Значение остальных элементов структуры, если таковое имеется, зависит от кода уведомления.</span><span class="sxs-lookup"><span data-stu-id="14d97-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="14d97-130">Каждый тип общего элемента управления имеет соответствующий набор кодов уведомления.</span><span class="sxs-lookup"><span data-stu-id="14d97-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="14d97-131">Общая библиотека элементов управления также предоставляет коды уведомлений, которые могут быть отправлены более чем одним типом общего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="14d97-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="14d97-132">Чтобы определить, какие коды уведомлений будут отправлены и какой формат они принимают, см. документацию по интересующему вас контролю.</span><span class="sxs-lookup"><span data-stu-id="14d97-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="14d97-133">Пример кода, демонстрирующий обработку сообщений [**WM \_ Notify**](wm-notify.md) , см. в справочном разделе по этому сообщению.</span><span class="sxs-lookup"><span data-stu-id="14d97-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14d97-134">См. также</span><span class="sxs-lookup"><span data-stu-id="14d97-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14d97-135">Справочник по общим элементам управления</span><span class="sxs-lookup"><span data-stu-id="14d97-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
