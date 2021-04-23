---
description: После инициализации необходимо создать экземпляр объекта СОКЕТа для использования клиентом.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Создание сокета для клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897345"
---
# <a name="creating-a-socket-for-the-client"></a><span data-ttu-id="932f9-103">Создание сокета для клиента</span><span class="sxs-lookup"><span data-stu-id="932f9-103">Creating a socket for the client</span></span>

<span data-ttu-id="932f9-104">После инициализации необходимо создать экземпляр объекта **сокета** для использования клиентом.</span><span class="sxs-lookup"><span data-stu-id="932f9-104">After initialization, a **SOCKET** object must be instantiated for use by the client.</span></span>

<span data-ttu-id="932f9-105">**Создание сокета**</span><span class="sxs-lookup"><span data-stu-id="932f9-105">**To create a socket**</span></span>

1.  <span data-ttu-id="932f9-106">Объявите объект [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) , содержащий структуру [**SOCKADDR**](sockaddr-2.md) , и инициализируйте эти значения.</span><span class="sxs-lookup"><span data-stu-id="932f9-106">Declare an [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) object that contains a [**sockaddr**](sockaddr-2.md) structure and initialize these values.</span></span> <span data-ttu-id="932f9-107">Для этого приложения семейство Интернет-адресов не указано, чтобы можно было вернуть адрес IPv6 или IPv4.</span><span class="sxs-lookup"><span data-stu-id="932f9-107">For this application, the Internet address family is unspecified so that either an IPv6 or IPv4 address can be returned.</span></span> <span data-ttu-id="932f9-108">Приложение запрашивает тип сокета в качестве сокета потока для протокола TCP.</span><span class="sxs-lookup"><span data-stu-id="932f9-108">The application requests the socket type to be a stream socket for the TCP protocol.</span></span>
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  <span data-ttu-id="932f9-109">Вызовите функцию [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , ЗАПРОСИВ IP-адрес для имени сервера, переданного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="932f9-109">Call the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function requesting the IP address for the server name passed on the command line.</span></span> <span data-ttu-id="932f9-110">TCP-порт сервера, к которому будет подключаться клиент, определяется портом по УМОЛЧАНИю \_ (27015) в этом примере.</span><span class="sxs-lookup"><span data-stu-id="932f9-110">The TCP port on the server that the client will connect to is defined by DEFAULT\_PORT as 27015 in this sample.</span></span> <span data-ttu-id="932f9-111">Функция **функцию getaddrinfo** возвращает свое значение в виде целого числа, которое проверяется на наличие ошибок.</span><span class="sxs-lookup"><span data-stu-id="932f9-111">The **getaddrinfo** function returns its value as an integer that is checked for errors.</span></span>
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  <span data-ttu-id="932f9-112">Создайте объект **сокета** с именем коннектсоккет.</span><span class="sxs-lookup"><span data-stu-id="932f9-112">Create a **SOCKET** object called ConnectSocket.</span></span>
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  <span data-ttu-id="932f9-113">Вызовите функцию [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и верните ее значение в переменную коннектсоккет.</span><span class="sxs-lookup"><span data-stu-id="932f9-113">Call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function and return its value to the ConnectSocket variable.</span></span> <span data-ttu-id="932f9-114">Для этого приложения используйте первый IP-адрес, возвращенный вызовом к [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , который соответствует семейству адресов, типу сокета и протоколу, указанным в параметре *указания* .</span><span class="sxs-lookup"><span data-stu-id="932f9-114">For this application, use the first IP address returned by the call to [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) that matched the address family, socket type, and protocol specified in the *hints* parameter.</span></span> <span data-ttu-id="932f9-115">В этом примере сокет потока TCP был указан с типом сокета \_ потока Сокк и протоколом иппрото \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="932f9-115">In this example, a TCP stream socket was specified with a socket type of SOCK\_STREAM and a protocol of IPPROTO\_TCP.</span></span> <span data-ttu-id="932f9-116">Семейство адресов оставлено неопределенным (AF \_ Unspecified), поэтому возвращенный IP-адрес может быть адресом IPv6 или IPv4 для сервера.</span><span class="sxs-lookup"><span data-stu-id="932f9-116">The address family was left unspecified (AF\_UNSPEC), so the returned IP address could be either an IPv6 or IPv4 address for the server.</span></span>

    <span data-ttu-id="932f9-117">Если клиентскому приложению требуется подключение только по протоколам IPv6 или IPv4, для семейства адресов необходимо задать значение AF \_ INET6 для IPv6 или AF \_ INET для IPv4 в параметре *указания* .</span><span class="sxs-lookup"><span data-stu-id="932f9-117">If the client application wants to connect using only IPv6 or IPv4, then the address family needs to be set to AF\_INET6 for IPv6 or AF\_INET for IPv4 in the *hints* parameter.</span></span>

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  <span data-ttu-id="932f9-118">Проверьте наличие ошибок, чтобы убедиться, что сокет является допустимым сокетом.</span><span class="sxs-lookup"><span data-stu-id="932f9-118">Check for errors to ensure that the socket is a valid socket.</span></span>
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

<span data-ttu-id="932f9-119">Параметры, передаваемые функции [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , можно изменить для разных реализаций.</span><span class="sxs-lookup"><span data-stu-id="932f9-119">The parameters passed to the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be changed for different implementations.</span></span>

<span data-ttu-id="932f9-120">Обнаружение ошибок является ключевой частью успешного сетевого кода.</span><span class="sxs-lookup"><span data-stu-id="932f9-120">Error detection is a key part of successful networking code.</span></span> <span data-ttu-id="932f9-121">Если вызов [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) завершается неудачей, он ВОЗВРАЩАЕТ недопустимый \_ сокет.</span><span class="sxs-lookup"><span data-stu-id="932f9-121">If the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) call fails, it returns INVALID\_SOCKET.</span></span> <span data-ttu-id="932f9-122">Оператор **If** в предыдущем коде используется для перехвата всех ошибок, которые могли произойти при создании сокета.</span><span class="sxs-lookup"><span data-stu-id="932f9-122">The **if** statement in the previous code is used to catch any errors that may have occurred while creating the socket.</span></span> <span data-ttu-id="932f9-123">[**Всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает номер ошибки, связанной с последней произошедшей ошибкой.</span><span class="sxs-lookup"><span data-stu-id="932f9-123">[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns an error number associated with the last error that occurred.</span></span>

> [!Note]  
> <span data-ttu-id="932f9-124">В зависимости от приложения может потребоваться более обширная проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="932f9-124">More extensive error checking may be necessary depending on the application.</span></span>
>
> <span data-ttu-id="932f9-125">Например, установка *hints.ai_family* в **AF_UNSPEC** может привести к сбою вызова Connect.</span><span class="sxs-lookup"><span data-stu-id="932f9-125">For example, setting *hints.ai_family* to **AF_UNSPEC** can cause the connect call to fail.</span></span> <span data-ttu-id="932f9-126">Если это происходит, используйте вместо этого определенное значение IPv4 (**AF_INET**) или IPv6 (**AF_INET6**).</span><span class="sxs-lookup"><span data-stu-id="932f9-126">If that happens, then use a specific IPv4 (**AF_INET**) or IPv6 (**AF_INET6**) value instead.</span></span>

<span data-ttu-id="932f9-127">[**Всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) используется для завершения использования \_ библиотеки DLL WS2 32.</span><span class="sxs-lookup"><span data-stu-id="932f9-127">[**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) is used to terminate the use of the WS2\_32 DLL.</span></span>

<span data-ttu-id="932f9-128">Следующий шаг: [Подключение к сокету](connecting-to-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="932f9-128">Next Step: [Connecting to a Socket](connecting-to-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="932f9-129">См. также</span><span class="sxs-lookup"><span data-stu-id="932f9-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="932f9-130">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="932f9-130">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="932f9-131">Инициализация Winsock</span><span class="sxs-lookup"><span data-stu-id="932f9-131">Initializing Winsock</span></span>](initializing-winsock.md)
</dt> <dt>

[<span data-ttu-id="932f9-132">Клиентское приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="932f9-132">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> </dl>

 

 
