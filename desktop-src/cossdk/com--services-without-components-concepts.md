---
description: В COM+ 1,5 введена возможность использования служб COM+ без компонентов.
ms.assetid: da93d164-234a-4d1e-b82c-f3f904bb8cb6
title: Службы COM+ без компонентов концепции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d692657d33143b9437a9c8134260a8c32431cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896322"
---
# <a name="com-services-without-components-concepts"></a><span data-ttu-id="efb04-103">Службы COM+ без компонентов концепции</span><span class="sxs-lookup"><span data-stu-id="efb04-103">COM+ Services Without Components Concepts</span></span>

<span data-ttu-id="efb04-104">В COM+ 1,5 введена возможность использования служб COM+ без компонентов.</span><span class="sxs-lookup"><span data-stu-id="efb04-104">COM+ 1.5 introduces the ability to use COM+ services without components.</span></span> <span data-ttu-id="efb04-105">Это значительно снижает затраты на производительность при использовании служб COM+ из среды, которая не использует компоненты, а также исключает сложность использования этих служб.</span><span class="sxs-lookup"><span data-stu-id="efb04-105">This significantly reduces the performance costs when using COM+ services from an environment that doesn't use components, and it also eliminates the complexity of using these services.</span></span> <span data-ttu-id="efb04-106">Начиная с IIS 6,0, IIS и ASP пользуются преимуществами использования служб COM+ без компонентов.</span><span class="sxs-lookup"><span data-stu-id="efb04-106">Beginning with IIS 6.0, IIS and ASP take advantage of using COM+ services without components.</span></span>

<span data-ttu-id="efb04-107">Изначально службы COM+ предназначены для использования с компонентами COM+.</span><span class="sxs-lookup"><span data-stu-id="efb04-107">COM+ services were originally designed to be used with COM+ components.</span></span> <span data-ttu-id="efb04-108">Однако некоторые среды программирования не основаны на компонентах, поэтому для использования служб COM+ требуются значительные издержки.</span><span class="sxs-lookup"><span data-stu-id="efb04-108">However, some programming environments are not component-based and therefore required substantial overhead to use COM+ services.</span></span> <span data-ttu-id="efb04-109">Например, до выпуска COM+ 1,5 службам IIS пришлось создавать объекты оболочки только для того, чтобы иметь возможность использовать службы транзакций COM+ на страницах ASP.</span><span class="sxs-lookup"><span data-stu-id="efb04-109">For example, before the release of COM+ 1.5, IIS had to create shim objects solely to be able to use COM+ transaction services in ASP pages.</span></span> <span data-ttu-id="efb04-110">Затраты на производительность, основанные на создании этих объектов, включают хранение данных конфигурации как в метабазе IIS, так и в базе данных регистрации COM+ (Регдб), а также дополнительный обмен данными между метабазой IIS и Регдб COM+, необходимый для эффективного управления данными конфигурации.</span><span class="sxs-lookup"><span data-stu-id="efb04-110">The performance costs that come from creating those objects include storing the configuration data in both the IIS metabase and the COM+ registration database (RegDB) as well as the extra communication between the IIS metabase and the COM+ RegDB that is needed to effectively manage the configuration data.</span></span>

<span data-ttu-id="efb04-111">Если службам IIS требуется использовать вторую службу COM+, например синхронизацию, для этого пришлось создать совершенно другой объект оболочки.</span><span class="sxs-lookup"><span data-stu-id="efb04-111">If IIS needed to use a second COM+ service, such as synchronization, it had to create a completely different shim object to do so.</span></span> <span data-ttu-id="efb04-112">Чтобы использовать транзакции и синхронизацию COM+, потребуется третий тип объекта оболочки совместимости.</span><span class="sxs-lookup"><span data-stu-id="efb04-112">To use both COM+ transactions and synchronization, a third type of shim object would be needed.</span></span> <span data-ttu-id="efb04-113">Сложность этого подхода масштабируется как O (N2), что делает реализацию новых служб чрезвычайно сложной.</span><span class="sxs-lookup"><span data-stu-id="efb04-113">The complexity of this approach scales as O(n2), making the implementation of new services extremely difficult.</span></span>

<span data-ttu-id="efb04-114">С появлением служб COM+ без компонентов, необходимые службы настраиваются с помощью объекта, созданного из класса.</span><span class="sxs-lookup"><span data-stu-id="efb04-114">With the introduction of COM+ services without components, the services that are needed are configured through an object instantiated from the class.</span></span> <span data-ttu-id="efb04-115">Класс [**ксервицеконфиг**](cserviceconfig.md) реализует интерфейсы, необходимые для настройки различных служб, обеспечивая гибкость для поддержки нескольких служб одновременно и возможность поддержки новых служб в будущем.</span><span class="sxs-lookup"><span data-stu-id="efb04-115">The [**CServiceConfig**](cserviceconfig.md) class implements the interfaces needed to configure the different services while providing the flexibility to support multiple services at the same time and the ability to support new services in the future.</span></span>

<span data-ttu-id="efb04-116">Затем настроенные службы можно использовать с помощью двух разных механизмов: они могут использоваться с помощью функции [**кокреатеактивити**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) , которая применяет службы ко всей работе, переданной функцией, и также может использоваться путем внедрения работы, которая использует службы между вызовами функций [**коентерсервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) и [**колеавесервицедомаин**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) .</span><span class="sxs-lookup"><span data-stu-id="efb04-116">The configured services can then be used through two different mechanisms: They can be used through the [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) function, which applies the services to all of the work submitted via the activity that is created by the function, and they can also be used by embedding the work that uses the services between calls to the [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) and [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) functions.</span></span> <span data-ttu-id="efb04-117">Ни одна из этих функций не требует создания новых компонентов, чтобы иметь возможность использовать службы COM+. требуется только объект [**ксервицеконфиг**](cserviceconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="efb04-117">None of these functions requires the creation of any new components to be able to use the COM+ services; only the [**CServiceConfig**](cserviceconfig.md) object is needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efb04-118">См. также</span><span class="sxs-lookup"><span data-stu-id="efb04-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efb04-119">Задачи служб COM+ без компонентов</span><span class="sxs-lookup"><span data-stu-id="efb04-119">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)
</dt> </dl>

 

 



