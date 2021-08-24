---
description: поддержка IPv6, приложение TCP/IP и сокеты Windows.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Поддержка IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f48e5b46ef1fcf1a2257db4a04b5435443552bb49f6c3c2b2dc4784077dcbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794804"
---
# <a name="ipv6-support"></a>Поддержка IPv6

для поддержки ipv4 и IPv6 в Windows XP с пакетом обновления 1 (SP1) и на Windows Server 2003 приложение должно создать два сокета, один сокет для использования с IPv4 и один сокет для использования с IPv6. Эти два сокета должны обрабатываться отдельно приложением.

если поставщик услуг TCP/IP в Windows XP с пакетом обновления 1 (SP1) и Windows Server 2003 поддерживает адресацию IPv4 и IPv6, он должен создать два отдельных сокета и прослушивать их отдельно.

-   Один раз для IPv4.
-   Один раз для семейства IPv6-адресов.

Windows Vista и более поздних версий предлагают возможность создания одного сокета IPv6, который может выполнять обработку трафика IPv6 и IPv4. Например, будет создан сокет прослушивания TCP для IPv6, переведен в режим двойного стека и привязан к порту 5001. Этот сокет с двойным стеком может принимать подключения от TCP-клиентов IPv6, подключающихся к порту 5001, а также от клиентов IPv4 TCP, подключающихся к порту 5001. Эта функция позволяет значительно упростить проектирование приложений и снизить издержки ресурсов, необходимые для размещения операций на двух отдельных сокетах. Однако существуют некоторые ограничения, которые должны быть выполнены для использования сокета с двумя стеками. Дополнительные сведения см. в разделе [сокеты с двойным стеком](dual-stack-sockets.md).

[**Всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) возвращает две структуры [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) для каждого поддерживаемого типа сокета ( \_ поток Сокк, СОКК \_ дграм, СОКК \_ RAW). **Иаддрессфамили** должен иметь значение AF \_ INET для адресации IPv4 и для AF \_ INET6 для адресации IPv6.

IPv6-адреса описаны в следующих структурах.

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

если приложение использует Windows сокеты 1,1 и желает использовать адреса IPv6, то может продолжать использовать все старые функции, которые принимают структуру [**sockaddr**](sockaddr-2.md) в качестве одного из параметров ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)и [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)и т. д.). Единственное изменение, которое требуется, — использовать **SOCKADDR \_ in6** вместо **SOCKADDR \_ в**.

Однако функции разрешения имен ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)и т. д.) и функции преобразования адреса ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ нтоа**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) нельзя использовать повторно, так как они предполагают, что IP-адрес имеет длину 4 байта. приложение, которое хочет выполнить разрешение имен и преобразование адресов для IPv6-адресов, должно использовать функции Windows сокеты 2. были введены многие новые функции, позволяющие приложениям Windows sockets 2 использовать преимущества IPv6, включая функции [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

дополнительные сведения о том, как включить возможности ipv6 в приложении, см. в разделе [руководство по ipv6 для приложений Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
