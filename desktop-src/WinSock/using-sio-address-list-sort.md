---
description: Запрос IOCTL с помощью \_ списка адресов SIO \_ \_ позволяет разработчикам приложений сортировать список адресов назначения IPv6 и IPv4, чтобы определить лучший доступный адрес для создания подключения. Запрос \_ \_ ioctl списка адресов SIO \_ поддерживается в Windows XP и более поздних версиях.
ms.assetid: bf380ddf-8171-4ef4-be47-94c7a6aabf0a
title: Использование SIO_ADDRESS_LIST_SORT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6452023b69ccf72c78b393c5059fee497997af51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272243"
---
# <a name="using-sio_address_list_sort"></a><span data-ttu-id="a2514-104">Использование функции \_ \_ сортировки списка \_ адресов SIO</span><span class="sxs-lookup"><span data-stu-id="a2514-104">Using SIO\_ADDRESS\_LIST\_SORT</span></span>

<span data-ttu-id="a2514-105">Запрос IOCTL с помощью **\_ \_ списка адресов \_ SIO** позволяет разработчикам приложений сортировать список адресов назначения IPv6 и IPv4, чтобы определить лучший доступный адрес для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="a2514-105">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL allows application developers to sort a list of IPv6 and IPv4 destination addresses to determine the best available address for making a connection.</span></span> <span data-ttu-id="a2514-106">Запрос **ioctl \_ \_ списка адресов \_ SIO** поддерживается в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a2514-106">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

<span data-ttu-id="a2514-107">В Windows Vista и более поздних версиях функция [**креатесортедаддресспаирс**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) принимает предоставленный список возможных IP-адресов назначения, пары адресов назначения с ЛОКАЛЬНЫМИ IP-адресами главного компьютера и сортирует пары в соответствии с тем, какая пара адресов лучше всего подходит для обмена данными между двумя одноранговыми узлами.</span><span class="sxs-lookup"><span data-stu-id="a2514-107">On Windows Vista and later, the [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.</span></span> <span data-ttu-id="a2514-108">Функцию **креатесортедаддресспаирс** следует использовать вместо **\_ списка адресов SIO \_ \_ Сортировать** ioctl в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a2514-108">The **CreateSortedAddressPairs** function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span>

<span data-ttu-id="a2514-109">В следующих разделах описываются рекомендации по использованию **для \_ \_ \_ сортировки списка адресов SIO**.</span><span class="sxs-lookup"><span data-stu-id="a2514-109">The following sections describe usage considerations for **SIO\_ADDRESS\_LIST\_SORT**.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2514-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2514-110">Parameters</span></span>

<span data-ttu-id="a2514-111">Буфер, переданный **в \_ \_ список адресов \_ SIO** , является структурой [**\_ \_ списка адресов сокетов**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a2514-111">The buffer passed to **SIO\_ADDRESS\_LIST\_SORT** is a [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure.</span></span> <span data-ttu-id="a2514-112">Каждый [**\_ адрес сокета**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) в списке должен быть в \_ формате SOCKADDR IN6.</span><span class="sxs-lookup"><span data-stu-id="a2514-112">Each [**SOCKET\_ADDRESS**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) in the list must be in SOCKADDR\_IN6 format.</span></span>

<span data-ttu-id="a2514-113">При **\_ \_ \_ сортировке по списку адресов SIO** ioctl выполняет сортировку адресов IPv6 и IPv4 в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a2514-113">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts both IPv6 and IPv4 addresses on Windows Vista and later.</span></span> <span data-ttu-id="a2514-114">Все адреса IPv4 в списке должны быть отсортированы в формате IPv6-адреса, сопоставленного с IPv4.</span><span class="sxs-lookup"><span data-stu-id="a2514-114">Any IPv4 addresses in the list to be sorted must be in the IPv4-mapped IPv6 address format.</span></span> <span data-ttu-id="a2514-115">Дополнительные сведения о формате IPv6-адресов, сопоставленных с IPv4, см. в разделе [сокеты с двойным стеком](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="a2514-115">For more information on the IPv4-mapped IPv6 address format, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="a2514-116">В Windows Server 2003 и Windows XP в **\_ \_ списке \_ адресов SIO** сортируются только адреса IPv6.</span><span class="sxs-lookup"><span data-stu-id="a2514-116">On Windows Server 2003, and Windows XP, **SIO\_ADDRESS\_LIST\_SORT** sorts only IPv6 addresses.</span></span> <span data-ttu-id="a2514-117">Адреса IPv4 в формате IPv6-адресов, сопоставленных с IPv4, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a2514-117">IPv4 addresses in the IPv4-mapped IPv6 address format are not supported.</span></span>

<span data-ttu-id="a2514-118">В выходных данных элемент **иаддресскаунт** структуры [**\_ \_ списка адресов сокетов**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) может быть меньше, чем при вводе, если код ioctl определяет, что некоторые адреса назначения недопустимы.</span><span class="sxs-lookup"><span data-stu-id="a2514-118">On output, the **iAddressCount** member of the [**SOCKET\_ADDRESS\_LIST**](/previous-versions/windows/desktop/legacy/aa385467(v=vs.85)) structure may be smaller than on input if the IOCTL code determines that some destination addresses are invalid.</span></span>

## <a name="sorting-determination"></a><span data-ttu-id="a2514-119">Определение сортировки</span><span class="sxs-lookup"><span data-stu-id="a2514-119">Sorting Determination</span></span>

<span data-ttu-id="a2514-120">Порядок сортировки адресов IPv6 для \_ списка адресов SIO \_ \_ Сортировка ioctl выполняется на основе таблицы префиксной политики.</span><span class="sxs-lookup"><span data-stu-id="a2514-120">The sorting order for IPv6 addresses for the SIO\_ADDRESS\_LIST\_SORT IOCTL is based on the prefix policy table.</span></span> <span data-ttu-id="a2514-121">Таблица политик префиксов настраивается с помощью служебной программы командной строки *Netsh.exe* .</span><span class="sxs-lookup"><span data-stu-id="a2514-121">The prefix policy table is configured using the *Netsh.exe* command line utility.</span></span> <span data-ttu-id="a2514-122">Следующие фрагменты командной строки иллюстрируют основные команды конфигурации таблицы политики префикса *Netsh.exe* :</span><span class="sxs-lookup"><span data-stu-id="a2514-122">The following command line snippets illustrate basic *Netsh.exe* prefix policy table configuration commands:</span></span>

``` syntax
netsh interface ipv6 show prefixpolicies
netsh interface ipv6 add prefixpolicy ::/96 3 4
netsh interface ipv6 delete prefixpolicy ::/96
netsh interface ipv6 set prefixpolicy ::/96 3 4
```

> [!Note]  
> <span data-ttu-id="a2514-123">В Windows Server 2003 и Windows XP первая команда Netsh, указанная выше, была описана ниже.</span><span class="sxs-lookup"><span data-stu-id="a2514-123">On Windows Server 2003 and Windows XP, the first netsh command listed above was as follows.</span></span> <span data-ttu-id="a2514-124">Все остальные связанные команды одинаковы.</span><span class="sxs-lookup"><span data-stu-id="a2514-124">All other related commands are the same.</span></span>

 

``` syntax
netsh interface ipv6 show prefixpolicy
```

<span data-ttu-id="a2514-125">Порядок адресов также определяется алгоритмом, описанным в RFC 3484 по *адресу по умолчанию для протокола IPv6* , опубликованного IETF.</span><span class="sxs-lookup"><span data-stu-id="a2514-125">Address ordering is also determined by an algorithm outlined in the RFC 3484 on *Default Address Selection for Internet Protocol version 6 (IPv6)* published by the IETF.</span></span> <span data-ttu-id="a2514-126">Дополнительные сведения см. на веб-сайте [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span><span class="sxs-lookup"><span data-stu-id="a2514-126">For more information, see [https://www.ietf.org/rfc/rfc3484.txt](https://tools.ietf.org/html/rfc3484).</span></span> <span data-ttu-id="a2514-127">(Этот ресурс может быть доступен только на английском языке.)</span><span class="sxs-lookup"><span data-stu-id="a2514-127">(This resource may only be available in English.)</span></span>

<span data-ttu-id="a2514-128">В **\_ списке адресов SIO при \_ \_ сортировке** через ioctl сортируются адреса от лучших к наихудшим, а при необходимости заполняется членами **\_ \_ идентификатора области sin6** .</span><span class="sxs-lookup"><span data-stu-id="a2514-128">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL sorts addresses from best to worst, and fills in **sin6\_scope\_id** members, if needed.</span></span> <span data-ttu-id="a2514-129">Для локальных адресов сайта \_ Сортировка списка адресов SIO \_ \_ либо заполняется идентификатором области, либо удаляет адрес.</span><span class="sxs-lookup"><span data-stu-id="a2514-129">For site-local addresses, SIO\_ADDRESS\_LIST\_SORT either fills in the scope-id, or removes the address.</span></span>

<span data-ttu-id="a2514-130">При **\_ \_ \_ сортировке списка адресов SIO** по протоколу ioctl игнорируется исходный адрес, привязанный к сокету, и выполняется сортировка только по списку адресов назначения, переданному в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="a2514-130">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL ignores the source address bound to the socket and only sorts by the destination address list passed as a parameter.</span></span>

<span data-ttu-id="a2514-131">Функцию [**креатесортедаддресспаирс**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) следует использовать вместо **\_ списка адресов SIO \_ \_ Сортировать** ioctl в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a2514-131">The [**CreateSortedAddressPairs**](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs) function should be used instead of the **SIO\_ADDRESS\_LIST\_SORT** IOCTL on Windows Vista and later.</span></span> <span data-ttu-id="a2514-132">Функция **креатесортедаддресспаирс** возвращает список пар адресов, содержащих локальный исходный адрес и адрес назначения.</span><span class="sxs-lookup"><span data-stu-id="a2514-132">The **CreateSortedAddressPairs** function returns a list of address pairs that contains a local source address and a destination address.</span></span> <span data-ttu-id="a2514-133">Это позволяет приложению использовать правильный исходный адрес для каждого адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="a2514-133">This provides an application the correct source address to use for each destination address.</span></span> <span data-ttu-id="a2514-134">Приложение также может фильтровать результаты путем поиска определенного исходного адреса.</span><span class="sxs-lookup"><span data-stu-id="a2514-134">An application can also filter the results by looking for a specific source address.</span></span> <span data-ttu-id="a2514-135">в результатах.</span><span class="sxs-lookup"><span data-stu-id="a2514-135">in the results.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2514-136">Требования</span><span class="sxs-lookup"><span data-stu-id="a2514-136">Requirements</span></span>

<span data-ttu-id="a2514-137">В файле заголовка *Winsock2. h* задан запрос IOCTL с **\_ \_ \_ сортировкой списка адресов SIO** .</span><span class="sxs-lookup"><span data-stu-id="a2514-137">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="a2514-138">В пакете средств разработки программного обеспечения Microsoft Windows (SDK), выпущенном для Windows Vista и более поздних версий, изменилась Организация файлов заголовков, а в файле заголовка *Ws2def. h* задано значение ioctl **\_ \_ \_ Sort List списка адресов SIO** .</span><span class="sxs-lookup"><span data-stu-id="a2514-138">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and **SIO\_ADDRESS\_LIST\_SORT** IOCTL is defined in the *Ws2def.h* header file.</span></span> <span data-ttu-id="a2514-139">Обратите внимание, что файл заголовка *Ws2def. h* автоматически включается в *Winsock2. h* и никогда не должен использоваться напрямую.</span><span class="sxs-lookup"><span data-stu-id="a2514-139">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

<span data-ttu-id="a2514-140">Запрос **ioctl \_ \_ списка адресов \_ SIO** поддерживается в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a2514-140">The **SIO\_ADDRESS\_LIST\_SORT** IOCTL is supported on Windows XP and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2514-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a2514-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2514-142">**креатесортедаддресспаирс**</span><span class="sxs-lookup"><span data-stu-id="a2514-142">**CreateSortedAddressPairs**</span></span>](/windows/win32/api/netioapi/nf-netioapi-createsortedaddresspairs)
</dt> </dl>

 

 
