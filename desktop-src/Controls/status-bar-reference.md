---
title: Строка состояния
description: В этом разделе содержатся сведения об элементах программирования, используемых элементами управления "строка состояния".
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "103794767"
---
# <a name="status-bar"></a><span data-ttu-id="67f2d-103">Строка состояния</span><span class="sxs-lookup"><span data-stu-id="67f2d-103">Status Bar</span></span>

<span data-ttu-id="67f2d-104">В этом разделе содержатся сведения об элементах программирования, используемых элементами управления "строка состояния".</span><span class="sxs-lookup"><span data-stu-id="67f2d-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="67f2d-105">Разделы общих сведений</span><span class="sxs-lookup"><span data-stu-id="67f2d-105">Overviews</span></span>



| <span data-ttu-id="67f2d-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="67f2d-106">Topic</span></span>                          | <span data-ttu-id="67f2d-107">Содержимое</span><span class="sxs-lookup"><span data-stu-id="67f2d-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67f2d-108">Строки состояния</span><span class="sxs-lookup"><span data-stu-id="67f2d-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="67f2d-109">*Строка состояния* — это горизонтальное окно в нижней части родительского окна, в котором приложение может отображать различные типы сведений о состоянии.</span><span class="sxs-lookup"><span data-stu-id="67f2d-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="67f2d-110">Функции</span><span class="sxs-lookup"><span data-stu-id="67f2d-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67f2d-111">Раздел</span><span class="sxs-lookup"><span data-stu-id="67f2d-111">Topic</span></span></th>
<th><span data-ttu-id="67f2d-112">Содержимое</span><span class="sxs-lookup"><span data-stu-id="67f2d-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="67f2d-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>креатестатусвиндов</strong></a></span><span class="sxs-lookup"><span data-stu-id="67f2d-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="67f2d-114">Создает окно состояния, которое обычно используется для вывода состояния приложения.</span><span class="sxs-lookup"><span data-stu-id="67f2d-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="67f2d-115">Окно обычно отображается в нижней части родительского окна и содержит указанный текст.</span><span class="sxs-lookup"><span data-stu-id="67f2d-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="67f2d-116">Эта функция является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="67f2d-116">This function is obsolete.</span></span> <span data-ttu-id="67f2d-117">Вместо этого используйте <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="67f2d-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="67f2d-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>дравстатустекст</strong></a></span><span class="sxs-lookup"><span data-stu-id="67f2d-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="67f2d-119">Функция <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>дравстатустекст</strong></a> Рисует указанный текст в стиле окна состояния с границами.</span><span class="sxs-lookup"><span data-stu-id="67f2d-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="67f2d-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>менухелп</strong></a></span><span class="sxs-lookup"><span data-stu-id="67f2d-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="67f2d-121">Обрабатывает <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> и <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> сообщения, а также отображает текст справки о текущем меню в указанном окне состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="67f2d-122">Сообщения</span><span class="sxs-lookup"><span data-stu-id="67f2d-122">Messages</span></span>



| <span data-ttu-id="67f2d-123">Раздел</span><span class="sxs-lookup"><span data-stu-id="67f2d-123">Topic</span></span>                                               | <span data-ttu-id="67f2d-124">Содержимое</span><span class="sxs-lookup"><span data-stu-id="67f2d-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67f2d-125">**SB — \_ границы**</span><span class="sxs-lookup"><span data-stu-id="67f2d-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="67f2d-126">Извлекает текущие значения ширины горизонтальных и вертикальных границ окна состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="67f2d-127">**\_значок SB**</span><span class="sxs-lookup"><span data-stu-id="67f2d-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="67f2d-128">Возвращает значок для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="67f2d-129">**SB \_**</span><span class="sxs-lookup"><span data-stu-id="67f2d-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="67f2d-130">Извлекает количество частей в окне состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="67f2d-131">Сообщение также получает координату правого края указанного числа частей.</span><span class="sxs-lookup"><span data-stu-id="67f2d-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="67f2d-132">**SB \_**</span><span class="sxs-lookup"><span data-stu-id="67f2d-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="67f2d-133">Извлекает ограничивающий прямоугольник части в окне состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="67f2d-134">**SB ( \_ SMS)**</span><span class="sxs-lookup"><span data-stu-id="67f2d-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="67f2d-135">Сообщение [**SB \_ gettext**](sb-gettext.md) извлекает текст из указанной части окна состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="67f2d-136">**SB \_ жеттекстленгс**</span><span class="sxs-lookup"><span data-stu-id="67f2d-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="67f2d-137">Сообщение [**SB \_ жеттекстленгс**](sb-gettextlength.md) извлекает длину текста (в символах) из указанной части окна состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="67f2d-138">**SB \_ жеттиптекст**</span><span class="sxs-lookup"><span data-stu-id="67f2d-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="67f2d-139">Извлекает текст подсказки для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="67f2d-140">Чтобы включить подсказки, необходимо создать строку состояния с помощью стиля [**\_ подсказок SBT**](status-bar-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="67f2d-141">**SB \_ жетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="67f2d-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="67f2d-142">Возвращает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="67f2d-143">**SB — \_ простой**</span><span class="sxs-lookup"><span data-stu-id="67f2d-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="67f2d-144">Проверяет, находится ли элемент управления "строка состояния" в простом режиме.</span><span class="sxs-lookup"><span data-stu-id="67f2d-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="67f2d-145">**SB \_ сетбкколор**</span><span class="sxs-lookup"><span data-stu-id="67f2d-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="67f2d-146">Задает цвет фона в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="67f2d-147">**SB \_ сетикон**</span><span class="sxs-lookup"><span data-stu-id="67f2d-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="67f2d-148">Задает значок для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="67f2d-149">**SB \_ сетминхеигхт**</span><span class="sxs-lookup"><span data-stu-id="67f2d-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="67f2d-150">Задает минимальную высоту области отображения окна состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="67f2d-151">**SB \_ сетпартс**</span><span class="sxs-lookup"><span data-stu-id="67f2d-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="67f2d-152">Задает количество частей в окне состояния и координату правого края каждой части.</span><span class="sxs-lookup"><span data-stu-id="67f2d-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="67f2d-153">**SB \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="67f2d-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="67f2d-154">Сообщение SB \_ SETTEXT задает текст в указанной части окна состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="67f2d-155">**SB \_ сеттиптекст**</span><span class="sxs-lookup"><span data-stu-id="67f2d-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="67f2d-156">Задает текст подсказки для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="67f2d-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="67f2d-157">Чтобы включить подсказки, строка состояния должна быть создана с помощью стиля [**\_ подсказок SBT**](status-bar-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="67f2d-158">**SB \_ сетуникодеформат**</span><span class="sxs-lookup"><span data-stu-id="67f2d-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="67f2d-159">Задает флаг формата символов Юникода для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="67f2d-160">Это сообщение позволяет изменить кодировку, используемую элементом управления во время выполнения, вместо того, чтобы повторно создавать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="67f2d-161">**SB \_ Simple**</span><span class="sxs-lookup"><span data-stu-id="67f2d-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="67f2d-162">Указывает, отображает ли окно состояния простой текст или отображает все фрагменты окна, заданные предыдущим сообщением [**SB \_ сетпартс**](sb-setparts.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="67f2d-163">Уведомления</span><span class="sxs-lookup"><span data-stu-id="67f2d-163">Notifications</span></span>



| <span data-ttu-id="67f2d-164">Раздел</span><span class="sxs-lookup"><span data-stu-id="67f2d-164">Topic</span></span>                                                 | <span data-ttu-id="67f2d-165">Содержимое</span><span class="sxs-lookup"><span data-stu-id="67f2d-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67f2d-166">NM \_ Click (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="67f2d-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="67f2d-167">Сообщает родительскому окну элемента управления "строка состояния", что пользователь щелкнул левой кнопкой мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="67f2d-168">[NM \_ Щелкните (строка состояния)](nm-click-status-bar.md) отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="67f2d-169">NM \_ дблклк (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="67f2d-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="67f2d-170">Сообщает родительскому окну элемента управления "строка состояния", что пользователь дважды щелкнул левую кнопку мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="67f2d-171">Это уведомление отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="67f2d-172">NM \_ ркликк (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="67f2d-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="67f2d-173">Сообщает родительскому окну элемента управления "строка состояния", что пользователь щелкнул правой кнопкой мыши в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="67f2d-174">Это уведомление отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="67f2d-175">NM \_ рдблклк (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="67f2d-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="67f2d-176">Уведомляет родительские окна элемента управления "строка состояния", что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="67f2d-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="67f2d-177">[NM \_ РДБЛКЛК (строка состояния)](nm-rdblclk-status-bar.md) отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="67f2d-178">СБН \_ симплемодечанже</span><span class="sxs-lookup"><span data-stu-id="67f2d-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="67f2d-179">Посылается элементом управления "строка состояния" при изменении простого режима из-за [**\_ простого сообщения SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="67f2d-180">Это уведомление отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="67f2d-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="67f2d-181">Константы</span><span class="sxs-lookup"><span data-stu-id="67f2d-181">Constants</span></span>



| <span data-ttu-id="67f2d-182">Раздел</span><span class="sxs-lookup"><span data-stu-id="67f2d-182">Topic</span></span>                                      | <span data-ttu-id="67f2d-183">Содержимое</span><span class="sxs-lookup"><span data-stu-id="67f2d-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67f2d-184">Стили строки состояния</span><span class="sxs-lookup"><span data-stu-id="67f2d-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="67f2d-185">В этом разделе перечислены стили в дополнение к стандартным стилям окна, поддерживаемым элементами управления " *строка состояния* ".</span><span class="sxs-lookup"><span data-stu-id="67f2d-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

