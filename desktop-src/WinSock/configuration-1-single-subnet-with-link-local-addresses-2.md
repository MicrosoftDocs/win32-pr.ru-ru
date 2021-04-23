---
description: Для первой конфигурации не требуется дополнительная настройка, Кроме установки протокола предварительной версии Microsoft IPv6.
ms.assetid: ceed4983-e088-44e8-9cfc-26afb3c35ba0
title: Конфигурация 1. Одна подсеть с адресами локальной связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d09feb44c222b7213da18a6745fc632f3903209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072750"
---
# <a name="configuration-1-single-subnet-with-link-local-addresses"></a><span data-ttu-id="af168-103">Конфигурация 1. Одна подсеть с адресами локальной связи</span><span class="sxs-lookup"><span data-stu-id="af168-103">Configuration 1: Single Subnet with Link-local Addresses</span></span>

<span data-ttu-id="af168-104">Для первой конфигурации не требуется дополнительная настройка, Кроме установки протокола предварительной версии Microsoft IPv6.</span><span class="sxs-lookup"><span data-stu-id="af168-104">The first configuration requires no additional configuration beyond installing the Microsoft IPv6 Technology Preview protocol.</span></span> <span data-ttu-id="af168-105">Эта конфигурация состоит по крайней мере из двух узлов в одной подсети.</span><span class="sxs-lookup"><span data-stu-id="af168-105">This configuration consists of at least two nodes on the same subnet.</span></span> <span data-ttu-id="af168-106">В терминологии IPv6 два узла находятся в одной и той же связи без промежуточных маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="af168-106">In IPv6 terminology, the two nodes are on the same link with no intermediate routers.</span></span>

<span data-ttu-id="af168-107">На следующем рисунке показана конфигурация двух узлов в одной подсети с использованием адресов локальной связи.</span><span class="sxs-lookup"><span data-stu-id="af168-107">The following illustration shows the configuration of two nodes on a single subnet using link-local addresses.</span></span>

![два узла, использующие адреса локальной связи.](images/v6mig-1.png)

<span data-ttu-id="af168-109">По умолчанию IPv6 настраивает IP-адреса локальной связи для каждого интерфейса, соответствующего установленным сетевым адаптерам Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af168-109">By default, IPv6 configures link-local IP addresses for each interface corresponding to installed Ethernet network adapters.</span></span> <span data-ttu-id="af168-110">Адреса локальной связи имеют префикс FE80::/64.</span><span class="sxs-lookup"><span data-stu-id="af168-110">Link-local addresses have the prefix fe80::/64.</span></span> <span data-ttu-id="af168-111">Последние 64 бит IPv6-адреса называются идентификатором интерфейса. он является производным от 48-разрядного IP-адреса сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="af168-111">The last 64 bits of the IPv6 address is known as the interface identifier and is derived from the 48-bit MAC address of the network adapter.</span></span>

<span data-ttu-id="af168-112">Чтобы создать идентификатор интерфейса IPv6 из 48-разрядного (6-байтового) Ethernet-адреса, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="af168-112">To create the IPv6 interface identifier from the 48-bit (6-byte) Ethernet MAC address:</span></span>

-   <span data-ttu-id="af168-113">Шестнадцатеричные цифры 0xFF – Fe вставляются между третьим и четвертым байтами MAC-адреса.</span><span class="sxs-lookup"><span data-stu-id="af168-113">The hex digits 0xff-fe are inserted between the third and fourth byte of the MAC address.</span></span>
-   <span data-ttu-id="af168-114">Двоичный/локальный бит, второй младший бит первого байта MAC-адреса, дополняется.</span><span class="sxs-lookup"><span data-stu-id="af168-114">The Universal/Local bit, the second low-order bit of the first byte of the MAC address, is complemented.</span></span> <span data-ttu-id="af168-115">Если значение равно 1, то оно будет равно 0, а если — 0, то значение будет равно 1.</span><span class="sxs-lookup"><span data-stu-id="af168-115">If it is a 1, it is turned to 0, and if it is a 0, it is turned to 1.</span></span>

<span data-ttu-id="af168-116">Например, для MAC-адреса 00-60-08-52 – F9-D8:</span><span class="sxs-lookup"><span data-stu-id="af168-116">For example, for the MAC address 00-60-08-52-f9-d8:</span></span>

-   <span data-ttu-id="af168-117">Шестнадцатеричные цифры 0xFF – Fe вставляются между 0x08 (третьим байтом) и 0x52 (четвертый байт) MAC-адреса, образуя 64-разрядный адрес 00-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="af168-117">The hex digits 0xff-fe are inserted between 0x08 (the third byte) and 0x52 (the fourth byte) of the MAC address, forming the 64-bit address 00-60-08-ff-fe-52-f9-d8.</span></span>
-   <span data-ttu-id="af168-118">Двоичный/локальный бит, второй младший бит 0x00 (первый байт) MAC-адреса дополняется.</span><span class="sxs-lookup"><span data-stu-id="af168-118">The Universal/Local bit, the second low-order bit of 0x00 (the first byte) of the MAC address is complemented.</span></span> <span data-ttu-id="af168-119">Второй младший бит 0x00 равен 0, что, когда дополняющийсь, становится 1.</span><span class="sxs-lookup"><span data-stu-id="af168-119">The second low-order bit of 0x00 is 0 which, when complemented, becomes 1.</span></span> <span data-ttu-id="af168-120">Результат заключается в том, что для первого байта 0x00 преобразуется в 0x02.</span><span class="sxs-lookup"><span data-stu-id="af168-120">The result is that for the first byte, 0x00 becomes 0x02.</span></span>

<span data-ttu-id="af168-121">Таким образом, идентификатор интерфейса IPv6, соответствующий MAC-адресу Ethernet 00-60-08-52-F9-D8, составляет 02-60-08-FF-FE-52-F9-D8.</span><span class="sxs-lookup"><span data-stu-id="af168-121">Therefore, the IPv6 interface identifier corresponding to the Ethernet MAC address of 00-60-08-52-f9-d8 is 02-60-08-ff-fe-52-f9-d8.</span></span>

<span data-ttu-id="af168-122">Адрес локальной связи узла — это сочетание префикса FE80::/64 и идентификатора 64-разрядного интерфейса, выраженного в шестнадцатеричной нотации IPv6.</span><span class="sxs-lookup"><span data-stu-id="af168-122">The link-local address of a node is the combination of the prefix fe80::/64 and the 64-bit interface identifier expressed in IPv6 colon-hexadecimal notation.</span></span> <span data-ttu-id="af168-123">Таким образом, адрес локальной связи этого узла примера с префиксом FE80::/64 и идентификатором интерфейса 02-60-08-FF-FE-52-F9-D8 — FE80:: 260:8FF: FE52: F9D8.</span><span class="sxs-lookup"><span data-stu-id="af168-123">Therefore, the link-local address of this example node with the prefix fe80::/64 and the interface identifier 02-60-08-ff-fe-52-f9-d8 is fe80::260:8ff:fe52:f9d8.</span></span>

<span data-ttu-id="af168-124">Вы можете просмотреть локальный адрес ссылки с помощью IPv6, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="af168-124">You can view your link local address by using ipv6 if, as demonstrated in the following example:</span></span>

<span data-ttu-id="af168-125">**IPv6, если**</span><span class="sxs-lookup"><span data-stu-id="af168-125">**ipv6 if**</span></span>

``` syntax
Interface 4 (site 1): Local Area Connection
  uses Neighbor Discovery
  link-level address: 00-10-5a-aa-20-a2
    preferred address fe80::210:5aff:feaa:20a2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ffaa:20a2, 1 refs, last reporter
  link MTU 1500 (true link MTU 1500)
  current hop limit 128
  reachable time 43500ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 3 (site 1): 6-over-4 Virtual Interface
  uses Neighbor Discovery
  link-level address: 10.0.0.2
    preferred address fe80::a00:2, infinite/infinite
    multicast address ff02::1, 1 refs, not reportable
    multicast address ff02::1:ff00:2, 1 refs, last reporter
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 34000ms (base 30000ms)
  retransmission interval 1000ms
  DAD transmits 1
Interface 2 (site 0): Tunnel Pseudo-Interface
  does not use Neighbor Discovery
  link-level address: 0.0.0.0
    preferred address ::10.0.0.2, infinite/infinite
  link MTU 1280 (true link MTU 65515)
  current hop limit 128
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
Interface 1 (site 0): Loopback Pseudo-Interface
  does not use Neighbor Discovery
  link-level address:
    preferred address ::1, infinite/infinite
  link MTU 1500 (true link MTU 1500)
  current hop limit 1
  reachable time 0ms (base 0ms)
  retransmission interval 0ms
  DAD transmits 0
```

<span data-ttu-id="af168-126">Интерфейс 4 — это интерфейс, соответствующий установленному адаптеру Ethernet с адресом локальной связи FE80:: 210:5AFF: феаа: 20A2.</span><span class="sxs-lookup"><span data-stu-id="af168-126">Interface 4 is an interface corresponding to an installed Ethernet adapter with a link-local address of fe80::210:5aff:feaa:20a2.</span></span>

<span data-ttu-id="af168-127">Дополнительные сведения об адресации IPv6 и обзоре концепций IPv6 см. в техническом документе Введение в IPv6.</span><span class="sxs-lookup"><span data-stu-id="af168-127">For more information on IPv6 addressing and an overview of IPv6 concepts, see the Introduction to IPv6 white paper.</span></span>

## <a name="testing-connectivity-between-two-link-local-hosts"></a><span data-ttu-id="af168-128">Проверка подключения между двумя локальными узлами связи</span><span class="sxs-lookup"><span data-stu-id="af168-128">Testing Connectivity Between Two Link-local Hosts</span></span>

<span data-ttu-id="af168-129">Можно выполнить простую проверку связи (обмен сообщениями эхо-запросов ICMPv6 и эхо-ответов), используя IPv6 между двумя узлами локальной связи.</span><span class="sxs-lookup"><span data-stu-id="af168-129">You can do a simple ping (an exchange of ICMPv6 Echo Request and Echo Reply messages) using IPv6 between two link-local hosts.</span></span>

<span data-ttu-id="af168-130">**Проверка связи с использованием IPv6 между двумя узлами локальной связи**</span><span class="sxs-lookup"><span data-stu-id="af168-130">**To ping using IPv6 between two link-local hosts**</span></span>

1.  <span data-ttu-id="af168-131">Установите предварительную версию Microsoft IPv6 для Windows на двух узлах Windows (узлы A и B), которые находятся в одной и той же связи (подсеть).</span><span class="sxs-lookup"><span data-stu-id="af168-131">Install the Microsoft IPv6 Technology Preview for Windows on two Windows hosts (Host A and Host B) that are on the same link (subnet).</span></span>
2.  <span data-ttu-id="af168-132">Используйте IPv6, если на узле A, чтобы получить адрес локальной связи для интерфейса Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af168-132">Use ipv6 if on Host A to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="af168-133">Пример. адрес локальной ссылки узла A — FE80:: 210:5AFF: феаа: 20A2.</span><span class="sxs-lookup"><span data-stu-id="af168-133">Example: The link-local address of Host A is fe80::210:5aff:feaa:20a2.</span></span>

3.  <span data-ttu-id="af168-134">Используйте IPv6, если на узле B получить адрес локальной связи для интерфейса Ethernet.</span><span class="sxs-lookup"><span data-stu-id="af168-134">Use ipv6 if on Host B to obtain the link-local address for the Ethernet interface.</span></span>

    <span data-ttu-id="af168-135">Пример. адрес локальной ссылки узла B — FE80:: 260:97FF: FE02:6EA5.</span><span class="sxs-lookup"><span data-stu-id="af168-135">Example: The link-local address of Host B is fe80::260:97ff:fe02:6ea5.</span></span>

4.  <span data-ttu-id="af168-136">С узла A проверьте связь с узлом B с помощью Ping6.exe.</span><span class="sxs-lookup"><span data-stu-id="af168-136">From Host A, ping Host B using Ping6.exe.</span></span>

    <span data-ttu-id="af168-137">Пример: ping6 FE80:: 260:97FF: FE02:6EA5</span><span class="sxs-lookup"><span data-stu-id="af168-137">Example: ping6 fe80::260:97ff:fe02:6ea5</span></span>

<span data-ttu-id="af168-138">Чтобы указать адрес источника, из которого отправляются сообщения запроса эха, можно также использовать параметр Ping6.exe-s.</span><span class="sxs-lookup"><span data-stu-id="af168-138">To specify the source address from which the Echo Request messages are sent, you can also use the Ping6.exe -s option.</span></span> <span data-ttu-id="af168-139">Например, чтобы отправить эхо-запросы на узел B с адреса IPv6 FE80:: 210:5AFF: феаа: 20A2, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="af168-139">For example, to send Echo Requests to Host B from the IPv6 address of fe80::210:5aff:feaa:20a2, use the following command:</span></span>

<span data-ttu-id="af168-140">**ping6-s FE80:: 210:5AFF: феаа: 20A2% 4 FE80:: 260:97FF: FE02:6EA5**</span><span class="sxs-lookup"><span data-stu-id="af168-140">**ping6 -s fe80::210:5aff:feaa:20a2%4 fe80::260:97ff:fe02:6ea5**</span></span>

<span data-ttu-id="af168-141">При проверке связи с локальным адресом локальной связи или локальным сайтом рекомендуется указать идентификатор области, чтобы адрес назначения был однозначно неоднозначным.</span><span class="sxs-lookup"><span data-stu-id="af168-141">When pinging a link-local or site-local address, it is recommended to specify the scope-ID to make the destination address unambiguous.</span></span> <span data-ttu-id="af168-142">В нотации для указания идентификатора области используется адрес% Scope-ID.</span><span class="sxs-lookup"><span data-stu-id="af168-142">The notation to specify the scope-ID is address%scope-ID.</span></span> <span data-ttu-id="af168-143">Для адресов локальной связи идентификатор области равен номеру интерфейса, отображаемому в команде IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="af168-143">For link-local addresses, the scope-ID is equal to the interface number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="af168-144">Для локальных адресов сайта идентификатор области равен номеру сайта, отображаемому в команде IPv6 if.</span><span class="sxs-lookup"><span data-stu-id="af168-144">For site-local addresses, the scope-ID is equal to the site number as displayed in the ipv6 if command.</span></span> <span data-ttu-id="af168-145">Например, чтобы отправить сообщения эхо-запросов на узел B с помощью области ID 4, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="af168-145">For example, to send Echo Request messages to Host B using scope-ID 4, use the following command:</span></span>

<span data-ttu-id="af168-146">**ping6 FE80:: 260:97FF: FE02:6EA5% 4**</span><span class="sxs-lookup"><span data-stu-id="af168-146">**ping6 fe80::260:97ff:fe02:6ea5%4**</span></span>

## <a name="related-topics"></a><span data-ttu-id="af168-147">См. также</span><span class="sxs-lookup"><span data-stu-id="af168-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af168-148">Рекомендуемые конфигурации для IPv6</span><span class="sxs-lookup"><span data-stu-id="af168-148">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> </dl>

 

 



