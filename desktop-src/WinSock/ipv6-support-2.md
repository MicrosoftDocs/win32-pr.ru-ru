---
description: Поддержка IPv6, приложение TCP/IP и сокеты Windows.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Поддержка IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145028"
---
# <a name="ipv6-support"></a><span data-ttu-id="b8a59-103">Поддержка IPv6</span><span class="sxs-lookup"><span data-stu-id="b8a59-103">IPv6 Support</span></span>

<span data-ttu-id="b8a59-104">Для поддержки IPv4 и IPv6 в Windows XP с пакетом обновления 1 (SP1) и Windows Server 2003 приложение должно создать два сокета, один сокет для использования с IPv4 и один сокет для использования с IPv6.</span><span class="sxs-lookup"><span data-stu-id="b8a59-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="b8a59-105">Эти два сокета должны обрабатываться отдельно приложением.</span><span class="sxs-lookup"><span data-stu-id="b8a59-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="b8a59-106">Если поставщик услуг TCP/IP в Windows XP с пакетом обновления 1 (SP1) и Windows Server 2003 поддерживает адресацию IPv4 и IPv6, он должен создать два отдельных сокета и прослушивать их отдельно.</span><span class="sxs-lookup"><span data-stu-id="b8a59-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="b8a59-107">Один раз для IPv4.</span><span class="sxs-lookup"><span data-stu-id="b8a59-107">Once for IPv4.</span></span>
-   <span data-ttu-id="b8a59-108">Один раз для семейства IPv6-адресов.</span><span class="sxs-lookup"><span data-stu-id="b8a59-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="b8a59-109">В Windows Vista и более поздних версиях предусмотрена возможность создания одного сокета IPv6, который может поддерживать как трафик IPv6, так и IPv4.</span><span class="sxs-lookup"><span data-stu-id="b8a59-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="b8a59-110">Например, будет создан сокет прослушивания TCP для IPv6, переведен в режим двойного стека и привязан к порту 5001.</span><span class="sxs-lookup"><span data-stu-id="b8a59-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="b8a59-111">Этот сокет с двойным стеком может принимать подключения от TCP-клиентов IPv6, подключающихся к порту 5001, а также от клиентов IPv4 TCP, подключающихся к порту 5001.</span><span class="sxs-lookup"><span data-stu-id="b8a59-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="b8a59-112">Эта функция позволяет значительно упростить проектирование приложений и снизить издержки ресурсов, необходимые для размещения операций на двух отдельных сокетах.</span><span class="sxs-lookup"><span data-stu-id="b8a59-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="b8a59-113">Однако существуют некоторые ограничения, которые должны быть выполнены для использования сокета с двумя стеками.</span><span class="sxs-lookup"><span data-stu-id="b8a59-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="b8a59-114">Дополнительные сведения см. в разделе [сокеты с двойным стеком](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="b8a59-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="b8a59-115">[**Всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) возвращает две структуры [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для каждого поддерживаемого типа сокета ( \_ поток Сокк, СОКК \_ дграм, СОКК \_ RAW).</span><span class="sxs-lookup"><span data-stu-id="b8a59-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="b8a59-116">**Иаддрессфамили** должен иметь значение AF \_ INET для адресации IPv4 и для AF \_ INET6 для адресации IPv6.</span><span class="sxs-lookup"><span data-stu-id="b8a59-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="b8a59-117">IPv6-адреса описаны в следующих структурах.</span><span class="sxs-lookup"><span data-stu-id="b8a59-117">The IPv6 addresses are described in the following structures.</span></span>

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

<span data-ttu-id="b8a59-118">Если приложение использует функции Windows Sockets 1,1 и желает использовать IPv6-адреса, то может продолжать использовать все старые функции, которые принимают структуру [**SOCKADDR**](sockaddr-2.md) в качестве одного из параметров ([**BIND**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto)и [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b8a59-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="b8a59-119">Единственное изменение, которое требуется, — использовать **SOCKADDR \_ in6** вместо **SOCKADDR \_ в**.</span><span class="sxs-lookup"><span data-stu-id="b8a59-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="b8a59-120">Однако функции разрешения имен ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)и т. д.) и функции преобразования адреса ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ нтоа**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) нельзя использовать повторно, так как они предполагают, что IP-адрес имеет длину 4 байта.</span><span class="sxs-lookup"><span data-stu-id="b8a59-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="b8a59-121">Приложение, которое хочет выполнить разрешение имен и преобразование адресов для IPv6-адресов, должно использовать функции Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="b8a59-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="b8a59-122">Реализовано множество новых функций, позволяющих приложениям Windows Sockets 2 использовать преимущества IPv6, включая функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="b8a59-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="b8a59-123">Дополнительные сведения о том, как включить возможности IPv6 в приложении, см. в разделе [руководство по IPv6 для приложений Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="b8a59-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 
