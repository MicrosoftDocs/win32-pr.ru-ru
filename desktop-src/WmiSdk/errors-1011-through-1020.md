---
description: Описывает ошибки поставщика WMI SNMP с 1011 по 1020.
ms.assetid: 5151a110-1532-48cc-832a-2cee21853b6b
ms.tgt_platform: multiple
title: Ошибки с 1011 по 1020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a73f90ce0fc161604d87672fb5b33f9708aa945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081273"
---
# <a name="errors-1011-through-1020"></a><span data-ttu-id="5a4fb-103">Ошибки с 1011 по 1020</span><span class="sxs-lookup"><span data-stu-id="5a4fb-103">Errors 1011 through 1020</span></span>

<span data-ttu-id="5a4fb-104">Описывает ошибки поставщика WMI SNMP с 1011 по 1020.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-104">Describes WMI SNMP provider errors 1011 through 1020.</span></span>

[<span data-ttu-id="5a4fb-105">Неустранимая ошибка 1011</span><span class="sxs-lookup"><span data-stu-id="5a4fb-105">Fatal Error 1011</span></span>](#fatal-error-1011)

[<span data-ttu-id="5a4fb-106">Неустранимая ошибка 1012</span><span class="sxs-lookup"><span data-stu-id="5a4fb-106">Fatal Error 1012</span></span>](#fatal-error-1012)

[<span data-ttu-id="5a4fb-107">Неустранимая ошибка 1013</span><span class="sxs-lookup"><span data-stu-id="5a4fb-107">Fatal Error 1013</span></span>](#fatal-error-1013)

[<span data-ttu-id="5a4fb-108">Предупреждение 1014</span><span class="sxs-lookup"><span data-stu-id="5a4fb-108">Warning 1014</span></span>](#warning-1014)

[<span data-ttu-id="5a4fb-109">Неустранимая ошибка 1015</span><span class="sxs-lookup"><span data-stu-id="5a4fb-109">Fatal Error 1015</span></span>](#fatal-error-1015)

[<span data-ttu-id="5a4fb-110">Неустранимая ошибка 1016</span><span class="sxs-lookup"><span data-stu-id="5a4fb-110">Fatal Error 1016</span></span>](#fatal-error-1016)

[<span data-ttu-id="5a4fb-111">Неустранимая ошибка 1018</span><span class="sxs-lookup"><span data-stu-id="5a4fb-111">Fatal Error 1018</span></span>](#fatal-error-1018)

[<span data-ttu-id="5a4fb-112">Неустранимая ошибка 1020</span><span class="sxs-lookup"><span data-stu-id="5a4fb-112">Fatal Error 1020</span></span>](#fatal-error-1020)

## <a name="fatal-error-1011"></a><span data-ttu-id="5a4fb-113">Неустранимая ошибка 1011</span><span class="sxs-lookup"><span data-stu-id="5a4fb-113">Fatal Error 1011</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Неустранимая>: " <fileName> : <строка \#> синтаксис члена <identifier> последовательности, <identifier> ,, отличается от конструкции синтаксиса объекта типа"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-114"><span id="_1011__Fatal_____fileName___line___the_SYNTAX_of_member__identifier__of_SEQUENCE___identifier___differs_from_the_SYNTAX_clause_of_the_OBJECT-TYPE_"></span><span id="_1011__fatal_____filename___line___the_syntax_of_member__identifier__of_sequence___identifier___differs_from_the_syntax_clause_of_the_object-type_"></span><span id="_1011__FATAL_____FILENAME___LINE___THE_SYNTAX_OF_MEMBER__IDENTIFIER__OF_SEQUENCE___IDENTIFIER___DIFFERS_FROM_THE_SYNTAX_CLAUSE_OF_THE_OBJECT-TYPE_"></span>**<1011, Fatal>: "<fileName>:<line\#> the SYNTAX of member <identifier> of SEQUENCE, <identifier>, differs from the SYNTAX clause of the OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-115">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="5a4fb-115">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5a4fb-116">Элемент последовательности должен совпадать с типом в предложении СИНТАКСИСа определения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-116">An element of a SEQUENCE must be same as the type in the SYNTAX clause of the OBJECT-TYPE definition.</span></span> <span data-ttu-id="5a4fb-117">Параметр <Line \#> является строкой предложения синтаксиса определения типа объекта.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-117">The <line\#> parameter is the line of the SYNTAX clause of the OBJECT-TYPE definition.</span></span>

<span data-ttu-id="5a4fb-118">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-118">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1012"></a><span data-ttu-id="5a4fb-119">Неустранимая ошибка 1012</span><span class="sxs-lookup"><span data-stu-id="5a4fb-119">Fatal Error 1012</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Неустранимая>: " <fileName> : <строка \#> предложение индекса или дополнения является обязательным только для объектов Sequence-Types"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-120"><span id="_1012__Fatal_____fileName___line___An_INDEX_or_AUGMENTS_clause_is_required_only_for_SEQUENCE_OBJECT-TYPES_"></span><span id="_1012__fatal_____filename___line___an_index_or_augments_clause_is_required_only_for_sequence_object-types_"></span><span id="_1012__FATAL_____FILENAME___LINE___AN_INDEX_OR_AUGMENTS_CLAUSE_IS_REQUIRED_ONLY_FOR_SEQUENCE_OBJECT-TYPES_"></span>**<1012, Fatal>: "<fileName>:<line\#> An INDEX or AUGMENTS clause is required only for SEQUENCE OBJECT-TYPES"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-121">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="5a4fb-121">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5a4fb-122">Предложение INDEX должно присутствовать только в определении типа объекта, синтаксис которого разрешается в тип последовательности.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-122">An INDEX clause must only be present in an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="5a4fb-123">Эта ошибка может возникать при компиляции MIB или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-123">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="fatal-error-1013"></a><span data-ttu-id="5a4fb-124">Неустранимая ошибка 1013</span><span class="sxs-lookup"><span data-stu-id="5a4fb-124">Fatal Error 1013</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Неустранимая>: " <fileName><строка \#>: <identifier> следует разрешить в тип последовательности"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-125"><span id="_1013__Fatal_____fileName__line_____identifier__should_resolve_to_a_SEQUENCE_type_"></span><span id="_1013__fatal_____filename__line_____identifier__should_resolve_to_a_sequence_type_"></span><span id="_1013__FATAL_____FILENAME__LINE_____IDENTIFIER__SHOULD_RESOLVE_TO_A_SEQUENCE_TYPE_"></span>**<1013, Fatal>: "<fileName><line\#>: <identifier> should resolve to a SEQUENCE type"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-126">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="5a4fb-126">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5a4fb-127">Тип, используемый в конструкции "последовательность", должен разрешаться в тип последовательности.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-127">A type used in the "SEQUENCE OF" construct must resolve to a SEQUENCE type.</span></span>

<span data-ttu-id="5a4fb-128">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-128">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="warning-1014"></a><span data-ttu-id="5a4fb-129">Предупреждение 1014</span><span class="sxs-lookup"><span data-stu-id="5a4fb-129">Warning 1014</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, предупреждение>: " <fileName> : <line \#>: нерекомендуемый идентификатор значения 0 в OID"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-130"><span id="_1014__Warning_____fileName___line____Sub-identifier_of_value_0_not_recommended_in_OIDs_"></span><span id="_1014__warning_____filename___line____sub-identifier_of_value_0_not_recommended_in_oids_"></span><span id="_1014__WARNING_____FILENAME___LINE____SUB-IDENTIFIER_OF_VALUE_0_NOT_RECOMMENDED_IN_OIDS_"></span>**<1014, Warning>: "<fileName>:<line\#>: Sub-identifier of value 0 not recommended in OIDs"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-131">**Тип объекта —** семантическое предупреждение модуля вызова макроса.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-131">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="5a4fb-132">Не рекомендуется, чтобы ни один объект в стандартной MIB в Интернете не использовал в ИДЕНТИФИКАТОРе объекта подидентификатор 0.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-132">It is recommended that no object in an Internet Standard MIB use a sub-identifier of zero in its OBJECT IDENTIFIER.</span></span>

<span data-ttu-id="5a4fb-133">Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-133">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1015"></a><span data-ttu-id="5a4fb-134">Неустранимая ошибка 1015</span><span class="sxs-lookup"><span data-stu-id="5a4fb-134">Fatal Error 1015</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Неустранимая>: " <fileName> : <line \#>: OBJECT-TYPEs <identifier> из модуля <identifier> и <identifier> из модуля <identifier> назначены одинаковые значения OID"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-135"><span id="_1015__Fatal_____fileName___line____OBJECT-TYPEs__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_OID_values_"></span><span id="_1015__fatal_____filename___line____object-types__identifier__from_module__identifier__and__identifier__from_module__identifier__are_assigned_the_same_oid_values_"></span><span id="_1015__FATAL_____FILENAME___LINE____OBJECT-TYPES__IDENTIFIER__FROM_MODULE__IDENTIFIER__AND__IDENTIFIER__FROM_MODULE__IDENTIFIER__ARE_ASSIGNED_THE_SAME_OID_VALUES_"></span>**<1015, Fatal>: "<fileName>:<line\#>: OBJECT-TYPEs <identifier> from module <identifier> and <identifier> from module <identifier> are assigned the same OID values"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-136">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="5a4fb-136">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5a4fb-137">Двум вызовам **типа объекта** (в одном или разных модулях) не должно быть присвоено одинаковое значение идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-137">Two **OBJECT-TYPE** invocations (in the same or different modules) must not be assigned the same Object Identifier value.</span></span>

<span data-ttu-id="5a4fb-138">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-138">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1016"></a><span data-ttu-id="5a4fb-139">Неустранимая ошибка 1016</span><span class="sxs-lookup"><span data-stu-id="5a4fb-139">Fatal Error 1016</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Неустранимая>: " <fileName> : <line \#>: значение в предложении дефвал не соответствует типу в ПРЕДЛОЖЕНии синтаксиса"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-140"><span id="_1016__Fatal_____fileName___line____Value_in_the_DEFVAL_clause_does_not_match_the_type_in_the_SYNTAX_clause_"></span><span id="_1016__fatal_____filename___line____value_in_the_defval_clause_does_not_match_the_type_in_the_syntax_clause_"></span><span id="_1016__FATAL_____FILENAME___LINE____VALUE_IN_THE_DEFVAL_CLAUSE_DOES_NOT_MATCH_THE_TYPE_IN_THE_SYNTAX_CLAUSE_"></span>**<1016, Fatal>: "<fileName>:<line\#>: Value in the DEFVAL clause does not match the type in the SYNTAX clause"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-141">Семантическая ошибка модуля вызова макроса **типа объекта** .</span><span class="sxs-lookup"><span data-stu-id="5a4fb-141">**OBJECT-TYPE** macro invocation module semantic error.</span></span> <span data-ttu-id="5a4fb-142">Значение в предложении ДЕФВАЛ должно быть значением типа, упомянутого в предложении СИНТАКСИСа.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-142">A value in a DEFVAL clause must be a value of the type mentioned in the SYNTAX clause.</span></span>

<span data-ttu-id="5a4fb-143">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-143">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1018"></a><span data-ttu-id="5a4fb-144">Неустранимая ошибка 1018</span><span class="sxs-lookup"><span data-stu-id="5a4fb-144">Fatal Error 1018</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Неустранимая>: " <fileName><line \#>: <symbol> в предложении Enterprise для типа ловушки не разрешается в значение OID"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-145"><span id="_1018__Fatal_____fileName__line_____symbol__in_ENTERPRISE_clause_of_TRAP-TYPE_does_not_resolve_to_an_OID_value_"></span><span id="_1018__fatal_____filename__line_____symbol__in_enterprise_clause_of_trap-type_does_not_resolve_to_an_oid_value_"></span><span id="_1018__FATAL_____FILENAME__LINE_____SYMBOL__IN_ENTERPRISE_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_AN_OID_VALUE_"></span>**<1018, Fatal>: "<fileName><line\#>: <symbol> in ENTERPRISE clause of TRAP-TYPE does not resolve to an OID value"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-146">Вызов макроса **типа ловушки** , ошибка семантического модуля для конкретной ошибки.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-146">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="5a4fb-147">Символ, используемый в предложении ENTERPRISE для вызова макроса **типа ловушки** , должен разрешаться в значение идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-147">The symbol used in the ENTERPRISE clause of a **TRAP-TYPE** macro invocation must resolve to an Object Identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-1020"></a><span data-ttu-id="5a4fb-148">Неустранимая ошибка 1020</span><span class="sxs-lookup"><span data-stu-id="5a4fb-148">Fatal Error 1020</span></span>

<dl> <dt>

<span data-ttu-id="5a4fb-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Неустранимая>: " <fileName><line \#>: значение, назначенное типу ловушки, <identifier> не разрешено в положительное целое число"**</span><span class="sxs-lookup"><span data-stu-id="5a4fb-149"><span id="_1020__Fatal_____fileName__line____Value_assigned_to_TRAP-TYPE__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__fatal_____filename__line____value_assigned_to_trap-type__identifier__does_not_resolve_to_a_positive_integer_"></span><span id="_1020__FATAL_____FILENAME__LINE____VALUE_ASSIGNED_TO_TRAP-TYPE__IDENTIFIER__DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1020, Fatal>: "<fileName><line\#>: Value assigned to TRAP-TYPE <identifier> does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="5a4fb-150">Вызов макроса **типа ловушки** , ошибка семантического модуля для конкретной ошибки.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-150">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="5a4fb-151">Символ, используемый при указании значения ловушки, не разрешается в положительное целое число.</span><span class="sxs-lookup"><span data-stu-id="5a4fb-151">A symbol used in specifying the trap value does not resolve to a positive integer.</span></span>

</dd> </dl>

 

 



