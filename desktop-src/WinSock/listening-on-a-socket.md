---
description: После привязки сокета к IP-адресу и порту в системе сервер должен прослушивать IP-адрес и порт для входящих запросов на подключение.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Прослушивание на сокете
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692280"
---
# <a name="listening-on-a-socket"></a><span data-ttu-id="e2bb3-103">Прослушивание на сокете</span><span class="sxs-lookup"><span data-stu-id="e2bb3-103">Listening on a Socket</span></span>

<span data-ttu-id="e2bb3-104">После привязки сокета к IP-адресу и порту в системе сервер должен прослушивать IP-адрес и порт для входящих запросов на подключение.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-104">After the socket is bound to an IP address and port on the system, the server must then listen on that IP address and port for incoming connection requests.</span></span>

## <a name="to-listen-on-a-socket"></a><span data-ttu-id="e2bb3-105">Прослушивание сокета</span><span class="sxs-lookup"><span data-stu-id="e2bb3-105">To listen on a socket</span></span>

<span data-ttu-id="e2bb3-106">Вызовите функцию [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , передав в качестве параметров созданный сокет и значение для *невыполненной работы*, максимальную длину очереди ожидающих подключений для приема.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-106">Call the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, passing as parameters the created socket and a value for the *backlog*, maximum length of the queue of pending connections to accept.</span></span> <span data-ttu-id="e2bb3-107">В этом примере параметру *невыполненной работы* было присвоено значение **сомаксконн**.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-107">In this example, the *backlog* parameter was set to **SOMAXCONN**.</span></span> <span data-ttu-id="e2bb3-108">Это значение представляет собой специальную константу, которая указывает поставщику Winsock для этого сокета максимально допустимое число ожидающих подключений в очереди.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-108">This value is a special constant that instructs the Winsock provider for this socket to allow a maximum reasonable number of pending connections in the queue.</span></span> <span data-ttu-id="e2bb3-109">Проверьте возвращаемое значение для общих ошибок.</span><span class="sxs-lookup"><span data-stu-id="e2bb3-109">Check the return value for general errors.</span></span>


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



<span data-ttu-id="e2bb3-110">Следующий шаг: [принятие подключения](accepting-a-connection.md)</span><span class="sxs-lookup"><span data-stu-id="e2bb3-110">Next Step: [Accepting a Connection](accepting-a-connection.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2bb3-111">См. также</span><span class="sxs-lookup"><span data-stu-id="e2bb3-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2bb3-112">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="e2bb3-112">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="e2bb3-113">Серверное приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="e2bb3-113">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="e2bb3-114">Привязка сокета</span><span class="sxs-lookup"><span data-stu-id="e2bb3-114">Binding a Socket</span></span>](binding-a-socket.md)
</dt> </dl>

 

 



