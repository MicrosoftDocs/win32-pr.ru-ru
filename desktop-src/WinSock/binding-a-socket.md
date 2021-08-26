---
description: Чтобы сервер мог принимать подключения клиентов, он должен быть привязан к сетевому адресу в системе.
ms.assetid: d08fb1a5-af17-4116-8757-ba0a513fb323
title: Привязка сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9e745395209228584ea5535864cca57e30494b2e30bfff02fe2abc527ed5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996923"
---
# <a name="binding-a-socket"></a>Привязка сокета

Чтобы сервер мог принимать подключения клиентов, он должен быть привязан к сетевому адресу в системе. В следующем коде показано, как привязать сокет, который уже был создан к IP-адресу и порту. Клиентские приложения используют IP-адрес и порт для подключения к сети узла.

## <a name="to-bind-a-socket"></a>Привязка сокета

Структура [**SOCKADDR**](sockaddr-2.md) содержит сведения о семействе адресов, IP-адресе и номере порта.

Вызовите функцию [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) , передав созданную структуру **сокета** и [**SOCKADDR**](sockaddr-2.md) , возвращенную из функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) в качестве параметров. Проверьте на наличие общих ошибок.


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



После вызова функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) сведения об адресе, возвращенные функцией [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , больше не нужны. Функция [**фриаддринфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) вызывается для высвобождения памяти, выделенной функцией **функцию getaddrinfo** для этих сведений об адресах.


```C++
    freeaddrinfo(result);

```



Следующий шаг: [прослушивание на сокете](listening-on-a-socket.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Серверное приложение Winsock](winsock-server-application.md)
</dt> <dt>

[Создание сокета для сервера](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



