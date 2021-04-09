---
title: Bluetooth и привязка
description: Bluetooth использует функцию bind для привязки к сокету.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth и привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891032"
---
# <a name="bluetooth-and-bind"></a>Bluetooth и привязка

Bluetooth использует функцию [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) для привязки к сокету. Чтобы привязать сокет Bluetooth, вызовите функцию **BIND** с помощью структуры [**SOCKADDR \_ БС**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) . Используйте структуру **SOCKADDR \_ БС** со следующими параметрами:

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

Для клиентских приложений элемент порта должен быть равен нулю, чтобы обеспечить назначение соответствующей локальной конечной точки. В серверных приложениях элемент порта должен быть допустимым номером порта или BT- \_ портом \_ ANY; порты, автоматически назначенные с помощью BT- \_ порта, \_ могут быть запрошены в дальнейшем при вызове функции [**жетсоккнаме**](bluetooth-and-getsockname.md) . Допустимый диапазон для запроса определенного порта RFCOMM — от 1 до 30. Каналы сервера являются глобальными ресурсами, и для RFCOMM на любом устройстве Bluetooth доступно только 30 каналов сервера, которые должны быть общими для всех сокетов Windows, принадлежащих семейству адресов Bluetooth. Если канал сервера недоступен или указанный канал сервера уже зарезервирован, вызов [**привязки**](/windows/desktop/api/winsock/nf-winsock-bind) завершается ошибкой.

После успешного возврата из BIND канал сервера резервируется до закрытия сокета. Используйте функцию [**жетсоккнаме**](bluetooth-and-getsockname.md) , чтобы получить номер канала для регистрации SDP.

Приложения должны использовать автоматическое выделение для канала сервера.

Функция [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) не объявляет серверное приложение автоматически с помощью средства распространения Bluetooth. приложения должны вызывать функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) для обнаружения удаленными приложениями Bluetooth.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сокеты Windows](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**выполняется**](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 