---
description: После завершения концептуальной и логической моделей можно принимать решения о физической реализации приложения.
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 'Физическая модель: архитектура приложения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142589"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="f0ba9-103">Физическая модель: архитектура приложения</span><span class="sxs-lookup"><span data-stu-id="f0ba9-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="f0ba9-104">После завершения концептуальной и логической моделей можно принимать решения о физической реализации приложения.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="f0ba9-105">Чтобы создать физическую модель, необходимо понять, где должны располагаться различные службы приложения и как они должны быть реализованы.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="f0ba9-106">Определение места, где должны находиться различные службы, перед реализацией служб.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="f0ba9-107">Одно из основных правил определения места существования различных служб: размещение компонента, где она используется.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="f0ba9-108">Если, например, компонент отображает сведения для базового клиента, он должен переключиться на компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="f0ba9-109">Если компонент проверяет сведения от базового клиента, он также должен находиться на компьютере базового клиента.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="f0ba9-110">Если компонент обновляет сведения в базе данных, он должен находиться на сервере базы данных.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="f0ba9-111">Конечно, есть и другие соображения, которые делают исключения из этого правила.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="f0ba9-112">Проблемы с производительностью и безопасностью также могут зависеть от того, где находится компонент.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="f0ba9-113">Рассмотрим следующий пример.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-113">Consider the following:</span></span>

-   <span data-ttu-id="f0ba9-114">Происходит ли частое изменение компонента, что усложняет распространение обновлений?</span><span class="sxs-lookup"><span data-stu-id="f0ba9-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="f0ba9-115">Будет ли компонент использоваться другими приложениями, такими как общий компонент проверки безопасности?</span><span class="sxs-lookup"><span data-stu-id="f0ba9-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="f0ba9-116">Создает ли компонент длительные вычисления или выполняет такие функции, как печать, которые можно разгрузить на сервер?</span><span class="sxs-lookup"><span data-stu-id="f0ba9-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="f0ba9-117">Можно ли улучшить безопасность компонента, поместив его на сервер?</span><span class="sxs-lookup"><span data-stu-id="f0ba9-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="f0ba9-118">Правильное размещение компонентов приложения также может изолировать команду разработчиков от дорогостоящих перекодирования при изменении системы или расположения данных.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="f0ba9-119">Например, размещение правил доступа к данным на уровне данных, а не в хранимых процедурах, упрощает изолированность приложения от зависимости от конкретной СУБД.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="f0ba9-120">Не только изменения являются ограниченными и тестируются подразделяется, но источники данных могут быть изменены, и данные могут быть распределены без фундаментального изменения приложения.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="f0ba9-121">Наконец, Поиск компонентов должен воспользоваться преимуществами повышения эффективности системы.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="f0ba9-122">Это время и экономичное размещение бизнес-объектов в централизованных расположениях в сети.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="f0ba9-123">Объекты могут совместно использоваться приложениями, а модульное тестирование можно выполнить до развертывания каких бы то ни было компонентов.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="f0ba9-124">Затраты на обслуживание также можно уменьшить, так как изменения правил происходят только в одной точке.</span><span class="sxs-lookup"><span data-stu-id="f0ba9-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0ba9-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f0ba9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0ba9-126">Концептуальная модель: требования к приложениям</span><span class="sxs-lookup"><span data-stu-id="f0ba9-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="f0ba9-127">Логическая модель: определение приложения и планирование</span><span class="sxs-lookup"><span data-stu-id="f0ba9-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



