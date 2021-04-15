---
description: Появились новые функции интерфейса сокетов Windows, специально разработанные для упрощения программирования Windows Sockets. Одно из преимуществ этих новых функций сокетов Windows — интегрированная поддержка IPv6 и IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Вызовы функций для IPv6-приложений Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701526"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="9a71b-104">Вызовы функций для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="9a71b-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="9a71b-105">Появились новые функции интерфейса сокетов Windows, специально разработанные для упрощения программирования Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9a71b-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="9a71b-106">Одно из преимуществ этих новых функций сокетов Windows — интегрированная поддержка IPv6 и IPv4.</span><span class="sxs-lookup"><span data-stu-id="9a71b-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="9a71b-107">К этим новым функциям сокетов Windows относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="9a71b-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="9a71b-108">**WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="9a71b-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="9a71b-109">**всаконнектбилист**</span><span class="sxs-lookup"><span data-stu-id="9a71b-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="9a71b-110">семейство функций [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**функцию getaddrinfo**, [**жетаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**жетаддринфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**фриаддринфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**фриаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**фриаддринфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)и [**сетаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span><span class="sxs-lookup"><span data-stu-id="9a71b-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="9a71b-111">семейство функций [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**жетнамеинфо** и [**жетнамеинфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span><span class="sxs-lookup"><span data-stu-id="9a71b-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="9a71b-112">Кроме того, добавлены новые вспомогательные функции IP с поддержкой IPv6 и IPv4 для упрощения программирования Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="9a71b-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="9a71b-113">К этим новым вспомогательным функциям IP относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="9a71b-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="9a71b-114">**жетадаптерсаддрессес**</span><span class="sxs-lookup"><span data-stu-id="9a71b-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="9a71b-115">При добавлении поддержки IPv6 в приложение следует использовать следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="9a71b-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="9a71b-116">Используйте [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) , чтобы установить подключение к конечной точке по заданному имени узла и порту.</span><span class="sxs-lookup"><span data-stu-id="9a71b-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="9a71b-117">Функция **WSAConnectByName** доступна в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9a71b-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="9a71b-118">Используйте [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) , чтобы установить соединение с одной из коллекций возможных конечных точек, представленных набором адресов назначения (имен узлов и портов).</span><span class="sxs-lookup"><span data-stu-id="9a71b-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="9a71b-119">Функция **всаконнектбилист** доступна в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9a71b-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="9a71b-120">Замените вызовы функции [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) вызовами одной из новых функций сокетов Windows [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="9a71b-121">Функция **функцию getaddrinfo** с поддержкой протокола IPv6 доступна в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9a71b-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="9a71b-122">Протокол IPv6 также поддерживается в Windows 2000 при установке предварительной версии технологии IPv6 для Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9a71b-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="9a71b-123">Замените вызовы функции [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) вызовами одной из новых функций сокетов Windows [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="9a71b-124">Функция **жетнамеинфо** с поддержкой протокола IPv6 доступна в Windows XP и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="9a71b-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="9a71b-125">Протокол IPv6 также поддерживается в Windows 2000 при установке предварительной версии технологии IPv6 для Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9a71b-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="9a71b-126">WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="9a71b-126">WSAConnectByName</span></span>

<span data-ttu-id="9a71b-127">Функция [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) упрощает подключение к конечной точке с помощью сокета на основе потока с заданным именем узла или IP-адресом назначения (IPv4 или IPv6).</span><span class="sxs-lookup"><span data-stu-id="9a71b-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="9a71b-128">Эта функция сокращает исходный код, необходимый для создания приложения IP, которое не зависит от используемой версии протокола IP.</span><span class="sxs-lookup"><span data-stu-id="9a71b-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="9a71b-129">**WSAConnectByName** заменяет следующие шаги в типичном приложении TCP на вызов одной функции:</span><span class="sxs-lookup"><span data-stu-id="9a71b-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="9a71b-130">Разрешение имени узла в набор IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="9a71b-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="9a71b-131">Для каждого IP-адреса:</span><span class="sxs-lookup"><span data-stu-id="9a71b-131">For each IP address:</span></span>
    -   <span data-ttu-id="9a71b-132">Создайте сокет соответствующего семейства адресов.</span><span class="sxs-lookup"><span data-stu-id="9a71b-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="9a71b-133">Пытается подключиться к удаленному IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="9a71b-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="9a71b-134">Если соединение прошло успешно, возвращается значение; в противном случае будет предпринята попытка следующего удаленного IP-адреса узла.</span><span class="sxs-lookup"><span data-stu-id="9a71b-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="9a71b-135">Функция [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) выходит за пределы простого разрешения имени, а затем пытается подключиться.</span><span class="sxs-lookup"><span data-stu-id="9a71b-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="9a71b-136">Функция использует все удаленные адреса, возвращенные разрешением имен, и все исходные IP-адреса локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="9a71b-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="9a71b-137">Сначала он пытается подключиться с использованием пар адресов с наибольшей вероятностью успеха.</span><span class="sxs-lookup"><span data-stu-id="9a71b-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="9a71b-138">Таким образом, **WSAConnectByName** не только гарантирует, что соединение будет установлено по возможности, но также снизит время, необходимое для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="9a71b-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="9a71b-139">Чтобы включить обмен данными по протоколам IPv6 и IPv4, используйте следующий метод:</span><span class="sxs-lookup"><span data-stu-id="9a71b-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="9a71b-140">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должна вызываться на сокете, созданном для \_ семейства адресов AF INET6, чтобы отключить параметр сокета **IPv6 \_ V6ONLY** перед вызовом [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span><span class="sxs-lookup"><span data-stu-id="9a71b-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="9a71b-141">Это достигается путем вызова функции **сетсоккопт** на сокете с параметром *Level* , для которого задано значение **иппрото \_ IPv6** (см. раздел [ \_ параметры сокета IPv6 иппрото](ipproto-ipv6-socket-options.md)), параметр *optname* установлен в **IPv6 \_ V6ONLY**, а параметр *оптвалуе* установлен в значение 0.</span><span class="sxs-lookup"><span data-stu-id="9a71b-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="9a71b-142">Если приложению требуется выполнить привязку к определенному локальному адресу или порту, [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) использовать нельзя, так как параметр сокета **WSAConnectByName** должен быть несвязанным сокетом.</span><span class="sxs-lookup"><span data-stu-id="9a71b-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="9a71b-143">В приведенном ниже примере кода для использования этой функции требуется всего несколько строк кода, чтобы реализовать приложение, которое не зависит от версии IP.</span><span class="sxs-lookup"><span data-stu-id="9a71b-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="9a71b-144">Установка соединения с помощью [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="9a71b-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a><span data-ttu-id="9a71b-145">всаконнектбилист</span><span class="sxs-lookup"><span data-stu-id="9a71b-145">WSAConnectByList</span></span>

<span data-ttu-id="9a71b-146">Функция [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) устанавливает соединение с узлом, используя набор возможных узлов (представленный НАБОРОМ IP-адресов и портов назначения).</span><span class="sxs-lookup"><span data-stu-id="9a71b-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="9a71b-147">Функция принимает все IP-адреса и порты для конечной точки и всех IP-адресов локального компьютера и пытается подключиться с использованием всех возможных сочетаний адресов.</span><span class="sxs-lookup"><span data-stu-id="9a71b-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="9a71b-148">[**Всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) связан с функцией [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="9a71b-149">Вместо того, чтобы брать одно имя узла, **всаконнектбилист** принимает список узлов (адреса назначения и пары портов) и подключается к одному из адресов и портов из предоставленного списка.</span><span class="sxs-lookup"><span data-stu-id="9a71b-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="9a71b-150">Эта функция предназначена для поддержки сценариев, в которых приложение должно подключаться к любому доступному узлу из списка потенциальных узлов.</span><span class="sxs-lookup"><span data-stu-id="9a71b-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="9a71b-151">Как и в случае с [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), функция [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) значительно сокращает исходный код, необходимый для создания, привязки и подключения сокета.</span><span class="sxs-lookup"><span data-stu-id="9a71b-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="9a71b-152">Эта функция значительно упрощает реализацию приложения, которое не зависит от версии IP.</span><span class="sxs-lookup"><span data-stu-id="9a71b-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="9a71b-153">Список адресов для узла, принимаемого этой функцией, может быть адресами IPv6 или IPv4.</span><span class="sxs-lookup"><span data-stu-id="9a71b-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="9a71b-154">Чтобы разрешить передачу адресов IPv6 и IPv4 в одном списке адресов, принятом функцией, необходимо выполнить следующие действия перед вызовом функции:</span><span class="sxs-lookup"><span data-stu-id="9a71b-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="9a71b-155">Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должна вызываться на сокете, созданном для \_ семейства адресов AF INET6, чтобы отключить параметр сокета **IPv6 \_ V6ONLY** перед вызовом [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span><span class="sxs-lookup"><span data-stu-id="9a71b-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="9a71b-156">Это достигается путем вызова функции **сетсоккопт** на сокете с параметром *Level* , для которого задано значение **иппрото \_ IPv6** (см. раздел [ \_ параметры сокета IPv6 иппрото](ipproto-ipv6-socket-options.md)), параметр *optname* установлен в **IPv6 \_ V6ONLY**, а параметр *оптвалуе* установлен в значение 0.</span><span class="sxs-lookup"><span data-stu-id="9a71b-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="9a71b-157">Все адреса IPv4 должны быть представлены в формате IPv6-адресов, сопоставленном с IPv4, что позволяет приложению только для IPv6 взаимодействовать с узлом IPv4.</span><span class="sxs-lookup"><span data-stu-id="9a71b-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="9a71b-158">Формат IPv6-адресов, сопоставленный с IPv4, позволяет представить адрес IPv4 узла IPv4 в качестве адреса IPv6.</span><span class="sxs-lookup"><span data-stu-id="9a71b-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="9a71b-159">Адрес IPv4 кодируется в младшие биты 32 IPv6-адреса, а старшие биты 96 содержат фиксированный префикс 0:0: 0:0: 0: FFFF.</span><span class="sxs-lookup"><span data-stu-id="9a71b-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="9a71b-160">Формат IPv6-адреса, сопоставленный с IPv4, указан в RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="9a71b-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="9a71b-161">Дополнительные сведения см. в разделе [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span><span class="sxs-lookup"><span data-stu-id="9a71b-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="9a71b-162">Макрос IN6ADDR \_ SETV4MAPPED в *мсткпип. h* можно использовать для преобразования адреса IPv4 в требуемый формат IPv6-адресов, сопоставленный с IPv4.</span><span class="sxs-lookup"><span data-stu-id="9a71b-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="9a71b-163">Установка соединения с помощью [ **всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="9a71b-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a><span data-ttu-id="9a71b-164">функцию getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="9a71b-164">getaddrinfo</span></span>

<span data-ttu-id="9a71b-165">Функция **функцию getaddrinfo** также выполняет обработку многих функций.</span><span class="sxs-lookup"><span data-stu-id="9a71b-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="9a71b-166">Ранее для создания, открытия, а затем привязки адреса к сокету были вызваны вызовы к числу функций сокетов Windows.</span><span class="sxs-lookup"><span data-stu-id="9a71b-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="9a71b-167">С помощью функции **функцию getaddrinfo** строки исходного кода, необходимые для выполнения такой работы, могут значительно снизиться.</span><span class="sxs-lookup"><span data-stu-id="9a71b-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="9a71b-168">В следующих двух примерах показан исходный код, необходимый для выполнения этих задач с функцией **функцию getaddrinfo** и без нее.</span><span class="sxs-lookup"><span data-stu-id="9a71b-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="9a71b-169">Выполнение открытия, подключения и привязки с помощью **функцию getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="9a71b-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="9a71b-170">Выполнение открытия, подключения и привязки без использования **функцию getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="9a71b-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="9a71b-171">Обратите внимание, что оба этих примера исходного кода выполняют те же задачи, но в первом примере с использованием функции **функцию getaddrinfo** меньше строк исходного кода и могут работать с адресами IPv6 или IPv4.</span><span class="sxs-lookup"><span data-stu-id="9a71b-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="9a71b-172">Количество строк исходного кода, исключенных с помощью функции **функцию getaddrinfo** , может быть различным.</span><span class="sxs-lookup"><span data-stu-id="9a71b-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="9a71b-173">В рабочем исходном коде приложение будет выполнять итерацию по набору адресов, возвращенных функцией [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) или [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="9a71b-174">Эти примеры пропускают этот шаг в пользу простоты.</span><span class="sxs-lookup"><span data-stu-id="9a71b-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="9a71b-175">Другая ошибка, которую необходимо решить при изменении существующего приложения IPv4 для поддержки IPv6, связано с порядком, в котором вызываются функции.</span><span class="sxs-lookup"><span data-stu-id="9a71b-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="9a71b-176">Для [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) требуется, чтобы последовательность вызовов функций была выполнена в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="9a71b-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="9a71b-177">На платформах, где используются IPv4 и IPv6, семейство адресов удаленного узла не известно заранее.</span><span class="sxs-lookup"><span data-stu-id="9a71b-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="9a71b-178">Чтобы определить IP-адрес и семейство адресов удаленного узла, необходимо сначала выполнить разрешение адресов с помощью функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="9a71b-179">Затем можно вызвать функцию [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , чтобы открыть сокет семейства адресов, возвращенный [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span><span class="sxs-lookup"><span data-stu-id="9a71b-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="9a71b-180">Это важное изменение в том, как написаны приложения Windows Sockets, так как многие приложения IPv4 обычно используют разный порядок вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="9a71b-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="9a71b-181">Большинство приложений IPv4 сначала создают сокет для \_ семейства адресов AF INET, затем выполняют разрешение имен, а затем используют сокет для подключения к разрешенному IP-адресу.</span><span class="sxs-lookup"><span data-stu-id="9a71b-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="9a71b-182">При создании таких приложений с поддержкой IPv6 вызов функции [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) должен быть отложен до разрешения имени после того, как семейство адресов детереминед.</span><span class="sxs-lookup"><span data-stu-id="9a71b-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="9a71b-183">Обратите внимание, что если разрешение имен Возвращает адреса IPv4 и IPv6, для подключения к этим адресам назначения необходимо использовать отдельные сокеты IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="9a71b-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="9a71b-184">Все эти сложности можно избежать с помощью функции [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) в Windows Vista и более поздних версий, поэтому разработчикам приложений рекомендуется использовать эту новую функцию.</span><span class="sxs-lookup"><span data-stu-id="9a71b-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="9a71b-185">В следующем примере кода показана правильная последовательность для выполнения разрешения имен (выполняется в четвертой строке в следующем примере исходного кода), а затем открывается сокет (выполняется в 19-<sup>й</sup> строке в следующем примере кода).</span><span class="sxs-lookup"><span data-stu-id="9a71b-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="9a71b-186">Этот пример является выдержкой из файла Client. c, который находится в [коде клиента с поддержкой IPv6](ipv6-enabled-client-code-2.md) в приложении б. Функция Принтеррор, вызываемая в следующем примере кода, указана в примере Client. c.</span><span class="sxs-lookup"><span data-stu-id="9a71b-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a><span data-ttu-id="9a71b-187">Функции IP Helper</span><span class="sxs-lookup"><span data-stu-id="9a71b-187">IP Helper Functions</span></span>

<span data-ttu-id="9a71b-188">Наконец, приложения, использующие вспомогательную функцию IP [**жетадаптерсинфо**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)и связанную со связанной структурой [**\_ \_ сведения о IP-адаптере**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), должны распознать, что эта функция и структура ограничены адресами IPv4.</span><span class="sxs-lookup"><span data-stu-id="9a71b-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="9a71b-189">Замены с поддержкой IPv6 для этой функции и структуры являются функцией [**жетадаптерсаддрессес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) и структурой [**IP- \_ адаптеров \_**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="9a71b-190">Приложения с поддержкой IPv6, использующие API вспомогательной функции IP, должны использовать функцию **жетадаптерсаддрессес** и соответствующую структуру **IP- \_ \_ адресов адаптера** с поддержкой IPv6, определенную в пакете средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9a71b-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="9a71b-191">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="9a71b-191">Recommendations</span></span>

<span data-ttu-id="9a71b-192">Лучший подход к обеспечению того, чтобы приложение использовало вызовы функций, совместимых с IPv6, — использовать функцию [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) для получения преобразования "узел-адрес".</span><span class="sxs-lookup"><span data-stu-id="9a71b-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="9a71b-193">Начиная с Windows XP функция **функцию getaddrinfo** делает функцию [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) ненужной, поэтому приложение должно использовать функцию **функцию getaddrinfo** вместо этого для будущих проектов программирования.</span><span class="sxs-lookup"><span data-stu-id="9a71b-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="9a71b-194">Хотя корпорация Майкрософт продолжит поддерживать **gethostbyname**, эта функция не будет расширена для поддержки IPv6.</span><span class="sxs-lookup"><span data-stu-id="9a71b-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="9a71b-195">Для прозрачной поддержки получения сведений об узле IPv6 и IPv4 необходимо использовать **функцию getaddrinfo**.</span><span class="sxs-lookup"><span data-stu-id="9a71b-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="9a71b-196">В следующем примере показано, как лучше использовать функцию **функцию getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="9a71b-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="9a71b-197">Обратите внимание, что функция, которая правильно используется в этом примере, обрабатывает преобразование адреса IPv6 и IPv4 в правильном формате, но также получает другие полезные сведения об узле, например поддерживаемые типы сокетов.</span><span class="sxs-lookup"><span data-stu-id="9a71b-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="9a71b-198">Этот пример является выдержкой из примера Client. c, который находится в приложении б.</span><span class="sxs-lookup"><span data-stu-id="9a71b-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> <span data-ttu-id="9a71b-199">Версия функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , поддерживающей IPv6, является новой для выпуска Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a71b-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="9a71b-200">Код, чтобы избежать</span><span class="sxs-lookup"><span data-stu-id="9a71b-200">Code to Avoid</span></span>

<span data-ttu-id="9a71b-201">Преобразование адресов узлов традиционно было достигнуто с помощью функции [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="9a71b-202">Начиная с Windows XP:</span><span class="sxs-lookup"><span data-stu-id="9a71b-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="9a71b-203">Функция **функцию getaddrinfo** делает функцию **gethostbyname** устаревшей.</span><span class="sxs-lookup"><span data-stu-id="9a71b-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="9a71b-204">Приложения должны использовать функцию **функцию getaddrinfo** вместо функции **gethostbyname** .</span><span class="sxs-lookup"><span data-stu-id="9a71b-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="9a71b-205">Задачи кодирования</span><span class="sxs-lookup"><span data-stu-id="9a71b-205">Coding Tasks</span></span>

<span data-ttu-id="9a71b-206">**Изменение существующего приложения IPv4 для добавления поддержки IPv6**</span><span class="sxs-lookup"><span data-stu-id="9a71b-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="9a71b-207">Получите служебную программу Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="9a71b-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="9a71b-208">Эта служебная программа устанавливается как часть Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9a71b-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="9a71b-209">Windows SDK доступен по подписке MSDN. ее также можно загрузить с веб-сайта Майкрософт ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="9a71b-210">Более старая версия средства *Checkv4.exe* была также включена в состав предварительной версии Microsoft IPv6 Technology Preview для Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9a71b-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="9a71b-211">Запустите служебную программу *Checkv4.exe* для своего кода.</span><span class="sxs-lookup"><span data-stu-id="9a71b-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="9a71b-212">Сведения о запуске программы версии для файлов см. в разделе [Использование служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="9a71b-213">Программа предупреждает о том, как использовать [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)и другие функции, предназначенные только для IPv4, и предоставляет рекомендации по их замене функциями, совместимыми с IPv6, такими как [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span><span class="sxs-lookup"><span data-stu-id="9a71b-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="9a71b-214">Замените все экземпляры функции **gethostbyname** и соответствующий код соответствующим образом с помощью функции **функцию getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="9a71b-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="9a71b-215">В Windows Vista при необходимости используйте функцию [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) или [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="9a71b-216">Замените все экземпляры функции [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) и соответствующий код соответствующим образом с помощью функции [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="9a71b-217">Кроме того, можно выполнить поиск экземпляров функций **gethostbyname** и [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) в базе кода, а также изменить все такое использование (и другой связанный код соответственно) на функции **функцию getaddrinfo** и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="9a71b-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a71b-218">См. также</span><span class="sxs-lookup"><span data-stu-id="9a71b-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a71b-219">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="9a71b-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="9a71b-220">Изменение структур данных для IPv6 Winsock Аппикатионс</span><span class="sxs-lookup"><span data-stu-id="9a71b-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="9a71b-221">Сокеты с двумя стеками для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="9a71b-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="9a71b-222">Использование жестко закодированных IPv4-адресов</span><span class="sxs-lookup"><span data-stu-id="9a71b-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="9a71b-223">Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="9a71b-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="9a71b-224">Базовые протоколы для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="9a71b-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
