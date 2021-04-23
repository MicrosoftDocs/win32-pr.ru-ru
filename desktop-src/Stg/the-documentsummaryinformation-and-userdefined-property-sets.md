---
title: Свойства Документсуммаринформатион и Пользователяопределенные задают
description: Набор свойств Документсуммаринформатион и Пользователяопределенные является расширением набора свойств сводных данных. Оба набора свойств могут существовать одновременно.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- документсуммаринформатион
- Наборы свойств Пользователяопределенные
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532105"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a><span data-ttu-id="b5e81-106">Свойства Документсуммаринформатион и Пользователяопределенные задают</span><span class="sxs-lookup"><span data-stu-id="b5e81-106">The DocumentSummaryInformation and UserDefined Property Sets</span></span>

<span data-ttu-id="b5e81-107">Набор свойств **документсуммаринформатион** и **пользователяопределенные** является расширением [набора свойств сводных данных](the-summary-information-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="b5e81-107">A **DocumentSummaryInformation** and **UserDefined** property set is an extension to [the Summary Information property set](the-summary-information-property-set.md).</span></span> <span data-ttu-id="b5e81-108">Оба набора свойств могут существовать одновременно.</span><span class="sxs-lookup"><span data-stu-id="b5e81-108">Both property sets can exist simultaneously.</span></span>

<span data-ttu-id="b5e81-109">Имя потока, содержащего набор свойств **документсуммаринформатион** , — **" \\ 005DocumentSummaryInformation"**.</span><span class="sxs-lookup"><span data-stu-id="b5e81-109">The name of the stream that contains the **DocumentSummaryInformation** property set is **"\\005DocumentSummaryInformation"**.</span></span> <span data-ttu-id="b5e81-110">Идентификатор формата (FMTID) для набора свойств **документсуммаринформатион** — **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="b5e81-110">The format identifier (FMTID) for the **DocumentSummaryInformation** property set is **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="b5e81-111">Объявление этого значения доступно в указанных файлах заголовков как **FMTID \_ доксуммаринформатион**.</span><span class="sxs-lookup"><span data-stu-id="b5e81-111">The declaration for this value is available in the provided header files as **FMTID\_DocSummaryInformation**.</span></span> <span data-ttu-id="b5e81-112">Дополнительные сведения см. [в разделе имена в IStorage](names-in-istorage.md), [набор свойств сводных данных, свойства](the-summary-information-property-set.md) [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) и [Format](format-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b5e81-112">For more information, see [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).</span></span>

<span data-ttu-id="b5e81-113">В этом потоке также имеется отдельный раздел для пользовательских свойств, определяемых пользователем, как в наборах свойств **документсуммаринформатион** и **пользователяопределенные** .</span><span class="sxs-lookup"><span data-stu-id="b5e81-113">This stream also has a separate section for the custom-user-defined properties as in the **DocumentSummaryInformation** and **UserDefined** property sets.</span></span> <span data-ttu-id="b5e81-114">Этот раздел отображается в интерфейсе [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) как отдельный набор свойств со следующим FMTID (доступен как **FMTID \_ усердефинедпропертиес**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span><span class="sxs-lookup"><span data-stu-id="b5e81-114">This section appears in the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interface as a separate property set, with the following FMTID (available as **FMTID\_UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.</span></span>

<span data-ttu-id="b5e81-115">Эти два набора свойств являются единственными, для которых один поток может содержать несколько наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="b5e81-115">These two property sets are the only ones for which a single stream can hold multiple property sets.</span></span> <span data-ttu-id="b5e81-116">Тот факт, что эти два набора свойств находятся в одном потоке, влияет на поведение интерфейса **IPropertySetStorage** .</span><span class="sxs-lookup"><span data-stu-id="b5e81-116">The fact that these two property sets are in a single stream affects the behavior of the **IPropertySetStorage** interface.</span></span> <span data-ttu-id="b5e81-117">Дополнительные сведения см. в разделе [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span><span class="sxs-lookup"><span data-stu-id="b5e81-117">For more information, see [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).</span></span>

<span data-ttu-id="b5e81-118">В следующей таблице перечислены добавленные свойства для набора свойств **документсуммаринформатион** и **пользователяопределенные** .</span><span class="sxs-lookup"><span data-stu-id="b5e81-118">The following table lists the added properties to the **DocumentSummaryInformation** and **UserDefined** property set.</span></span> <span data-ttu-id="b5e81-119">Как и в задании свойства **SummaryInformation** , имена обычно не сохраняются в наборе свойств, но выводятся из идентификатора свойства.</span><span class="sxs-lookup"><span data-stu-id="b5e81-119">As in the **SummaryInformation** property set, the names are not typically stored in the property set, but are inferred from the property identifier.</span></span>



| <span data-ttu-id="b5e81-120">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="b5e81-120">Property name</span></span>      | <span data-ttu-id="b5e81-121">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="b5e81-121">Property identifier</span></span>     | <span data-ttu-id="b5e81-122">Значение идентификатора свойства</span><span class="sxs-lookup"><span data-stu-id="b5e81-122">Property identifier value</span></span> | <span data-ttu-id="b5e81-123">Тип варианта</span><span class="sxs-lookup"><span data-stu-id="b5e81-123">VARIANT type</span></span>                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| <span data-ttu-id="b5e81-124">Категория</span><span class="sxs-lookup"><span data-stu-id="b5e81-124">Category</span></span>           | <span data-ttu-id="b5e81-125">**\_Категория пиддси**</span><span class="sxs-lookup"><span data-stu-id="b5e81-125">**PIDDSI\_CATEGORY**</span></span>    | <span data-ttu-id="b5e81-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="b5e81-126">0x00000002</span></span>                | <span data-ttu-id="b5e81-127">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="b5e81-127">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="b5e81-128">пресентатионтаржет</span><span class="sxs-lookup"><span data-stu-id="b5e81-128">PresentationTarget</span></span> | <span data-ttu-id="b5e81-129">**ПИДДСИ \_ пресформат**</span><span class="sxs-lookup"><span data-stu-id="b5e81-129">**PIDDSI\_PRESFORMAT**</span></span>  | <span data-ttu-id="b5e81-130">0x00000003</span><span class="sxs-lookup"><span data-stu-id="b5e81-130">0x00000003</span></span>                | <span data-ttu-id="b5e81-131">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="b5e81-131">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="b5e81-132">Байты</span><span class="sxs-lookup"><span data-stu-id="b5e81-132">Bytes</span></span>              | <span data-ttu-id="b5e81-133">**ПИДДСИ \_ BYTECOUNT**</span><span class="sxs-lookup"><span data-stu-id="b5e81-133">**PIDDSI\_BYTECOUNT**</span></span>   | <span data-ttu-id="b5e81-134">0x00000004</span><span class="sxs-lookup"><span data-stu-id="b5e81-134">0x00000004</span></span>                | <span data-ttu-id="b5e81-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-135">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-136">Линии</span><span class="sxs-lookup"><span data-stu-id="b5e81-136">Lines</span></span>              | <span data-ttu-id="b5e81-137">**ПИДДСИ \_ линекаунт**</span><span class="sxs-lookup"><span data-stu-id="b5e81-137">**PIDDSI\_LINECOUNT**</span></span>   | <span data-ttu-id="b5e81-138">0x00000005</span><span class="sxs-lookup"><span data-stu-id="b5e81-138">0x00000005</span></span>                | <span data-ttu-id="b5e81-139">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-139">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-140">Абзацы</span><span class="sxs-lookup"><span data-stu-id="b5e81-140">Paragraphs</span></span>         | <span data-ttu-id="b5e81-141">**ПИДДСИ \_ паркаунт**</span><span class="sxs-lookup"><span data-stu-id="b5e81-141">**PIDDSI\_PARCOUNT**</span></span>    | <span data-ttu-id="b5e81-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="b5e81-142">0x00000006</span></span>                | <span data-ttu-id="b5e81-143">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-143">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-144">Слайды</span><span class="sxs-lookup"><span data-stu-id="b5e81-144">Slides</span></span>             | <span data-ttu-id="b5e81-145">**ПИДДСИ \_ слидекаунт**</span><span class="sxs-lookup"><span data-stu-id="b5e81-145">**PIDDSI\_SLIDECOUNT**</span></span>  | <span data-ttu-id="b5e81-146">0x00000007</span><span class="sxs-lookup"><span data-stu-id="b5e81-146">0x00000007</span></span>                | <span data-ttu-id="b5e81-147">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-147">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-148">Примечания</span><span class="sxs-lookup"><span data-stu-id="b5e81-148">Notes</span></span>              | <span data-ttu-id="b5e81-149">**ПИДДСИ \_ нотекаунт**</span><span class="sxs-lookup"><span data-stu-id="b5e81-149">**PIDDSI\_NOTECOUNT**</span></span>   | <span data-ttu-id="b5e81-150">0x00000008</span><span class="sxs-lookup"><span data-stu-id="b5e81-150">0x00000008</span></span>                | <span data-ttu-id="b5e81-151">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-151">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-152">хидденслидес</span><span class="sxs-lookup"><span data-stu-id="b5e81-152">HiddenSlides</span></span>       | <span data-ttu-id="b5e81-153">**ПИДДСИ \_ хидденкаунт**</span><span class="sxs-lookup"><span data-stu-id="b5e81-153">**PIDDSI\_HIDDENCOUNT**</span></span> | <span data-ttu-id="b5e81-154">0x00000009</span><span class="sxs-lookup"><span data-stu-id="b5e81-154">0x00000009</span></span>                | <span data-ttu-id="b5e81-155">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-155">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-156">ммклипс</span><span class="sxs-lookup"><span data-stu-id="b5e81-156">MMClips</span></span>            | <span data-ttu-id="b5e81-157">**ПИДДСИ \_ ммклипкаунт**</span><span class="sxs-lookup"><span data-stu-id="b5e81-157">**PIDDSI\_MMCLIPCOUNT**</span></span> | <span data-ttu-id="b5e81-158">0x0000000A</span><span class="sxs-lookup"><span data-stu-id="b5e81-158">0x0000000A</span></span>                | <span data-ttu-id="b5e81-159">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="b5e81-159">**VT\_I4**</span></span>                        |
| <span data-ttu-id="b5e81-160">скалекроп</span><span class="sxs-lookup"><span data-stu-id="b5e81-160">ScaleCrop</span></span>          | <span data-ttu-id="b5e81-161">**\_масштабирование пиддси**</span><span class="sxs-lookup"><span data-stu-id="b5e81-161">**PIDDSI\_SCALE**</span></span>       | <span data-ttu-id="b5e81-162">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="b5e81-162">0x0000000B</span></span>                | <span data-ttu-id="b5e81-163">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="b5e81-163">**VT\_BOOL**</span></span>                      |
| <span data-ttu-id="b5e81-164">хеадингпаирс</span><span class="sxs-lookup"><span data-stu-id="b5e81-164">HeadingPairs</span></span>       | <span data-ttu-id="b5e81-165">**ПИДДСИ \_ хеадингпаир**</span><span class="sxs-lookup"><span data-stu-id="b5e81-165">**PIDDSI\_HEADINGPAIR**</span></span> | <span data-ttu-id="b5e81-166">0x0000000C</span><span class="sxs-lookup"><span data-stu-id="b5e81-166">0x0000000C</span></span>                | <span data-ttu-id="b5e81-167">**VT \_ вариант** \| **\_ вектора VT**</span><span class="sxs-lookup"><span data-stu-id="b5e81-167">**VT\_VARIANT** \| **VT\_VECTOR**</span></span> |
| <span data-ttu-id="b5e81-168">титлесофпартс</span><span class="sxs-lookup"><span data-stu-id="b5e81-168">TitlesofParts</span></span>      | <span data-ttu-id="b5e81-169">**ПИДДСИ \_ докпартс**</span><span class="sxs-lookup"><span data-stu-id="b5e81-169">**PIDDSI\_DOCPARTS**</span></span>    | <span data-ttu-id="b5e81-170">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="b5e81-170">0x0000000D</span></span>                | <span data-ttu-id="b5e81-171">**VT \_ вектор** \| **VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="b5e81-171">**VT\_VECTOR** \| **VT\_LPSTR**</span></span>   |
| <span data-ttu-id="b5e81-172">Manager</span><span class="sxs-lookup"><span data-stu-id="b5e81-172">Manager</span></span>            | <span data-ttu-id="b5e81-173">**ПИДДСИ \_ Manager**</span><span class="sxs-lookup"><span data-stu-id="b5e81-173">**PIDDSI\_MANAGER**</span></span>     | <span data-ttu-id="b5e81-174">0x0000000E</span><span class="sxs-lookup"><span data-stu-id="b5e81-174">0x0000000E</span></span>                | <span data-ttu-id="b5e81-175">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="b5e81-175">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="b5e81-176">Company</span><span class="sxs-lookup"><span data-stu-id="b5e81-176">Company</span></span>            | <span data-ttu-id="b5e81-177">**\_компания пиддси**</span><span class="sxs-lookup"><span data-stu-id="b5e81-177">**PIDDSI\_COMPANY**</span></span>     | <span data-ttu-id="b5e81-178">0x0000000F</span><span class="sxs-lookup"><span data-stu-id="b5e81-178">0x0000000F</span></span>                | <span data-ttu-id="b5e81-179">**VT \_ LPSTR**</span><span class="sxs-lookup"><span data-stu-id="b5e81-179">**VT\_LPSTR**</span></span>                     |
| <span data-ttu-id="b5e81-180">линксуптодате</span><span class="sxs-lookup"><span data-stu-id="b5e81-180">LinksUpToDate</span></span>      | <span data-ttu-id="b5e81-181">**ПИДДСИ \_ линксдирти**</span><span class="sxs-lookup"><span data-stu-id="b5e81-181">**PIDDSI\_LINKSDIRTY**</span></span>  | <span data-ttu-id="b5e81-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="b5e81-182">0x00000010</span></span>                | <span data-ttu-id="b5e81-183">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="b5e81-183">**VT\_BOOL**</span></span>                      |



 

<span data-ttu-id="b5e81-184">Эти свойства имеют следующие варианты использования.</span><span class="sxs-lookup"><span data-stu-id="b5e81-184">These properties have the following uses:</span></span>

<dl> <dt>

<span data-ttu-id="b5e81-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Категори</span><span class="sxs-lookup"><span data-stu-id="b5e81-185"><span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Category</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-186">Текстовая строка, введенная пользователем и указывающая категорию, к которой принадлежит файл (МЕМО, предложение и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b5e81-186">A text string typed by the user that indicates what category the file belongs to (memo, proposal, and so on).</span></span> <span data-ttu-id="b5e81-187">Он удобен для поиска файлов одного типа.</span><span class="sxs-lookup"><span data-stu-id="b5e81-187">It is useful for finding files of same type.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>пресентатионтаржет</span><span class="sxs-lookup"><span data-stu-id="b5e81-188"><span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-189">Целевой формат представления (35mm, принтер, видео и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b5e81-189">Target format for presentation (35mm, printer, video, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Байт</span><span class="sxs-lookup"><span data-stu-id="b5e81-190"><span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-191">Число байтов.</span><span class="sxs-lookup"><span data-stu-id="b5e81-191">Number of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Строки</span><span class="sxs-lookup"><span data-stu-id="b5e81-192"><span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Lines</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-193">Число строк.</span><span class="sxs-lookup"><span data-stu-id="b5e81-193">Number of lines.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Абзацев</span><span class="sxs-lookup"><span data-stu-id="b5e81-194"><span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Paragraphs</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-195">Число абзацев.</span><span class="sxs-lookup"><span data-stu-id="b5e81-195">Number of paragraphs.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Слайды</span><span class="sxs-lookup"><span data-stu-id="b5e81-196"><span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-197">Число слайдов.</span><span class="sxs-lookup"><span data-stu-id="b5e81-197">Number of slides.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Заметки о</span><span class="sxs-lookup"><span data-stu-id="b5e81-198"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notes</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-199">Число страниц, содержащих примечания.</span><span class="sxs-lookup"><span data-stu-id="b5e81-199">Number of pages that contain notes.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>хидденслидес</span><span class="sxs-lookup"><span data-stu-id="b5e81-200"><span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-201">Число скрытых слайдов.</span><span class="sxs-lookup"><span data-stu-id="b5e81-201">Number of slides that are hidden.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>ммклипс</span><span class="sxs-lookup"><span data-stu-id="b5e81-202"><span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-203">Число звуковых или видеоклипов.</span><span class="sxs-lookup"><span data-stu-id="b5e81-203">Number of sound or video clips.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>скалекроп</span><span class="sxs-lookup"><span data-stu-id="b5e81-204"><span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-205">Задайте значение true (-1) при необходимости масштабирования эскиза.</span><span class="sxs-lookup"><span data-stu-id="b5e81-205">Set to True (-1) when scaling of the thumbnail is desired.</span></span> <span data-ttu-id="b5e81-206">Если значение не задано, обрезка не требуется.</span><span class="sxs-lookup"><span data-stu-id="b5e81-206">If not set, cropping is desired.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>хеадингпаирс</span><span class="sxs-lookup"><span data-stu-id="b5e81-207"><span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-208">Внутренне используемое свойство, указывающее группировку различных частей документа и количество элементов в каждой группе.</span><span class="sxs-lookup"><span data-stu-id="b5e81-208">Internally used property indicating the grouping of different document parts and the number of items in each group.</span></span> <span data-ttu-id="b5e81-209">Заголовки частей документа хранятся в свойстве **титлесофпартс** .</span><span class="sxs-lookup"><span data-stu-id="b5e81-209">The titles of the document parts are stored in the **TitlesofParts** property.</span></span> <span data-ttu-id="b5e81-210">Свойство **хеадингпаирс** хранится в виде вектора Variant в повторяющихся парах значений **VT \_ LPSTR** (или **VT \_ LPWSTR**) и **VT \_ I4** .</span><span class="sxs-lookup"><span data-stu-id="b5e81-210">The **HeadingPairs** property is stored as a vector of variants, in repeating pairs of **VT\_LPSTR** (or **VT\_LPWSTR**) and **VT\_I4** values.</span></span> <span data-ttu-id="b5e81-211">Значение **VT \_ LPSTR** представляет имя заголовка, а значение **VT \_ I4** указывает количество частей документа под этим заголовком.</span><span class="sxs-lookup"><span data-stu-id="b5e81-211">The **VT\_LPSTR** value represents a heading name, and the **VT\_I4** value indicates the count of document parts under that heading.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>титлесофпартс</span><span class="sxs-lookup"><span data-stu-id="b5e81-212"><span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-213">Имена частей документа.</span><span class="sxs-lookup"><span data-stu-id="b5e81-213">Names of document parts.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Configuration</span><span class="sxs-lookup"><span data-stu-id="b5e81-214"><span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-215">Руководитель проекта.</span><span class="sxs-lookup"><span data-stu-id="b5e81-215">Manager of the project.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Во</span><span class="sxs-lookup"><span data-stu-id="b5e81-216"><span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Company</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-217">Название компании.</span><span class="sxs-lookup"><span data-stu-id="b5e81-217">Company name.</span></span>

</dd> <dt>

<span data-ttu-id="b5e81-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>линксуптодате</span><span class="sxs-lookup"><span data-stu-id="b5e81-218"><span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate</span></span>
</dt> <dd>

<span data-ttu-id="b5e81-219">Логическое значение, указывающее, страдает ли пользовательская связь от чрезмерного шума для всех приложений.</span><span class="sxs-lookup"><span data-stu-id="b5e81-219">Boolean value to indicate whether the custom links are hampered by excessive noise, for all applications.</span></span>

> [!Note]  
> <span data-ttu-id="b5e81-220">Как описано в 12,3.</span><span class="sxs-lookup"><span data-stu-id="b5e81-220">As described in 12.3.</span></span> <span data-ttu-id="b5e81-221">Сериализованный формат для наборов свойств спецификации OLE 2,0, элементы Vector в свойствах **хеадингпаирс** и **титлесофпартс** должны быть согласованы по 32 разрядности в пределах набора свойств.</span><span class="sxs-lookup"><span data-stu-id="b5e81-221">Serialized Format for Property Sets of the OLE 2.0 Design Specification, vector elements in the **HeadingPairs** and **TitlesofParts** properties should be aligned on 32 bit boundaries within the property set.</span></span> <span data-ttu-id="b5e81-222">Однако в наборах свойств **документсуммаринформатион** и **пользователяопределенные** , если кодовая страница набора свойств не является Юникодом, эти элементы должны быть упакованы.</span><span class="sxs-lookup"><span data-stu-id="b5e81-222">However, in the **DocumentSummaryInformation** and **UserDefined** property sets, when the code page of the property set is not Unicode, these elements must be packed.</span></span>

 

</dd> </dl>

<span data-ttu-id="b5e81-223">Набор свойств **пользователяопределенные** можно использовать для хранения любых свойств.</span><span class="sxs-lookup"><span data-stu-id="b5e81-223">The **UserDefined** property set can be used to hold any properties.</span></span> <span data-ttu-id="b5e81-224">Как правило, он используется для хранения именованных свойств, созданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="b5e81-224">Typically, it is used to store named properties created by a user.</span></span>

 

 




