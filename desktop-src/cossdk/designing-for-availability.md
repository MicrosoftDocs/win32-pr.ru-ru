---
description: Доступность — это способность приложения допускать сбои в ресурсах сервера.
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: Проектирование для обеспечения доступности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538813"
---
# <a name="designing-for-availability"></a><span data-ttu-id="60324-103">Проектирование для обеспечения доступности</span><span class="sxs-lookup"><span data-stu-id="60324-103">Designing for Availability</span></span>

<span data-ttu-id="60324-104">Доступность — это способность приложения допускать сбои в ресурсах сервера.</span><span class="sxs-lookup"><span data-stu-id="60324-104">Availability is the ability of an application to tolerate failures in server resources.</span></span> <span data-ttu-id="60324-105">Это означает, что клиент по-своему будет обрабатываться с ошибкой, и в идеале этот сбой прозрачен для клиента.</span><span class="sxs-lookup"><span data-stu-id="60324-105">This means that the client continues to be served through the failure and that, ideally, the failure is transparent to the client.</span></span> <span data-ttu-id="60324-106">Очевидно, что сбой может происходить из аппаратных или программных источников, поэтому необходимо разработать оба варианта.</span><span class="sxs-lookup"><span data-stu-id="60324-106">Obviously, the failure can come from either hardware or software sources, so you must develop for both cases.</span></span>

<span data-ttu-id="60324-107">На доступность могут влиять следующие факторы.</span><span class="sxs-lookup"><span data-stu-id="60324-107">Availability can be affected by the following factors:</span></span>

-   <span data-ttu-id="60324-108">Модель приложения.</span><span class="sxs-lookup"><span data-stu-id="60324-108">Application model.</span></span> <span data-ttu-id="60324-109">Для обеспечения наивысшей доступности убедитесь, что критическая логика приложения выполняется с помощью службы [транзакций COM+](com--transactions.md) .</span><span class="sxs-lookup"><span data-stu-id="60324-109">For highest availability, ensure that the critical application logic is conducted using the [COM+ transactions](com--transactions.md) service.</span></span> <span data-ttu-id="60324-110">Кроме того, использование механизма компенсации может быть эффективным, чтобы ресурсы оставались в работоспособном состоянии после сбоев.</span><span class="sxs-lookup"><span data-stu-id="60324-110">In addition, using a compensation mechanism can be effective in ensuring that resources remain in a healthy state after failures.</span></span>
-   <span data-ttu-id="60324-111">Клиентская модель.</span><span class="sxs-lookup"><span data-stu-id="60324-111">Client model.</span></span> <span data-ttu-id="60324-112">Интегрируйте логику повторных попыток в клиентское приложение и стремитесь к постепенному снижению производительности приложения, если ресурсы или службы недоступны.</span><span class="sxs-lookup"><span data-stu-id="60324-112">Integrate "retry on failure" logic into the client application, and strive for a graceful degradation in the application if resources or services are unavailable.</span></span> <span data-ttu-id="60324-113">Узнайте, что клиент ожидает от приложения, и создайте конструкцию, которая позволяет альтернативам при возникновении сбоя.</span><span class="sxs-lookup"><span data-stu-id="60324-113">Understand what the client is expecting from the application, and create a design that allows for alternatives when a failure occurs.</span></span>
-   <span data-ttu-id="60324-114">Доступность данных и состояния.</span><span class="sxs-lookup"><span data-stu-id="60324-114">Data/state availability.</span></span> <span data-ttu-id="60324-115">Для обеспечения единообразного доступа к постоянным данным используйте кластеризацию Windows, чтобы обеспечить поддержку отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="60324-115">For consistent access to persistent data, use Windows Clustering to provide failover support.</span></span>
-   <span data-ttu-id="60324-116">Доступность службы.</span><span class="sxs-lookup"><span data-stu-id="60324-116">Service availability.</span></span> <span data-ttu-id="60324-117">Балансировку сетевой нагрузки можно использовать для балансировки нагрузки входящих IP-запросов в кластере серверов.</span><span class="sxs-lookup"><span data-stu-id="60324-117">You can use Network Load Balancing to load balance incoming IP requests across a cluster of servers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60324-118">См. также</span><span class="sxs-lookup"><span data-stu-id="60324-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60324-119">Проектирование для развертывания</span><span class="sxs-lookup"><span data-stu-id="60324-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="60324-120">Проектирование для масштабируемости</span><span class="sxs-lookup"><span data-stu-id="60324-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="60324-121">Разработка для обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="60324-121">Designing for Security</span></span>](designing-for-security.md)
</dt> </dl>

 

 



