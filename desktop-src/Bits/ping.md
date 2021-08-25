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
ms.openlocfilehash: 479e03e6e18c0ec7421bd225744c5181029fc2b2e220f35c7bae7a3b02d42b07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004894"
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

## <a name="remarks"></a>Remarks

Пакет **ping** является необязательным. Вместо отправки пакета **проверки связи** можно использовать пакет [**создания сеанса**](create-session.md) для установления соединения и согласования безопасности. Однако для этой цели более эффективно использовать пакет **ping** .

## <a name="see-also"></a>См. также

<dl> <dt>

[**Подтверждение проверки связи**](ack-for-ping.md)
</dt> <dt>

[**Создание сеанса**](create-session.md)
</dt> </dl>

 

 




