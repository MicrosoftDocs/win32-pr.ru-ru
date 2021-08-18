---
title: Create-Session
description: Используйте пакет Create-Session, чтобы запросить сеанс передачи с сервером BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Sessionные БИТЫ
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021192"
---
# <a name="create-session"></a>Create-Session

Используйте пакет **создания сеанса** , чтобы запросить сеанс передачи с сервером BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Заголовки

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS
</dt> <dd>

Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.

Замените Remote-URL абсолютным или относительным URI. Обычно замените Remote-URL именем удаленного файла задания. Рекомендации по балансировке сетевой нагрузки см. в заголовке BITS-Host-ID.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Идентифицирует этот пакет запроса как пакет Create-Session.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Поддерживаемые BITS — протоколы
</dt> <dd>

Разделенный пробелами список протоколов, поддерживаемых клиентом. Используйте строковые идентификаторы GUID для обнаружения протоколов. Укажите список в порядке предпочтения от наиболее предпочтительных. В следующей таблице перечислены протоколы, поддерживаемые клиентом BITS. Замените {GUID1}... {Гуидн} с одним или несколькими строковыми идентификаторами GUID из списка.



| Протокол                                          | Описание                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | протокол Upload BITS 1,5<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarks

Перед отправкой пакета Create-Session необходимо отправить пакет [**проверки связи**](ping.md) для установки HTTP-соединения. Пакет Create-Session может также установить соединение. Однако Create-Session пакет менее эффективен.

Сервер выбирает нужный протокол из списка, который предоставляется клиентом в заголовке BITS-Supported-protocols. Сервер возвращает выбранный протокол в заголовке BITS-Protocol [**подтверждения для пакета ответа на создание сеанса**](ack-for-create-session.md) .

Клиент ожидает, что сервер возвратит подтверждение на ответный пакет [**для создания сеанса**](ack-for-create-session.md) . Если серверу удалось установить сеанс, клиент использует пакет запроса [**фрагмента**](fragment.md) для отправки диапазонов файла на сервер.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подтверждение для создания сеанса**](ack-for-create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> <dt>

[**Проверка связи**](ping.md)
</dt> </dl>

 

 





