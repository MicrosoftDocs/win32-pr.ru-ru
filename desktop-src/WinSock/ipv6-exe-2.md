---
description: Все настройки IPv6 выполняются с помощью средства Ipv6.exe.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263069"
---
# <a name="ipv6exe"></a><span data-ttu-id="6875c-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="6875c-103">Ipv6.exe</span></span>

<span data-ttu-id="6875c-104">Все настройки IPv6 выполняются с помощью средства Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="6875c-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="6875c-105">Это средство в основном используется для запросов и настройки интерфейсов IPv6, адресов, кэшей и маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6875c-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="6875c-106">Ниже приведены подкоманды IPv6.</span><span class="sxs-lookup"><span data-stu-id="6875c-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="6875c-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6, если** \[ наличии\#\]</span><span class="sxs-lookup"><span data-stu-id="6875c-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-108">Отображает сведения об интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="6875c-108">Displays information about interfaces.</span></span> <span data-ttu-id="6875c-109">Если указан номер интерфейса, отображается только информация об этом интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="6875c-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="6875c-110">В противном случае отображаются сведения обо всех интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="6875c-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="6875c-111">Выходные данные включают адрес канального уровня интерфейса и список IPv6-адресов, назначенных интерфейсу, включая текущий MTU интерфейса и максимальный (true) MTU, который может поддерживать интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6875c-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="6875c-112">Интерфейс \# 1 — это псевдо-интерфейс, используемый для замыкания на себя.</span><span class="sxs-lookup"><span data-stu-id="6875c-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="6875c-113">Интерфейс \# 2 — это псевдо-интерфейс, используемый для настроенного туннелирования, автоматического туннелирования и туннелирования 6to4.</span><span class="sxs-lookup"><span data-stu-id="6875c-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="6875c-114">Другие интерфейсы нумеруются последовательно в порядке их создания.</span><span class="sxs-lookup"><span data-stu-id="6875c-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="6875c-115">Этот порядок меняется от одного компьютера к другому.</span><span class="sxs-lookup"><span data-stu-id="6875c-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="6875c-116">Адреса канального уровня в *AA* - *BB* - *CC* - *дд*/с -  - форматом *FF* — это адреса Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6875c-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="6875c-117">Адрес уровня связи *в.* *б*. *в*. *d* — это интерфейсы с 6 по 4.</span><span class="sxs-lookup"><span data-stu-id="6875c-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="6875c-118">Дополнительные сведения о 6-over-4 см. в RFC 2529.</span><span class="sxs-lookup"><span data-stu-id="6875c-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="6875c-119">Два псевдо-интерфейса не используют обнаружение соседей IPv6.</span><span class="sxs-lookup"><span data-stu-id="6875c-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ИФК IPv6** , если \# \[ Пересылка \] \[ объявлений \] \[ -переслано \] \[ -объявлений \] \[ MTU \# байт сайт \] \[ -идентификатор\]</span><span class="sxs-lookup"><span data-stu-id="6875c-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-121">Управляет атрибутами интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-121">Controls interface attributes.</span></span> <span data-ttu-id="6875c-122">Интерфейсы могут пересылаться, в этом случае они пересылают пакеты с адресами назначения, не назначенными интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="6875c-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="6875c-123">Интерфейсы можно объявлять, в этом случае они отправляют объявления маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6875c-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="6875c-124">Эти атрибуты могут управляться независимо друг от друга.</span><span class="sxs-lookup"><span data-stu-id="6875c-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="6875c-125">Интерфейс либо отправляет запросы маршрутизатора и получает объявления маршрутизатора, либо получает запросы маршрутизатора и отправляет объявления маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6875c-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="6875c-126">Поскольку два псевдо-интерфейса не используют обнаружение соседей, они не могут быть настроены для отправки объявлений маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6875c-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="6875c-127">Пересылка может быть сокращена как форв и объявлена как расширенная.</span><span class="sxs-lookup"><span data-stu-id="6875c-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="6875c-128">Также можно задать MTU для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="6875c-129">Новое значение MTU должно быть меньше или равно максимальному значению MTU (true) канала (по протоколу IPv6, если) и больше или равно минимальному значению параметра IPv6 MTU (1280 байт).</span><span class="sxs-lookup"><span data-stu-id="6875c-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="6875c-130">Идентификатор сайта для интерфейса также можно изменить.</span><span class="sxs-lookup"><span data-stu-id="6875c-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="6875c-131">Идентификаторы сайтов используются в \_ поле идентификатора области sin6 \_ с адресами, локальными для сайта.</span><span class="sxs-lookup"><span data-stu-id="6875c-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IPv6 IFD** , если\#</span><span class="sxs-lookup"><span data-stu-id="6875c-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="6875c-133">Удаляет интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6875c-133">Deletes an interface.</span></span> <span data-ttu-id="6875c-134">Невозможно удалить петлевой и туннельный псевдо-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="6875c-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**IPv6 NC** \[ Если \# \[ адрес\]\]</span><span class="sxs-lookup"><span data-stu-id="6875c-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-136">Отображает содержимое кэша соседей.</span><span class="sxs-lookup"><span data-stu-id="6875c-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="6875c-137">Если указан номер интерфейса, то отображаются только содержимое кэша соседей этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="6875c-138">В противном случае отображаются содержимое всех кэшей соседей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="6875c-139">Если указан интерфейс, можно указать IPv6-адрес для вывода только этой записи кэша соседей.</span><span class="sxs-lookup"><span data-stu-id="6875c-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="6875c-140">Для каждой записи кэша соседей отображаются интерфейс, адрес IPv6, адрес канального уровня и состояние REACH.</span><span class="sxs-lookup"><span data-stu-id="6875c-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**НКФ IPv6** \[ Если \# \[ адрес\]\]</span><span class="sxs-lookup"><span data-stu-id="6875c-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-142">Очищает указанные записи кэша соседей.</span><span class="sxs-lookup"><span data-stu-id="6875c-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="6875c-143">Очищаются только записи кэша соседей без ссылок.</span><span class="sxs-lookup"><span data-stu-id="6875c-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="6875c-144">Так как записи кэша маршрутов содержат ссылки на записи кэша соседей, кэш маршрутов должен быть сброшен первыми.</span><span class="sxs-lookup"><span data-stu-id="6875c-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="6875c-145">Записи таблицы маршрутизации также могут содержать ссылки на записи кэша соседей.</span><span class="sxs-lookup"><span data-stu-id="6875c-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**версия-кандидат IPv6** \[ Если \# адрес\]</span><span class="sxs-lookup"><span data-stu-id="6875c-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-147">Отображает содержимое кэша маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6875c-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="6875c-148">Кэш маршрутов — это имя реализации IPv6 для целевого кэша.</span><span class="sxs-lookup"><span data-stu-id="6875c-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="6875c-149">Если указан интерфейс и адрес, отображается запись кэша маршрутов для достижения адреса через интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6875c-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="6875c-150">В противном случае отображаются все записи кэша маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6875c-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="6875c-151">Для каждой записи кэша маршрутов отображаются адрес IPv6 и текущий интерфейс следующего прыжка и адрес соседнего узла.</span><span class="sxs-lookup"><span data-stu-id="6875c-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="6875c-152">Предпочтительный исходный адрес для использования с этим назначением, текущий MTU для достижения этого места назначения через интерфейс и определение того, является ли это записью кэша для конкретного интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="6875c-153">Для адреса назначения также отображается любой адрес (для мобильных устройств).</span><span class="sxs-lookup"><span data-stu-id="6875c-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="6875c-154">Адрес назначения может иметь несколько записей кэша маршрутов — столько же, сколько один для каждого исходящего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="6875c-155">Однако адрес назначения может иметь не более одной записи кэша маршрутов, которая не зависит от интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="6875c-156">Конкретный интерфейс — запись кэша маршрутов используется только в том случае, если приложение явно указывает на исходящий интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6875c-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Если \# \[ адрес\]\]</span><span class="sxs-lookup"><span data-stu-id="6875c-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-158">Очищает указанные записи кэша маршрутов.</span><span class="sxs-lookup"><span data-stu-id="6875c-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**IPv6 BC**</span><span class="sxs-lookup"><span data-stu-id="6875c-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="6875c-160">Отображает содержимое кэша привязки, в котором содержатся привязки между домашними адресами и адресами для мобильных устройств IPv6.</span><span class="sxs-lookup"><span data-stu-id="6875c-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="6875c-161">Для каждой привязки отображаются домашний адрес, адрес для ввода в конце, порядковый номер привязки и время существования.</span><span class="sxs-lookup"><span data-stu-id="6875c-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**аду IPv6** , если \# /Аддресс \[ время существования Корпоративная \[ \] \] \[ \] \[ рассылка ключом/pl рассылки\]</span><span class="sxs-lookup"><span data-stu-id="6875c-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-163">Добавляет или удаляет назначение адресов одноадресной рассылки или адреса многоадресной рассылки в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="6875c-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="6875c-164">Адрес одноадресной рассылки действует, если не указано пустое значение.</span><span class="sxs-lookup"><span data-stu-id="6875c-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="6875c-165">Если значение не указано, время существования бесконечно.</span><span class="sxs-lookup"><span data-stu-id="6875c-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="6875c-166">Если указано только допустимое время существования, предпочтительное время жизни равно допустимому времени существования.</span><span class="sxs-lookup"><span data-stu-id="6875c-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="6875c-167">Можно указать бесконечное время жизни или конечное значение в секундах.</span><span class="sxs-lookup"><span data-stu-id="6875c-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="6875c-168">Предпочтительное время существования должно быть меньше или равно допустимому времени существования.</span><span class="sxs-lookup"><span data-stu-id="6875c-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="6875c-169">Задание нулевого времени жизни приводит к удалению адреса.</span><span class="sxs-lookup"><span data-stu-id="6875c-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="6875c-170">Вы можете сократить время существования в течение срока жизни.</span><span class="sxs-lookup"><span data-stu-id="6875c-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="6875c-171">Для адресов многоадресной рассылки единственными допустимыми значениями времени жизни являются нуль и Infinite.</span><span class="sxs-lookup"><span data-stu-id="6875c-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**СПТ IPv6**</span><span class="sxs-lookup"><span data-stu-id="6875c-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="6875c-173">Отображает текущее содержимое таблицы префиксов сайта.</span><span class="sxs-lookup"><span data-stu-id="6875c-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="6875c-174">Для каждого префикса сайта команда отображает префикс, интерфейс, к которому применяется префикс сайта, и время существования префикса в секундах.</span><span class="sxs-lookup"><span data-stu-id="6875c-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="6875c-175">Префиксы сайта обычно настраиваются в объявлениях маршрутизатора по-своему.</span><span class="sxs-lookup"><span data-stu-id="6875c-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="6875c-176">Они используются в функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) для фильтрации недопустимых адресов локального сайта.</span><span class="sxs-lookup"><span data-stu-id="6875c-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>префикс **IPv6 СПУ** , если \# \[ время жизни L\]</span><span class="sxs-lookup"><span data-stu-id="6875c-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-178">Добавляет, удаляет или обновляет префикс в таблице префиксов сайта.</span><span class="sxs-lookup"><span data-stu-id="6875c-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="6875c-179">Требуется префикс и номер интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6875c-179">The prefix and interface number are required.</span></span> <span data-ttu-id="6875c-180">Время существования префикса сайта, указанное в секундах, по умолчанию равно бесконечности, если не указано.</span><span class="sxs-lookup"><span data-stu-id="6875c-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="6875c-181">При указании нулевого времени жизни префикс сайта удаляется.</span><span class="sxs-lookup"><span data-stu-id="6875c-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="6875c-182">Эта команда не требуется для обычной конфигурации узлов или маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="6875c-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**IPv6 RT**</span><span class="sxs-lookup"><span data-stu-id="6875c-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="6875c-184">Отображает текущее содержимое таблицы маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="6875c-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="6875c-185">Для каждой записи таблицы маршрутизации команда отображает префикс маршрута, интерфейс связи или соседа следующего прыжка в интерфейсе, значение предпочтения (с меньшим приоритетом) и время существования в секундах.</span><span class="sxs-lookup"><span data-stu-id="6875c-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="6875c-186">Записи таблицы маршрутизации также могут иметь атрибуты **публикации** и **устаревания** .</span><span class="sxs-lookup"><span data-stu-id="6875c-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="6875c-187">По умолчанию они возрастают (время существования меньше, чем оставшаяся константа) и не публикуются (не используются при формировании объявлений маршрутизатора).</span><span class="sxs-lookup"><span data-stu-id="6875c-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="6875c-188">Для узлов записи таблицы маршрутизации обычно настраиваются в объявлениях маршрутизатора по-своему.</span><span class="sxs-lookup"><span data-stu-id="6875c-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="6875c-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>префикс **IPv6 рту** , если \# \[ /некссоп \] \[ время жизни L \] \[ предпочтение P \] \[ Публикация \] \[ возраст \] \[ СПЛ сайт-длина префикса\]</span><span class="sxs-lookup"><span data-stu-id="6875c-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="6875c-190">Добавляет или удаляет маршрут в таблице маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="6875c-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="6875c-191">Требуется префикс маршрута.</span><span class="sxs-lookup"><span data-stu-id="6875c-191">The route prefix is required.</span></span> <span data-ttu-id="6875c-192">Префикс может быть ссылкой на указанный интерфейс или следующий прыжок, указанный с адресом соседа в интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="6875c-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="6875c-193">Маршрут может иметь время существования в секундах, с бесконечным значением по умолчанию и предпочтением со значением по умолчанию 0 или наиболее предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="6875c-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="6875c-194">При указании нулевого времени жизни маршрут удаляется.</span><span class="sxs-lookup"><span data-stu-id="6875c-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="6875c-195">Если маршрут указан как опубликованный, указывая, что он будет использоваться при создании объявлений маршрутизатора, это не возрастет.</span><span class="sxs-lookup"><span data-stu-id="6875c-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="6875c-196">Время существования маршрута не учитывается, поэтому оно фактически бесконечно, но значение используется в объявлениях маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6875c-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="6875c-197">При необходимости маршрут может быть указан как опубликованный маршрут, который также возрастает.</span><span class="sxs-lookup"><span data-stu-id="6875c-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="6875c-198">Неопубликованный маршрут по умолчанию всегда возрастает.</span><span class="sxs-lookup"><span data-stu-id="6875c-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="6875c-199">Необязательный подпараметр СПЛ можно использовать для указания длины префикса сайта, связанной с маршрутом.</span><span class="sxs-lookup"><span data-stu-id="6875c-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="6875c-200">Длина префикса сайта используется только при отправке объявлений маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="6875c-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="6875c-201">Время жизни может быть сокращено как жизненный, предпочтения как преф и опубликовано как Pub.</span><span class="sxs-lookup"><span data-stu-id="6875c-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



