---
description: новые функции появились в интерфейсе сокетов Windows, специально разработанном для упрощения программирования Windowsных сокетов. одно из преимуществ этих новых функций Windows сокетов — интегрированная поддержка IPv6 и IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Вызовы функций для IPv6-приложений Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241db1f7e07264fe4f0c776834d17c48cff4780b06e6a42816d36a50fa22cef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051672"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>Вызовы функций для IPv6-приложений Winsock

новые функции появились в интерфейсе сокетов Windows, специально разработанном для упрощения программирования Windowsных сокетов. одно из преимуществ этих новых функций Windows сокетов — интегрированная поддержка IPv6 и IPv4.

эти новые функции Windows сокетов включают следующее:

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   семейство функций [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**функцию getaddrinfo**, [**жетаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**жетаддринфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**фриаддринфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**фриаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**фриаддринфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)и [**сетаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   семейство функций [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**жетнамеинфо** и [**жетнамеинфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

кроме того, добавлены новые вспомогательные функции IP с поддержкой IPv6 и IPv4 для упрощения программирования Windowsных сокетов. К этим новым вспомогательным функциям IP относятся следующие.

-   [**жетадаптерсаддрессес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

При добавлении поддержки IPv6 в приложение следует использовать следующие рекомендации:

-   Используйте [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) , чтобы установить подключение к конечной точке по заданному имени узла и порту. функция **WSAConnectByName** доступна в Windows Vista и более поздних версиях.
-   Используйте [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) , чтобы установить соединение с одной из коллекций возможных конечных точек, представленных набором адресов назначения (имен узлов и портов). функция **всаконнектбилист** доступна в Windows Vista и более поздних версиях.
-   замените вызовы функции [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) вызовами одной из новых функций сокетов [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows. функция **функцию getaddrinfo** с поддержкой протокола IPv6 доступна в Windows XP и более поздних версиях. протокол ipv6 также поддерживается в Windows 2000 при установке предварительной версии технологии ipv6 для Windows 2000.
-   замените вызовы функции [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) вызовами одной из новых функций сокетов [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows. функция **жетнамеинфо** с поддержкой протокола IPv6 доступна в Windows XP и более поздних версиях. протокол ipv6 также поддерживается в Windows 2000 при установке предварительной версии технологии ipv6 для Windows 2000.

## <a name="wsaconnectbyname"></a>WSAConnectByName

Функция [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) упрощает подключение к конечной точке с помощью сокета на основе потока с заданным именем узла или IP-адресом назначения (IPv4 или IPv6). Эта функция сокращает исходный код, необходимый для создания приложения IP, которое не зависит от используемой версии протокола IP. **WSAConnectByName** заменяет следующие шаги в типичном приложении TCP на вызов одной функции:

-   Разрешение имени узла в набор IP-адресов.
-   Для каждого IP-адреса:
    -   Создайте сокет соответствующего семейства адресов.
    -   Пытается подключиться к удаленному IP-адресу. Если соединение прошло успешно, возвращается значение; в противном случае будет предпринята попытка следующего удаленного IP-адреса узла.

Функция [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) выходит за пределы простого разрешения имени, а затем пытается подключиться. Функция использует все удаленные адреса, возвращенные разрешением имен, и все исходные IP-адреса локального компьютера. Сначала он пытается подключиться с использованием пар адресов с наибольшей вероятностью успеха. Таким образом, **WSAConnectByName** не только гарантирует, что соединение будет установлено по возможности, но также снизит время, необходимое для установления соединения.

Чтобы включить обмен данными по протоколам IPv6 и IPv4, используйте следующий метод:

-   Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должна вызываться на сокете, созданном для \_ семейства адресов AF INET6, чтобы отключить параметр сокета **IPv6 \_ V6ONLY** перед вызовом [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea). Это достигается путем вызова функции **сетсоккопт** на сокете с параметром *Level* , для которого задано значение **иппрото \_ IPv6** (см. раздел [ \_ параметры сокета IPv6 иппрото](ipproto-ipv6-socket-options.md)), параметр *optname* установлен в **IPv6 \_ V6ONLY**, а параметр *оптвалуе* установлен в значение 0.

Если приложению требуется выполнить привязку к определенному локальному адресу или порту, [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) использовать нельзя, так как параметр сокета **WSAConnectByName** должен быть несвязанным сокетом.

В приведенном ниже примере кода для использования этой функции требуется всего несколько строк кода, чтобы реализовать приложение, которое не зависит от версии IP.

Установка соединения с помощью [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a>всаконнектбилист

Функция [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) устанавливает соединение с узлом, используя набор возможных узлов (представленный НАБОРОМ IP-адресов и портов назначения). Функция принимает все IP-адреса и порты для конечной точки и всех IP-адресов локального компьютера и пытается подключиться с использованием всех возможных сочетаний адресов.

[**Всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) связан с функцией [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) . Вместо того, чтобы брать одно имя узла, **всаконнектбилист** принимает список узлов (адреса назначения и пары портов) и подключается к одному из адресов и портов из предоставленного списка. Эта функция предназначена для поддержки сценариев, в которых приложение должно подключаться к любому доступному узлу из списка потенциальных узлов.

Как и в случае с [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), функция [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) значительно сокращает исходный код, необходимый для создания, привязки и подключения сокета. Эта функция значительно упрощает реализацию приложения, которое не зависит от версии IP. Список адресов для узла, принимаемого этой функцией, может быть адресами IPv6 или IPv4.

Чтобы разрешить передачу адресов IPv6 и IPv4 в одном списке адресов, принятом функцией, необходимо выполнить следующие действия перед вызовом функции:

-   Функция [**сетсоккопт**](/windows/desktop/api/winsock/nf-winsock-setsockopt) должна вызываться на сокете, созданном для \_ семейства адресов AF INET6, чтобы отключить параметр сокета **IPv6 \_ V6ONLY** перед вызовом [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist). Это достигается путем вызова функции **сетсоккопт** на сокете с параметром *Level* , для которого задано значение **иппрото \_ IPv6** (см. раздел [ \_ параметры сокета IPv6 иппрото](ipproto-ipv6-socket-options.md)), параметр *optname* установлен в **IPv6 \_ V6ONLY**, а параметр *оптвалуе* установлен в значение 0.
-   Все адреса IPv4 должны быть представлены в формате IPv6-адресов, сопоставленном с IPv4, что позволяет приложению только для IPv6 взаимодействовать с узлом IPv4. Формат IPv6-адресов, сопоставленный с IPv4, позволяет представить адрес IPv4 узла IPv4 в качестве адреса IPv6. Адрес IPv4 кодируется в младшие биты 32 IPv6-адреса, а старшие биты 96 содержат фиксированный префикс 0:0: 0:0: 0: FFFF. Формат IPv6-адреса, сопоставленный с IPv4, указан в RFC 4291. Дополнительные сведения см. в разделе [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). Макрос IN6ADDR \_ SETV4MAPPED в *мсткпип. h* можно использовать для преобразования адреса IPv4 в требуемый формат IPv6-адресов, сопоставленный с IPv4.

Установка соединения с помощью [ **всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a>функцию getaddrinfo

Функция **функцию getaddrinfo** также выполняет обработку многих функций. ранее для создания, открытия, а затем привязки адреса к сокету были вызваны вызовы к ряду функций Windows сокетов. С помощью функции **функцию getaddrinfo** строки исходного кода, необходимые для выполнения такой работы, могут значительно снизиться. В следующих двух примерах показан исходный код, необходимый для выполнения этих задач с функцией **функцию getaddrinfo** и без нее.

выполнение открытия, Подключение и привязки с помощью **функцию getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



выполнить открытие, Подключение и привязку без использования **функцию getaddrinfo**


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



Обратите внимание, что оба этих примера исходного кода выполняют те же задачи, но в первом примере с использованием функции **функцию getaddrinfo** меньше строк исходного кода и могут работать с адресами IPv6 или IPv4. Количество строк исходного кода, исключенных с помощью функции **функцию getaddrinfo** , может быть различным.

> [!Note]  
> В рабочем исходном коде приложение будет выполнять итерацию по набору адресов, возвращенных функцией [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) или [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . Эти примеры пропускают этот шаг в пользу простоты.

 

Другая ошибка, которую необходимо решить при изменении существующего приложения IPv4 для поддержки IPv6, связано с порядком, в котором вызываются функции. Для [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) требуется, чтобы последовательность вызовов функций была выполнена в определенном порядке.

На платформах, где используются IPv4 и IPv6, семейство адресов удаленного узла не известно заранее. Чтобы определить IP-адрес и семейство адресов удаленного узла, необходимо сначала выполнить разрешение адресов с помощью функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . Затем можно вызвать функцию [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) , чтобы открыть сокет семейства адресов, возвращенный [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo). это важное изменение в том, как записываются Windowsные приложения сокетов, так как многие приложения IPv4 обычно используют разный порядок вызовов функций.

Большинство приложений IPv4 сначала создают сокет для \_ семейства адресов AF INET, затем выполняют разрешение имен, а затем используют сокет для подключения к разрешенному IP-адресу. При создании таких приложений с поддержкой IPv6 вызов функции [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) должен быть отложен до разрешения имени после того, как семейство адресов детереминед. Обратите внимание, что если разрешение имен Возвращает адреса IPv4 и IPv6, для подключения к этим адресам назначения необходимо использовать отдельные сокеты IPv4 и IPv6. все эти сложности можно избежать с помощью функции [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) в Windows Vista и более поздних версий, поэтому разработчикам приложений рекомендуется использовать эту новую функцию.

В следующем примере кода показана правильная последовательность для выполнения разрешения имен (выполняется в четвертой строке в следующем примере исходного кода), а затем открывается сокет (выполняется в 19-<sup>й</sup> строке в следующем примере кода). Этот пример является выдержкой из файла Client. c, который находится в [коде клиента с поддержкой IPv6](ipv6-enabled-client-code-2.md) в приложении б. Функция Принтеррор, вызываемая в следующем примере кода, указана в примере Client. c.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a>Функции IP Helper

Наконец, приложения, использующие вспомогательную функцию IP [**жетадаптерсинфо**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)и связанную со связанной структурой [**\_ \_ сведения о IP-адаптере**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), должны распознать, что эта функция и структура ограничены адресами IPv4. Замены с поддержкой IPv6 для этой функции и структуры являются функцией [**жетадаптерсаддрессес**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) и структурой [**IP- \_ адаптеров \_**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) . приложения с поддержкой ipv6, использующие API вспомогательной функции IP, должны использовать функцию **жетадаптерсаддрессес** и соответствующую структуру **ip- \_ \_ адресов адаптера** с поддержкой ipv6, определенную в пакете sdk для Microsoft Windows Software Development Kit.

## <a name="recommendations"></a>Рекомендации

Лучший подход к обеспечению того, чтобы приложение использовало вызовы функций, совместимых с IPv6, — использовать функцию [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) для получения преобразования "узел-адрес". начиная с Windows XP функция **функцию getaddrinfo** делает функцию [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) ненужной, поэтому приложение должно использовать функцию **функцию getaddrinfo** вместо этого для будущих проектов программирования. Хотя корпорация Майкрософт продолжит поддерживать **gethostbyname**, эта функция не будет расширена для поддержки IPv6. Для прозрачной поддержки получения сведений об узле IPv6 и IPv4 необходимо использовать **функцию getaddrinfo**.

В следующем примере показано, как лучше использовать функцию **функцию getaddrinfo** . Обратите внимание, что функция, которая правильно используется в этом примере, обрабатывает преобразование адреса IPv6 и IPv4 в правильном формате, но также получает другие полезные сведения об узле, например поддерживаемые типы сокетов. Этот пример является выдержкой из примера Client. c, который находится в приложении б.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> версия функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) , поддерживающей IPv6, является новой для выпуска Windows XP Windows.

 

Код, чтобы избежать

Преобразование адресов узлов традиционно было достигнуто с помощью функции [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) . начиная с Windows XP:

-   Функция **функцию getaddrinfo** делает функцию **gethostbyname** устаревшей.
-   Приложения должны использовать функцию **функцию getaddrinfo** вместо функции **gethostbyname** .

Задачи кодирования

**Изменение существующего приложения IPv4 для добавления поддержки IPv6**

1.  Получите служебную программу Checkv4.exe. эта служебная программа устанавливается как часть Windows SDK. Windows SDK доступен по подписке MSDN. ее также можно загрузить с веб-сайта майкрософт ( https://msdn.microsoft.com) . более старая версия средства *Checkv4.exe* была также включена в состав предварительной версии Microsoft IPv6 Technology Preview для Windows 2000.
2.  Запустите служебную программу *Checkv4.exe* для своего кода. Сведения о запуске программы версии для файлов см. в разделе [Использование служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md) .
3.  Программа предупреждает о том, как использовать [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)и другие функции, предназначенные только для IPv4, и предоставляет рекомендации по их замене функциями, совместимыми с IPv6, такими как [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).
4.  Замените все экземпляры функции **gethostbyname** и соответствующий код соответствующим образом с помощью функции **функцию getaddrinfo** . в Windows Vista при необходимости используйте функцию [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) или [**всаконнектбилист**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) .
5.  Замените все экземпляры функции [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) и соответствующий код соответствующим образом с помощью функции [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

Кроме того, можно выполнить поиск экземпляров функций **gethostbyname** и [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) в базе кода, а также изменить все такое использование (и другой связанный код соответственно) на функции **функцию getaddrinfo** и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[рекомендации по IPv6 для приложений Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Изменение структур данных для IPv6 Winsock Аппикатионс](changing-data-structures-2.md)
</dt> <dt>

[Сокеты с двумя стеками для IPv6-приложений Winsock](dual-stack-sockets.md)
</dt> <dt>

[Использование жестко закодированных IPv4-адресов](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock](user-interface-issues-2.md)
</dt> <dt>

[Базовые протоколы для IPv6-приложений Winsock](underlying-protocols-2.md)
</dt> </dl>

 

 
