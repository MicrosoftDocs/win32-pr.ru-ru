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
# <a name="errors-1081-through-1090"></a><span data-ttu-id="b77ff-103">Ошибки с 1081 по 1090</span><span class="sxs-lookup"><span data-stu-id="b77ff-103">Errors 1081 through 1090</span></span>

<span data-ttu-id="b77ff-104">Описывает ошибки поставщика WMI SNMP с 1081 по 1090.</span><span class="sxs-lookup"><span data-stu-id="b77ff-104">Describes WMI SNMP provider errors 1081 through 1090.</span></span>

[<span data-ttu-id="b77ff-105">Неустранимая ошибка 1081</span><span class="sxs-lookup"><span data-stu-id="b77ff-105">Fatal Error 1081</span></span>](#fatal-error-1081)

[<span data-ttu-id="b77ff-106">Неустранимая ошибка 1082</span><span class="sxs-lookup"><span data-stu-id="b77ff-106">Fatal Error 1082</span></span>](#fatal-error-1082)

[<span data-ttu-id="b77ff-107">Неустранимая ошибка 1084</span><span class="sxs-lookup"><span data-stu-id="b77ff-107">Fatal Error 1084</span></span>](#fatal-error-1084)

[<span data-ttu-id="b77ff-108">Предупреждение 1085</span><span class="sxs-lookup"><span data-stu-id="b77ff-108">Warning 1085</span></span>](#warning-1085)

[<span data-ttu-id="b77ff-109">Предупреждение 1086</span><span class="sxs-lookup"><span data-stu-id="b77ff-109">Warning 1086</span></span>](#warning-1086)

[<span data-ttu-id="b77ff-110">Неустранимая ошибка 1087</span><span class="sxs-lookup"><span data-stu-id="b77ff-110">Fatal Error 1087</span></span>](#fatal-error-1087)

[<span data-ttu-id="b77ff-111">Неустранимая ошибка 1089</span><span class="sxs-lookup"><span data-stu-id="b77ff-111">Fatal Error 1089</span></span>](#fatal-error-1089)

[<span data-ttu-id="b77ff-112">Неустранимая ошибка 1090</span><span class="sxs-lookup"><span data-stu-id="b77ff-112">Fatal Error 1090</span></span>](#fatal-error-1090)

## <a name="fatal-error-1081"></a><span data-ttu-id="b77ff-113">Неустранимая ошибка 1081</span><span class="sxs-lookup"><span data-stu-id="b77ff-113">Fatal Error 1081</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Неустранимая>: " <fileName> строка \#>: символ <identifier> отсутствует в импортированном модуле <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="b77ff-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Fatal>: "<fileName>line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-115">Семантическая ошибка модуля в перекрестных ссылках, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b77ff-115">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="b77ff-116">Символ, импортированный из модуля, не разрешается ни на что в этом модуле.</span><span class="sxs-lookup"><span data-stu-id="b77ff-116">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="b77ff-117">Если на самом деле ссылка на этот символ содержится в MIB, возникает эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="b77ff-117">If that symbol is actually referenced in the MIB, this error occurs.</span></span>

</dd> </dl>

## <a name="fatal-error-1082"></a><span data-ttu-id="b77ff-118">Неустранимая ошибка 1082</span><span class="sxs-lookup"><span data-stu-id="b77ff-118">Fatal Error 1082</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Неустранимая>: " <fileName> : <line \#>: Недопустимое предложение состояния <clause> "**</span><span class="sxs-lookup"><span data-stu-id="b77ff-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-120">Вызов макроса **удостоверения объекта** , ошибка семантического модуля SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="b77ff-120">**OBJECT-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="b77ff-121">Предложение STATUS вызова **удостоверения объекта** должно иметь значение "Current", "устарело" или "устарело".</span><span class="sxs-lookup"><span data-stu-id="b77ff-121">The STATUS clause of an **OBJECT-IDENTITY** invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1084"></a><span data-ttu-id="b77ff-122">Неустранимая ошибка 1084</span><span class="sxs-lookup"><span data-stu-id="b77ff-122">Fatal Error 1084</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Неустранимая>: "имя_файла><строка \#>: идентификатор модуля — требуется после раздела Imports для всех модулей SNMPv2"**</span><span class="sxs-lookup"><span data-stu-id="b77ff-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Fatal>: "fileName><line\#>: MODULE-IDENTITY required after the IMPORTS section for all SNMPv2 modules"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-124">Вызов макроса **удостоверения модуля** , ошибка семантического модуля SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="b77ff-124">**MODULE-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="b77ff-125">В базе MIB SNMPv2C должен быть один и только один вызов **удостоверения модуля** сразу после раздела Imports.</span><span class="sxs-lookup"><span data-stu-id="b77ff-125">There must be one and only one **MODULE-IDENTITY** invocation in an SNMPv2C MIB, immediately after the IMPORTS section.</span></span>

</dd> </dl>

## <a name="warning-1085"></a><span data-ttu-id="b77ff-126">Предупреждение 1085</span><span class="sxs-lookup"><span data-stu-id="b77ff-126">Warning 1085</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, предупреждение>: " <fileName><строка \#>: в модуле не найдены группы <name> . Не удалось выполнить ИДЕНТИФИКАЦИю модуля. Попытка загрузить модуль в Смир завершится ошибкой "**</span><span class="sxs-lookup"><span data-stu-id="b77ff-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Warning>: "<fileName><line\#>: No groups found in module <name>. Could not fabricate MODULE-IDENTITY. Attempt to load the module into the SMIR will fail"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-128">Предупреждение о семантической семантике модуля (в особенности).</span><span class="sxs-lookup"><span data-stu-id="b77ff-128">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="b77ff-129">Эта ошибка возникает, если в модуле не найдены группы объектов.</span><span class="sxs-lookup"><span data-stu-id="b77ff-129">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="warning-1086"></a><span data-ttu-id="b77ff-130">Предупреждение 1086</span><span class="sxs-lookup"><span data-stu-id="b77ff-130">Warning 1086</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, предупреждение>: " <fileName><строка \#>: группы не найдены в модуле <name> "**</span><span class="sxs-lookup"><span data-stu-id="b77ff-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Warning>: "<fileName><line\#>: No groups found in module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-132">Предупреждение о семантической семантике модуля (в особенности).</span><span class="sxs-lookup"><span data-stu-id="b77ff-132">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="b77ff-133">Эта ошибка возникает, если в модуле не найдены группы объектов.</span><span class="sxs-lookup"><span data-stu-id="b77ff-133">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="fatal-error-1087"></a><span data-ttu-id="b77ff-134">Неустранимая ошибка 1087</span><span class="sxs-lookup"><span data-stu-id="b77ff-134">Fatal Error 1087</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Неустранимая>: " <fileName><line \#>: Недопустимое предложение состояния <clause> для макроса текстового соглашения"**</span><span class="sxs-lookup"><span data-stu-id="b77ff-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Fatal>: "<fileName><line\#>: Invalid STATUS clause <clause> for a TEXTUAL-CONVENTION macro"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-136">Назначение типа, ошибка семантического модуля SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="b77ff-136">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="b77ff-137">Предложение Status для вызова макроса **ТЕКСТОВОГО соглашения** должно иметь значение "Current", "устарело" или "устарело".</span><span class="sxs-lookup"><span data-stu-id="b77ff-137">The status clause of a **TEXTUAL-CONVENTION** macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1089"></a><span data-ttu-id="b77ff-138">Неустранимая ошибка 1089</span><span class="sxs-lookup"><span data-stu-id="b77ff-138">Fatal Error 1089</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Неустранимая>: " <fileName> : <строка \#>: символ <identifier> в предложении дополнения не разрешается в объект Row-Type"**</span><span class="sxs-lookup"><span data-stu-id="b77ff-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Fatal>: "<fileName>:<line\#>: Symbol <identifier> in AUGMENTS clause does not resolve to a row OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-140">**Объект — тип объекта** вызова макроса SNMPv2c — особая семантическая ошибка модуля.</span><span class="sxs-lookup"><span data-stu-id="b77ff-140">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="b77ff-141">Если имеется предложение дополнения, идентификатор в предложении дополнения должен разрешаться в объект TABLE-TYPE.</span><span class="sxs-lookup"><span data-stu-id="b77ff-141">If an AUGMENTS clause is present, then the identifier in the AUGMENTS clause must resolve to a table OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1090"></a><span data-ttu-id="b77ff-142">Неустранимая ошибка 1090</span><span class="sxs-lookup"><span data-stu-id="b77ff-142">Fatal Error 1090</span></span>

<dl> <dt>

<span data-ttu-id="b77ff-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Неустранимая>: " <fileName> : <строка \#> подразумеваемое предложение используется только для последнего объекта индекса"**</span><span class="sxs-lookup"><span data-stu-id="b77ff-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Fatal>: "<fileName>:<line\#> IMPLIED clause is useful only for the last INDEX object"**</span></span>
</dt> <dd>

<span data-ttu-id="b77ff-144">**Объект — тип объекта** вызова макроса SNMPv2c — особая семантическая ошибка модуля.</span><span class="sxs-lookup"><span data-stu-id="b77ff-144">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="b77ff-145">Предложение ПОДРАЗУМЕВАЕМых может быть связано только с последним объектом в предложении INDEX.</span><span class="sxs-lookup"><span data-stu-id="b77ff-145">The IMPLIED clause can be associated only with the last object in the INDEX clause.</span></span>

</dd> </dl>

 

 



