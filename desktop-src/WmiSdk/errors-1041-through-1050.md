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
# <a name="errors-1041-through-1050"></a><span data-ttu-id="f2c51-103">Ошибки с 1041 по 1050</span><span class="sxs-lookup"><span data-stu-id="f2c51-103">Errors 1041 through 1050</span></span>

<span data-ttu-id="f2c51-104">Описывает ошибки поставщика WMI SNMP с 1041 по 1050.</span><span class="sxs-lookup"><span data-stu-id="f2c51-104">Describes WMI SNMP provider errors 1041 through 1050.</span></span>

[<span data-ttu-id="f2c51-105">Неустранимая ошибка 1041</span><span class="sxs-lookup"><span data-stu-id="f2c51-105">Fatal Error 1041</span></span>](#fatal-error-1041)

[<span data-ttu-id="f2c51-106">Неустранимая ошибка 1042</span><span class="sxs-lookup"><span data-stu-id="f2c51-106">Fatal Error 1042</span></span>](#fatal-error-1042)

[<span data-ttu-id="f2c51-107">Предупреждение 1043</span><span class="sxs-lookup"><span data-stu-id="f2c51-107">Warning 1043</span></span>](#warning-1043)

[<span data-ttu-id="f2c51-108">Неустранимая ошибка 1044</span><span class="sxs-lookup"><span data-stu-id="f2c51-108">Fatal Error 1044</span></span>](#fatal-error-1044)

[<span data-ttu-id="f2c51-109">Предупреждение 1045</span><span class="sxs-lookup"><span data-stu-id="f2c51-109">Warning 1045</span></span>](#warning-1045)

[<span data-ttu-id="f2c51-110">Предупреждение 1046</span><span class="sxs-lookup"><span data-stu-id="f2c51-110">Warning 1046</span></span>](#warning-1046)

[<span data-ttu-id="f2c51-111">Предупреждение 1047</span><span class="sxs-lookup"><span data-stu-id="f2c51-111">Warning 1047</span></span>](#warning-1047)

[<span data-ttu-id="f2c51-112">Предупреждение 1048</span><span class="sxs-lookup"><span data-stu-id="f2c51-112">Warning 1048</span></span>](#warning-1048)

[<span data-ttu-id="f2c51-113">Неустранимая ошибка 1049</span><span class="sxs-lookup"><span data-stu-id="f2c51-113">Fatal Error 1049</span></span>](#fatal-error-1049)

## <a name="fatal-error-1041"></a><span data-ttu-id="f2c51-114">Неустранимая ошибка 1041</span><span class="sxs-lookup"><span data-stu-id="f2c51-114">Fatal Error 1041</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в спецификации диапазона не разрешается в целочисленное значение"**</span><span class="sxs-lookup"><span data-stu-id="f2c51-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Fatal>: "<fileName><line\#>: Identifier <identifier> in range specification does not resolve to an integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-116">Семантическая ошибка модуля в спецификации Range или size, характерная для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-116">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-117">Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="f2c51-117">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="f2c51-118">Любое значение, используемое при указании диапазона, должно быть целым числом.</span><span class="sxs-lookup"><span data-stu-id="f2c51-118">Any value used in specifying a range must be an integer.</span></span>

</dd> </dl>

## <a name="fatal-error-1042"></a><span data-ttu-id="f2c51-119">Неустранимая ошибка 1042</span><span class="sxs-lookup"><span data-stu-id="f2c51-119">Fatal Error 1042</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Неустранимая>: " <fileName><line \#>: Верхняя граница спецификации диапазона меньше нижней границы"**</span><span class="sxs-lookup"><span data-stu-id="f2c51-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Fatal>: "<fileName><line\#>: Upper bound of range specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-121">Семантическая ошибка модуля в спецификации Range или size, характерная для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-121">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-122">Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="f2c51-122">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="f2c51-123">Нижняя граница спецификации диапазона или размера не должна превышать верхнюю границу.</span><span class="sxs-lookup"><span data-stu-id="f2c51-123">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="warning-1043"></a><span data-ttu-id="f2c51-124">Предупреждение 1043</span><span class="sxs-lookup"><span data-stu-id="f2c51-124">Warning 1043</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, предупреждение>: " <fileName> : <строка \#>: объект-Type с синтаксисом" Sequence ", должен иметь предложение доступа" недоступно "**</span><span class="sxs-lookup"><span data-stu-id="f2c51-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE", should have an ACCESS clause "not-accessible"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-126">**Тип объекта —** семантическое предупреждение модуля вызова макроса.</span><span class="sxs-lookup"><span data-stu-id="f2c51-126">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="f2c51-127">Таблица или концептуальная строка (последовательность или типы объектов последовательности, соответственно) должны иметь значение "недоступно".</span><span class="sxs-lookup"><span data-stu-id="f2c51-127">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="f2c51-128">Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-128">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1044"></a><span data-ttu-id="f2c51-129">Неустранимая ошибка 1044</span><span class="sxs-lookup"><span data-stu-id="f2c51-129">Fatal Error 1044</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Неустранимая>: " <fileName><line \#>: переопределение символа <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="f2c51-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Fatal>: "<fileName><line\#>: Redefinition of symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-131">Семантическая ошибка модуля, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-131">Module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-132">Переопределение дескрипторов объектов, вызовов макросов и типов ASN. 1 приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="f2c51-132">Redefinition of object descriptors, macro invocations, and ASN.1 types cause an error.</span></span>

</dd> </dl>

## <a name="warning-1045"></a><span data-ttu-id="f2c51-133">Предупреждение 1045</span><span class="sxs-lookup"><span data-stu-id="f2c51-133">Warning 1045</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, предупреждение>: " <fileName><линереференце to Standard Symbol <symbolName> предполагается для определения, как в <moduleName> . Если вы хотите ссылаться на определение в текущем модуле, используйте нотации "Module. Symbol".**</span><span class="sxs-lookup"><span data-stu-id="f2c51-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Warning>: "<fileName><lineReference to standard symbol <symbolName> assumed to be for the definition as in <moduleName>. Use the "module.symbol" notations, if you want to refer to the definition in the current module"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-135">Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-135">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-136">Символ, известный компилятору, был переопределен, и на него имеется ссылка.</span><span class="sxs-lookup"><span data-stu-id="f2c51-136">A symbol known to the compiler has been redefined, and is being referenced.</span></span> <span data-ttu-id="f2c51-137">Компилятор предполагает стандартное определение символа.</span><span class="sxs-lookup"><span data-stu-id="f2c51-137">The compiler assumes the standard definition of the symbol.</span></span> <span data-ttu-id="f2c51-138">Таким образом, чтобы использовать переопределение стандартного символа, необходимо использовать нотацию Module. Symbol.</span><span class="sxs-lookup"><span data-stu-id="f2c51-138">Therefore, to use a redefinition of the standard symbol, you must use the "Module.Symbol" notation.</span></span>

</dd> </dl>

## <a name="warning-1046"></a><span data-ttu-id="f2c51-139">Предупреждение 1046</span><span class="sxs-lookup"><span data-stu-id="f2c51-139">Warning 1046</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, предупреждение>: " <fileName><строка \#>: не <symbol> определено. Предполагается стандартное определение "**</span><span class="sxs-lookup"><span data-stu-id="f2c51-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Warning>: "<fileName><line\#>: <symbol> undefined. Assuming standard definition"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-141">Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-141">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-142">Символ, известный компилятору, не должен быть переопределен или использоваться без импорта.</span><span class="sxs-lookup"><span data-stu-id="f2c51-142">A symbol known to the compiler must not be redefined or used without being imported.</span></span>

</dd> </dl>

## <a name="warning-1047"></a><span data-ttu-id="f2c51-143">Предупреждение 1047</span><span class="sxs-lookup"><span data-stu-id="f2c51-143">Warning 1047</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, предупреждение>: " <fileName><строка \#>: определение типа <symbol> определено, но не указано в ссылке"**</span><span class="sxs-lookup"><span data-stu-id="f2c51-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Warning>: "<fileName><line\#>: Type definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-145">Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-145">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-146">Все назначения значений и определения типов должны быть на месте.</span><span class="sxs-lookup"><span data-stu-id="f2c51-146">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="warning-1048"></a><span data-ttu-id="f2c51-147">Предупреждение 1048</span><span class="sxs-lookup"><span data-stu-id="f2c51-147">Warning 1048</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, предупреждение>: " <fileName><строка \#>: определение значения <symbol> определено, но не указано в ссылке"**</span><span class="sxs-lookup"><span data-stu-id="f2c51-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Warning>: "<fileName><line\#>: Value definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-149">Семантическое предупреждение модуля, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="f2c51-149">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="f2c51-150">Все назначения значений и определения типов должны быть на месте.</span><span class="sxs-lookup"><span data-stu-id="f2c51-150">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="fatal-error-1049"></a><span data-ttu-id="f2c51-151">Неустранимая ошибка 1049</span><span class="sxs-lookup"><span data-stu-id="f2c51-151">Fatal Error 1049</span></span>

<dl> <dt>

<span data-ttu-id="f2c51-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Неустранимая>: " <fileName> : <line \#>: предложение дефвал недопустимо для Object-Type с синтаксисом NetworkAddress"**</span><span class="sxs-lookup"><span data-stu-id="f2c51-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Fatal>: "<fileName>:<line\#>: DEFVAL clause not allowed for OBJECT-TYPE with SYNTAX NetworkAddress"**</span></span>
</dt> <dd>

<span data-ttu-id="f2c51-153">**Объект-тип** вызова макроса с определенной семантикой модуля.</span><span class="sxs-lookup"><span data-stu-id="f2c51-153">**OBJECT-TYPE** macro invocation SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="f2c51-154">Предложение ДЕФВАЛ недопустимо для типа OBJECT-TYPE, предложение СИНТАКСИСа которого разрешается в NetworkAddress.</span><span class="sxs-lookup"><span data-stu-id="f2c51-154">The DEFVAL clause is not allowed for an OBJECT-TYPE whose SYNTAX clause resolves to NetworkAddress.</span></span>

</dd> </dl>

 

 



