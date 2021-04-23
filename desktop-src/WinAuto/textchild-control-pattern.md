---
title: Шаблон элемента управления Текстчилд
description: Содержит рекомендации и соглашения для реализации Итекстчилдпровидер, включая сведения о свойствах и методах. Шаблон элемента управления Текстчилд используется для доступа к ближайшему предку элемента, который поддерживает шаблон элемента управления Text.
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Текстчилд
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Текстчилд
- Модель автоматизации пользовательского интерфейса, Итекстчилдпровидер
- ITextChildProvider
- реализация шаблонов элементов управления Текстчилд модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Текстчилд
- шаблоны элементов управления, Итекстчилдпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Текстчилд
- шаблоны элементов управления, Текстчилд
- интерфейсы, Итекстчилдпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793615"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="680d5-114">Шаблон элемента управления Текстчилд</span><span class="sxs-lookup"><span data-stu-id="680d5-114">TextChild Control Pattern</span></span>

<span data-ttu-id="680d5-115">Содержит рекомендации и соглашения для реализации [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="680d5-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="680d5-116">Шаблон элемента управления **текстчилд** используется для доступа к ближайшему предку элемента, который поддерживает шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="680d5-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="680d5-117">Например, предположим, что текст в документе содержит внедренное изображение и гиперссылку, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="680d5-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![снимок экрана с текстом, содержащим внедренное изображение и гиперссылку](images/textchild-pattern.png)

<span data-ttu-id="680d5-119">Если вы используете средства автоматизации пользовательского интерфейса Майкрософт для проверки дерева автоматизации пользовательского интерфейса для этого содержимого документа, оно может отобразить элемент документа с одним дочерним элементом, который представляет изображение, и другой дочерний элемент, представляющий гиперссылку.</span><span class="sxs-lookup"><span data-stu-id="680d5-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="680d5-120">Пример:</span><span class="sxs-lookup"><span data-stu-id="680d5-120">For example:</span></span>

![снимок экрана с командой "проверить отчет" в примере дерева элементов автоматизации пользовательского интерфейса](images/textchild-pattern-tree.png)

<span data-ttu-id="680d5-122">Как правило, элемент Document в предыдущем примере поддерживает шаблон элемента управления [Text](uiauto-implementingtextandtextrange.md) , но два дочерних элемента документа не имеют.</span><span class="sxs-lookup"><span data-stu-id="680d5-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="680d5-123">Если клиентское приложение автоматизации пользовательского интерфейса содержит ссылку на элемент Image или элемент Hyperlink, клиент может использовать шаблон элемента управления **текстчилд** как удобный способ доступа к шаблону текстконтрол, предоставляемому содержащим элементом Document.</span><span class="sxs-lookup"><span data-stu-id="680d5-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="680d5-124">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="680d5-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="680d5-125">При реализации интерфейса [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="680d5-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="680d5-126">Свойство [**итекстчилдпровидер:: объект textcontainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) должно указывать ближайший элемент предка, который поддерживает интерфейс [**итекстпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) , независимо от того, поддерживаются ли элементы, набольшиеся в цепочке предков, также поддерживать **итекстпровидер**.</span><span class="sxs-lookup"><span data-stu-id="680d5-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="680d5-127">Элемент не должен поддерживать интерфейс [**итекстпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) и [итекстчилдпровидер \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="680d5-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="680d5-128">Элемент, реализующий [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) , должен быть дочерним элементом или потомком элемента, реализующего [**итекстпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span><span class="sxs-lookup"><span data-stu-id="680d5-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="680d5-129">Этот элемент также не обязательно должен реализовывать [шаблон элемента управления Text](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span><span class="sxs-lookup"><span data-stu-id="680d5-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="680d5-130">Свойство [**итекстчилдпровидер:: TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) должно указывать тот же текстовый диапазон, что и элемент, содержащийся в элементе Provider Text, когда его функция [**Итекстпровидер:: ранжефромчилд**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) вызывается с дочерним элементом text как вложенный дочерний элемент.</span><span class="sxs-lookup"><span data-stu-id="680d5-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="680d5-131">Обязательные члены для **итекстчилдпровидер**</span><span class="sxs-lookup"><span data-stu-id="680d5-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="680d5-132">Эти свойства и методы необходимы для реализации интерфейса [**итекстчилдпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) .</span><span class="sxs-lookup"><span data-stu-id="680d5-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="680d5-133">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="680d5-133">Required members</span></span>                                                     | <span data-ttu-id="680d5-134">Тип члена</span><span class="sxs-lookup"><span data-stu-id="680d5-134">Member type</span></span> | <span data-ttu-id="680d5-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="680d5-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="680d5-136">**Объект textcontainer**</span><span class="sxs-lookup"><span data-stu-id="680d5-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="680d5-137">Свойство</span><span class="sxs-lookup"><span data-stu-id="680d5-137">Property</span></span>    | <span data-ttu-id="680d5-138">Нет</span><span class="sxs-lookup"><span data-stu-id="680d5-138">None</span></span>  |
| [<span data-ttu-id="680d5-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="680d5-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="680d5-140">Свойство</span><span class="sxs-lookup"><span data-stu-id="680d5-140">Property</span></span>    | <span data-ttu-id="680d5-141">Нет</span><span class="sxs-lookup"><span data-stu-id="680d5-141">None</span></span>  |



 

<span data-ttu-id="680d5-142">Этот шаблон элемента управления не имеет связанных методов или событий.</span><span class="sxs-lookup"><span data-stu-id="680d5-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="680d5-143">См. также</span><span class="sxs-lookup"><span data-stu-id="680d5-143">Related topics</span></span>

<span data-ttu-id="680d5-144">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="680d5-144">**Conceptual**</span></span>

- [<span data-ttu-id="680d5-145">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="680d5-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="680d5-146">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="680d5-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="680d5-147">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="680d5-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)