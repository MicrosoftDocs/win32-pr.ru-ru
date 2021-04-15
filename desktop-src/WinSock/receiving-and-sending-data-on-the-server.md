---
description: В следующем коде показаны функции recv и Send, используемые сервером.
ms.assetid: 26990b06-196a-4fb1-92d8-c5fa096d2b09
title: Получение и отправка данных на сервере
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ab20f074db750bef6459c6b9fcb5fd5636a522
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702102"
---
# <a name="receiving-and-sending-data-on-the-server"></a><span data-ttu-id="fd914-103">Получение и отправка данных на сервере</span><span class="sxs-lookup"><span data-stu-id="fd914-103">Receiving and Sending Data on the Server</span></span>

<span data-ttu-id="fd914-104">В следующем коде показаны функции [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) и [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) , используемые сервером.</span><span class="sxs-lookup"><span data-stu-id="fd914-104">The following code demonstrates the [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) and [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) functions used by the server.</span></span>

### <a name="to-receive-and-send-data-on-a-socket"></a><span data-ttu-id="fd914-105">Получение и отправка данных на сокете</span><span class="sxs-lookup"><span data-stu-id="fd914-105">To receive and send data on a socket</span></span>


```C++
#define DEFAULT_BUFLEN 512

char recvbuf[DEFAULT_BUFLEN];
int iResult, iSendResult;
int recvbuflen = DEFAULT_BUFLEN;

// Receive until the peer shuts down the connection
do {

    iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);

        // Echo the buffer back to the sender
        iSendResult = send(ClientSocket, recvbuf, iResult, 0);
        if (iSendResult == SOCKET_ERROR) {
            printf("send failed: %d\n", WSAGetLastError());
            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }
        printf("Bytes sent: %d\n", iSendResult);
    } else if (iResult == 0)
        printf("Connection closing...\n");
    else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ClientSocket);
        WSACleanup();
        return 1;
    }

} while (iResult > 0);
```



<span data-ttu-id="fd914-106">Функции [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) и [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) возвращают целочисленное значение числа отправленных или полученных байтов соответственно, или ошибка.</span><span class="sxs-lookup"><span data-stu-id="fd914-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="fd914-107">Каждая функция также принимает одни и те же параметры: активный сокет, буфер **char** , число байтов для отправки или получения и любые используемые флаги.</span><span class="sxs-lookup"><span data-stu-id="fd914-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="fd914-108">Следующий шаг: [Отключение сервера](disconnecting-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="fd914-108">Next Step: [Disconnecting the Server](disconnecting-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd914-109">См. также</span><span class="sxs-lookup"><span data-stu-id="fd914-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd914-110">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="fd914-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="fd914-111">Серверное приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="fd914-111">Winsock Server Application</span></span>](winsock-server-application.md)
</dt> <dt>

[<span data-ttu-id="fd914-112">Принятие подключения</span><span class="sxs-lookup"><span data-stu-id="fd914-112">Accepting a Connection</span></span>](accepting-a-connection.md)
</dt> </dl>

 

 



