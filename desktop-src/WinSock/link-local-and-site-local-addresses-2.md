---
description: Локальная связь IPv6 и локальные адреса сайта называются адресами с заданной областью.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Локальная связь IPv6 и локальные адреса сайтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701511"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a><span data-ttu-id="ecef1-103">Локальная связь IPv6 и локальные адреса сайтов</span><span class="sxs-lookup"><span data-stu-id="ecef1-103">IPv6 Link-local and Site-local Addresses</span></span>

<span data-ttu-id="ecef1-104">Локальная связь IPv6 и локальные адреса сайта называются адресами с заданной областью.</span><span class="sxs-lookup"><span data-stu-id="ecef1-104">IPv6 link-local and site-local addresses are called scoped addresses.</span></span> <span data-ttu-id="ecef1-105">API сокетов Windows (Winsock) поддерживает элемент **\_ \_ идентификатора области sin6** в структуре [**SOCKADDR \_ in6**](sockaddr-2.md) для использования с адресами в области.</span><span class="sxs-lookup"><span data-stu-id="ecef1-105">The Windows Sockets (Winsock) API supports the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure for use with scoped addresses.</span></span> <span data-ttu-id="ecef1-106">Для локальных адресов IPv6-канала (префикс FE80::/10) элемент **\_ \_ идентификатора области sin6** в структуре **SOCKADDR \_ in6** является номером интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ecef1-106">For IPv6 link-local addresses (fe80::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is the interface number.</span></span> <span data-ttu-id="ecef1-107">Для локальных адресов сайта IPv6 (префикс FEC0::/10) элемент **\_ \_ идентификатора области sin6** в структуре **SOCKADDR \_ in6** является идентификатором сайта.</span><span class="sxs-lookup"><span data-stu-id="ecef1-107">For IPv6 site-local addresses (fec0::/10 prefix), the **sin6\_scope\_id** member in the **sockaddr\_in6** structure is a site identifier.</span></span>

<span data-ttu-id="ecef1-108">Ниже приведен пример локального адреса IPv6 для канала в интерфейсе \# 5.</span><span class="sxs-lookup"><span data-stu-id="ecef1-108">An example of a link-local IPv6 address on interface \#5 is the following:</span></span>

``` syntax
fe80::208:74ff:feda:625c%5
```

<span data-ttu-id="ecef1-109">Следующая команда доступна в Windows XP с пакетом обновления 1 (SP1) и более поздних версий для запроса и настройки IPv6 на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="ecef1-109">The following command is available on Windows XP with Service Pack 1 (SP1) and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="ecef1-110">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="ecef1-110">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="ecef1-111">Изменения конфигурации, выполненные с помощью команд Netsh.exe, являются постоянными и не теряются при перезапуске компьютера или протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="ecef1-111">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="ecef1-112">До выхода Windows XP с пакетом обновления 1 (SP1) Конфигурация IPv6 и управление использовали несколько старых средств командной строки (Net.exe, Ipv6.exe и Ipsec6.exe) для настройки IPv6 и управления им.</span><span class="sxs-lookup"><span data-stu-id="ecef1-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools (Net.exe, Ipv6.exe, and Ipsec6.exe) to configure and manage IPv6.</span></span> <span data-ttu-id="ecef1-113">При использовании этих старых средств изменения IPv6 не являются постоянными и теряются при перезапуске компьютера или протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="ecef1-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span> <span data-ttu-id="ecef1-114">Эти старые средства командной строки поддерживаются только в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ecef1-114">These older command-line tools are only supported on Windows XP.</span></span>

<span data-ttu-id="ecef1-115">В Windows XP с пакетом обновления 1 (SP1) Следующая команда выводит список интерфейсов IPv6 на локальном компьютере, включая индекс интерфейса, имя интерфейса и различные другие свойства интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ecef1-115">On Windows XP with SP1, the following command will display the list of IPv6 interfaces on a local computer including the interface index, the interface name, and various other interface properties.</span></span>

<span data-ttu-id="ecef1-116">**интерфейс netsh interface IPv6 отобразить интерфейс**</span><span class="sxs-lookup"><span data-stu-id="ecef1-116">**netsh interface ipv6 show interface**</span></span>

<span data-ttu-id="ecef1-117">В Windows XP с пакетом обновления 1 (SP1) Следующая команда изменит идентификатор сайта, связанный с индексом интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ecef1-117">On Windows XP with SP1, the following command will change the site identifier associated with an interface index.</span></span>

<span data-ttu-id="ecef1-118">**netsh interface IPv6 Set Interface <InterfaceIndex or Name> ИД сайта = значение**</span><span class="sxs-lookup"><span data-stu-id="ecef1-118">**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**</span></span>

<span data-ttu-id="ecef1-119">В Windows XP Следующая старая команда также изменит идентификатор сайта, связанный с локальным адресом сайта, на 3.</span><span class="sxs-lookup"><span data-stu-id="ecef1-119">On Windows XP, the following older command will also change the site identifier associated with a site-local address to 3.</span></span>

<span data-ttu-id="ecef1-120">**IPv6-рту FEC0::/10 3**</span><span class="sxs-lookup"><span data-stu-id="ecef1-120">**ipv6 rtu fec0::/10 3**</span></span>

<span data-ttu-id="ecef1-121">Если вы отправляете или подключаетесь к адресу с заданной областью, элемент **\_ \_ идентификатора области sin6** в структуре [**SOCKADDR \_ in6**](sockaddr-2.md) может оставаться неопределенным (ноль), который представляет адрес неоднозначной области.</span><span class="sxs-lookup"><span data-stu-id="ecef1-121">If you are sending or connecting to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure can be left unspecified (zero) which represents an ambiguous scoped address.</span></span> <span data-ttu-id="ecef1-122">Например, следующий адрес локальной связи неоднозначен:</span><span class="sxs-lookup"><span data-stu-id="ecef1-122">For example, the following link-local address is ambiguous:</span></span>

``` syntax
fe80::10
```

<span data-ttu-id="ecef1-123">При привязке к адресу в области **sin6 элемент \_ \_ идентификатора области видимости** в структуре [**SOCKADDR \_ in6**](sockaddr-2.md) должен содержать ненулевое значение, указывающее допустимый номер интерфейса для адреса локальной связи или идентификатор сайта для локального адреса сайта.</span><span class="sxs-lookup"><span data-stu-id="ecef1-123">If you are binding to a scoped address, then the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure must contain a nonzero value that specifies a valid interface number for a link-local address or a site identifier for a site-local address.</span></span>

## <a name="ambiguous-scoped-addresses"></a><span data-ttu-id="ecef1-124">Неоднозначные адреса в области</span><span class="sxs-lookup"><span data-stu-id="ecef1-124">Ambiguous Scoped Addresses</span></span>

<span data-ttu-id="ecef1-125">Если вы отправляете или подключаетесь к адресу в области и не указали **элемент \_ \_ идентификатора области sin6** в структуре [**SOCKADDR \_ in6**](sockaddr-2.md) , то адрес в области является неоднозначным.</span><span class="sxs-lookup"><span data-stu-id="ecef1-125">If you are sending or connecting to a scoped address and have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, then the scoped address is ambiguous.</span></span> <span data-ttu-id="ecef1-126">Чтобы устранить эту проблему, протокол IPv6 сначала определяет, привязан ли сокет к исходному адресу.</span><span class="sxs-lookup"><span data-stu-id="ecef1-126">To resolve this, the IPv6 protocol first determines whether you have bound the socket to a source address.</span></span> <span data-ttu-id="ecef1-127">Если это так, привязанный исходный адрес разрешает неоднозначность, предоставляя номер интерфейса или идентификатор сайта.</span><span class="sxs-lookup"><span data-stu-id="ecef1-127">If so, the bound source address resolves the ambiguity by supplying an interface number or site identifier.</span></span>

<span data-ttu-id="ecef1-128">Если вы отправляете или подключаетесь к адресу в области и не указали **элемент \_ \_ идентификатора области sin6** или не привязываете исходный адрес, протокол IPv6 проверяет таблицу маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="ecef1-128">If you are sending or connecting to a scoped address and have neither specified the **sin6\_scope\_id** member nor bound a source address, then the IPv6 protocol checks the routing table.</span></span> <span data-ttu-id="ecef1-129">Например, следующая команда отобразит таблицу маршрутизации IPv6 на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="ecef1-129">For example, the following command will display the IPv6 routing table on a local computer:</span></span>

<span data-ttu-id="ecef1-130">**netsh interface IPv6 отобразить маршрут**</span><span class="sxs-lookup"><span data-stu-id="ecef1-130">**netsh interface ipv6 show route**</span></span>

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

<span data-ttu-id="ecef1-131">Это означает, что адреса локальной связи по умолчанию обрабатываются как ссылки на интерфейс \# 13 и \# 14.</span><span class="sxs-lookup"><span data-stu-id="ecef1-131">This indicates that link-local addresses are treated as on-link to interface \#13 and \#14 by default.</span></span>

<span data-ttu-id="ecef1-132">Неоднозначность возникает, если на локальном компьютере имеется несколько сетевых адаптеров.</span><span class="sxs-lookup"><span data-stu-id="ecef1-132">Ambiguity arises when a local computer has multiple network adapters.</span></span> <span data-ttu-id="ecef1-133">Например, приведенная выше команда **netsh** указывает, что существует два сетевых интерфейса (подключение по локальной сети и беспроводное сетевое подключение).</span><span class="sxs-lookup"><span data-stu-id="ecef1-133">For example, the **netsh** command above indicates there are two network interfaces (Local Area Connection and Wireless Network Connection).</span></span> <span data-ttu-id="ecef1-134">Если в приложении указан адрес локальной ссылки (например, FE80:: 10) без идентификатора области, то не будет ясно, какой адаптер использовать для отправки пакета.</span><span class="sxs-lookup"><span data-stu-id="ecef1-134">When an application specifies a destination link-local address (fe80::10, for example) without a scope ID, it is not clear which adapter to use to send the packet.</span></span> <span data-ttu-id="ecef1-135">При отправке пакета только адрес назначения для адреса локальной связи (FE80::/64) или IPv6 в области действия ссылки (FF00::/8) может пострадать от идентификатора области действия.</span><span class="sxs-lookup"><span data-stu-id="ecef1-135">Only a link-local unicast (fe80::/64) or a link-scope multicast (ff00::/8) IPv6 destination address can suffer from not having a scope ID when sending a packet.</span></span>

## <a name="neighbor-discovery"></a><span data-ttu-id="ecef1-136">Обнаружение окружения</span><span class="sxs-lookup"><span data-stu-id="ecef1-136">Neighbor Discovery</span></span>

<span data-ttu-id="ecef1-137">Если вы не указали элемент **\_ \_ идентификатора области sin6** в структуре [**SOCKADDR \_ in6**](sockaddr-2.md) , не привязываете исходный адрес и не указали маршрут для адресов локальной связи, протокол IPv6 попытается найти соседа по локальному адресу.</span><span class="sxs-lookup"><span data-stu-id="ecef1-137">If you have not specified the **sin6\_scope\_id** member in the [**sockaddr\_in6**](sockaddr-2.md) structure, have not bound a source address, and have not specified a route for link-local addresses, then the IPv6 protocol will try Neighbor Discovery to resolve the destination link-local address.</span></span> <span data-ttu-id="ecef1-138">Для отправляемого пакета выполняется попытка выполнить один интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ecef1-138">For a given packet being sent, one interface is tried.</span></span> <span data-ttu-id="ecef1-139">Первый из предустановленного интерфейса считается наиболее предпочтительным интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="ecef1-139">This first interface that is tried is considered the most preferred interface.</span></span> <span data-ttu-id="ecef1-140">Если при обнаружении соседей не удается разрешить адрес локальной связи в интерфейсе, отправляемый пакет удаляется, а система запоминает, что локальный адрес ссылки на целевой канал недоступен для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ecef1-140">If Neighbor Discovery fails to resolve the link-local address on an interface, the packet to be sent is dropped and the system remembers that the destination link-local address is not reachable over that interface.</span></span> <span data-ttu-id="ecef1-141">В следующем пакете, который будет отправляться при выполнении всех тех же условий, будет предпринята попытка поиска соседей по другому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="ecef1-141">On the next packet to be sent under all of the same conditions, a different interface is tried for Neighbor Discovery.</span></span> <span data-ttu-id="ecef1-142">Этот процесс проходит через каждый интерфейс на локальном компьютере для каждого нового пакета до тех пор, пока обнаружение соседей не ответит на адрес локальной ссылки или если все возможные интерфейсы были выполнены и не прошли.</span><span class="sxs-lookup"><span data-stu-id="ecef1-142">This process continues through each of the interfaces on a local computer for each new packet until Neighbor Discovery responds for the destination link-local address or all of the possible interfaces have been tried and failed.</span></span> <span data-ttu-id="ecef1-143">Каждый раз при попытке разрешить соседу происходит сбой одного интерфейса для этого соседа.</span><span class="sxs-lookup"><span data-stu-id="ecef1-143">Each time an attempt to resolve the neighbor fails, one interface is eliminated for that neighbor.</span></span>

<span data-ttu-id="ecef1-144">Если адрес назначения для локальной ссылки разрешается, то этот интерфейс используется для отправки текущего пакета.</span><span class="sxs-lookup"><span data-stu-id="ecef1-144">If the destination link-local address resolves, then that interface is used to send the current packet.</span></span> <span data-ttu-id="ecef1-145">Этот интерфейс также используется для всех последующих пакетов с неоднозначным ограничением, которые отправляются на тот же адрес назначения локальной связи.</span><span class="sxs-lookup"><span data-stu-id="ecef1-145">This interface is also used for any subsequent ambiguously-scoped packets that are sent to the same link-local destination address.</span></span>

<span data-ttu-id="ecef1-146">Если при обнаружении соседей не удается разрешить конечный адрес локальной ссылки во всех интерфейсах, система пытается отправить пакет на самый предпочтительный интерфейс (первый интерфейс попытался выполнить попытку).</span><span class="sxs-lookup"><span data-stu-id="ecef1-146">If Neighbor Discovery fails to resolve the destination link-local address on all interfaces, the system then tries to send the packet on the most preferred interface (the first interface tried).</span></span> <span data-ttu-id="ecef1-147">Сетевой стек продолжает пытаться разрешить адрес назначения локальной ссылки на наиболее предпочтительном интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ecef1-147">The network stack keeps trying to resolve the destination link-local address on the most preferred interface.</span></span> <span data-ttu-id="ecef1-148">По истечении некоторого периода времени после сбоя обнаружения соседей на всех интерфейсах сетевой стек снова перезагрузит процесс и попытается разрешить адрес локальной ссылки на все интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="ecef1-148">After a period of time after Neighbor Discovery has failed on all interfaces, the network stack will restart the process again and try to resolve the destination link-local address on all of the interfaces.</span></span> <span data-ttu-id="ecef1-149">В настоящее время этот интервал времени снова попытался выполнить обнаружение соседей на всех интерфейсах — 60 секунд.</span><span class="sxs-lookup"><span data-stu-id="ecef1-149">Currently, this time interval when Neighbor Discovery is again tried on all interfaces is 60 seconds.</span></span> <span data-ttu-id="ecef1-150">Однако этот интервал времени может измениться в версиях Windows и не должен предполагаться приложением.</span><span class="sxs-lookup"><span data-stu-id="ecef1-150">However, this time interval may change on versions of Windows and should not be assumed by an application.</span></span>

> [!Note]  
> <span data-ttu-id="ecef1-151">Если приложение привязывает один и тот же адрес локальной связи к другому интерфейсу после того, как обнаружение соседа разрешило адрес локальной связи, он не переопределит интерфейс с адресом локальной связи, возвращенным при поиске соседей.</span><span class="sxs-lookup"><span data-stu-id="ecef1-151">If an application binds the same link-local address to a different interface after Neighbor Discovery has resolved the link-local address, that will not override the interface with the link-local destination address returned by Neighbor Discovery.</span></span>

 

<span data-ttu-id="ecef1-152">Дополнительные сведения об обнаружении соседей для IP версии 6 см. в разделе [RFC4861](https://tools.ietf.org/html/rfc4861) , опубликованный IETF.</span><span class="sxs-lookup"><span data-stu-id="ecef1-152">For more information on Neighbor Discovery for IP version 6, see [RFC4861](https://tools.ietf.org/html/rfc4861) published by the IETF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ecef1-153">См. также</span><span class="sxs-lookup"><span data-stu-id="ecef1-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecef1-154">Префиксы сайта IPv6</span><span class="sxs-lookup"><span data-stu-id="ecef1-154">IPv6 Site Prefixes</span></span>](site-prefixes-2.md)
</dt> <dt>

[<span data-ttu-id="ecef1-155">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="ecef1-155">Ipv6.exe</span></span>](ipv6-exe-2.md)
</dt> <dt>

[<span data-ttu-id="ecef1-156">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="ecef1-156">Netsh.exe</span></span>](netsh-exe.md)
</dt> <dt>

[<span data-ttu-id="ecef1-157">Использование IPv6</span><span class="sxs-lookup"><span data-stu-id="ecef1-157">Using IPv6</span></span>](using-ipv6-2.md)
</dt> </dl>

 

 



