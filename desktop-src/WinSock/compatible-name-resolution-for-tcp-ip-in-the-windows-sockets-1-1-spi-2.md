---
description: Windows Сокеты 1,1 определяют ряд подпрограмм, которые использовались для разрешения имен IPv4 в сетях TCP/IP. Эти функции также называются функциями Жетксбии и включают следующее.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: совместимое разрешение имен для TCP/IP в сокетах Windows 1,1 SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea355eb85d41a507e4970bf0c8d925a41ed81ca51c08b9c77955ad702a62d27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051682"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a>совместимое разрешение имен для TCP/IP в сокетах Windows 1,1 SPI

Windows Сокеты 1,1 определяют ряд подпрограмм, которые использовались для разрешения имен IPv4 в сетях TCP/IP. Эти функции также называются функциями **жетксбии** и включают следующее.

[**имя узла**](/windows/desktop/api/winsock/nf-winsock-gethostname)

[**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[**жетпротобинаме**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[**жетпротобинумбер**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[**жетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[**жетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-getservbyport)

Также определены асинхронные версии этих функций.

[**всаасинкжесостбяддр**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[**всаасинкжесостбинаме**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[**всаасинкжетпротобинаме**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[**всаасинкжетпротобинумбер**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[**всаасинкжетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[**всаасинкжетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

Эти функции относятся к сетям TCP/IP. разработчикам приложений, не зависящих от протокола, не рекомендуется продолжать использовать эти функции, связанные с транспортом. однако, чтобы обеспечить максимальную обратную совместимость с сокетами Windows 1,1, предыдущие функции продолжают поддерживаться до тех пор, пока имеется хотя бы один поставщик пространства имен, поддерживающий \_ семейство адресов AF INET.

*\_32.dllWs2* реализует эти функции совместимости с точки зрения нового, независимого от протокола имени средства разрешения имен с помощью соответствующей последовательности вызовов [**функций всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)и [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) . Ниже приведены сведения о сопоставлении функций **жетксбии** с функциями разрешения имен. Ws2 \_32.dll обрабатывает различия между асинхронной и синхронной версиями функций **жетксбии** , так что обсуждаются только реализации синхронных функций **жетксбии** .

 

 
