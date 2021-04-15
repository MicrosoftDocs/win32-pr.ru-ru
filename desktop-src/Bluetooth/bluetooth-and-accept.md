---
title: Bluetooth и Accept
description: Bluetooth использует функцию Accept для включения входящих попыток подключения к сокету.
ms.assetid: 79708118-2f70-4759-b5d6-cf5cfc33c27e
keywords:
- гласит
- Bluetooth
- Bluetooth
- Bluetooth и Accept
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28dff84ec05429411614e64a08ab159a5ee134b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105654340"
---
# <a name="bluetooth-and-accept"></a>Bluetooth и Accept

Bluetooth использует функцию [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) для включения входящих попыток подключения к сокету. БС \_ -адрес клиентского приложения получается путем считывания раздела, относящегося к транспорту Bluetooth, возвращенной структуры [**SOCKADDR**](/windows/desktop/WinSock/sockaddr-2) . Использование функции **Accept** с Bluetooth имеет следующий формат:

-   Параметр *addr* функции [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) является необязательным указателем на буфер, который получает адрес связывающей сущности, как известно на уровне связи. Возвращается указатель на структуру [**\_ БС SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) с адресом удаленного устройства Bluetooth.
-   Параметр *аддрлен* функции [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) является необязательным указателем на целое число, которое содержит длину адреса в байтах. Целое число должно быть больше или равно значению **sizeof** ([**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**гласит**](/windows/desktop/api/winsock2/nf-winsock2-accept)
</dt> </dl>

 

 