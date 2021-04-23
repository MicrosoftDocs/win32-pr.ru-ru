---
description: Обратите внимание, что все функции 1,1 сокетов Windows для разрешения имен относятся только к сетям TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692303"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="e0ae0-103">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="e0ae0-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="e0ae0-104">Все функции 1,1 сокетов Windows для разрешения имен относятся только к сетям TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="e0ae0-105">Разработчикам приложений настоятельно не рекомендуется продолжать использовать эти функции, связанные с транспортом, которые поддерживают только IPv4.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="e0ae0-106">Разработчики приложений должны использовать следующие функции, которые не зависят от протокола и поддерживают разрешение имен IPv6 и IPv4.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="e0ae0-107">**функцию getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="e0ae0-108">**жетаддринфоекс**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="e0ae0-109">**жетаддринфов**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="e0ae0-110">**жетнамеинфо**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="e0ae0-111">**жетнамеинфов**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="e0ae0-112">Сокеты Windows 1,1 определяют ряд подпрограмм, используемых для разрешения имен с помощью сетей TCP/IP (IP версии 4).</span><span class="sxs-lookup"><span data-stu-id="e0ae0-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="e0ae0-113">Они иногда называются **жетксбии** функциями и включают следующее:</span><span class="sxs-lookup"><span data-stu-id="e0ae0-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="e0ae0-114">**имя узла**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="e0ae0-115">**жесостбяддр**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="e0ae0-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="e0ae0-117">**жетпротобинаме**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="e0ae0-118">**жетпротобинумбер**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="e0ae0-119">**жетсервбинаме**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="e0ae0-120">**жетсервбипорт**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="e0ae0-121">Также определены асинхронные версии этих функций.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="e0ae0-122">**всаасинкжесостбяддр**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="e0ae0-123">**всаасинкжесостбинаме**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="e0ae0-124">**всаасинкжетпротобинаме**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="e0ae0-125">**всаасинкжетпротобинумбер**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="e0ae0-126">**всаасинкжетсервбинаме**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="e0ae0-127">**всаасинкжетсервбипорт**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="e0ae0-128">Существуют также две функции, реализованные в Winsock2.dll, которые используются для преобразования точечной нотации IPv4-адресов в строковые и двоичные представления соответственно.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="e0ae0-129">**INET \_ АДР**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="e0ae0-130">**INET \_ нтоа**</span><span class="sxs-lookup"><span data-stu-id="e0ae0-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="e0ae0-131">Для обеспечения исключительной обратной совместимости с сокетами Windows 1,1 все старые функции только с протоколом IPv4 продолжают поддерживаться до тех пор, пока имеется хотя бы один поставщик пространства имен, поддерживающий \_ семейство адресов inet (эти функции не относятся к IP версии 6, обозначенной AF \_ INET6).</span><span class="sxs-lookup"><span data-stu-id="e0ae0-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="e0ae0-132">32.dll Ws2 \_ реализует эти функции совместимости с точки зрения нового, независимого от протокола имени средства разрешения имен с помощью соответствующей последовательности вызовов функций [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End** .</span><span class="sxs-lookup"><span data-stu-id="e0ae0-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="e0ae0-133">Ниже приведены сведения о сопоставлении функций **жетксбии** с функциями разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="e0ae0-134">WSs2 \_32.dll обрабатывает различия между асинхронной и синхронной версиями функций **жетксбии** , поэтому обсуждаются только реализации синхронных функций **жетксбии** .</span><span class="sxs-lookup"><span data-stu-id="e0ae0-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="e0ae0-135">В этом разделе описывается совместимое разрешение имен для TCP/IP в API-интерфейсе Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="e0ae0-136">В следующем списке перечислены подразделы этого раздела.</span><span class="sxs-lookup"><span data-stu-id="e0ae0-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="e0ae0-137">Базовый подход для Жетксбии в API</span><span class="sxs-lookup"><span data-stu-id="e0ae0-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="e0ae0-138">Функции жетпротобинаме и жетпротобинумбер в API</span><span class="sxs-lookup"><span data-stu-id="e0ae0-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="e0ae0-139">Функции жетсервбинаме и жетсервбипорт в API</span><span class="sxs-lookup"><span data-stu-id="e0ae0-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="e0ae0-140">Функция GetHostByName в API</span><span class="sxs-lookup"><span data-stu-id="e0ae0-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="e0ae0-141">Функция жесостбяддр в API</span><span class="sxs-lookup"><span data-stu-id="e0ae0-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="e0ae0-142">Функция onhostname в API</span><span class="sxs-lookup"><span data-stu-id="e0ae0-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="e0ae0-143">См. также</span><span class="sxs-lookup"><span data-stu-id="e0ae0-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0ae0-144">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="e0ae0-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="e0ae0-145">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="e0ae0-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
