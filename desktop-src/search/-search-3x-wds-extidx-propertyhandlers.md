---
description: Microsoft Windows Search использует обработчики свойств для извлечения значений свойств из элементов и использует схему системы свойств, чтобы определить, как должно индексироваться конкретное свойство.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Разработка обработчиков свойств для поиска Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262944"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="e1c12-103">Разработка обработчиков свойств для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="e1c12-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="e1c12-104">Microsoft Windows Search использует обработчики свойств для извлечения значений свойств из элементов и использует схему системы свойств, чтобы определить, как должно индексироваться конкретное свойство.</span><span class="sxs-lookup"><span data-stu-id="e1c12-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="e1c12-105">Для чтения и индексации значений свойств обработчики свойств вызываются вне процесса поиска Windows для повышения безопасности и надежности.</span><span class="sxs-lookup"><span data-stu-id="e1c12-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="e1c12-106">В отличие от этого, обработчики свойств вызываются проводником Windows в процессе чтения и записи значений свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="e1c12-107">Этот раздел дополняет раздел [системы свойств](../properties/building-property-handlers.md) информацией, относящейся к службе поиска Windows, и содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="e1c12-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="e1c12-108">Разработка решений для обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="e1c12-109">Решения для свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="e1c12-110">Поддержка полнотекстовых каталогов</span><span class="sxs-lookup"><span data-stu-id="e1c12-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="e1c12-111">Рекомендации по Имплементататион операционной системы</span><span class="sxs-lookup"><span data-stu-id="e1c12-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="e1c12-112">Запись файлов описания свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="e1c12-113">Реализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="e1c12-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="e1c12-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="e1c12-115">ипропертисторе</span><span class="sxs-lookup"><span data-stu-id="e1c12-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="e1c12-116">ипропертисторекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="e1c12-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="e1c12-117">Проверка индексации элементов</span><span class="sxs-lookup"><span data-stu-id="e1c12-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="e1c12-118">Установка и регистрация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="e1c12-119">Тестирование и устранение неполадок обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="e1c12-120">Тесты установки и установки</span><span class="sxs-lookup"><span data-stu-id="e1c12-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="e1c12-121">Устранение неполадок обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="e1c12-122">Использование обработчиков свойств System-Supplied</span><span class="sxs-lookup"><span data-stu-id="e1c12-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="e1c12-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e1c12-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="e1c12-124">Разработка решений для обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="e1c12-125">Реализация обработчиков свойств включает следующие шаги.</span><span class="sxs-lookup"><span data-stu-id="e1c12-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="e1c12-126">Принятие решений по проектированию в отношении свойств, которые вы хотите поддерживать.</span><span class="sxs-lookup"><span data-stu-id="e1c12-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="e1c12-127">Создание файла описания свойства (. пропдеск) для свойств, которые еще не находятся в системе свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="e1c12-128">Реализация и тестирование обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="e1c12-129">Установка и регистрация обработчиков свойств и файлов описания свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="e1c12-130">Тестирование установки и регистрации обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="e1c12-131">Прежде чем начать, необходимо принять во внимание следующие вопросы по проектированию:</span><span class="sxs-lookup"><span data-stu-id="e1c12-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="e1c12-132">Какие свойства имеют или должны поддерживать формат файла?</span><span class="sxs-lookup"><span data-stu-id="e1c12-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="e1c12-133">Эти свойства уже включены в схему системы?</span><span class="sxs-lookup"><span data-stu-id="e1c12-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="e1c12-134">Можно ли использовать существующий обработчик свойств, предоставляемый системой?</span><span class="sxs-lookup"><span data-stu-id="e1c12-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="e1c12-135">Какие свойства могут отображаться для конечных пользователей?</span><span class="sxs-lookup"><span data-stu-id="e1c12-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="e1c12-136">Какие свойства могут изменять пользователи?</span><span class="sxs-lookup"><span data-stu-id="e1c12-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="e1c12-137">Должна ли поддержка полнотекстового поиска происходить из обработчика свойств или фильтра?</span><span class="sxs-lookup"><span data-stu-id="e1c12-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="e1c12-138">Требуется ли поддержка устаревших приложений?</span><span class="sxs-lookup"><span data-stu-id="e1c12-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="e1c12-139">Если да, то что я реализую?</span><span class="sxs-lookup"><span data-stu-id="e1c12-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="e1c12-140">Прежде чем продолжить, см. раздел [Использование обработчиков свойств System-Supplied](#using-system-supplied-property-handlers) , чтобы узнать, можно ли использовать предоставляемый системой обработчик свойств, сохранив как ресурсы времени, так и время разработки.</span><span class="sxs-lookup"><span data-stu-id="e1c12-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="e1c12-141">После принятия этих решений можно написать формальные описания пользовательских свойств, чтобы система поиска Windows могла начать индексирование файлов и свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="e1c12-142">Эти формальные описания представляют собой XML-файлы, описанные в [схеме описание свойства](/previous-versions//cc144127(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e1c12-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="e1c12-143">Решения для свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-143">Property Decisions</span></span>

<span data-ttu-id="e1c12-144">Принимая во внимание, какие свойства следует поддерживать, необходимо выяснить, какие именно индексированные пользователи должны выполнять поиск.</span><span class="sxs-lookup"><span data-stu-id="e1c12-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="e1c12-145">Например, вы можете найти 100 потенциально полезных свойств для типа файлов, но пользователи могут заинтересовать Поиск только в нескольких случаях.</span><span class="sxs-lookup"><span data-stu-id="e1c12-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="e1c12-146">Кроме того, может потребоваться, чтобы пользователи отображали разные, более крупные или меньшие группы этих свойств в проводнике Windows и позволяли пользователям изменять только подмножество отображаемых свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="e1c12-147">Тип файлов может поддерживать любые определяемые пользователем свойства, а также набор системных свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="e1c12-148">Перед созданием пользовательского свойства проверьте [системные свойства](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) , чтобы узнать, является ли свойство, которое требуется поддерживать, уже определенным системным свойством.</span><span class="sxs-lookup"><span data-stu-id="e1c12-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="e1c12-149">Всегда Обеспечьте поддержку наиболее важных системных свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="e1c12-150">Для разработки свойств рекомендуется использовать матрицу:</span><span class="sxs-lookup"><span data-stu-id="e1c12-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="e1c12-151">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="e1c12-151">Property name</span></span> | <span data-ttu-id="e1c12-152">Является индексируемым?</span><span class="sxs-lookup"><span data-stu-id="e1c12-152">Is indexable?</span></span> | <span data-ttu-id="e1c12-153">Может ли быть воспроизведен?</span><span class="sxs-lookup"><span data-stu-id="e1c12-153">Is displayable?</span></span> | <span data-ttu-id="e1c12-154">Является редактируемым?</span><span class="sxs-lookup"><span data-stu-id="e1c12-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="e1c12-155">property1</span><span class="sxs-lookup"><span data-stu-id="e1c12-155">property1</span></span>     | <span data-ttu-id="e1c12-156">Да</span><span class="sxs-lookup"><span data-stu-id="e1c12-156">Y</span></span>             | <span data-ttu-id="e1c12-157">Да</span><span class="sxs-lookup"><span data-stu-id="e1c12-157">Y</span></span>               | <span data-ttu-id="e1c12-158">Нет</span><span class="sxs-lookup"><span data-stu-id="e1c12-158">N</span></span>            |
| <span data-ttu-id="e1c12-159">свойство...</span><span class="sxs-lookup"><span data-stu-id="e1c12-159">property...</span></span>   | <span data-ttu-id="e1c12-160">Да</span><span class="sxs-lookup"><span data-stu-id="e1c12-160">Y</span></span>             | <span data-ttu-id="e1c12-161">Да</span><span class="sxs-lookup"><span data-stu-id="e1c12-161">Y</span></span>               | <span data-ttu-id="e1c12-162">Нет</span><span class="sxs-lookup"><span data-stu-id="e1c12-162">N</span></span>            |
| <span data-ttu-id="e1c12-163">пропертин</span><span class="sxs-lookup"><span data-stu-id="e1c12-163">propertyn</span></span>     | <span data-ttu-id="e1c12-164">Нет</span><span class="sxs-lookup"><span data-stu-id="e1c12-164">N</span></span>             | <span data-ttu-id="e1c12-165">Нет</span><span class="sxs-lookup"><span data-stu-id="e1c12-165">N</span></span>               | <span data-ttu-id="e1c12-166">Нет</span><span class="sxs-lookup"><span data-stu-id="e1c12-166">N</span></span>            |



 

<span data-ttu-id="e1c12-167">Для каждого из этих свойств необходимо определить, какие атрибуты должны иметься, а затем описать их в XML-файлах описания свойств (. пропдеск).</span><span class="sxs-lookup"><span data-stu-id="e1c12-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="e1c12-168">Атрибуты включают в себя тип данных свойства, метку, строку справки и многое другое.</span><span class="sxs-lookup"><span data-stu-id="e1c12-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="e1c12-169">Для индексируемых свойств следует обратить особое внимание на следующие атрибуты свойств, найденные в XML-элементе [сеарчинфо](../properties/propdesc-schema-searchinfo.md)   файла описания свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1c12-170">attribute</span><span class="sxs-lookup"><span data-stu-id="e1c12-170">Attribute</span></span></th>
<th><span data-ttu-id="e1c12-171">Описание</span><span class="sxs-lookup"><span data-stu-id="e1c12-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1c12-172">ининвертединдекс</span><span class="sxs-lookup"><span data-stu-id="e1c12-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="e1c12-173">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e1c12-173">Optional.</span></span> <span data-ttu-id="e1c12-174">Указывает, должно ли значение свойства строки разбиваться на слова и каждое слово, хранящееся в инвертированном индексе.</span><span class="sxs-lookup"><span data-stu-id="e1c12-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="e1c12-175">Инвертированный индекс обеспечивает эффективный поиск слов и фраз по значению свойства с помощью CONTAINS или FREETEXT (например, SELECT... ГДЕ содержит &quot; сометекст &quot; ).</span><span class="sxs-lookup"><span data-stu-id="e1c12-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="e1c12-176">Если задано значение <strong>false</strong>, поиск выполняется по всей строке.</span><span class="sxs-lookup"><span data-stu-id="e1c12-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="e1c12-177">Большинство строковых свойств должно иметь значение <strong>true</strong>. свойства, не являющиеся строковыми, должны иметь значение <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="e1c12-178">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c12-179">Столбец</span><span class="sxs-lookup"><span data-stu-id="e1c12-179">isColumn</span></span></td>
<td><span data-ttu-id="e1c12-180">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e1c12-180">Optional.</span></span> <span data-ttu-id="e1c12-181">Указывает, должно ли свойство храниться в базе данных Windows Search как столбец.</span><span class="sxs-lookup"><span data-stu-id="e1c12-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="e1c12-182">Сохранение свойства в виде столбца включает извлечение, сортировку, группирование и фильтрацию (то есть использование любого предиката, кроме CONTAINS или FREETEXT) для значения всего столбца.</span><span class="sxs-lookup"><span data-stu-id="e1c12-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="e1c12-183">Свойства, отображаемые пользователю, должны иметь значение <strong>true</strong> , если оно не является очень большим текстовым свойством (например, текстом документа), которое будет искаться в инвертированном индексе.</span><span class="sxs-lookup"><span data-stu-id="e1c12-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="e1c12-184">Значение по умолчанию — <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c12-185">исколумнспарсе</span><span class="sxs-lookup"><span data-stu-id="e1c12-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="e1c12-186">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e1c12-186">Optional.</span></span> <span data-ttu-id="e1c12-187">Указывает, принимает ли свойство пробел, если значение равно <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="e1c12-188">Свойство без разрежения для каждого элемента занимает место, даже если значение равно <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="e1c12-189">Если свойство является многозначным, этот атрибут всегда имеет <strong>значение true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="e1c12-190">Этот атрибут должен иметь значение <strong>false</strong> только в том случае, если для каждого элемента имеется какое-либо из значений.</span><span class="sxs-lookup"><span data-stu-id="e1c12-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="e1c12-191">Значение по умолчанию — <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c12-192">колумниндекстипе</span><span class="sxs-lookup"><span data-stu-id="e1c12-192">columnIndexType</span></span></td>
<td><span data-ttu-id="e1c12-193">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e1c12-193">Optional.</span></span> <span data-ttu-id="e1c12-194">Для оптимизации запросов система поиска Windows может создавать вторичные индексы для свойств, имеющих<strong>значение IsTrue = true</strong>.</span><span class="sxs-lookup"><span data-stu-id="e1c12-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="e1c12-195">Это требует больше обработки и места на диске во время индексирования, но повышает производительность при выполнении запросов.</span><span class="sxs-lookup"><span data-stu-id="e1c12-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="e1c12-196">Если свойство планируется сортировать, группировать или фильтровать (то есть с помощью =,! =, <, >, LIKE, СОВПАДЕНИй) часто от пользователей, для этого атрибута следует задать значение &quot; ondisk &quot; .</span><span class="sxs-lookup"><span data-stu-id="e1c12-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="e1c12-197">Значение по умолчанию — &quot; нотиндексед &quot; .</span><span class="sxs-lookup"><span data-stu-id="e1c12-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="e1c12-198">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e1c12-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="e1c12-199">Нотиндексед: не создан вторичный индекс.</span><span class="sxs-lookup"><span data-stu-id="e1c12-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="e1c12-200">На жестком диске. Создайте и сохраните вторичный индекс на диске.</span><span class="sxs-lookup"><span data-stu-id="e1c12-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c12-201">maxSize</span><span class="sxs-lookup"><span data-stu-id="e1c12-201">maxSize</span></span></td>
<td><span data-ttu-id="e1c12-202">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e1c12-202">Optional.</span></span> <span data-ttu-id="e1c12-203">Указывает максимальный размер, допустимый для значения свойства, хранящегося в базе данных поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="e1c12-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="e1c12-204">Это ограничение применяется к элементам индвидуал вектора, а не к вектору в целом.</span><span class="sxs-lookup"><span data-stu-id="e1c12-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="e1c12-205">Значения, превышающие этот размер, усекаются.</span><span class="sxs-lookup"><span data-stu-id="e1c12-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="e1c12-206">Значение по умолчанию — &quot; 128 &quot; (байт).</span><span class="sxs-lookup"><span data-stu-id="e1c12-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="e1c12-207">В настоящее время при вычислении объема данных, принимаемых из файла, Поиск Windows не использует параметр maxSize.</span><span class="sxs-lookup"><span data-stu-id="e1c12-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="e1c12-208">Вместо этого в средстве поиска Windows используется ограничение на размер файла и Максгровфактор (Размер файла N \* Максгровфактор), считанные из реестра в HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->диспетчере сбора — >Максгровфактор.</span><span class="sxs-lookup"><span data-stu-id="e1c12-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="e1c12-209">Максгровфактор по умолчанию — четыре (4).</span><span class="sxs-lookup"><span data-stu-id="e1c12-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="e1c12-210">Следовательно, если тип файла является небольшим в общем размере, но имеет большие свойства, Поиск Windows может не принимать все данные свойства, которые вы хотите выпустить.</span><span class="sxs-lookup"><span data-stu-id="e1c12-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="e1c12-211">Однако вы можете увеличить Максгровфактор в соответствии со своими потребностями.</span><span class="sxs-lookup"><span data-stu-id="e1c12-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="e1c12-212">Для атрибута Колумниндекстипе преимущество более быстрых запросов должно быть в сравнении с увеличением времени индексирования и затратами на пространство, которые могут повлечь дополнительные индексы.</span><span class="sxs-lookup"><span data-stu-id="e1c12-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="e1c12-213">Однако эта стоимость оплачивается только для тех элементов, которые имеют значение, отличное от **null** , поэтому для большинства свойств этот атрибут можно задать равным "ondisk".</span><span class="sxs-lookup"><span data-stu-id="e1c12-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="e1c12-214">Поддержка полнотекстовых каталогов</span><span class="sxs-lookup"><span data-stu-id="e1c12-214">Full-Text Support</span></span>

<span data-ttu-id="e1c12-215">Как правило, полнотекстовый поиск поддерживается компонентами, называемыми [фильтрами](-search-3x-wds-extidx-filters.md). Однако для текстовых типов файлов с несложными форматами файлов обработчики свойств могут предоставлять эту функцию с меньшим объемом усилий при разработке.</span><span class="sxs-lookup"><span data-stu-id="e1c12-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="e1c12-216">Ознакомьтесь с разделом [Full-Text Content](../properties/building-property-handlers-property-handlers.md) , чтобы сравнить функциональные возможности обработчика фильтров и свойств, чтобы решить, что лучше всего подходит для вашего типа файлов.</span><span class="sxs-lookup"><span data-stu-id="e1c12-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="e1c12-217">Важно то, что фильтры могут обрабатывали несколько идентификаторов языка (LCID) для каждого файла, а обработчики свойств — нет.</span><span class="sxs-lookup"><span data-stu-id="e1c12-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="e1c12-218">Так как обработчики свойств не могут поблочировать содержимое, так как фильтры могут, большие файлы (даже если они являются несложными форматами файлов) должны быть полностью загружены в память.</span><span class="sxs-lookup"><span data-stu-id="e1c12-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="e1c12-219">Рекомендации по Имплементататион операционной системы</span><span class="sxs-lookup"><span data-stu-id="e1c12-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="e1c12-220">Сведения о реализации Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1c12-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="e1c12-221">В Windows 7 и более поздних версиях существует новое поведение при регистрации обработчика свойства, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)или нового расширения.</span><span class="sxs-lookup"><span data-stu-id="e1c12-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="e1c12-222">При установке нового обработчика свойств и (или) **IFilter** файлы с соответствующими расширениями автоматически индексируются.</span><span class="sxs-lookup"><span data-stu-id="e1c12-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="e1c12-223">В Windows 7 рекомендуется устанавливать [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) вместе с соответствующими обработчиками свойств, а **IFilter** регистрироваться перед обработчиком свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="e1c12-224">Регистрация обработчика свойств инициирует немедленную повторную индексацию ранее индексированных файлов, не требуя предварительной перезагрузки, и использует преимущества всех ранее зарегистрированных IFilter (-ов) для индексации содержимого.</span><span class="sxs-lookup"><span data-stu-id="e1c12-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="e1c12-225">Если установлен только интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) без соответствующего обработчика свойства, то автоматическая повторная индексация происходит либо после перезапуска службы индексирования, либо после перезагрузки системы.</span><span class="sxs-lookup"><span data-stu-id="e1c12-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="e1c12-226">Для флагов описания свойств, характерных для Windows 7, см. следующие справочные разделы:</span><span class="sxs-lookup"><span data-stu-id="e1c12-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="e1c12-227">жетпропертисторефлагс</span><span class="sxs-lookup"><span data-stu-id="e1c12-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="e1c12-228">\_тип COLUMNINDEX \_ пропдеск</span><span class="sxs-lookup"><span data-stu-id="e1c12-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="e1c12-229">\_ \_ Флаги сеарчинфо пропдеск</span><span class="sxs-lookup"><span data-stu-id="e1c12-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="e1c12-230">Сведения о реализации Windows Vista и более ранних версий</span><span class="sxs-lookup"><span data-stu-id="e1c12-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="e1c12-231">До выхода Windows Vista фильтры поддерживали синтаксический анализ и перечисление содержимого файлов и свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="e1c12-232">С появлением системы свойств обработчики свойств обрабатывали свойства файла, а фильтры обрабатывали содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="e1c12-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="e1c12-233">Для Windows Vista необходимо разработать только частичную реализацию интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)в координации с обработчиком свойств, как описано в разделе рекомендации [по созданию обработчиков фильтров в службе поиска Windows](-search-3x-wds-extidx-filters.md).</span><span class="sxs-lookup"><span data-stu-id="e1c12-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="e1c12-234">Хотя система свойств также включена в установку Windows Search для Windows XP, сторонние и устаревшие приложения могут потребовать, чтобы фильтры обрабатывали как содержимое, так и свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="e1c12-235">Поэтому при разработке на платформе Windows XP необходимо предоставить полную реализацию фильтра, а также обработчик свойств для типа файла или пользовательского свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="e1c12-236">Запись файлов описания свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-236">Writing Property Description Files</span></span>

<span data-ttu-id="e1c12-237">Структура XML-файлов описания свойств (. пропдеск) описана в разделе [пропертидескриптион](../properties/propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c12-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="e1c12-238">Определенный интерес для поиска — атрибуты элемента [сеарчинфо](../properties/propdesc-schema-searchinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e1c12-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="e1c12-239">После выбора свойств для поддержки необходимо создать и зарегистрировать файлы описания свойств для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="e1c12-240">При регистрации пропдеск файлов они включаются в список свойств схемы и становятся именами столбцов в хранилище свойств поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="e1c12-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="e1c12-241">Вы можете зарегистрировать описания пользовательских свойств с помощью функции [псрегистерпропертисчема](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , API-оболочки, вызывающей ипропертисистем:: регистерпропертисчема подсистемы схемы.</span><span class="sxs-lookup"><span data-stu-id="e1c12-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="e1c12-242">Эта функция информирует подсистему схемы добавления файлов схемы описания свойств (. пропдеск), используя пути к файлам. пропдеск на локальном компьютере, обычно каталог установки приложения в разделе "Program Files".</span><span class="sxs-lookup"><span data-stu-id="e1c12-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="e1c12-243">Как правило, установка или приложение (например, установщик обработчика свойств) будут вызывать этот метод после установки пропдеск-файлов.</span><span class="sxs-lookup"><span data-stu-id="e1c12-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="e1c12-244">Реализация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-244">Implementing Property Handlers</span></span>

<span data-ttu-id="e1c12-245">Разработка обработчика свойств включает реализацию следующих интерфейсов:</span><span class="sxs-lookup"><span data-stu-id="e1c12-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="e1c12-246">Иинитиалзевисстреам: обеспечивает инициализацию обработчика свойств на основе потока.</span><span class="sxs-lookup"><span data-stu-id="e1c12-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="e1c12-247">Ипропертисторе: перечисляет, возвращает и задает значения свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="e1c12-248">Ипропертисторекапабилитиес: необязательный.</span><span class="sxs-lookup"><span data-stu-id="e1c12-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="e1c12-249">Определяет, могут ли пользователи изменять свойство из пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e1c12-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="e1c12-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="e1c12-250">IInitializeWithStream</span></span>

<span data-ttu-id="e1c12-251">Как описано в разделе [система свойств](../properties/building-property-handlers.md) , настоятельно рекомендуется реализовать обработчики свойств с **IInitializeWithStream** для инициализации на основе потоков.</span><span class="sxs-lookup"><span data-stu-id="e1c12-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="e1c12-252">Если вы решили не реализовывать IInitializeWithStream, обработчик свойств должен отказаться от выполнения в процессе изоляции, установив флаг Дисаблепроцессисолатион в разделе реестра обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="e1c12-253">Отключение изоляции процессов обычно предназначено только для устаревших обработчиков свойств и должно быть стренуауслио без какого-либо нового кода.</span><span class="sxs-lookup"><span data-stu-id="e1c12-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="e1c12-254">ипропертисторе</span><span class="sxs-lookup"><span data-stu-id="e1c12-254">IPropertyStore</span></span>

<span data-ttu-id="e1c12-255">Чтобы создать обработчик свойства, необходимо реализовать интерфейс [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) со следующими методами.</span><span class="sxs-lookup"><span data-stu-id="e1c12-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="e1c12-256">Метод</span><span class="sxs-lookup"><span data-stu-id="e1c12-256">Method</span></span>   | <span data-ttu-id="e1c12-257">Описание</span><span class="sxs-lookup"><span data-stu-id="e1c12-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="e1c12-258">Commit</span><span class="sxs-lookup"><span data-stu-id="e1c12-258">Commit</span></span>   | <span data-ttu-id="e1c12-259">Сохраняет изменение свойства в файле.</span><span class="sxs-lookup"><span data-stu-id="e1c12-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="e1c12-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="e1c12-260">GetAt</span></span>    | <span data-ttu-id="e1c12-261">Извлекает ключ свойства из массива свойств элемента.</span><span class="sxs-lookup"><span data-stu-id="e1c12-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="e1c12-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="e1c12-262">GetCount</span></span> | <span data-ttu-id="e1c12-263">Возвращает число свойств, присоединенных к файлу.</span><span class="sxs-lookup"><span data-stu-id="e1c12-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="e1c12-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="e1c12-264">GetValue</span></span> | <span data-ttu-id="e1c12-265">Извлекает данные для определенного свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="e1c12-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="e1c12-266">SetValue</span></span> | <span data-ttu-id="e1c12-267">Задает новое значение свойства или заменяет или удаляет существующее значение.</span><span class="sxs-lookup"><span data-stu-id="e1c12-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="e1c12-268">Важные рекомендации по реализации этого интерфейса включены в документацию по [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="e1c12-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="e1c12-269">Если обработчик свойств создает несколько значений для одного и того же свойства для заданного элемента, в каталог сохраняется только Последнее значение.</span><span class="sxs-lookup"><span data-stu-id="e1c12-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="e1c12-270">ипропертисторекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="e1c12-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="e1c12-271">При необходимости обработчики свойств могут реализовать этот интерфейс, чтобы запретить пользователю изменять определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="e1c12-272">Эти свойства обычно могут быть изменены на странице сведений и на панели, но их редактирование запрещено в обработчике реализующего свойства.</span><span class="sxs-lookup"><span data-stu-id="e1c12-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="e1c12-273">Правильная реализация этого интерфейса обеспечивает более удобный пользовательский интерфейс, чем альтернатива — простую ошибку времени выполнения из оболочки.</span><span class="sxs-lookup"><span data-stu-id="e1c12-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="e1c12-274">Проверка индексации элементов</span><span class="sxs-lookup"><span data-stu-id="e1c12-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="e1c12-275">Теперь, когда вы реализовали обработчик свойств, необходимо убедиться, что элементы обработчика зарегистрированы для получения индекса.</span><span class="sxs-lookup"><span data-stu-id="e1c12-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="e1c12-276">Для инициации повторного индексирования можно использовать [Диспетчер каталогов](-search-3x-wds-mngidx-catalog-manager.md) . Кроме того, можно использовать [Диспетчер области сканирования](-search-3x-wds-extidx-csm.md) для настройки правил по умолчанию, указывающих URL-адреса, которые должен обходить индексатор.</span><span class="sxs-lookup"><span data-stu-id="e1c12-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="e1c12-277">Другой вариант — выполнить пример кода переиндексации в [примерах пакета SDK для Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="e1c12-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="e1c12-278">Дополнительные сведения см. в разделе [Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md) и [диспетчера области сканирования](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="e1c12-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="e1c12-279">Установка и регистрация обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="e1c12-280">При реализации обработчика свойств необходимо зарегистрировать его и расширение имени файла, связанное с обработчиком.</span><span class="sxs-lookup"><span data-stu-id="e1c12-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="e1c12-281">В следующем примере показаны разделы и значения реестра, необходимые для этого.</span><span class="sxs-lookup"><span data-stu-id="e1c12-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="e1c12-282">Тестирование и устранение неполадок обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="e1c12-283">В следующем списке приведены рекомендации по типам выполняемых тестов.</span><span class="sxs-lookup"><span data-stu-id="e1c12-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="e1c12-284">Проверка получения выходных данных из каждого отдельного свойства, поддерживаемого типом файла.</span><span class="sxs-lookup"><span data-stu-id="e1c12-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="e1c12-285">Используйте большие значения свойств, например крупные метатаг в HTML-документах.</span><span class="sxs-lookup"><span data-stu-id="e1c12-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="e1c12-286">Убедитесь, что обработчик свойств не получает дескрипторы файлов, отредактировав его после получения выходных данных из обработчика свойств или с помощью такого средства, как oh.exe до и после перечисления свойств файла.</span><span class="sxs-lookup"><span data-stu-id="e1c12-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="e1c12-287">Проверьте все типы файлов, связанные с обработчиком свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="e1c12-288">Например, убедитесь, что фильтр HTML работает с типами файлов HTM и HTML.</span><span class="sxs-lookup"><span data-stu-id="e1c12-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="e1c12-289">Тестирование с поврежденными файлами.</span><span class="sxs-lookup"><span data-stu-id="e1c12-289">Test with corrupted files.</span></span> <span data-ttu-id="e1c12-290">Корректное завершение обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="e1c12-291">Если приложение поддерживает шифрование, проверьте, что обработчик свойства не выводит зашифрованный текст.</span><span class="sxs-lookup"><span data-stu-id="e1c12-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="e1c12-292">Если обработчик свойств поддерживает полнотекстовый поиск:</span><span class="sxs-lookup"><span data-stu-id="e1c12-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="e1c12-293">Используйте в содержимом файлов несколько специальных символов Юникода и проверьте их выходные данные.</span><span class="sxs-lookup"><span data-stu-id="e1c12-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="e1c12-294">Протестируйте обработку очень больших документов, чтобы убедиться, что обработчик свойств работает правильно.</span><span class="sxs-lookup"><span data-stu-id="e1c12-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="e1c12-295">Тесты установки и установки</span><span class="sxs-lookup"><span data-stu-id="e1c12-295">Installation and Setup Tests</span></span>

<span data-ttu-id="e1c12-296">Наконец, необходимо протестировать подпрограммы установки и удаления.</span><span class="sxs-lookup"><span data-stu-id="e1c12-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="e1c12-297">Установка должна быть восстановлена после неудачных установок (например, после отмены и повторного запуска программы установки).</span><span class="sxs-lookup"><span data-stu-id="e1c12-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="e1c12-298">Удаление должно удалить все файлы, связанные с обработчиком свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="e1c12-299">Удаление не должно удалять файлы, отличные от тех, которые связаны с установкой обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="e1c12-300">Разделы реестра, связанные с обработчиком свойств, должны быть удалены при удалении.</span><span class="sxs-lookup"><span data-stu-id="e1c12-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="e1c12-301">Удаление должно работать, даже если файлы удаляются из каталога установки.</span><span class="sxs-lookup"><span data-stu-id="e1c12-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="e1c12-302">Устранение неполадок обработчиков свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="e1c12-303">Ниже приведены некоторые распространенные ошибки, возникающие при разработке обработчиков свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="e1c12-304">Установка файлов. пропдеск или библиотек DLL в каталоге пользователя.</span><span class="sxs-lookup"><span data-stu-id="e1c12-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="e1c12-305">Регистрация компонентов с использованием относительных путей.</span><span class="sxs-lookup"><span data-stu-id="e1c12-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="e1c12-306">Регистрация компонентов в разделе HKEY \_ текущий \_ пользователь, а не на \_ локальном компьютере hKey \_ .</span><span class="sxs-lookup"><span data-stu-id="e1c12-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="e1c12-307">Не удается задать Дисаблепроцессисолатион для обработчиков, не являющихся потоками.</span><span class="sxs-lookup"><span data-stu-id="e1c12-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="e1c12-308">Размещение тестового файла в неиндексированном расположении.</span><span class="sxs-lookup"><span data-stu-id="e1c12-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="e1c12-309">Если у вас возникают проблемы с работой обработчика свойств с индексатором, вот несколько советов по устранению неполадок:</span><span class="sxs-lookup"><span data-stu-id="e1c12-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="e1c12-310">Убедитесь, что описания свойств (пропдеск-файлы) помечены как "IsTrue" = "**true**", "View" = "**true**", а для "IsTrue" — "**true**" соответственно.</span><span class="sxs-lookup"><span data-stu-id="e1c12-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="e1c12-311">Убедитесь, что пропдеск-файлы находятся в глобальном расположении.</span><span class="sxs-lookup"><span data-stu-id="e1c12-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="e1c12-312">Убедитесь, что пропдеск файлы зарегистрированы с помощью абсолютных путей.</span><span class="sxs-lookup"><span data-stu-id="e1c12-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="e1c12-313">Убедитесь, что в журнале событий не записаны сбои при регистрации файла. пропдеск.</span><span class="sxs-lookup"><span data-stu-id="e1c12-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="e1c12-314">Убедитесь, что библиотеки DLL находятся в глобальном расположении (а не в вашем профиле пользователя).</span><span class="sxs-lookup"><span data-stu-id="e1c12-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="e1c12-315">Убедитесь, что библиотеки DLL зарегистрированы в \_ разделе \_ \\ классы программного обеспечения для локального компьютера hKey \\ .</span><span class="sxs-lookup"><span data-stu-id="e1c12-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="e1c12-316">Убедитесь, что библиотеки DLL зарегистрированы с использованием полных путей (или строки с РАСШИРЕНИЕМ \_ \_ SZ, которые расширяются до абсолютных путей с помощью переменных среды, известных системной учетной записью).</span><span class="sxs-lookup"><span data-stu-id="e1c12-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="e1c12-317">Убедитесь, что обработчик свойств работает в проводнике Windows.</span><span class="sxs-lookup"><span data-stu-id="e1c12-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="e1c12-318">Хотя мы рекомендуем использовать IInitializeWithStream, при необходимости использования IInitializeWithFile или Иинитиализевиситем убедитесь, что вы указали Дисаблепроцессисолатион.</span><span class="sxs-lookup"><span data-stu-id="e1c12-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="e1c12-319">Убедитесь, что в панели управления параметры индексирования список типов файлов указан в виде индексированного типа файлов.</span><span class="sxs-lookup"><span data-stu-id="e1c12-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="e1c12-320">Убедитесь, что тестовый файл находится в индексированном расположении.</span><span class="sxs-lookup"><span data-stu-id="e1c12-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="e1c12-321">Убедитесь, что тестовый файл был изменен со времени установки обработчика свойств.</span><span class="sxs-lookup"><span data-stu-id="e1c12-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="e1c12-322">Если тестовый файл находится в индексированном расположении, а индексатор уже выполнил обход содержимого этого расположения, необходимо изменить файл каким-либо образом, чтобы запустить повторное индексирование файла.</span><span class="sxs-lookup"><span data-stu-id="e1c12-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="e1c12-323">Использование обработчиков свойств System-Supplied</span><span class="sxs-lookup"><span data-stu-id="e1c12-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="e1c12-324">Windows включает ряд обработчиков свойств, предоставляемых системой, которые можно использовать, если формат файла совместим.</span><span class="sxs-lookup"><span data-stu-id="e1c12-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="e1c12-325">При определении нового расширения файла, использующего один из этих форматов, можно использовать предоставляемые системой обработчики, зарегистрировав идентификатор класса обработчика (CLSID) для расширения файла.</span><span class="sxs-lookup"><span data-stu-id="e1c12-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="e1c12-326">Для регистрации системных обработчиков свойств для типа формата файла можно использовать идентификатор CLSID, приведенный в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e1c12-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="e1c12-327">Формат</span><span class="sxs-lookup"><span data-stu-id="e1c12-327">Format</span></span>          | <span data-ttu-id="e1c12-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="e1c12-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="e1c12-329">Докфиле OLE</span><span class="sxs-lookup"><span data-stu-id="e1c12-329">OLE DocFile</span></span>     | <span data-ttu-id="e1c12-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span><span class="sxs-lookup"><span data-stu-id="e1c12-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="e1c12-331">Сохранение игрового XML</span><span class="sxs-lookup"><span data-stu-id="e1c12-331">Save Game XML</span></span>   | <span data-ttu-id="e1c12-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="e1c12-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="e1c12-333">Обработчик XPS/OPC</span><span class="sxs-lookup"><span data-stu-id="e1c12-333">XPS/OPC handler</span></span> | <span data-ttu-id="e1c12-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span><span class="sxs-lookup"><span data-stu-id="e1c12-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="e1c12-335">XML</span><span class="sxs-lookup"><span data-stu-id="e1c12-335">XML</span></span>             | <span data-ttu-id="e1c12-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="e1c12-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="e1c12-337">Перед созданием пользовательского свойства необходимо убедиться, что не определено системное свойство, которое можно использовать.</span><span class="sxs-lookup"><span data-stu-id="e1c12-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="e1c12-338">Вы можете перечислить определяемые системой свойства, вызвав [**псенумератепропертидескриптионс**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) или используя средство командной строки prop.exe.</span><span class="sxs-lookup"><span data-stu-id="e1c12-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="e1c12-339">Системная схема определяет, как эти свойства взаимодействуют с индексатором, и вы не можете изменить это свойство.</span><span class="sxs-lookup"><span data-stu-id="e1c12-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="e1c12-340">Кроме того, приложение, используемое для создания, изменения и сохранения типа файлов, должно также соответствовать определенному поведению.</span><span class="sxs-lookup"><span data-stu-id="e1c12-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="e1c12-341">Например, если приложение реализует безусловное сохранение (при этом во время редактирования создается временный файл, а затем Реплацефиле () используется для замены новой версии старой), она должна переносить все свойства из исходного файла в новый файл.</span><span class="sxs-lookup"><span data-stu-id="e1c12-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="e1c12-342">Сбой означает, что файл теряет свойства, добавленные пользователями или другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="e1c12-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="e1c12-343">**Пример**</span><span class="sxs-lookup"><span data-stu-id="e1c12-343">**Example**</span></span>

<span data-ttu-id="e1c12-344">Ниже показана регистрация предоставляемого системой обработчика Докфиле OLE для типа файла с. Расширение Оледокфиле.</span><span class="sxs-lookup"><span data-stu-id="e1c12-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="e1c12-345">Ниже показано, как зарегистрировать сведения о списке свойств, чтобы получить свойства. Файлы Оледокфиле отображаются на вкладке и области сведений.</span><span class="sxs-lookup"><span data-stu-id="e1c12-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="e1c12-346">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e1c12-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e1c12-347">**Reference**</span><span class="sxs-lookup"><span data-stu-id="e1c12-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e1c12-348">Сопоставления свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="e1c12-349">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="e1c12-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e1c12-350">Рекомендации по созданию обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="e1c12-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="e1c12-351">Процесс индексирования</span><span class="sxs-lookup"><span data-stu-id="e1c12-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="e1c12-352">Разработка обработчиков протоколов</span><span class="sxs-lookup"><span data-stu-id="e1c12-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="e1c12-353">Определяемые системой свойства для пользовательских форматов файлов</span><span class="sxs-lookup"><span data-stu-id="e1c12-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="e1c12-354">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="e1c12-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e1c12-355">Система свойств</span><span class="sxs-lookup"><span data-stu-id="e1c12-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="e1c12-356">[Свойства системы](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="e1c12-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="e1c12-357">Примеры пакета SDK для Windows Search</span><span class="sxs-lookup"><span data-stu-id="e1c12-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
