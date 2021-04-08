---
title: Формат буфера обмена HTML
description: В этом разделе описывается формат буфера обмена HTML.
ms.assetid: e891393f-234f-4c94-b581-c4e5f885d2ab
keywords:
- Пользовательский интерфейс Windows, буфер обмена
- буфер обмена, вырезание данных
- буфер обмена, копирование данных
- буфер обмена, вставленные данные
- буфер обмена, форматы
- буфер обмена, формат HTML
- буфер обмена, Вырезание текста HTML
- буфер обмена, вставленный HTML-текст
- Формат буфера обмена CF_HTML
- буфер обмена, формат CF_HTML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75cdcd9c2fc982a7cbde38bba4b7dec6738f1793
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068147"
---
# <a name="html-clipboard-format"></a><span data-ttu-id="d3b7b-113">Формат буфера обмена HTML</span><span class="sxs-lookup"><span data-stu-id="d3b7b-113">HTML Clipboard Format</span></span>

<span data-ttu-id="d3b7b-114">Требования к передаче HTML-текста с помощью буфера обмена зависят от сценария.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-114">The requirements for transferring HTML text by means of the clipboard differ depending on scenario.</span></span> <span data-ttu-id="d3b7b-115">В этой статье рассматриваются вырезанные и вставленные фрагменты HTML-документа.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-115">This article is concerned with cutting and pasting fragments of an HTML document.</span></span> <span data-ttu-id="d3b7b-116">Возможны требования для передачи целых документов HTML через буфер обмена. Однако эта статья посвящена требованию для перемещения фрагментов выбранного текста HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-116">There may be requirements for transferring entire HTML documents through the clipboard; however, this article is driven by a requirement to transfer fragments of selected HTML text.</span></span> <span data-ttu-id="d3b7b-117">Таким образом, метод, который требует скопировать весь HTML-документ в буфер обмена, считается слишком высокой плотностью.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-117">As such, a method that required the entire HTML document to be copied to the clipboard is seen as too heavyweight.</span></span>

<span data-ttu-id="d3b7b-118">\_Формат буфера обмена HTML CF позволяет хранить фрагмент необработанного HTML-текста и его контекста в буфере обмена как ASCII.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-118">The CF\_HTML clipboard format allows a fragment of raw HTML text and its context to be stored on the clipboard as ASCII.</span></span> <span data-ttu-id="d3b7b-119">Это позволяет приложению контекст фрагмента кода HTML, который состоит из всех тегов, предшествующих окружающим тегам, проанализировать с помощью приложения, чтобы можно было отметить окружающие Теги фрагмента HTML с их атрибутами.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-119">This allows the context of the HTML fragment, which consists of all preceding surrounding tags, to be examined by an application so that the surrounding tags of the HTML fragment can be noted with their attributes.</span></span> <span data-ttu-id="d3b7b-120">Несмотря на то, что вы решаете, как интерпретировать такие фрагменты, на основе реализаций IE4/MSHTML сюда входят некоторые основные рекомендации.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-120">Although it is up to applications to decide how to interpret such fragments, some basic guidelines are included here based on IE4/MSHTML implementations.</span></span>

<span data-ttu-id="d3b7b-121">Официальное имя буфера обмена (строка, используемое Регистерклипбоардформат) имеет формат HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-121">The official name of the clipboard (the string used by RegisterClipboardFormat) is HTML Format.</span></span>

-   [<span data-ttu-id="d3b7b-122">Описание</span><span class="sxs-lookup"><span data-stu-id="d3b7b-122">Description</span></span>](#description)
-   [<span data-ttu-id="d3b7b-123">Сценарии</span><span class="sxs-lookup"><span data-stu-id="d3b7b-123">Scenarios</span></span>](#scenarios)

## <a name="description"></a><span data-ttu-id="d3b7b-124">Описание</span><span class="sxs-lookup"><span data-stu-id="d3b7b-124">Description</span></span>

<span data-ttu-id="d3b7b-125">\_HTML-код в формате CF является текстовым форматом (и, помимо прочего, в формате HTML и использует UTF-8) и включает `description` , необязательный элемент `context` и, в контексте `fragment` .</span><span class="sxs-lookup"><span data-stu-id="d3b7b-125">CF\_HTML is entirely text format (to be, among other things, in the HTML spirit, and uses UTF-8) and includes a `description`, an optional `context`, and, within the context, the `fragment`.</span></span>

<span data-ttu-id="d3b7b-126">Ниже приведен пример буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-126">The following is an example of a clipboard:</span></span>


```
Version:0.9
    StartHTML:71
    EndHTML:170
    StartFragment:140
    EndFragment:160
    StartSelection:140
    EndSelection:160
    <!DOCTYPE>
    <HTML>
    <HEAD>
    <TITLE> The HTML Clipboard</TITLE>
    <BASE HREF="https://sample/specs">
    </HEAD>
    <BODY>
    <UL>
    <!--StartFragment -->
    <LI> The Fragment </LI>
    <!--EndFragment -->
    </UL>
    </BODY>
    </HTML>
```



<span data-ttu-id="d3b7b-127">Описание включает номер версии буфера обмена и смещение, указывающие, где начинается и завершается контекст и фрагмент.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-127">The description includes the clipboard version number and offsets, indicating where the context and the fragment start and end.</span></span> <span data-ttu-id="d3b7b-128">Описание представляет собой список ключевых слов текста ASCII (min/Shift не имеет смысла), за которым следует строка, разделенная двоеточием (:).</span><span class="sxs-lookup"><span data-stu-id="d3b7b-128">The description is a list of ASCII text keywords (min/maj is not meaningful) followed by a string and separated by a colon (:).</span></span>

<span data-ttu-id="d3b7b-129">**Версия**: номер версии VV буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-129">**Version**: vv version number of the clipboard.</span></span> <span data-ttu-id="d3b7b-130">Начальная версия — 0,9.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-130">Starting version is 0.9.</span></span>

<span data-ttu-id="d3b7b-131">**Старстмл**: byteCount от начала буфера обмена до начала контекста или значение-1, если контекст отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-131">**StartHTML**: bytecount from the beginning of the clipboard to the start of the context, or -1 if no context.</span></span>

<span data-ttu-id="d3b7b-132">**Ендхтмл**: byteCount от начала буфера обмена до конца контекста или значение-1, если контекст отсутствует.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-132">**EndHTML**: bytecount from the beginning of the clipboard to the end of the context, or -1 if no context.</span></span>

<span data-ttu-id="d3b7b-133">**Стартфрагмент**: byteCount от начала буфера обмена до начала фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-133">**StartFragment**: bytecount from the beginning of the clipboard to the start of the fragment.</span></span>

<span data-ttu-id="d3b7b-134">**Ендфрагмент**: byteCount от начала буфера обмена до конца фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-134">**EndFragment**: bytecount from the beginning of the clipboard to the end of the fragment.</span></span>

<span data-ttu-id="d3b7b-135">**Стартселектион**: byteCount от начала буфера обмена до начала выбора.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-135">**StartSelection**: bytecount from the beginning of the clipboard to the start of the selection.</span></span>

<span data-ttu-id="d3b7b-136">**Ендселектион**: byteCount от начала буфера обмена до конца выделенного фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-136">**EndSelection**: bytecount from the beginning of the clipboard to the end of the selection.</span></span>

<span data-ttu-id="d3b7b-137">Ключевые слова Стартселектион и Ендселектион необязательны и должны быть опущены, если не нужно, чтобы приложение создавало эти сведения.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-137">The StartSelection and EndSelection keywords are optional and must both be omitted if you do not want the application to generate this information.</span></span>

<span data-ttu-id="d3b7b-138">Другие сведения об этом типе можно добавить здесь позже, так как HTML-код начинается с Старстмлоффсет.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-138">Other information of this kind could be added here later, since the HTML starts at the StartHTMLoffset.</span></span> <span data-ttu-id="d3b7b-139">Например, несколько пар Стартфрагмент/Ендфрагмент можно добавить позже для поддержки несмежных фрагментов.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-139">For example, multiple pairs of StartFragment / EndFragment could be added later to support noncontiguous selection of fragments.</span></span>

<span data-ttu-id="d3b7b-140">Для удобства работы программ, создающих битекаунтс, битекаунтс можно оставлять пустыми.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-140">For the convenience of the programs generating the bytecounts, bytecounts could be left padded by zeros.</span></span> <span data-ttu-id="d3b7b-141">Например, программы, создающие битекаунтс, могут произвольно повлиять на десять (10) нулей на каждое ключевое слово (Старстмл: 0000000000), а затем, когда известно точное Старстмл byteCount (скажем, 71), программа может заменить соответствующее количество нулей на byteCount (Старстмл: 0000000071).</span><span class="sxs-lookup"><span data-stu-id="d3b7b-141">For example, programs generating the bytecounts could arbitrarily affect ten (10) zeros to each keyword (StartHTML: 0000000000) and then, when the exact StartHTML bytecount is known (say, 71), the program can replace the appropriate number of zeros by the bytecount (StartHTML: 0000000071).</span></span>

<span data-ttu-id="d3b7b-142">Единственным набором символов, поддерживаемым буфером обмена, является Юникод в кодировке UTF-8.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-142">The only character set supported by the clipboard is Unicode in its UTF-8 encoding.</span></span> <span data-ttu-id="d3b7b-143">Поскольку первые символы UTF-8 и ASCII совпадают, описание всегда равно ASCII, но байты контекста (начиная с Старстмл) могут использовать любые другие символы, закодированные в кодировке UTF-8.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-143">Because the first characters of UTF-8 and ASCII match, the description is always ASCII, but the bytes of the context (starting at StartHTML) could be using any other characters coded in UTF-8.</span></span>

<span data-ttu-id="d3b7b-144">Конец строк в заголовке формата буфера обмена может быть CR или CR/LF или LF.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-144">End of lines in the clipboard format header could be CR or CR/LF or LF.</span></span>

<span data-ttu-id="d3b7b-145">Фрагмент содержит чистый, допустимый HTML, представляющий область, выбранную пользователем (например, для копирования).</span><span class="sxs-lookup"><span data-stu-id="d3b7b-145">The fragment contains pure, valid HTML representing the area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="d3b7b-146">Он содержит выделенный текст, а также открывающие теги и атрибуты любого элемента, у которого есть закрывающий тег в выделенном тексте, и закрывающие теги в конце фрагмента для любого включенного открывающего тега.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-146">This contains the selected text plus the opening tags and attributes of any element that has an end tag within the selected text, and end tags at the end of the fragment for any start tag included.</span></span> <span data-ttu-id="d3b7b-147">Это все сведения, необходимые для базового использования фрагмента HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-147">This is all information required for basic pasting of an HTML fragment.</span></span>

<span data-ttu-id="d3b7b-148">Перед фрагментом необходимо указать комментарии HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-148">The fragment should be preceded and followed by the HTML comments</span></span> <!--StartFragment--> <span data-ttu-id="d3b7b-149">и</span><span class="sxs-lookup"><span data-stu-id="d3b7b-149">and</span></span> <!--EndFragment--> <span data-ttu-id="d3b7b-150">(не допускаются пробелы между!--и текстом) для удобного указания места начала и окончания фрагмента.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-150">(no space allowed between the !-- and the text) to conveniently indicate where the fragment starts and ends.</span></span> <span data-ttu-id="d3b7b-151">Таким результатом, начало и конец фрагмента обозначаются наличием этих комментариев и Стартфрагмент и Ендфрагмент количество байт в описании.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-151">Thus the start and end of the fragment are indicated by the presence of these comments and by StartFragment and EndFragment byte counts in the description.</span></span> <span data-ttu-id="d3b7b-152">Для их получения требуются средства.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-152">Tools are expected to produce this information.</span></span> <span data-ttu-id="d3b7b-153">Эта избыточность была введена, чтобы быстро найти начало фрагмента (из числа байтов) и пометить расположение фрагмента непосредственно в дереве HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-153">This redundancy has been introduced to be able to rapidly find the start of the fragment (from the byte count) and mark the position of the fragment directly in the HTML tree.</span></span>

<span data-ttu-id="d3b7b-154">Выбор указывает внутри фрагмента точную HTML-область, выбранную пользователем (например, для копирования).</span><span class="sxs-lookup"><span data-stu-id="d3b7b-154">The selection indicates inside the fragment the exact HTML area the user has selected (to Copy, for example).</span></span> <span data-ttu-id="d3b7b-155">Это добавляет дополнительные сведения к фрагменту, указывая точный выделенный текст без открывающих тегов и закрывающих тегов, которые были добавлены, чтобы убедиться, что фрагмент имеет правильный формат HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-155">This adds more information to the fragment by indicating the exact selected text, without the opening tags and end tags that have been added to ensure the fragment is well-formed HTML.</span></span>

<span data-ttu-id="d3b7b-156">Выбор является необязательным, так как в фрагмент для базовых вставлений содержится достаточная информация.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-156">The selection is optional, as sufficient information is included in the fragment for basic pasting.</span></span> <span data-ttu-id="d3b7b-157">Если выделение не сохранено, то Стартселектион и Ендселектион не сохраняются в заголовке.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-157">If the selection is not stored, both StartSelection and EndSelection are not stored in the header.</span></span>

<span data-ttu-id="d3b7b-158">Контекст представляет собой допустимый полный HTML-документ.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-158">The context is a valid, complete HTML document.</span></span> <span data-ttu-id="d3b7b-159">В этой статье содержатся фрагменты и все предшествующие Теги (открывающие и закрывающие теги). Эти теги представляют все родительские узлы фрагмента до HTML-узла.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-159">This article contains the fragment and all preceding surrounding tags (start and end tags; these preceding surrounding tags represent all the parent nodes of the fragment, until the HTML node).</span></span> <span data-ttu-id="d3b7b-160">Статья также содержит полный заголовок и позволяет включать базовые элементы и названия, например, для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-160">The article also contains the complete HEAD, and allows the BASE and TITLE elements, for example, to be included so this additional information can be obtained.</span></span> <span data-ttu-id="d3b7b-161">Приложение, которое копирует фрагмент HTML-кода в буфер обмена, может создать базовый элемент для включения в контекст, если такой элемент еще не существует, чтобы можно было разрешить частичные URL-адреса в фрагменте.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-161">An application copying a fragment of HTML to the clipboard can choose to create a BASE element to include in the context if such an element is not already present so that partial URLs in the fragment can be resolved.</span></span>

<span data-ttu-id="d3b7b-162">Контекст является необязательным, так как в фрагмент включается достаточная информация для базового размещения фрагмента кода HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-162">The context is optional, as sufficient information is included in the fragment for basic pasting of an HTML fragment to take place.</span></span> <span data-ttu-id="d3b7b-163">Если контекст не сохранен, то сохраняется только фрагмент и Старстмл = Ендхтмл =-1.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-163">If the context is not stored, the fragment only is stored and the StartHTML=EndHTML=-1.</span></span>

## <a name="scenarios"></a><span data-ttu-id="d3b7b-164">Сценарии</span><span class="sxs-lookup"><span data-stu-id="d3b7b-164">Scenarios</span></span>

<span data-ttu-id="d3b7b-165">В следующих сценариях описывается, как редактор HTML IE4/MSHTML обрабатывает HTML-Вырезание и вставку. другие приложения могут и не следовать этим сценариям.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-165">The following scenarios describe how the IE4/MSHTML HTML editor handles HTML cut and paste; other applications may or may not follow these scenarios.</span></span> <span data-ttu-id="d3b7b-166">Формат буфера обмена, описанный здесь, предназначен для обеспечения гибкости работы приложения.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-166">The clipboard format described here is intended to allow flexibility for how an application chooses to function.</span></span> <span data-ttu-id="d3b7b-167">(В этих сценариях отображается только хороший код HTML, т. е. без перекрывающихся тегов.)</span><span class="sxs-lookup"><span data-stu-id="d3b7b-167">(These scenarios show only good HTML, that is, no overlapping tags.)</span></span>

1.  <span data-ttu-id="d3b7b-168">Простой фрагмент кода HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-168">Simple Fragment of HTML.</span></span>
    -   -   <span data-ttu-id="d3b7b-169">Текст HTML:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-169">HTML text:</span></span>

            <span data-ttu-id="d3b7b-170"><BODY>Это обычный <B>шрифт полужирным </B>начертанием полужирный <I> <B> </B>курсив.</I></BODY></span><span class="sxs-lookup"><span data-stu-id="d3b7b-170"><BODY>This is normal <B>This is bold </B><I><B>This is bold italic </B>This is italic </I></BODY></span></span>

        -   <span data-ttu-id="d3b7b-171">Отображается как:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-171">Appears as:</span></span>

            <span data-ttu-id="d3b7b-172">Это обычный **шрифт полужирным** шрифтом    \* **полужирный** курсив   \*</span><span class="sxs-lookup"><span data-stu-id="d3b7b-172">This is normal **This is bold**  \***This is bold italic**  This is italic\*</span></span>

        -   <span data-ttu-id="d3b7b-173">Текст между \* \* выбранным и скопированным в буфер обмена:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-173">The text between the \*\* is selected and copied to the clipboard:</span></span>

            <span data-ttu-id="d3b7b-174">Это **обычный** \* \* **Шрифт. полужирный** полужирный    \* **курсив** .   \* \* \* *— курсив*</span><span class="sxs-lookup"><span data-stu-id="d3b7b-174">This is normal **This is** \*\* **bold**   \***This is bold italic**  This\*\*\* *is italic*</span></span>

        -   <span data-ttu-id="d3b7b-175">Это то, что будет находиться в буфере обмена (Обратите внимание, что это IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="d3b7b-175">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <span data-ttu-id="d3b7b-176">Версия: 0.9</span><span class="sxs-lookup"><span data-stu-id="d3b7b-176">Version:0.9</span></span>

            <span data-ttu-id="d3b7b-177">Старстмл: 71</span><span class="sxs-lookup"><span data-stu-id="d3b7b-177">StartHTML:71</span></span>

            <span data-ttu-id="d3b7b-178">Ендхтмл: 160</span><span class="sxs-lookup"><span data-stu-id="d3b7b-178">EndHTML:160</span></span>

            <span data-ttu-id="d3b7b-179">Стартфрагмент: 130</span><span class="sxs-lookup"><span data-stu-id="d3b7b-179">StartFragment:130</span></span>

            <span data-ttu-id="d3b7b-180">Ендфрагмент: 150</span><span class="sxs-lookup"><span data-stu-id="d3b7b-180">EndFragment:150</span></span>

            <span data-ttu-id="d3b7b-181">**Стартселектион: 130**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-181">**StartSelection:130**</span></span>

            <span data-ttu-id="d3b7b-182">**Ендселектион: 150**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-182">**EndSelection:150**</span></span>

            <!DOCTYPE ...>

            <BODY>

            <!-- StartFragment -->>

            <span data-ttu-id="d3b7b-183">**<B>полужирный</B><I><B>курсив</B>.</I>**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-183">**<B>bold</B><I><B>This is bold italic</B>This</I>**</span></span>

            <!-- EndFragment -->

            </BODY>

            </HTML>

        -   <span data-ttu-id="d3b7b-184">В этом сценарии в контексте отображаются только тег BODY и HTML-тег, так как он предшествует выбранному фрагменту.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-184">In this scenario only the BODY tag and the HTML tag appear in the context as it precedes the selected fragment.</span></span> <span data-ttu-id="d3b7b-185">Обратите внимание, что открывающие и закрывающие теги включены в контекст.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-185">Note that start tags and end tags are included in the context.</span></span> <span data-ttu-id="d3b7b-186">Выделение, разделенное Стартселектион и Ендселектион, выделяется полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-186">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

2.  <span data-ttu-id="d3b7b-187">Фрагмент таблицы в формате HTML.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-187">Fragment of a table in HTML.</span></span>
    -   -   <span data-ttu-id="d3b7b-188">Текст HTML:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-188">HTML text:</span></span>

            <BODY><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="d3b7b-189">Head1</span><span class="sxs-lookup"><span data-stu-id="d3b7b-189">Head1</span></span></TH><TD><span data-ttu-id="d3b7b-190">Элемент 1</span><span class="sxs-lookup"><span data-stu-id="d3b7b-190">Item 1</span></span></TD><TD><span data-ttu-id="d3b7b-191">Элемент 2</span><span class="sxs-lookup"><span data-stu-id="d3b7b-191">Item 2</span></span></TD><TD><span data-ttu-id="d3b7b-192">Элемент 3</span><span class="sxs-lookup"><span data-stu-id="d3b7b-192">Item 3</span></span></TD><TD><span data-ttu-id="d3b7b-193">Элемент 4</span><span class="sxs-lookup"><span data-stu-id="d3b7b-193">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="d3b7b-194">Элемент 5</span><span class="sxs-lookup"><span data-stu-id="d3b7b-194">Item 5</span></span></TD><TD><span data-ttu-id="d3b7b-195">Элемент 6</span><span class="sxs-lookup"><span data-stu-id="d3b7b-195">Item 6</span></span></TD><TD><span data-ttu-id="d3b7b-196">Элемент 7</span><span class="sxs-lookup"><span data-stu-id="d3b7b-196">Item 7</span></span></TD><TD><span data-ttu-id="d3b7b-197">Элемент 8</span><span class="sxs-lookup"><span data-stu-id="d3b7b-197">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="d3b7b-198">Head2</span><span class="sxs-lookup"><span data-stu-id="d3b7b-198">Head2</span></span></TH><TD><span data-ttu-id="d3b7b-199">Элемент 9</span><span class="sxs-lookup"><span data-stu-id="d3b7b-199">Item 9</span></span></TD><TD><span data-ttu-id="d3b7b-200">Элемент 10</span><span class="sxs-lookup"><span data-stu-id="d3b7b-200">Item 10</span></span></TD><TD><span data-ttu-id="d3b7b-201">Элемент 11</span><span class="sxs-lookup"><span data-stu-id="d3b7b-201">Item 11</span></span></TD><TD><span data-ttu-id="d3b7b-202">Элемент 12</span><span class="sxs-lookup"><span data-stu-id="d3b7b-202">Item 12</span></span></TD></TR></TABLE></BODY>

        -   <span data-ttu-id="d3b7b-203">Отображается как: ></span><span class="sxs-lookup"><span data-stu-id="d3b7b-203">Appears as: ></span></span><TABLE BORDER><TR><TH ROWSPAN=2><span data-ttu-id="d3b7b-204">Head1</span><span class="sxs-lookup"><span data-stu-id="d3b7b-204">Head1</span></span></TH><TD><span data-ttu-id="d3b7b-205">Элемент 1</span><span class="sxs-lookup"><span data-stu-id="d3b7b-205">Item 1</span></span></TD><TD><span data-ttu-id="d3b7b-206">Элемент 2</span><span class="sxs-lookup"><span data-stu-id="d3b7b-206">Item 2</span></span></TD><TD><span data-ttu-id="d3b7b-207">Элемент 3</span><span class="sxs-lookup"><span data-stu-id="d3b7b-207">Item 3</span></span></TD><TD><span data-ttu-id="d3b7b-208">Элемент 4</span><span class="sxs-lookup"><span data-stu-id="d3b7b-208">Item 4</span></span></TD></TR><TR><TD><span data-ttu-id="d3b7b-209">Элемент 5</span><span class="sxs-lookup"><span data-stu-id="d3b7b-209">Item 5</span></span></TD><TD><span data-ttu-id="d3b7b-210">Элемент 6</span><span class="sxs-lookup"><span data-stu-id="d3b7b-210">Item 6</span></span></TD><TD><span data-ttu-id="d3b7b-211">Элемент 7</span><span class="sxs-lookup"><span data-stu-id="d3b7b-211">Item 7</span></span></TD><TD><span data-ttu-id="d3b7b-212">Элемент 8</span><span class="sxs-lookup"><span data-stu-id="d3b7b-212">Item 8</span></span></TD></TR><TR><TH><span data-ttu-id="d3b7b-213">Head2</span><span class="sxs-lookup"><span data-stu-id="d3b7b-213">Head2</span></span></TH><TD><span data-ttu-id="d3b7b-214">Элемент 9</span><span class="sxs-lookup"><span data-stu-id="d3b7b-214">Item 9</span></span></TD><TD><span data-ttu-id="d3b7b-215">Элемент 10</span><span class="sxs-lookup"><span data-stu-id="d3b7b-215">Item 10</span></span></TD><TD><span data-ttu-id="d3b7b-216">Элемент 11</span><span class="sxs-lookup"><span data-stu-id="d3b7b-216">Item 11</span></span></TD><TD><span data-ttu-id="d3b7b-217">Элемент 12</span><span class="sxs-lookup"><span data-stu-id="d3b7b-217">Item 12</span></span></TD></TR></TABLE><span data-ttu-id="d3b7b-218"><! \[ Корпорация\[\]\]></span><span class="sxs-lookup"><span data-stu-id="d3b7b-218"><!\[CDATA\[\]\]></span></span>
        -   <span data-ttu-id="d3b7b-219">Элементы таблицы 6, Item7, Item 10 и Item 11 выбираются в виде блока и копируются в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-219">The Item 6, Item7, Item 10, and Item 11 elements of the table are selected as a block and copied to the clipboard.</span></span>
        -   <span data-ttu-id="d3b7b-220">Это то, что будет находиться в буфере обмена (Обратите внимание, что это IE4/MSHTML):</span><span class="sxs-lookup"><span data-stu-id="d3b7b-220">This is what will be on the clipboard (note this is IE4/MSHTML's interpretation):</span></span>

            <!DOCTYPE ...>

            <HTML><BODY><TABLE BORDER>

            <!--StartFragment-->

            <span data-ttu-id="d3b7b-221">**<TR><TD>Элемент 6 Item 7, элемент 10, элемент </TD> <TD> </TD> </TR> <TR> <TD> </TD> <TD> 11</TD></TR>**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-221">**<TR><TD>Item 6</TD><TD>Item 7</TD></TR><TR><TD>Item 10</TD><TD>Item 11</TD></TR>**</span></span>

            <!--EndFragment-->

            </TABLE>

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

3.  <span data-ttu-id="d3b7b-222">Вставлен фрагмент упорядоченного списка в обычный текст.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-222">Pasting a fragment of an ordered list into plain text.</span></span>
    -   -   <span data-ttu-id="d3b7b-223">Текст HTML:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-223">HTML text:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="d3b7b-224">Элемент 1</span><span class="sxs-lookup"><span data-stu-id="d3b7b-224">Item 1</span></span><LI><span data-ttu-id="d3b7b-225">Элемент 2</span><span class="sxs-lookup"><span data-stu-id="d3b7b-225">Item 2</span></span><LI><span data-ttu-id="d3b7b-226">Элемент 3</span><span class="sxs-lookup"><span data-stu-id="d3b7b-226">Item 3</span></span><LI><span data-ttu-id="d3b7b-227">Элемент 4</span><span class="sxs-lookup"><span data-stu-id="d3b7b-227">Item 4</span></span><LI><span data-ttu-id="d3b7b-228">Элемент 5</span><span class="sxs-lookup"><span data-stu-id="d3b7b-228">Item 5</span></span><LI><span data-ttu-id="d3b7b-229">Элемент 6</span><span class="sxs-lookup"><span data-stu-id="d3b7b-229">Item 6</span></span></OL></BODY>

        -   <span data-ttu-id="d3b7b-230">Отображается как:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-230">Appears as:</span></span>
            1.  <span data-ttu-id="d3b7b-231">Элемент 1</span><span class="sxs-lookup"><span data-stu-id="d3b7b-231">Item 1</span></span>
            2.  <span data-ttu-id="d3b7b-232">Элемент 2</span><span class="sxs-lookup"><span data-stu-id="d3b7b-232">Item 2</span></span>
            3.  <span data-ttu-id="d3b7b-233">Элемент 3</span><span class="sxs-lookup"><span data-stu-id="d3b7b-233">Item 3</span></span>
            4.  <span data-ttu-id="d3b7b-234">Элемент 4</span><span class="sxs-lookup"><span data-stu-id="d3b7b-234">Item 4</span></span>
            5.  <span data-ttu-id="d3b7b-235">Элемент 5</span><span class="sxs-lookup"><span data-stu-id="d3b7b-235">Item 5</span></span>
            6.  <span data-ttu-id="d3b7b-236">Элемент 6</span><span class="sxs-lookup"><span data-stu-id="d3b7b-236">Item 6</span></span>
        -   <span data-ttu-id="d3b7b-237">Пользователь выбирает и копирует элементы с 3 по 5 в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-237">The user selects and copies items 3 through 5 to the clipboard.</span></span> <span data-ttu-id="d3b7b-238">Следующий HTML-код находится в буфере обмена:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-238">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="d3b7b-239"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="d3b7b-239"><DOCTYPE...><HTML><BODY></span></span><OL TYPE = a>

            <!-- StartFragment-->

            <span data-ttu-id="d3b7b-240">**<LI>Элемент 3, элемент 4, элемент <LI> <LI> 5**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-240">**<LI>Item 3<LI>Item 4<LI>Item 5**</span></span>

            <!-- EndFragment-->

            </OL></BODY></HTML>

            <span data-ttu-id="d3b7b-241">Выделение, разделенное Стартселектион и Ендселектион, выделяется полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-241">The selection, as delimited by StartSelection and EndSelection, is show in bold.</span></span>

        -   <span data-ttu-id="d3b7b-242">Если теперь этот фрагмент вставлен в пустой документ, будет создан следующий HTML:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-242">If this fragment is now pasted into an empty document, the following HTML will be created:</span></span>

            <BODY><OL TYPE = a><LI><span data-ttu-id="d3b7b-243">Элемент 3</span><span class="sxs-lookup"><span data-stu-id="d3b7b-243">Item 3</span></span><LI><span data-ttu-id="d3b7b-244">Элемент 4</span><span class="sxs-lookup"><span data-stu-id="d3b7b-244">Item 4</span></span><LI><span data-ttu-id="d3b7b-245">Элемент 5</span><span class="sxs-lookup"><span data-stu-id="d3b7b-245">Item 5</span></span></OL></BODY>

        -   <span data-ttu-id="d3b7b-246">Отображается как:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-246">Appearing as:</span></span>
            1.  <span data-ttu-id="d3b7b-247">Элемент 3</span><span class="sxs-lookup"><span data-stu-id="d3b7b-247">Item 3</span></span>
            2.  <span data-ttu-id="d3b7b-248">Элемент 4</span><span class="sxs-lookup"><span data-stu-id="d3b7b-248">Item 4</span></span>
            3.  <span data-ttu-id="d3b7b-249">Элемент 5</span><span class="sxs-lookup"><span data-stu-id="d3b7b-249">Item 5</span></span>

4.  <span data-ttu-id="d3b7b-250">Вставлена частично выделенная область.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-250">Pasting a partially selected region.</span></span>
    -   -   <span data-ttu-id="d3b7b-251">Текст HTML:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-251">HTML text:</span></span>

            <P> <span data-ttu-id="d3b7b-252">IE4/MSHTML — это редактор WYSIWYG, который поддерживает:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-252">IE4/MSHTML is a WYSIWYG Editor that supports :</span></span><UL><LI><span data-ttu-id="d3b7b-253">Вырезать</span><span class="sxs-lookup"><span data-stu-id="d3b7b-253">Cut</span></span><LI><span data-ttu-id="d3b7b-254">Копировать</span><span class="sxs-lookup"><span data-stu-id="d3b7b-254">Copy</span></span><LI><span data-ttu-id="d3b7b-255">Вставить</span><span class="sxs-lookup"><span data-stu-id="d3b7b-255">Paste</span></span></UL><P><span data-ttu-id="d3b7b-256">Это отличный инструмент!</span><span class="sxs-lookup"><span data-stu-id="d3b7b-256">This is a Great Tool !</span></span>

        -   <span data-ttu-id="d3b7b-257">Отображается как: IE4/MSHTML — это редактор WYSIWYG, который поддерживает:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-257">Appears as:IE4/MSHTML is a WYSIWYG Editor that supports :</span></span>
            -   -   <span data-ttu-id="d3b7b-258">Вырезать</span><span class="sxs-lookup"><span data-stu-id="d3b7b-258">Cut</span></span>
                -   <span data-ttu-id="d3b7b-259">Копировать</span><span class="sxs-lookup"><span data-stu-id="d3b7b-259">Copy</span></span>
                -   <span data-ttu-id="d3b7b-260">Вставить</span><span class="sxs-lookup"><span data-stu-id="d3b7b-260">Paste</span></span>

        -   <span data-ttu-id="d3b7b-261">Пользователь выбирает из "WYSIWYG" до "COP". Следующий HTML-код находится в буфере обмена:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-261">The user selects from "WYSIWYG" until "Cop".The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="d3b7b-262"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="d3b7b-262"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <P>

            <span data-ttu-id="d3b7b-263">**Редактор WYSIWYG, который поддерживает**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-263">**WYSIWYG Editor, which supports**</span></span>

            <span data-ttu-id="d3b7b-264">**<UL><LI>Вырезать <LI> COP**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-264">**<UL><LI>Cut<LI>Cop**</span></span>

            </UL>

            <!-- EndFragment-->

            </BODY></HTML>The selection, as delimited by StartSelection and EndSelection, is shown in bold.

     
    -   -   <span data-ttu-id="d3b7b-265">Пользователь выбирает "opy" до "отличного".</span><span class="sxs-lookup"><span data-stu-id="d3b7b-265">The user selects from "opy" until "Great".</span></span>

            <span data-ttu-id="d3b7b-266">Следующий HTML-код находится в буфере обмена:</span><span class="sxs-lookup"><span data-stu-id="d3b7b-266">The following HTML is in the clipboard:</span></span>

            <span data-ttu-id="d3b7b-267"><DOCTYPE... ><HTML><BODY></span><span class="sxs-lookup"><span data-stu-id="d3b7b-267"><DOCTYPE...><HTML><BODY></span></span>

            <!-- StartFragment-->

            <UL><LI>

            <span data-ttu-id="d3b7b-268">**OPY <LI> Вставить </UL> <P> это отличный**</span><span class="sxs-lookup"><span data-stu-id="d3b7b-268">**opy<LI>Paste</UL><P> This is a Great**</span></span>

            </P>

            <!-- EndFragment-->

            </BODY></HTML>

            <span data-ttu-id="d3b7b-269">Выделение, разделенное Стартселектион и Ендселектион, выделяется полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="d3b7b-269">The selection, as delimited by StartSelection and EndSelection, is shown in bold.</span></span>

 

 




