---
description: В следующем коде показаны функции Send и recv, используемые клиентом после установки соединения.
ms.assetid: 9c6d366d-2bc6-4c92-8d0b-21c51e08ed4f
title: Отправка и получение данных на клиенте
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d91ee507d78bc2638a6d3f7383cd6a930651e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693394"
---
# <a name="sending-and-receiving-data-on-the-client"></a><span data-ttu-id="0f28a-103">Отправка и получение данных на клиенте</span><span class="sxs-lookup"><span data-stu-id="0f28a-103">Sending and Receiving Data on the Client</span></span>

<span data-ttu-id="0f28a-104">В следующем коде показаны функции [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) и [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) , используемые клиентом после установки соединения.</span><span class="sxs-lookup"><span data-stu-id="0f28a-104">The following code demonstrates the [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions used by the client once a connection is established.</span></span>

## <a name="client"></a><span data-ttu-id="0f28a-105">Клиент</span><span class="sxs-lookup"><span data-stu-id="0f28a-105">Client</span></span>


```C++
#define DEFAULT_BUFLEN 512

int recvbuflen = DEFAULT_BUFLEN;

const char *sendbuf = "this is a test";
char recvbuf[DEFAULT_BUFLEN];

int iResult;

// Send an initial buffer
iResult = send(ConnectSocket, sendbuf, (int) strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

printf("Bytes Sent: %ld\n", iResult);

// shutdown the connection for sending since no more data will be sent
// the client can still use the ConnectSocket for receiving data
iResult = shutdown(ConnectSocket, SD_SEND);
if (iResult == SOCKET_ERROR) {
    printf("shutdown failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data until the server closes the connection
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0)
        printf("Bytes received: %d\n", iResult);
    else if (iResult == 0)
        printf("Connection closed\n");
    else
        printf("recv failed: %d\n", WSAGetLastError());
} while (iResult > 0);
```



<span data-ttu-id="0f28a-106">Функции [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) и [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) возвращают целочисленное значение числа отправленных или полученных байтов соответственно, или ошибка.</span><span class="sxs-lookup"><span data-stu-id="0f28a-106">The [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions both return an integer value of the number of bytes sent or received, respectively, or an error.</span></span> <span data-ttu-id="0f28a-107">Каждая функция также принимает одни и те же параметры: активный сокет, буфер **char** , число байтов для отправки или получения и любые используемые флаги.</span><span class="sxs-lookup"><span data-stu-id="0f28a-107">Each function also takes the same parameters: the active socket, a **char** buffer, the number of bytes to send or receive, and any flags to use.</span></span>

<span data-ttu-id="0f28a-108">Следующий шаг: [Отключение клиента](disconnecting-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="0f28a-108">Next Step: [Disconnecting the Client](disconnecting-the-client.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f28a-109">См. также</span><span class="sxs-lookup"><span data-stu-id="0f28a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f28a-110">начало работы с помощью Winsock</span><span class="sxs-lookup"><span data-stu-id="0f28a-110">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="0f28a-111">Клиентское приложение Winsock</span><span class="sxs-lookup"><span data-stu-id="0f28a-111">Winsock Client Application</span></span>](winsock-client-application.md)
</dt> <dt>

[<span data-ttu-id="0f28a-112">Подключение к сокету</span><span class="sxs-lookup"><span data-stu-id="0f28a-112">Connecting to a Socket</span></span>](connecting-to-a-socket.md)
</dt> </dl>

 

 



