---
description: Описывает ошибки поставщика WMI SNMP с 1091 по 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Ошибки с 1091 по 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf582a3df41fbc7c329f5a993555a2d76145ded0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713108"
---
# <a name="errors-1091-through-1100"></a>Ошибки с 1091 по 1100

Описывает ошибки поставщика WMI SNMP с 1091 по 1100.

[Предупреждение 1091](#warning-1091)

[Неустранимая ошибка 1092](#fatal-error-1092)

[Неустранимая ошибка 1093](#fatal-error-1093)

[Неустранимая ошибка 1094](#fatal-error-1094)

[Неустранимая ошибка 1095](#fatal-error-1095)

[Неустранимая ошибка 1097](#fatal-error-1097)

[Неустранимая ошибка 1098](#fatal-error-1098)

[Неустранимая ошибка 1099](#fatal-error-1099)

## <a name="warning-1091"></a>Предупреждение 1091

<dl> <dt>

<span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, предупреждение>: " <fileName> : <строка \#> подразумеваемое предложение не допускается для объектов фиксированного размера"**
</dt> <dd>

**Объект — тип объекта** вызова макроса SNMPv2c — заданное предупреждение семантики модуля. Ключевое слово ПОДРАЗУМЕВАЕМое может присутствовать только для объекта с синтаксисом переменной длины, например ИДЕНТИФИКАТОРом объекта или СТРОКой ОКТЕТа переменной длины в предложении INDEX.

</dd> </dl>

## <a name="fatal-error-1092"></a>Неустранимая ошибка 1092

<dl> <dt>

<span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Неустранимая>: " <fileName> : <line \#> предложение подразумеваемого недопустимо для объектов, которые могут иметь нулевую длину"**
</dt> <dd>

**Объект — тип объекта** вызова макроса SNMPv2c — особая семантическая ошибка модуля. Предложение ПОДРАЗУМЕВАЕМого нельзя использовать для объекта переменной длины, если этот объект может иметь нулевую длину.

</dd> </dl>

## <a name="fatal-error-1093"></a>Неустранимая ошибка 1093

<dl> <dt>

<span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Неустранимая>: " <fileName><line \#>: в соответствии с SMI v1 можно перечислять только тип" integer "**
</dt> <dd>

Назначение типа, ошибка семантического модуля для конкретной задачи. Перечисление с неизвестной MIB может использовать только тип INTEGER.

</dd> </dl>

## <a name="fatal-error-1094"></a>Неустранимая ошибка 1094

<dl> <dt>

<span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Неустранимая>: " <fileName><line \#>: тип, используемый в перечислении, не разрешается в один из разрешенных типов"**
</dt> <dd>

Назначение типа, ошибка семантического модуля SNMPv2C. Тип, используемый в перечислении, должен быть ЦЕЛОЧИСЛЕНным или эквивалентным типом или другим перечислением.

</dd> </dl>

## <a name="fatal-error-1095"></a>Неустранимая ошибка 1095

<dl> <dt>

<span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Неустранимая>: " <fileName><line \#>: член перечисления не является членом родительского перечисления"**
</dt> <dd>

Назначение типа, ошибка семантического модуля SNMPv2C. Если используется другое перечисление, его набор элементов должен быть подмножеством набора элементов родительского перечисления.

</dd> </dl>

## <a name="fatal-error-1097"></a>Неустранимая ошибка 1097

<dl> <dt>

<span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Неустранимая>: " <fileName><line \#>: идентификатор <name> не разрешается в целочисленное значение"**
</dt> <dd>

Назначение типа, ошибка семантического модуля SNMPv2C. Значения в типе BITS должны быть целочисленными значениями.

</dd> </dl>

## <a name="fatal-error-1098"></a>Неустранимая ошибка 1098

<dl> <dt>

<span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Неустранимая>: " <fileName><строка \#>: повторяющееся значение <value> в конструкции BITS"**
</dt> <dd>

Назначение типа, ошибка семантического модуля SNMPv2C. В конструкции BITS не должно быть повторяющихся имен и значений. Параметр <Line \#> — это расположение повторения имени и значения.

</dd> </dl>

## <a name="fatal-error-1099"></a>Неустранимая ошибка 1099

<dl> <dt>

<span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Неустранимая>: " <fileName><строка \#>: повторяющееся имя <identifier> в конструкции BITS"**
</dt> <dd>

Назначение типа, ошибка семантического модуля SNMPv2C. В конструкции BITS не должно быть повторяющихся имен и значений. Параметр <Line \#> — это расположение повторения имени и значения.

</dd> </dl>

 

 



