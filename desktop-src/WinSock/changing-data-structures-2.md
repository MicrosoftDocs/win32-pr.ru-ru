---
description: При добавлении поддержки IPv6 необходимо убедиться, что приложение определяет структуры данных правильного размера.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Изменение структур данных для IPv6 Winsock Аппикатионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2c91e19ed733d111bd4e12d824da6ee1a988e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701553"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a><span data-ttu-id="503e7-103">Изменение структур данных для IPv6 Winsock Аппикатионс</span><span class="sxs-lookup"><span data-stu-id="503e7-103">Changing Data Structures for IPv6 Winsock Appications</span></span>

<span data-ttu-id="503e7-104">При добавлении поддержки IPv6 необходимо убедиться, что приложение определяет структуры данных правильного размера.</span><span class="sxs-lookup"><span data-stu-id="503e7-104">When adding support for IPv6, you must ensure that your application defines properly sized data structures.</span></span> <span data-ttu-id="503e7-105">Размер IPv6-адреса гораздо больше, чем адрес IPv4.</span><span class="sxs-lookup"><span data-stu-id="503e7-105">The size of an IPv6 address is much larger than an IPv4 address.</span></span> <span data-ttu-id="503e7-106">Структуры, жестко запрограммированные для обработки размера адреса IPv4 при хранении IP-адреса, приведут к проблемам в приложении и должны быть изменены.</span><span class="sxs-lookup"><span data-stu-id="503e7-106">Structures that are hard-coded to handle the size of an IPv4 address when storing an IP address will cause problems in your application, and must be modified.</span></span>

<span data-ttu-id="503e7-107">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="503e7-107">Best Practice</span></span>

<span data-ttu-id="503e7-108">Лучшим подходом к обеспечению правильности размера структур является использование структуры [**\_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="503e7-108">The best approach to ensuring that your structures are properly sized is to use the [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure.</span></span> <span data-ttu-id="503e7-109">Структура **\_ хранилища SOCKADDR** не зависит от версии IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="503e7-109">The **SOCKADDR\_STORAGE** structure is agnostic to IP address version.</span></span> <span data-ttu-id="503e7-110">Если для хранения IP-адресов используется структура **\_ хранилища SOCKADDR** , адреса IPv4 и IPv6 могут быть правильно обработаны с одной базой кода.</span><span class="sxs-lookup"><span data-stu-id="503e7-110">When the **SOCKADDR\_STORAGE** structure is used to store IP addresses, IPv4 and IPv6 addresses can be properly handled with one code base.</span></span>

<span data-ttu-id="503e7-111">Следующий пример, который является выдержкой из файла Server. c, найденного в приложении б, определяет подходящее использование структуры **\_ хранилища SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="503e7-111">The following example, which is an excerpt taken from the Server.c file found in Appendix B, identifies an appropriate use of the **SOCKADDR\_STORAGE** structure.</span></span> <span data-ttu-id="503e7-112">Обратите внимание, что структура при правильном использовании, как показано в этом примере, корректно обрабатывает адрес IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="503e7-112">Notice that the structure, when used properly as this example shows, gracefully handles either an IPv4 or IPv6 address.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

#define BUFFER_SIZE 512
#define DEFAULT_PORT "27015"

int main(int argc, char **argv)
{
    char Buffer[BUFFER_SIZE] = {0};
    char *Hostname;
    int Family = AF_UNSPEC;
    int SocketType = SOCK_STREAM;
    char *Port = DEFAULT_PORT;
    char *Address = NULL;
    int i = 0;
    DWORD dwRetval = 0;
    int iResult = 0;
    int FromLen = 0;
    int AmountRead = 0;

    SOCKADDR_STORAGE From;

    WSADATA wsaData;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;

    // Parse arguments
    if (argc >= 1) {
        Hostname = argv[1];
    }    

   // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }

    From.ss_family = (ADDRESS_FAMILY) Family;
    
    //...
        
        return 0;
}
```



> [!Note]  
> <span data-ttu-id="503e7-113">Структура [**\_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) является новой для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="503e7-113">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure is new for Windows XP.</span></span>

 

<span data-ttu-id="503e7-114">Код, чтобы избежать</span><span class="sxs-lookup"><span data-stu-id="503e7-114">Code To Avoid</span></span>

<span data-ttu-id="503e7-115">Как правило, многие приложения используют структуру [**SOCKADDR**](sockaddr-2.md) для хранения независимых от протокола адресов или **SOCKADDR \_ в** структуре для IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="503e7-115">Typically, many applications used the [**sockaddr**](sockaddr-2.md) structure to store protocol-independent addresses, or the **sockaddr\_in** structure for IP addresses.</span></span> <span data-ttu-id="503e7-116">Ни структура SOCKADDR, ни **SOCKADDR \_ в** структуре не имеют достаточного размера для хранения IPv6-адресов, и поэтому они недостаточно, если приложение должно быть совместимо с IPv6.</span><span class="sxs-lookup"><span data-stu-id="503e7-116">Neither the sockaddr structure nor the **sockaddr\_in** structure is large enough to hold IPv6 addresses, and therefore both are insufficient if your application is to be IPv6 compatible.</span></span>

<span data-ttu-id="503e7-117">Задача "программирование"</span><span class="sxs-lookup"><span data-stu-id="503e7-117">Coding Task</span></span>

<span data-ttu-id="503e7-118">**Изменение существующей базы кода с IPv4 на IPv4 и взаимодействие с IPv6**</span><span class="sxs-lookup"><span data-stu-id="503e7-118">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="503e7-119">Получите служебную программу Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="503e7-119">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="503e7-120">Эта программа входит в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows, который предоставляется через подписку MSDN или из Интернета в качестве загружаемого файла.</span><span class="sxs-lookup"><span data-stu-id="503e7-120">The utility is included with the Microsoft Windows Software Development Kit (SDK) which is made available through your MSDN subscription, or from the web as a download.</span></span>
2.  <span data-ttu-id="503e7-121">Запустите служебную программу Checkv4.exe для своего кода.</span><span class="sxs-lookup"><span data-stu-id="503e7-121">Run the Checkv4.exe utility against your code.</span></span> <span data-ttu-id="503e7-122">Узнайте, как запустить служебную программу Checkv4.exe для файлов в разделе об [использовании служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="503e7-122">Learn about how to run the Checkv4.exe utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="503e7-123">Служебная программа предупреждает вас об использовании **SOCKADDR** или **SOCKADDR \_ в** структурах и предоставляет рекомендации по замене либо с помощью совместимого с IPv6 [**структуры \_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="503e7-123">The utility alerts you to usage of **sockaddr** or **sockaddr\_in** structures, and provides recommendations on how to replace either with the IPv6 compatible structure [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).</span></span>
4.  <span data-ttu-id="503e7-124">Замените все подобные экземпляры и соответствующий код соответствующим образом, чтобы использовать структуру **\_ хранилища SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="503e7-124">Replace any such instances, and associated code as appropriate, to use the **SOCKADDR\_STORAGE** structure.</span></span>

<span data-ttu-id="503e7-125">Кроме того, можно выполнить поиск экземпляров **SOCKADDR** и **SOCKADDR \_ в** базе кода в структурах, а также изменить все такое использование (и другой связанный код соответственно) на структуру **\_ хранилища SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="503e7-125">Alternatively, you can search your code base for instances of the **sockaddr** and **sockaddr\_in** structures, and change all such usage (and other associated code, as appropriate) to the **SOCKADDR\_STORAGE** structure.</span></span>

> [!Note]  
> <span data-ttu-id="503e7-126">Структуры **\_ хранилища** **аддринфо** и SOCKADDR включают в себя протокол и члены семейства адресов (семейство **ии \_** и **\_ семейство SS**) соответственно.</span><span class="sxs-lookup"><span data-stu-id="503e7-126">The **addrinfo** and **SOCKADDR\_STORAGE** structures include protocol and address family members (**ai\_family** and **ss\_family**), respectively.</span></span> <span data-ttu-id="503e7-127">RFC 2553 указывает, что член **\_ семейства AI** [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) в качестве целого числа, а **\_ семейство SS** указано как короткое, а прямое копирование между этими членами приводит к ошибке компилятора.</span><span class="sxs-lookup"><span data-stu-id="503e7-127">RFC 2553 specifies the **ai\_family** member of [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) as an int, while **ss\_family** is specified as a short; as such, a direct copy between those members results in a compiler error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="503e7-128">См. также</span><span class="sxs-lookup"><span data-stu-id="503e7-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="503e7-129">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="503e7-129">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="503e7-130">Сокеты с двумя стеками для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="503e7-130">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="503e7-131">Вызовы функций для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="503e7-131">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="503e7-132">Использование жестко закодированных IPv4-адресов</span><span class="sxs-lookup"><span data-stu-id="503e7-132">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="503e7-133">Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="503e7-133">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="503e7-134">Базовые протоколы для IPv6-приложений Winsock</span><span class="sxs-lookup"><span data-stu-id="503e7-134">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
