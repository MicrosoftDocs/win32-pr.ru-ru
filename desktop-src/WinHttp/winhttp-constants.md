---
description: В этом разделе определяются константы, используемые WinHTTP.
ms.assetid: 460f1463-57a8-47eb-9957-17976757bd7f
title: Константы WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e37b0e4de7aa3df5e155933bea2be25386c1637
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113175006"
---
# <a name="winhttp-constants"></a>Константы WinHTTP

WinHTTP использует следующие константы:

<dl>

<dt>

[**сообщения об ошибках**](error-messages.md)
</dt> <dd>

Сообщения об ошибках, относящиеся к функциям WinHTTP. эти функции также возвращают Windows сообщения об ошибках, если это уместно. Значение, соответствующее каждой константе, является значением константы для функций интерфейса прикладного программирования (API) и младшими 16 битами номера ошибки для объекта [**WinHttpRequest**](winhttprequest.md) .

</dd> <dt>

[**Коды состояния HTTP**](http-status-codes.md)
</dt> <dd>

Константы и соответствующие значения, указывающие коды состояния HTTP, возвращаемые серверами в Интернете.

</dd> <dt>

[**Флаги параметров**](option-flags.md)
</dt> <dd>

Флаги параметров, поддерживаемые [**винхттпкуерйоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) и [**винхттпсетоптион**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption). Все допустимые флаги параметров имеют значение, большее или равное \_ первому \_ параметру WinHTTP, и меньше или равно \_ последнему \_ параметру WinHTTP.

</dd> <dt>

[**\_Порт Интернета**](internet-port.md)
</dt> <dd>

Значение слова, указывающее порт.

</dd> <dt>

[**\_схема Интернета**](internet-scheme.md)
</dt> <dd>

Схемы Интернета, поддерживаемые WinHTTP.

</dd>

<dt>

[**Флаги сведений о запросе**](query-info-flags.md)
</dt>
<dd>

Атрибуты и модификаторы, используемые [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).
</dd>

<dt>

**WINHTTP_EXTENDED_HEADER_FLAG_UNICODE**
</dt>
<dd>

Имеет значение 0x00000001. Указывает, [винхттпаддрекуессеадерсекс](/windows/win32/api/winhttp/nf-winhttp-winhttpaddrequestheadersex) , что передаваемые строки являются строками в Юникоде.
</dd>

<dt>

**WINHTTP_READ_DATA_EX_FLAG_FILL_BUFFER**
</dt>
<dd>

Имеет значение 0x0000000000000001ull. Указывает, что [винхттпреаддатаекс](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddataex) не должен завершать вызов до тех пор, пока предоставленный буфер данных не будет заполнен или не завершится ответ. Передача этого флага делает поведение **винхттпреаддатаекс** эквивалентным для [WinHttpReadData](/windows/win32/api/winhttp/nf-winhttp-winhttpreaddata).
</dd>

</dl>
