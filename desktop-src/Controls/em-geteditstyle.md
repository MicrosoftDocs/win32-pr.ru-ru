---
title: Сообщение EM_GETEDITSTYLE (RichEdit. h)
description: Извлекает текущие флаги изменения стиля.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- Элементы управления Windows для EM_GETEDITSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9264338ea525cc0165e1ed942d90654b95357b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071739"
---
# <a name="em_geteditstyle-message"></a><span data-ttu-id="6cdcc-104">\_Сообщение ЖЕТЕДИТСТИЛЕ EM</span><span class="sxs-lookup"><span data-stu-id="6cdcc-104">EM\_GETEDITSTYLE message</span></span>

<span data-ttu-id="6cdcc-105">Извлекает текущие флаги изменения стиля.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-105">Retrieves the current edit style flags.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cdcc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6cdcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cdcc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6cdcc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdcc-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6cdcc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6cdcc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6cdcc-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cdcc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6cdcc-111">Return value</span></span>

<span data-ttu-id="6cdcc-112">Возвращает текущие флаги изменения стиля, которые могут включать одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6cdcc-112">Returns the current edit style flags, which can include one or more of the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cdcc-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6cdcc-113">Return code</span></span></th>
<th><span data-ttu-id="6cdcc-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6cdcc-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-115"><dt><strong>SES_BEEPONMAXTEXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-116">Расширенное редактирование вызовет системный звуковой сигнал, если пользователь пытается ввести больше максимального числа символов.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-116">Rich Edit will call the system beeper if the user attempts to enter more than the maximum characters.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-117"><dt><strong>SES_BIDI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-117"><dt><strong>SES_BIDI</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-118">Включает двунаправленную обработку.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-118">Turns on bidirectional processing.</span></span> <span data-ttu-id="6cdcc-119">Этот параметр автоматически включается с помощью расширенного редактирования, если доступны следующие стили окна: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-119">This is automatically turned on by Rich Edit if any of the following window styles are active: <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>.</span></span> <span data-ttu-id="6cdcc-120">Однако этот параметр полезен для обработки этих стилей окна при использовании пользовательской реализации <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>итекссост</strong></a> (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-120">However, this setting is useful for handling these window styles when using a custom implementation of <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-121"><dt><strong>SES_CTFALLOWEMBED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-122"><strong>Windows XP с пакетом обновления 1 (SP1</strong>): разрешить вставку внедренных объектов с помощью TSF (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-122"><strong>Windows XP with SP1</strong>: Allow embedded objects to be inserted using TSF (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-123"><dt><strong>SES_CTFALLOWPROOFING</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-124"><strong>Windows XP с пакетом обновления 1 (SP1</strong>): разрешает советы по проверке правописания TSF (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-124"><strong>Windows XP with SP1</strong>: Allows TSF proofing tips (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-125"><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-126"><strong>Windows XP с пакетом обновления 1 (SP1</strong>): разрешает советы SMARTTAG для TSF (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-126"><strong>Windows XP with SP1</strong>: Allows TSF SmartTag tips (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-127"><dt><strong>SES_CTFNOLOCK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-128"><strong>Windows 8</strong>: не разрешать доступ на чтение и запись для блокировки TSF.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-128"><strong>Windows 8</strong>: Do not allow the TSF lock read/write access.</span></span> <span data-ttu-id="6cdcc-129">Это приостанавливает ввод TSF.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-129">This pauses TSF input.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-130"><dt><strong>SES_DEFAULTLATINLIGA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-131"><strong>Windows 8</strong>: шрифты с лигатурой типа "Fi" отображаются с функциями OpenType по умолчанию, что приводит к улучшенному оформлению (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-131"><strong>Windows 8</strong>: Fonts with an fi ligature are displayed with default OpenType features resulting in improved typography (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-132"><dt><strong>SES_DRAFTMODE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-133"><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: использовать шрифты режима черновика для вывода текста.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-133"><strong>Windows XP with SP1</strong>: Use draft mode fonts to display text.</span></span> <span data-ttu-id="6cdcc-134">Режим черновика является параметром специальных возможностей, в котором элемент управления отображает текст с одним шрифтом. шрифт определяется параметром системы для шрифта, используемого в окнах сообщений.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-134">Draft mode is an accessibility option where the control displays the text with a single font; the font is determined by the system setting for the font used in message boxes.</span></span> <span data-ttu-id="6cdcc-135">Например, доступные пользователи могут читать текст проще, если он является однородным, а не сочетанием шрифтов и стилей (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-135">For example, accessible users may read text easier if it is uniform, rather than a mix of fonts and styles (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-136"><dt><strong>SES_EMULATE10</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-136"><dt><strong>SES_EMULATE10</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-137"><strong>Windows 8</strong>: Эмуляция поведения RichEdit 1,0.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-137"><strong>Windows 8</strong>: Emulate RichEdit 1.0 behavior.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6cdcc-138">Если вы действительно хотите это поведение, используйте riched32.dll Windows вместо riched20.dll или msftedit.dll.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-138">If you really want this behavior, use the Windows riched32.dll instead of riched20.dll or msftedit.dll.</span></span> <span data-ttu-id="6cdcc-139">Riched32.dll имеет больше функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-139">Riched32.dll had more functionality.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-140"><dt><strong>SES_EMULATESYSEDIT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-141">Если этот бит включен, широкие возможности редактирования попытаются эмулировать элемент управления "изменение системы" (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-141">When this bit is on, rich edit attempts to emulate the system edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-142"><dt><strong>SES_EXTENDBACKCOLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-143">Расширяет цвет фона до границ прямоугольника клиента (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-143">Extends the background color all the way to the edges of the client rectangle (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-144"><dt><strong>SES_HIDEGRIDLINES</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-145"><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: Если ширина линий сетки таблицы равна нулю, линии сетки не отображаются.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-145"><strong>Windows XP with SP1</strong>: If the width of table gridlines is zero, gridlines are not displayed.</span></span> <span data-ttu-id="6cdcc-146">Это эквивалентно функции скрыть сетку в меню таблицы Word (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-146">This is equivalent to the hide gridlines feature in Word's table menu (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-147"><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-148"><strong>Windows 8</strong>: когда курсор наведен на ссылку, отобразится подсказка с адресом целевой ссылки (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-148"><strong>Windows 8</strong>: When the cursor is over a link, display a tooltip with the target link address (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-149"><dt><strong>SES_LOGICALCARET</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-150"><strong>Windows 8</strong>: укажите логическую информацию о курсоре вместо точечного рисунка курсора, как описано в <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>Итекссост:: ткссеткаретпос</strong></a> (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-150"><strong>Windows 8</strong>: Provide logical caret information instead of a caret bitmap as described in <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost::TxSetCaretPos</strong></a> (default: 0).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-151"><dt><strong>SES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-151"><dt><strong>SES_LOWERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-152">Преобразует все входные символы в нижний регистр (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-152">Converts all input characters to lowercase (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-153"><dt><strong>SES_MAPCPS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-153"><dt><strong>SES_MAPCPS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-154">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-154">Obsolete.</span></span> <span data-ttu-id="6cdcc-155">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-155">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-156"><dt><strong>SES_MULTISELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-156"><dt><strong>SES_MULTISELECT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-157"><strong>Windows 8</strong>. Включение множественного выбора с индивидуальным выбором мыши при нажатии клавиши Ctrl (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-157"><strong>Windows 8</strong>: Enable multiselection with individual mouse selections made while the Ctrl key is pressed (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-158"><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-159"><strong>Windows 8</strong>: не изменять высоту строки для восточно-азиатского текста (по умолчанию: 0, что регулирует высоту линии на 15%).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-159"><strong>Windows 8</strong>: Do not adjust line height for East Asian text (default: 0 which adjusts the line height by 15%).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-160"><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-161">Отправляет <a href="en-link.md">EN_LINK</a> уведомления о ссылках, которые не имеют фокуса.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-161">Sends <a href="en-link.md">EN_LINK</a> notification from links that do not have focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-162"><dt><strong>SES_NOIME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-162"><dt><strong>SES_NOIME</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-163">Запрещает редакторы IME для данного экземпляра элемента управления Rich Edit (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-163">Disallows IMEs for this instance of the rich edit control (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-164"><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-165">Если этот бит включен, то Расширенное редактирование не проверяет последовательность введенного текста.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-165">When this bit is on, rich edit does not verify the sequence of typed text.</span></span> <span data-ttu-id="6cdcc-166">Для некоторых языков (например, тайского и вьетнамского) требуется проверка порядка входных последовательностей перед их отправкой в резервное хранилище (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-166">Some languages (such as Thai and Vietnamese) require verifying the input sequence order before submitting it to the backing store (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-167"><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-168">Когда происходит Киллфокус, прокрутите до начала текста (позиции символа, равной 0) (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-168">When KillFocus occurs, scroll to the beginning of the text (character position equal to 0) (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-169"><dt><strong>SES_SMARTDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-170"><strong>Windows 8</strong>: Добавление или удаление пробела в соответствии с контекстом при перетаскивании текста (значение по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-170"><strong>Windows 8</strong>: Add or delete a space according to the context when dropping text (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-171"><dt><strong>SES_USECRLF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-171"><dt><strong>SES_USECRLF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-172">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-172">Obsolete.</span></span> <span data-ttu-id="6cdcc-173">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-173">Do not use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-174"><dt><strong>SES_WORDDRAGDROP</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-175"><strong>Windows 8</strong>. Если выбран параметр Word SELECT, убедитесь, что расположение сброса находится на границе слова (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-175"><strong>Windows 8</strong>: If word select is active, ensure that the drop location is at a word boundary (default: 0).</span></span> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-176"><dt><strong>SES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-176"><dt><strong>SES_UPPERCASE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-177">Преобразует все входные символы в верхний регистр (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-177">Converts all input characters to uppercase (default: 0).</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-178"><dt><strong>SES_USEAIMM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-178"><dt><strong>SES_USEAIMM</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-179">Использует компонент активного входного метода IMM, поставляемый с Internet Explorer 4,0 или более поздней версии (по умолчанию: 0).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-179">Uses the Active IMM input method component that ships with Internet Explorer 4.0 or later (default: 0).</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-180"><dt><strong>SES_USEATFONT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-180"><dt><strong>SES_USEATFONT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-181"><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: использует шрифт @, предназначенный для вертикального текста; Он используется с стилем окна <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6cdcc-181"><strong>Windows XP with SP1</strong>: Uses an @ font, which is designed for vertical text; this is used with the <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> window style.</span></span> <span data-ttu-id="6cdcc-182">Имя @ Font начинается с символа @, например &quot; @Batang &quot; (по умолчанию: 0, но автоматически включается для вертикального макета текста).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-182">The name of an @ font begins with the @ symbol, for example, &quot;@Batang&quot; (default: 0, but is automatically turned on for vertical text layout).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="6cdcc-183"><dt><strong>SES_USECTF</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-183"><dt><strong>SES_USECTF</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-184"><strong>Windows XP с пакетом обновления 1 (SP1)</strong>: включает поддержку TSF.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-184"><strong>Windows XP with SP1</strong>: Turns on TSF support.</span></span> <span data-ttu-id="6cdcc-185">(по умолчанию: 0)</span><span class="sxs-lookup"><span data-stu-id="6cdcc-185">(default: 0)</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="6cdcc-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="6cdcc-186"><dt><strong>SES_XLTCRCRLFTOCR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="6cdcc-187">Включает перевод Кркрлфс в CR.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-187">Turns on translation of CRCRLFs to CRs.</span></span> <span data-ttu-id="6cdcc-188">Если этот бит включен и файл считывается в, все экземпляры КРКРЛФ будут внутренне преобразованы в жесткие запросы CR.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-188">When this bit is on and a file is read in, all instances of CRCRLF will be converted to hard CRs internally.</span></span> <span data-ttu-id="6cdcc-189">Это повлияет на перенос текста.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-189">This will affect the text wrapping.</span></span> <span data-ttu-id="6cdcc-190">Обратите внимание, что если такой файл сохраняется в виде обычного текста, запросы CR будут заменены символами CRLF.</span><span class="sxs-lookup"><span data-stu-id="6cdcc-190">Note that if such a file is saved as plain text, the CRs will be replaced by CRLFs.</span></span> <span data-ttu-id="6cdcc-191">Это стандарт txt для обычного текста (по умолчанию: 0, который удаляет Кркрлфс на входе).</span><span class="sxs-lookup"><span data-stu-id="6cdcc-191">This is the .txt standard for plain text (default: 0, which deletes CRCRLFs on input).</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6cdcc-192">Требования</span><span class="sxs-lookup"><span data-stu-id="6cdcc-192">Requirements</span></span>



| <span data-ttu-id="6cdcc-193">Требование</span><span class="sxs-lookup"><span data-stu-id="6cdcc-193">Requirement</span></span> | <span data-ttu-id="6cdcc-194">Значение</span><span class="sxs-lookup"><span data-stu-id="6cdcc-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cdcc-195">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6cdcc-195">Minimum supported client</span></span><br/> | <span data-ttu-id="6cdcc-196">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6cdcc-196">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6cdcc-197">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6cdcc-197">Minimum supported server</span></span><br/> | <span data-ttu-id="6cdcc-198">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6cdcc-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6cdcc-199">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6cdcc-199">Redistributable</span></span><br/>          | <span data-ttu-id="6cdcc-200">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="6cdcc-200">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="6cdcc-201">Header</span><span class="sxs-lookup"><span data-stu-id="6cdcc-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="6cdcc-202"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cdcc-202"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cdcc-203">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6cdcc-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cdcc-204">**EM \_ сетедитстиле**</span><span class="sxs-lookup"><span data-stu-id="6cdcc-204">**EM\_SETEDITSTYLE**</span></span>](em-seteditstyle.md)
</dt> </dl>

 

