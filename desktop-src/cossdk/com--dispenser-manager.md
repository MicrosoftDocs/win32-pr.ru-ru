---
description: Диспетчер распределителя предоставляет пулы ресурсов для распределительов ресурсов и гарантирует, что ресурс, предоставленный распределителем ресурсов, будет правильно прикреплен в транзакции объектов приложения.
ms.assetid: c8986943-56a1-4668-9e80-7ab2a42333a8
title: Диспетчер распределителя COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2422b7debb8ee12ed97444f3b16f31e663e1e71
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538837"
---
# <a name="com-dispenser-manager"></a><span data-ttu-id="58860-103">Диспетчер распределителя COM+</span><span class="sxs-lookup"><span data-stu-id="58860-103">COM+ Dispenser Manager</span></span>

<span data-ttu-id="58860-104">Диспетчер распределителя предоставляет пулы ресурсов для распределителя ресурсов и гарантирует, что ресурс, предоставленный распределителем ресурсов, будет правильно прикреплен к транзакции объекта приложения.</span><span class="sxs-lookup"><span data-stu-id="58860-104">The dispenser manager provides resource pooling for the resource dispensers and ensures that a resource supplied by a resource dispenser is correctly enlisted in the application object's transaction.</span></span> <span data-ttu-id="58860-105">Диспетчер распределителя ресурсов автоматически освобождает ресурсы, которые еще зарезервированы в конце времени существования объекта, устраняя вероятность утечки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58860-105">The dispenser manager automatically reclaims resources that are still reserved at the end of an object's lifetime, eliminating the possibility of resource "leaks."</span></span> <span data-ttu-id="58860-106">Диспетчер распределителя может попросить распределителя ресурсов создать новый ресурс или удалить бездействующие ресурсы при необходимости для настройки уровней инвентаризации вместо использования статических параметров.</span><span class="sxs-lookup"><span data-stu-id="58860-106">The dispenser manager can ask a resource dispenser to create a new resource or to destroy idle resources when necessary to adjust inventory levels, rather than using static settings.</span></span>

> [!Note]  
> <span data-ttu-id="58860-107">Так как интерфейсы распределителя ресурсов, предоставляемые приложению, не должны быть COM-интерфейсами, диспетчер распределителя можно использовать в процессе без инициализации COM, например для поддержки распределителя ресурсов ODBC.</span><span class="sxs-lookup"><span data-stu-id="58860-107">Because resource dispenser interfaces exposed to the application are not required to be COM interfaces, the dispenser manager can be used in a process without initializing COM, for example, to support the ODBC resource dispenser.</span></span>

 

<span data-ttu-id="58860-108">При создании ресурса распределитель ресурсов может указать время, в течение которого бездействующий ресурс будет оставаться в пуле до его уничтожения.</span><span class="sxs-lookup"><span data-stu-id="58860-108">Upon resource creation, the resource dispenser may specify how long an idle resource is allowed to remain in the pool before it's destroyed.</span></span> <span data-ttu-id="58860-109">Поток, выполняемый в диспетчере распределителя, всегда ищет эти бездействующие ресурсы.</span><span class="sxs-lookup"><span data-stu-id="58860-109">A thread that runs in the dispenser manager is always looking for these idle resources.</span></span>

## <a name="the-inventory-statistics-manager"></a><span data-ttu-id="58860-110">Диспетчер статистики инвентаризации</span><span class="sxs-lookup"><span data-stu-id="58860-110">The Inventory Statistics Manager</span></span>

<span data-ttu-id="58860-111">Диспетчер распределителя использует *Диспетчер статистики инвентаризации* для управления уровнями инвентаризации ресурсов пула.</span><span class="sxs-lookup"><span data-stu-id="58860-111">The dispenser manager uses the *inventory statistics manager* to manage pool resource inventory levels.</span></span> <span data-ttu-id="58860-112">Диспетчер статистики инвентаризации ведет запись о том, когда используется каждый ресурс, и удаляет ресурсы из инвентаризации, если они не использовались в течение *x* секунд, где значение *x* задается для каждого ресурса при создании ресурса.</span><span class="sxs-lookup"><span data-stu-id="58860-112">The inventory statistics manager maintains a record of when each resource was used and removes resources from inventory when they have not been used for *x* seconds, where the value of *x* is set per resource when the resource is created.</span></span>

## <a name="the-holder-component"></a><span data-ttu-id="58860-113">Компонент держателя</span><span class="sxs-lookup"><span data-stu-id="58860-113">The Holder Component</span></span>

<span data-ttu-id="58860-114">Диспетчер распределителя опрашивает каждый *держатель*, компонент, созданный диспетчером распределителя, который выводит список инвентаризации ресурсов для каждого распределителя ресурсов каждые 10 секунд, что позволяет изменять их инвентаризацию.</span><span class="sxs-lookup"><span data-stu-id="58860-114">The dispenser manager polls each *holder*, a component created by the dispenser manager that lists the resource inventory for each resource dispenser, every 10 seconds to allow it to readjust its resource inventory.</span></span> <span data-ttu-id="58860-115">Каждый держатель вызывает диспетчер статистики инвентаризации, чтобы предложить уровни инвентаризации для каждого типа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58860-115">Each holder calls the inventory statistics manager to suggest inventory levels for each type of resource.</span></span> <span data-ttu-id="58860-116">В результате держатель может попросить распределителя ресурсов создать или уничтожить некоторые запасы.</span><span class="sxs-lookup"><span data-stu-id="58860-116">As a result, the holder may ask the resource dispenser to either create or destroy some inventory.</span></span>

<span data-ttu-id="58860-117">Держатель владельца и ресурса взаимодействует с запросами ресурсов определенного типа.</span><span class="sxs-lookup"><span data-stu-id="58860-117">The holder and resource dispenser communicate to request resources of a particular type.</span></span> <span data-ttu-id="58860-118">Между владельцем и распределителем ресурсов существуют следующие связи:</span><span class="sxs-lookup"><span data-stu-id="58860-118">The following relationships exist between the holder and resource dispenser:</span></span>

-   <span data-ttu-id="58860-119">Держатель может запросить ресурс от распределителя ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58860-119">The holder can request a resource from the resource dispenser.</span></span> <span data-ttu-id="58860-120">Распределитель ресурсов либо возвращает доступный ресурс, либо создает новый.</span><span class="sxs-lookup"><span data-stu-id="58860-120">The resource dispenser either returns an available resource or creates a new one.</span></span>
-   <span data-ttu-id="58860-121">Владелец может уведомить распределитель ресурсов о том, что приложению больше не требуется ресурс, а затем вернуть его в пул ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58860-121">The holder can notify the resource dispenser that an application no longer needs a resource and then return it to the resource pool.</span></span>
-   <span data-ttu-id="58860-122">Владелец и распределитель ресурсов работают вместе для поддержания размера пула ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58860-122">The holder and the resource dispenser work together to maintain the size of the resource pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58860-123">См. также</span><span class="sxs-lookup"><span data-stu-id="58860-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58860-124">Основные понятия распределителя ресурсов COM+</span><span class="sxs-lookup"><span data-stu-id="58860-124">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



