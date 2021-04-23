---
description: Другим аспектом разработки приложений, который следует рассмотреть, является разница в поведении локальных или интракомпутер операций и поведение при выполнении операций между двумя компьютерами, подключенными к сети.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Поведение приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541642"
---
# <a name="application-behavior"></a><span data-ttu-id="7845a-103">Поведение приложения</span><span class="sxs-lookup"><span data-stu-id="7845a-103">Application Behavior</span></span>

<span data-ttu-id="7845a-104">Другим аспектом разработки приложений, который следует рассмотреть, является разница в поведении локальных или интракомпутер операций и поведение при выполнении операций между двумя компьютерами, подключенными к сети.</span><span class="sxs-lookup"><span data-stu-id="7845a-104">Another aspect of application development to consider is the difference in behavior between local, or intracomputer operations, and behavior when operations take place between two networked computers.</span></span> <span data-ttu-id="7845a-105">Существуют поведения приложений, которые могут хорошо работать на локальном компьютере, но при работе по сети это приводит к значительному снижению производительности и потреблению ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7845a-105">There are application behaviors that may work acceptably well on a local computer, but when run across a network, cause significant performance degradation and resource consumption.</span></span> <span data-ttu-id="7845a-106">При разработке приложений Windows Sockets следует избегать приведенных ниже поведений приложений.</span><span class="sxs-lookup"><span data-stu-id="7845a-106">The following application behaviors should be avoided when developing Windows Sockets applications.</span></span>

## <a name="behaviors-to-avoid"></a><span data-ttu-id="7845a-107">Варианты поведения, которые следует избегать</span><span class="sxs-lookup"><span data-stu-id="7845a-107">Behaviors to Avoid</span></span>

-   <span data-ttu-id="7845a-108">Приложения для разговора.</span><span class="sxs-lookup"><span data-stu-id="7845a-108">Chatty Applications.</span></span>

    <span data-ttu-id="7845a-109">Некоторые приложения выполняют много небольших транзакций.</span><span class="sxs-lookup"><span data-stu-id="7845a-109">Some applications perform many small transactions.</span></span> <span data-ttu-id="7845a-110">При объединении сетевых издержек, связанных с каждой такой транзакцией, этот результат умножается.</span><span class="sxs-lookup"><span data-stu-id="7845a-110">When combined with the network overhead associated with each such transaction, the effect is multiplied.</span></span> <span data-ttu-id="7845a-111">В сети небольшие транзакции могут потреблять столько ресурсов и столько же времени, сколько и большие транзакции.</span><span class="sxs-lookup"><span data-stu-id="7845a-111">In networking, small transactions can consume as many resources and as much time as large transactions.</span></span> <span data-ttu-id="7845a-112">Лучшим подходом является объединение большого количества небольших транзакций в одну большую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="7845a-112">A better approach is to combine many small transactions into a single large transaction.</span></span>

-   <span data-ttu-id="7845a-113">Сериализованные транзакции.</span><span class="sxs-lookup"><span data-stu-id="7845a-113">Serialized Transactions.</span></span>

    <span data-ttu-id="7845a-114">Ненужная сериализация транзакций может привести к снижению производительности и повлиять на масштабируемость.</span><span class="sxs-lookup"><span data-stu-id="7845a-114">Unnecessary serialization of transactions can result in poor performance, and affect scalability.</span></span> <span data-ttu-id="7845a-115">Например, 1000. для завершения сериализованных транзакций требуется по крайней мере 1000 \* RTT.</span><span class="sxs-lookup"><span data-stu-id="7845a-115">For example, 1000 serialized transactions take at least 1000 \* RTT to complete.</span></span> <span data-ttu-id="7845a-116">Лучшим подходом является параллельное выполнение несвязанных транзакций.</span><span class="sxs-lookup"><span data-stu-id="7845a-116">A better approach is to run unrelated transactions in parallel.</span></span> <span data-ttu-id="7845a-117">Когда сериализованные приложения объединяются с приложениями в чате, скорость реагирования может быть серьезно затруднна.</span><span class="sxs-lookup"><span data-stu-id="7845a-117">When serialized applications are combined with chatty applications, responsiveness can be seriously hampered.</span></span>

    > [!Note]  
    > <span data-ttu-id="7845a-118">Правильная десериализация приложения может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="7845a-118">Properly deserializing an application can be difficult.</span></span> <span data-ttu-id="7845a-119">Если переход от сериализованного к параллельному оказывается слишком сложным, рассмотрите возможность объединения нескольких транзакций в меньшее количество больших транзакций.</span><span class="sxs-lookup"><span data-stu-id="7845a-119">If changing from serialized to parallel proves too difficult, consider combining multiple transactions into fewer large transactions.</span></span>

     

-   <span data-ttu-id="7845a-120">Транзакции FAT.</span><span class="sxs-lookup"><span data-stu-id="7845a-120">Fat Transactions.</span></span>

    <span data-ttu-id="7845a-121">Приложения, отправляющие ненужные байты в сети, считаются приложениями FAT.</span><span class="sxs-lookup"><span data-stu-id="7845a-121">Applications that send unnecessary bytes on the network are considered fat applications.</span></span> <span data-ttu-id="7845a-122">Приложения, отправляющие ненужные байты в сети, увеличивают нагрузку на сеть и снижают производительность.</span><span class="sxs-lookup"><span data-stu-id="7845a-122">Applications that send unnecessary bytes on the network increase network overhead, and performance is hampered.</span></span> <span data-ttu-id="7845a-123">Эта ситуация часто возникает из неэффективных структур данных или неэффективной потоковой передачи данных.</span><span class="sxs-lookup"><span data-stu-id="7845a-123">This situation often comes from inefficient data structures or inefficient data streaming.</span></span> <span data-ttu-id="7845a-124">Для устранения этой проблемы Оптимизируйте структуры данных или используйте сжатие.</span><span class="sxs-lookup"><span data-stu-id="7845a-124">To remedy this, optimize data structures, or consider using compression.</span></span>

<span data-ttu-id="7845a-125">В следующих разделах рассматриваются аспекты разработки приложений, которые следует учитывать.</span><span class="sxs-lookup"><span data-stu-id="7845a-125">The following sections address aspects of application development to consider.</span></span>

-   [<span data-ttu-id="7845a-126">Проблемы, связанные с TCP/IP</span><span class="sxs-lookup"><span data-stu-id="7845a-126">TCP/IP-specific Issues</span></span>](tcp-ip-specific-issues-2.md)
-   [<span data-ttu-id="7845a-127">Распознавание замедляют работу приложений</span><span class="sxs-lookup"><span data-stu-id="7845a-127">Recognizing Slow Applications</span></span>](recognizing-slow-applications-2.md)
-   [<span data-ttu-id="7845a-128">Вычисление накладных расходов с помощью netstat</span><span class="sxs-lookup"><span data-stu-id="7845a-128">Calculating Overhead with Netstat</span></span>](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a><span data-ttu-id="7845a-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7845a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7845a-130">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="7845a-130">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



