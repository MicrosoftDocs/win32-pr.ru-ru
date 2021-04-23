---
description: COM+ управляет потоками. Каждый компонент COM имеет свойство ThreadingModel, которое можно указать при разработке компонента. Это свойство определяет, как объекты компонентов назначаются потокам для выполнения метода.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Атрибут модели потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423266"
---
# <a name="threading-model-attribute"></a><span data-ttu-id="703e5-105">Атрибут модели потоков</span><span class="sxs-lookup"><span data-stu-id="703e5-105">Threading Model Attribute</span></span>

<span data-ttu-id="703e5-106">COM+ управляет потоками.</span><span class="sxs-lookup"><span data-stu-id="703e5-106">COM+ manages threads for you.</span></span> <span data-ttu-id="703e5-107">Каждый компонент COM имеет свойство **ThreadingModel** , которое можно указать при разработке компонента.</span><span class="sxs-lookup"><span data-stu-id="703e5-107">Every COM component has a **ThreadingModel** property that you can specify when you develop the component.</span></span> <span data-ttu-id="703e5-108">Это свойство определяет, как объекты компонента назначаются потокам для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="703e5-108">This property determines how the component's objects are assigned to threads for method execution.</span></span>

<span data-ttu-id="703e5-109">Для просмотра свойства потоковой модели можно использовать средство администрирования "службы компонентов", щелкнув правой кнопкой мыши компонент в папке **компоненты** , выбрав пункт **свойства**, а затем перейдя на вкладку **параллелизм** . В рамках **потоковой модели** возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="703e5-109">You can use the Component Services administrative tool to view the threading-model property by right-clicking a component in the **Components** folder, clicking **Properties**, and then clicking the **Concurrency** tab. Under **Threading Model**, the possible values are as follows:</span></span>

-   <span data-ttu-id="703e5-110">**Контейнер основного потока**</span><span class="sxs-lookup"><span data-stu-id="703e5-110">**Main Thread Apartment**</span></span>
-   <span data-ttu-id="703e5-111">**Контейнер с одним потоком**</span><span class="sxs-lookup"><span data-stu-id="703e5-111">**Single Thread Apartment**</span></span>
-   <span data-ttu-id="703e5-112">**Контейнер свободных потоков**</span><span class="sxs-lookup"><span data-stu-id="703e5-112">**Free Thread Apartment**</span></span>
-   <span data-ttu-id="703e5-113">**Нейтральное подразделение**</span><span class="sxs-lookup"><span data-stu-id="703e5-113">**Neutral Apartment**</span></span>
-   <span data-ttu-id="703e5-114">**Любое подразделение**</span><span class="sxs-lookup"><span data-stu-id="703e5-114">**Any Apartment**</span></span>

<span data-ttu-id="703e5-115">Предпочтительная модель потоков для COM+ — это [нейтральное подразделение](neutral-apartments.md).</span><span class="sxs-lookup"><span data-stu-id="703e5-115">The preferred threading model for COM+ is the [neutral apartment](neutral-apartments.md).</span></span> <span data-ttu-id="703e5-116">Однако если не указать модель потоков для компонента, COM+ использует главный контейнер потока, который является значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="703e5-116">However, if you do not specify a threading model for your component, COM+ uses the main thread apartment, which is the default.</span></span>

> [!Note]  
> <span data-ttu-id="703e5-117">Более подробные сведения см. [в разделе Выбор модели потоков](/windows/desktop/com/choosing-the-threading-model).</span><span class="sxs-lookup"><span data-stu-id="703e5-117">For more detailed information, see [Choosing the Threading Model](/windows/desktop/com/choosing-the-threading-model).</span></span>

 

<span data-ttu-id="703e5-118">В следующей таблице показана модель программирования для апартаментов в COM+.</span><span class="sxs-lookup"><span data-stu-id="703e5-118">The following table shows the programming model for apartments in COM+.</span></span>



| <span data-ttu-id="703e5-119">Модель</span><span class="sxs-lookup"><span data-stu-id="703e5-119">Model</span></span>                     | <span data-ttu-id="703e5-120">Разделение</span><span class="sxs-lookup"><span data-stu-id="703e5-120">Apartment</span></span>                                                 | <span data-ttu-id="703e5-121">Бесплатный</span><span class="sxs-lookup"><span data-stu-id="703e5-121">Free</span></span>                               | <span data-ttu-id="703e5-122">Оба</span><span class="sxs-lookup"><span data-stu-id="703e5-122">Both</span></span>                               | <span data-ttu-id="703e5-123">нейтральное выражение.</span><span class="sxs-lookup"><span data-stu-id="703e5-123">Neutral</span></span>                      | <span data-ttu-id="703e5-124">Не указано</span><span class="sxs-lookup"><span data-stu-id="703e5-124">Not Specified</span></span>                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| <span data-ttu-id="703e5-125">С одним потоком, без Main</span><span class="sxs-lookup"><span data-stu-id="703e5-125">Single-threaded, not main</span></span> | <span data-ttu-id="703e5-126">Создано в текущем апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-126">Created in current apartment</span></span>                              | <span data-ttu-id="703e5-127">Создано в многопоточном подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-127">Created in multithreaded apartment</span></span> | <span data-ttu-id="703e5-128">Создано в текущем апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-128">Created in current apartment</span></span>       | <span data-ttu-id="703e5-129">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-129">Created in neutral apartment</span></span> | <span data-ttu-id="703e5-130">Создано в основном потоковом подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-130">Created in main threaded apartment</span></span> |
| <span data-ttu-id="703e5-131">Один поток, основной</span><span class="sxs-lookup"><span data-stu-id="703e5-131">Single-threaded, main</span></span>     | <span data-ttu-id="703e5-132">Создано в текущем апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-132">Created in current apartment</span></span>                              | <span data-ttu-id="703e5-133">Создано в многопоточном подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-133">Created in multithreaded apartment</span></span> | <span data-ttu-id="703e5-134">Создано в текущем апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-134">Created in current apartment</span></span>       | <span data-ttu-id="703e5-135">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-135">Created in neutral apartment</span></span> | <span data-ttu-id="703e5-136">Создано в текущем апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-136">Created in current apartment</span></span>       |
| <span data-ttu-id="703e5-137">Многопоточных</span><span class="sxs-lookup"><span data-stu-id="703e5-137">Multithreaded</span></span>             | <span data-ttu-id="703e5-138">Создано в однопотоковом апартаменте узла</span><span class="sxs-lookup"><span data-stu-id="703e5-138">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="703e5-139">Создано в многопоточном подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-139">Created in multithreaded apartment</span></span> | <span data-ttu-id="703e5-140">Создано в многопоточном подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-140">Created in multithreaded apartment</span></span> | <span data-ttu-id="703e5-141">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-141">Created in neutral apartment</span></span> | <span data-ttu-id="703e5-142">Создано в основном потоковом подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-142">Created in main threaded apartment</span></span> |
| <span data-ttu-id="703e5-143">Нейтральный (в потоке STA)</span><span class="sxs-lookup"><span data-stu-id="703e5-143">Neutral (on STA thread)</span></span>   | <span data-ttu-id="703e5-144">Создано в размещающем однопотоковое подразделение для этого потока</span><span class="sxs-lookup"><span data-stu-id="703e5-144">Created in host single-threaded apartment for this thread</span></span> | <span data-ttu-id="703e5-145">Создано в многопоточном подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-145">Created in multithreaded apartment</span></span> | <span data-ttu-id="703e5-146">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-146">Created in neutral apartment</span></span>       | <span data-ttu-id="703e5-147">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-147">Created in neutral apartment</span></span> | <span data-ttu-id="703e5-148">Создано в основном потоковом подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-148">Created in main threaded apartment</span></span> |
| <span data-ttu-id="703e5-149">Нейтральный (в потоке MTA)</span><span class="sxs-lookup"><span data-stu-id="703e5-149">Neutral (on MTA thread)</span></span>   | <span data-ttu-id="703e5-150">Создано в однопотоковом апартаменте узла</span><span class="sxs-lookup"><span data-stu-id="703e5-150">Created in host single-threaded apartment</span></span>                 | <span data-ttu-id="703e5-151">Создано в многопоточном подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-151">Created in multithreaded apartment</span></span> | <span data-ttu-id="703e5-152">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-152">Created in neutral apartment</span></span>       | <span data-ttu-id="703e5-153">Создано в нейтральном апартаменте</span><span class="sxs-lookup"><span data-stu-id="703e5-153">Created in neutral apartment</span></span> | <span data-ttu-id="703e5-154">Создано в основном потоковом подразделении</span><span class="sxs-lookup"><span data-stu-id="703e5-154">Created in main threaded apartment</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="703e5-155">См. также</span><span class="sxs-lookup"><span data-stu-id="703e5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="703e5-156">**ThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="703e5-156">**ThreadingModel**</span></span>](components.md)
</dt> </dl>

 

 
