---
description: После инициализации необходимо создать экземпляр объекта СОКЕТа для использования клиентом.
ms.assetid: 088a79ef-b430-4860-8edc-902a1a03ed0d
title: Создание сокета для клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64467406f13ed40bdbe134e7796dd2aa5ff7bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897345"
---
# <a name="creating-a-socket-for-the-client"></a>Создание сокета для клиента

После инициализации необходимо создать экземпляр объекта **сокета** для использования клиентом.

**Создание сокета**

1.  Объявите объект [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) , содержащий структуру [**SOCKADDR**](sockaddr-2.md) , и инициализируйте эти значения. Для этого приложения семейство Интернет-адресов не указано, чтобы можно было вернуть адрес IPv6 или IPv4. Приложение запрашивает тип сокета в качестве сокета потока для протокола TCP.
    ```C++
    struct addrinfo *result = NULL,
                    *ptr = NULL,
                    hints;

    ZeroMemory( &hints, sizeof(hints) );
    hints.ai_family = AF_UNSPEC;
    hints.ai_socktype = SOCK_STREAM;
    hints.ai_protocol = IPPROTO_TCP;
    ```

    

2.  Вызовите функцию [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , ЗАПРОСИВ IP-адрес для имени сервера, переданного в командной строке. TCP-порт сервера, к которому будет подключаться клиент, определяется портом по УМОЛЧАНИю \_ (27015) в этом примере. Функция **функцию getaddrinfo** возвращает свое значение в виде целого числа, которое проверяется на наличие ошибок.
    ```C++
    #define DEFAULT_PORT "27015"

    // Resolve the server address and port
    iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
    if (iResult != 0) {
        printf("getaddrinfo failed: %d\n", iResult);
        WSACleanup();
        return 1;
    }
    ```

    

3.  Создайте объект **сокета** с именем коннектсоккет.
    ```C++
    SOCKET ConnectSocket = INVALID_SOCKET;
    ```

    

4.  Вызовите функцию [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) и верните ее значение в переменную коннектсоккет. Для этого приложения используйте первый IP-адрес, возвращенный вызовом к [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , который соответствует семейству адресов, типу сокета и протоколу, указанным в параметре *указания* . В этом примере сокет потока TCP был указан с типом сокета \_ потока Сокк и протоколом иппрото \_ TCP. Семейство адресов оставлено неопределенным (AF \_ Unspecified), поэтому возвращенный IP-адрес может быть адресом IPv6 или IPv4 для сервера.

    Если клиентскому приложению требуется подключение только по протоколам IPv6 или IPv4, для семейства адресов необходимо задать значение AF \_ INET6 для IPv6 или AF \_ INET для IPv4 в параметре *указания* .

    ```C++
    // Attempt to connect to the first address returned by
    // the call to getaddrinfo
    ptr=result;

    // Create a SOCKET for connecting to server
    ConnectSocket = socket(ptr->ai_family, ptr->ai_socktype, 
        ptr->ai_protocol);
    ```

    

5.  Проверьте наличие ошибок, чтобы убедиться, что сокет является допустимым сокетом.
    ```C++
    if (ConnectSocket == INVALID_SOCKET) {
        printf("Error at socket(): %ld\n", WSAGetLastError());
        freeaddrinfo(result);
        WSACleanup();
        return 1;
    }
    ```

    

Параметры, передаваемые функции [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , можно изменить для разных реализаций.

Обнаружение ошибок является ключевой частью успешного сетевого кода. Если вызов [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) завершается неудачей, он ВОЗВРАЩАЕТ недопустимый \_ сокет. Оператор **If** в предыдущем коде используется для перехвата всех ошибок, которые могли произойти при создании сокета. [**Всажетластеррор**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) возвращает номер ошибки, связанной с последней произошедшей ошибкой.

> [!Note]  
> В зависимости от приложения может потребоваться более обширная проверка ошибок.
>
> Например, установка *hints.ai_family* в **AF_UNSPEC** может привести к сбою вызова Connect. Если это происходит, используйте вместо этого определенное значение IPv4 (**AF_INET**) или IPv6 (**AF_INET6**).

[**Всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) используется для завершения использования \_ библиотеки DLL WS2 32.

Следующий шаг: [Подключение к сокету](connecting-to-a-socket.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Инициализация Winsock](initializing-winsock.md)
</dt> <dt>

[Клиентское приложение Winsock](winsock-client-application.md)
</dt> </dl>

 

 
