---
description: Описывает ошибки поставщика WMI SNMP с 1001 по 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Ошибки с 1001 по 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712111"
---
# <a name="errors-1001-through-1010"></a>Ошибки с 1001 по 1010

Описывает ошибки поставщика WMI SNMP с 1001 по 1010.

[Неустранимая ошибка 1001](#fatal-error-1001)

[Неустранимая ошибка 1002](#fatal-error-1002)

[Неустранимая ошибка 1003](#fatal-error-1003)

[Предупреждение 1004](#warning-1004)

[Предупреждение 1005](#warning-1005)

[Неустранимая ошибка 1006](#fatal-error-1006)

[Неустранимая ошибка 1008](#fatal-error-1008)

## <a name="fatal-error-1001"></a>Неустранимая ошибка 1001

<dl> <dt>

<span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Неустранимая>: " <fileName> : <line \#>: предложение синтаксиса типа Object-Type не разрешается в допустимые типы"
</dt> <dd>

Семантическая ошибка модуля вызова макроса типа объекта. Предложение СИНТАКСИСа макроса типа OBJECT-TYPE должно разрешаться в тип или подтип, сформированный с помощью спецификации SIZE или Range, которую разрешает SMI или SNMPv2C. Если это не так, то сообщается о неустранимой ошибке 1001.

Эта ошибка может возникать при компиляции MIB или SNMPv2C.

К типам, которые допускаются SMI, используют следующие типы:

-   INTEGER
-   NULL
-   СТРОКА ОКТЕТА
-   ИДЕНТИФИКАТОР ОБЪЕКТА
-   NetworkAddress
-   IPAddress
-   Счетчик
-   Датчик
-   Значение TIMETICKS
-   Непрозрачный
-   DisplayString
-   фисаддресс

Типы, разрешенные SMI SNMPv2C:

-   INTEGER
-   СТРОКА ОКТЕТА
-   ИДЕНТИФИКАТОР ОБЪЕКТА
-   BITS
-   Integer32
-   IPAddress
-   Counter32
-   Значение TIMETICKS
-   Непрозрачный
-   Counter64
-   Unsigned32
-   DisplayString
-   фисаддресс
-   MacAddress
-   трусвалуе
-   тестандинкр
-   аутономаустипе
-   инстанцепоинтер
-   вариаблепоинтер
-   ровпоинтер
-   ровстатус
-   TimeStamp
-   TimeInterval
-   DateAndTime
-   StorageType
-   тдомаин
-   таддресс

</dd> </dl>

## <a name="fatal-error-1002"></a>Неустранимая ошибка 1002

<dl> <dt>

<span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Неустранимая>: " <fileName> : <line \#>: Недопустимое предложение доступа <clause> "
</dt> <dd>

Семантическая ошибка модуля вызова макроса типа объекта. В версии в версии с параметром "макрос" должен быть предложен доступ только для чтения, "только запись", "чтение/запись" или "недоступно".

Для SNMPv2C предложение MAX-ACCESS должно иметь значение "только для чтения", "чтение-создать", "чтение/запись" или "недоступно".

</dd> </dl>

## <a name="fatal-error-1003"></a>Неустранимая ошибка 1003

<dl> <dt>

<span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Неустранимая>: " <fileName> : <line \#>: Недопустимое предложение состояния <clause> "
</dt> <dd>

Семантическая ошибка модуля вызова макроса типа объекта. В версии с параметром STATUS в качестве условия вызова макроса типа OBJECT должен быть "обязательный", "необязательный", "устаревший" или "устаревший".

Для SNMPv2C предложение STATUS вызова макроса типа OBJECT должно быть "Current", "устарело" или "устарело".

</dd> </dl>

## <a name="warning-1004"></a>Предупреждение 1004

<dl> <dt>

<span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> : <line \#>: Object-Type <identifier> , синтаксис которого разрешается в один из типов счетчиков, не заканчивается буквой" "
</dt> <dd>

Тип объекта — семантическое предупреждение модуля вызова макроса. Идентификатор объекта счетчика СИНТАКСИСа (в версии/с) или Counter32 и Counter64 (SNMPv2C) должен быть во множественном числе.

Это предупреждение может возникать при компиляции MIB либо SNMPv2C.

</dd> </dl>

## <a name="warning-1005"></a>Предупреждение 1005

<dl> <dt>

<span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, предупреждение>: " <fileName> : <строка \#>: объект-Type с синтаксисом" Sequence ", должен иметь предложение доступа" недоступно "
</dt> <dd>

Тип объекта — семантическое предупреждение модуля вызова макроса. Таблица или концептуальная строка (последовательность или типы объектов последовательности, соответственно) должны иметь значение "недоступно".

Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1006"></a>Неустранимая ошибка 1006

<dl> <dt>

<span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Неустранимая>: " <fileName> : <строка \#> объектный тип <identifier> , который имеет синтаксическую последовательность, не имеет предложения index или дополнения"
</dt> <dd>

Семантическая ошибка модуля вызова макроса типа объекта. В настоящее время для определения типа объекта должно присутствовать предложение INDEX, синтаксис которого разрешается в тип последовательности.

Для SNMPv2C для объявления концептуальной строки должен присутствовать либо индекс, либо предложение дополнения.

</dd> </dl>

## <a name="fatal-error-1008"></a>Неустранимая ошибка 1008

<dl> <dt>

<span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Неустранимая>: " <fileName> : <line \#>: объект-Type <identifier> , который имеет синтаксис" Sequence ", не был указан"
</dt> <dd>

Семантическая ошибка модуля вызова макроса типа объекта. ОБЪЕКТный тип с предложением СИНТАКСИСа в качестве типа последовательности должен быть представлен в предложении СИНТАКСИСа только одного вызова типа объекта, который означает объявление таблицы, то есть объект с предложением СИНТАКСИСа в виде последовательности типа. Параметр <Line \#> ссылается на вторую точку ссылки.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

 

 



