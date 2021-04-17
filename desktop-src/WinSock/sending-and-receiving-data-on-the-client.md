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
# <a name="sending-and-receiving-data-on-the-client"></a>Отправка и получение данных на клиенте

В следующем коде показаны функции [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) и [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) , используемые клиентом после установки соединения.

## <a name="client"></a>Клиент


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



Функции [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) и [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) возвращают целочисленное значение числа отправленных или полученных байтов соответственно, или ошибка. Каждая функция также принимает одни и те же параметры: активный сокет, буфер **char** , число байтов для отправки или получения и любые используемые флаги.

Следующий шаг: [Отключение клиента](disconnecting-the-client.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Клиентское приложение Winsock](winsock-client-application.md)
</dt> <dt>

[Подключение к сокету](connecting-to-a-socket.md)
</dt> </dl>

 

 



