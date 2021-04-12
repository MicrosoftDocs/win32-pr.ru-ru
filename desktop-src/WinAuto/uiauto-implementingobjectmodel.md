---
title: Шаблон элемента управления ObjectModel
description: Описывает правила и соглашения для реализации Иобжектмоделпровидер, включая сведения о методах. Шаблон элемента управления ObjectModel используется для предоставления указателя на базовую объектную модель документа.
ms.assetid: 90A6937E-0E98-41EF-8EEB-E23CB71510E4
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления ObjectModel
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления ObjectModel
- Модель автоматизации пользовательского интерфейса, Иобжектмоделпровидер
- IObjectModelProvider
- Реализация шаблона элемента управления ObjectModel модели автоматизации пользовательского интерфейса
- Шаблон элемента управления ObjectModel
- шаблоны элементов управления, Иобжектмоделпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса ObjectModel
- шаблоны элементов управления, ObjectModel
- интерфейсы, Иобжектмоделпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ff115233faf19f93963153a0b2a0a1ff52c3f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338337"
---
# <a name="objectmodel-control-pattern"></a><span data-ttu-id="3e6f6-114">Шаблон элемента управления ObjectModel</span><span class="sxs-lookup"><span data-stu-id="3e6f6-114">ObjectModel Control Pattern</span></span>

<span data-ttu-id="3e6f6-115">Описывает правила и соглашения для реализации [**иобжектмоделпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), включая сведения о методах.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-115">Describes guidelines and conventions for implementing [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider), including information about methods.</span></span> <span data-ttu-id="3e6f6-116">Шаблон элемента управления **ObjectModel** используется для предоставления указателя на базовую объектную модель документа.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-116">The **ObjectModel** control pattern is used to expose a pointer to the underlying object model of a document.</span></span>

<span data-ttu-id="3e6f6-117">Многие приложения реализуют обширные объектные модели, которые расширяют возможности, предоставляемые Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-117">Many applications implement rich object models that add value beyond what Microsoft UI Automation provides.</span></span> <span data-ttu-id="3e6f6-118">Этот шаблон элемента управления позволяет клиенту переходить от элемента модели автоматизации пользовательского интерфейса к базовой объектной модели.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-118">This control pattern allows a client to navigate from a UI Automation element into the underlying object model.</span></span>

<span data-ttu-id="3e6f6-119">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3e6f6-120">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="3e6f6-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3e6f6-121">Обязательные члены для **иобжектмоделпровидер**</span><span class="sxs-lookup"><span data-stu-id="3e6f6-121">Required Members for **IObjectModelProvider**</span></span>](#required-members-for-iobjectmodelprovider)
-   [<span data-ttu-id="3e6f6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3e6f6-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3e6f6-123">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="3e6f6-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3e6f6-124">При реализации шаблона элемента управления **ObjectModel** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-124">When implementing the **ObjectModel** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3e6f6-125">Метод [**иобжектмоделпровидер:: жетундерлингобжектмодел**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) должен возвращать указатель на объект, который как можно ближе к исходному ЭЛЕМЕНТУ пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-125">The [**IObjectModelProvider::GetUnderlyingObjectModel**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) method should return a pointer to the object that is as close as possible to the source UI element.</span></span> <span data-ttu-id="3e6f6-126">Например, в веб-браузере поставщик автоматизации пользовательского интерфейса для одного элемента должен возвращать указатель объектной модели для элемента.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-126">For example, in a web browser, a UI Automation provider for a single element should return an object model pointer for the element.</span></span> <span data-ttu-id="3e6f6-127">Возврат указателя объектной модели для корневого каталога документа будет гораздо менее полезным.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-127">Returning an object model pointer for the document root would be far less useful.</span></span>
-   <span data-ttu-id="3e6f6-128">Ожидается, что клиент шаблона элемента управления **ObjectModel** должен иметь IID для интерфейса, который они ищут, поэтому он достаточно для возврата простого указателя [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3e6f6-128">The client of the **ObjectModel** control pattern is expected to have the IID for the interface they are seeking, which is why it is enough to return a simple [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>
-   <span data-ttu-id="3e6f6-129">Поскольку модель автоматизации пользовательского интерфейса маршалирует указатель на клиентский процесс, поставщик должен ждать, что клиент получает доступ к объектной модели, используя стандартные методики модели объектов компонентов (COM).</span><span class="sxs-lookup"><span data-stu-id="3e6f6-129">Because UI Automation marshals the pointer to the client process, the provider should expect the client to access the object model using standard Component Object Model (COM) practices.</span></span>

## <a name="required-members-for-iobjectmodelprovider"></a><span data-ttu-id="3e6f6-130">Обязательные члены для **иобжектмоделпровидер**</span><span class="sxs-lookup"><span data-stu-id="3e6f6-130">Required Members for **IObjectModelProvider**</span></span>

<span data-ttu-id="3e6f6-131">Для реализации интерфейса [**иобжектмоделпровидер**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) требуется следующий метод.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-131">The following method is required for implementing the [**IObjectModelProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iobjectmodelprovider) interface.</span></span>



| <span data-ttu-id="3e6f6-132">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="3e6f6-132">Required members</span></span>                                                                             | <span data-ttu-id="3e6f6-133">Тип члена</span><span class="sxs-lookup"><span data-stu-id="3e6f6-133">Member type</span></span> | <span data-ttu-id="3e6f6-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e6f6-134">Notes</span></span>                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e6f6-135">**жетундерлингобжектмодел**</span><span class="sxs-lookup"><span data-stu-id="3e6f6-135">**GetUnderlyingObjectModel**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iobjectmodelprovider-getunderlyingobjectmodel) | <span data-ttu-id="3e6f6-136">Метод</span><span class="sxs-lookup"><span data-stu-id="3e6f6-136">Method</span></span>      | <span data-ttu-id="3e6f6-137">Возвращает указатель COM на базовую объектную модель.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-137">Returns a COM pointer to the underlying object model.</span></span> <span data-ttu-id="3e6f6-138">Клиент должен вызвать метод [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения конкретных указателей на объектную модель.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-138">The client is expected to call the [**IUnknown::QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to retrieve specific object model pointers.</span></span> |



 

<span data-ttu-id="3e6f6-139">Этот шаблон элемента управления не имеет связанных событий.</span><span class="sxs-lookup"><span data-stu-id="3e6f6-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e6f6-140">См. также</span><span class="sxs-lookup"><span data-stu-id="3e6f6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e6f6-141">Типы элементов управления и поддерживаемые ими шаблоны элементов управления</span><span class="sxs-lookup"><span data-stu-id="3e6f6-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3e6f6-142">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3e6f6-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="3e6f6-143">Общие сведения о дереве модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="3e6f6-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 