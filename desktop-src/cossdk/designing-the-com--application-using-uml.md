---
description: Разработка успешного приложения COM+ требует архитектурного проектирования приложений.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Проектирование приложения COM+ с помощью UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423317"
---
# <a name="designing-the-com-application-using-uml"></a><span data-ttu-id="4c095-103">Проектирование приложения COM+ с помощью UML</span><span class="sxs-lookup"><span data-stu-id="4c095-103">Designing the COM+ Application Using UML</span></span>

<span data-ttu-id="4c095-104">Разработка успешного приложения COM+ требует архитектурного проектирования приложений.</span><span class="sxs-lookup"><span data-stu-id="4c095-104">Developing a successful COM+ application requires up-front application architectural design.</span></span> <span data-ttu-id="4c095-105">Язык UML (Unified Modeling Language) (UML) является ключом к разработке разработки.</span><span class="sxs-lookup"><span data-stu-id="4c095-105">The Unified Modeling Language (UML) is key to this design development.</span></span> <span data-ttu-id="4c095-106">UML — это нотация моделирования для данных и процессов приложений, которая сочетает в себе лучшие методики отрасли программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4c095-106">The UML is a modeling notation for application data and processes that combines the best practices of the software industry.</span></span> <span data-ttu-id="4c095-107">Поскольку UML разбивает приложение на три представления, отражающие приложение, а также его упаковку и реализацию, Нотация моделирования хорошо расширяется для поддержки моделирования предприятия.</span><span class="sxs-lookup"><span data-stu-id="4c095-107">Because the UML breaks the application into three views that reflect the application as well as its packaging and implementation, the modeling notation extends well to support enterprise modeling.</span></span>

<span data-ttu-id="4c095-108">UML-язык предназначен для трех представлений приложения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4c095-108">The UML addresses three views of the application, as follows:</span></span>

-   <span data-ttu-id="4c095-109">Статическое представление, которое моделируется информацией, полученной из пользовательских сценариев и схем классов.</span><span class="sxs-lookup"><span data-stu-id="4c095-109">The static view, which is modeled by information taken from user scenarios and class diagrams.</span></span>
-   <span data-ttu-id="4c095-110">Динамическое представление, смоделированное с помощью схем последовательности, совместной работы и перехода состояния.</span><span class="sxs-lookup"><span data-stu-id="4c095-110">The dynamic view, which is modeled using sequence, collaboration, and state transition diagrams.</span></span>
-   <span data-ttu-id="4c095-111">Функциональное представление, которое является более традиционным описательным описанием с использованием псевдокода и спецификаций.</span><span class="sxs-lookup"><span data-stu-id="4c095-111">The functional view, which is the more traditional descriptive narrative using pseudocode and specifications.</span></span>

<span data-ttu-id="4c095-112">Сведения для этих представлений можно собрать, выполнив три этапа проектирования, которые хорошо подходят для UML.</span><span class="sxs-lookup"><span data-stu-id="4c095-112">The information for these views can be gathered by following three design steps that work well with the UML.</span></span> <span data-ttu-id="4c095-113">Перед написанием одной строки кода необходимо создать следующие модели:</span><span class="sxs-lookup"><span data-stu-id="4c095-113">Before writing a single line of code, you need to create the following models:</span></span>

<dl> <dt>

<span data-ttu-id="4c095-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Концептуальная модель</span><span class="sxs-lookup"><span data-stu-id="4c095-114"><span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Conceptual model</span></span>
</dt> <dd>

<span data-ttu-id="4c095-115">Решите, какие компоненты и службы требуются.</span><span class="sxs-lookup"><span data-stu-id="4c095-115">Decide what components and services are required.</span></span>

</dd> <dt>

<span data-ttu-id="4c095-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Логическая модель</span><span class="sxs-lookup"><span data-stu-id="4c095-116"><span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Logical model</span></span>
</dt> <dd>

<span data-ttu-id="4c095-117">Определите, в каком логическом уровне структуры они принадлежат.</span><span class="sxs-lookup"><span data-stu-id="4c095-117">Determine which logical design tier they belong in.</span></span>

</dd> <dt>

<span data-ttu-id="4c095-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Физическая модель</span><span class="sxs-lookup"><span data-stu-id="4c095-118"><span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Physical model</span></span>
</dt> <dd>

<span data-ttu-id="4c095-119">Определите, где находятся компоненты физически и как они должны быть закодированы.</span><span class="sxs-lookup"><span data-stu-id="4c095-119">Determine where the components reside physically and how they are to be coded.</span></span>

</dd> </dl>

<span data-ttu-id="4c095-120">Затем эти модели можно использовать с инструментами вариантов на основе UML.</span><span class="sxs-lookup"><span data-stu-id="4c095-120">These models can then be used with UML-based CASE tools.</span></span> <span data-ttu-id="4c095-121">Дополнительные сведения об этих трех моделях проектирования см. в следующих подразделах этого раздела:</span><span class="sxs-lookup"><span data-stu-id="4c095-121">For more information on these three design models, see the following topics in this section:</span></span>

-   [<span data-ttu-id="4c095-122">Концептуальная модель: требования к приложениям</span><span class="sxs-lookup"><span data-stu-id="4c095-122">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
-   [<span data-ttu-id="4c095-123">Логическая модель: определение приложения и планирование</span><span class="sxs-lookup"><span data-stu-id="4c095-123">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
-   [<span data-ttu-id="4c095-124">Физическая модель: архитектура приложения</span><span class="sxs-lookup"><span data-stu-id="4c095-124">The Physical Model: Application Architecture</span></span>](the-physical-model--application-architecture.md)

## <a name="related-topics"></a><span data-ttu-id="4c095-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4c095-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c095-126">Предположения и принципы разработки COM+</span><span class="sxs-lookup"><span data-stu-id="4c095-126">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="4c095-127">Общие рекомендации по проектированию для использования COM+</span><span class="sxs-lookup"><span data-stu-id="4c095-127">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="4c095-128">Оптимизация взаимодействия с уровнем бизнес-логики COM+</span><span class="sxs-lookup"><span data-stu-id="4c095-128">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[<span data-ttu-id="4c095-129">Другие средства Майкрософт для создания распределенных приложений</span><span class="sxs-lookup"><span data-stu-id="4c095-129">Other Microsoft Tools for Building Distributed Applications</span></span>](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



