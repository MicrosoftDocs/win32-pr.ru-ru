---
description: Вычисление накладных расходов с помощью netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Вычисление накладных расходов с помощью netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701563"
---
# <a name="calculating-overhead-with-netstat"></a><span data-ttu-id="490eb-103">Вычисление накладных расходов с помощью netstat</span><span class="sxs-lookup"><span data-stu-id="490eb-103">Calculating Overhead with Netstat</span></span>

<span data-ttu-id="490eb-104">Чтобы избежать снижения нагрузки на данные, такие как широковещательный или многоадресный трафик, следует вычислять накладные расходы с помощью netstat в тихой сети.</span><span class="sxs-lookup"><span data-stu-id="490eb-104">Calculating overhead with Netstat should be performed on a quiet network to avoid other network traffic from skewing the data, such as broadcast or multicast traffic.</span></span>

<span data-ttu-id="490eb-105">**Вычисление сетевой нагрузки приложения с помощью программы netstat**</span><span class="sxs-lookup"><span data-stu-id="490eb-105">**To calculate an application's network overhead using Netstat**</span></span>

1.  <span data-ttu-id="490eb-106">Получение статистики текущего интерфейса с помощью программы netstat.</span><span class="sxs-lookup"><span data-stu-id="490eb-106">Retrieve the current interface statistics using Netstat.</span></span>
2.  <span data-ttu-id="490eb-107">Запустите приложение.</span><span class="sxs-lookup"><span data-stu-id="490eb-107">Execute the application.</span></span>
3.  <span data-ttu-id="490eb-108">Получите статистику интерфейса снова с помощью программы netstat.</span><span class="sxs-lookup"><span data-stu-id="490eb-108">Get the interface statistics, again using Netstat.</span></span>
4.  <span data-ttu-id="490eb-109">Вычислите число байтов, полученных между двумя измерениями netstat.</span><span class="sxs-lookup"><span data-stu-id="490eb-109">Calculate the number of bytes received between the two Netstat measurements.</span></span>

## <a name="example"></a><span data-ttu-id="490eb-110">Пример</span><span class="sxs-lookup"><span data-stu-id="490eb-110">Example</span></span>

<span data-ttu-id="490eb-111">В следующем примере показаны эти действия с использованием TTCP для отправки 10 байт данных по одному байту за раз.</span><span class="sxs-lookup"><span data-stu-id="490eb-111">The following example demonstrates these steps, using TTCP to send 10 bytes of data, one byte at a time.</span></span>

<span data-ttu-id="490eb-112">Во-первых, вычисляется теоретическая нагрузка на приложение.</span><span class="sxs-lookup"><span data-stu-id="490eb-112">First, a theoretical overhead for the application is calculated.</span></span> <span data-ttu-id="490eb-113">Для этого теста все пакеты имеют размер 60 байт (минимум Ethernet).</span><span class="sxs-lookup"><span data-stu-id="490eb-113">For this test, all packets are 60 bytes (the Ethernet minimum).</span></span> <span data-ttu-id="490eb-114">Для этого требуется три пакета, чтобы настроить подключение, 10 пакетов данных, 10 пакетов подтверждения (отложенное подтверждение инициируется почти каждый раз) и четыре пакета для корректного закрытия подключения.</span><span class="sxs-lookup"><span data-stu-id="490eb-114">This transfer requires three packets to set up the connection, 10 data packets, 10 acknowledgment packets (delayed ACK is triggered nearly every time), and four packets to close the connection gracefully.</span></span>

<span data-ttu-id="490eb-115">Это соответствует 27 пакетам по 60 байт или 1620 байт (3 + 4 + 10 + 10) \* 60 = 1620).</span><span class="sxs-lookup"><span data-stu-id="490eb-115">This equates to 27 packets of 60 bytes each, or 1620 bytes (3+4+10+10)\*60=1620).</span></span> <span data-ttu-id="490eb-116">Так как передаются только 10 байт данных, нагрузка составляет 1610 байт, что превышает 99% нагрузки на протокол.</span><span class="sxs-lookup"><span data-stu-id="490eb-116">Since only 10 bytes of data are transferred, the overhead is 1610 bytes, which is over 99% protocol overhead.</span></span>

### <a name="commands"></a><span data-ttu-id="490eb-117">Команды</span><span class="sxs-lookup"><span data-stu-id="490eb-117">Commands</span></span>

<span data-ttu-id="490eb-118">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="490eb-118">**netstat -e**</span></span>

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

<span data-ttu-id="490eb-119">**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**</span><span class="sxs-lookup"><span data-stu-id="490eb-119">**ttcp -t -h0 -D -l1 -n10 -p9 172.31.71.99**</span></span>

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

<span data-ttu-id="490eb-120">**netstat-e**</span><span class="sxs-lookup"><span data-stu-id="490eb-120">**netstat -e**</span></span>

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a><span data-ttu-id="490eb-121">Вычисления</span><span class="sxs-lookup"><span data-stu-id="490eb-121">Calculations</span></span>

<span data-ttu-id="490eb-122">**Отправлено:** 816 байт</span><span class="sxs-lookup"><span data-stu-id="490eb-122">**Sent:** 816 bytes</span></span>

<span data-ttu-id="490eb-123">**Получено:** 674 байт</span><span class="sxs-lookup"><span data-stu-id="490eb-123">**Received:** 674 bytes</span></span>

<span data-ttu-id="490eb-124">**Всего байт:** 1490</span><span class="sxs-lookup"><span data-stu-id="490eb-124">**Total bytes:** 1490</span></span>

<span data-ttu-id="490eb-125">**Байт пользователя:** 10</span><span class="sxs-lookup"><span data-stu-id="490eb-125">**User bytes:** 10</span></span>

<span data-ttu-id="490eb-126">**Накладные расходы:** 1480/1490 = 99,3%</span><span class="sxs-lookup"><span data-stu-id="490eb-126">**Overhead:** 1480/1490 = 99.3%</span></span>

<span data-ttu-id="490eb-127">\* \* Гудпут: \* \* = 5 байт/сек (или 40 бит/с)</span><span class="sxs-lookup"><span data-stu-id="490eb-127">\*\*Goodput:  \*\*= 5 bytes/second (or 40 bits/s)</span></span>

> [!Note]  
> <span data-ttu-id="490eb-128">Фактические переданные байты не соответствуют теоретическому значению, так как в значениях netstat не учитывается размер байтов для заполнения.</span><span class="sxs-lookup"><span data-stu-id="490eb-128">Actual bytes transferred do not match the theoretical values due to padding bytes not being accounted for in the Netstat values.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="490eb-129">См. также</span><span class="sxs-lookup"><span data-stu-id="490eb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="490eb-130">Поведение приложения</span><span class="sxs-lookup"><span data-stu-id="490eb-130">Application Behavior</span></span>](application-behavior-2.md)
</dt> <dt>

[<span data-ttu-id="490eb-131">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="490eb-131">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



