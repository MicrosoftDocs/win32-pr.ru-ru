---
description: Чтобы клиент мог обмениваться данными по сети, он должен подключиться к серверу.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Подключение к сокету
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa4461e1b00ba073320529d03e3b0fe32cdae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701551"
---
# <a name="connecting-to-a-socket"></a><span data-ttu-id="6875c-103">Подключение к сокету</span><span class="sxs-lookup"><span data-stu-id="6875c-103">Connecting to a Socket</span></span>

<span data-ttu-id="6875c-104">Чтобы клиент мог обмениваться данными по сети, он должен подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="6875c-104">For a client to communicate on a network, it must connect to a server.</span></span>

## <a name="to-connect-to-a-socket"></a><span data-ttu-id="6875c-105">Подключение к сокету</span><span class="sxs-lookup"><span data-stu-id="6875c-105">To connect to a socket</span></span>

<span data-ttu-id="6875c-106">Вызовите функцию [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , передав созданный сокет и структуру [**SOCKADDR**](sockaddr-2.md) в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="6875c-106">Call the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters.</span></span> <span data-ttu-id="6875c-107">Проверьте на наличие общих ошибок.</span><span class="sxs-lookup"><span data-stu-id="6875c-107">Check for general errors.</span></span>


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="6875c-108">Функция [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) используется для определения значений в структуре [**SOCKADDR**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="6875c-108">The [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure.</span></span> <span data-ttu-id="6875c-109">В этом примере первый IP-адрес, возвращенный функцией **функцию getaddrinfo** , используется для указания структуры **SOCKADDR** , передаваемой в [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span><span class="sxs-lookup"><span data-stu-id="6875c-109">In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect).</span></span> <span data-ttu-id="6875c-110">Если при вызове **Connect** происходит сбой с первым IP-адресом, попробуйте выполнить следующую структуру [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) в связанном списке, возвращенном из функции **функцию getaddrinfo** .</span><span class="sxs-lookup"><span data-stu-id="6875c-110">If the **connect** call fails to the first IP address, then try the next [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) structure in the linked list returned from the **getaddrinfo** function.</span></span>

<span data-ttu-id="6875c-111">Сведения, указанные в структуре [**SOCKADDR**](sockaddr-2.md) , включают:</span><span class="sxs-lookup"><span data-stu-id="6875c-111">The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:</span></span>

-   <span data-ttu-id="6875c-112">IP-адрес сервера, к которому клиент будет пытаться подключиться.</span><span class="sxs-lookup"><span data-stu-id="6875c-112">the IP address of the server that the client will try to connect to.</span></span>
-   <span data-ttu-id="6875c-113">номер порта на сервере, к которому будет подключаться клиент.</span><span class="sxs-lookup"><span data-stu-id="6875c-113">the port number on the server that the client will connect to.</span></span> <span data-ttu-id="6875c-114">Этот порт был указан как порт 27015, когда клиент вызвал функцию [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="6875c-114">This port was specified as port 27015 when the client called the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span>

<span data-ttu-id="6875c-115">Следующий шаг: [Отправка и получение данных на клиенте](sending-and-receiving-data-on-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="6875c-115">Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6875c-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6875c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6875c-117">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="6875c-117">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="6875c-118">Клиентское приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="6875c-118">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="6875c-119">Создание сокета для клиента</span><span class="sxs-lookup"><span data-stu-id="6875c-119">Creating a Socket for the Client</span></span>](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
