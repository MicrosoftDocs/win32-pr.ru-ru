---
description: Чтобы клиент мог обмениваться данными по сети, он должен подключиться к серверу.
ms.assetid: fb52d2b7-70fa-497a-bbb4-42b25ea9d136
title: Подключение к сокету
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a5a81c18089bdf5f35e96aa55a8ede87dc88598a98acd3bc5ab8338afb1208
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132677"
---
# <a name="connecting-to-a-socket"></a>Подключение к сокету

Чтобы клиент мог обмениваться данными по сети, он должен подключиться к серверу.

## <a name="to-connect-to-a-socket"></a>Подключение к сокету

Вызовите функцию [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , передав созданный сокет и структуру [**SOCKADDR**](sockaddr-2.md) в качестве параметров. Проверьте на наличие общих ошибок.


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



Функция [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) используется для определения значений в структуре [**SOCKADDR**](sockaddr-2.md) . В этом примере первый IP-адрес, возвращенный функцией **функцию getaddrinfo** , используется для указания структуры **SOCKADDR** , передаваемой в [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect). Если при вызове **Connect** происходит сбой с первым IP-адресом, попробуйте выполнить следующую структуру [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) в связанном списке, возвращенном из функции **функцию getaddrinfo** .

Сведения, указанные в структуре [**SOCKADDR**](sockaddr-2.md) , включают:

-   IP-адрес сервера, к которому клиент будет пытаться подключиться.
-   номер порта на сервере, к которому будет подключаться клиент. Этот порт был указан как порт 27015, когда клиент вызвал функцию [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

Следующий шаг: [Отправка и получение данных на клиенте](sending-and-receiving-data-on-the-client.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Клиентское приложение Winsock](winsock-client-application.md)
</dt> <dt>

[Создание сокета для клиента](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 
