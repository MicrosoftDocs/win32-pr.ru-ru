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
# <a name="errors-1021-through-1030"></a><span data-ttu-id="4a895-103">Ошибки с 1021 по 1030</span><span class="sxs-lookup"><span data-stu-id="4a895-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="4a895-104">Описывает ошибки поставщика WMI SNMP с 1021 по 1033.</span><span class="sxs-lookup"><span data-stu-id="4a895-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="4a895-105">Неустранимая ошибка 1021</span><span class="sxs-lookup"><span data-stu-id="4a895-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="4a895-106">Неустранимая ошибка 1022</span><span class="sxs-lookup"><span data-stu-id="4a895-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="4a895-107">Неустранимая ошибка 1023</span><span class="sxs-lookup"><span data-stu-id="4a895-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="4a895-108">Неустранимая ошибка 1024</span><span class="sxs-lookup"><span data-stu-id="4a895-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="4a895-109">Неустранимая ошибка 1025</span><span class="sxs-lookup"><span data-stu-id="4a895-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="4a895-110">Неустранимая ошибка 1026</span><span class="sxs-lookup"><span data-stu-id="4a895-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="4a895-111">Предупреждение 1027</span><span class="sxs-lookup"><span data-stu-id="4a895-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="4a895-112">Неустранимая ошибка 1028</span><span class="sxs-lookup"><span data-stu-id="4a895-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="4a895-113">Неустранимая ошибка 1029</span><span class="sxs-lookup"><span data-stu-id="4a895-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="4a895-114">Неустранимая ошибка 1030</span><span class="sxs-lookup"><span data-stu-id="4a895-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="4a895-115">Неустранимая ошибка 1021</span><span class="sxs-lookup"><span data-stu-id="4a895-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="4a895-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в предложении VARIABLEs типа ловушки не разрешается в скалярный тип объекта"**</span><span class="sxs-lookup"><span data-stu-id="4a895-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-117">Вызов макроса **типа ловушки** , ошибка семантического модуля для конкретной ошибки.</span><span class="sxs-lookup"><span data-stu-id="4a895-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="4a895-118">Каждый элемент в списке переменных, используемых в предложении VARIABLEs для вызова макроса **типа ловушки** , должен разрешаться в имя скалярного экземпляра типа объекта.</span><span class="sxs-lookup"><span data-stu-id="4a895-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="4a895-119">Неустранимая ошибка 1022</span><span class="sxs-lookup"><span data-stu-id="4a895-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="4a895-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Неустранимая>: " <fileName><строка \#>: значение не разрешено к типу <type> "**</span><span class="sxs-lookup"><span data-stu-id="4a895-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-121">Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-122">Неверное значение для значения **RHS, равного значению, строке** октета или присваивания значения идентификатору объекта.</span><span class="sxs-lookup"><span data-stu-id="4a895-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="4a895-123">Неустранимая ошибка 1023</span><span class="sxs-lookup"><span data-stu-id="4a895-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="4a895-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Неустранимая>: " <fileName><строка \#>: идентификатор <identifier> не разрешается в тип <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="4a895-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-125">Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-126">Символ (ссылка на значение) для параметра RHS ЦЕЛОго числа, **null**, строки октета или присваивания значения идентификатора объекта не разрешается в правильный тип.</span><span class="sxs-lookup"><span data-stu-id="4a895-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="4a895-127">Неустранимая ошибка 1024</span><span class="sxs-lookup"><span data-stu-id="4a895-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="4a895-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Неустранимая>: " <fileName><строка \#>: отрицательное целое число в определении значения OID"**</span><span class="sxs-lookup"><span data-stu-id="4a895-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-129">Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-130">Все значения в списке компонентов OID должны быть неотрицательными (желательно положительными) целыми числами.</span><span class="sxs-lookup"><span data-stu-id="4a895-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="4a895-131">Неустранимая ошибка 1025</span><span class="sxs-lookup"><span data-stu-id="4a895-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="4a895-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Неустранимая>: "идентификатор <identifier> в значении OID не разрешается в положительное целое"**</span><span class="sxs-lookup"><span data-stu-id="4a895-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-133">Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-134">Все значения в списке компонентов OID должны быть неотрицательными (желательно положительными) целыми числами.</span><span class="sxs-lookup"><span data-stu-id="4a895-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="4a895-135">Неустранимая ошибка 1026</span><span class="sxs-lookup"><span data-stu-id="4a895-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="4a895-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в значении OID не разрешается в значение OID или положительное целое"**</span><span class="sxs-lookup"><span data-stu-id="4a895-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-137">Семантическая ошибка модуля назначения значений, характерная для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-138">Первый компонент, используемый в значении OID, должен разрешаться в значение OID или ЦЕЛОе число.</span><span class="sxs-lookup"><span data-stu-id="4a895-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="4a895-139">Предупреждение 1027</span><span class="sxs-lookup"><span data-stu-id="4a895-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="4a895-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, предупреждение>: " <fileName><строка \#>: импортированный символ не <identifier> используется"**</span><span class="sxs-lookup"><span data-stu-id="4a895-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-141">ИМПОРТИРУЕТ семантическое предупреждение для модуля раздела, характерное для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-142">Для каждого неиспользуемого импортированного символа выдается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="4a895-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="4a895-143">Неустранимая ошибка 1028</span><span class="sxs-lookup"><span data-stu-id="4a895-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="4a895-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Неустранимая>: "модуль <identifier> не импортирован в раздел Imports"**</span><span class="sxs-lookup"><span data-stu-id="4a895-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-145">Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-146">Имя модуля, используемое для ссылки на символ, должно либо присутствовать в предложении IMPORTs, либо быть именем текущего модуля.</span><span class="sxs-lookup"><span data-stu-id="4a895-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="4a895-147">Неустранимая ошибка 1029</span><span class="sxs-lookup"><span data-stu-id="4a895-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="4a895-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Неустранимая>: " <fileName><строка \#>: текущий модуль <identifier> не может быть импортирован"**</span><span class="sxs-lookup"><span data-stu-id="4a895-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-149">Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-150">Имя текущего модуля также имеет значение в списке ИМПОРТов.</span><span class="sxs-lookup"><span data-stu-id="4a895-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="4a895-151">Неустранимая ошибка 1030</span><span class="sxs-lookup"><span data-stu-id="4a895-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="4a895-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Неустранимая>: " <fileName><строка \#>: символ <identifier> не импортирован из модуля <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="4a895-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="4a895-153">Семантическая ошибка модуля импорта раздела, относящаяся к ни к, ни к, ни к SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="4a895-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="4a895-154">Вы использовали нотацию "Module. Symbol", но символ не был импортирован из указанного модуля в разделе IMPORTs.</span><span class="sxs-lookup"><span data-stu-id="4a895-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



