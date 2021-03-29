---
title: Cancel-Session
description: Используйте пакет Cancel-Session, чтобы завершить сеанс передачи с сервером BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Sessionные БИТЫ
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105654251"
---
# <a name="cancel-session"></a>Cancel-Session

Используйте пакет **Cancel-Session** для завершения сеанса передачи с сервером BITS.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
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

Идентифицирует этот пакет запроса как пакет Cancel-Session.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID
</dt> <dd>

Строковый идентификатор GUID, определяющий сеанс на сервере. Замените {GUID} идентификатором сеанса, возвращаемым сервером в ответ на запрос на создание пакета ответа [**для создания сеанса**](ack-for-create-session.md) .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот пакет отменяет задание отправки, если оно отправляется до отправки последнего фрагмента. Cancel-Session не влияет на файл, последний фрагмент которого уже был отправлен. Когда сервер BITS получает последний фрагмент, он записывает файл в конечное место назначения, а в случае отправки-ответа отправляет файл в серверное приложение. В случае отправки-ответа пакет Cancel-Session отменяет часть ответа задания отправки и ответа.

Сервер BITS освобождает все ресурсы и удаляет все временные файлы при получении этого пакета.

Клиент BITS отправляет этот пакет, когда пользователь отменяет задание.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Подтверждение для создания сеанса**](ack-for-create-session.md)
</dt> <dt>

[**Закрыть — сеанс**](close-session.md)
</dt> </dl>

 

 




