---
title: Стили элемента управления Edit (Winuser. h)
description: Чтобы создать элемент управления "поле ввода" с помощью функции CreateWindow или CreateWindowEx, укажите класс EDIT, соответствующие константы стиля окна и сочетание следующих стилей элемента управления Edit.
ms.assetid: 336c69b7-bc23-4b93-8968-ad63a1703385
topic_type:
- apiref
api_name:
- ES_AUTOHSCROLL
- ES_AUTOVSCROLL
- ES_CENTER
- ES_LEFT
- ES_LOWERCASE
- ES_MULTILINE
- ES_NOHIDESEL
- ES_NUMBER
- ES_OEMCONVERT
- ES_PASSWORD
- ES_READONLY
- ES_RIGHT
- ES_UPPERCASE
- ES_WANTRETURN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 9b255aee665c32f9a14be4946dee0122dad626bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648635"
---
# <a name="edit-control-styles"></a><span data-ttu-id="c7406-103">Изменить стили элемента управления</span><span class="sxs-lookup"><span data-stu-id="c7406-103">Edit Control Styles</span></span>

<span data-ttu-id="c7406-104">Чтобы создать элемент управления "поле ввода" с помощью функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , укажите класс Edit, соответствующие константы стиля окна и сочетание следующих стилей элемента управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-104">To create an edit control using the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specify the EDIT class, appropriate window style constants, and a combination of the following edit control styles.</span></span> <span data-ttu-id="c7406-105">После создания элемента управления эти стили нельзя изменить, за исключением указанных.</span><span class="sxs-lookup"><span data-stu-id="c7406-105">After the control has been created, these styles cannot be modified, except as noted.</span></span>

## <a name="example"></a><span data-ttu-id="c7406-106">Пример</span><span class="sxs-lookup"><span data-stu-id="c7406-106">Example</span></span>

```cpp
LRESULT MsgCreate(HWND hwnd, UINT uMessage, WPARAM wparam, LPARAM lparam)
{
    lparam;
    wparam;
    uMessage;

    // Create Edit control for typing to be sent to server
    if (NULL == (hOutWnd = CreateWindow("EDIT",
                           NULL,
                           WS_BORDER | WS_CHILD | WS_VISIBLE | WS_VSCROLL | ES_LEFT | 
                           ES_MULTILINE | ES_AUTOVSCROLL,
                           0,0,0,0,
                           hwnd,
                           (HMENU) ID_OUTBOX,
                           (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE),
                           NULL)))
        return FALSE;
    return TRUE;
}
```

<span data-ttu-id="c7406-107">Пример из [классической выборки Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) на сайте GitHub.</span><span class="sxs-lookup"><span data-stu-id="c7406-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/netds/winsock/ipxchat/IpxChat.c) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="c7406-108">Константы</span><span class="sxs-lookup"><span data-stu-id="c7406-108">Constants</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c7406-109">Константа</span><span class="sxs-lookup"><span data-stu-id="c7406-109">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c7406-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c7406-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ES_AUTOHSCROLL"></span><span id="es_autohscroll"></span><dl> <span data-ttu-id="c7406-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-111"><dt><strong>ES_AUTOHSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-112">Автоматически прокручивает текст вправо на 10 символов, когда пользователь вводит символ в конце строки.</span><span class="sxs-lookup"><span data-stu-id="c7406-112">Automatically scrolls text to the right by 10 characters when the user types a character at the end of the line.</span></span> <span data-ttu-id="c7406-113">Когда пользователь нажимает клавишу ВВОД, элемент управления прокручивает весь текст обратно в нулевое расположение.</span><span class="sxs-lookup"><span data-stu-id="c7406-113">When the user presses the ENTER key, the control scrolls all text back to position zero.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_AUTOVSCROLL"></span><span id="es_autovscroll"></span><dl> <span data-ttu-id="c7406-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-114"><dt><strong>ES_AUTOVSCROLL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-115">Автоматически прокручивает текст вверх на одну страницу, когда пользователь нажимает клавишу ВВОД в последней строке.</span><span class="sxs-lookup"><span data-stu-id="c7406-115">Automatically scrolls text up one page when the user presses the ENTER key on the last line.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_CENTER"></span><span id="es_center"></span><dl> <span data-ttu-id="c7406-116"><dt><strong>ES_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-116"><dt><strong>ES_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-117">Центрирование текста в однострочном или многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-117">Centers text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_LEFT"></span><span id="es_left"></span><dl> <span data-ttu-id="c7406-118"><dt><strong>ES_LEFT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-118"><dt><strong>ES_LEFT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-119">Выровняйте текст по левому полю.</span><span class="sxs-lookup"><span data-stu-id="c7406-119">Aligns text with the left margin.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_LOWERCASE"></span><span id="es_lowercase"></span><dl> <span data-ttu-id="c7406-120"><dt><strong>ES_LOWERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-120"><dt><strong>ES_LOWERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-121">Преобразует все символы в нижний регистр по мере их ввода в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c7406-121">Converts all characters to lowercase as they are typed into the edit control.</span></span><br/> <span data-ttu-id="c7406-122">Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c7406-122">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_MULTILINE"></span><span id="es_multiline"></span><dl> <span data-ttu-id="c7406-123"><dt><strong>ES_MULTILINE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-123"><dt><strong>ES_MULTILINE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-124">Задает многострочный элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-124">Designates a multiline edit control.</span></span> <span data-ttu-id="c7406-125">Значение по умолчанию — однострочный элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-125">The default is single-line edit control.</span></span> <br/> <span data-ttu-id="c7406-126">Если элемент управления "поле ввода" находится в диалоговом окне, то по умолчанию нажатием клавиши Ввод выполняется активация кнопки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7406-126">When the multiline edit control is in a dialog box, the default response to pressing the ENTER key is to activate the default button.</span></span> <span data-ttu-id="c7406-127">Чтобы использовать клавишу ВВОД в качестве возврата каретки, используйте стиль <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7406-127">To use the ENTER key as a carriage return, use the <a href="rich-edit-control-styles.md"><strong>ES_WANTRETURN</strong></a> style.</span></span><br/> <span data-ttu-id="c7406-128">Если элемент управления "поле ввода" не находится в диалоговом окне и указан стиль <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> , элемент управления "поле ввода" отображает как можно больше строк и прокручивает по вертикали, когда пользователь нажимает клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c7406-128">When the multiline edit control is not in a dialog box and the <a href="rich-edit-control-styles.md"><strong>ES_AUTOVSCROLL</strong></a> style is specified, the edit control shows as many lines as possible and scrolls vertically when the user presses the ENTER key.</span></span> <span data-ttu-id="c7406-129">Если не указать <strong>ES_AUTOVSCROLL</strong>, в элементе управления "поле ввода" отображается столько строк, сколько возможно, и звуковые сигналы, если пользователь нажмет клавишу ВВОД, когда больше не удастся отобразить какие бы то ни было строки.</span><span class="sxs-lookup"><span data-stu-id="c7406-129">If you do not specify <strong>ES_AUTOVSCROLL</strong>, the edit control shows as many lines as possible and beeps if the user presses the ENTER key when no more lines can be displayed.</span></span><br/> <span data-ttu-id="c7406-130">Если указать стиль <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> , то многострочный элемент управления "поле ввода" автоматически прокручивается горизонтально, когда курсор выходит за правый края элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c7406-130">If you specify the <a href="rich-edit-control-styles.md"><strong>ES_AUTOHSCROLL</strong></a> style, the multiline edit control automatically scrolls horizontally when the caret goes past the right edge of the control.</span></span> <span data-ttu-id="c7406-131">Чтобы начать новую строку, пользователь должен нажать клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c7406-131">To start a new line, the user must press the ENTER key.</span></span> <span data-ttu-id="c7406-132">Если не указать <strong>ES_AUTOHSCROLL</strong>, элемент управления автоматически заключает слова в начало следующей строки, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="c7406-132">If you do not specify <strong>ES_AUTOHSCROLL</strong>, the control automatically wraps words to the beginning of the next line when necessary.</span></span> <span data-ttu-id="c7406-133">Новая строка также запускается, если пользователь нажмет клавишу ВВОД.</span><span class="sxs-lookup"><span data-stu-id="c7406-133">A new line is also started if the user presses the ENTER key.</span></span> <span data-ttu-id="c7406-134">Размер окна определяет расположение переданного слова.</span><span class="sxs-lookup"><span data-stu-id="c7406-134">The window size determines the position of the Wordwrap.</span></span> <span data-ttu-id="c7406-135">Если размер окна изменяется, то в Вордвраппинг положении изменяется и текст отображается повторно.</span><span class="sxs-lookup"><span data-stu-id="c7406-135">If the window size changes, the Wordwrapping position changes and the text is redisplayed.</span></span><br/> <span data-ttu-id="c7406-136">Элементы управления для многострочного редактирования могут иметь полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c7406-136">Multiline edit controls can have scroll bars.</span></span> <span data-ttu-id="c7406-137">Элемент управления "Правка" с полосами прокрутки обрабатывает собственные сообщения с полосой прокрутки.</span><span class="sxs-lookup"><span data-stu-id="c7406-137">An edit control with scroll bars processes its own scroll bar messages.</span></span> <span data-ttu-id="c7406-138">Обратите внимание, что элементы управления редактирования без полос прокрутки прокручиваться, как описано в предыдущих абзацах, и обрабатывают все сообщения, отправленные родительским окном.</span><span class="sxs-lookup"><span data-stu-id="c7406-138">Note that edit controls without scroll bars scroll as described in the previous paragraphs and process any scroll messages sent by the parent window.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_NOHIDESEL"></span><span id="es_nohidesel"></span><dl> <span data-ttu-id="c7406-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-139"><dt><strong>ES_NOHIDESEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-140">Инвертирует поведение по умолчанию для элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c7406-140">Negates the default behavior for an edit control.</span></span> <span data-ttu-id="c7406-141">Поведение по умолчанию скрывает выделение, когда элемент управления теряет фокус ввода и инвертирует выбор, когда элемент управления получает фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="c7406-141">The default behavior hides the selection when the control loses the input focus and inverts the selection when the control receives the input focus.</span></span> <span data-ttu-id="c7406-142">Если указать <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, выделенный текст будет инвертирован, даже если элемент управления не имеет фокуса.</span><span class="sxs-lookup"><span data-stu-id="c7406-142">If you specify <a href="rich-edit-control-styles.md"><strong>ES_NOHIDESEL</strong></a>, the selected text is inverted, even if the control does not have the focus.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_NUMBER"></span><span id="es_number"></span><dl> <span data-ttu-id="c7406-143"><dt><strong>ES_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-143"><dt><strong>ES_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-144">Позволяет указывать в элементе управления "поле ввода" только цифры.</span><span class="sxs-lookup"><span data-stu-id="c7406-144">Allows only digits to be entered into the edit control.</span></span> <span data-ttu-id="c7406-145">Обратите внимание, что даже при использовании этого набора все равно можно вставить нецифры в элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-145">Note that, even with this set, it is still possible to paste non-digits into the edit control.</span></span> <br/> <span data-ttu-id="c7406-146">Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c7406-146">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/> <span data-ttu-id="c7406-147">Чтобы перевести текст, который был вставлен в элемент управления "поле ввода", в целочисленное значение, используйте функцию <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>жетдлгитеминт</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7406-147">To translate text that was entered into the edit control to an integer value, use the <a href="/windows/desktop/api/winuser/nf-winuser-getdlgitemint"><strong>GetDlgItemInt</strong></a> function.</span></span> <span data-ttu-id="c7406-148">Чтобы задать для текста элемента управления "поле ввода" строковое представление указанного целого числа, используйте функцию <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>сетдлгитеминт</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="c7406-148">To set the text of the edit control to the string representation of a specified integer, use the <a href="/windows/desktop/api/winuser/nf-winuser-setdlgitemint"><strong>SetDlgItemInt</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_OEMCONVERT"></span><span id="es_oemconvert"></span><dl> <span data-ttu-id="c7406-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-149"><dt><strong>ES_OEMCONVERT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-150">Преобразует текст, указанный в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c7406-150">Converts text entered in the edit control.</span></span> <span data-ttu-id="c7406-151">Текст преобразуется из набора символов Windows в набор символов OEM, а затем обратно в набор символов Windows.</span><span class="sxs-lookup"><span data-stu-id="c7406-151">The text is converted from the Windows character set to the OEM character set and then back to the Windows character set.</span></span> <span data-ttu-id="c7406-152">Это обеспечивает правильное преобразование символов, когда приложение вызывает функцию <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>чартуем</strong></a> для преобразования строки Windows в элементе управления "поле ввода" в символы OEM.</span><span class="sxs-lookup"><span data-stu-id="c7406-152">This ensures proper character conversion when the application calls the <a href="/windows/desktop/api/winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> function to convert a Windows string in the edit control to OEM characters.</span></span> <span data-ttu-id="c7406-153">Этот стиль наиболее удобен для элементов управления для редактирования, содержащих имена файлов, которые будут использоваться в файловых системах, не поддерживающих Юникод.</span><span class="sxs-lookup"><span data-stu-id="c7406-153">This style is most useful for edit controls that contain file names that will be used on file systems that do not support Unicode.</span></span> <br/> <span data-ttu-id="c7406-154">Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c7406-154">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_PASSWORD"></span><span id="es_password"></span><dl> <span data-ttu-id="c7406-155"><dt><strong>ES_PASSWORD</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-155"><dt><strong>ES_PASSWORD</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-156">Отображает звездочку (\*) для каждого символа, вводимого в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c7406-156">Displays an asterisk (\*) for each character typed into the edit control.</span></span> <span data-ttu-id="c7406-157">Этот стиль допустим только для однострочных элементов управления редактирования.</span><span class="sxs-lookup"><span data-stu-id="c7406-157">This style is valid only for single-line edit controls.</span></span> <br/> <span data-ttu-id="c7406-158">Чтобы изменить отображаемые символы или установить или снять этот стиль, используйте <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> сообщение.</span><span class="sxs-lookup"><span data-stu-id="c7406-158">To change the characters that is displayed, or set or clear this style, use the <a href="em-setpasswordchar.md"><strong>EM_SETPASSWORDCHAR</strong></a> message.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c7406-159">Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте.</span><span class="sxs-lookup"><span data-stu-id="c7406-159">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="c7406-160">Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</span><span class="sxs-lookup"><span data-stu-id="c7406-160">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_READONLY"></span><span id="es_readonly"></span><dl> <span data-ttu-id="c7406-161"><dt><strong>ES_READONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-161"><dt><strong>ES_READONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-162">Не разрешает пользователю вводить или редактировать текст в элементе управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c7406-162">Prevents the user from typing or editing text in the edit control.</span></span><br/> <span data-ttu-id="c7406-163">Чтобы изменить стиль после создания элемента управления, используйте <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> сообщение.</span><span class="sxs-lookup"><span data-stu-id="c7406-163">To change this style after the control has been created, use the <a href="em-setreadonly.md"><strong>EM_SETREADONLY</strong></a> message.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_RIGHT"></span><span id="es_right"></span><dl> <span data-ttu-id="c7406-164"><dt><strong>ES_RIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-164"><dt><strong>ES_RIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-165">Выровнять текст по правому краю в однострочном или многострочном элементе управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-165">Right-aligns text in a single-line or multiline edit control.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ES_UPPERCASE"></span><span id="es_uppercase"></span><dl> <span data-ttu-id="c7406-166"><dt><strong>ES_UPPERCASE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-166"><dt><strong>ES_UPPERCASE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-167">Преобразует все символы в верхний регистр по мере их ввода в элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="c7406-167">Converts all characters to uppercase as they are typed into the edit control.</span></span> <br/> <span data-ttu-id="c7406-168">Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c7406-168">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ES_WANTRETURN"></span><span id="es_wantreturn"></span><dl> <span data-ttu-id="c7406-169"><dt><strong>ES_WANTRETURN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c7406-169"><dt><strong>ES_WANTRETURN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="c7406-170">Указывает, что возврат каретки должен быть вставлен, когда пользователь нажимает клавишу ВВОД при вводе текста в многострочный элемент управления "поле ввода" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="c7406-170">Specifies that a carriage return be inserted when the user presses the ENTER key while entering text into a multiline edit control in a dialog box.</span></span> <span data-ttu-id="c7406-171">Если этот стиль не указан, нажатие клавиши ВВОД приведет к тому же результату, что и нажатие кнопки по умолчанию в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="c7406-171">If you do not specify this style, pressing the ENTER key has the same effect as pressing the dialog box's default push button.</span></span> <span data-ttu-id="c7406-172">Этот стиль не влияет на однострочный элемент управления Edit.</span><span class="sxs-lookup"><span data-stu-id="c7406-172">This style has no effect on a single-line edit control.</span></span> <br/> <span data-ttu-id="c7406-173">Чтобы изменить стиль после создания элемента управления, используйте <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c7406-173">To change this style after the control has been created, use <a href="/windows/desktop/api/winuser/nf-winuser-setwindowlonga"><strong>SetWindowLong</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="c7406-174">Требования</span><span class="sxs-lookup"><span data-stu-id="c7406-174">Requirements</span></span>



| <span data-ttu-id="c7406-175">Требование</span><span class="sxs-lookup"><span data-stu-id="c7406-175">Requirement</span></span> | <span data-ttu-id="c7406-176">Значение</span><span class="sxs-lookup"><span data-stu-id="c7406-176">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7406-177">Header</span><span class="sxs-lookup"><span data-stu-id="c7406-177">Header</span></span><br/> | <dl> <span data-ttu-id="c7406-178"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7406-178"><dt>Winuser.h</dt></span></span> </dl> |



