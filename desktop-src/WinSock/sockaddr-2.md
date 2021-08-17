---
description: Структура SOCKADDR зависит от выбранного протокола.
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: SOCKADDR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: afdacd0b4579bcb73bfaaa2da0b3714c7d597d94c0d25020e7353e3afd168d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117927325"
---
# <a name="sockaddr"></a>SOCKADDR

Структура SOCKADDR зависит от выбранного протокола. За исключением *параметра \* \_ семейства Sin* , содержимое SOCKADDR выражается в порядке сетевого байта.

Функции Winsock, использующие SOCKADDR, не строго обрабатываются как указатели на структуру SOCKADDR. Структура интерпретируется по-разному в контексте различных семейств адресов. Единственное требование заключается в том, что первый **u- \_ короткий** — это семейство адресов, а общий размер буфера памяти в байтах — *namelen*.

Структура [**\_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) также хранит сведения об адресе сокета, и структура достаточно велика для хранения сведений об адресах IPv4 или IPv6. Использование структуры **\_ хранилища SOCKADDR** способствует использованию семейства протоколов и независящей от версии протокола и упрощает разработку. Рекомендуется использовать структуру **\_ хранения SOCKADDR** вместо структуры SOCKADDR. структура **\_ хранилища SOCKADDR** поддерживается на Windows Server 2003 и более поздних версий.

Структура SOCKADDR и SOCKADDR \_ в представленных ниже структурах используются с IPv4. Другие протоколы используют аналогичные структуры.

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

\_Приведенные ниже SOCKADDR in6 и SOCKADDR \_ in6 \_ используются с IPv6.

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

в пакете Microsoft Windows Software Development Kit (SDK), выпущенном для Windows Vista и более поздних версий, **SOCKADDR** и **SOCKADDR \_ в** тегах typedef определяются для SOCKADDR и SOCKADDR \_ в структурах следующим образом:

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

в Windows SDK, выпущенном для Windows Vista и более поздних версий, организация файлов заголовков изменилась, а sockaddr и sockaddr \_ в структурах определяются в файле заголовка файла *Ws2def. h* , а не в файле заголовка *Winsock2. h* . Файл заголовка *Ws2def. h* автоматически включается в заголовочный файл *Winsock2. h* . \_Структура in6 SOCKADDR определена в файле заголовка *Ws2ipdef. h* , а не в файле заголовка *Ws2tcpip. h* . Файл заголовка *Ws2ipdef. h* автоматически включается в заголовочный файл *Ws2tcpip. h* . Файлы заголовков *Ws2def. h* и *Ws2ipdef. h* никогда не следует использовать напрямую.

## <a name="example-code"></a>Пример кода

В следующем примере демонстрируется использование структуры **SOCKADDR** .


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a>См. также

[**\_хранилище SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
