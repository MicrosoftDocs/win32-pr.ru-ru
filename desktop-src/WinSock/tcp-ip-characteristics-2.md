---
description: Протокол TCP/IP имеет характеристики, позволяющие использовать его в качестве стандартизированных требований к реализации.
ms.assetid: 6e9b3878-85f0-4572-9c00-a2e7647286ff
title: Характеристики TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 561ab497d6f37c1c84b0203088b29e216ff0a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910579"
---
# <a name="tcpip-characteristics"></a><span data-ttu-id="ec553-103">Характеристики TCP/IP</span><span class="sxs-lookup"><span data-stu-id="ec553-103">TCP/IP Characteristics</span></span>

<span data-ttu-id="ec553-104">Протокол TCP/IP имеет характеристики, позволяющие использовать его в качестве стандартизированных требований к реализации.</span><span class="sxs-lookup"><span data-stu-id="ec553-104">TCP/IP has characteristics that enable the protocol to operate as its standardized implementation requirements dictate.</span></span> <span data-ttu-id="ec553-105">Эти характеристики могут сочетаться с вариантами разработки, что приводит к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="ec553-105">These characteristics can combine with development choices that result in poor performance.</span></span> <span data-ttu-id="ec553-106">Влияние этих характеристик TCP/IP на приложение зависит от того, является ли приложение транзакционным или потоковым.</span><span class="sxs-lookup"><span data-stu-id="ec553-106">The impact these TCP/IP characteristics have on an application depend on whether the application is transactional or streaming.</span></span>

<span data-ttu-id="ec553-107">На транзакционные приложения влияют накладные расходы, необходимые для установки соединения и завершения его работы.</span><span class="sxs-lookup"><span data-stu-id="ec553-107">Transactional applications are affected by the overhead required for connection establishment and termination.</span></span> <span data-ttu-id="ec553-108">Например, при каждом установлении подключения в сети Ethernet необходимо отправить три пакета примерно 60 байта, а для Exchange требуется примерно один RTT.</span><span class="sxs-lookup"><span data-stu-id="ec553-108">For example, each time a connection is established on an Ethernet network, three packets of approximately 60 bytes each must be sent, and approximately one RTT is required for the exchange.</span></span> <span data-ttu-id="ec553-109">При завершении соединения происходит обмен четырьмя пакетами.</span><span class="sxs-lookup"><span data-stu-id="ec553-109">When termination of a connection occurs, four packets are exchanged.</span></span> <span data-ttu-id="ec553-110">Это для каждого подключения; приложение, которое открывает и закрывает соединения, часто приводит к такой нагрузке при каждом возникновении.</span><span class="sxs-lookup"><span data-stu-id="ec553-110">This is for each connection; an application that opens and closes connections often incurs this overhead on each occurrence.</span></span>

<span data-ttu-id="ec553-111">Другой аспект TCP/IP — это *замедляют запуск*, который выполняется при каждом установлении соединения.</span><span class="sxs-lookup"><span data-stu-id="ec553-111">Another aspect of TCP/IP is *slow-start*, which takes place whenever a connection is established.</span></span> <span data-ttu-id="ec553-112">Замедляют-Start — искусственное ограничение количества сегментов данных, которые могут быть отправлены до получения подтверждения этих сегментов.</span><span class="sxs-lookup"><span data-stu-id="ec553-112">Slow-start is an artificial limit on the number of data segments that can be sent before acknowledgment of those segments is received.</span></span> <span data-ttu-id="ec553-113">Процесс с пониженным запуском предназначен для ограничения перегрузки сети.</span><span class="sxs-lookup"><span data-stu-id="ec553-113">Slow-start is designed to limit network congestion.</span></span> <span data-ttu-id="ec553-114">При установлении соединения по протоколу Ethernet, независимо от размера окна получателя, передача на 4 КБ может занять до 3-4 RTT из-за медленного запуска.</span><span class="sxs-lookup"><span data-stu-id="ec553-114">When a connection over Ethernet is established, regardless of the receiver's window size, a 4 KB transmission can take up to 3-4 RTT due to slow-start.</span></span>

<span data-ttu-id="ec553-115">Оптимизация TCP/IP, называемая алгоритмом Nagle, также может ограничить скорость передачи данных для соединения.</span><span class="sxs-lookup"><span data-stu-id="ec553-115">A TCP/IP optimization called the Nagle Algorithm can also limit data transfer speed on a connection.</span></span> <span data-ttu-id="ec553-116">Алгоритм Nagle предназначен для уменьшения нагрузки на протоколы для приложений, отправляющих небольшие объемы данных, таких как Telnet, который отправляет по одному символу за раз.</span><span class="sxs-lookup"><span data-stu-id="ec553-116">The Nagle Algorithm is designed to reduce protocol overhead for applications that send small amounts of data, such as Telnet, which sends a single character at a time.</span></span> <span data-ttu-id="ec553-117">Вместо немедленной отправки пакета с большим количеством заголовков и небольшими данными стек ожидает больше данных от приложения или подтверждения, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="ec553-117">Rather than immediately send a packet with lots of header and little data, the stack waits for more data from the application, or an acknowledgment, before proceeding.</span></span>

<span data-ttu-id="ec553-118">Отложенные подтверждения, обычно называемые *отложенным подтверждением*, также разрабатываются в протоколе TCP/IP, чтобы обеспечить более эффективную пиггибаккинг подтверждений, когда возвращаемые данные поступают из принимающего приложения.</span><span class="sxs-lookup"><span data-stu-id="ec553-118">Delayed acknowledgments, commonly referred to as *delayed ACK*, are also designed into TCP/IP to enable more efficient piggybacking of acknowledgments when return data is forthcoming from the receiving side application.</span></span> <span data-ttu-id="ec553-119">К сожалению, если эти данные не являются готовыми и отправитель ожидает подтверждения, может возникнуть задержка примерно 200 мс на отправку.</span><span class="sxs-lookup"><span data-stu-id="ec553-119">Unfortunately, if this data is not forthcoming and the sending side is waiting for an acknowledgment, delays of approximately 200 milliseconds per send can occur.</span></span>

<span data-ttu-id="ec553-120">При закрытии подключения TCP ресурсы подключения на узле, который инициировал закрытие, переносятся в состояние ожидания, которое называется временем ожидания, чтобы защититься от повреждения данных в случае, если в сети имеются дублирующиеся пакеты.</span><span class="sxs-lookup"><span data-stu-id="ec553-120">When a TCP connection is closed, connection resources at the node that initiated the close are put into a wait state, called TIME-WAIT, to guard against data corruption if duplicate packets linger in the network.</span></span> <span data-ttu-id="ec553-121">Это гарантирует, что оба конца будут завершены с подключением.</span><span class="sxs-lookup"><span data-stu-id="ec553-121">This ensures both ends are finished with the connection.</span></span> <span data-ttu-id="ec553-122">Это может привести к исчерпанию ресурсов, необходимых для каждого подключения, например ОЗУ и портов, когда приложения часто открывают и закрывают подключения.</span><span class="sxs-lookup"><span data-stu-id="ec553-122">This can cause depletion of resources required per-connection, such as RAM and ports, when applications open and close connections frequently.</span></span>

<span data-ttu-id="ec553-123">Помимо затронутых отложенных ПОДТВЕРЖДЕНий и других схем предотвращения перегрузки, для потоковых приложений также может повлиять слишком маленький размер окна приема по умолчанию на принимающей стороне.</span><span class="sxs-lookup"><span data-stu-id="ec553-123">Besides being affected by delayed ACK and other congestion avoidance schemes, streaming applications can also be affected by a too-small default receive window size on the receiving end.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec553-124">См. также</span><span class="sxs-lookup"><span data-stu-id="ec553-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec553-125">Поведение приложения</span><span class="sxs-lookup"><span data-stu-id="ec553-125">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="ec553-126">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="ec553-126">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="ec553-127">Алгоритм Nagle</span><span class="sxs-lookup"><span data-stu-id="ec553-127">Nagle Algorithm</span></span>](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



