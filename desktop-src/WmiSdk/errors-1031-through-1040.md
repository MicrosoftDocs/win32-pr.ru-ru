---
description: Описывает ошибки поставщика WMI SNMP с 1031 по 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Ошибки с 1031 по 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5986ba80a55d2d8f3d4a87b0587331765aa38d67
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886881"
---
# <a name="errors-1031-through-1040"></a>Ошибки с 1031 по 1040

Описывает ошибки поставщика WMI SNMP с 1031 по 1040.

[Предупреждение 1031](#warning-1031)

[Неустранимая ошибка 1032](#fatal-error-1032)

[Неустранимая ошибка 1033](#fatal-error-1033)

[Предупреждение 1034](#warning-1034)

[Предупреждение 1036](#warning-1036)

[Неустранимая ошибка 1037](#fatal-error-1037)

[Неустранимая ошибка 1038](#fatal-error-1038)

[Неустранимая ошибка 1039](#fatal-error-1039)

[Неустранимая ошибка 1040](#fatal-error-1040)

## <a name="warning-1031"></a>Предупреждение 1031

<dl> <dt>

<span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, предупреждение>: " &lt; имя_файла &gt; : <Line \#>: Идентификатор стандартного &lt; символа &gt; должен быть импортирован из &lt; идентификатора модуля &gt; . Предполагается стандартное определение ".**
</dt> <dd>

ИМПОРТИРУЕТ семантическое предупреждение для модуля раздела, характерное для не SNMPv2C. Если идентификатор SNMP, известный компилятору, находится в разделе IMPORTs, то модуль, из которого он импортируется, должен быть одним из стандартных модулей.

Некоторые часто используемые ИМПОРТы — "предполагаемый набор знаний" в части компилятора. Компилятору не нужно требовать доступ к другим информационным модулям для их устранения.

Встроенные ИМПОРТы в стандартных и SNMPv2C описаны в следующих таблицах.

</dd> </dl>

**Встроенные операции импорта в энергоязыке**



| Класс импорта | Модуль      | Экземпляры                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| Значение ASN. 1  | RFC1155 — SMI | Интернет, каталог, управление, экспериментальный, частный, предприятия |
|              | RFC1213-MIB | MIB-II и IP-адрес, интерфейсы, передача                             |
| ASN. 1 тип   | RFC1155 — SMI | NetworkAddress, IpAddress, Counter, датчик, значение TIMETICKS, непрозрачный        |
|              | RFC1213-MIB | DisplayString, Фисаддресс                                          |
| Сомакрос ASN. 1  | RFC — 1212    | OBJECT-TYPE                                                         |
|              | RFC — 1215    | ТИП ЛОВУШКИ                                                           |



 

**Встроенные ИМПОРТы SNMPv2C**



| Класс импорта       | Модуль      | Экземпляры                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Значение ASN. 1        | SNMPv2 — SMI  | org, DoD, Интернет, каталог, руководства, MIB-2, передача, экспериментальные, частные, предприятия, безопасность, SNMPv2, Снмпдомаинс, Снмппроксис, Снмпмодулес                                                           |
|                    | SNMPv2-TM   | rfc1157Proxy                                                                                                                                                                                                   |
| Идентификация объектов    | SNMPv2 — SMI  | зеродотзеро                                                                                                                                                                                                    |
|                    | SNMPv2-TM   | Снмпудпдомаин, Снмпклнсдомаин, Смнпконсдомаин, Снмпддпдомаин, Снмпипксдомаин, rfc1157Domain                                                                                                                     |
| ASN. 1 тип         | SNMPv2 — SMI  | Integer32, IpAddress, Counter32, значение TIMETICKS, непрозрачный, Counter64, Unsigned32, значение Gauge32                                                                                                                             |
| Сомакрос ASN. 1        | SNMPv2 — SMI  | ИДЕНТИФИКАТОР МОДУЛЯ, ОБЪЕКТНО-УДОСТОВЕРЕНИЕ, ОБЪЕКТ-ТИП, ТИП УВЕДОМЛЕНИЯ                                                                                                                                               |
|                    | SNMPv2-CONF | ОБЪЕКТ-ГРУППА, УВЕДОМЛЕНИЕ-ГРУППА, МОДУЛЬ-СООТВЕТСТВИЕ, ВОЗМОЖНОСТИ АГЕНТА                                                                                                                                        |
|                    | SNMPv2-TC   | ТЕКСТОВОЕ СОГЛАШЕНИЕ                                                                                                                                                                                             |
| Текстовое соглашение | SNMPv2-TC   | DisplayString, Фисаддресс, MacAddress, Трусвалуе, Тестандинкр, Аутономаустипе, Инстанцепоинтер, Вариаблепоинтер, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress |
|                    | SNMPv2-TM   | Снмпудпаддресс, Снмпосиаддресс, Снмпнбпаддресс, Снмпипксаддресс                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a>Неустранимая ошибка 1032

<dl> <dt>

<span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Неустранимая>: " &lt; имя_файла &gt;<строка \#>: повторяющееся значение &lt; &gt; в перечислении"**
</dt> <dd>

Семантическая ошибка модуля в перечислении, относящаяся к неограниченному или SNMPv2C. Дублирующихся значений не должно быть. Параметр <Line \#> — это расположение повторения имени и значения.

</dd> </dl>

## <a name="fatal-error-1033"></a>Неустранимая ошибка 1033

<dl> <dt>

<span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Неустранимая>: " &lt; имя_файла &gt;<строка \#>: &lt; идентификатор повторяющегося имени &gt; в перечислении"**
</dt> <dd>

Семантическая ошибка модуля в перечислении, относящаяся к неограниченному или SNMPv2C. Дублирующихся имен не должно быть. Параметр <Line \#> — это расположение повторения имени и значения.

</dd> </dl>

## <a name="warning-1034"></a>Предупреждение 1034

<dl> <dt>

<span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, предупреждение>: " &lt; имя_файла &gt;<строка \#>: значение 0, запрещенное в перечислении"**
</dt> <dd>

Семантическое предупреждение модуля в перечислении, характерное для неограниченного или SNMPv2C. Рекомендуется, чтобы именованное значение нуль не применялось в перечислении.

</dd> </dl>

## <a name="warning-1036"></a>Предупреждение 1036

<dl> <dt>

<span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, предупреждение> " &lt; имя_файла &gt;<строка \#>: значение в перечислении не разрешается в положительное целое"**
</dt> <dd>

Семантическое предупреждение модуля в перечислении, характерное для неограниченного или SNMPv2C. Отрицательное значение недопустимо в перечислении.

</dd> </dl>

## <a name="fatal-error-1037"></a>Неустранимая ошибка 1037

<dl> <dt>

<span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Неустранимая>: " &lt; имя_файла &gt;<строка \#>: &lt; идентификатор идентификатора &gt; не РАЗрешается в строку октета или непрозрачные типы"**
</dt> <dd>

Семантическая ошибка модуля в спецификации размера, характерная для не SNMPv2C. Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность.

</dd> </dl>

## <a name="fatal-error-1038"></a>Неустранимая ошибка 1038

<dl> <dt>

<span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Неустранимая>: " &lt; имя_файла &gt;<строка \#>: идентификатор идентификатора не &lt; &gt; разрешает тип целого числа или датчика"**
</dt> <dd>

Семантическая ошибка модуля в спецификации диапазона. Эта ошибка может возникать в SNMPv2C или с.

В стандарте, символ, используемый в спецификации диапазона, должен разрешаться в ЦЕЛОе число или датчик.

В SNMPv2C символ, используемый в спецификации диапазона, должен разрешаться в целые числа, значение Gauge32, integer32 или Unsigned32.

</dd> </dl>

## <a name="fatal-error-1039"></a>Неустранимая ошибка 1039

<dl> <dt>

<span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Неустранимая>: &lt; fileName &gt;<строка \#>: отрицательное значение используется в спецификации размера "**
</dt> <dd>

Семантическая ошибка модуля в спецификации размера, характерная для не SNMPv2C. Любое значение, используемое при указании размера, не должно быть отрицательным.

</dd> </dl>

## <a name="fatal-error-1040"></a>Неустранимая ошибка 1040

<dl> <dt>

<span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Неустранимая>: " &lt; имя_файла &gt;<строка \#>: &lt; идентификатор идентификатора &gt; в спецификации размера не разрешается в неотрицательное целочисленное значение"**
</dt> <dd>

Семантическая ошибка модуля в спецификации Range или size, характерная для не SNMPv2C. Любой символ, используемый при указании значения в спецификации размера, разрешается в неотрицательное значение.

</dd> </dl>

 

 



