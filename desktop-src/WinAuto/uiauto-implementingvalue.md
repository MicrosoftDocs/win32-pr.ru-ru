---
title: Шаблон элемента управления Value
description: Описывает правила и соглашения для реализации Ивалуепровидер, включая сведения о свойствах и методах.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Value
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Value
- Модель автоматизации пользовательского интерфейса, Ивалуепровидер
- IValueProvider
- реализация шаблонов элементов управления "значение модели автоматизации пользовательского интерфейса"
- Шаблоны элементов управления Value
- шаблоны элементов управления, Ивалуепровидер
- шаблоны элементов управления, реализация значения автоматизации пользовательского интерфейса
- шаблоны элементов управления, значение
- интерфейсы, Ивалуепровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413301"
---
# <a name="value-control-pattern"></a><span data-ttu-id="c269d-113">Шаблон элемента управления Value</span><span class="sxs-lookup"><span data-stu-id="c269d-113">Value Control Pattern</span></span>

<span data-ttu-id="c269d-114">Описывает правила и соглашения для реализации [**ивалуепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="c269d-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="c269d-115">Шаблон элемента управления **value** используется для поддержки элементов управления с внутренним значением, не охватывающим диапазон, которые могут быть представлены в виде строки.</span><span class="sxs-lookup"><span data-stu-id="c269d-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="c269d-116">Строку значения можно изменять в зависимости от элемента управления и его параметров.</span><span class="sxs-lookup"><span data-stu-id="c269d-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="c269d-117">Примеры элементов управления, реализующих этот шаблон элемента управления, см. в разделе [типы элементов управления и поддерживаемые шаблоны элементов управления](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c269d-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="c269d-118">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="c269d-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c269d-119">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="c269d-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c269d-120">Обязательные члены для **ивалуепровидер**</span><span class="sxs-lookup"><span data-stu-id="c269d-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="c269d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="c269d-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c269d-122">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="c269d-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c269d-123">При реализации шаблона элемента управления **value** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="c269d-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c269d-124">Элементы управления, такие как элемент списка или элемент дерева, должны поддерживать шаблон элемента управления **value** , если значение любого из элементов доступно для редактирования, независимо от текущего режима редактирования элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c269d-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="c269d-125">Родительский элемент управления также должен поддерживать шаблон элемента управления **value** , если дочерние элементы доступны для редактирования.</span><span class="sxs-lookup"><span data-stu-id="c269d-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="c269d-126">На следующем рисунке показан пример изменяемого элемента списка.</span><span class="sxs-lookup"><span data-stu-id="c269d-126">The following image shows an example of an editable list item.</span></span>

    ![Иллюстрация, демонстрирующая редактируемый элемент списка](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="c269d-128">Одинарные и многострочные элементы управления редактирования должны реализовывать [**итекстпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , чтобы предоставить доступ к содержимому только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c269d-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="c269d-129">Элементы управления для многострочного редактирования должны реализовывать [**ивалуепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) , если их содержимое можно изменить.</span><span class="sxs-lookup"><span data-stu-id="c269d-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="c269d-130">[**Ивалуепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) не поддерживает извлечение сведений о форматировании или значений подстрок.</span><span class="sxs-lookup"><span data-stu-id="c269d-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="c269d-131">Реализуйте [**итекстпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) в этих сценариях.</span><span class="sxs-lookup"><span data-stu-id="c269d-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="c269d-132">[**Ивалуепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) должен быть реализован элементами управления, такими как элемент управления выбора цвета из Microsoft Word (см. следующий рисунок), который поддерживает строковое сопоставление между значением цвета (например, "желтый") и эквивалентным внутренним значением [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="c269d-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![Иллюстрация, показывающая сопоставление строк цветовой палитры](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="c269d-134">Свойство "IsReadOnly" элемента управления должно иметь значение **true** , **а свойство** [**итекстпровидер:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) — значение **false** , прежде чем разрешить вызов [**итекстпровидер:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span><span class="sxs-lookup"><span data-stu-id="c269d-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="c269d-135">Обязательные члены для **ивалуепровидер**</span><span class="sxs-lookup"><span data-stu-id="c269d-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="c269d-136">Для реализации интерфейса [**ивалуепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) требуются следующие свойства и методы.</span><span class="sxs-lookup"><span data-stu-id="c269d-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="c269d-137">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="c269d-137">Required members</span></span>                                       | <span data-ttu-id="c269d-138">Тип члена</span><span class="sxs-lookup"><span data-stu-id="c269d-138">Member type</span></span> | <span data-ttu-id="c269d-139">Примечания</span><span class="sxs-lookup"><span data-stu-id="c269d-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c269d-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="c269d-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="c269d-141">Свойство</span><span class="sxs-lookup"><span data-stu-id="c269d-141">Property</span></span>    | <span data-ttu-id="c269d-142">Нет</span><span class="sxs-lookup"><span data-stu-id="c269d-142">None</span></span>  |
| [<span data-ttu-id="c269d-143">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c269d-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="c269d-144">Свойство</span><span class="sxs-lookup"><span data-stu-id="c269d-144">Property</span></span>    | <span data-ttu-id="c269d-145">Нет</span><span class="sxs-lookup"><span data-stu-id="c269d-145">None</span></span>  |
| [<span data-ttu-id="c269d-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="c269d-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="c269d-147">Метод</span><span class="sxs-lookup"><span data-stu-id="c269d-147">Method</span></span>      | <span data-ttu-id="c269d-148">Нет</span><span class="sxs-lookup"><span data-stu-id="c269d-148">None</span></span>  |



 

<span data-ttu-id="c269d-149">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="c269d-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c269d-150">См. также</span><span class="sxs-lookup"><span data-stu-id="c269d-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c269d-151">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="c269d-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c269d-152">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c269d-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c269d-153">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="c269d-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="c269d-154">Шаблоны элементов управления Text и TextRange</span><span class="sxs-lookup"><span data-stu-id="c269d-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 