---
description: Группировка объектов в пул — это автоматическая служба, предоставляемая COM+, которая позволяет настроить компонент для сохранения активных экземпляров в пуле, готовых к использованию любым клиентом, запрашивающим этот компонент.
ms.assetid: 74a45220-449a-4d89-a979-a206e5e3d3ad
title: Основные понятия пула объектов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb2aa6481b2493371801d0d274420d356b0a32e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423282"
---
# <a name="com-object-pooling-concepts"></a><span data-ttu-id="9ff1b-103">Основные понятия пула объектов COM+</span><span class="sxs-lookup"><span data-stu-id="9ff1b-103">COM+ Object Pooling Concepts</span></span>

<span data-ttu-id="9ff1b-104">Группировка объектов в пул — это автоматическая служба, предоставляемая COM+, которая позволяет настроить компонент для сохранения активных экземпляров в пуле, готовых к использованию любым клиентом, запрашивающим этот компонент.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-104">Object pooling is an automatic service provided by COM+ that enables you to configure a component to have instances of itself kept active in a pool, ready to be used by any client that requests the component.</span></span> <span data-ttu-id="9ff1b-105">Можно выполнять административную настройку и мониторинг пула, поддерживаемого для данного компонента, указывая такие характеристики, как размер пула и время ожидания запроса на создание.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-105">You can administratively configure and monitor the pool maintained for a given component, specifying characteristics such as pool size and creation request time-out values.</span></span> <span data-ttu-id="9ff1b-106">Когда приложение выполняется, COM+ управляет пулом, обрабатывая сведения об активации и повторном использовании объектов в соответствии с заданными критериями.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-106">When the application is running, COM+ manages the pool for you, handling the details of object activation and reuse according to the criteria you have specified.</span></span>

<span data-ttu-id="9ff1b-107">Вы можете добиться очень значительных преимуществ производительности и масштабирования, используя объекты таким образом, особенно при написании, чтобы воспользоваться всеми преимуществами повторного использования.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-107">You can achieve very significant performance and scaling benefits by reusing objects in this manner, particularly when they are written to take full advantage of reuse.</span></span> <span data-ttu-id="9ff1b-108">При использовании пула объектов вы получаете следующие преимущества:</span><span class="sxs-lookup"><span data-stu-id="9ff1b-108">With object pooling, you gain the following benefits:</span></span>

-   <span data-ttu-id="9ff1b-109">Вы можете ускорить использование объектов для каждого клиента, разделять время на инициализацию и получение ресурсов от реальной работы, выполняемой объектом для клиентов.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-109">You can speed object use time for each client, factoring out time-consuming initialization and resource acquisition from the actual work that the object performs for clients.</span></span>
-   <span data-ttu-id="9ff1b-110">Вы можете поделиться затратами на приобретение дорогостоящих ресурсов для всех клиентов.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-110">You can share the cost of acquiring expensive resources across all clients.</span></span>
-   <span data-ttu-id="9ff1b-111">Вы можете предварительно распределять объекты при запуске приложения, прежде чем поступать в клиентские запросы.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-111">You can pre-allocate objects when the application starts, before any client requests come in.</span></span>
-   <span data-ttu-id="9ff1b-112">Вы можете управлять использованием ресурсов с помощью управления административным пулом, например, установив соответствующий максимальный уровень пула, можно оставаться открытым только столько подключений к базам данных, сколько есть лицензия.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-112">You can govern resource use with administrative pool management for example, by setting an appropriate maximum pool level, you can keep open only as many database connections as you have a license for.</span></span>
-   <span data-ttu-id="9ff1b-113">Вы можете административно настроить пулы, чтобы воспользоваться преимуществами доступных аппаратных ресурсов, можно легко настроить конфигурацию пула по мере изменения доступных ресурсов оборудования.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-113">You can administratively configure pooling to take best advantage of available hardware resources you can easily adjust the pool configuration as available hardware resources change.</span></span>
-   <span data-ttu-id="9ff1b-114">Время повторной активации можно ускорить для объектов, использующих [JIT-активацию](com--just-in-time-activation.md), и намеренно управлять выделением ресурсов для клиентов.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-114">You can speed reactivation time for objects that use [just-in-time (JIT) activation](com--just-in-time-activation.md), while deliberately controlling how resources are dedicated to clients.</span></span>

## <a name="writing-poolable-objects"></a><span data-ttu-id="9ff1b-115">Запись объектов в пуле</span><span class="sxs-lookup"><span data-stu-id="9ff1b-115">Writing Poolable Objects</span></span>

<span data-ttu-id="9ff1b-116">Объекты, которые могут быть объединены в пул, должны отвечать определенным требованиям, чтобы обеспечить использование одного экземпляра объекта несколькими клиентами.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-116">Poolable objects must meet certain requirements to enable a single object instance to be used by multiple clients.</span></span> <span data-ttu-id="9ff1b-117">Например, они не могут удерживать состояние клиента или иметь сходство потоков.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-117">For example, they can't hold client state or have any thread affinity.</span></span> <span data-ttu-id="9ff1b-118">Транзакционные объекты также имеют определенные требования, в то же, что управляемые ресурсы, удерживаемые объектом poold, должны прикрепляться к транзакции вручную.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-118">Transactional objects also have particular requirements, in that managed resources held by a pooled object must be manually enlisted in a transaction.</span></span>

<span data-ttu-id="9ff1b-119">Объекты в составе пула могут реализовывать [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) , чтобы контролировать их повторное использование.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-119">Pooled objects can implement [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) to control how they are reused.</span></span> <span data-ttu-id="9ff1b-120">Это позволяет выполнять инициализацию при активации в заданном контексте, очищать состояние клиента при деактивации и указывать, когда они находятся в непригодном для использования состоянии.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-120">This enables them to perform initialization when activated in a given context, to clean up any client state on deactivation, and to indicate when they are in a non-reusable state.</span></span>

<span data-ttu-id="9ff1b-121">Часто бывает полезно писать объекты poold довольно универсально, чтобы их можно было изменять с помощью строки конструктора.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-121">Often, it useful to write poolable objects in a somewhat generic fashion so that they can be administratively customized with a constructor string.</span></span> <span data-ttu-id="9ff1b-122">Например, объект может быть записан для хранения универсального соединения ODBC с определенным DSN, указанным администратором в строке конструктора.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-122">For example, an object might be written to hold a generic ODBC connection, with a particular DSN administratively specified in a constructor string.</span></span>

<span data-ttu-id="9ff1b-123">Подразделы этого раздела, описанные в следующей таблице, содержат сведения о том, как работает пул объектов в COM+, а также сведения о том, как создавать, настраивать и реализовывать объекты, доступные в пуле.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-123">The topics in this section, described in the following table, provide information about how object pooling works in COM+, as well as information about how to write, configure, and implement poolable objects.</span></span>



| <span data-ttu-id="9ff1b-124">Раздел</span><span class="sxs-lookup"><span data-stu-id="9ff1b-124">Topic</span></span>                                                                                                 | <span data-ttu-id="9ff1b-125">Описание</span><span class="sxs-lookup"><span data-stu-id="9ff1b-125">Description</span></span>                                                                                              |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ff1b-126">Как работает пул объектов</span><span class="sxs-lookup"><span data-stu-id="9ff1b-126">How Object Pooling Works</span></span>](how-object-pooling-works.md)<br/>                                   | <span data-ttu-id="9ff1b-127">Представляет основные понятия.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-127">Presents basic concepts.</span></span><br/>                                                                      |
| [<span data-ttu-id="9ff1b-128">Повышение производительности с помощью пула объектов</span><span class="sxs-lookup"><span data-stu-id="9ff1b-128">Improving Performance with Object Pooling</span></span>](improving-performance-with-object-pooling.md)<br/> | <span data-ttu-id="9ff1b-129">Содержит конкретные сведения о наиболее эффективном использовании пула объектов.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-129">Provides specific details on how you can use object pooling most effectively.</span></span><br/>                 |
| [<span data-ttu-id="9ff1b-130">Требования к объектам в пуле</span><span class="sxs-lookup"><span data-stu-id="9ff1b-130">Requirements for Poolable Objects</span></span>](requirements-for-poolable-objects.md)<br/>                 | <span data-ttu-id="9ff1b-131">Содержит сведения о том, как написать объект, который должен быть помещен в пул.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-131">Provides details on how to write an object that is to be pooled.</span></span><br/>                              |
| [<span data-ttu-id="9ff1b-132">Группирование транзакционных объектов в пул</span><span class="sxs-lookup"><span data-stu-id="9ff1b-132">Pooling Transactional Objects</span></span>](pooling-transactional-objects.md)<br/>                         | <span data-ttu-id="9ff1b-133">Предоставляет подробные сведения о специальных требованиях, применяемых к транзакционным объектам в пуле.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-133">Provides details about the special requirements that apply to poolable transactional objects.</span></span><br/> |
| [<span data-ttu-id="9ff1b-134">Управление временем существования и состоянием объекта</span><span class="sxs-lookup"><span data-stu-id="9ff1b-134">Controlling Object Lifetime and State</span></span>](controlling-object-lifetime-and-state.md)<br/>         | <span data-ttu-id="9ff1b-135">Описывает, как можно реализовать объекты в составе пула, чтобы контролировать их повторное использование.</span><span class="sxs-lookup"><span data-stu-id="9ff1b-135">Describes how pooled objects can be implemented to control how they are reused.</span></span><br/>               |



 

## <a name="related-topics"></a><span data-ttu-id="9ff1b-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9ff1b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ff1b-137">Задачи пула объектов COM+</span><span class="sxs-lookup"><span data-stu-id="9ff1b-137">COM+ Object Pooling Tasks</span></span>](com--object-pooling-tasks.md)
</dt> </dl>

 

 




