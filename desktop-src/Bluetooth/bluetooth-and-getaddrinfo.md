---
title: Bluetooth и функцию getaddrinfo
description: Функция функцию getaddrinfo предоставляет преобразование из имени узла в адрес для транспортов на основе IP-адресов. Поскольку функция функцию getaddrinfo относится только к транспортам на основе IP-адресов, она завершается сбоем на сокетах Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth и функцию getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793537"
---
# <a name="bluetooth-and-getaddrinfo"></a>Bluetooth и функцию getaddrinfo

Функция [**функцию getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) предоставляет преобразование из имени узла в адрес для транспортов на основе IP-адресов. Поскольку функция **функцию getaddrinfo** относится только к транспортам на основе IP-адресов, она завершается сбоем на сокетах Bluetooth.

Чтобы выполнить преобразование из имени узла в адрес для сокетов Bluetooth, используйте функцию [**всалукупсервицебегин**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) с **\_ контейнерами Луп** для запроса удаленных устройств, а затем найдите конкретное соответствующее удаленное имя и соответствующий адрес.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**функцию getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 