---
title: Close-Session
description: Используйте пакет Close-Session, чтобы сообщить серверу BITS о завершении передачи файла и завершить сеанс.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Sessionные БИТЫ
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021202"
---
# <a name="close-session"></a>Close-Session

Используйте пакет **закрытия сеанса** , чтобы сообщить серверу BITS о завершении передачи файла и завершить сеанс.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Заголовки

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>\_запись BITS
</dt> <dd>

Команда, относящаяся к службе BITS, которая определяет этот пакет серверу BITS.

Замените Remote-URL абсолютным или относительным URI. Обычно замените Remote-URL именем удаленного файла задания. Рекомендации по балансировке сетевой нагрузки см. в заголовке BITS-Host-ID в пакете [**создания сеанса**](create-session.md) .

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Идентифицирует этот пакет запроса как пакет Close-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID
</dt> <dd>

Строковый идентификатор GUID, определяющий сеанс на сервере. Замените {GUID} идентификатором сеанса, возвращаемым сервером в ответ на запрос на создание пакета ответа [**для создания сеанса**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

Сервер BITS освобождает все ресурсы и удаляет все временные файлы при получении этого пакета.

Для заданий отправки и ответа необходимо загрузить ответ перед отправкой **закрытого сеанса**. В противном случае ответ будет потерян.

Если отправить этот пакет перед отправкой всех фрагментов, файл отправки будет удален; невозможно передать частичный файл.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подтверждение для закрытия сеанса**](ack-for-close-session.md)
</dt> <dt>

[**Отмена — сеанс**](cancel-session.md)
</dt> <dt>

[**Создание сеанса**](create-session.md)
</dt> </dl>

 

 




