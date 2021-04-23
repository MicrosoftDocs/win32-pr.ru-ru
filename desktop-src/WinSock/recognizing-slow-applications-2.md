---
description: Это пошаговое руководством определяет медленную работу приложения Microsoft Windows с непарной производительностью.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Распознавание замедляют работу приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702887"
---
# <a name="recognizing-slow-applications"></a><span data-ttu-id="7a28e-103">Распознавание замедляют работу приложений</span><span class="sxs-lookup"><span data-stu-id="7a28e-103">Recognizing Slow Applications</span></span>

<span data-ttu-id="7a28e-104">Это пошаговое руководством определяет *медленную работу* приложения Microsoft Windows с непарной производительностью.</span><span class="sxs-lookup"><span data-stu-id="7a28e-104">This guide identifies a *slow* application as a Microsoft Windows application with impaired performance.</span></span> <span data-ttu-id="7a28e-105">В медленных приложениях имеется одна или несколько следующих симптомов:</span><span class="sxs-lookup"><span data-stu-id="7a28e-105">A slow application exhibits one or more of the following symptoms:</span></span>

-   <span data-ttu-id="7a28e-106">Использование ЦП и сети мало.</span><span class="sxs-lookup"><span data-stu-id="7a28e-106">CPU and network utilization are low.</span></span>

    <span data-ttu-id="7a28e-107">Компьютер ожидает чего-либо.</span><span class="sxs-lookup"><span data-stu-id="7a28e-107">The computer appears to be waiting on something.</span></span> <span data-ttu-id="7a28e-108">Часто приложение ожидает в сети.</span><span class="sxs-lookup"><span data-stu-id="7a28e-108">Often, the application is waiting on the network.</span></span>

-   <span data-ttu-id="7a28e-109">Отключение алгоритма Nagle с помощью \_ параметра сокета TCP-задержки повышает производительность.</span><span class="sxs-lookup"><span data-stu-id="7a28e-109">Turning off the Nagle Algorithm through the TCP\_NODELAY socket option increases performance.</span></span>

    <span data-ttu-id="7a28e-110">Это указывает на другие проблемы и не должно рассматриваться как решение.</span><span class="sxs-lookup"><span data-stu-id="7a28e-110">This indicates other problems, and should not be considered a solution.</span></span> <span data-ttu-id="7a28e-111">Отключение алгоритма Nagle увеличивает нагрузку на протокол.</span><span class="sxs-lookup"><span data-stu-id="7a28e-111">Turning off the Nagle algorithm increases the protocol overhead.</span></span> <span data-ttu-id="7a28e-112">Не используйте этот метод в качестве исправления для неработающих приложений — только в качестве указания, что приложению требуется другая работа для устранения проблем с производительностью.</span><span class="sxs-lookup"><span data-stu-id="7a28e-112">Do not use this method as a fix for the broken applications—only as an indication the application needs other work to fix performance issues.</span></span>

-   <span data-ttu-id="7a28e-113">Приложение имеет высокую нагрузку.</span><span class="sxs-lookup"><span data-stu-id="7a28e-113">The application exhibits high overhead.</span></span>

    <span data-ttu-id="7a28e-114">Чтобы вычислить нагрузку на приложения, определите объем данных, предназначенных для перемещения в каждом направлении.</span><span class="sxs-lookup"><span data-stu-id="7a28e-114">To calculate your applications overhead, determine how much data you intended to transfer in each direction.</span></span> <span data-ttu-id="7a28e-115">Затем используйте netstat и добавьте (для Ethernet) 60 байт для каждого пакета и 500 байт для каждого подключения.</span><span class="sxs-lookup"><span data-stu-id="7a28e-115">Then use Netstat and add (for Ethernet) 60 bytes for each packet and 500 bytes for each connection.</span></span> <span data-ttu-id="7a28e-116">Для потоковой передачи по сети Ethernet лучше всего около 6% накладных расходов.</span><span class="sxs-lookup"><span data-stu-id="7a28e-116">The best overhead that can be expected for streaming over Ethernet is approximately 6%.</span></span> <span data-ttu-id="7a28e-117">При подключении через модем лучшие накладные расходы повышены примерно на 2% из-за того, что канал PPP использует сжатие заголовков.</span><span class="sxs-lookup"><span data-stu-id="7a28e-117">For a modem connection, the best overhead is approximately 2%, due to the fact that a PPP link uses header compression.</span></span> <span data-ttu-id="7a28e-118">Дополнительные сведения см. [в разделе Вычисление издержек с помощью netstat](calculating-overhead-with-netstat-2.md) .</span><span class="sxs-lookup"><span data-stu-id="7a28e-118">See [Calculating Overhead with Netstat](calculating-overhead-with-netstat-2.md) for more information.</span></span>

-   <span data-ttu-id="7a28e-119">Отклик приложения замедлится, когда соединение имеет большой RTT.</span><span class="sxs-lookup"><span data-stu-id="7a28e-119">Application response slows when the connection has a large RTT.</span></span>

    <span data-ttu-id="7a28e-120">Если приложение не приближается к пропускной способности связи, большое время приема-передачи не должно оказывать никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="7a28e-120">Assuming the application is not approaching the link's bandwidth, a large RTT should have little or no effect.</span></span> <span data-ttu-id="7a28e-121">Значительное снижение производительности при большом RTT — это четкий знак сериализованной обработки и много небольших транзакций.</span><span class="sxs-lookup"><span data-stu-id="7a28e-121">A dramatic slowdown with a large RTT is a clear sign of serialized processing and many small transactions.</span></span>

<span data-ttu-id="7a28e-122">Каждое приложение должно быть протестировано в среде с большим RTT.</span><span class="sxs-lookup"><span data-stu-id="7a28e-122">Every application should be tested in an environment with a large RTT.</span></span> <span data-ttu-id="7a28e-123">Это открывает большинство приложений, которые пострадает от неудовлетворительных вариантов разработки.</span><span class="sxs-lookup"><span data-stu-id="7a28e-123">Doing so reveals most applications that suffer from poor development choices.</span></span> <span data-ttu-id="7a28e-124">Это тестирование может выполняться в нескольких средах, включая беспроводную ЛОКАЛЬную сеть, симулятор с задержкой канала или вспомогательную сеть.</span><span class="sxs-lookup"><span data-stu-id="7a28e-124">This testing can be performed in several environments, including a wireless LAN network, a link-delay simulator, or a satellite network.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a28e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="7a28e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a28e-126">Поведение приложения</span><span class="sxs-lookup"><span data-stu-id="7a28e-126">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="7a28e-127">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="7a28e-127">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="7a28e-128">Алгоритм Nagle</span><span class="sxs-lookup"><span data-stu-id="7a28e-128">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



