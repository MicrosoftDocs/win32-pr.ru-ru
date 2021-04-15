---
title: Сценарий 3. счетчики производительности
description: Счетчики производительности измеряют количество информации или данных в соответствии с количеством, размером, длительностью и частотой получения запрашиваемых или получаемых данных.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "105661793"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="02784-103">Сценарий 3. счетчики производительности</span><span class="sxs-lookup"><span data-stu-id="02784-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="02784-104">Счетчики производительности измеряют количество информации или данных в соответствии с количеством, размером, длительностью и частотой получения запрашиваемых или получаемых данных.</span><span class="sxs-lookup"><span data-stu-id="02784-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="02784-105">Не следует получать список сведений из счетчика, например список сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="02784-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="02784-106">Вместо этого используйте счетчики производительности для получения таких количеств, как количество сообщений об ошибках с момента запуска или скорость, с которой формируются сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="02784-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="02784-107">Счетчики производительности для HTTP.sys</span><span class="sxs-lookup"><span data-stu-id="02784-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="02784-108">Начиная с Windows Vista и Windows Server 2008, HTTP.sys имеет следующие счетчики метрик производительности, помогающие отслеживать, диагностировать и планировать производительность веб-серверов. компонент API сервера HTTP содержит следующие счетчики производительности, помогающие выполнять мониторинг, диагностику и планирование ресурсов для веб-серверов.</span><span class="sxs-lookup"><span data-stu-id="02784-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="02784-109">Счетчики службы HTTP:</span><span class="sxs-lookup"><span data-stu-id="02784-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="02784-110">Количество URI в кэше, добавленных с момента запуска, удаленных с момента запуска и количества удалений кэша</span><span class="sxs-lookup"><span data-stu-id="02784-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="02784-111">Попаданий в кэш в секунду и промахов кэша в секунду</span><span class="sxs-lookup"><span data-stu-id="02784-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="02784-112">Группы URL-адресов служб HTTP:</span><span class="sxs-lookup"><span data-stu-id="02784-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="02784-113">Скорость отправки данных, скорость получения данных, передано байт (Отправлено и получено)</span><span class="sxs-lookup"><span data-stu-id="02784-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="02784-114">Максимальное число подключений, частота попыток подключения, частота запросов GET и HEAD и общее число запросов</span><span class="sxs-lookup"><span data-stu-id="02784-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="02784-115">Очереди запросов службы HTTP:</span><span class="sxs-lookup"><span data-stu-id="02784-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="02784-116">Число запросов в очереди, возраст самых старых запросов в очереди (возраст последнего запроса в очереди)</span><span class="sxs-lookup"><span data-stu-id="02784-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="02784-117">Интенсивность поступления запросов в очередь, скорость отклонения, общее число отклоненных запросов, частота попаданий в кэш</span><span class="sxs-lookup"><span data-stu-id="02784-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="02784-118">**Доступ к счетчикам производительности**</span><span class="sxs-lookup"><span data-stu-id="02784-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="02784-119">Введите **perfmon** в командной строке, чтобы запустить консоль диагностики производительности.</span><span class="sxs-lookup"><span data-stu-id="02784-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="02784-120">Выберите **системный монитор** в элементе управления "дерево", а затем откройте окно **Добавить счетчики** , нажав кнопку **+** .</span><span class="sxs-lookup"><span data-stu-id="02784-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="02784-121">На странице **Добавление счетчиков** выберите из трех наборов счетчиков производительности: **служба HTTP**, **очереди запросов службы HTTP** или **группы URL-адресов службы HTTP**.</span><span class="sxs-lookup"><span data-stu-id="02784-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="02784-122">Чтобы просмотреть счетчики в наборах счетчиков " **очереди запросов службы HTTP** " и " **группы URL-адресов службы HTTP** ", выберите **экземпляры** и нажмите кнопку **Добавить**, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="02784-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="02784-123">Чтобы просмотреть счетчики службы HTTP, выберите набор счетчиков в левой области и нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="02784-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="02784-124">Для каждого компьютера существует только один экземпляр счетчиков API HTTP-сервера, так как эти счетчики представляют состояние на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="02784-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="02784-125">При использовании экземпляров счетчиков производительности группы URL-адресов идентификатор экземпляра (для счетчика производительности) будет совпадать с ИДЕНТИФИКАТОРом группы URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="02784-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="02784-126">Идентификатор группы URL-адресов можно просмотреть, выполнив **команду netsh http servicestate**.</span><span class="sxs-lookup"><span data-stu-id="02784-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="02784-127">При использовании экземпляров счетчиков производительности очереди запросов имя экземпляра соответствует имени очереди запросов.</span><span class="sxs-lookup"><span data-stu-id="02784-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="02784-128">Имя очереди запросов (если оно существует) может отображаться тем же **netsh http servicestate**.</span><span class="sxs-lookup"><span data-stu-id="02784-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="02784-129">Однако некоторые серверные приложения могут иметь неименованные очереди запросов, которые не могут быть сопоставлены с ИДЕНТИФИКАТОРом экземпляра счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="02784-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




