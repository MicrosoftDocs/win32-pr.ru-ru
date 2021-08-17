---
description: Описывает ошибки поставщика WMI SNMP с 1011 по 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Ошибки с 1011 по 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960c646e600f57a9ce98230b12a89424ec9c61dc94c4fdc5360fb6ceaeda24d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374504"
---
# <a name="errors-1011-through-1020"></a>Ошибки с 1011 по 1020

Описывает ошибки поставщика WMI SNMP с 1011 по 1020.

[Неустранимая ошибка 1011](#fatal-error-1011)

[Неустранимая ошибка 1012](#fatal-error-1012)

[Неустранимая ошибка 1013](#fatal-error-1013)

[Предупреждение 1014](#warning-1014)

[Неустранимая ошибка 1015](#fatal-error-1015)

[Неустранимая ошибка 1016](#fatal-error-1016)

[Неустранимая ошибка 1018](#fatal-error-1018)

[Неустранимая ошибка 1020](#fatal-error-1020)

## <a name="fatal-error-1011"></a>Неустранимая ошибка 1011

<dl> <dt>

<span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Неустранимая>: " <fileName> : <строка \#> синтаксис члена <identifier> последовательности, <identifier> ,, отличается от конструкции синтаксиса объекта типа"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Элемент последовательности должен совпадать с типом в предложении СИНТАКСИСа определения типа объекта. Параметр <Line \#> является строкой предложения синтаксиса определения типа объекта.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1012"></a>Неустранимая ошибка 1012

<dl> <dt>

<span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Неустранимая>: " <fileName> : <строка \#> предложение индекса или дополнения является обязательным только для объектов Sequence-Types"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Предложение INDEX должно присутствовать только в определении типа объекта, синтаксис которого разрешается в тип последовательности.

Эта ошибка может возникать при компиляции MIB или SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1013"></a>Неустранимая ошибка 1013

<dl> <dt>

<span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Неустранимая>: " <fileName><строка \#>: <identifier> следует разрешить в тип последовательности"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Тип, используемый в конструкции "последовательность", должен разрешаться в тип последовательности.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="warning-1014"></a>Предупреждение 1014

<dl> <dt>

<span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, предупреждение>: " <fileName> : <line \#>: нерекомендуемый идентификатор значения 0 в OID"**
</dt> <dd>

**Тип объекта —** семантическое предупреждение модуля вызова макроса. Не рекомендуется, чтобы ни один объект в стандартной MIB в Интернете не использовал в ИДЕНТИФИКАТОРе объекта подидентификатор 0.

Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1015"></a>Неустранимая ошибка 1015

<dl> <dt>

<span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Неустранимая>: " <fileName> : <line \#>: OBJECT-TYPEs <identifier> из модуля <identifier> и <identifier> из модуля <identifier> назначены одинаковые значения OID"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Двум вызовам **типа объекта** (в одном или разных модулях) не должно быть присвоено одинаковое значение идентификатора объекта.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1016"></a>Неустранимая ошибка 1016

<dl> <dt>

<span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Неустранимая>: " <fileName> : <line \#>: значение в предложении дефвал не соответствует типу в ПРЕДЛОЖЕНии синтаксиса"**
</dt> <dd>

Семантическая ошибка модуля вызова макроса **типа объекта** . Значение в предложении ДЕФВАЛ должно быть значением типа, упомянутого в предложении СИНТАКСИСа.

Эта ошибка может возникать в SNMPv2C или с.

</dd> </dl>

## <a name="fatal-error-1018"></a>Неустранимая ошибка 1018

<dl> <dt>

<span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Неустранимая>: " <fileName><line \#>: <symbol> в предложении Enterprise для типа ловушки не разрешается в значение OID"**
</dt> <dd>

Вызов макроса **типа ловушки** , ошибка семантического модуля для конкретной ошибки. Символ, используемый в предложении ENTERPRISE для вызова макроса **типа ловушки** , должен разрешаться в значение идентификатора объекта.

</dd> </dl>

## <a name="fatal-error-1020"></a>Неустранимая ошибка 1020

<dl> <dt>

<span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Неустранимая>: " <fileName><line \#>: значение, назначенное типу ловушки, <identifier> не разрешено в положительное целое число"**
</dt> <dd>

Вызов макроса **типа ловушки** , ошибка семантического модуля для конкретной ошибки. Символ, используемый при указании значения ловушки, не разрешается в положительное целое число.

</dd> </dl>

 

 



