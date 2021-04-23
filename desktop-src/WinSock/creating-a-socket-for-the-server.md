---
description: После инициализации объект СОКЕТа должен быть создан для использования сервером.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Создание сокета для сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145085"
---
# <a name="creating-a-socket-for-the-server"></a><span data-ttu-id="7a534-103">Создание сокета для сервера</span><span class="sxs-lookup"><span data-stu-id="7a534-103">Creating a Socket for the Server</span></span>

<span data-ttu-id="7a534-104">После инициализации объект **сокета** должен быть создан для использования сервером.</span><span class="sxs-lookup"><span data-stu-id="7a534-104">After initialization, a **SOCKET** object must be instantiated for use by the server.</span></span>

<span data-ttu-id="7a534-105">**Создание сокета для сервера**</span><span class="sxs-lookup"><span data-stu-id="7a534-105">**To create a socket for the server**</span></span>

1.  <span data-ttu-id="7a534-106">Функция [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) используется для определения значений в структуре [**SOCKADDR**](sockaddr-2.md) :</span><span class="sxs-lookup"><span data-stu-id="7a534-106">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure:</span></span>

    -   <span data-ttu-id="7a534-107">**AF \_ INET** используется для указания семейства IPv4-адресов.</span><span class="sxs-lookup"><span data-stu-id="7a534-107">**AF\_INET** is used to specify the IPv4 address family.</span></span>
    -   <span data-ttu-id="7a534-108">**Сокк \_ ПОТОК** используется для указания сокета потока.</span><span class="sxs-lookup"><span data-stu-id="7a534-108">**SOCK\_STREAM** is used to specify a stream socket.</span></span>
    -   <span data-ttu-id="7a534-109">**Иппрото \_ Протокол TCP используется** для указания протокола TCP.</span><span class="sxs-lookup"><span data-stu-id="7a534-109">**IPPROTO\_TCP** is used to specify the TCP protocol .</span></span>
    -   <span data-ttu-id="7a534-110">**AI \_ ПАССИВный** флаг указывает, что вызывающий объект планирует использовать возвращенную структуру адреса сокета в вызове функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) .</span><span class="sxs-lookup"><span data-stu-id="7a534-110">**AI\_PASSIVE** flag indicates the caller intends to use the returned socket address structure in a call to the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function.</span></span> <span data-ttu-id="7a534-111">Если флаг **AI \_ passive** установлен и параметр *nodeName* для функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) является **пустым** указателем, часть IP-адреса в структуре адресов сокетов **устанавливается в значение a для адресов \_** IPv4 или **IN6ADDR \_ ANY \_ init** для IPv6-адресов.</span><span class="sxs-lookup"><span data-stu-id="7a534-111">When the **AI\_PASSIVE** flag is set and *nodename* parameter to the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is a **NULL** pointer, the IP address portion of the socket address structure is set to **INADDR\_ANY** for IPv4 addresses or **IN6ADDR\_ANY\_INIT** for IPv6 addresses.</span></span>
    -   <span data-ttu-id="7a534-112">27015 — номер порта, связанного с сервером, к которому будет подключаться клиент.</span><span class="sxs-lookup"><span data-stu-id="7a534-112">27015 is the port number associated with the server that the client will connect to.</span></span>

    <span data-ttu-id="7a534-113">Структура [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) используется функцией [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="7a534-113">The [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure is used by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="7a534-114">Создайте объект **сокета** с именем листенсоккет, чтобы сервер мог прослушивать подключения клиентов.</span><span class="sxs-lookup"><span data-stu-id="7a534-114">Create a **SOCKET** object called ListenSocket for the server to listen for client connections.</span></span>
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  <span data-ttu-id="7a534-115">Вызовите функцию [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и верните ее значение в переменную листенсоккет.</span><span class="sxs-lookup"><span data-stu-id="7a534-115">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ListenSocket variable.</span></span> <span data-ttu-id="7a534-116">Для этого серверного приложения используйте первый IP-адрес, возвращенный вызовом [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , который соответствует семейству адресов, типу сокета и протоколу, указанным в параметре *указания* .</span><span class="sxs-lookup"><span data-stu-id="7a534-116">For this server application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="7a534-117">В этом примере был запрошен сокет потока TCP для IPv4 с семейством адресов IPv4, типом сокета \_ потока Сокк и протоколом иппрото \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="7a534-117">In this example, a TCP stream socket for IPv4 was requested with an address family of IPv4, a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="7a534-118">Поэтому для Листенсоккет запрашивается IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="7a534-118">So an IPv4 address is requested for the ListenSocket.</span></span>

    <span data-ttu-id="7a534-119">Если серверное приложение ожидает передачи данных по протоколу IPv6, для семейства адресов необходимо задать значение AF \_ INET6 в параметре *указания* .</span><span class="sxs-lookup"><span data-stu-id="7a534-119">If the server application wants to listen on IPv6, then the address family needs to be set to AF\_INET6 in the *hints* parameter.</span></span> <span data-ttu-id="7a534-120">Если сервер желает прослушивать как IPv6, так и IPv4, необходимо создать два сокета прослушивания: один для IPv6 и один для IPv4.</span><span class="sxs-lookup"><span data-stu-id="7a534-120">If a server wants to listen on both IPv6 and IPv4, two listen sockets must be created, one for IPv6 and one for IPv4.</span></span> <span data-ttu-id="7a534-121">Эти два сокета должны обрабатываться отдельно приложением.</span><span class="sxs-lookup"><span data-stu-id="7a534-121">These two sockets must be handled separately by the application.</span></span>

    <span data-ttu-id="7a534-122">Windows Vista и более поздних версий предлагают возможность создания одного сокета IPv6, который находится в режиме двойного стека, для прослушивания как IPv6, так и IPv4.</span><span class="sxs-lookup"><span data-stu-id="7a534-122">Windows Vista and later offer the ability to create a single IPv6 socket that is put in dual stack mode to listen on both IPv6 and IPv4.</span></span> <span data-ttu-id="7a534-123">Дополнительные сведения об этой функции см. в разделе [сокеты с двойным стеком](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="7a534-123">For more information on this feature, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  <span data-ttu-id="7a534-124">Проверьте наличие ошибок, чтобы убедиться, что сокет является допустимым сокетом.</span><span class="sxs-lookup"><span data-stu-id="7a534-124">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="7a534-125">Следующий шаг: [Привязка сокета](binding-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="7a534-125">Next Step: [Binding a Socket](binding-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a534-126">См. также</span><span class="sxs-lookup"><span data-stu-id="7a534-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a534-127">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="7a534-127">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="7a534-128">Инициализация Winsock</span><span class="sxs-lookup"><span data-stu-id="7a534-128">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="7a534-129">Серверное приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="7a534-129">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> </dl>

 

 
