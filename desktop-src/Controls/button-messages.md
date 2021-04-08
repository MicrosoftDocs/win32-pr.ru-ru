---
title: 'Сообщения кнопки '
description: Кнопка может отправить сообщения в свое родительское окно, а родительское окно может посылать сообщения кнопке.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103796681"
---
# <a name="button-messages"></a><span data-ttu-id="04786-103">Сообщения кнопки </span><span class="sxs-lookup"><span data-stu-id="04786-103">Button Messages</span></span>

<span data-ttu-id="04786-104">Кнопка может отправить сообщения в свое родительское окно, а родительское окно может посылать сообщения кнопке.</span><span class="sxs-lookup"><span data-stu-id="04786-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="04786-105">В этом разделе рассматриваются следующие темы.</span><span class="sxs-lookup"><span data-stu-id="04786-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="04786-106">Отправка сообщений на кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="04786-107">Обработка сообщений с помощью кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="04786-108">Сообщения с уведомлениями от кнопок</span><span class="sxs-lookup"><span data-stu-id="04786-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="04786-109">Цветовые сообщения для кнопок</span><span class="sxs-lookup"><span data-stu-id="04786-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="04786-110">Обработка сообщений по умолчанию для кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="04786-111">См. также</span><span class="sxs-lookup"><span data-stu-id="04786-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="04786-112">Отправка сообщений на кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="04786-113">Родительское окно может отсылать сообщения кнопке в перекрытом или дочернем окне с помощью функции [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , а также передавать сообщения кнопке в диалоговом окне с помощью функций [**сенддлгитеммессаже**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**чеккдлгбуттон**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**чеккрадиобуттон**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)и [**исдлгбуттончеккед**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .</span><span class="sxs-lookup"><span data-stu-id="04786-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="04786-114">Приложение может использовать сообщение [**BM- \_ Check**](bm-getcheck.md) для получения состояния флажка или переключателя.</span><span class="sxs-lookup"><span data-stu-id="04786-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="04786-115">Приложение может также использовать сообщение [**BM- \_ State**](bm-getstate.md) для получения текущих состояний кнопки (состояние проверки, состояние отправки и состояние фокусировки).</span><span class="sxs-lookup"><span data-stu-id="04786-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="04786-116">Чтобы получить сведения о конкретном состоянии, используйте битовую маску в возвращенном значении состояния.</span><span class="sxs-lookup"><span data-stu-id="04786-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="04786-117">Сообщение [**BM \_ сетчекк**](bm-setcheck.md) устанавливает состояние флажка или переключателя; сообщение возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="04786-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="04786-118">Сообщение [**BM \_ SETSTATE**](bm-setstate.md) устанавливает состояние принудительной отправки кнопки; это сообщение также возвращает ноль.</span><span class="sxs-lookup"><span data-stu-id="04786-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="04786-119">Сообщение [**BM \_ SETSTYLE**](bm-setstyle.md) изменяет стиль кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="04786-120">Он предназначен для изменения стилей кнопок в типе (например, при изменении флажка на автоматический флажок).</span><span class="sxs-lookup"><span data-stu-id="04786-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="04786-121">Он не предназначен для изменения типов (например, изменения флажка для переключателя).</span><span class="sxs-lookup"><span data-stu-id="04786-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="04786-122">Приложение не должно изменять тип кнопки с одного типа на другой.</span><span class="sxs-lookup"><span data-stu-id="04786-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="04786-123">Кнопка в стиле [**\_ точечный рисунок BS**](button-styles.md) или [**\_ значок BS**](button-styles.md) отображает точечный рисунок или значок, а не текст.</span><span class="sxs-lookup"><span data-stu-id="04786-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="04786-124">Сообщение [**BM \_ сетимаже**](bm-setimage.md) связывает маркер с растровым изображением или значком с помощью кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="04786-125">Сообщение [**BM- \_ Image**](bm-getimage.md) получает маркер для растрового изображения или значка, связанного с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="04786-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="04786-126">Приложение также может использовать сообщение [**DM \_ жетдефид**](/windows/desktop/dlgbox/dm-getdefid) для получения идентификатора элемента управления "кнопка по умолчанию" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="04786-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="04786-127">Приложение может использовать сообщение [**DM \_ сетдефид**](/windows/desktop/dlgbox/dm-setdefid) для установки кнопки отправки по умолчанию для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="04786-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="04786-128">Вызов функции [**чеккдлгбуттон**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) или [**чеккрадиобуттон**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) эквивалентен отправке сообщения [**BM \_ сетчекк**](bm-setcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="04786-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="04786-129">Вызов функции [**исдлгбуттончеккед**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) эквивалентен отправке сообщения [**BM- \_ Check**](bm-getcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="04786-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="04786-130">Обработка сообщений с помощью кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-130">Handling Messages from a Button</span></span>

<span data-ttu-id="04786-131">Уведомления из кнопки отправляются в виде [**\_ команды WM**](/windows/desktop/menurc/wm-command) или [**\_ уведомления WM notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="04786-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="04786-132">Сведения об используемом сообщении можно найти на справочной странице для каждого уведомления.</span><span class="sxs-lookup"><span data-stu-id="04786-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="04786-133">Дополнительные сведения об обработке сообщений см. в разделе [Управление сообщениями](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="04786-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="04786-134">См. также сообщения кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="04786-135">Сообщения с уведомлениями от кнопок</span><span class="sxs-lookup"><span data-stu-id="04786-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="04786-136">Когда пользователь нажимает кнопку, ее состояние изменяется, а кнопка отправляет коды уведомлений в виде [**\_ командных сообщений WM**](/windows/desktop/menurc/wm-command) в родительское окно.</span><span class="sxs-lookup"><span data-stu-id="04786-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="04786-137">Например, элемент управления "Кнопка отправки" отправляет [млрд долл \_ щелчком](bn-clicked.md) код уведомления каждый раз, когда пользователь нажимает кнопку.</span><span class="sxs-lookup"><span data-stu-id="04786-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="04786-138">Во всех случаях (за исключением служб [BCN \_ хотитемчанже](bcn-hotitemchange.md)) слово с низким порядком в параметре *wParam* содержит идентификатор элемента управления, а слово с высоким порядком *wParam* содержит код уведомления, а параметр *lParam* содержит управляющий маркер окна.</span><span class="sxs-lookup"><span data-stu-id="04786-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="04786-139">Как сообщение, так и ответ родительского окна зависят от типа, стиля и текущего состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="04786-140">Ниже приведены коды уведомлений для кнопок, которые должны отслеживать и обрабатываться приложением.</span><span class="sxs-lookup"><span data-stu-id="04786-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="04786-141">Код уведомления</span><span class="sxs-lookup"><span data-stu-id="04786-141">Notification code</span></span>                                                        | <span data-ttu-id="04786-142">Описание</span><span class="sxs-lookup"><span data-stu-id="04786-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="04786-143">\_ХОТИТЕМЧАНЖЕ BCN</span><span class="sxs-lookup"><span data-stu-id="04786-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="04786-144">Мышь, которая была нажата или оставлена в клиентской области кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="04786-145">\_щелчок млрд долл</span><span class="sxs-lookup"><span data-stu-id="04786-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="04786-146">Пользователь щелкнул кнопку.</span><span class="sxs-lookup"><span data-stu-id="04786-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="04786-147">[Млрд долл \_ ДБЛКЛК](bn-dblclk.md) или [млрд долл \_ даублекликкед](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="04786-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="04786-148">Пользователь дважды щелкнул кнопку.</span><span class="sxs-lookup"><span data-stu-id="04786-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="04786-149">\_Отключение млрд долл</span><span class="sxs-lookup"><span data-stu-id="04786-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="04786-150">Кнопка отключена.</span><span class="sxs-lookup"><span data-stu-id="04786-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="04786-151">[Млрд долл \_ ОТПРАВЛЕНные](bn-pushed.md) или [млрд долл \_ хилите](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="04786-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="04786-152">Пользователь отправил кнопку.</span><span class="sxs-lookup"><span data-stu-id="04786-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="04786-153">МЛРД долл \_ киллфокус</span><span class="sxs-lookup"><span data-stu-id="04786-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="04786-154">Кнопка потеряла фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="04786-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="04786-155">МЛРД долл \_ Заливка</span><span class="sxs-lookup"><span data-stu-id="04786-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="04786-156">Кнопка должна быть окрашена.</span><span class="sxs-lookup"><span data-stu-id="04786-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="04786-157">МЛРД долл \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="04786-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="04786-158">Кнопка получила фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="04786-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="04786-159">[Млрд долл \_ Unpushd](bn-unpushed.md) или [млрд долл \_ унхилите](bn-unhilite.md)</span><span class="sxs-lookup"><span data-stu-id="04786-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="04786-160">Кнопка больше не помещается.</span><span class="sxs-lookup"><span data-stu-id="04786-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="04786-161">Кнопка отправляет [млрд долл \_ Disable](bn-disable.md), [млрд долл \_](bn-pushed.md) [ \_ pushd](bn-unpushed.md) , [млрд долл \_ киллфокус](bn-killfocus.md), [млрд долл \_ Paint](bn-paint.md), [млрд долл \_ SETFOCUS](bn-setfocus.md)и млрд долл неотправленные коды уведомлений только в том случае, если у него есть стиль [**\_ уведомления BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="04786-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="04786-162">[Млрд долл \_](bn-dblclk.md) Коды уведомлений дблклк отправляются автоматически для кнопок [**BS \_ усербуттон**](button-styles.md), [**BS \_**](button-styles.md)и [**BS \_ овнердрав**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="04786-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="04786-163">Другие типы кнопок отправляют млрд долл \_ дблклк только в том случае, если они имеют стиль " **BS \_** ".</span><span class="sxs-lookup"><span data-stu-id="04786-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="04786-164">Все кнопки отправляют [млрд долл \_ нажатый](bn-clicked.md) код уведомления, независимо от стилей их кнопок.</span><span class="sxs-lookup"><span data-stu-id="04786-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="04786-165">Для автоматических кнопок система изменяет состояние принудительной отправки и закрашивает кнопку.</span><span class="sxs-lookup"><span data-stu-id="04786-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="04786-166">В этом случае приложение обычно обрабатывает только млрд доллные коды уведомлений о [ \_ нажатии](bn-clicked.md) и [млрд долл \_ дблклк](bn-dblclk.md) .</span><span class="sxs-lookup"><span data-stu-id="04786-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="04786-167">Для неавтоматических кнопок приложение обычно отвечает на код уведомления, отправляя сообщение для изменения состояния кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="04786-168">Дополнительные сведения об отправке сообщений кнопкам см. [в разделе Отправка сообщений на кнопки](#sending-messages-to-buttons).</span><span class="sxs-lookup"><span data-stu-id="04786-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="04786-169">Когда пользователь выбирает рисуемую пользователем кнопку, кнопка отправляет родительское окно сообщение [**WM \_ DRAWITEM**](wm-drawitem.md) , содержащее идентификатор рисуемого элемента управления и сведения о его измерениях и состоянии.</span><span class="sxs-lookup"><span data-stu-id="04786-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="04786-170">Цветовые сообщения для кнопок</span><span class="sxs-lookup"><span data-stu-id="04786-170">Button Color Messages</span></span>

<span data-ttu-id="04786-171">Система предоставляет значения цвета по умолчанию для кнопок.</span><span class="sxs-lookup"><span data-stu-id="04786-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="04786-172">Приложение может получить значения по умолчанию для этих цветов, вызвав функцию [**жетсисколор**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) , или задать значения, вызвав функцию [**сетсисколорс**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="04786-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="04786-173">В следующей таблице показаны значения цвета кнопки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04786-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="04786-174">Значение</span><span class="sxs-lookup"><span data-stu-id="04786-174">Value</span></span>               | <span data-ttu-id="04786-175">Цвет элемента</span><span class="sxs-lookup"><span data-stu-id="04786-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04786-176">ЦВЕТ \_ бтнфаце</span><span class="sxs-lookup"><span data-stu-id="04786-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="04786-177">Лицевая кнопка.</span><span class="sxs-lookup"><span data-stu-id="04786-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="04786-178">ЦВЕТ \_ бтнхигхлигхт</span><span class="sxs-lookup"><span data-stu-id="04786-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="04786-179">Выделение области (верхняя и левая границы) кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="04786-180">ЦВЕТ \_ бтншадов</span><span class="sxs-lookup"><span data-stu-id="04786-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="04786-181">Область тени (Нижняя и правая границы) кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="04786-182">ЦВЕТ \_ бтнтекст</span><span class="sxs-lookup"><span data-stu-id="04786-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="04786-183">Обычный (несерый) текст в кнопках.</span><span class="sxs-lookup"><span data-stu-id="04786-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="04786-184">ЦВЕТ \_ грайтекст</span><span class="sxs-lookup"><span data-stu-id="04786-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="04786-185">Отключенный (серый) текст в кнопках.</span><span class="sxs-lookup"><span data-stu-id="04786-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="04786-186">Этот цвет имеет значение 0, если текущий драйвер экрана не поддерживает сплошной серый цвет.</span><span class="sxs-lookup"><span data-stu-id="04786-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="04786-187">\_окно цвета</span><span class="sxs-lookup"><span data-stu-id="04786-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="04786-188">Фон окна.</span><span class="sxs-lookup"><span data-stu-id="04786-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="04786-189">ЦВЕТ \_ WINDOWFRAME</span><span class="sxs-lookup"><span data-stu-id="04786-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="04786-190">Фреймы окна.</span><span class="sxs-lookup"><span data-stu-id="04786-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="04786-191">ЦВЕТная \_ WINDOWTEXT</span><span class="sxs-lookup"><span data-stu-id="04786-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="04786-192">Текст в Windows.</span><span class="sxs-lookup"><span data-stu-id="04786-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="04786-193">Однако вызов [**сетсисколорс**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) влияет на все приложения, поэтому не следует вызывать эту функцию для настройки кнопок приложения.</span><span class="sxs-lookup"><span data-stu-id="04786-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="04786-194">Система отправляет сообщение [**WM \_ ктлколорбтн**](wm-ctlcolorbtn.md) в родительское окно кнопки перед рисованием кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="04786-195">Это сообщение содержит маркер для контекста устройства кнопки и маркер дочернего окна.</span><span class="sxs-lookup"><span data-stu-id="04786-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="04786-196">Родительское окно может использовать эти маркеры для изменения цветов текста и фона кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="04786-197">Однако только рисуемые владельцем кнопки реагируют на родительское окно, обрабатывающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="04786-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="04786-198">Обработка сообщений по умолчанию для кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-198">Button Default Message Processing</span></span>

<span data-ttu-id="04786-199">Процедура окна для стандартного класса элемента управления "Кнопка" выполняет обработку по умолчанию для всех сообщений, которые не обрабатывает процедура элемента управления "Кнопка".</span><span class="sxs-lookup"><span data-stu-id="04786-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="04786-200">Когда процедура управления кнопками возвращает **false** для любого сообщения, предопределенная процедура окна проверяет сообщения и выполняет действия по умолчанию, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="04786-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04786-201">Сообщение</span><span class="sxs-lookup"><span data-stu-id="04786-201">Message</span></span></th>
<th><span data-ttu-id="04786-202">Действие по умолчанию</span><span class="sxs-lookup"><span data-stu-id="04786-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04786-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="04786-204">Отправляет кнопке <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> и <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> сообщение, а также отправляет родительское окно а <a href="bn-clicked.md">BN_CLICKED</a> код уведомления.</span><span class="sxs-lookup"><span data-stu-id="04786-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="04786-206">Возвращает состояние проверки кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="04786-208">Возвращает маркер для растрового изображения или значка, связанного с кнопкой, или <strong>значение NULL</strong> , если кнопка не имеет точечного рисунка или значка.</span><span class="sxs-lookup"><span data-stu-id="04786-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="04786-210">Возвращает текущее состояние проверки, состояние отправки и состояние фокуса кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="04786-212">Задает состояние проверки для всех стилей переключателей и флажков.</span><span class="sxs-lookup"><span data-stu-id="04786-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="04786-213">Если параметр <em>wParam</em> больше нуля для переключателей, то кнопке присваивается стиль <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="04786-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="04786-215">Связывает заданное изображение или маркер значка с кнопкой и возвращает маркер предыдущего точечного рисунка или значка.</span><span class="sxs-lookup"><span data-stu-id="04786-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="04786-217">Задает состояние принудительной отправки кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-217">Sets the push state of the button.</span></span> <span data-ttu-id="04786-218">Для кнопок, рисуемых владельцем, в родительское окно отправляется <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> сообщение, если изменилось состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="04786-220">Задает стиль кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-220">Sets the button style.</span></span> <span data-ttu-id="04786-221">Если неупорядоченное слово параметра <em>lParam</em> имеет <strong>значение true</strong>, кнопка перерисовывается.</span><span class="sxs-lookup"><span data-stu-id="04786-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="04786-223">Устанавливает флажок или автоматический флажок, когда пользователь нажимает клавиши "плюс" (+) или "равно" (=).</span><span class="sxs-lookup"><span data-stu-id="04786-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="04786-224">Очищает флажок или автоматический флажок, когда пользователь нажимает клавишу "минус" (–).</span><span class="sxs-lookup"><span data-stu-id="04786-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="04786-226">Закрашивает кнопку.</span><span class="sxs-lookup"><span data-stu-id="04786-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="04786-228">Стирает фон для рисуемых владельцем кнопок.</span><span class="sxs-lookup"><span data-stu-id="04786-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="04786-229">Фон других кнопок удаляется как часть <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> и <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> обработки.</span><span class="sxs-lookup"><span data-stu-id="04786-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="04786-231">Возвращает значения, которые указывают тип входных данных, обработанных процедурой кнопки по умолчанию, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="04786-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="04786-232">Стиль кнопки</span><span class="sxs-lookup"><span data-stu-id="04786-232">Button style</span></span></th>
<th><span data-ttu-id="04786-233">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04786-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04786-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="04786-235">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="04786-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="04786-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="04786-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="04786-239">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="04786-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="04786-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="04786-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="04786-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="04786-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="04786-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="04786-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="04786-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="04786-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="04786-249">Возвращает маркер текущего шрифта.</span><span class="sxs-lookup"><span data-stu-id="04786-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="04786-251">Помещает кнопку, если пользователь нажимает клавишу пробел.</span><span class="sxs-lookup"><span data-stu-id="04786-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="04786-253">Освобождает захват мыши для всех вариантов, кроме клавиши TAB.</span><span class="sxs-lookup"><span data-stu-id="04786-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="04786-255">Удаляет прямоугольник фокуса с кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="04786-256">Для кнопок push и кнопок по умолчанию прямоугольник фокуса становится недействительным.</span><span class="sxs-lookup"><span data-stu-id="04786-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="04786-257">Если кнопка имеет захват мыши, запись снимается, кнопка не нажата и все состояния отправки удаляются.</span><span class="sxs-lookup"><span data-stu-id="04786-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="04786-259">Отправляет <a href="bn-dblclk.md">BN_DBLCLK</a> код уведомления родительскому окну для переключателей и рисуемых владельцем кнопок.</span><span class="sxs-lookup"><span data-stu-id="04786-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="04786-260">Для других кнопок двойной щелчок обрабатывается как сообщение <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="04786-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="04786-262">Выделяется кнопка, если указатель мыши находится внутри прямоугольника клиента кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="04786-264">Освобождает захват мыши, если кнопка была захвачена мышью.</span><span class="sxs-lookup"><span data-stu-id="04786-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="04786-266">Выполняет то же действие, что и <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, если кнопка имеет захват мыши.</span><span class="sxs-lookup"><span data-stu-id="04786-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="04786-267">В противном случае никакие действия не выполняются.</span><span class="sxs-lookup"><span data-stu-id="04786-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="04786-269">Превращает любую кнопку <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> в кнопку <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="04786-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="04786-271">Возвращает ХТТРАНСПАРЕНТ, если элемент управления "Кнопка" является полем группы.</span><span class="sxs-lookup"><span data-stu-id="04786-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="04786-273">Рисует кнопку в соответствии со стилем и текущим состоянием.</span><span class="sxs-lookup"><span data-stu-id="04786-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="04786-275">Рисует прямоугольник фокуса на кнопке, чтобы получить фокус.</span><span class="sxs-lookup"><span data-stu-id="04786-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="04786-276">Для переключателей и автоматических переключателей родительскому окну отправляется <a href="bn-clicked.md">BN_CLICKED</a> код уведомления.</span><span class="sxs-lookup"><span data-stu-id="04786-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="04786-278">Задает новый шрифт и при необходимости обновляет окно.</span><span class="sxs-lookup"><span data-stu-id="04786-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04786-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="04786-280">Задает текст кнопки.</span><span class="sxs-lookup"><span data-stu-id="04786-280">Sets the text of the button.</span></span> <span data-ttu-id="04786-281">В случае поля группы сообщение заполняет существующий текст перед перерисовкой поля группы новым текстом.</span><span class="sxs-lookup"><span data-stu-id="04786-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04786-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="04786-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="04786-283">Освобождает захват мыши для всех вариантов, кроме клавиши TAB.</span><span class="sxs-lookup"><span data-stu-id="04786-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="04786-284">Предопределенная процедура окна передает все остальные сообщения функции [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) для обработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04786-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04786-285">См. также</span><span class="sxs-lookup"><span data-stu-id="04786-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04786-286">Управляющие сообщения</span><span class="sxs-lookup"><span data-stu-id="04786-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 