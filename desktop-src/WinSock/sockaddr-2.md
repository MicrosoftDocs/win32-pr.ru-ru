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
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711769"
---
# <a name="sockaddr"></a><span data-ttu-id="cb21e-103">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="cb21e-103">sockaddr</span></span>

<span data-ttu-id="cb21e-104">Структура SOCKADDR зависит от выбранного протокола.</span><span class="sxs-lookup"><span data-stu-id="cb21e-104">The sockaddr structure varies depending on the protocol selected.</span></span> <span data-ttu-id="cb21e-105">За исключением *параметра \* \_ семейства Sin* , содержимое SOCKADDR выражается в порядке сетевого байта.</span><span class="sxs-lookup"><span data-stu-id="cb21e-105">Except for the *sin\*\_family* parameter, sockaddr contents are expressed in network byte order.</span></span>

<span data-ttu-id="cb21e-106">Функции Winsock, использующие SOCKADDR, не строго обрабатываются как указатели на структуру SOCKADDR.</span><span class="sxs-lookup"><span data-stu-id="cb21e-106">Winsock functions using sockaddr are not strictly interpreted to be pointers to a sockaddr structure.</span></span> <span data-ttu-id="cb21e-107">Структура интерпретируется по-разному в контексте различных семейств адресов.</span><span class="sxs-lookup"><span data-stu-id="cb21e-107">The structure is interpreted differently in the context of different address families.</span></span> <span data-ttu-id="cb21e-108">Единственное требование заключается в том, что первый **u- \_ короткий** — это семейство адресов, а общий размер буфера памяти в байтах — *namelen*.</span><span class="sxs-lookup"><span data-stu-id="cb21e-108">The only requirements are that the first **u\_short** is the address family and the total size of the memory buffer in bytes is *namelen*.</span></span>

<span data-ttu-id="cb21e-109">Структура [**\_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) также хранит сведения об адресе сокета, и структура достаточно велика для хранения сведений об адресах IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="cb21e-109">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure also stores socket address information and the structure is sufficiently large to store IPv4 or IPv6 address information.</span></span> <span data-ttu-id="cb21e-110">Использование структуры **\_ хранилища SOCKADDR** способствует использованию семейства протоколов и независящей от версии протокола и упрощает разработку.</span><span class="sxs-lookup"><span data-stu-id="cb21e-110">The use of the **SOCKADDR\_STORAGE** structure promotes protocol-family and protocol-version independence, and simplifies development.</span></span> <span data-ttu-id="cb21e-111">Рекомендуется использовать структуру **\_ хранения SOCKADDR** вместо структуры SOCKADDR.</span><span class="sxs-lookup"><span data-stu-id="cb21e-111">It is recommended that the **SOCKADDR\_STORAGE** structure be used in place of the sockaddr structure.</span></span> <span data-ttu-id="cb21e-112">Структура **\_ хранилища SOCKADDR** поддерживается в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="cb21e-112">The **SOCKADDR\_STORAGE** structure is supported on Windows Server 2003 and later.</span></span>

<span data-ttu-id="cb21e-113">Структура SOCKADDR и SOCKADDR \_ в представленных ниже структурах используются с IPv4.</span><span class="sxs-lookup"><span data-stu-id="cb21e-113">The sockaddr structure and sockaddr\_in structures below are used with IPv4.</span></span> <span data-ttu-id="cb21e-114">Другие протоколы используют аналогичные структуры.</span><span class="sxs-lookup"><span data-stu-id="cb21e-114">Other protocols use similar structures.</span></span>

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

<span data-ttu-id="cb21e-115">\_Приведенные ниже SOCKADDR in6 и SOCKADDR \_ in6 \_ используются с IPv6.</span><span class="sxs-lookup"><span data-stu-id="cb21e-115">The sockaddr\_in6 and sockaddr\_in6\_old structures below are used with IPv6.</span></span>

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

<span data-ttu-id="cb21e-116">В пакете средств разработки программного обеспечения Microsoft Windows (SDK), выпущенном для Windows Vista и более поздних версий, **SOCKADDR** и **SOCKADDR \_ в** тегах typedef определяются для SOCKADDR и SOCKADDR \_ в структурах следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cb21e-116">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, **SOCKADDR** and **SOCKADDR\_IN** typedef tags are defined for sockaddr and sockaddr\_in structures as follows:</span></span>

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

<span data-ttu-id="cb21e-117">В Windows SDK, выпущенном для Windows Vista и более поздних версий, Организация файлов заголовков изменилась, а SOCKADDR и SOCKADDR \_ в структурах определяются в файле заголовка файла *Ws2def. h* , а не в файле заголовка *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="cb21e-117">On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the sockaddr and sockaddr\_in structures are defined in the *Ws2def.h* header file, not the *Winsock2.h* header file.</span></span> <span data-ttu-id="cb21e-118">Файл заголовка *Ws2def. h* автоматически включается в заголовочный файл *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="cb21e-118">The *Ws2def.h* header file is automatically included by the *Winsock2.h* header file.</span></span> <span data-ttu-id="cb21e-119">\_Структура in6 SOCKADDR определена в файле заголовка *Ws2ipdef. h* , а не в файле заголовка *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="cb21e-119">The sockaddr\_in6 structure is defined in the *Ws2ipdef.h* header file, not the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="cb21e-120">Файл заголовка *Ws2ipdef. h* автоматически включается в заголовочный файл *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="cb21e-120">The *Ws2ipdef.h* header file is automatically included by the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="cb21e-121">Файлы заголовков *Ws2def. h* и *Ws2ipdef. h* никогда не следует использовать напрямую.</span><span class="sxs-lookup"><span data-stu-id="cb21e-121">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="example-code"></a><span data-ttu-id="cb21e-122">Пример кода</span><span class="sxs-lookup"><span data-stu-id="cb21e-122">Example Code</span></span>

<span data-ttu-id="cb21e-123">В следующем примере демонстрируется использование структуры **SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="cb21e-123">The following example demonstrates the use of the **sockaddr** structure.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="cb21e-124">См. также:</span><span class="sxs-lookup"><span data-stu-id="cb21e-124">See Also</span></span>

<span data-ttu-id="cb21e-125">[**\_хранилище SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb21e-125">[**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span></span>


 

 
