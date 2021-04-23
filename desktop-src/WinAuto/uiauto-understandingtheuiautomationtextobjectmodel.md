---
title: Основные сведения об объектной модели текста автоматизации пользовательского интерфейса
description: В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт обращаются к текстовому содержимому элемента управления на основе текста.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- Клиенты, общие сведения о модели объектов текста автоматизации пользовательского интерфейса
- Клиенты, текстовые элементы управления
- Клиенты, текстовые диапазоны
- Клиенты, шаблон элемента управления Text
- Клиенты, шаблон элемента управления TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774876"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="5eb12-108">Основные сведения об объектной модели текста автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="5eb12-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="5eb12-109">В этом разделе описывается, как клиентские приложения автоматизации пользовательского интерфейса Майкрософт обращаются к текстовому содержимому элемента управления на основе текста.</span><span class="sxs-lookup"><span data-stu-id="5eb12-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="5eb12-110">Объектная модель для конкретного элемента управления</span><span class="sxs-lookup"><span data-stu-id="5eb12-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="5eb12-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5eb12-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="5eb12-112">Текстовые элементы управления предоставляют текстовое содержимое в клиентские приложения автоматизации пользовательского интерфейса через простую объектную модель текста.</span><span class="sxs-lookup"><span data-stu-id="5eb12-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="5eb12-113">Клиентские приложения имеют доступ к объектной модели Text через интерфейсы шаблонов элементов управления [Text и TextRange](uiauto-about-text-and-textrange-patterns.md) , включая [**иуиаутоматионтекстпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) и [**иуиаутоматионтекстранже**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span><span class="sxs-lookup"><span data-stu-id="5eb12-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="5eb12-114">Клиентские приложения могут использовать эти интерфейсы для получения текстового содержимого, текстовых атрибутов и внедренных объектов, таких как таблицы и гиперссылки, из текстовых элементов управления.</span><span class="sxs-lookup"><span data-stu-id="5eb12-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="5eb12-115">Типы элементов управления, поддерживающие модель объектов текста модели автоматизации пользовательского интерфейса, включают в себя типы [Edit](uiauto-supporteditcontroltype.md) и [Document](uiauto-supportdocumentcontroltype.md) Control.</span><span class="sxs-lookup"><span data-stu-id="5eb12-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="5eb12-116">Другие типы элементов управления, такие как [ToolTip](uiauto-supporttooltipcontroltype.md) и [Text](uiauto-supporttextcontroltype.md) , могут также поддерживать объектную модель текста, но не обязательно должны.</span><span class="sxs-lookup"><span data-stu-id="5eb12-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="5eb12-117">Объектная модель текста модели автоматизации пользовательского интерфейса не предоставляет средств для вставки или изменения текста.</span><span class="sxs-lookup"><span data-stu-id="5eb12-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="5eb12-118">Однако некоторые элементы управления позволяют вставлять и изменять текст либо с помощью интерфейса [**иуиаутоматионвалуепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) , либо с помощью прямого ввода с клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="5eb12-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="5eb12-119">Объектная модель для конкретного элемента управления</span><span class="sxs-lookup"><span data-stu-id="5eb12-119">Control-specific Object Model</span></span>

<span data-ttu-id="5eb12-120">Элемент управления на основе текста, реализующий собственный модель DOM (DOM), может предоставлять модель DOM путем реализации шаблона элемента управления [ObjectModel](uiauto-implementingobjectmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="5eb12-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="5eb12-121">Предоставление модели DOM может предоставить клиентским приложениям больший доступ к содержимому элемента управления на основе текста и управлять им.</span><span class="sxs-lookup"><span data-stu-id="5eb12-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="5eb12-122">Клиентское приложение может определить, реализует ли конкретный текстовый элемент управления модель DOM путем извлечения интерфейса [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) элемента управления.</span><span class="sxs-lookup"><span data-stu-id="5eb12-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="5eb12-123">Затем вызовите метод [**иуиаутоматионелемент:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , указав идентификатор свойства [**UIA \_ исобжектмоделпаттернаваилаблепропертид**](uiauto-control-pattern-availability-propids.md) , и вариант, который получает значение true, если элемент управления реализует DOM.</span><span class="sxs-lookup"><span data-stu-id="5eb12-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="5eb12-124">Чтобы получить доступ к модели DOM, вызовите метод [**иуиаутоматионелемент:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , указав идентификатор шаблона элемента управления [**UIA \_ обжектмоделпаттернид**](uiauto-controlpattern-ids.md) и переменную, которая получает интерфейс [**иуиаутоматионобжектмоделпаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) .</span><span class="sxs-lookup"><span data-stu-id="5eb12-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="5eb12-125">Вызовите метод [**иуиаутоматионобжектмоделпаттерн:: жетундерлингобжектмодел**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) , чтобы получить интерфейс DOM.</span><span class="sxs-lookup"><span data-stu-id="5eb12-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5eb12-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5eb12-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb12-127">Шаблоны элементов управления Text и TextRange</span><span class="sxs-lookup"><span data-stu-id="5eb12-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="5eb12-128">Поддержка модели автоматизации пользовательского интерфейса для текстового содержимого</span><span class="sxs-lookup"><span data-stu-id="5eb12-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="5eb12-129">Работа с элементами управления на основе текста</span><span class="sxs-lookup"><span data-stu-id="5eb12-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




