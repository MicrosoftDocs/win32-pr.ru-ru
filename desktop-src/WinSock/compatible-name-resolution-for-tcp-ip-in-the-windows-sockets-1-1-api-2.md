---
description: обратите внимание, что функции Windows сокеты 1,1 для разрешения имен относятся только к сетям TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13dfb1a403f782d0349e20729117fe1f4aed01479b01a6c2b5968f1d9bf15f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322304"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1

> [!Note]  
> все функции сокетов 1,1 Windows для разрешения имен относятся только к сетям TCP/IP IPv4. Разработчикам приложений настоятельно не рекомендуется продолжать использовать эти функции, связанные с транспортом, которые поддерживают только IPv4.

 

Разработчики приложений должны использовать следующие функции, которые не зависят от протокола и поддерживают разрешение имен IPv6 и IPv4.

-   [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**жетаддринфоекс**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**жетаддринфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**жетнамеинфов**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Сокеты 1,1 определяют ряд подпрограмм, используемых для разрешения имен с помощью сетей TCP/IP (IP версии 4). Они иногда называются **жетксбии** функциями и включают следующее:

<dl>

[**имя узла**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**жетпротобинаме**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**жетпротобинумбер**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**жетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**жетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

Также определены асинхронные версии этих функций.

<dl>

[**всаасинкжесостбяддр**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**всаасинкжесостбинаме**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**всаасинкжетпротобинаме**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**всаасинкжетпротобинумбер**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**всаасинкжетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**всаасинкжетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

Существуют также две функции, реализованные в Winsock2.dll, которые используются для преобразования точечной нотации IPv4-адресов в строковые и двоичные представления соответственно.

<dl>

[**INET \_ АДР**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**INET \_ нтоа**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

для обеспечения исключительной обратной совместимости с сокетами Windows 1,1 все устаревшие функции только с протоколом IPv4 продолжают поддерживаться до тех пор, пока имеется хотя бы один поставщик пространства имен, поддерживающий \_ семейство адресов INET (эти функции не относятся к IP версии 6, обозначенной AF \_ INET6).

32.dll Ws2 \_ реализует эти функции совместимости с точки зрения нового, независимого от протокола имени средства разрешения имен с помощью соответствующей последовательности вызовов функций [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) / **Next** / **End** . Ниже приведены сведения о сопоставлении функций **жетксбии** с функциями разрешения имен. WSs2 \_32.dll обрабатывает различия между асинхронной и синхронной версиями функций **жетксбии** , поэтому обсуждаются только реализации синхронных функций **жетксбии** .

в этом разделе описывается совместимость разрешения имен для TCP/IP в интерфейсе API Windows sockets 1,1. В следующем списке перечислены подразделы этого раздела.

-   [Базовый подход для Жетксбии в API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Функции жетпротобинаме и жетпротобинумбер в API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Функции жетсервбинаме и жетсервбипорт в API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Функция GetHostByName в API](gethostbyname-function-in-the-api-2.md)
-   [Функция жесостбяддр в API](gethostbyaddr-function-in-the-api-2.md)
-   [Функция onhostname в API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Разрешение имен, не зависящее от протокола](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Регистрация и разрешение имен](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
