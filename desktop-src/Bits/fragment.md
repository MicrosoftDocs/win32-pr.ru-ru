---
title: Fragment
description: Используйте пакет фрагмента, чтобы отправить фрагмент файла отправки на сервер.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- БИТЫ фрагмента
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613acaabc017b9e673d2cba6a64f84db054a4cdc0d73a0639fcf8455edff8298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528834"
---
# <a name="fragment"></a>Fragment

Используйте пакет **фрагмента** , чтобы отправить фрагмент файла отправки на сервер.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
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

Идентифицирует этот пакет запроса как пакет фрагмента.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS — Session-ID
</dt> <dd>

Строковый идентификатор GUID, определяющий сеанс на сервере. Замените {GUID} идентификатором сеанса, возвращаемым сервером в ответ на запрос на создание пакета ответа [**для создания сеанса**](ack-for-create-session.md) .

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name
</dt> <dd>

Укажите этот заголовок только с начальным фрагментом. Замените filename именем локального файла в задании. Имя не включает путь.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Длина содержимого
</dt> <dd>

Замените length числом байтов, отправленных в тексте фрагмента.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Диапазон содержимого
</dt> <dd>

Указывает серверу, куда применять диапазон в целевом файле. Замените Range на начальное и конечное смещение диапазона в целевом файле. Смещение отсчитывается от нуля. Если заданный диапазон перекрывает существующий диапазон, BITS записывает только неперекрывающиеся части диапазона; BITS не перезаписывает существующее содержимое. Например, если первый пакет содержал диапазон от 0 до 100, а второй пакет содержал диапазон от 50 до 150, BITS записывает только байты с 101 по 150 из второго пакета. Замените Total — length общим числом байтов в файле.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Кодирование содержимого
</dt> <dd>

Замените кодировку типом кодировки, используемой клиентом в фрагменте. Клиент должен использовать кодировку, которую сервер определяет в заголовке Accept-Encoding [**подтверждения для пакета ответа на создание сеанса**](ack-for-create-session.md) . Сервер использует тип кодировки для декодирования фрагмента. Все фрагменты должны указывать одинаковую кодировку.

Не отправляйте этот заголовок, если тип кодировки — Identity. Сервер BITS поддерживает только кодирование удостоверений.

</dd> </dl>

## <a name="remarks"></a>Remarks

Фрагмент — это диапазон байтов, отправленных в тексте пакета. Клиент отправляет фрагменты в последовательном порядке, начиная с нулевого смещения. сервер не отслеживает несмежные диапазоны. Если клиент отправляет несмежные диапазоны, сервер возвращает код возврата HTTP 416 (с диапазоном, который не соответствует) в ответе [**ACK для ответа фрагмента**](ack-for-fragment.md) .

Заголовки Content-*XXXX* — это стандартные заголовки HTTP 1,1. Дополнительные сведения о заголовках Content-*XXXX* см. в спецификации [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .

## <a name="see-also"></a>См. также

<dl> <dt>

[**Подтверждение для фрагмента**](ack-for-fragment.md)
</dt> <dt>

[**Закрыть — сеанс**](close-session.md)
</dt> <dt>

[**Создание сеанса**](create-session.md)
</dt> </dl>

 

 




