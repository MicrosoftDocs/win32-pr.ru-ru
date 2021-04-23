---
title: Шаблон элемента управления Синчронизединпут
description: Описывает правила и соглашения для реализации Исинчронизединпутпровидер, включая сведения о свойствах и методах.
ms.assetid: 3e2d65ea-8093-4e65-b43e-28478ec74607
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Синчронизединпут
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Синчронизединпут
- Модель автоматизации пользовательского интерфейса, Исинчронизединпутпровидер
- ISynchronizedInputProvider
- реализация шаблонов элементов управления Синчронизединпут модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Синчронизединпут
- шаблоны элементов управления, Исинчронизединпутпровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Синчронизединпут
- шаблоны элементов управления, Синчронизединпут
- интерфейсы, Исинчронизединпутпровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 105e75163fdac742adaad6b778c251b4b7b8ae70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700641"
---
# <a name="synchronizedinput-control-pattern"></a><span data-ttu-id="40e3f-113">Шаблон элемента управления Синчронизединпут</span><span class="sxs-lookup"><span data-stu-id="40e3f-113">SynchronizedInput Control Pattern</span></span>

<span data-ttu-id="40e3f-114">Описывает правила и соглашения для реализации [**исинчронизединпутпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), включая сведения о свойствах и методах.</span><span class="sxs-lookup"><span data-stu-id="40e3f-114">Describes guidelines and conventions for implementing [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider), including information about properties and methods.</span></span> <span data-ttu-id="40e3f-115">Шаблон элемента управления **синчронизединпут** позволяет клиентским приложениям автоматизации пользовательского интерфейса Майкрософт направлять ввод мыши или клавиатуры в конкретный элемент пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="40e3f-115">The **SynchronizedInput** control pattern enables Microsoft UI Automation client applications to direct the mouse or keyboard input to a specific UI element.</span></span>

<span data-ttu-id="40e3f-116">Этот шаблон элемента управления обычно используется в скриптах автоматизированного теста для отправки ввода с клавиатуры или мыши в конкретный элемент пользовательского интерфейса, а затем для проверки того, что элемент получил входные данные.</span><span class="sxs-lookup"><span data-stu-id="40e3f-116">This control pattern is typically used in automated test scripts to send mouse or keyboard input to a specific user-interface element, and then verify that the element received the input.</span></span>

<span data-ttu-id="40e3f-117">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="40e3f-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="40e3f-118">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="40e3f-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="40e3f-119">Обязательные члены для **исинчронизединпутпровидер**</span><span class="sxs-lookup"><span data-stu-id="40e3f-119">Required Members for **ISynchronizedInputProvider**</span></span>](#required-members-for-isynchronizedinputprovider)
-   [<span data-ttu-id="40e3f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="40e3f-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="40e3f-121">Правила и соглашения реализации</span><span class="sxs-lookup"><span data-stu-id="40e3f-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="40e3f-122">При реализации шаблона элемента управления **синчронизединпут** Обратите внимание на следующие правила и соглашения.</span><span class="sxs-lookup"><span data-stu-id="40e3f-122">When implementing the **SynchronizedInput** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="40e3f-123">При вызове метода [**исинчронизединпутпровидер:: стартлистенинг**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) поставщик автоматизации пользовательского интерфейса должен начать проверку входных данных указанного типа, а затем выполнить одно из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="40e3f-123">When the [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) method is called, the UI Automation provider should start checking for input of the specified type, and then take one of the following actions:</span></span>
    -   <span data-ttu-id="40e3f-124">При обнаружении совпадающих входных данных для элемента поставщик должен вызвать событие [**UIA \_ инпутреачедтаржетевентид**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="40e3f-124">When matching input is found for the element, the provider should raise the [**UIA\_InputReachedTargetEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="40e3f-125">При обнаружении совпадающих входных данных, но при достижении другого элемента поставщик должен вызвать событие [**UIA \_ инпутреачедосерелементевентид**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="40e3f-125">When matching input is found, but it reached a different element, the provider should raise the [**UIA\_InputReachedOtherElementEventId**](uiauto-event-ids.md) event.</span></span>
    -   <span data-ttu-id="40e3f-126">При обнаружении несовпадающих входных данных поставщик должен отменить входные данные и вызвать событие [**UIA \_ инпутдискардедевентид**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="40e3f-126">When mismatched input is found, the provider should discard the input and raise the [**UIA\_InputDiscardedEventId**](uiauto-event-ids.md) event.</span></span>
-   <span data-ttu-id="40e3f-127">Поставщик автоматизации пользовательского интерфейса должен отбросить ввод, если он предназначен для элемента, отличного от текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="40e3f-127">The UI Automation provider must discard the input if it is for an element other than the current element.</span></span>
-   <span data-ttu-id="40e3f-128">Когда элемент получает входные данные или вызывается метод [**исинчронизединпутпровидер:: Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) , поставщик прекращает проверку входных данных и переходит в нормальное состояние.</span><span class="sxs-lookup"><span data-stu-id="40e3f-128">When the element receives the input, or when the [**ISynchronizedInputProvider::Cancel**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel) method is called, the provider stops checking input and continues as normal.</span></span>
-   <span data-ttu-id="40e3f-129">Если метод [**исинчронизединпутпровидер:: стартлистенинг**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) вызывается, когда поставщик уже прослушивает входные данные, поставщик должен вернуть [**UIA \_ E \_ INVALIDOPERATION**](uiauto-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="40e3f-129">If [**ISynchronizedInputProvider::StartListening**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening) is called when the provider is already listening for input, the provider should return [**UIA\_E\_INVALIDOPERATION**](uiauto-error-codes.md).</span></span>

## <a name="required-members-for-isynchronizedinputprovider"></a><span data-ttu-id="40e3f-130">Обязательные члены для **исинчронизединпутпровидер**</span><span class="sxs-lookup"><span data-stu-id="40e3f-130">Required Members for **ISynchronizedInputProvider**</span></span>

<span data-ttu-id="40e3f-131">Для реализации интерфейса [**исинчронизединпутпровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) требуются следующие свойства, методы и события.</span><span class="sxs-lookup"><span data-stu-id="40e3f-131">The following properties, methods, and events are required for implementing the [**ISynchronizedInputProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-isynchronizedinputprovider) interface.</span></span>



| <span data-ttu-id="40e3f-132">Обязательные члены</span><span class="sxs-lookup"><span data-stu-id="40e3f-132">Required members</span></span>                                                                         | <span data-ttu-id="40e3f-133">Тип члена</span><span class="sxs-lookup"><span data-stu-id="40e3f-133">Member type</span></span> | <span data-ttu-id="40e3f-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="40e3f-134">Notes</span></span> |
|------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="40e3f-135">**стартлистенинг**</span><span class="sxs-lookup"><span data-stu-id="40e3f-135">**StartListening**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-startlistening)               | <span data-ttu-id="40e3f-136">Метод</span><span class="sxs-lookup"><span data-stu-id="40e3f-136">Method</span></span>      | <span data-ttu-id="40e3f-137">Нет</span><span class="sxs-lookup"><span data-stu-id="40e3f-137">None</span></span>  |
| [<span data-ttu-id="40e3f-138">**Отменить**</span><span class="sxs-lookup"><span data-stu-id="40e3f-138">**Cancel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-isynchronizedinputprovider-cancel)                               | <span data-ttu-id="40e3f-139">Метод</span><span class="sxs-lookup"><span data-stu-id="40e3f-139">Method</span></span>      | <span data-ttu-id="40e3f-140">Нет</span><span class="sxs-lookup"><span data-stu-id="40e3f-140">None</span></span>  |
| [<span data-ttu-id="40e3f-141">**UIA \_ инпутреачедтаржетевентид**</span><span class="sxs-lookup"><span data-stu-id="40e3f-141">**UIA\_InputReachedTargetEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="40e3f-142">Событие</span><span class="sxs-lookup"><span data-stu-id="40e3f-142">Event</span></span>       | <span data-ttu-id="40e3f-143">Нет</span><span class="sxs-lookup"><span data-stu-id="40e3f-143">None</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="40e3f-144">См. также</span><span class="sxs-lookup"><span data-stu-id="40e3f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40e3f-145">Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="40e3f-145">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




