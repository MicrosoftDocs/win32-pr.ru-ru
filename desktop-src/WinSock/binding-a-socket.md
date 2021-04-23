---
description: Чтобы сервер мог принимать подключения клиентов, он должен быть привязан к сетевому адресу в системе.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Привязка сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc71ad25837a070074fefa2e3693c5546839ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711045"
---
# <a name="binding-a-socket"></a><span data-ttu-id="e40b8-103">Привязка сокета</span><span class="sxs-lookup"><span data-stu-id="e40b8-103">Binding a Socket</span></span>

<span data-ttu-id="e40b8-104">Чтобы сервер мог принимать подключения клиентов, он должен быть привязан к сетевому адресу в системе.</span><span class="sxs-lookup"><span data-stu-id="e40b8-104">For a server to accept client connections, it must be bound to a network address within the system.</span></span> <span data-ttu-id="e40b8-105">В следующем коде показано, как привязать сокет, который уже был создан к IP-адресу и порту.</span><span class="sxs-lookup"><span data-stu-id="e40b8-105">The following code demonstrates how to bind a socket that has already been created to an IP address and port.</span></span> <span data-ttu-id="e40b8-106">Клиентские приложения используют IP-адрес и порт для подключения к сети узла.</span><span class="sxs-lookup"><span data-stu-id="e40b8-106">Client applications use the IP address and port to connect to the host network.</span></span>

## <a name="to-bind-a-socket"></a><span data-ttu-id="e40b8-107">Привязка сокета</span><span class="sxs-lookup"><span data-stu-id="e40b8-107">To bind a socket</span></span>

<span data-ttu-id="e40b8-108">Структура [**SOCKADDR**](sockaddr-2.md) содержит сведения о семействе адресов, IP-адресе и номере порта.</span><span class="sxs-lookup"><span data-stu-id="e40b8-108">The [**sockaddr**](sockaddr-2.md) structure holds information regarding the address family, IP address, and port number.</span></span>

<span data-ttu-id="e40b8-109">Вызовите функцию [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , передав созданную структуру **сокета** и [**SOCKADDR**](sockaddr-2.md) , возвращенную из функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="e40b8-109">Call the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function, passing the created **socket** and [**sockaddr**](sockaddr-2.md) structure returned from the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function as parameters.</span></span> <span data-ttu-id="e40b8-110">Проверьте на наличие общих ошибок.</span><span class="sxs-lookup"><span data-stu-id="e40b8-110">Check for general errors.</span></span>


```C++
    // Setup the TCP listening socket
    iResult = bind( ListenSocket, result->ai_addr, (int)result->ai_addrlen);
    if (iResult == SOCKET_ERROR) {
        printf("bind failed with error: %d\n", WSAGetLastError());
        freeaddrinfo(result);
        closesocket(ListenSocket);
        WSACleanup();
        return 1;
    }
```



<span data-ttu-id="e40b8-111">После вызова функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) сведения об адресе, возвращенные функцией [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="e40b8-111">Once the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called, the address information returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is no longer needed.</span></span> <span data-ttu-id="e40b8-112">Функция [**фриаддринфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) вызывается для высвобождения памяти, выделенной функцией **функцию getaddrinfo** для этих сведений об адресах.</span><span class="sxs-lookup"><span data-stu-id="e40b8-112">The [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) function is called to free the memory allocated by the **getaddrinfo** function for this address information.</span></span>


```C++
    freeaddrinfo(result);

```



<span data-ttu-id="e40b8-113">Следующий шаг: [прослушивание на сокете](listening-on-a-socket.md)</span><span class="sxs-lookup"><span data-stu-id="e40b8-113">Next Step: [Listening on a Socket](listening-on-a-socket.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e40b8-114">См. также</span><span class="sxs-lookup"><span data-stu-id="e40b8-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e40b8-115">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="e40b8-115">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="e40b8-116">Серверное приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="e40b8-116">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="e40b8-117">Создание сокета для сервера</span><span class="sxs-lookup"><span data-stu-id="e40b8-117">Creating a Socket for the Server</span></span>](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



