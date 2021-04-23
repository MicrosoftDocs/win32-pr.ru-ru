---
description: 6to4 — это метод подключения узлов или сайтов IPv6 через существующую интернет-инфраструктуру IPv4.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Конфигурация 2: трафик IPv6 между узлами в разных подсетях объединенной сети IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497466"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="93dfe-103">Конфигурация 2: трафик IPv6 между узлами в разных подсетях объединенной сети IPv4 (6to4)</span><span class="sxs-lookup"><span data-stu-id="93dfe-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="93dfe-104">6to4 — это метод подключения узлов или сайтов IPv6 через существующую интернет-инфраструктуру IPv4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="93dfe-105">Он использует уникальный префикс адреса для предоставления изолированным сайтам IPv6 собственного адресного пространства IPv6.</span><span class="sxs-lookup"><span data-stu-id="93dfe-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="93dfe-106">6to4 похож на "псевдо-ISP", предоставляя возможность подключения по протоколу IPv6.</span><span class="sxs-lookup"><span data-stu-id="93dfe-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="93dfe-107">Вы можете использовать 6to4 для прямого взаимодействия с другими сайтами 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="93dfe-108">6to4 не требует использования маршрутизаторов IPv6 и трафика IPv6, инкапсулированного в заголовок IPv4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="93dfe-109">На следующем рисунке показана конфигурация двух узлов в отдельных подсетях с помощью 6to4 для взаимодействия через маршрутизатор IPv4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![узлы, использующие 6to4 для взаимодействия через маршрутизатор IPv4.](images/v6mig-2.png)

<span data-ttu-id="93dfe-111">Основным требованием для использования 6to4 является один глобально маршрутизируемый IPv4-адрес для сайта.</span><span class="sxs-lookup"><span data-stu-id="93dfe-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="93dfe-112">Предположим, что ваш сайт состоит из коллекции компьютеров IPv6, которыми вы управляете (в некоторых системах используется протокол IPv6 Microsoft и некоторые другие реализации IPv6).</span><span class="sxs-lookup"><span data-stu-id="93dfe-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="93dfe-113">Предположим также, что все компьютеры IPv6 подключены напрямую с использованием Ethernet или 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="93dfe-114">Глобальный маршрутизируемый IPv4-адрес должен быть назначен одному из компьютеров, на которых установлен протокол IPv6.</span><span class="sxs-lookup"><span data-stu-id="93dfe-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="93dfe-115">Этот компьютер будет шлюзом 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="93dfe-116">Если у вас есть адрес IPv4, который является частью частного адресного пространства (10.0.0.0/8, 172.16.0.0/12 или 192.168.0.0/16) или адресного пространства автоматического частного IP-адреса (APIPA) 169.254.0.0/16, используемого Windows 2000, он не поддерживает глобальную маршрутизацию.</span><span class="sxs-lookup"><span data-stu-id="93dfe-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="93dfe-117">В противном случае он, вероятно, является общедоступным IP-адресом и поддерживает глобальную маршрутизацию.</span><span class="sxs-lookup"><span data-stu-id="93dfe-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="93dfe-118">См. раздел [Отладка конфигурации 6to4](#debugging-6to4-configuration) в этом документе для получения дополнительной помощи в определении того, поддерживает ли подключение к поставщику услуг Интернета 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="93dfe-119">Средство 6to4cfg.exe</span><span class="sxs-lookup"><span data-stu-id="93dfe-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="93dfe-120">Средство 6to4cfg.exe автоматизирует конфигурацию 6to4, автоматически обнаруживает IPv4-адрес глобальной маршрутизации и создает префикс 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="93dfe-121">Он либо выполняет настройку напрямую, либо может написать скрипт конфигурации, который можно проверить и запустить позже.</span><span class="sxs-lookup"><span data-stu-id="93dfe-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="93dfe-122">Ниже приведен синтаксис команды Basic 6to4cfg.exe.</span><span class="sxs-lookup"><span data-stu-id="93dfe-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="93dfe-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*файлов*\]</span><span class="sxs-lookup"><span data-stu-id="93dfe-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-124">Записывает скрипт конфигурации в файл, если указать имя файла.</span><span class="sxs-lookup"><span data-stu-id="93dfe-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="93dfe-125">В скрипте конфигурации используется Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="93dfe-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="93dfe-126">Можно указать Con в качестве имени файла для записи скрипта конфигурации в выходные данные консоли, что полезно для просмотра 6to4cfg.exe, выполняемых в тестовом сценарии.</span><span class="sxs-lookup"><span data-stu-id="93dfe-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="93dfe-127">Если имя файла не указано, 6to4cfg.exe напрямую обновляет конфигурацию IPv6 на компьютере.</span><span class="sxs-lookup"><span data-stu-id="93dfe-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="93dfe-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="93dfe-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-129">Станет маршрутизатором шлюза 6to4 для вашей локальной сети, что обеспечивает маршрутизацию всех интерфейсов и назначенных префиксов подсети.</span><span class="sxs-lookup"><span data-stu-id="93dfe-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="93dfe-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="93dfe-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-131">Включает адрес локальной адресации сайта на сайте 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="93dfe-132">Эта команда полезна только при использовании совместно с параметром-r.</span><span class="sxs-lookup"><span data-stu-id="93dfe-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="93dfe-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="93dfe-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-134">Указывает, что конфигурация 6to4 должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="93dfe-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="93dfe-135">Таким образом, 6to4cfg-u меняет воздействие 6to4cfg и 6to4cfg-r-u на обратный результат 6to4cfg-r и т. д.</span><span class="sxs-lookup"><span data-stu-id="93dfe-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="93dfe-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *Relay*</span><span class="sxs-lookup"><span data-stu-id="93dfe-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-137">Указывает имя или IPv4-адрес маршрутизатора ретранслятора 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="93dfe-138">Имя по умолчанию — 6to4.ipv6.microsoft.com, маршрутизатор ретранслятора 6to4 в Интернете.</span><span class="sxs-lookup"><span data-stu-id="93dfe-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="93dfe-139"><span id="-b"></span><span id="-B"></span>-б</span><span class="sxs-lookup"><span data-stu-id="93dfe-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-140">Указывает, что 6to4cfg.exe выбирает "лучший" адрес ретранслятора вместо первого.</span><span class="sxs-lookup"><span data-stu-id="93dfe-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="93dfe-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *адрес*</span><span class="sxs-lookup"><span data-stu-id="93dfe-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="93dfe-142">Задает локальный IPv4-адрес для префикса 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="93dfe-143">Настройка 6to4 вручную</span><span class="sxs-lookup"><span data-stu-id="93dfe-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="93dfe-144">В этом примере адресом шлюза 6to4 является 172.31.42.239.</span><span class="sxs-lookup"><span data-stu-id="93dfe-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="93dfe-145">Для использования 6to4 необходим собственный глобально направляемый IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="93dfe-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="93dfe-146">IP-адрес 172.31.42.239 используется только в качестве примера.</span><span class="sxs-lookup"><span data-stu-id="93dfe-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="93dfe-147">Это частный адрес, который не поддерживает глобальную маршрутизацию в Интернете.</span><span class="sxs-lookup"><span data-stu-id="93dfe-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="93dfe-148">32-битный глобально поддерживающий адресацию адрес IPv4 объединяется с 16-разрядным префиксом 2002::/16 для 48 формирования префикса IPv6-адреса для сайта.</span><span class="sxs-lookup"><span data-stu-id="93dfe-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="93dfe-149">В этом примере префиксом сайта 6to4 является 2002: ac1f: 2aef::/48.</span><span class="sxs-lookup"><span data-stu-id="93dfe-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="93dfe-150">Обратите внимание, что ac1f: 2aef — шестнадцатеричная кодировка 172.31.42.239 (разумеется, вы будете использовать другой префикс, основанный на глобально маршрутизируемой IPv4-адресе).</span><span class="sxs-lookup"><span data-stu-id="93dfe-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="93dfe-151">С помощью префикса сайта 6to4 можно назначать адреса и префиксы подсетей внутри сайта.</span><span class="sxs-lookup"><span data-stu-id="93dfe-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="93dfe-152">В этом примере предполагается, что вы используете подсеть 0 для ручной настройки адреса 6to4 на компьютере шлюза 6to4 и используете подсеть 1 для автоматической настройки адресов в сегменте сети Ethernet.</span><span class="sxs-lookup"><span data-stu-id="93dfe-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="93dfe-153">Однако возможны и другие варианты.</span><span class="sxs-lookup"><span data-stu-id="93dfe-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="93dfe-154">Используйте Ipv6.exe, чтобы включить 6to4 на компьютере шлюза 6to4:</span><span class="sxs-lookup"><span data-stu-id="93dfe-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="93dfe-155">**IPv6-рту 2002::/16 2**</span><span class="sxs-lookup"><span data-stu-id="93dfe-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="93dfe-156">Команда **IPv6 рту** выполняет обновление таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="93dfe-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="93dfe-157">Его можно использовать для добавления, удаления или обновления маршрута.</span><span class="sxs-lookup"><span data-stu-id="93dfe-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="93dfe-158">В этом случае он включает 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="93dfe-159">Аргумент 2002::/16 — это префикс маршрута, указывающий уникальный префикс 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="93dfe-160">Аргумент 2 указывает интерфейс по ссылке для этого префикса.</span><span class="sxs-lookup"><span data-stu-id="93dfe-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="93dfe-161">Интерфейс \# 2 — это "псевдо-интерфейс", используемый для настроенных туннелей, автоматического туннелирования и 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="93dfe-162">Если адрес назначения IPv6 соответствует префиксу 2002::/16, то для формирования IPv4-адреса назначения извлекаются биты 32, которые следуют за префиксом в адресе назначения.</span><span class="sxs-lookup"><span data-stu-id="93dfe-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="93dfe-163">Пакет инкапсулируется с помощью заголовка IPv4 и отправляется на адрес назначения IPv4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="93dfe-164">Настройте адрес 6to4 на компьютере шлюза 6to4:</span><span class="sxs-lookup"><span data-stu-id="93dfe-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="93dfe-165">**IPv6 аду 2/2002: ac1f: 2aef:: ac1f: 2aef**</span><span class="sxs-lookup"><span data-stu-id="93dfe-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="93dfe-166">Команда **IPv6 аду** выполняет обновление адреса.</span><span class="sxs-lookup"><span data-stu-id="93dfe-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="93dfe-167">Его можно использовать для добавления, удаления или обновления адреса в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="93dfe-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="93dfe-168">В этом экземпляре настраивается адрес 6to4 компьютера.</span><span class="sxs-lookup"><span data-stu-id="93dfe-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="93dfe-169">Аргумент 2/2002: ac1f: 2aef:: ac1f: 2aef задает как интерфейс, так и адрес.</span><span class="sxs-lookup"><span data-stu-id="93dfe-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="93dfe-170">Для этого требуется настроить адрес 2002: ac1f: 2aef:: ac1f: 2aef в интерфейсе \# 2.</span><span class="sxs-lookup"><span data-stu-id="93dfe-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="93dfe-171">Адрес создается с помощью префикса сайта 2002: ac1f: 2aef::/48, Subnet 0 — префикс подсети 2002: ac1f: 2aef::/64 и идентификатор 64-разрядного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="93dfe-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="93dfe-172">В соглашении показано использование IPv4-адреса компьютера для идентификатора интерфейса, назначенного интерфейсу \# 2.</span><span class="sxs-lookup"><span data-stu-id="93dfe-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="93dfe-173">Для использования ac1f: 2aef следует заменить на шестнадцатеричную кодировку собственного глобально направляемого IPv4-адреса.</span><span class="sxs-lookup"><span data-stu-id="93dfe-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="93dfe-174">Две предыдущие команды достаточно для обеспечения взаимодействия с другими сайтами 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="93dfe-175">Например, можно попробовать проверить связь с сайтом Microsoft 6to4:</span><span class="sxs-lookup"><span data-stu-id="93dfe-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="93dfe-176">**ping6 2002:836b: 9820:: 836b: 9820**</span><span class="sxs-lookup"><span data-stu-id="93dfe-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="93dfe-177">Чтобы обеспечить связь с 6bone, необходимо создать туннель по умолчанию для ретранслятора 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="93dfe-178">Вы можете использовать маршрутизатор ретранслятора Microsoft 6to4, 131.107.152.32:</span><span class="sxs-lookup"><span data-stu-id="93dfe-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="93dfe-179">**IPv6-рту::/0 2/:: 131.107.152.32 Pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="93dfe-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="93dfe-180">Команда **IPv6 рту** выполняет обновление таблицы маршрутизации, устанавливая в этом экземпляре маршрут по умолчанию к ретранслятору 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="93dfe-181">Аргумент::/0 является префиксом маршрута.</span><span class="sxs-lookup"><span data-stu-id="93dfe-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="93dfe-182">Префикс нулевой длины указывает, что это маршрут по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="93dfe-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="93dfe-183">Аргумент 2/:: 131.107.152.32 указывает соседа следующего прыжка для этого префикса.</span><span class="sxs-lookup"><span data-stu-id="93dfe-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="93dfe-184">Для этого необходимо перенаправить пакеты, соответствующие префиксу, на адрес:: 131.107.152.32, используя интерфейс \# 2.</span><span class="sxs-lookup"><span data-stu-id="93dfe-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="93dfe-185">Пересылка пакета в:: 131.107.152.32 в интерфейсе \# 2 приводит к тому, что он инкапсулируется в заголовок v4 и отправляется в 131.107.152.32.</span><span class="sxs-lookup"><span data-stu-id="93dfe-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="93dfe-186">Аргумент Pub делает этот маршрут опубликованным.</span><span class="sxs-lookup"><span data-stu-id="93dfe-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="93dfe-187">Так как это касается только маршрутизаторов, оно не действует, пока не будет включена маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="93dfe-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="93dfe-188">Аналогичным образом время жизни в 30 минут соответствует только в том случае, если включена маршрутизация.</span><span class="sxs-lookup"><span data-stu-id="93dfe-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="93dfe-189">Вы можете получить доступ к сайтам 6bone и сайтам 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="93dfe-190">Чтобы протестировать это, можно использовать следующую команду:</span><span class="sxs-lookup"><span data-stu-id="93dfe-190">You can use the following command to test this:</span></span>

<span data-ttu-id="93dfe-191">**ping6 3FFE: 1CFF: 0: F5:: 1**</span><span class="sxs-lookup"><span data-stu-id="93dfe-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="93dfe-192">Последним шагом является включение маршрутизации на шлюзе 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="93dfe-193">В этом примере предполагается, что интерфейс \# 3 на компьютере шлюза является интерфейсом Ethernet, а интерфейс \# 4 — с 6 по 4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="93dfe-194">Ваш компьютер может по-разному почислить свои интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="93dfe-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="93dfe-195">Следующие две команды присваивают префиксы подсети двум ссылкам.</span><span class="sxs-lookup"><span data-stu-id="93dfe-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="93dfe-196">Префиксы подсети являются производными от префикса 6to4 сайта 2002: ac1f: 2aef::/48:</span><span class="sxs-lookup"><span data-stu-id="93dfe-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="93dfe-197">**IPv6 рту 2002: ac1f: 2aef: 1::/64 3 Pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="93dfe-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="93dfe-198">**IPv6 рту 2002: ac1f: 2aef: 2::/64 4 Pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="93dfe-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="93dfe-199">Команда **IPv6 рту** указывает, что префикс 2002: ac1f: 2aef: 1::/64 — ссылка на интерфейс \# 3.</span><span class="sxs-lookup"><span data-stu-id="93dfe-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="93dfe-200">Он настраивает первый префикс подсети в интерфейсе Ethernet.</span><span class="sxs-lookup"><span data-stu-id="93dfe-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="93dfe-201">Маршрут публикуется со временем существования 30 минут.</span><span class="sxs-lookup"><span data-stu-id="93dfe-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="93dfe-202">Аналогичным образом, префикс 2002: ac1f: 2aef: 2::/64 настраивается в интерфейсе 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="93dfe-203">Следующие три команды позволяют компьютеру шлюза 6to4 работать как маршрутизатор:</span><span class="sxs-lookup"><span data-stu-id="93dfe-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="93dfe-204">**IPv6-ИФК 2 форв**</span><span class="sxs-lookup"><span data-stu-id="93dfe-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="93dfe-205">**IPv6 ИФК 3 форв**</span><span class="sxs-lookup"><span data-stu-id="93dfe-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="93dfe-206">**IPv6 ИФК 4 форв**</span><span class="sxs-lookup"><span data-stu-id="93dfe-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="93dfe-207">Команда **IPv6 ИФК** управляет атрибутами интерфейса.</span><span class="sxs-lookup"><span data-stu-id="93dfe-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="93dfe-208">Маршрутизатор перенаправляет пакеты и отправляет объявления маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="93dfe-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="93dfe-209">В реализации Microsoft IPv6 эти атрибуты каждого интерфейса управляются отдельно.</span><span class="sxs-lookup"><span data-stu-id="93dfe-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="93dfe-210">Интерфейс \# 2 не требуется для рекламы, так как он является псевдо-интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="93dfe-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="93dfe-211">Если у компьютера есть дополнительные интерфейсы, их также следует настроить для перенаправления и рекламы.</span><span class="sxs-lookup"><span data-stu-id="93dfe-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="93dfe-212">После выполнения этих команд протокол IPv6 Microsoft автоматически настраивает адреса в интерфейсах \# 3 и \# 4 с помощью соответствующих префиксов подсети, и два интерфейса начинают отправлять объявления маршрутизатора примерно через 3 – 10 минут.</span><span class="sxs-lookup"><span data-stu-id="93dfe-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="93dfe-213">Узлы, принимающие эти объявления маршрутизатора, автоматически настраивают маршрут по умолчанию и адрес 6to4, полученный из префикса подсети.</span><span class="sxs-lookup"><span data-stu-id="93dfe-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="93dfe-214">Они будут обмениваться данными с другими сайтами 6to4 и 6bone через компьютер шлюза.</span><span class="sxs-lookup"><span data-stu-id="93dfe-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="93dfe-215">Отладка конфигурации 6to4</span><span class="sxs-lookup"><span data-stu-id="93dfe-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="93dfe-216">**Отладка конфигурации 6to4**</span><span class="sxs-lookup"><span data-stu-id="93dfe-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="93dfe-217">Проверьте подключение IPv4 к маршрутизатору ретранслятора 6to4:</span><span class="sxs-lookup"><span data-stu-id="93dfe-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="93dfe-218">**Проверка связи 6to4.ipv6.microsoft.com**</span><span class="sxs-lookup"><span data-stu-id="93dfe-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="93dfe-219">Если это не удается, значит, у вас нет глобальных подключений к Интернету.</span><span class="sxs-lookup"><span data-stu-id="93dfe-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="93dfe-220">Проверка инкапсуляции IPv6 с помощью автоматического туннелирования:</span><span class="sxs-lookup"><span data-stu-id="93dfe-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="93dfe-221">**ping6:: 131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="93dfe-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="93dfe-222">Если это не удается, возможно, имеется брандмауэр или транслятор сетевых адресов (NAT) между компьютером и Интернетом.</span><span class="sxs-lookup"><span data-stu-id="93dfe-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="93dfe-223">В случае успеха подключение к Интернету может поддерживать 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="93dfe-224">Проверьте отображение команды IPv6 RT.</span><span class="sxs-lookup"><span data-stu-id="93dfe-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="93dfe-225">Вы увидите маршрут 2002::/16-> 2.</span><span class="sxs-lookup"><span data-stu-id="93dfe-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="93dfe-226">Проверьте отображение команды IPv6 if 2.</span><span class="sxs-lookup"><span data-stu-id="93dfe-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="93dfe-227">Вы увидите предпочтительный адрес с префиксом 2002::/16.</span><span class="sxs-lookup"><span data-stu-id="93dfe-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="93dfe-228">Адрес IPv4 маршрутизатора ретранслятора Microsoft 6to4 для 131.107.152.32 может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="93dfe-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="93dfe-229">Если шаг 2 выше не работает, проверьте выходные данные команды ping в шаге 1, чтобы проверить IPv4-адрес маршрутизатора ретранслятора Microsoft 6to4.</span><span class="sxs-lookup"><span data-stu-id="93dfe-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="93dfe-230">См. также</span><span class="sxs-lookup"><span data-stu-id="93dfe-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93dfe-231">Рекомендуемые конфигурации для IPv6</span><span class="sxs-lookup"><span data-stu-id="93dfe-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="93dfe-232">Одна подсеть с адресами локальной связи</span><span class="sxs-lookup"><span data-stu-id="93dfe-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="93dfe-233">Использование IPsec между двумя узлами локальной связи</span><span class="sxs-lookup"><span data-stu-id="93dfe-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



