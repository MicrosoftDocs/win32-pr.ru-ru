---
title: Общие сведения о типах элементов управления автоматизации пользовательского интерфейса
description: Типы элементов управления Microsoft UI Automation — это свойства, которые служат известными идентификаторами, которые указывают тип элемента управления, представляемого определенным элементом пользовательского интерфейса, например поле со списком или кнопку.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Модель автоматизации пользовательского интерфейса, общие сведения о типах элементов управления
- Модель автоматизации пользовательского интерфейса, свойство UIA_LocalizedControlTypePropertyId
- типы элементов управления, сведения
- типы элементов управления, реквизиты
- типы элементов управления, предварительные требования
- типы элементов управления, предопределенные
- типы элементов управления, UIA_LocalizedControlTypePropertyId свойство
- стандартные типы элементов управления
- UIA_LocalizedControlTypePropertyId, свойство
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533209"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="0c505-112">Общие сведения о типах элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="0c505-113">Типы элементов управления Microsoft UI Automation — это свойства, которые служат известными идентификаторами, которые указывают тип элемента управления, представляемого определенным элементом пользовательского интерфейса, например поле со списком или кнопку.</span><span class="sxs-lookup"><span data-stu-id="0c505-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="0c505-114">Клиентские приложения используют тип для определения возможностей элемента управления и для определения способа взаимодействия с ним.</span><span class="sxs-lookup"><span data-stu-id="0c505-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="0c505-115">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="0c505-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="0c505-116">Необходимые компоненты элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="0c505-117">Свойство Локализедконтролтипе</span><span class="sxs-lookup"><span data-stu-id="0c505-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="0c505-118">Текущие типы элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="0c505-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0c505-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="0c505-120">Необходимые компоненты элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="0c505-121">Каждый тип элемента управления модели автоматизации пользовательского интерфейса имеет набор связанных с ним условий.</span><span class="sxs-lookup"><span data-stu-id="0c505-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="0c505-122">Когда поставщик присваивает элементу управления тип, поставщик должен обеспечить соответствие элемента управления всем условиям, связанным с этим типом элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="0c505-123">Условия включают следующее.</span><span class="sxs-lookup"><span data-stu-id="0c505-123">The conditions include the following:</span></span>

-   <span data-ttu-id="0c505-124">Шаблоны элементов управления модели автоматизации пользовательского интерфейса: каждый тип элемента управления имеет набор шаблонов элементов управления, которые должен поддерживать элемент управления, необязательный набор и набор, который элемент управления не должен поддерживать.</span><span class="sxs-lookup"><span data-stu-id="0c505-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="0c505-125">Значения свойств автоматизации пользовательского интерфейса. Каждый тип элемента управления содержит набор свойств, которые должен поддерживать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="0c505-126">События автоматизации пользовательского интерфейса. Каждый тип элемента управления содержит набор событий, которые должен поддерживать элемент управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="0c505-127">Дерево автоматизации пользовательского интерфейса. Каждый тип элемента управления определяет порядок отображения элемента управления в дереве автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c505-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="0c505-128">Если элемент управления удовлетворяет условиям для определенного типа элемента управления, значение свойства [**иуиаутоматионелемент:: куррентконтролтипе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (или [**Иуиаутоматионелемент:: качедконтролтипе**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) будет означать, что тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="0c505-129">Если элемент управления не соответствует спецификациям для конкретного типа элемента управления, используйте [**UIA \_ кустомконтролтипеид**](uiauto-controltype-ids.md) в качестве идентификатора типа элемента управления и полностью Опишите элемент управления с помощью соответствующих шаблонов элементов управления и свойств.</span><span class="sxs-lookup"><span data-stu-id="0c505-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="0c505-130">Можно также задать для свойства [**UIA \_ локализедконтролтипепропертид**](uiauto-automation-element-propids.md) строку, которая лучше описывает тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="0c505-131">Свойство Локализедконтролтипе</span><span class="sxs-lookup"><span data-stu-id="0c505-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="0c505-132">Если для описания элемента управления используется стандартный тип элемента управления, используйте значение по умолчанию для свойства [**UIA \_ локализедконтролтипепропертид**](uiauto-automation-element-propids.md) и позвольте автоматизации пользовательского интерфейса предоставить локализованную строку для правильного предоставления поставщикам.</span><span class="sxs-lookup"><span data-stu-id="0c505-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="0c505-133">Если для описания элемента управления нельзя использовать стандартный тип элемента управления, задайте для свойства **UIA \_ локализедконтролтипепропертид** локализованную строку, которая точно описывает тип элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="0c505-134">Строка должна быть краткой, но достаточно точной, чтобы с помощью вспомогательной технологии, такой как средство чтения с экрана, можно было использовать его в пользовательском интерфейсе для информирования пользователя о типе элемента управления.</span><span class="sxs-lookup"><span data-stu-id="0c505-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="0c505-135">Текущие типы элементов управления автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="0c505-136">В следующих разделах описываются типы элементов управления модели автоматизации пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="0c505-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="0c505-137">Для каждого типа элемента управления описание включает набор условий, которые должен поддерживать элемент управления данного типа:</span><span class="sxs-lookup"><span data-stu-id="0c505-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="0c505-138">Тип элемента управления панель приложений</span><span class="sxs-lookup"><span data-stu-id="0c505-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="0c505-139">Тип элемента управления Button</span><span class="sxs-lookup"><span data-stu-id="0c505-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="0c505-140">Тип элемента управления Calendar</span><span class="sxs-lookup"><span data-stu-id="0c505-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="0c505-141">Тип элемента управления CheckBox</span><span class="sxs-lookup"><span data-stu-id="0c505-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="0c505-142">Тип элемента управления ComboBox</span><span class="sxs-lookup"><span data-stu-id="0c505-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="0c505-143">Тип элемента управления DataGrid</span><span class="sxs-lookup"><span data-stu-id="0c505-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="0c505-144">Тип элемента управления DataItem</span><span class="sxs-lookup"><span data-stu-id="0c505-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="0c505-145">Тип элемента управления документом</span><span class="sxs-lookup"><span data-stu-id="0c505-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="0c505-146">Изменить тип элемента управления</span><span class="sxs-lookup"><span data-stu-id="0c505-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="0c505-147">Тип элемента управления Group</span><span class="sxs-lookup"><span data-stu-id="0c505-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="0c505-148">Тип элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="0c505-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="0c505-149">Тип элемента управления HeaderItem</span><span class="sxs-lookup"><span data-stu-id="0c505-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="0c505-150">Тип элемента управления HyperLink</span><span class="sxs-lookup"><span data-stu-id="0c505-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="0c505-151">Тип элемента управления Image</span><span class="sxs-lookup"><span data-stu-id="0c505-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="0c505-152">Тип элемента управления List</span><span class="sxs-lookup"><span data-stu-id="0c505-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="0c505-153">Тип элемента управления ListItem</span><span class="sxs-lookup"><span data-stu-id="0c505-153">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="0c505-154">Тип элемента управления Menu</span><span class="sxs-lookup"><span data-stu-id="0c505-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="0c505-155">Тип элемента управления MenuBar</span><span class="sxs-lookup"><span data-stu-id="0c505-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="0c505-156">Тип элемента управления MenuItem</span><span class="sxs-lookup"><span data-stu-id="0c505-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="0c505-157">Тип элемента управления панели</span><span class="sxs-lookup"><span data-stu-id="0c505-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="0c505-158">Тип элемента управления ProgressBar</span><span class="sxs-lookup"><span data-stu-id="0c505-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="0c505-159">Тип элемента управления RadioButton</span><span class="sxs-lookup"><span data-stu-id="0c505-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="0c505-160">Тип элемента управления ScrollBar</span><span class="sxs-lookup"><span data-stu-id="0c505-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="0c505-161">Тип элемента управления Семантикзум</span><span class="sxs-lookup"><span data-stu-id="0c505-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="0c505-162">Тип элемента управления Separator</span><span class="sxs-lookup"><span data-stu-id="0c505-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="0c505-163">Тип элемента управления Slider</span><span class="sxs-lookup"><span data-stu-id="0c505-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="0c505-164">Тип элемента управления "Счетчик"</span><span class="sxs-lookup"><span data-stu-id="0c505-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="0c505-165">Тип элемента управления SplitButton</span><span class="sxs-lookup"><span data-stu-id="0c505-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="0c505-166">Тип элемента управления StatusBar</span><span class="sxs-lookup"><span data-stu-id="0c505-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="0c505-167">Тип элемента управления Tab</span><span class="sxs-lookup"><span data-stu-id="0c505-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="0c505-168">Тип элемента управления TabItem</span><span class="sxs-lookup"><span data-stu-id="0c505-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="0c505-169">Тип элемента управления Table</span><span class="sxs-lookup"><span data-stu-id="0c505-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="0c505-170">Тип элемента управления "текст"</span><span class="sxs-lookup"><span data-stu-id="0c505-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="0c505-171">Тип элемента управления Thumb</span><span class="sxs-lookup"><span data-stu-id="0c505-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="0c505-172">Тип элемента управления "заголовок"</span><span class="sxs-lookup"><span data-stu-id="0c505-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="0c505-173">Тип элемента управления ToolBar</span><span class="sxs-lookup"><span data-stu-id="0c505-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="0c505-174">Тип элемента управления ToolTip</span><span class="sxs-lookup"><span data-stu-id="0c505-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="0c505-175">Тип элемента управления "дерево"</span><span class="sxs-lookup"><span data-stu-id="0c505-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="0c505-176">Тип элемента управления TreeItem</span><span class="sxs-lookup"><span data-stu-id="0c505-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="0c505-177">Тип элемента управления окна</span><span class="sxs-lookup"><span data-stu-id="0c505-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="0c505-178">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0c505-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0c505-179">**Reference**</span><span class="sxs-lookup"><span data-stu-id="0c505-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c505-180">Идентификаторы типов элементов управления</span><span class="sxs-lookup"><span data-stu-id="0c505-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="0c505-181">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="0c505-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c505-182">Поддержка типов элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="0c505-183">Поддержка автоматизации пользовательского интерфейса для стандартных элементов управления</span><span class="sxs-lookup"><span data-stu-id="0c505-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="0c505-184">Основы модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="0c505-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 