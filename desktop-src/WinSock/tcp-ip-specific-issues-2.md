---
description: Некоторые методы программирования выполняются с проблемами производительности, связанными с реализацией TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Проблемы, связанные с TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712125"
---
# <a name="tcpip-specific-issues"></a><span data-ttu-id="7faf9-103">Проблемы, связанные с TCP/IP</span><span class="sxs-lookup"><span data-stu-id="7faf9-103">TCP/IP-specific Issues</span></span>

<span data-ttu-id="7faf9-104">Некоторые методы программирования выполняются с проблемами производительности, связанными с реализацией TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7faf9-104">Certain programming techniques run into performance issues that are linked to the implementation of TCP/IP.</span></span> <span data-ttu-id="7faf9-105">Такие проблемы с производительностью не предполагают, что TCP/IP не является эффективным или узким местом производительности. скорее, эти проблемы возникают, когда не понимаются операции TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="7faf9-105">Such performance issues do not suggest that TCP/IP is inefficient or a performance bottleneck; rather, these issues are seen when TCP/IP operations are not understood.</span></span>

<span data-ttu-id="7faf9-106">Следующие проблемы являются типичными сценариями, в которых сочетание операций TCP/IP и параметров разработки сетевых приложений приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="7faf9-106">The following issues identify common scenarios in which the combination of TCP/IP operation and network application development choices result in poor performance.</span></span>

-   <span data-ttu-id="7faf9-107">Приложения с большим количеством подключений.</span><span class="sxs-lookup"><span data-stu-id="7faf9-107">Connect-heavy Applications.</span></span>

    <span data-ttu-id="7faf9-108">Некоторые приложения создают новое соединение TCP для каждой транзакции.</span><span class="sxs-lookup"><span data-stu-id="7faf9-108">Some applications instantiate a new TCP connection for each transaction.</span></span> <span data-ttu-id="7faf9-109">Подключение по протоколу TCP занимает некоторое время, вносит дополнительные RTTs и может замедляться запуском.</span><span class="sxs-lookup"><span data-stu-id="7faf9-109">TCP connection establishment takes time, contributes extra RTTs, and is subject to slow-start.</span></span> <span data-ttu-id="7faf9-110">Кроме того, закрытые подключения подчиняются времени ожидания, при котором используются системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7faf9-110">In addition, the closed connections are subject to TIME-WAIT, which consumes system resources.</span></span>

    <span data-ttu-id="7faf9-111">Приложения с большим количеством подключений часто используются в основном, так как их легко создать. Тестирование и обработка ошибок очень просты.</span><span class="sxs-lookup"><span data-stu-id="7faf9-111">Connect-heavy applications are common largely because they are easy to create; testing and error handling is very simple.</span></span> <span data-ttu-id="7faf9-112">Обнаружение ошибок в постоянном подключении может занять значительный объем кода и усилий, поэтому иногда он не завершается.</span><span class="sxs-lookup"><span data-stu-id="7faf9-112">Detecting faults on a persistent connection can take considerable code and effort, and therefore is sometimes not completed.</span></span>

    <span data-ttu-id="7faf9-113">Исследует эту ситуацию, повторно используя TCP-соединение.</span><span class="sxs-lookup"><span data-stu-id="7faf9-113">Remedy this situation by reusing the TCP connection.</span></span> <span data-ttu-id="7faf9-114">Это может привести к сериализации через TCP-подключение, если только транзакции не мультиплексированы по нескольким соединениям.</span><span class="sxs-lookup"><span data-stu-id="7faf9-114">This may cause serialization over the TCP connection unless the transactions are multiplexed over multiple connections.</span></span> <span data-ttu-id="7faf9-115">При использовании этого подхода число подключений должно быть ограничено двумя, и требуется формирование кадров уровня приложения и расширенная обработка ошибок.</span><span class="sxs-lookup"><span data-stu-id="7faf9-115">If this approach is taken, the number of connections should be limited to two, and application-layer framing and advanced error handling are required.</span></span>

-   <span data-ttu-id="7faf9-116">Буферы отправки нулевой длины и блокировки отправляются.</span><span class="sxs-lookup"><span data-stu-id="7faf9-116">Zero-length Send Buffers and Blocking Sends.</span></span>

    <span data-ttu-id="7faf9-117">Отключение буферизации с помощью функции [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) для установки буфера отправки (so \_ сндбуф) в нулевое значение похоже на отключение кэширования диска.</span><span class="sxs-lookup"><span data-stu-id="7faf9-117">Turning off buffering by using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set the send buffer (SO\_SNDBUF) to zero is similar to turning off disk caching.</span></span> <span data-ttu-id="7faf9-118">При задании для буфера отправки нулевого значения и отправке блокировки отправка приложения имеет 50% шансов на попадание в 200-миллисекунду с отложенным подтверждением.</span><span class="sxs-lookup"><span data-stu-id="7faf9-118">When setting the send buffer to zero and issuing blocking sends, an application has a fifty percent chance of hitting a 200-millisecond delayed acknowledgment.</span></span>

    <span data-ttu-id="7faf9-119">Не отключайте буферизацию отправки, если не учитывается влияние на все сетевые среды.</span><span class="sxs-lookup"><span data-stu-id="7faf9-119">Do not turn off send buffering unless you have considered the impact in all network environments.</span></span> <span data-ttu-id="7faf9-120">Одно исключение. потоковые данные, использующие перекрывающиеся операции ввода-вывода, должны устанавливать буфер отправки в ноль.</span><span class="sxs-lookup"><span data-stu-id="7faf9-120">One exception: streaming data using overlapped I/O should set the send buffer to zero.</span></span>

-   <span data-ttu-id="7faf9-121">Отправка и отправка — получение модели программирования.</span><span class="sxs-lookup"><span data-stu-id="7faf9-121">Send-Send-Receive programming model.</span></span>

    <span data-ttu-id="7faf9-122">Структурирование приложения для выполнения отправки и отправки — повышает вероятность возникновения алгоритма Nagle, что приводит к задержке RTT + 200 мс.</span><span class="sxs-lookup"><span data-stu-id="7faf9-122">Structuring an application to perform send-send-receives increases your chances of encountering the Nagle Algorithm, which causes a delay of RTT+200 ms.</span></span> <span data-ttu-id="7faf9-123">Алгоритм Nagle может быть обнаружен, если последняя отправка меньше, чем максимальный размер сегмента TCP (MSS, максимальный объем данных в одной датаграмме).</span><span class="sxs-lookup"><span data-stu-id="7faf9-123">The Nagle Algorithm may be encountered if the last send is less than the TCP Maximum Segment Size (MSS, the maximum data in a single datagram).</span></span> <span data-ttu-id="7faf9-124">MSS может быть очень большим значением (64 КБ и даже больше в IPv6), поэтому не учитывается как обычно небольшой MSS.</span><span class="sxs-lookup"><span data-stu-id="7faf9-124">MSS can be a very large value (64K in IPv4, and even larger in IPv6), so do not count on a typically small MSS.</span></span> <span data-ttu-id="7faf9-125">Лучшим вариантом является объединение двух отправок в одну функцию send с помощью функции [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) или **memcpy** .</span><span class="sxs-lookup"><span data-stu-id="7faf9-125">A better option is to combine the two sends into a single send using the [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) or **memcpy** function.</span></span>

-   <span data-ttu-id="7faf9-126">Большое количество одновременных подключений.</span><span class="sxs-lookup"><span data-stu-id="7faf9-126">Large Number of Simultaneous Connections.</span></span>

    <span data-ttu-id="7faf9-127">Количество одновременных подключений не должно превышать два, за исключением приложений специального назначения.</span><span class="sxs-lookup"><span data-stu-id="7faf9-127">Concurrent connections should not exceed two, except in special purpose applications.</span></span> <span data-ttu-id="7faf9-128">Превышение двух одновременных подключений приведет к нерасходованию ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7faf9-128">Exceeding two concurrent connections results in wasted resources.</span></span> <span data-ttu-id="7faf9-129">Хорошим правилом является наличие до четырех кратковременных подключений или двух постоянных подключений на назначение.</span><span class="sxs-lookup"><span data-stu-id="7faf9-129">A good rule is to have up to four short lived connections, or two persistent connections per destination.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7faf9-130">См. также</span><span class="sxs-lookup"><span data-stu-id="7faf9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7faf9-131">Поведение приложения</span><span class="sxs-lookup"><span data-stu-id="7faf9-131">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="7faf9-132">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="7faf9-132">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="7faf9-133">Алгоритм Nagle</span><span class="sxs-lookup"><span data-stu-id="7faf9-133">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



