---
title: Использование элементов управления Rich Edit
description: В этом разделе содержатся разделы, демонстрирующие создание и использование элементов управления Rich Edit.
ms.assetid: 2c4717c9-3257-42d5-9c36-89b7e524e788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0489660bb6849d0de76ae7fc2f4e21ca931662a8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104488421"
---
# <a name="using-rich-edit-controls"></a><span data-ttu-id="fca9a-103">Использование элементов управления Rich Edit</span><span class="sxs-lookup"><span data-stu-id="fca9a-103">Using Rich Edit Controls</span></span>

<span data-ttu-id="fca9a-104">В этом разделе содержатся разделы, демонстрирующие создание и использование элементов управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fca9a-104">This section contains topics that demonstrate how to create and use rich edit controls.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fca9a-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="fca9a-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fca9a-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="fca9a-106">Topic</span></span></th>
<th><span data-ttu-id="fca9a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fca9a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fca9a-108"><a href="create-rich-edit-controls.md">Создание элементов управления с богатыми возможностями редактирования</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-108"><a href="create-rich-edit-controls.md">How to Create Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-109">Чтобы создать элемент управления Rich Edit, вызовите функцию <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> , указав класс окна редактирования Rich.</span><span class="sxs-lookup"><span data-stu-id="fca9a-109">To create a rich edit control, call the <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa"><strong>CreateWindowEx</strong></a> function, specifying the rich edit window class.</span></span> <span data-ttu-id="fca9a-110">Для Microsoft Rich Edit 4,1 (Msftedit.dll) укажите MSFTEDIT_CLASS в качестве класса окна.</span><span class="sxs-lookup"><span data-stu-id="fca9a-110">For Microsoft Rich Edit 4.1 (Msftedit.dll), specify MSFTEDIT_CLASS as the window class.</span></span> <span data-ttu-id="fca9a-111">Для всех предыдущих версий укажите RICHEDIT_CLASS.</span><span class="sxs-lookup"><span data-stu-id="fca9a-111">For all previous versions, specify RICHEDIT_CLASS.</span></span> <span data-ttu-id="fca9a-112">Дополнительные сведения см. в разделе <a href="about-rich-edit-controls.md">версии расширенного редактирования</a>.</span><span class="sxs-lookup"><span data-stu-id="fca9a-112">For more information, see <a href="about-rich-edit-controls.md">Versions of Rich Edit</a>.</span></span> <br/> <span data-ttu-id="fca9a-113">Широкие возможности управления редактированием поддерживают большинство стилей окон, используемых с элементами управления "поле ввода", а также дополнительными стилями.</span><span class="sxs-lookup"><span data-stu-id="fca9a-113">Rich edit controls support most of the window styles used with edit controls as well as additional styles.</span></span> <span data-ttu-id="fca9a-114">Если нужно разрешить несколько строк текста в элементе управления, следует указать стиль окна <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="fca9a-114">You should specify the <a href="edit-control-styles.md"><strong>ES_MULTILINE</strong></a> window style if you want to allow more than one line of text in the control.</span></span> <span data-ttu-id="fca9a-115">Дополнительные сведения см. в разделе <a href="rich-edit-control-styles.md">стили элементов управления Rich Edit</a>.</span><span class="sxs-lookup"><span data-stu-id="fca9a-115">For more information, see <a href="rich-edit-control-styles.md">Rich Edit Control Styles</a>.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fca9a-116"><a href="format-text-in-rich-edit-controls.md">Форматирование текста в элементах управления Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-116"><a href="format-text-in-rich-edit-controls.md">How to Format Text in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-117">Приложение может отправить сообщения в элемент управления Rich Edit, чтобы форматировать символы и абзацы и получать сведения о форматировании.</span><span class="sxs-lookup"><span data-stu-id="fca9a-117">An application can send messages to a rich edit control in order to format characters and paragraphs and retrieve formatting information.</span></span> <span data-ttu-id="fca9a-118">Атрибуты форматирования абзаца включают выравнивание, табуляцию, отступы, нумерацию и простые таблицы.</span><span class="sxs-lookup"><span data-stu-id="fca9a-118">Paragraph formatting attributes include alignment, tabs, indents, numbering, and simple tables.</span></span> <span data-ttu-id="fca9a-119">Для символов можно указать имя шрифта, размер, цвет и эффекты, такие как полужирный, курсив и защищенный.</span><span class="sxs-lookup"><span data-stu-id="fca9a-119">For characters, you can specify font name, size, color, and effects such as bold, italic, and protected.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fca9a-120"><a href="interact-with-the-current-selection.md">Как взаимодействовать с текущим выделением</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-120"><a href="interact-with-the-current-selection.md">How to Interact with the Current Selection</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-121">Пользователь может выбрать текст в элементе управления Rich Edit с помощью мыши или клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="fca9a-121">The user can select text in a rich edit control by using the mouse or the keyboard.</span></span> <span data-ttu-id="fca9a-122"><em>Текущий выделенный фрагмент</em> — это диапазон выбранных символов или позиция точки вставки, если ни одна из символов не выбрана.</span><span class="sxs-lookup"><span data-stu-id="fca9a-122">The <em>current selection</em> is the range of selected characters, or the position of the insertion point if no characters are selected.</span></span> <span data-ttu-id="fca9a-123">Приложение может получить сведения о текущем выделении, задать его, определить, когда оно изменяется, а также показать или скрыть выделение выделения.</span><span class="sxs-lookup"><span data-stu-id="fca9a-123">An application can get information about the current selection, set it, determine when it changes, and show or hide the selection highlight.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fca9a-124"><a href="use-rich-edit-text-operations.md">Как использовать широкие операции редактирования текста</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-124"><a href="use-rich-edit-text-operations.md">How to Use Rich Edit Text Operations</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-125">Приложение может отсылать сообщения для получения или поиска текста в элементе управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fca9a-125">An application can send messages to retrieve or find text in a rich edit control.</span></span> <span data-ttu-id="fca9a-126">Можно получить выделенный текст или указанный фрагмент текста.</span><span class="sxs-lookup"><span data-stu-id="fca9a-126">You can retrieve either the selected text or a specified range of text.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fca9a-127"><a href="use-word-and-line-break-information.md">Использование сведений о разрывах слов и строк</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-127"><a href="use-word-and-line-break-information.md">How to Use Word and Line Break Information</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-128">Форматированный элемент управления "поле ввода" вызывает функцию, называемую процедурой разрыва слов, чтобы найти разрывы между словами и определить, где она может разбивать строки.</span><span class="sxs-lookup"><span data-stu-id="fca9a-128">A rich edit control calls a function called a word-break procedure to find breaks between words and to determine where it can break lines.</span></span> <span data-ttu-id="fca9a-129">Этот элемент управления использует эти сведения при выполнении операций переноса по словам и при обработке сочетания клавиш CTRL + стрелка влево и CTRL + стрелка вправо.</span><span class="sxs-lookup"><span data-stu-id="fca9a-129">The control uses this information when performing word-wrap operations and when processing CTRL+LEFT ARROW key and CTRL+RIGHT ARROW key combinations.</span></span> <span data-ttu-id="fca9a-130">Приложение может отправить сообщения в элемент управления Rich Edit, чтобы заменить процедуру разбиения по словам по умолчанию, получить сведения о разрыве слов и определить линию, на которую попадает заданный символ.</span><span class="sxs-lookup"><span data-stu-id="fca9a-130">An application can send messages to a rich edit control to replace the default word-break procedure, to retrieve word-break information, and to determine what line a given character falls on.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fca9a-131"><a href="use-rich-edit-clipboard-operations.md">Использование многофункциональных операций редактирования буфера обмена</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-131"><a href="use-rich-edit-clipboard-operations.md">How to Use Rich Edit Clipboard Operations</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-132">Приложение может вставить содержимое буфера обмена в форматируемый элемент управления с помощью наиболее доступного формата буфера обмена или конкретного формата буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="fca9a-132">An application can paste the contents of the clipboard into a rich edit control by using either the best available clipboard format or a specific clipboard format.</span></span> <span data-ttu-id="fca9a-133">Кроме того, можно определить, может ли элемент управления с расширенным редактированием вставлять формат буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="fca9a-133">You can also determine whether a rich edit control is capable of pasting a clipboard format.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fca9a-134"><a href="use-streams.md">Использование потоков</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-134"><a href="use-streams.md">How to Use Streams</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-135">Потоки можно использовать для перемещения данных в элемент управления Rich Edit или из него.</span><span class="sxs-lookup"><span data-stu-id="fca9a-135">You can use streams to transfer data into or out of a rich edit control.</span></span> <span data-ttu-id="fca9a-136">Поток определяется структурой <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>едитстреам</strong></a> , которая задает буфер и функцию обратного вызова, определяемую приложением.</span><span class="sxs-lookup"><span data-stu-id="fca9a-136">A stream is defined by an <a href="/windows/desktop/api/Richedit/ns-richedit-editstream"><strong>EDITSTREAM</strong></a> structure, which specifies a buffer and an application-defined callback function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fca9a-137"><a href="automatically-resize-rich-edit-controls.md">Автоматическое изменение размера элементов управления Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-137"><a href="automatically-resize-rich-edit-controls.md">How to Automatically Resize Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-138">Приложение может изменить размер элемента управления Rich Edit при необходимости, чтобы его размер всегда совпадал с его содержимым.</span><span class="sxs-lookup"><span data-stu-id="fca9a-138">An application can resize a rich edit control as needed so that it is always the same size as its contents.</span></span> <span data-ttu-id="fca9a-139">Форматированный элемент управления "поле ввода" поддерживает такие функции, которые называются <em>ненижними</em> , отправляя родительское окно <a href="en-requestresize.md">EN_REQUESTRESIZE</a> код уведомления всякий раз, когда изменяется размер содержимого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="fca9a-139">A rich edit control supports this so-called <em>bottomless</em> functionality by sending its parent window an <a href="en-requestresize.md">EN_REQUESTRESIZE</a> notification code whenever the size of the control's content changes.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fca9a-140"><a href="use-rich-edit-control-notification-codes.md">Использование расширенных кодов уведомлений элемента управления редактированием</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-140"><a href="use-rich-edit-control-notification-codes.md">How to Use Rich Edit Control Notification Codes</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-141">Родительское окно элемента управления Rich Edit может обрабатывать коды уведомлений для отслеживания событий, влияющих на элемент управления.</span><span class="sxs-lookup"><span data-stu-id="fca9a-141">A rich edit control's parent window can process notification codes to monitor events that affect the control.</span></span> <span data-ttu-id="fca9a-142">Элементы управления Rich Edit поддерживают все коды уведомлений, используемые с элементами управления "поле ввода", а также несколько дополнительных.</span><span class="sxs-lookup"><span data-stu-id="fca9a-142">Rich edit controls support all of the notification codes that are used with edit controls, as well as several additional ones.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fca9a-143"><a href="use-font-binding-in-rich-edit-controls.md">Использование привязки шрифтов в элементах управления Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-143"><a href="use-font-binding-in-rich-edit-controls.md">How to Use Font Binding in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-144">Microsoft Rich Edit 3,0 присваивает набор символов обычным текстовым символам в зависимости от контекста.</span><span class="sxs-lookup"><span data-stu-id="fca9a-144">Microsoft Rich Edit 3.0 assigns a character set to plain-text characters depending on their context.</span></span> <span data-ttu-id="fca9a-145">Ниже приведены некоторые примеры.</span><span class="sxs-lookup"><span data-stu-id="fca9a-145">Some examples are:</span></span> <br/>
<ul>
<li><span data-ttu-id="fca9a-146">Греческие символы назначаются <strong>GREEK_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="fca9a-146">Greek characters are assigned <strong>GREEK_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="fca9a-147">Символы хангыль назначаются <strong>HANGUL_CHARSET</strong>.</span><span class="sxs-lookup"><span data-stu-id="fca9a-147">Hangul symbols are assigned <strong>HANGUL_CHARSET</strong>.</span></span></li>
<li><span data-ttu-id="fca9a-148">Китайские иероглифы назначаются <strong>SHIFTJIS_CHARSET</strong> , если рядом с ними расположены символы Кана, или <strong>GB2312_CHARSET</strong> , если поблизости не найдено ни одного символа Кана.</span><span class="sxs-lookup"><span data-stu-id="fca9a-148">Chinese characters are assigned <strong>SHIFTJIS_CHARSET</strong> if kana characters are found nearby, or <strong>GB2312_CHARSET</strong> if no kana are found nearby.</span></span></li>
<li><span data-ttu-id="fca9a-149">Ненейтральные символы ANSI назначаются <strong>ANSI_CHARSET</strong> в любом событии.</span><span class="sxs-lookup"><span data-stu-id="fca9a-149">Non-neutral ANSI characters are assigned <strong>ANSI_CHARSET</strong> in any event.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fca9a-150"><a href="using-rich-edit-com.md">Использование OLE в элементах управления Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-150"><a href="using-rich-edit-com.md">How to Use OLE in Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-151">В этом разделе содержатся сведения об использовании связывания и внедрения объектов (OLE) в элементах управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fca9a-151">This section contains information about using object linking and embedding (OLE) in rich edit controls.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fca9a-152"><a href="printing-rich-edit-controls.md">Печать содержимого элементов управления Rich Edit</a></span><span class="sxs-lookup"><span data-stu-id="fca9a-152"><a href="printing-rich-edit-controls.md">How to Print the Contents of Rich Edit Controls</a></span></span><br/></td>
<td><span data-ttu-id="fca9a-153">В этом разделе содержатся сведения о печати содержимого элементов управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fca9a-153">This section contains information about how to print the contents of rich edit controls.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

 

