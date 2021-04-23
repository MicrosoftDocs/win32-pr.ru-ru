---
description: Служба инструментирования COM+ позволяет создавать собственные программы управления событиями COM+ и ведения журналов, если требуется отобразить различные метрики производительности для компонентов COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Основные понятия инструментария COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710725"
---
# <a name="com-instrumentation-concepts"></a><span data-ttu-id="dcf42-103">Основные понятия инструментария COM+</span><span class="sxs-lookup"><span data-stu-id="dcf42-103">COM+ Instrumentation Concepts</span></span>

<span data-ttu-id="dcf42-104">Служба инструментирования COM+ позволяет создавать собственные программы управления событиями COM+ и ведения журналов, если требуется отобразить различные метрики производительности для компонентов COM+.</span><span class="sxs-lookup"><span data-stu-id="dcf42-104">The COM+ instrumentation service enables you to build your own COM+ event management and logging programs when you want to display various performance metrics for your COM+ components.</span></span> <span data-ttu-id="dcf42-105">Инструментирование COM+ можно также использовать для настройки пользовательских событий и для преобразования событий COM+ в формат анализатор Visual Studio (VSA) при обновлении пакетов MTS, получающих события MTS.</span><span class="sxs-lookup"><span data-stu-id="dcf42-105">COM+ instrumentation can also be used to configure user-defined events and to convert COM+ events to Visual Studio Analyzer (VSA) format when you are upgrading MTS packages that are receiving MTS events.</span></span>

> [!Note]  
> <span data-ttu-id="dcf42-106">Начиная с Windows Server 2003, только администраторы имеют права доступа на чтение журналов трассировки для системных событий.</span><span class="sxs-lookup"><span data-stu-id="dcf42-106">As of Windows Server 2003, only administrators have read access privileges to the trace logs for system events.</span></span>

 

<span data-ttu-id="dcf42-107">Подписавшись на события, опубликованные издателем системных событий, клиенты могут реализовать [интерфейсы инструментария com+](com--instrumentation-interfaces.md) для получения уведомлений для различных МЕТРИК производительности com+, таких как сведения об отдельных объектах com+, приложениях COM+ и службах com+.</span><span class="sxs-lookup"><span data-stu-id="dcf42-107">By subscribing to the events published by the system events publisher, clients can implement the [COM+ instrumentation interfaces](com--instrumentation-interfaces.md) to receive notifications for a variety of COM+ performance metrics, such as information about specific COM+ objects, COM+ applications, and COM+ services.</span></span> <span data-ttu-id="dcf42-108">Метрики публикуются на клиенте с помощью [службы событий COM+](com--events.md)— системы слабо связанных событий (лце), которая хранит сведения о событиях от разных издателей в хранилище событий в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="dcf42-108">The metrics are published to the client by using the [COM+ events service](com--events.md), a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.</span></span>

> [!Note]  
> <span data-ttu-id="dcf42-109">Инструментирование COM+ не гарантирует доставку события.</span><span class="sxs-lookup"><span data-stu-id="dcf42-109">COM+ instrumentation does not guarantee the delivery of an event.</span></span>

 

<span data-ttu-id="dcf42-110">Каждая метрика имеет метку времени, указывающую время создания метрики, а не время ее отправки или получения.</span><span class="sxs-lookup"><span data-stu-id="dcf42-110">Every metric has a timestamp that indicates the time when the metric was generated, not the time that it was dispatched or received.</span></span> <span data-ttu-id="dcf42-111">Клиент может сопоставить метку времени и узнать стоимость выполнения приложения COM+, стоимость транзакции, выполняемой в приложении COM+, или стоимость вызова метода внутри приложения COM+.</span><span class="sxs-lookup"><span data-stu-id="dcf42-111">The client can correlate the timestamp and find out the cost of running a COM+ application, the cost of a transaction executed inside a COM+ application, or the cost of a method call inside of a COM+ application.</span></span>

<span data-ttu-id="dcf42-112">Можно также использовать службу инструментария COM+ для фильтрации конкретных сведений о метриках производительности, которые необходимо просмотреть.</span><span class="sxs-lookup"><span data-stu-id="dcf42-112">You can also use the COM+ Instrumentation service to filter for the specific performance metrics information that you want to see.</span></span> <span data-ttu-id="dcf42-113">Например, при подписке на интерфейс или метод инструментария COM+ можно указать свойства для подписки в структуре [**комсвксевентинфо**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , например идентификатор приложения (элемент **ГУИДАПП** ) или идентификатор процесса (**двпид** Member).</span><span class="sxs-lookup"><span data-stu-id="dcf42-113">For example, when you subscribe to a COM+ instrumentation interface or method, you can specify properties for the subscription in the [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) structure, such as the application ID (**guidApp** member) or the process ID (**dwPid** member).</span></span>

<span data-ttu-id="dcf42-114">Если указан идентификатор приложения, вы получаете только метрики из указанного приложения.</span><span class="sxs-lookup"><span data-stu-id="dcf42-114">When the application ID is specified, you receive only the metrics from the specified application.</span></span> <span data-ttu-id="dcf42-115">Если указан идентификатор процесса, вы получаете метрики из указанного серверного приложения и библиотечных приложений, загруженных в этот процесс.</span><span class="sxs-lookup"><span data-stu-id="dcf42-115">When the process ID is specified, you receive metrics from the specified server application and library applications that are loaded in that process.</span></span> <span data-ttu-id="dcf42-116">Пользователь может указать идентификатор приложения и идентификатор процесса, но идентификатор приложения должен быть сервером серверного приложения, работающего в процессе с указанным ИДЕНТИФИКАТОРом процесса.</span><span class="sxs-lookup"><span data-stu-id="dcf42-116">The user can specify both the application ID and the process ID, but the application ID has to be that of the server application running in the process with the specified process ID.</span></span> <span data-ttu-id="dcf42-117">Если ни один из этих параметров не указан, пользователь получает метрики из всех серверных и библиотечных приложений.</span><span class="sxs-lookup"><span data-stu-id="dcf42-117">If neither is specified, the user receives metrics from all the server and library applications.</span></span>

<span data-ttu-id="dcf42-118">Метрики инструментария COM+ предоставляют достаточно информации для приложения мониторинга, чтобы сопоставлять их с метриками операционной системы для анализа производительности, планирования загрузки, а также для моделирования и прогнозирования.</span><span class="sxs-lookup"><span data-stu-id="dcf42-118">The COM+ instrumentation metrics provide enough information for the monitoring application to correlate them with the operating system metrics for performance analysis, capacity planning, and for modeling and prediction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcf42-119">См. также</span><span class="sxs-lookup"><span data-stu-id="dcf42-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcf42-120">Интерфейсы инструментария COM+</span><span class="sxs-lookup"><span data-stu-id="dcf42-120">COM+ Instrumentation Interfaces</span></span>](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



