---
description: Описывает ошибки поставщика WMI SNMP с 1041 по 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Ошибки с 1041 по 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef466d1b1226b14d895fef81be24baee45354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080584"
---
# <a name="errors-1041-through-1050"></a>Ошибки с 1041 по 1050

Описывает ошибки поставщика WMI SNMP с 1041 по 1050.

[Неустранимая ошибка 1041](#fatal-error-1041)

[Неустранимая ошибка 1042](#fatal-error-1042)

[Предупреждение 1043](#warning-1043)

[Неустранимая ошибка 1044](#fatal-error-1044)

[Предупреждение 1045](#warning-1045)

[Предупреждение 1046](#warning-1046)

[Предупреждение 1047](#warning-1047)

[Предупреждение 1048](#warning-1048)

[Неустранимая ошибка 1049](#fatal-error-1049)

## <a name="fatal-error-1041"></a>Неустранимая ошибка 1041

<dl> <dt>

<span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в спецификации диапазона не разрешается в целочисленное значение"**
</dt> <dd>

Семантическая ошибка модуля в спецификации Range или size, характерная для не SNMPv2C. Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность. Любое значение, используемое при указании диапазона, должно быть целым числом.

</dd> </dl>

## <a name="fatal-error-1042"></a>Неустранимая ошибка 1042

<dl> <dt>

<span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Неустранимая>: " <fileName><line \#>: Верхняя граница спецификации диапазона меньше нижней границы"**
</dt> <dd>

Семантическая ошибка модуля в спецификации Range или size, характерная для не SNMPv2C. Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность. Нижняя граница спецификации диапазона или размера не должна превышать верхнюю границу.

</dd> </dl>

## <a name="warning-1043"></a>Предупреждение 1043

<dl> <dt>

<span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, предупреждение>: " <fileName> : <строка \#>: объект-Type с синтаксисом" Sequence ", должен иметь предложение доступа" недоступно "**
</dt> <dd>

**Тип объекта —** семантическое предупреждение модуля вызова макроса. Таблица или концептуальная строка (последовательность или типы объектов последовательности, соответственно) должны иметь значение "недоступно".

Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.

</dd> </dl>

## <a name="fatal-error-1044"></a>Неустранимая ошибка 1044

<dl> <dt>

<span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Неустранимая>: " <fileName><line \#>: переопределение символа <identifier> "**
</dt> <dd>

Семантическая ошибка модуля, характерная для неограниченного или SNMPv2C. Переопределение дескрипторов объектов, вызовов макросов и типов ASN. 1 приводит к ошибке.

</dd> </dl>

## <a name="warning-1045"></a>Предупреждение 1045

<dl> <dt>

<span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, предупреждение>: " <fileName><линереференце to Standard Symbol <symbolName> предполагается для определения, как в <moduleName> . Если вы хотите ссылаться на определение в текущем модуле, используйте нотации "Module. Symbol".**
</dt> <dd>

Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C. Символ, известный компилятору, был переопределен, и на него имеется ссылка. Компилятор предполагает стандартное определение символа. Таким образом, чтобы использовать переопределение стандартного символа, необходимо использовать нотацию Module. Symbol.

</dd> </dl>

## <a name="warning-1046"></a>Предупреждение 1046

<dl> <dt>

<span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, предупреждение>: " <fileName><строка \#>: не <symbol> определено. Предполагается стандартное определение "**
</dt> <dd>

Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C. Символ, известный компилятору, не должен быть переопределен или использоваться без импорта.

</dd> </dl>

## <a name="warning-1047"></a>Предупреждение 1047

<dl> <dt>

<span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, предупреждение>: " <fileName><строка \#>: определение типа <symbol> определено, но не указано в ссылке"**
</dt> <dd>

Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C. Все назначения значений и определения типов должны быть на месте.

</dd> </dl>

## <a name="warning-1048"></a>Предупреждение 1048

<dl> <dt>

<span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, предупреждение>: " <fileName><строка \#>: определение значения <symbol> определено, но не указано в ссылке"**
</dt> <dd>

Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C. Все назначения значений и определения типов должны быть на месте.

</dd> </dl>

## <a name="fatal-error-1049"></a>Неустранимая ошибка 1049

<dl> <dt>

<span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Неустранимая>: " <fileName> : <line \#>: предложение дефвал недопустимо для Object-Type с синтаксисом NetworkAddress"**
</dt> <dd>

**Объект-тип** вызова макроса с определенной семантикой модуля. Предложение ДЕФВАЛ недопустимо для типа OBJECT-TYPE, предложение СИНТАКСИСа которого разрешается в NetworkAddress.

</dd> </dl>

 

 



