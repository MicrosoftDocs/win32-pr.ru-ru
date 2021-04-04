---
description: После того как сервер завершит получение данных от клиента и отправит данные обратно клиенту, сервер отключится от клиента и завершит работу сокета.
ms.assetid: 67f33645-d57a-48bd-9f0c-9e816f528204
title: Отключение сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6abf7754da39a891b3d29c69f6c835706debd36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897341"
---
# <a name="disconnecting-the-server"></a><span data-ttu-id="1fc11-103">Отключение сервера</span><span class="sxs-lookup"><span data-stu-id="1fc11-103">Disconnecting the Server</span></span>

<span data-ttu-id="1fc11-104">После того как сервер завершит получение данных от клиента и отправит данные обратно клиенту, сервер отключится от клиента и завершит работу сокета.</span><span class="sxs-lookup"><span data-stu-id="1fc11-104">Once the server is completed receiving data from the client and sending data back to the client, the server disconnects from the client and shutdowns the socket.</span></span>

<span data-ttu-id="1fc11-105">**Отключение и завершение работы сокета**</span><span class="sxs-lookup"><span data-stu-id="1fc11-105">**To disconnect and shutdown a socket**</span></span>

1.  <span data-ttu-id="1fc11-106">Когда сервер отправляет данные клиенту, функция [**завершения работы**](/windows/desktop/api/winsock/nf-winsock-shutdown) может быть вызвана указанием SD \_ Send для завершения отправной стороны сокета.</span><span class="sxs-lookup"><span data-stu-id="1fc11-106">When the server is done sending data to the client, the [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) function can be called specifying SD\_SEND to shutdown the sending side of the socket.</span></span> <span data-ttu-id="1fc11-107">Это позволяет клиенту освобождать некоторые ресурсы для этого сокета.</span><span class="sxs-lookup"><span data-stu-id="1fc11-107">This allows the client to release some of the resources for this socket.</span></span> <span data-ttu-id="1fc11-108">Серверное приложение по-прежнему может принимать данные через сокет.</span><span class="sxs-lookup"><span data-stu-id="1fc11-108">The server application can still receive data on the socket.</span></span>
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ClientSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  <span data-ttu-id="1fc11-109">Когда клиентское приложение выполняет получение данных, вызывается функция [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) для закрытия сокета.</span><span class="sxs-lookup"><span data-stu-id="1fc11-109">When the client application is done receiving data, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function is called to close the socket.</span></span>

    <span data-ttu-id="1fc11-110">После завершения работы клиентского приложения с помощью DLL-библиотеки Windows Sockets функция [**всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) вызывается для освобождения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fc11-110">When the client application is completed using the Windows Sockets DLL, the [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) function is called to release resources.</span></span>

    ```C++
    // cleanup
    closesocket(ClientSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-server-source-code"></a><span data-ttu-id="1fc11-111">Полный исходный код сервера</span><span class="sxs-lookup"><span data-stu-id="1fc11-111">Complete Server Source Code</span></span>

-   [<span data-ttu-id="1fc11-112">Полный код сервера</span><span class="sxs-lookup"><span data-stu-id="1fc11-112">Complete Server Code</span></span>](complete-server-code.md)

## <a name="related-topics"></a><span data-ttu-id="1fc11-113">См. также</span><span class="sxs-lookup"><span data-stu-id="1fc11-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fc11-114">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="1fc11-114">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="1fc11-115">Серверное приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="1fc11-115">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="1fc11-116">Получение и отправка данных на сервере</span><span class="sxs-lookup"><span data-stu-id="1fc11-116">Receiving and Sending Data on the Server</span></span>](receiving-and-sending-data-on-the-server.md)
</dt> <dt>

[<span data-ttu-id="1fc11-117">Выполнение примера кода клиента и сервера Winsock</span><span class="sxs-lookup"><span data-stu-id="1fc11-117">Running the Winsock Client and Server Code Sample</span></span>](finished-server-and-client-code.md)
</dt> </dl>

 

 



