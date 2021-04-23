---
title: Тип элемента управления панель приложений
description: В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления панель приложений.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Модель автоматизации пользовательского интерфейса, поддержка типа элемента управления панель приложений
- Модель автоматизации пользовательского интерфейса, тип элемента управления панель приложений
- Модель автоматизации пользовательского интерфейса, шаблоны элементов управления для типа элемента управления панель приложений
- шаблоны элементов управления, тип элемента управления панель приложений
- Поддержка типа элемента управления панель приложений
- Тип элемента управления панель приложений
- типы элементов управления, панель приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488092"
---
# <a name="appbar-control-type"></a><span data-ttu-id="ded33-110">Тип элемента управления панель приложений</span><span class="sxs-lookup"><span data-stu-id="ded33-110">AppBar Control Type</span></span>

<span data-ttu-id="ded33-111">В этом разделе содержатся сведения о поддержке автоматизации пользовательского интерфейса Майкрософт для типа элемента управления **панель приложений** .</span><span class="sxs-lookup"><span data-stu-id="ded33-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="ded33-112">Панель приложения — это элемент пользовательского интерфейса, который предоставляет пользователю навигацию, команды и средства.</span><span class="sxs-lookup"><span data-stu-id="ded33-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="ded33-113">Для приложений Магазина Windows можно отобразить панели приложений для приложений, нажав клавиши Windows + Z.</span><span class="sxs-lookup"><span data-stu-id="ded33-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="ded33-114">В следующих разделах определяется необходимая древовидная структура модели автоматизации пользовательского интерфейса, свойства, шаблоны элементов управления и события для типа элемента управления **панель приложений** .</span><span class="sxs-lookup"><span data-stu-id="ded33-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="ded33-115">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="ded33-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ded33-116">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="ded33-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ded33-117">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="ded33-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ded33-118">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="ded33-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ded33-119">Соответствующие события</span><span class="sxs-lookup"><span data-stu-id="ded33-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="ded33-120">См. также</span><span class="sxs-lookup"><span data-stu-id="ded33-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ded33-121">Типичная древовидная структура</span><span class="sxs-lookup"><span data-stu-id="ded33-121">Typical Tree Structure</span></span>

<span data-ttu-id="ded33-122">В следующей таблице описывается типичный элемент управления и представление содержимого дерева модели автоматизации пользовательского интерфейса, которое относится к элементам управления **панель приложений** и описывает, что может содержаться в каждом представлении.</span><span class="sxs-lookup"><span data-stu-id="ded33-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ded33-123">**Является наиболее** распространенным элементом в **панель приложений** , но также возможны другие элементы управления, которые вызывают действия для приложения.</span><span class="sxs-lookup"><span data-stu-id="ded33-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="ded33-124">**Панель приложений** может также иметь 0 или более разделителей (тип элемента управления **separator** ), которые отображаются в представлении элемента управления, как и между другими элементами управления.</span><span class="sxs-lookup"><span data-stu-id="ded33-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="ded33-125">Дополнительные сведения о дереве автоматизации пользовательского интерфейса см. в разделе [Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ded33-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ded33-126">Представление элемента управления</span><span class="sxs-lookup"><span data-stu-id="ded33-126">Control View</span></span></th>
<th><span data-ttu-id="ded33-127">Представление содержимого</span><span class="sxs-lookup"><span data-stu-id="ded33-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ded33-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="ded33-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="ded33-129">Button (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ded33-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="ded33-130">Другие элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ded33-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ded33-131">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="ded33-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="ded33-132">Button (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ded33-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="ded33-133">Другие элементы управления (0 или более)</span><span class="sxs-lookup"><span data-stu-id="ded33-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="ded33-134">Соответствующие свойства</span><span class="sxs-lookup"><span data-stu-id="ded33-134">Relevant Properties</span></span>

<span data-ttu-id="ded33-135">В следующей таблице перечислены свойства модели автоматизации пользовательского интерфейса, значения или определения которых особенно важны для элементов управления, реализующих тип элемента управления **панель приложений** .</span><span class="sxs-lookup"><span data-stu-id="ded33-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="ded33-136">Дополнительные сведения о свойствах модели автоматизации пользовательского интерфейса см. в разделе [Получение свойств элементов модели автоматизации пользовательского интерфейса](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="ded33-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ded33-137">Свойство модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ded33-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ded33-138">Значение</span><span class="sxs-lookup"><span data-stu-id="ded33-138">Value</span></span>      | <span data-ttu-id="ded33-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="ded33-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ded33-140">**UIA \_ аутоматионидпропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ded33-141">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ded33-141">See notes.</span></span> | <span data-ttu-id="ded33-142">Значение этого свойства должно быть уникальным среди всех одноранговых элементов в необработанном представлении дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ded33-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="ded33-143">**UIA \_ баундингректанглепропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ded33-144">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ded33-144">See notes.</span></span> | <span data-ttu-id="ded33-145">Значение, представляемое этим свойством, должно включать все содержащиеся в нем элементы управления.</span><span class="sxs-lookup"><span data-stu-id="ded33-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="ded33-146">**UIA \_ контролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ded33-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="ded33-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="ded33-148">**UIA \_ исконтентелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ded33-149">FALSE</span><span class="sxs-lookup"><span data-stu-id="ded33-149">FALSE</span></span>      | <span data-ttu-id="ded33-150">Элемент управления "панель приложений" не включается в представление содержимого дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ded33-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="ded33-151">**UIA \_ исконтролелементпропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ded33-152">true</span><span class="sxs-lookup"><span data-stu-id="ded33-152">TRUE</span></span>       | <span data-ttu-id="ded33-153">Элемент управления "панель приложений" всегда включается в представление элемента управления дерева модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ded33-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="ded33-154">**UIA \_ искэйбоардфокусаблепропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ded33-155">См. примечания</span><span class="sxs-lookup"><span data-stu-id="ded33-155">See notes</span></span>  | <span data-ttu-id="ded33-156">Если элемент управления может получать фокус клавиатуры, он должен поддерживать это свойство.</span><span class="sxs-lookup"><span data-stu-id="ded33-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="ded33-157">Элементы управления на панели приложения обычно могут принимать фокус клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="ded33-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="ded33-158">**UIA \_ исоффскринпропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ded33-159">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ded33-159">See notes.</span></span> | <span data-ttu-id="ded33-160">Значение этого свойства зависит от того, можно ли видеть элемент управления на экране.</span><span class="sxs-lookup"><span data-stu-id="ded33-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="ded33-161">**UIA \_ лабеледбипропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ded33-162">NULL</span><span class="sxs-lookup"><span data-stu-id="ded33-162">Null</span></span>       | <span data-ttu-id="ded33-163">Элементы управления "панель приложений" обычно не имеют метки.</span><span class="sxs-lookup"><span data-stu-id="ded33-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="ded33-164">**UIA \_ локализедконтролтипепропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ded33-165">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ded33-165">See notes.</span></span> | <span data-ttu-id="ded33-166">Локализованная строка, соответствующая типу элемента управления **панель приложений** .</span><span class="sxs-lookup"><span data-stu-id="ded33-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="ded33-167">Значение по умолчанию — "панель приложений" для en-US или English (США).</span><span class="sxs-lookup"><span data-stu-id="ded33-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="ded33-168">**UIA \_ намепропертид**</span><span class="sxs-lookup"><span data-stu-id="ded33-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ded33-169">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="ded33-169">See notes.</span></span> | <span data-ttu-id="ded33-170">Элементу управления "панель приложений" не требуется имя, если приложение не содержит более одной панели приложений.</span><span class="sxs-lookup"><span data-stu-id="ded33-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="ded33-171">Если в приложении имеется несколько панелей приложений, используйте это свойство для различения имен, например "Top" или "Bottom".</span><span class="sxs-lookup"><span data-stu-id="ded33-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ded33-172">Обязательные события</span><span class="sxs-lookup"><span data-stu-id="ded33-172">Required Events</span></span>

<span data-ttu-id="ded33-173">В следующей таблице перечислены события автоматизации пользовательского интерфейса, которые должны поддерживаться элементами управления "панель приложений".</span><span class="sxs-lookup"><span data-stu-id="ded33-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="ded33-174">Дополнительные сведения о событиях см. в разделе [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="ded33-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ded33-175">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ded33-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ded33-176">Примечания</span><span class="sxs-lookup"><span data-stu-id="ded33-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ded33-177">**UIA \_ аутоматионфокусчанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="ded33-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ded33-178">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства баундингректанглепропертид.</span><span class="sxs-lookup"><span data-stu-id="ded33-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ded33-179">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исенабледпропертид.</span><span class="sxs-lookup"><span data-stu-id="ded33-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ded33-180">Если элемент управления поддерживает свойство « [**включено**](uiauto-automation-element-propids.md) », оно должно поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="ded33-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ded33-181">[**UIA \_**](uiauto-automation-element-propids.md) Событие изменения свойства исоффскринпропертид.</span><span class="sxs-lookup"><span data-stu-id="ded33-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ded33-182">Если элемент управления поддерживает свойство [**исоффскрин**](uiauto-automation-element-propids.md) , он должен поддерживать это событие.</span><span class="sxs-lookup"><span data-stu-id="ded33-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="ded33-183">**UIA \_ структуречанжедевентид**</span><span class="sxs-lookup"><span data-stu-id="ded33-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="ded33-184">Соответствующие события</span><span class="sxs-lookup"><span data-stu-id="ded33-184">Relevant Events</span></span>

<span data-ttu-id="ded33-185">В следующей таблице перечислены события модели автоматизации пользовательского интерфейса, которые особенно важны для элементов управления, которые реализуют тип элемента управления **панель приложений** , но не являются строго обязательными.</span><span class="sxs-lookup"><span data-stu-id="ded33-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="ded33-186">Событие автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ded33-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="ded33-187">Примечания</span><span class="sxs-lookup"><span data-stu-id="ded33-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ded33-188">**UIA \_ менуклоседевентид**</span><span class="sxs-lookup"><span data-stu-id="ded33-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="ded33-189">Реализации платформы могут вызывать это событие при закрытии элемента управления "панель приложений".</span><span class="sxs-lookup"><span data-stu-id="ded33-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="ded33-190">**UIA \_ менуопенедевентид**</span><span class="sxs-lookup"><span data-stu-id="ded33-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="ded33-191">Реализации платформы могут вызывать это событие при открытии элемента управления "панель приложений".</span><span class="sxs-lookup"><span data-stu-id="ded33-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="ded33-192">**иуиаутоматионпропертичанжедевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="ded33-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="ded33-193">Обработчик событий изменения свойства.</span><span class="sxs-lookup"><span data-stu-id="ded33-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="ded33-194">См. также</span><span class="sxs-lookup"><span data-stu-id="ded33-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ded33-195">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="ded33-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ded33-196">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ded33-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ded33-197">Общие сведения о модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="ded33-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="ded33-198">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="ded33-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ded33-199">**Элемент управления XAML панель приложений**</span><span class="sxs-lookup"><span data-stu-id="ded33-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="ded33-200">[**WinJS. UI. панель приложений, объект**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="ded33-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 