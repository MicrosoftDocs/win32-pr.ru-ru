---
description: Описывает ошибки поставщика WMI SNMP с 1021 по 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Ошибки с 1021 по 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662783"
---
# <a name="errors-1021-through-1030"></a>Ошибки с 1021 по 1030

Описывает ошибки поставщика WMI SNMP с 1021 по 1033.

[Неустранимая ошибка 1021](#fatal-error-1021)

[Неустранимая ошибка 1022](#fatal-error-1022)

[Неустранимая ошибка 1023](#fatal-error-1023)

[Неустранимая ошибка 1024](#fatal-error-1024)

[Неустранимая ошибка 1025](#fatal-error-1025)

[Неустранимая ошибка 1026](#fatal-error-1026)

[Предупреждение 1027](#warning-1027)

[Неустранимая ошибка 1028](#fatal-error-1028)

[Неустранимая ошибка 1029](#fatal-error-1029)

[Неустранимая ошибка 1030](#fatal-error-1030)

## <a name="fatal-error-1021"></a>Неустранимая ошибка 1021

<dl> <dt>

<span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в предложении VARIABLEs типа ловушки не разрешается в скалярный тип объекта"**
</dt> <dd>

Вызов макроса **типа ловушки** , ошибка семантического модуля для конкретной ошибки. Каждый элемент в списке переменных, используемых в предложении VARIABLEs для вызова макроса **типа ловушки** , должен разрешаться в имя скалярного экземпляра типа объекта.

</dd> </dl>

## <a name="fatal-error-1022"></a>Неустранимая ошибка 1022

<dl> <dt>

<span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Неустранимая>: " <fileName><строка \#>: значение не разрешено к типу <type> "**
</dt> <dd>

Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C. Неверное значение для значения **RHS, равного значению, строке** октета или присваивания значения идентификатору объекта.

</dd> </dl>

## <a name="fatal-error-1023"></a>Неустранимая ошибка 1023

<dl> <dt>

<span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Неустранимая>: " <fileName><строка \#>: идентификатор <identifier> не разрешается в тип <identifier> "**
</dt> <dd>

Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C. Символ (ссылка на значение) для параметра RHS ЦЕЛОго числа, **null**, строки октета или присваивания значения идентификатора объекта не разрешается в правильный тип.

</dd> </dl>

## <a name="fatal-error-1024"></a>Неустранимая ошибка 1024

<dl> <dt>

<span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Неустранимая>: " <fileName><строка \#>: отрицательное целое число в определении значения OID"**
</dt> <dd>

Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C. Все значения в списке компонентов OID должны быть неотрицательными (желательно положительными) целыми числами.

</dd> </dl>

## <a name="fatal-error-1025"></a>Неустранимая ошибка 1025

<dl> <dt>

<span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Неустранимая>: "идентификатор <identifier> в значении OID не разрешается в положительное целое"**
</dt> <dd>

Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C. Все значения в списке компонентов OID должны быть неотрицательными (желательно положительными) целыми числами.

</dd> </dl>

## <a name="fatal-error-1026"></a>Неустранимая ошибка 1026

<dl> <dt>

<span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в значении OID не разрешается в значение OID или положительное целое"**
</dt> <dd>

Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C. Первый компонент, используемый в значении OID, должен разрешаться в значение OID или ЦЕЛОе число.

</dd> </dl>

## <a name="warning-1027"></a>Предупреждение 1027

<dl> <dt>

<span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, предупреждение>: " <fileName><строка \#>: импортированный символ не <identifier> используется"**
</dt> <dd>

ИМПОРТИРУЕТ семантическое предупреждение для модуля раздела, характерное для не SNMPv2C. Для каждого неиспользуемого импортированного символа выдается предупреждение.

</dd> </dl>

## <a name="fatal-error-1028"></a>Неустранимая ошибка 1028

<dl> <dt>

<span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Неустранимая>: "модуль <identifier> не импортирован в раздел Imports"**
</dt> <dd>

Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C. Имя модуля, используемое для ссылки на символ, должно либо присутствовать в предложении IMPORTs, либо быть именем текущего модуля.

</dd> </dl>

## <a name="fatal-error-1029"></a>Неустранимая ошибка 1029

<dl> <dt>

<span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Неустранимая>: " <fileName><строка \#>: текущий модуль <identifier> не может быть импортирован"**
</dt> <dd>

Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C. Имя текущего модуля также имеет значение в списке ИМПОРТов.

</dd> </dl>

## <a name="fatal-error-1030"></a>Неустранимая ошибка 1030

<dl> <dt>

<span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Неустранимая>: " <fileName><строка \#>: символ <identifier> не импортирован из модуля <identifier> "**
</dt> <dd>

Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C. Вы использовали нотацию "Module. Symbol", но символ не был импортирован из указанного модуля в разделе IMPORTs.

</dd> </dl>

 

 



