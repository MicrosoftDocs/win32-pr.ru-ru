---
description: При добавлении поддержки IPv6 необходимо убедиться, что приложение определяет структуры данных правильного размера.
ms.assetid: 2bf353e2-38d5-462c-9e6c-65886b617215
title: Изменение структур данных для IPv6 Winsock Аппикатионс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999c0d0c5a335c1367165c227fc1aad805579db5a790a19d316a1624e922947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741554"
---
# <a name="changing-data-structures-for-ipv6-winsock-appications"></a>Изменение структур данных для IPv6 Winsock Аппикатионс

При добавлении поддержки IPv6 необходимо убедиться, что приложение определяет структуры данных правильного размера. Размер IPv6-адреса гораздо больше, чем адрес IPv4. Структуры, жестко запрограммированные для обработки размера адреса IPv4 при хранении IP-адреса, приведут к проблемам в приложении и должны быть изменены.

Рекомендации

Лучшим подходом к обеспечению правильности размера структур является использование структуры [**\_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) . Структура **\_ хранилища SOCKADDR** не зависит от версии IP-адреса. Если для хранения IP-адресов используется структура **\_ хранилища SOCKADDR** , адреса IPv4 и IPv6 могут быть правильно обработаны с одной базой кода.

Следующий пример, который является выдержкой из файла Server. c, найденного в приложении б, определяет подходящее использование структуры **\_ хранилища SOCKADDR** . Обратите внимание, что структура при правильном использовании, как показано в этом примере, корректно обрабатывает адрес IPv4 или IPv6.


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
> структура [**\_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) является новой для Windows XP.

 

Код, чтобы избежать

Как правило, многие приложения используют структуру [**SOCKADDR**](sockaddr-2.md) для хранения независимых от протокола адресов или **SOCKADDR \_ в** структуре для IP-адресов. Ни структура SOCKADDR, ни **SOCKADDR \_ в** структуре не имеют достаточного размера для хранения IPv6-адресов, и поэтому они недостаточно, если приложение должно быть совместимо с IPv6.

Задача "программирование"

**Изменение существующей базы кода с IPv4 на IPv4 и взаимодействие с IPv6**

1.  Получите служебную программу Checkv4.exe. эта программа входит в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows, который предоставляется через подписку MSDN или из интернета в качестве загружаемого файла.
2.  Запустите служебную программу Checkv4.exe для своего кода. Узнайте, как запустить служебную программу Checkv4.exe для файлов в разделе об [использовании служебной программы Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  Служебная программа предупреждает вас об использовании **SOCKADDR** или **SOCKADDR \_ в** структурах и предоставляет рекомендации по замене либо с помощью совместимого с IPv6 [**структуры \_ хранилища SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)).
4.  Замените все подобные экземпляры и соответствующий код соответствующим образом, чтобы использовать структуру **\_ хранилища SOCKADDR** .

Кроме того, можно выполнить поиск экземпляров **SOCKADDR** и **SOCKADDR \_ в** базе кода в структурах, а также изменить все такое использование (и другой связанный код соответственно) на структуру **\_ хранилища SOCKADDR** .

> [!Note]  
> Структуры **\_ хранилища** **аддринфо** и SOCKADDR включают в себя протокол и члены семейства адресов (семейство **ии \_** и **\_ семейство SS**) соответственно. RFC 2553 указывает, что член **\_ семейства AI** [**аддринфо**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) в качестве целого числа, а **\_ семейство SS** указано как короткое, а прямое копирование между этими членами приводит к ошибке компилятора.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[рекомендации по IPv6 для приложений Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Сокеты с двумя стеками для IPv6-приложений Winsock](dual-stack-sockets.md)
</dt> <dt>

[Вызовы функций для IPv6-приложений Winsock](function-calls-2.md)
</dt> <dt>

[Использование жестко закодированных IPv4-адресов](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Проблемы с пользовательским интерфейсом для IPv6-приложений Winsock](user-interface-issues-2.md)
</dt> <dt>

[Базовые протоколы для IPv6-приложений Winsock](underlying-protocols-2.md)
</dt> </dl>

 

 
