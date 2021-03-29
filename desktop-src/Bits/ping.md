---
title: Проверка связи
description: Используйте пакет Ping для установления соединения и согласования безопасности с сервером.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Проверка связи
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "105654255"
---
# <a name="ping"></a>Проверка связи

Используйте пакет **ping** для установления соединения и согласования безопасности с сервером.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a>Заголовки

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS
</dt> <dd>

Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.

Замените Remote-URL абсолютным или относительным URI. Обычно замените Remote-URL именем удаленного файла задания.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Идентифицирует этот пакет запроса как пакет проверки связи.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Пакет **ping** является необязательным. Вместо отправки пакета **проверки связи** можно использовать пакет [**создания сеанса**](create-session.md) для установления соединения и согласования безопасности. Однако для этой цели более эффективно использовать пакет **ping** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подтверждение проверки связи**](ack-for-ping.md)
</dt> <dt>

[**Создание сеанса**](create-session.md)
</dt> </dl>

 

 




