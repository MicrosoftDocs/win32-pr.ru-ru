---
title: Тип элемента управления документом
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления документом.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления Document
- Модель автоматизации пользовательского интерфейса, тип элемента управления документом
- Модель автоматизации пользовательского интерфейса, древовидная структура для типа элемента управления Document
- Модель автоматизации пользовательского интерфейса, свойства для типа элемента управления Document
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления Document
- Модель автоматизации пользовательского интерфейса, события для типа элемента управления документом
- Древовидные структуры, тип элемента управления документом
- свойства, тип элемента управления Document
- шаблоны элементов управления, тип элемента управления Document
- события, тип элемента управления Document
- Поддержка типа элемента управления Document
- Document - тип элемента управления
- типы элементов управления, древовидная структура для типа элемента управления Document
- типы элементов управления, шаблоны элементов управления для типа документа
- типы элементов управления, поддержка документов
- типы элементов управления, документ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067868"
---
# <a name="document-control-type"></a><span data-ttu-id="2b2fa-119">Тип элемента управления документом</span><span class="sxs-lookup"><span data-stu-id="2b2fa-119">Document Control Type</span></span>

<span data-ttu-id="2b2fa-120">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **документом** .</span><span class="sxs-lookup"><span data-stu-id="2b2fa-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="2b2fa-121">С помощью элементов управления "Документ" пользователи могут просматривать несколько страниц текста и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="2b2fa-122">В отличие от элементов управления "поле ввода", которые поддерживают только простую строку неформатированного текста, элементы управления "документ" могут размещать текст с широким стилем и форматированием.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="2b2fa-123">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **Document** .</span><span class="sxs-lookup"><span data-stu-id="2b2fa-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="2b2fa-124">Требования к автоматизации пользовательского интерфейса применяются ко всем элементам управления документом, где платформа или платформа пользовательского интерфейса интегрирует поддержку модели автоматизации пользовательского интерфейса для типов элементов управления и шаблонов элементов управления.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2b2fa-125">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2b2fa-126">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="2b2fa-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2b2fa-127">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="2b2fa-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2b2fa-128">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="2b2fa-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="2b2fa-129">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="2b2fa-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2b2fa-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2b2fa-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2b2fa-131">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="2b2fa-131">Typical Tree Structure</span></span>

<span data-ttu-id="2b2fa-132">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления "документ" и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="2b2fa-133">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2b2fa-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b2fa-134">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="2b2fa-134">Control View</span></span></th>
<th><span data-ttu-id="2b2fa-135">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="2b2fa-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2b2fa-136">Документ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-136">Document</span></span>
<ul>
<li><span data-ttu-id="2b2fa-137">Различается</span><span class="sxs-lookup"><span data-stu-id="2b2fa-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2b2fa-138">Документ</span><span class="sxs-lookup"><span data-stu-id="2b2fa-138">Document</span></span>
<ul>
<li><span data-ttu-id="2b2fa-139">Различается</span><span class="sxs-lookup"><span data-stu-id="2b2fa-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="2b2fa-140">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="2b2fa-140">Relevant Properties</span></span>

<span data-ttu-id="2b2fa-141">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления документом.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="2b2fa-142">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="2b2fa-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="2b2fa-143">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b2fa-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="2b2fa-144">Значение</span><span class="sxs-lookup"><span data-stu-id="2b2fa-144">Value</span></span>        | <span data-ttu-id="2b2fa-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b2fa-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b2fa-146">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="2b2fa-147">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-147">See notes.</span></span>   | <span data-ttu-id="2b2fa-148">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="2b2fa-149">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="2b2fa-150">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-150">See notes.</span></span>   | <span data-ttu-id="2b2fa-151">Внешний прямоугольник, содержащий весь элемент управления.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="2b2fa-152">**UIA \_ кликкаблепоинтпропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="2b2fa-153">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-153">See notes.</span></span>   | <span data-ttu-id="2b2fa-154">Документ имеет активную точку, при щелчке которой фокус перемещается в один из его элементов в контейнере документа.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="2b2fa-155">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="2b2fa-156">**Document**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="2b2fa-157">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2b2fa-158">true</span><span class="sxs-lookup"><span data-stu-id="2b2fa-158">TRUE</span></span>         | <span data-ttu-id="2b2fa-159">Элемент управления "документ" всегда включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="2b2fa-160">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2b2fa-161">true</span><span class="sxs-lookup"><span data-stu-id="2b2fa-161">TRUE</span></span>         | <span data-ttu-id="2b2fa-162">Элемент управления "документ" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="2b2fa-163">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="2b2fa-164">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-164">See notes.</span></span>   | <span data-ttu-id="2b2fa-165">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="2b2fa-166">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2b2fa-167">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-167">See notes.</span></span>   | <span data-ttu-id="2b2fa-168">Значение этого свойства должно быть меткой элемента управления "Документ".</span><span class="sxs-lookup"><span data-stu-id="2b2fa-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="2b2fa-169">Как правило, используется заголовок документа.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="2b2fa-170">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="2b2fa-171">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-171">See notes.</span></span>   | <span data-ttu-id="2b2fa-172">Локализованная строка, соответствующая типу элемента управления **Document** .</span><span class="sxs-lookup"><span data-stu-id="2b2fa-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="2b2fa-173">Значение по умолчанию — "Document" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="2b2fa-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="2b2fa-174">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="2b2fa-175">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-175">See notes.</span></span>   | <span data-ttu-id="2b2fa-176">Элемент управления "документ" обычно получает свое имя из имени файла, из которого он загружается.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="2b2fa-177">Оно часто отображается в заголовке, содержащем окна или рамки.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="2b2fa-178">Обязательные шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="2b2fa-178">Required Control Patterns</span></span>

<span data-ttu-id="2b2fa-179">В следующей таблице перечислены шаблоны элементов управления модели автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "документ".</span><span class="sxs-lookup"><span data-stu-id="2b2fa-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="2b2fa-180">Дополнительные сведения о шаблонах элементов управления см. в разделе [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2b2fa-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2b2fa-181">Шаблон элемента управления/свойство шаблона</span><span class="sxs-lookup"><span data-stu-id="2b2fa-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="2b2fa-182">Поддержка/значение</span><span class="sxs-lookup"><span data-stu-id="2b2fa-182">Support/Value</span></span> | <span data-ttu-id="2b2fa-183">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b2fa-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b2fa-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="2b2fa-185">Зависит</span><span class="sxs-lookup"><span data-stu-id="2b2fa-185">Depends</span></span>       | <span data-ttu-id="2b2fa-186">Элемент управления "Документ" может занимать, превышающую область просмотра.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="2b2fa-187">Элемент управления должен поддерживать шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , если содержимое прокручивается.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="2b2fa-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="2b2fa-189">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2b2fa-189">Required</span></span>      | <span data-ttu-id="2b2fa-190">Все элементы управления "документ" должны поддерживать шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="2b2fa-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="2b2fa-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="2b2fa-192">Зависит</span><span class="sxs-lookup"><span data-stu-id="2b2fa-192">Depends</span></span>       | <span data-ttu-id="2b2fa-193">Хотя клиенты автоматизации пользовательского интерфейса могут использовать [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) для получения текстовых данных о документе, им нужен шаблон элемента управления [value](uiauto-implementingvalue.md) для установки внутреннего значения.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="2b2fa-194">Простой текстовый ввод возможен только с помощью шаблона элемента управления Value.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="2b2fa-195">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="2b2fa-195">Required Events</span></span>

<span data-ttu-id="2b2fa-196">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "документ".</span><span class="sxs-lookup"><span data-stu-id="2b2fa-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="2b2fa-197">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2b2fa-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2b2fa-198">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b2fa-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="2b2fa-199">Примечания</span><span class="sxs-lookup"><span data-stu-id="2b2fa-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b2fa-200">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="2b2fa-201">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="2b2fa-202">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="2b2fa-203">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="2b2fa-204">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="2b2fa-205">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="2b2fa-206">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="2b2fa-207">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталлискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="2b2fa-208">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2b2fa-209">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="2b2fa-210">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2b2fa-211">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллхоризонталвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="2b2fa-212">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2b2fa-213">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикаллискроллаблепропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="2b2fa-214">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2b2fa-215">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалскроллперцентпропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="2b2fa-216">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="2b2fa-217">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства скроллвертикалвиевсизепропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="2b2fa-218">Если элемент управления поддерживает шаблон элемента управления [Scroll](uiauto-implementingscroll.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="2b2fa-219">**\_Выбор UIA \_ инвалидатедевентид**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="2b2fa-220">Если элемент управления поддерживает шаблон элемента управления [Selection](uiauto-implementingselection.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="2b2fa-221">**\_Текстовая \_ ТЕКСТСЕЛЕКТИОНЧАНЖЕДЕВЕНТИДа UIA**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="2b2fa-222">**\_Текстовая \_ ТЕКСТЧАНЖЕДЕВЕНТИДа UIA**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="2b2fa-223">[**UIA \_**](uiauto-control-pattern-propids.md) Событие изменения свойства валуевалуепропертид.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="2b2fa-224">Если элемент управления поддерживает шаблон элемента управления [value](uiauto-implementingvalue.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="2b2fa-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="2b2fa-225">См. также</span><span class="sxs-lookup"><span data-stu-id="2b2fa-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2b2fa-226">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2b2fa-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b2fa-227">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b2fa-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2b2fa-228">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="2b2fa-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




