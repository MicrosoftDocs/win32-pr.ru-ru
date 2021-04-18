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

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Серверное приложение Winsock](winsock-server-application.md)
</dt> <dt>

[Создание сокета для сервера](creating-a-socket-for-the-server.md)
</dt> </dl>

 

 



