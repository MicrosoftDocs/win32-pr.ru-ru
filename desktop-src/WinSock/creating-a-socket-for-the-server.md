---
description: После инициализации объект СОКЕТа должен быть создан для использования сервером.
ms.assetid: 2f3a7cab-3296-41ec-ac7e-224655b92a7c
title: Создание сокета для сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd3fb00cb8b1155f4d26d94c9a88328256effe23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145085"
---
# <a name="creating-a-socket-for-the-server"></a>Создание сокета для сервера

После инициализации объект **сокета** должен быть создан для использования сервером.

**Создание сокета для сервера**

1.  Функция [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) используется для определения значений в структуре [**SOCKADDR**](sockaddr-2.md) :

    -   **AF \_ INET** используется для указания семейства IPv4-адресов.
    -   **Сокк \_ ПОТОК** используется для указания сокета потока.
    -   **Иппрото \_ Протокол TCP используется** для указания протокола TCP.
    -   **AI \_ ПАССИВный** флаг указывает, что вызывающий объект планирует использовать возвращенную структуру адреса сокета в вызове функции [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) . Если флаг **AI \_ passive** установлен и параметр *nodeName* для функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) является **пустым** указателем, часть IP-адреса в структуре адресов сокетов **устанавливается в значение a для адресов \_** IPv4 или **IN6ADDR \_ ANY \_ init** для IPv6-адресов.
    -   27015 — номер порта, связанного с сервером, к которому будет подключаться клиент.

    Структура [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) используется функцией [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .

    ```C++
    #define DEFAULT_PORT "27015"

    struct addrinfo *result = NULL, *ptr = NULL, hints;

    ZeroMemory(&hints, sizeof (hints));
    hints.ai_family = AF_INET;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    hints.ai_flags = AI_PASSIVE;

    // Resolve the local address and port to be used by the server
    iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Создайте объект **сокета** с именем листенсоккет, чтобы сервер мог прослушивать подключения клиентов.
    ```C++
    SOCKET ListenSocket = INVALID_SOCKET;
    ```

    

3.  Вызовите функцию [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и верните ее значение в переменную листенсоккет. Для этого серверного приложения используйте первый IP-адрес, возвращенный вызовом [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , который соответствует семейству адресов, типу сокета и протоколу, указанным в параметре *указания* . В этом примере был запрошен сокет потока TCP для IPv4 с семейством адресов IPv4, типом сокета \_ потока Сокк и протоколом иппрото \_ TCP. Поэтому для Листенсоккет запрашивается IPv4-адрес.

    Если серверное приложение ожидает передачи данных по протоколу IPv6, для семейства адресов необходимо задать значение AF \_ INET6 в параметре *указания* . Если сервер желает прослушивать как IPv6, так и IPv4, необходимо создать два сокета прослушивания: один для IPv6 и один для IPv4. Эти два сокета должны обрабатываться отдельно приложением.

    Windows Vista и более поздних версий предлагают возможность создания одного сокета IPv6, который находится в режиме двойного стека, для прослушивания как IPv6, так и IPv4. Дополнительные сведения об этой функции см. в разделе [сокеты с двойным стеком](dual-stack-sockets.md).

    ```C++
    // Create a SOCKET for the server to listen for client connections

    ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
    ```

    

4.  Проверьте наличие ошибок, чтобы убедиться, что сокет является допустимым сокетом.
    ```C++
    if (ListenSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Следующий шаг: [Привязка сокета](binding-a-socket.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Инициализация Winsock](initializing-winsock.md)
</dt> <dt>

[Серверное приложение Winsock](winsock-server-application.md)
</dt> </dl>

 

 
