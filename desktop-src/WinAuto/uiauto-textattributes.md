---
title: Атрибуты текста модели автоматизации пользовательского интерфейса
description: В этом разделе описывается, как Microsoft UI Automation предоставляет свойства форматирования и стиля текстового содержимого, а также предоставляет список поддерживаемых текстовых атрибутов.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Модель автоматизации пользовательского интерфейса, атрибуты текста
- атрибуты текста, сведения
- атрибуты текста, типы Variant
- атрибуты текста, типы данных
- Модель автоматизации пользовательского интерфейса, список атрибутов
- Модель автоматизации пользовательского интерфейса, список атрибутов текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353627"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="0a397-109">Атрибуты текста модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0a397-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="0a397-110">В этом разделе описывается, как Microsoft UI Automation предоставляет свойства форматирования и стиля *текстового содержимого*, а также предоставляет список поддерживаемых текстовых атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0a397-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="0a397-111">Поставщики автоматизации пользовательского интерфейса предоставляют текстовые атрибуты с помощью методов [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) и [**финдаттрибуте**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) шаблона элемента управления [TextRange](uiauto-about-text-and-textrange-patterns.md) .</span><span class="sxs-lookup"><span data-stu-id="0a397-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="0a397-112">Клиентские приложения используют метод [**иуиаутоматионтекстранже:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) для получения значения определенного текстового атрибута для текстового диапазона.</span><span class="sxs-lookup"><span data-stu-id="0a397-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="0a397-113">Клиенты могут использовать метод [**иуиаутоматионтекстранже:: финдаттрибуте**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) для поиска текста с определенным атрибутом в текстовом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="0a397-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="0a397-114">Если найден любой совпадающий текст, метод создает новый текстовый диапазон, содержащий соответствующий текст.</span><span class="sxs-lookup"><span data-stu-id="0a397-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="0a397-115">Атрибуты текста в следующем списке поддерживаются шаблоном элемента управления **TextRange** .</span><span class="sxs-lookup"><span data-stu-id="0a397-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="0a397-116">Имена атрибутов являются производными от идентификаторов текстовых атрибутов модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0a397-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="0a397-117">Например, атрибут **аниматионстиле** идентифицируется клиентами как [**UIA \_ Аниматионстилеаттрибутеид**](uiauto-textattribute-ids.md) (определенный в UIAutomationClient. h) и поставщиками как **текст, \_ аниматионстиле \_ \_ GUID атрибута** (определенный в уиаутоматионкореапи. h).</span><span class="sxs-lookup"><span data-stu-id="0a397-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="0a397-118">Дополнительные сведения о каждом поддерживаемом текстовом атрибуте см. в разделе [**идентификаторы текстовых атрибутов**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="0a397-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a397-119">Некоторые из перечисленных атрибутов поддерживаются начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0a397-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="0a397-120">Дополнительные сведения о поддержке версий см. в разделе [**идентификаторы текстовых атрибутов**](uiauto-textattribute-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="0a397-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="0a397-121">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0a397-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0a397-122">Атрибуты примечаний</span><span class="sxs-lookup"><span data-stu-id="0a397-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="0a397-123">Атрибуты шрифтов</span><span class="sxs-lookup"><span data-stu-id="0a397-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="0a397-124">Атрибуты языка</span><span class="sxs-lookup"><span data-stu-id="0a397-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="0a397-125">Атрибут ссылки</span><span class="sxs-lookup"><span data-stu-id="0a397-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="0a397-126">Атрибуты полей страницы</span><span class="sxs-lookup"><span data-stu-id="0a397-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="0a397-127">Атрибуты выравнивания текста</span><span class="sxs-lookup"><span data-stu-id="0a397-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="0a397-128">Атрибуты цвета текста</span><span class="sxs-lookup"><span data-stu-id="0a397-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="0a397-129">Атрибуты оформления текста</span><span class="sxs-lookup"><span data-stu-id="0a397-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="0a397-130">Атрибуты стиля текста</span><span class="sxs-lookup"><span data-stu-id="0a397-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="0a397-131">Атрибуты взаимодействия и выбора</span><span class="sxs-lookup"><span data-stu-id="0a397-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="0a397-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0a397-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="0a397-133">Атрибуты примечаний</span><span class="sxs-lookup"><span data-stu-id="0a397-133">Annotation Attributes</span></span>

<span data-ttu-id="0a397-134">Объекты аннотации и типы заметок доступны через следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0a397-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="0a397-135">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-135">Attribute</span></span>             | <span data-ttu-id="0a397-136">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0a397-137">**аннотатионобжектс**</span><span class="sxs-lookup"><span data-stu-id="0a397-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="0a397-138">**UIA \_ аннотатионобжектсаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-annotation-type-identifiers.md) |
| <span data-ttu-id="0a397-139">**аннотатионтипес**</span><span class="sxs-lookup"><span data-stu-id="0a397-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="0a397-140">**UIA \_ аннотатионтипесаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="0a397-141">Атрибуты шрифтов</span><span class="sxs-lookup"><span data-stu-id="0a397-141">Font Attributes</span></span>

<span data-ttu-id="0a397-142">Имя, размер и плотность шрифта доступны через следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0a397-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="0a397-143">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-143">Attribute</span></span>      | <span data-ttu-id="0a397-144">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="0a397-145">**FontName**</span></span>   | [<span data-ttu-id="0a397-146">**UIA \_ фонтнамеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="0a397-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="0a397-147">**FontSize**</span></span>   | [<span data-ttu-id="0a397-148">**UIA \_ фонтсизеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="0a397-149">**FontWeight**</span><span class="sxs-lookup"><span data-stu-id="0a397-149">**FontWeight**</span></span> | [<span data-ttu-id="0a397-150">**UIA \_ фонтвеигхтаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="0a397-151">Атрибуты языка</span><span class="sxs-lookup"><span data-stu-id="0a397-151">Language Attributes</span></span>

<span data-ttu-id="0a397-152">Сведения о языке текста доступны через следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0a397-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="0a397-153">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-153">Attribute</span></span>              | <span data-ttu-id="0a397-154">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-155">**Язык и региональные параметры**</span><span class="sxs-lookup"><span data-stu-id="0a397-155">**Culture**</span></span>            | [<span data-ttu-id="0a397-156">**UIA \_ културеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="0a397-157">**текстфловдиректионс**</span><span class="sxs-lookup"><span data-stu-id="0a397-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="0a397-158">**UIA \_ текстфловдиректионсаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="0a397-159">Атрибут ссылки</span><span class="sxs-lookup"><span data-stu-id="0a397-159">Link Attribute</span></span>

<span data-ttu-id="0a397-160">Следующий атрибут предоставляет текстовый диапазон, который является целевым объектом ссылки в документе.</span><span class="sxs-lookup"><span data-stu-id="0a397-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="0a397-161">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-161">Attribute</span></span> | <span data-ttu-id="0a397-162">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-163">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="0a397-163">**Link**</span></span>  | [<span data-ttu-id="0a397-164">**UIA \_ линкаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="0a397-165">Атрибуты полей страницы</span><span class="sxs-lookup"><span data-stu-id="0a397-165">Page Margin Attributes</span></span>

<span data-ttu-id="0a397-166">Ограничивающие прямоугольники текстового диапазона не предоставляют координаты текста на странице.</span><span class="sxs-lookup"><span data-stu-id="0a397-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="0a397-167">Однако поставщик может предоставить сведения о полях страницы, используя следующие текстовые атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0a397-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="0a397-168">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-168">Attribute</span></span>          | <span data-ttu-id="0a397-169">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="0a397-170">**MarginBottom**</span></span>   | [<span data-ttu-id="0a397-171">**UIA \_ маргинботтоматтрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="0a397-172">**маргинлеадинг**</span><span class="sxs-lookup"><span data-stu-id="0a397-172">**MarginLeading**</span></span>  | [<span data-ttu-id="0a397-173">**UIA \_ маргинлеадингаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="0a397-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="0a397-174">**MarginTop**</span></span>      | [<span data-ttu-id="0a397-175">**UIA \_ маргинтопаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-176">**маргинтраилинг**</span><span class="sxs-lookup"><span data-stu-id="0a397-176">**MarginTrailing**</span></span> | [<span data-ttu-id="0a397-177">**UIA \_ маргинтраилингаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="0a397-178">Атрибуты выравнивания текста</span><span class="sxs-lookup"><span data-stu-id="0a397-178">Text Alignment Attributes</span></span>

<span data-ttu-id="0a397-179">Сведения о выравнивании текста, такие как отступы, параметры табуляции и выравнивание по горизонтали, доступны через следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0a397-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="0a397-180">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-180">Attribute</span></span>                   | <span data-ttu-id="0a397-181">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-182">**хоризонталтексталигнмент**</span><span class="sxs-lookup"><span data-stu-id="0a397-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="0a397-183">**UIA \_ хоризонталтексталигнментаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0a397-184">**индентатионфирстлине**</span><span class="sxs-lookup"><span data-stu-id="0a397-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="0a397-185">**UIA \_ индентатионфирстлинеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="0a397-186">**индентатионлеадинг**</span><span class="sxs-lookup"><span data-stu-id="0a397-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="0a397-187">**UIA \_ индентатионлеадингаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-188">**индентатионтраилинг**</span><span class="sxs-lookup"><span data-stu-id="0a397-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="0a397-189">**UIA \_ индентатионтраилингаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="0a397-190">**Вкладки**</span><span class="sxs-lookup"><span data-stu-id="0a397-190">**Tabs**</span></span>                    | [<span data-ttu-id="0a397-191">**UIA \_ табсаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="0a397-192">Атрибуты цвета текста</span><span class="sxs-lookup"><span data-stu-id="0a397-192">Text Color Attributes</span></span>

<span data-ttu-id="0a397-193">Цвета переднего плана и текста фона доступны в следующих текстовых атрибутах.</span><span class="sxs-lookup"><span data-stu-id="0a397-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="0a397-194">Оба цвета указываются как тип данных [**COLORREF**](/windows/desktop/gdi/colorref) .</span><span class="sxs-lookup"><span data-stu-id="0a397-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="0a397-195">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-195">Attribute</span></span>           | <span data-ttu-id="0a397-196">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="0a397-197">**BackgroundColor**</span></span> | [<span data-ttu-id="0a397-198">**UIA \_ баккграундколораттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0a397-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="0a397-199">**ForegroundColor**</span></span> | [<span data-ttu-id="0a397-200">**UIA \_ фореграундколораттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="0a397-201">Атрибуты оформления текста</span><span class="sxs-lookup"><span data-stu-id="0a397-201">Text Decoration Attributes</span></span>

<span data-ttu-id="0a397-202">Оформление текста включает такие области, как маркеры, подчеркивание и анимация.</span><span class="sxs-lookup"><span data-stu-id="0a397-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="0a397-203">Если текст содержит начальные маркеры или числа, то символ или текст, используемый для маркера или номера, должен быть включен в текстовый поток, если применимо.</span><span class="sxs-lookup"><span data-stu-id="0a397-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="0a397-204">Сведения о украшениях текста доступны через следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0a397-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="0a397-205">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-205">Attribute</span></span>              | <span data-ttu-id="0a397-206">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-207">**аниматионстиле**</span><span class="sxs-lookup"><span data-stu-id="0a397-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="0a397-208">**UIA \_ аниматионстилеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="0a397-209">**буллетстиле**</span><span class="sxs-lookup"><span data-stu-id="0a397-209">**BulletStyle**</span></span>        | [<span data-ttu-id="0a397-210">**UIA \_ буллетстилеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="0a397-211">**аутлинестилес**</span><span class="sxs-lookup"><span data-stu-id="0a397-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="0a397-212">**UIA \_ аутлинестилесаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-213">**оверлинеколор**</span><span class="sxs-lookup"><span data-stu-id="0a397-213">**OverlineColor**</span></span>      | [<span data-ttu-id="0a397-214">**UIA \_ оверлинеколораттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-215">**оверлинестиле**</span><span class="sxs-lookup"><span data-stu-id="0a397-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="0a397-216">**UIA \_ оверлинестилеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-217">**стрикесраугхколор**</span><span class="sxs-lookup"><span data-stu-id="0a397-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="0a397-218">**UIA \_ стрикесраугхколораттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0a397-219">**стрикесраугхстиле**</span><span class="sxs-lookup"><span data-stu-id="0a397-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="0a397-220">**UIA \_ стрикесраугхстилеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0a397-221">**ундерлинеколор**</span><span class="sxs-lookup"><span data-stu-id="0a397-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="0a397-222">**UIA \_ ундерлинеколораттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="0a397-223">**ундерлинестиле**</span><span class="sxs-lookup"><span data-stu-id="0a397-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="0a397-224">**UIA \_ ундерлинестилеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="0a397-225">Атрибуты стиля текста</span><span class="sxs-lookup"><span data-stu-id="0a397-225">Text Style Attributes</span></span>

<span data-ttu-id="0a397-226">Сведения о стилях текста доступны при наличии следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0a397-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="0a397-227">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-227">Attribute</span></span>         | <span data-ttu-id="0a397-228">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-229">**капстиле**</span><span class="sxs-lookup"><span data-stu-id="0a397-229">**CapStyle**</span></span>      | [<span data-ttu-id="0a397-230">**UIA \_ капстилеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="0a397-231">**IsHidden**</span></span>      | [<span data-ttu-id="0a397-232">**UIA \_ ишидденаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-233">**Курсив**</span><span class="sxs-lookup"><span data-stu-id="0a397-233">**IsItalic**</span></span>      | [<span data-ttu-id="0a397-234">**UIA \_ иситаликаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="0a397-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="0a397-236">**UIA \_ исреадонляттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="0a397-237">**иссуперскрипт**</span><span class="sxs-lookup"><span data-stu-id="0a397-237">**IsSuperscript**</span></span> | [<span data-ttu-id="0a397-238">**UIA \_ иссуперскриптаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0a397-239">**иссубскрипт**</span><span class="sxs-lookup"><span data-stu-id="0a397-239">**IsSubscript**</span></span>   | [<span data-ttu-id="0a397-240">**UIA \_ иссубскриптаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="0a397-241">Атрибуты взаимодействия и выбора</span><span class="sxs-lookup"><span data-stu-id="0a397-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="0a397-242">Сведения о текущем выделении текста в диапазоне и состоянии фокуса доступны при наличии следующих атрибутов.</span><span class="sxs-lookup"><span data-stu-id="0a397-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="0a397-243">attribute</span><span class="sxs-lookup"><span data-stu-id="0a397-243">Attribute</span></span>              | <span data-ttu-id="0a397-244">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="0a397-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a397-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="0a397-245">**IsActive**</span></span>           | [<span data-ttu-id="0a397-246">**UIA \_ исактивеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="0a397-247">**селектионактивинд**</span><span class="sxs-lookup"><span data-stu-id="0a397-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="0a397-248">**UIA \_ селектионактивиндаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="0a397-249">**каретпоситион**</span><span class="sxs-lookup"><span data-stu-id="0a397-249">**CaretPosition**</span></span>      | [<span data-ttu-id="0a397-250">**UIA \_ каретпоситионаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="0a397-251">**каретбидимоде**</span><span class="sxs-lookup"><span data-stu-id="0a397-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="0a397-252">**UIA \_ каретбидимодеаттрибутеид**</span><span class="sxs-lookup"><span data-stu-id="0a397-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="0a397-253">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0a397-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0a397-254">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0a397-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0a397-255">Сведения о шаблонах элементов автоматизации пользовательского интерфейса Text и TextRange</span><span class="sxs-lookup"><span data-stu-id="0a397-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="0a397-256">Шаблоны элементов управления Text и TextRange</span><span class="sxs-lookup"><span data-stu-id="0a397-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="0a397-257">Работа с элементами управления на основе текста</span><span class="sxs-lookup"><span data-stu-id="0a397-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 