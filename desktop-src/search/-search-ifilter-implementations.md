---
description: Корпорация Майкрософт предоставляет несколько стандартных фильтров для поиска Windows. Клиенты вызывают эти обработчики фильтров (которые являются реализациями интерфейса IFilter) для извлечения текста и свойств из документа.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Обработчики фильтров, поставляемые с Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144128"
---
# <a name="filter-handlers-that-ship-with-windows"></a><span data-ttu-id="7874e-104">Обработчики фильтров, поставляемые с Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-104">Filter Handlers that Ship with Windows</span></span>

<span data-ttu-id="7874e-105">Корпорация Майкрософт предоставляет несколько стандартных фильтров для поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="7874e-105">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="7874e-106">Клиенты вызывают эти обработчики фильтров (которые являются реализациями интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) для извлечения текста и свойств из документа.</span><span class="sxs-lookup"><span data-stu-id="7874e-106">Clients call these filter handlers (which are implementations of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface) to extract text and properties from a document.</span></span>

<span data-ttu-id="7874e-107">Этот раздел организован следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7874e-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="7874e-108">Примечания по реализации поиска Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-108">Windows Search Implementation Notes</span></span>](#windows-search-implementation-notes)
  - [<span data-ttu-id="7874e-109">Реализация Windows 7 и 10</span><span class="sxs-lookup"><span data-stu-id="7874e-109">Windows 7 and 10 Implementation</span></span>](#windows-7-and-10-implementation)
  - [<span data-ttu-id="7874e-110">Реализация Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7874e-110">Windows Vista Implementation</span></span>](#windows-vista-implementation)
  - [<span data-ttu-id="7874e-111">Устаревшая реализация</span><span class="sxs-lookup"><span data-stu-id="7874e-111">Legacy Implementation</span></span>](#legacy-implementation)
- [<span data-ttu-id="7874e-112">Фильтры поиска Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-112">Windows Search Filters</span></span>](#filter-handlers-that-ship-with-windows)
  - [<span data-ttu-id="7874e-113">Обработчик фильтра MIME</span><span class="sxs-lookup"><span data-stu-id="7874e-113">MIME Filter Handler</span></span>](#mime-filter-handler)
  - [<span data-ttu-id="7874e-114">Обработчик фильтра HTML</span><span class="sxs-lookup"><span data-stu-id="7874e-114">HTML Filter Handler</span></span>](#html-filter-handler)
  - [<span data-ttu-id="7874e-115">Обработчик фильтра документов</span><span class="sxs-lookup"><span data-stu-id="7874e-115">Document Filter Handler</span></span>](#document-filter-handler)
  - [<span data-ttu-id="7874e-116">Обработчик обычного текстового фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-116">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)
  - [<span data-ttu-id="7874e-117">Обработчик бинарного или неопределенного фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-117">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler)
- [<span data-ttu-id="7874e-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7874e-118">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="7874e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7874e-119">Related topics</span></span>](#related-topics)

## <a name="windows-search-implementation-notes"></a><span data-ttu-id="7874e-120">Примечания по реализации поиска Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-120">Windows Search Implementation Notes</span></span>

<span data-ttu-id="7874e-121">В Windows 7 и более поздних версиях фильтры, написанные в управляемом коде, явным образом блокируются.</span><span class="sxs-lookup"><span data-stu-id="7874e-121">In Windows 7 and later, filters written in managed code are explicitly blocked.</span></span> <span data-ttu-id="7874e-122">Фильтры должны быть написаны в машинном коде из-за потенциальных проблем с управлением версиями среды CLR в процессе выполнения нескольких надстроек.</span><span class="sxs-lookup"><span data-stu-id="7874e-122">Filters MUST be written in native code due to potential CLR versioning issues with the process that multiple add-ins run in.</span></span>

### <a name="windows-7-and-10-implementation"></a><span data-ttu-id="7874e-123">Реализация Windows 7 и 10</span><span class="sxs-lookup"><span data-stu-id="7874e-123">Windows 7 and 10 Implementation</span></span>

<span data-ttu-id="7874e-124">В Windows 7 и более поздних версиях существует новое поведение, возникающее при регистрации обработчика фильтра, обработчика свойств или нового расширения.</span><span class="sxs-lookup"><span data-stu-id="7874e-124">In Windows 7 and later, there is new behavior that occurs when registering a filter handler, property handler, or new extension.</span></span> <span data-ttu-id="7874e-125">При установке нового обработчика свойств и (или) обработчика фильтра файлы с соответствующими расширениями автоматически индексируются повторно.</span><span class="sxs-lookup"><span data-stu-id="7874e-125">When a new property handler and/or filter handler is installed, files with the corresponding extensions are automatically re-indexed.</span></span>

<span data-ttu-id="7874e-126">В Windows 7 и более поздних версиях рекомендуется установить обработчик фильтра в сочетании с соответствующими обработчиками свойств и зарегистрировать обработчик фильтра перед обработчиком свойства.</span><span class="sxs-lookup"><span data-stu-id="7874e-126">In Windows 7 and later, we recommend that you install a filter handler in conjunction with its corresponding property handlers, and that you register the filter handler before the property handler.</span></span> <span data-ttu-id="7874e-127">Регистрация обработчика свойств инициирует немедленную повторную индексацию ранее индексированных файлов без необходимости предварительной перезагрузки и использует преимущества всех ранее зарегистрированных обработчиков фильтров для индексирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="7874e-127">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a restart, and takes advantage of any previously registered filter handlers for the purpose of content indexing.</span></span>

<span data-ttu-id="7874e-128">Если только обработчик фильтра установлен без соответствующего обработчика свойства, то автоматическое повторное индексирование происходит либо после перезапуска службы индексирования, либо после перезапуска системы.</span><span class="sxs-lookup"><span data-stu-id="7874e-128">If only a filter handler is installed without a corresponding property handler, then automatic re-indexing occurs either after a restart of the indexing service, or a restart of the system.</span></span>

<span data-ttu-id="7874e-129">Для флагов описания свойств, характерных для Windows 7, см. следующие справочные разделы: [жетпропертисторефлагс](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [пропдеск \_ COLUMNINDEX \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) и [пропдеск \_ сеарчинфо \_ flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span><span class="sxs-lookup"><span data-stu-id="7874e-129">For property description flags specific to Windows 7, see the following reference topics: [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PROPDESC\_COLUMNINDEX\_TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) and [PROPDESC\_SEARCHINFO\_FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).</span></span>

### <a name="windows-vista-implementation"></a><span data-ttu-id="7874e-130">Реализация Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7874e-130">Windows Vista Implementation</span></span>

<span data-ttu-id="7874e-131">В Windows Vista и более ранних версиях установка обработчика [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) или свойства не инициирует повторную индексацию существующих элементов, если только независимый поставщик программного обеспечения явно не вызывает перестроение или повторную индексацию соответствующих URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="7874e-131">In Windows Vista and earlier, installing an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) or property handler does not initiate a re-indexing of existing items unless an independent software vendor (ISV) explicitly calls a rebuild or re-indexing of matching URLs.</span></span>

<span data-ttu-id="7874e-132">Существуют два основных различия между устаревшими приложениями, такими как служба индексирования и более новые приложения, такие как поиск Windows, которые следует учитывать при реализации фильтров:</span><span class="sxs-lookup"><span data-stu-id="7874e-132">There are two major differences between legacy applications like Indexing Service and newer applications like Windows Search that you should be aware of when implementing filters:</span></span>

- <span data-ttu-id="7874e-133">Использование интерфейса [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .</span><span class="sxs-lookup"><span data-stu-id="7874e-133">Use of the [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface.</span></span>
- <span data-ttu-id="7874e-134">Использование обработчиков свойств.</span><span class="sxs-lookup"><span data-stu-id="7874e-134">Use of property handlers.</span></span>

<span data-ttu-id="7874e-135">Прежде всего, для Windows Vista и Windows Search 3,0 и более поздних версий требуется использовать [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="7874e-135">First, Windows Vista and Windows Search 3.0 and later require you use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) for the following reasons:</span></span>

- <span data-ttu-id="7874e-136">Для обеспечения производительности и будущей совместимости.</span><span class="sxs-lookup"><span data-stu-id="7874e-136">To ensure performance and future compatibility.</span></span>
- <span data-ttu-id="7874e-137">Для повышения безопасности.</span><span class="sxs-lookup"><span data-stu-id="7874e-137">To help increase security.</span></span> <span data-ttu-id="7874e-138">Фильтры, реализованные с помощью [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) , более безопасны, поскольку контекст, в котором выполняется фильтр, не требует наличия прав на открытие файлов на диске или по сети.</span><span class="sxs-lookup"><span data-stu-id="7874e-138">Filters implemented with [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) are more secure because the context in which the filter runs does not need the rights to open files on the disk or over the network.</span></span>

<span data-ttu-id="7874e-139">Хотя в Windows Search используется только [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), в фильтрах можно также включить реализации интерфейса [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) и/или [иперсистстораже](/windows/win32/api/objidl/nn-objidl-ipersiststorage) , чтобы обеспечить обратную совместимость.</span><span class="sxs-lookup"><span data-stu-id="7874e-139">While Windows Search uses only [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), you can also include [IPersistFile Interface](/windows/win32/api/objidl/nn-objidl-ipersistfile) and/or [IPersistStorage Interface](/windows/win32/api/objidl/nn-objidl-ipersiststorage) implementations in your filters for backward compatibility.</span></span>

<span data-ttu-id="7874e-140">Второе основное отличие заключается в том, что Windows Vista и Windows Search 3,0 и более поздних версий имеют новую [систему свойств](../properties/building-property-handlers.md) , использующую обработчики свойств для перечисления свойств элементов.</span><span class="sxs-lookup"><span data-stu-id="7874e-140">The second major difference is that Windows Vista and Windows Search 3.0 and later have a new [Property System](../properties/building-property-handlers.md) that uses property handlers to enumerate properties of items.</span></span>

<span data-ttu-id="7874e-141">Однако иногда требуется реализовать фильтр, который обрабатывает как содержимое, так и свойства, чтобы:</span><span class="sxs-lookup"><span data-stu-id="7874e-141">However, there are times when you need to implement a filter that handles both content and properties in order to:</span></span>

- <span data-ttu-id="7874e-142">Поддержка устаревших реализаций MSSearch.</span><span class="sxs-lookup"><span data-stu-id="7874e-142">Support legacy MSSearch implementations.</span></span>
- <span data-ttu-id="7874e-143">Просмотр ссылок.</span><span class="sxs-lookup"><span data-stu-id="7874e-143">Traverse links.</span></span>
- <span data-ttu-id="7874e-144">Сохранение сведений о языке.</span><span class="sxs-lookup"><span data-stu-id="7874e-144">Preserve language information.</span></span>
- <span data-ttu-id="7874e-145">Рекурсивно фильтровать внедренные элементы.</span><span class="sxs-lookup"><span data-stu-id="7874e-145">Recursively filter embedded items.</span></span>

<span data-ttu-id="7874e-146">В таких ситуациях требуется полная реализация фильтра, включая метод [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) для доступа к значениям свойств.</span><span class="sxs-lookup"><span data-stu-id="7874e-146">In these situations, you need a full filter implementation, including the [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) method to access property values.</span></span>

### <a name="legacy-implementation"></a><span data-ttu-id="7874e-147">Устаревшая реализация</span><span class="sxs-lookup"><span data-stu-id="7874e-147">Legacy Implementation</span></span>

<span data-ttu-id="7874e-148">Как отмечалось ранее, Windows Vista и Windows Search включают новую систему свойств, которая инкапсулирует свойства элемента, которые отделены от содержимого элемента.</span><span class="sxs-lookup"><span data-stu-id="7874e-148">As noted earlier, Windows Vista and Windows Search include a new property system that encapsulates an item's properties that is separate from an item's content.</span></span> <span data-ttu-id="7874e-149">Эта система свойств не существует в более ранних версиях Microsoft Windows Desktop Search (WDS) 2. x.</span><span class="sxs-lookup"><span data-stu-id="7874e-149">This property system does not exist in earlier versions of Microsoft Windows Desktop Search (WDS) 2.x.</span></span> <span data-ttu-id="7874e-150">Если фильтр должен поддерживать другие приложения, как описано выше, может потребоваться выполнить обработку как содержимого, так и свойств.</span><span class="sxs-lookup"><span data-stu-id="7874e-150">If your filter must support other applications as described above, it may need to handle both content and properties.</span></span>

<span data-ttu-id="7874e-151">Дополнительные сведения о разработке совместимого фильтра см. в следующих разделах: [IFilter (для устаревших приложений)](/windows/win32/api/filter/nn-filter-ifilter)и [Разработка надстроек фильтров (для устаревших приложений)](../lwef/-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="7874e-151">For more information on developing a compatible filter, see the following topics, [IFilter (for legacy applications)](/windows/win32/api/filter/nn-filter-ifilter), and [Developing Filter Add-ins (for legacy applications)](../lwef/-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="windows-search-filters"></a><span data-ttu-id="7874e-152">Фильтры поиска Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-152">Windows Search Filters</span></span>

<span data-ttu-id="7874e-153">Корпорация Майкрософт предоставляет несколько стандартных фильтров для поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="7874e-153">Microsoft supplies several standard filters with Windows Search.</span></span> <span data-ttu-id="7874e-154">В следующей таблице приведены сводные данные по содержимому библиотеки [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  .</span><span class="sxs-lookup"><span data-stu-id="7874e-154">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  DLL contents are summarized in the following table.</span></span> <span data-ttu-id="7874e-155">Щелкнув имя обработчика фильтра, можно перейти к описанию реализации **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="7874e-155">Clicking the name of a filter handler takes you to the description for that **IFilter** implementation.</span></span>

| <span data-ttu-id="7874e-156">Обработчик фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-156">Filter handler</span></span>                                                  | <span data-ttu-id="7874e-157">Отфильтрованные файлы</span><span class="sxs-lookup"><span data-stu-id="7874e-157">Files filtered</span></span>                              | <span data-ttu-id="7874e-158">Библиотека DLL IFilter</span><span class="sxs-lookup"><span data-stu-id="7874e-158">IFilter DLL</span></span>  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [<span data-ttu-id="7874e-159">Обработчик фильтра MIME</span><span class="sxs-lookup"><span data-stu-id="7874e-159">MIME Filter Handler</span></span>](#mime-filter-handler)                     | <span data-ttu-id="7874e-160">Многоцелевое расширение электронной почты в Интернете (MIME)</span><span class="sxs-lookup"><span data-stu-id="7874e-160">Multipurpose Internet Mail Extension (MIME)</span></span> | <span data-ttu-id="7874e-161">mimefilt.dll</span><span class="sxs-lookup"><span data-stu-id="7874e-161">mimefilt.dll</span></span> |
| [<span data-ttu-id="7874e-162">Обработчик фильтра HTML</span><span class="sxs-lookup"><span data-stu-id="7874e-162">HTML Filter Handler</span></span>](#html-filter-handler)                     | <span data-ttu-id="7874e-163">HTML 3,0 или более ранняя версия</span><span class="sxs-lookup"><span data-stu-id="7874e-163">HTML 3.0 or earlier</span></span>                         | <span data-ttu-id="7874e-164">nlhtml.dll</span><span class="sxs-lookup"><span data-stu-id="7874e-164">nlhtml.dll</span></span>   |
| [<span data-ttu-id="7874e-165">Обработчик фильтра документов</span><span class="sxs-lookup"><span data-stu-id="7874e-165">Document Filter Handler</span></span>](#document-filter-handler)             | <span data-ttu-id="7874e-166">Microsoft Word, Excel, PowerPoint</span><span class="sxs-lookup"><span data-stu-id="7874e-166">Microsoft Word, Excel, PowerPoint</span></span>           | <span data-ttu-id="7874e-167">offfilt.dll</span><span class="sxs-lookup"><span data-stu-id="7874e-167">offfilt.dll</span></span>  |
| [<span data-ttu-id="7874e-168">Обработчик обычного текстового фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-168">Plain Text Filter Handler</span></span>](#plain-text-filter-handler)         | <span data-ttu-id="7874e-169">Обычные текстовые файлы — IFilter по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7874e-169">Plain text files - Default IFilter</span></span>          | <span data-ttu-id="7874e-170">query.dll</span><span class="sxs-lookup"><span data-stu-id="7874e-170">query.dll</span></span>    |
| [<span data-ttu-id="7874e-171">Обработчик бинарного или неопределенного фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-171">Binary or Null Filter Handler</span></span>](#binary-or-null-filter-handler) | <span data-ttu-id="7874e-172">Двоичные файлы-IFilter null</span><span class="sxs-lookup"><span data-stu-id="7874e-172">Binary files - Null IFilter</span></span>                 | <span data-ttu-id="7874e-173">query.dll</span><span class="sxs-lookup"><span data-stu-id="7874e-173">query.dll</span></span>    |

### <a name="mime-filter-handler"></a><span data-ttu-id="7874e-174">Обработчик фильтра MIME</span><span class="sxs-lookup"><span data-stu-id="7874e-174">MIME Filter Handler</span></span>

<span data-ttu-id="7874e-175">Обработчик фильтра MIME (в mimefilt.dll) извлекает текст и сведения о свойствах из файлов с расширениями. EML,. MHT и. MHTML.</span><span class="sxs-lookup"><span data-stu-id="7874e-175">The MIME filter handler (in mimefilt.dll) extracts text and property information from files with the extensions .eml, .mht and .mhtml.</span></span>

### <a name="html-filter-handler"></a><span data-ttu-id="7874e-176">Обработчик фильтра HTML</span><span class="sxs-lookup"><span data-stu-id="7874e-176">HTML Filter Handler</span></span>

<span data-ttu-id="7874e-177">Обработчик HTML-фильтра (в nlhtml.dll) извлекает из класса "хтмлфилес" текст и сведения о свойствах, чтобы их можно было индексировать с помощью поиска Windows.</span><span class="sxs-lookup"><span data-stu-id="7874e-177">The HTML filter handler (in nlhtml.dll) extracts text and property information from the class "htmlfiles" so that it can be indexed by Windows Search.</span></span> <span data-ttu-id="7874e-178">Описание связи между [**фильтрами IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и File см. в разделе "поиск DLL-библиотеки IFilter для файла" статьи [Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7874e-178">For a description of the association between [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) and file type, see "Finding the IFilter DLL for a File" in [Registering Filter Handlers](-search-ifilter-registering-filters.md).</span></span>

<span data-ttu-id="7874e-179">`META`Для передачи специальных запросов на обработку HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)можно использовать функцию тегов HTML-документов.</span><span class="sxs-lookup"><span data-stu-id="7874e-179">You can use the `META` tag feature of HTML documents to convey special handling requests to the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter).</span></span> <span data-ttu-id="7874e-180">`META` Теги находятся рядом с началом HTML-файла в `HEAD ... /HEAD` тегах, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7874e-180">`META` tags occur near the beginning of an html file within the `HEAD ... /HEAD` tags, as illustrated in the following example.</span></span>

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

<span data-ttu-id="7874e-181">Некоторые HTML- `META` теги автоматически сопоставляются с хорошо известными набором свойств и ЗНАЧЕНИЯМИ идентификатора свойства (PID), поэтому запросы к этим свойствам будут искать сопоставленное содержимое.</span><span class="sxs-lookup"><span data-stu-id="7874e-181">Some HTML `META` tags are automatically mapped to well known property set and property ID (property identifier (PID)) values so that queries on these properties will search the mapped contents.</span></span> <span data-ttu-id="7874e-182">Некоторые примеры перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7874e-182">Some examples are listed in the following table.</span></span> <span data-ttu-id="7874e-183">Список системных свойств, которые можно использовать для форматов файлов, см. в разделе [свойства, определяемые системой для пользовательских форматов файлов](-shell-systemdefinedpropertiesforfileformats.md).</span><span class="sxs-lookup"><span data-stu-id="7874e-183">For a list of system properties that you can use for your file formats, see [System-Defined Properties for Custom File Formats](-shell-systemdefinedpropertiesforfileformats.md).</span></span>

| <span data-ttu-id="7874e-184">Пример свойства</span><span class="sxs-lookup"><span data-stu-id="7874e-184">Property example</span></span>                              | <span data-ttu-id="7874e-185">Сопоставлено с</span><span class="sxs-lookup"><span data-stu-id="7874e-185">Mapped to</span></span>                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7874e-186">Meta Name = "author" Content = "Рут"</span><span class="sxs-lookup"><span data-stu-id="7874e-186">meta name="author" content="ruth"</span></span>             | <span data-ttu-id="7874e-187">Свойство Author в наборе свойств сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7874e-187">The author property in the Summary Information property set.</span></span>            |
| <span data-ttu-id="7874e-188">Meta Name = "subject" содержимое = "обработка текста"</span><span class="sxs-lookup"><span data-stu-id="7874e-188">meta name="subject" content="word processing"</span></span> | <span data-ttu-id="7874e-189">Свойство Subject в наборе свойств сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7874e-189">The subject property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="7874e-190">Meta Name = "Ключевые слова" Content = "шрифты, Serif"</span><span class="sxs-lookup"><span data-stu-id="7874e-190">meta name="keywords" content="fonts, serif"</span></span>   | <span data-ttu-id="7874e-191">Свойство keyword в наборе свойств сводных данных.</span><span class="sxs-lookup"><span data-stu-id="7874e-191">The keyword property in the Summary Information property set.</span></span>           |
| <span data-ttu-id="7874e-192">Meta Name = "MS. Category" содержимое = "вымышление"</span><span class="sxs-lookup"><span data-stu-id="7874e-192">meta name="ms.category" content="fiction"</span></span>     | <span data-ttu-id="7874e-193">Свойство Category в наборе свойств сведения о сводке документа.</span><span class="sxs-lookup"><span data-stu-id="7874e-193">The category property in the document Summary Information property set.</span></span> |

<span data-ttu-id="7874e-194">Некоторые функции [**интерфейса IFILTER**](/windows/win32/api/filter/nn-filter-ifilter) HTML перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7874e-194">Some features of the HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) are listed in the following table.</span></span>

[comment]: # (Эта таблица должна быть HTML, чтобы правильно форматировать образцы в нем)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7874e-196">Задача</span><span class="sxs-lookup"><span data-stu-id="7874e-196">Task</span></span></th>
<th><span data-ttu-id="7874e-197">Действие</span><span class="sxs-lookup"><span data-stu-id="7874e-197">Action</span></span></th>
<th><span data-ttu-id="7874e-198">Пример</span><span class="sxs-lookup"><span data-stu-id="7874e-198">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7874e-199">Создание специальных абстракций из файлов</span><span class="sxs-lookup"><span data-stu-id="7874e-199">Creating special abstracts from files</span></span></td>
<td><span data-ttu-id="7874e-200">Используйте <code>META NAME=&quot;DESCRIPTION&quot;...</code> тег, чтобы указать <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> использовать строку, следующую за ключевым словом, в <code>CONTENT</code> качестве абстрактного документа.</span><span class="sxs-lookup"><span data-stu-id="7874e-200">Use the <code>META NAME=&quot;DESCRIPTION&quot;...</code> tag to instruct the <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> to use the string following the <code>CONTENT</code> keyword as the document abstract.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7874e-201">Процесс фильтрации может формировать абстракции для каждого отфильтрованного файла, который по умолчанию является набором символов в начале файла.</span><span class="sxs-lookup"><span data-stu-id="7874e-201">The filtering process can generate abstracts for each filtered file, which default to being a set of characters at the beginning of the file.</span></span>
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="7874e-202">Предотвращение фильтрации отдельных файлов</span><span class="sxs-lookup"><span data-stu-id="7874e-202">Preventing individual files from being filtered</span></span></td>
<td><span data-ttu-id="7874e-203">Добавьте <code>meta name</code> тег в файл.</span><span class="sxs-lookup"><span data-stu-id="7874e-203">Add a <code>meta name</code> tag to the file.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7874e-204">Задание кода языка для файла (чтобы убедиться, что система выбирает правильные языковые разделители слов и файлы неучитываемых слов)</span><span class="sxs-lookup"><span data-stu-id="7874e-204">Setting the language code for a file (to ensure the system chooses the correct language word breakers and noise word files)</span></span></td>
<td><span data-ttu-id="7874e-205">Добавьте следующий <code>meta name</code> тег в файл, где поле Content указывает соответствующий код языка (в символах или с использованием значения языкового стандарта).</span><span class="sxs-lookup"><span data-stu-id="7874e-205">Add the following <code>meta name</code> tag to the file, where the content field specifies the appropriate language code (either in characters or by using the locale value).</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a><span data-ttu-id="7874e-206">Обработчик фильтра документов</span><span class="sxs-lookup"><span data-stu-id="7874e-206">Document Filter Handler</span></span>

<span data-ttu-id="7874e-207">Обработчик фильтра документов (в offilt.dll) Фильтрует файлы для некоторых расширений документов в Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="7874e-207">The Document filter handler (in offilt.dll) filters files for some extensions of documents in Microsoft Office.</span></span> <span data-ttu-id="7874e-208">К ним относятся файлы с расширениями DOC, MDB, PPT и xlt, например.</span><span class="sxs-lookup"><span data-stu-id="7874e-208">These include files with the extensions .doc, .mdb, .ppt, and .xlt, for example.</span></span>

### <a name="plain-text-filter-handler"></a><span data-ttu-id="7874e-209">Обработчик обычного текстового фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-209">Plain Text Filter Handler</span></span>

<span data-ttu-id="7874e-210">Для обычных текстовых файлов в Windows Search используется обработчик текстовых фильтров, который фильтрует как системные свойства (например, имена файлов), так и содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="7874e-210">For plain-text files, Windows Search uses the text filter handler, which filters both the system properties (such as file names) and the contents of a file.</span></span> <span data-ttu-id="7874e-211">Если у типа файлов нет связи [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) в реестре, Windows Search индексирует только свойства оболочки для этого файла.</span><span class="sxs-lookup"><span data-stu-id="7874e-211">When a file type does not have an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) association in the registry, Windows Search indexes only the Shell properties for the file.</span></span> <span data-ttu-id="7874e-212">Однако пользователь может использовать **Дополнительные параметры** на панели управления " **Параметры индексирования** " для **индексирования свойств** или **свойств индекса и содержимого файлов**.</span><span class="sxs-lookup"><span data-stu-id="7874e-212">However the user can use the **Advanced Options** in the **Indexing Options** control panel to **Index Properties** or **Index Properties and File Contents**.</span></span>

![снимок экрана, отображающий диалоговое окно "Дополнительные параметры"](images/ifilteradvancedoptions.png)

<span data-ttu-id="7874e-214">Если пользователь выбирает этот параметр для типа файла без связанного с ним [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), для извлечения содержимого файла используется обработчик текстового фильтра.</span><span class="sxs-lookup"><span data-stu-id="7874e-214">If the user chooses this option for a file type without an associated [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), the text filter handler is used to extract the content of the file.</span></span> <span data-ttu-id="7874e-215">Обработчик текстового фильтра не «понимает» формат документа; при фильтрации содержимого файла файл обрабатывается как последовательность символов.</span><span class="sxs-lookup"><span data-stu-id="7874e-215">The text filter handler does not "understand" any document format; when filtering the contents of a file, it treats the file as a sequence of characters.</span></span> <span data-ttu-id="7874e-216">Он проверяет метку порядка следования байтов Юникода в начале файла.</span><span class="sxs-lookup"><span data-stu-id="7874e-216">It does check for the Unicode byte-order mark at the beginning of the file.</span></span>

### <a name="binary-or-null-filter-handler"></a><span data-ttu-id="7874e-217">Обработчик бинарного или неопределенного фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-217">Binary or Null Filter Handler</span></span>

<span data-ttu-id="7874e-218">При обнаружении зарегистрированного двоичного файла используется обработчик фильтра null.</span><span class="sxs-lookup"><span data-stu-id="7874e-218">When a registered binary file is encountered, the null filter handler is used.</span></span> <span data-ttu-id="7874e-219">Обработчик фильтра null извлекает только системные свойства.</span><span class="sxs-lookup"><span data-stu-id="7874e-219">The null filter handler retrieves only the system properties.</span></span> <span data-ttu-id="7874e-220">Содержимое двоичного файла не фильтруется.</span><span class="sxs-lookup"><span data-stu-id="7874e-220">The contents of a binary file are not filtered.</span></span> <span data-ttu-id="7874e-221">Примерами системных свойств являются **filename**, **LastWriteTime**, **Размер файла** и **Attributes**.</span><span class="sxs-lookup"><span data-stu-id="7874e-221">Examples of system properties are **FileName**, **LastWriteTime**, **FileSize**, and **Attributes**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7874e-222">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="7874e-222">Additional Resources</span></span>

- <span data-ttu-id="7874e-223">Пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="7874e-223">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="7874e-224">Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7874e-224">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="7874e-225">Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="7874e-225">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="7874e-226">Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7874e-226">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7874e-227">См. также</span><span class="sxs-lookup"><span data-stu-id="7874e-227">Related topics</span></span>

[<span data-ttu-id="7874e-228">Разработка обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="7874e-228">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="7874e-229">О обработчиках фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-229">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="7874e-230">Рекомендации по созданию обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-230">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="7874e-231">Возвращение свойств из обработчика фильтра</span><span class="sxs-lookup"><span data-stu-id="7874e-231">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="7874e-232">Реализация обработчиков фильтров в поиске Windows</span><span class="sxs-lookup"><span data-stu-id="7874e-232">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="7874e-233">Регистрация обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="7874e-233">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)

[<span data-ttu-id="7874e-234">Тестирование обработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="7874e-234">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
