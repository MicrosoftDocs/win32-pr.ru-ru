---
description: После того как клиент завершит отправку и получение данных, клиент отключится от сервера и завершит работу сокета.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Отсоединение клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343532"
---
# <a name="disconnecting-the-client"></a><span data-ttu-id="daf8f-103">Отсоединение клиента</span><span class="sxs-lookup"><span data-stu-id="daf8f-103">Disconnecting the Client</span></span>

<span data-ttu-id="daf8f-104">После того как клиент завершит отправку и получение данных, клиент отключится от сервера и завершит работу сокета.</span><span class="sxs-lookup"><span data-stu-id="daf8f-104">Once the client is completed sending and receiving data, the client disconnects from the server and shutdowns the socket.</span></span>

<span data-ttu-id="daf8f-105">**Отключение и завершение работы сокета**</span><span class="sxs-lookup"><span data-stu-id="daf8f-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="daf8f-106">Когда клиент завершает отправку данных на сервер, функция [**завершения работы**](/windows/desktop/api/winsock/nf-winsock-shutdown) может быть вызвана указанием SD \_ Send для завершения отправной стороны сокета.</span><span class="sxs-lookup"><span data-stu-id="daf8f-106">When the client is done sending data to the server, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="daf8f-107">Это позволяет серверу освобождать некоторые ресурсы для этого сокета.</span><span class="sxs-lookup"><span data-stu-id="daf8f-107">This allows the server to release some of the resources for this socket.</span></span> <span data-ttu-id="daf8f-108">Клиентское приложение по-прежнему может принимать данные на сокете.</span><span class="sxs-lookup"><span data-stu-id="daf8f-108">The client application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="daf8f-109">Когда клиентское приложение выполняет получение данных, вызывается функция [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) для закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="daf8f-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="daf8f-110">После завершения работы клиентского приложения с помощью DLL-библиотеки Windows Sockets функция [**всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) вызывается для освобождения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="daf8f-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a><span data-ttu-id="daf8f-111">Полный исходный код клиента</span><span class="sxs-lookup"><span data-stu-id="daf8f-111">Complete Client Source Code</span></span>

-   [<span data-ttu-id="daf8f-112">Завершение клиентского кода</span><span class="sxs-lookup"><span data-stu-id="daf8f-112">Complete Client Code</span></span>](complete-client-code.md)

## <a name="related-topics"></a><span data-ttu-id="daf8f-113">См. также</span><span class="sxs-lookup"><span data-stu-id="daf8f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf8f-114">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="daf8f-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="daf8f-115">Клиентское приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="daf8f-115">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="daf8f-116">Отправка и получение данных на клиенте</span><span class="sxs-lookup"><span data-stu-id="daf8f-116">Sending and Receiving Data on the Client</span></span>](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



