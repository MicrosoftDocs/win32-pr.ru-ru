---
description: Описывает ошибки поставщика WMI SNMP с 1081 по 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Ошибки с 1081 по 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a80399ef61bce644813447559a76bf9710873be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683220"
---
# <a name="errors-1081-through-1090"></a>Ошибки с 1081 по 1090

Описывает ошибки поставщика WMI SNMP с 1081 по 1090.

[Неустранимая ошибка 1081](#fatal-error-1081)

[Неустранимая ошибка 1082](#fatal-error-1082)

[Неустранимая ошибка 1084](#fatal-error-1084)

[Предупреждение 1085](#warning-1085)

[Предупреждение 1086](#warning-1086)

[Неустранимая ошибка 1087](#fatal-error-1087)

[Неустранимая ошибка 1089](#fatal-error-1089)

[Неустранимая ошибка 1090](#fatal-error-1090)

## <a name="fatal-error-1081"></a>Неустранимая ошибка 1081

<dl> <dt>

<span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Неустранимая>: " <fileName> строка \#>: символ <identifier> отсутствует в импортированном модуле <identifier> "**
</dt> <dd>

Семантическая ошибка модуля в перекрестных ссылках, характерная для неограниченного или SNMPv2C. Символ, импортированный из модуля, не разрешается ни на что в этом модуле. Если на самом деле ссылка на этот символ содержится в MIB, возникает эта ошибка.

</dd> </dl>

## <a name="fatal-error-1082"></a>Неустранимая ошибка 1082

<dl> <dt>

<span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Неустранимая>: " <fileName> : <line \#>: Недопустимое предложение состояния <clause> "**
</dt> <dd>

Вызов макроса **удостоверения объекта** , ошибка семантического модуля SNMPv2c. Предложение STATUS вызова **удостоверения объекта** должно иметь значение "Current", "устарело" или "устарело".

</dd> </dl>

## <a name="fatal-error-1084"></a>Неустранимая ошибка 1084

<dl> <dt>

<span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Неустранимая>: "имя_файла><строка \#>: идентификатор модуля — требуется после раздела Imports для всех модулей SNMPv2"**
</dt> <dd>

Вызов макроса **удостоверения модуля** , ошибка семантического модуля SNMPv2c. В базе MIB SNMPv2C должен быть один и только один вызов **удостоверения модуля** сразу после раздела Imports.

</dd> </dl>

## <a name="warning-1085"></a>Предупреждение 1085

<dl> <dt>

<span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, предупреждение>: " <fileName><строка \#>: в модуле не найдены группы <name> . Не удалось выполнить ИДЕНТИФИКАЦИю модуля. Попытка загрузить модуль в Смир завершится ошибкой "**
</dt> <dd>

Предупреждение о семантической семантике модуля (в особенности). Эта ошибка возникает, если в модуле не найдены группы объектов.

</dd> </dl>

## <a name="warning-1086"></a>Предупреждение 1086

<dl> <dt>

<span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, предупреждение>: " <fileName><строка \#>: группы не найдены в модуле <name> "**
</dt> <dd>

Предупреждение о семантической семантике модуля (в особенности). Эта ошибка возникает, если в модуле не найдены группы объектов.

</dd> </dl>

## <a name="fatal-error-1087"></a>Неустранимая ошибка 1087

<dl> <dt>

<span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Неустранимая>: " <fileName><line \#>: Недопустимое предложение состояния <clause> для макроса текстового соглашения"**
</dt> <dd>

Назначение типа, ошибка семантического модуля SNMPv2C. Предложение Status для вызова макроса **ТЕКСТОВОГО соглашения** должно иметь значение "Current", "устарело" или "устарело".

</dd> </dl>

## <a name="fatal-error-1089"></a>Неустранимая ошибка 1089

<dl> <dt>

<span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Неустранимая>: " <fileName> : <строка \#>: символ <identifier> в предложении дополнения не разрешается в объект Row-Type"**
</dt> <dd>

**Объект — тип объекта** вызова макроса SNMPv2c — особая семантическая ошибка модуля. Если имеется предложение дополнения, идентификатор в предложении дополнения должен разрешаться в объект TABLE-TYPE.

</dd> </dl>

## <a name="fatal-error-1090"></a>Неустранимая ошибка 1090

<dl> <dt>

<span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Неустранимая>: " <fileName> : <строка \#> подразумеваемое предложение используется только для последнего объекта индекса"**
</dt> <dd>

**Объект — тип объекта** вызова макроса SNMPv2c — особая семантическая ошибка модуля. Предложение ПОДРАЗУМЕВАЕМых может быть связано только с последним объектом в предложении INDEX.

</dd> </dl>

 

 



