---
title: Использование RPC с прокси-сервером Winsock
description: Использование RPC с прокси-сервером Winsock
ms.assetid: d36e2737-f6a0-40ce-92e0-058976c08eb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5f658cf60d7e530da99ee139dbcdcbb2c89685
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070577"
---
# <a name="using-rpc-with-winsock-proxy"></a>Использование RPC с прокси-сервером Winsock

В выпуске сервера Microsoft Internet Access Server входит Winsock Proxy, улучшенная версия API Windows Sockets версии 1,1. Прокси-сервер Winsock позволяет приложению Windows Sockets, работающему на клиенте частной сети, работать так же, как если бы оно было напрямую подключено к удаленному Интернет-серверу. Прокси-сервер Microsoft выступает в качестве узла для этого подключения. Это означает, что все подключения на уровне приложения проходят через один защищенный компьютер — компьютер шлюза, на котором работает прокси-сервер Microsoft.

Обычно для передачи датаграмм-пакетов библиотека DLL транспорта RPC обходит функции [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) и [**реквфром**](/windows/desktop/api/winsock/nf-winsock-recvfrom) , предоставленные в Wsock32.dll, и напрямую взаимодействует с драйвером соответствующего устройства. Это повышает скорость передачи пакетов, но делает функции прокси-сервера Winsock недоступными для приложения.

Каждый поставщик сетевых протоколов имеет связанный GUID. Библиотека времени выполнения RPC сравнивает идентификаторы GUID и IPX с известными идентификаторами Майкрософт. Если они не совпадают, RPC автоматически использует Winsock.

Другой возможностью прокси-сервера Winsock является возможность имитировать транспортный протокол TCP через транспорт Novell SPX, если на клиентском компьютере SPX не установлен протокол TCP. Чтобы использовать эту функцию с приложениями RPC, измените системный реестр на каждом клиентском компьютере, чтобы добавить эту запись:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ClientProtocols
   ncacn_ip_tcp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltccm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Измените реестр на каждом сервере, чтобы добавить эту запись:

```
HKEY_LOCAL_MACHINE\Software\Microsoft\Rpc\ServerProtocols
   ncacn_ip_tcp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
   ncadg_ip_udp = "rpcltscm.dll"<dl>
<dt>

   Data type
</dt>
<dd>   REG_SZ</dd>
</dl>
```

Дополнительные сведения о протоколах транспорта RPC см. в разделе [Указание последовательностей протоколов](specifying-protocol-sequences.md). Дополнительные сведения о прокси-сервере Winsock см. в документации по продукту для сервера Microsoft Internet Access Server.

В Windows 2000 не реализованы записи реестра **ClientProtocols** и **серверпротоколс** . Корпорация Майкрософт предоставляет все хорошо известные транспорты в составе библиотеки времени выполнения. Поэтому эти записи не требуются.

 

 