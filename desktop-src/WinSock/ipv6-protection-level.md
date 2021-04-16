---
description: '\_ \_ Параметр сокета уровня защиты IPv6 позволяет разработчикам размещать ограничения доступа к сокетам IPv6.'
ms.assetid: bfb934b3-1e86-431f-a21c-880048d32d35
title: IPV6_PROTECTION_LEVEL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e2a8dd70bb1fb5b21f74f8939f11da0d9e2a3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692281"
---
# <a name="ipv6_protection_level"></a><span data-ttu-id="2b635-103">\_Уровень защиты \_ IPv6</span><span class="sxs-lookup"><span data-stu-id="2b635-103">IPV6\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="2b635-104">\_ \_ Параметр сокета уровня защиты IPv6 позволяет разработчикам размещать ограничения доступа к сокетам IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b635-104">The IPV6\_PROTECTION\_LEVEL socket option enables developers to place access restrictions on IPv6 sockets.</span></span> <span data-ttu-id="2b635-105">Такие ограничения позволяют приложению, работающему в частной локальной сети, просто и надежно защититься от внешних атак.</span><span class="sxs-lookup"><span data-stu-id="2b635-105">Such restrictions enable an application running on a private LAN to simply and robustly harden itself against external attacks.</span></span> <span data-ttu-id="2b635-106">\_ \_ Параметр сокета уровня защиты IPv6 расширяет или ограничивает область действия прослушивающего сокета, обеспечивая неограниченный доступ от общедоступных и частных пользователей при необходимости или ограничивающий доступ только для того же сайта, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="2b635-106">The IPV6\_PROTECTION\_LEVEL socket option widens or narrows the scope of a listening socket, enabling unrestricted access from public and private users when appropriate, or restricting access only to the same site, as required.</span></span>

<span data-ttu-id="2b635-107">\_Уровень защиты IPv6 \_ в настоящее время имеет три определенных уровня защиты.</span><span class="sxs-lookup"><span data-stu-id="2b635-107">IPV6\_PROTECTION\_LEVEL currently has three defined protection levels.</span></span>



| <span data-ttu-id="2b635-108">Уровень защиты</span><span class="sxs-lookup"><span data-stu-id="2b635-108">Protection level</span></span>                                                                                                                                 | <span data-ttu-id="2b635-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2b635-109">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b635-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>\_НЕограниченный уровень защиты \_</span><span class="sxs-lookup"><span data-stu-id="2b635-110"><span id="PROTECTION_LEVEL_UNRESTRICTED"></span><span id="protection_level_unrestricted"></span>PROTECTION\_LEVEL\_UNRESTRICTED</span></span><br/>       | <span data-ttu-id="2b635-111">Используется приложениями, предназначенными для работы в Интернете, включая приложения, использующие преимущества возможностей обхода NAT IPv6, встроенные в Windows (например, Teredo).</span><span class="sxs-lookup"><span data-stu-id="2b635-111">Used by applications designed to operate across the Internet, including applications taking advantage of IPv6 NAT traversal capabilities built into Windows (Teredo, for example).</span></span> <span data-ttu-id="2b635-112">Эти приложения могут обходить брандмауэры протокола IPv4, поэтому они должны быть защищены от атак из Интернета, направленных на открытый порт.</span><span class="sxs-lookup"><span data-stu-id="2b635-112">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/> |
| <span data-ttu-id="2b635-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>\_еджерестриктед уровня \_ защиты</span><span class="sxs-lookup"><span data-stu-id="2b635-113"><span id="PROTECTION_LEVEL_EDGERESTRICTED"></span><span id="protection_level_edgerestricted"></span>PROTECTION\_LEVEL\_EDGERESTRICTED</span></span><br/> | <span data-ttu-id="2b635-114">Используется приложениями, предназначенными для взаимодействия через Интернет.</span><span class="sxs-lookup"><span data-stu-id="2b635-114">Used by applications designed to operate across the Internet.</span></span> <span data-ttu-id="2b635-115">Этот параметр не разрешает обход NAT с помощью реализации Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="2b635-115">This setting does not allow NAT traversal using the Windows Teredo implementation.</span></span> <span data-ttu-id="2b635-116">Эти приложения могут обходить брандмауэры протокола IPv4, поэтому они должны быть защищены от атак из Интернета, направленных на открытый порт.</span><span class="sxs-lookup"><span data-stu-id="2b635-116">These applications may bypass IPv4 firewalls, so applications must be hardened against Internet attacks directed at the opened port.</span></span><br/>                                   |
| <span data-ttu-id="2b635-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>\_ \_ ограниченный уровень защиты</span><span class="sxs-lookup"><span data-stu-id="2b635-117"><span id="PROTECTION_LEVEL_RESTRICTED"></span><span id="protection_level_restricted"></span>PROTECTION\_LEVEL\_RESTRICTED</span></span><br/>             | <span data-ttu-id="2b635-118">Используется приложениями интрасети, которые не реализуют сценарии Интернета.</span><span class="sxs-lookup"><span data-stu-id="2b635-118">Used by intranet applications that do not implement Internet scenarios.</span></span> <span data-ttu-id="2b635-119">Эти приложения обычно не тестируются и не защищаются против атак из Интернета.</span><span class="sxs-lookup"><span data-stu-id="2b635-119">These applications are generally not tested or hardened against Internet-style attacks.</span></span><br/> <span data-ttu-id="2b635-120">Этот параметр ограничивает получаемый трафик локальным.</span><span class="sxs-lookup"><span data-stu-id="2b635-120">This setting will limit the received traffic to link-local only.</span></span><br/>                                                                             |



 

<span data-ttu-id="2b635-121">В следующем примере кода представлены определенные значения для каждого из них:</span><span class="sxs-lookup"><span data-stu-id="2b635-121">The following code example provides the defined values for each:</span></span>

``` syntax
#define PROTECTION_LEVEL_UNRESTRICTED   10  /* for peer-to-peer apps */
#define PROTECTION_LEVEL_EDGERESTRICTED 20  /* Same as unrestricted, except for Teredo  */
#define PROTECTION_LEVEL_RESTRICTED     30  /* for Intranet apps     */
```

<span data-ttu-id="2b635-122">Эти значения являются взаимоисключающими и не могут быть объединены в одном вызове функции [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .</span><span class="sxs-lookup"><span data-stu-id="2b635-122">These values are mutually exclusive, and cannot be combined in a single [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function call.</span></span> <span data-ttu-id="2b635-123">Другие значения для этого параметра сокета зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="2b635-123">Other values for this socket option are reserved.</span></span> <span data-ttu-id="2b635-124">Эти уровни защиты применяются только к входящим подключениям.</span><span class="sxs-lookup"><span data-stu-id="2b635-124">These protection levels apply only to incoming connections.</span></span> <span data-ttu-id="2b635-125">Установка этого параметра сокета не влияет на исходящие пакеты или соединения.</span><span class="sxs-lookup"><span data-stu-id="2b635-125">Setting this socket option has no effect on outbound packets or connections.</span></span>

<span data-ttu-id="2b635-126">В Windows 7 и Windows Server 2008 R2 значение по умолчанию для \_ уровня защиты IPv6 \_ не указано, а **\_ уровень защиты \_ по умолчанию** определен как-1 — недопустимое значение для \_ уровня защиты IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="2b635-126">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="2b635-127">В Windows Vista и Windows Server 2008 значением по умолчанию для \_ уровня защиты IPv6 \_ является **\_ \_ Неограниченный уровень защиты** , а **\_ уровень защиты \_ по умолчанию** определяется равным – 1 — недопустимое значение для \_ уровня защиты IPv6 \_ .</span><span class="sxs-lookup"><span data-stu-id="2b635-127">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to -1, an illegal value for IPV6\_PROTECTION\_LEVEL.</span></span>

<span data-ttu-id="2b635-128">В Windows Server 2003 и Windows XP значением по умолчанию для \_ уровня защиты IPv6 является уровень защиты \_ **\_ \_ еджерестриктед** , **а \_ уровень защиты \_ по умолчанию** — **уровень \_ защиты \_ еджерестриктед**.</span><span class="sxs-lookup"><span data-stu-id="2b635-128">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED** and **PROTECTION\_LEVEL\_DEFAULT** is defined to be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

> [!Note]  
> <span data-ttu-id="2b635-129">\_ \_ Перед привязкой сокета необходимо задать параметр сокета уровня защиты IPv6.</span><span class="sxs-lookup"><span data-stu-id="2b635-129">The IPV6\_PROTECTION\_LEVEL socket option should be set before the socket is bound.</span></span> <span data-ttu-id="2b635-130">В противном случае пакеты, полученные между вызовами [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) и [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) , будут соответствовать **\_ уровню защиты \_ еджерестриктед** и могут быть переданы в приложение.</span><span class="sxs-lookup"><span data-stu-id="2b635-130">Otherwise, packets received between [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) and [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) calls will conform to **PROTECTION\_LEVEL\_EDGERESTRICTED**, and may be delivered to the application.</span></span>

 

<span data-ttu-id="2b635-131">В следующей таблице описан результат применения каждого уровня защиты к сокету прослушивания.</span><span class="sxs-lookup"><span data-stu-id="2b635-131">The following table describes the effect of applying each protection level to a listening socket.</span></span>

<span data-ttu-id="2b635-132">Уровень защиты</span><span class="sxs-lookup"><span data-stu-id="2b635-132">Protection level</span></span>

<span data-ttu-id="2b635-133">Разрешенный входящий трафик</span><span class="sxs-lookup"><span data-stu-id="2b635-133">Incoming traffic permitted</span></span>

<span data-ttu-id="2b635-134">Тот же сайт</span><span class="sxs-lookup"><span data-stu-id="2b635-134">Same site</span></span>

<span data-ttu-id="2b635-135">External</span><span class="sxs-lookup"><span data-stu-id="2b635-135">External</span></span>

<span data-ttu-id="2b635-136">Обход NAT (Teredo)</span><span class="sxs-lookup"><span data-stu-id="2b635-136">NAT traversal (Teredo)</span></span>

<span data-ttu-id="2b635-137">\_ \_ ограниченный уровень защиты</span><span class="sxs-lookup"><span data-stu-id="2b635-137">PROTECTION\_LEVEL\_RESTRICTED</span></span>

<span data-ttu-id="2b635-138">Да</span><span class="sxs-lookup"><span data-stu-id="2b635-138">Yes</span></span>

<span data-ttu-id="2b635-139">Нет</span><span class="sxs-lookup"><span data-stu-id="2b635-139">No</span></span>

<span data-ttu-id="2b635-140">Нет</span><span class="sxs-lookup"><span data-stu-id="2b635-140">No</span></span>

<span data-ttu-id="2b635-141">\_еджерестриктед уровня \_ защиты</span><span class="sxs-lookup"><span data-stu-id="2b635-141">PROTECTION\_LEVEL\_EDGERESTRICTED</span></span>

<span data-ttu-id="2b635-142">Да</span><span class="sxs-lookup"><span data-stu-id="2b635-142">Yes</span></span>

<span data-ttu-id="2b635-143">Да</span><span class="sxs-lookup"><span data-stu-id="2b635-143">Yes</span></span>

<span data-ttu-id="2b635-144">Нет</span><span class="sxs-lookup"><span data-stu-id="2b635-144">No</span></span>

<span data-ttu-id="2b635-145">\_НЕограниченный уровень защиты \_</span><span class="sxs-lookup"><span data-stu-id="2b635-145">PROTECTION\_LEVEL\_UNRESTRICTED</span></span>

<span data-ttu-id="2b635-146">Да</span><span class="sxs-lookup"><span data-stu-id="2b635-146">Yes</span></span>

<span data-ttu-id="2b635-147">Да</span><span class="sxs-lookup"><span data-stu-id="2b635-147">Yes</span></span>

<span data-ttu-id="2b635-148">Да</span><span class="sxs-lookup"><span data-stu-id="2b635-148">Yes</span></span>



 

<span data-ttu-id="2b635-149">В приведенной выше таблице **один и тот же столбец сайта** является сочетанием следующего:</span><span class="sxs-lookup"><span data-stu-id="2b635-149">In the table above, the **Same site** column is a combination of the following:</span></span>

-   <span data-ttu-id="2b635-150">Связывание локальных адресов</span><span class="sxs-lookup"><span data-stu-id="2b635-150">Link local addresses</span></span>
-   <span data-ttu-id="2b635-151">Локальные адреса сайта</span><span class="sxs-lookup"><span data-stu-id="2b635-151">Site Local addresses</span></span>
-   <span data-ttu-id="2b635-152">Глобальные адреса, известные для того же сайта (соответствующие таблице префиксов сайта);</span><span class="sxs-lookup"><span data-stu-id="2b635-152">Global addresses known to belong to the same site (matching the site prefix table)</span></span>

<span data-ttu-id="2b635-153">В Windows 7 и Windows Server 2008 R2 значение по умолчанию для \_ уровня защиты IPv6 \_ не указано.</span><span class="sxs-lookup"><span data-stu-id="2b635-153">On Windows 7 and Windows Server 2008 R2, the default value for IPV6\_PROTECTION\_LEVEL is unspecified.</span></span> <span data-ttu-id="2b635-154">Если на локальном компьютере не установлено программное обеспечение брандмауэра с поддержкой обхода узлов (брандмауэр Windows отключен или установлен какой-либо другой брандмауэр, который игнорирует трафик Teredo), трафик Teredo будет получен только в том случае, если \_ для параметра сокет уровня защиты IPv6 задано значение \_ **\_ \_ Неограниченный уровень защиты**.</span><span class="sxs-lookup"><span data-stu-id="2b635-154">If there is no edge-traversal aware firewall software installed on the local computer (Windows firewall is disabled or some other firewall is installed that ignores Teredo traffic), you will receive Teredo traffic only if you set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="2b635-155">Однако брандмауэр Windows или любая политика брандмауэра с поддержкой обхода краев может игнорировать этот параметр в зависимости от параметров политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2b635-155">However, Windows firewall or any edge-traversal aware firewall policy may ignore this option based on policy settings for the firewall.</span></span> <span data-ttu-id="2b635-156">Если установить этот параметр сокета в состояние **защиты без \_ \_ ограничений**, приложение будет связываться с явной целью получения трафика, обход которого проходит через брандмауэр узла, установленный на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2b635-156">By setting this socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, the application is communicating its explicit intent to receive edge traversed traffic by the host firewall installed on the local machine.</span></span> <span data-ttu-id="2b635-157">Поэтому, если установлен брандмауэр узла с поддержкой обхода узлов, он будет принимать окончательное решение о принятии пакета.</span><span class="sxs-lookup"><span data-stu-id="2b635-157">So if there is an edge-traversal aware host firewall installed, it will have the final decision on accepting a packet.</span></span> <span data-ttu-id="2b635-158">По умолчанию без указания параметра сокета:</span><span class="sxs-lookup"><span data-stu-id="2b635-158">By default, without any socket option set:</span></span>

-   <span data-ttu-id="2b635-159">o Если брандмауэр Windows включен (или установлен другой брандмауэр узла с поддержкой обхода узлов) на локальном компьютере, будет наблюдаться любое принудительное применение.</span><span class="sxs-lookup"><span data-stu-id="2b635-159">o If Windows firewall is enabled (or another edge-traversal aware host firewall is installed) on the local computer, whatever it enforces will be observed.</span></span> <span data-ttu-id="2b635-160">Стандартный брандмауэр узла, поддерживающий обходы узлов, блокирует трафик Teredo по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b635-160">Typical edge-traversal aware host firewall will block Teredo traffic by default.</span></span> <span data-ttu-id="2b635-161">Поэтому приложения будут наблюдать по умолчанию так, как если бы это был **\_ уровень защиты \_ еджерестриктед**.</span><span class="sxs-lookup"><span data-stu-id="2b635-161">Therefore applications will observe the default as if it was **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>
-   <span data-ttu-id="2b635-162">o Если брандмауэр Windows не включен и на локальном компьютере не установлен другой брандмауэр узла с поддержкой пограничной передачи, то по умолчанию будет использоваться **уровень защиты \_ \_ еджерестриктед**.</span><span class="sxs-lookup"><span data-stu-id="2b635-162">o If Windows firewall is not enabled and no other edge-traversal aware host firewall is installed on the local system, the default will be **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span>

<span data-ttu-id="2b635-163">В Windows Vista и Windows Server 2008 значением по умолчанию для \_ уровня защиты IPv6 \_ является **\_ \_ Неограниченный уровень защиты**.</span><span class="sxs-lookup"><span data-stu-id="2b635-163">On Windows Vista and Windows Server 2008, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="2b635-164">Но действующее значение зависит от того, включен ли брандмауэр Windows.</span><span class="sxs-lookup"><span data-stu-id="2b635-164">But the effective value depends on whether Windows firewall is enabled.</span></span> <span data-ttu-id="2b635-165">В брандмауэре Windows учитывается режим обхода, независимо от того, какое значение задано для \_ уровня защиты IPv6 \_ и игнорируется, если уровень защиты IPv6 \_ \_ не **\_ \_ ограничен**.</span><span class="sxs-lookup"><span data-stu-id="2b635-165">The Windows firewall is edge-traversal aware (Teredo aware), no matter what value is set for the IPV6\_PROTECTION\_LEVEL and ignores if IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span> <span data-ttu-id="2b635-166">Поэтому эффективное значение зависит от политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="2b635-166">So the effective value depends on the firewall policy.</span></span> <span data-ttu-id="2b635-167">Если брандмауэр Windows отключен и на локальном компьютере не установлен другой брандмауэр с поддержкой обхода узлов, для уровня защиты IPV6 по умолчанию используется значение \_ \_ **\_ \_ Неограниченный уровень защиты**.</span><span class="sxs-lookup"><span data-stu-id="2b635-167">When Windows firewall is disabled and no other edge-traversal aware firewall is installed on the local computer, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_UNRESTRICTED**.</span></span>

<span data-ttu-id="2b635-168">В Windows Server 2003 и Windows XP значением по умолчанию для \_ уровня защиты IPv6 \_ является **\_ уровень защиты \_ еджерестриктед**.</span><span class="sxs-lookup"><span data-stu-id="2b635-168">On Windows Server 2003 and Windows XP, the default value for IPV6\_PROTECTION\_LEVEL is **PROTECTION\_LEVEL\_EDGERESTRICTED**.</span></span> <span data-ttu-id="2b635-169">Если не установлен \_ \_ параметр сокета уровня защиты IPv6 на **уровень защиты \_ без \_ ограничений**, трафик Teredo не будет получен.</span><span class="sxs-lookup"><span data-stu-id="2b635-169">Unless you have set the IPV6\_PROTECTION\_LEVEL socket option to **PROTECTION\_LEVEL\_UNRESTRICTED**, you would not receive any Teredo traffic.</span></span>

<span data-ttu-id="2b635-170">В зависимости от \_ уровня защиты IPv6 \_ приложение, которому требуется незапрошенный трафик из Интернета, может не получить незапрошенный трафик.</span><span class="sxs-lookup"><span data-stu-id="2b635-170">Depending on the IPV6\_PROTECTION\_LEVEL, an application that requires unsolicited traffic from the Internet may not be capable of receiving unsolicited traffic.</span></span> <span data-ttu-id="2b635-171">Однако эти требования не требуются для получения запрошенного трафика через интерфейс Windows Teredo.</span><span class="sxs-lookup"><span data-stu-id="2b635-171">However, these requirements are not necessary for receiving solicited traffic over the Windows Teredo interface.</span></span> <span data-ttu-id="2b635-172">Дополнительные сведения о взаимодействии с Teredo см. в статье [Получение запрошенного трафика через Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span><span class="sxs-lookup"><span data-stu-id="2b635-172">For more details on the interaction with Teredo, see [Receiving Solicited Traffic Over Teredo](../teredo/receiving-solicited-traffic-over-teredo.md).</span></span>

<span data-ttu-id="2b635-173">Если входящие пакеты или подключения отклоняются из-за установленного уровня защиты, отклонения обрабатываются так, как если бы ни одно приложение не прослушивает этот сокет.</span><span class="sxs-lookup"><span data-stu-id="2b635-173">When incoming packets or connections are refused due to the set protection level, rejection is handled as if no application was listening on that socket.</span></span>

> [!Note]
>
> <span data-ttu-id="2b635-174">\_ \_ Параметр сокета уровня защиты IPv6 не обязательно размещает ограничения доступа для сокетов IPv6 или ОГРАНИЧИВАЕТ обход NAT с помощью какого-либо метода, отличного от Windows Teredo, или даже другой реализации Teredo другим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="2b635-174">The IPV6\_PROTECTION\_LEVEL socket option does not necessarily place access restrictions on IPv6 sockets or restrict NAT traversal using some method other than Windows Teredo or even using another implementation of Teredo by another vendor.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2b635-175">См. также</span><span class="sxs-lookup"><span data-stu-id="2b635-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b635-176">**жетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="2b635-176">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="2b635-177">Получение запрошенного трафика через Teredo</span><span class="sxs-lookup"><span data-stu-id="2b635-177">Receiving Solicited Traffic Over Teredo</span></span>](../teredo/receiving-solicited-traffic-over-teredo.md)
</dt> <dt>

[<span data-ttu-id="2b635-178">**сетсоккопт**</span><span class="sxs-lookup"><span data-stu-id="2b635-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 
