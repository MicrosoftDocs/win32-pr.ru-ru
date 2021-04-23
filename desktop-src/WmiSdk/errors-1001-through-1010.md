---
description: Описывает ошибки поставщика WMI SNMP с 1001 по 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Ошибки с 1001 по 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712111"
---
# <a name="errors-1001-through-1010"></a><span data-ttu-id="82fd9-103">Ошибки с 1001 по 1010</span><span class="sxs-lookup"><span data-stu-id="82fd9-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="82fd9-104">Описывает ошибки поставщика WMI SNMP с 1001 по 1010.</span><span class="sxs-lookup"><span data-stu-id="82fd9-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="82fd9-105">Неустранимая ошибка 1001</span><span class="sxs-lookup"><span data-stu-id="82fd9-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="82fd9-106">Неустранимая ошибка 1002</span><span class="sxs-lookup"><span data-stu-id="82fd9-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="82fd9-107">Неустранимая ошибка 1003</span><span class="sxs-lookup"><span data-stu-id="82fd9-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="82fd9-108">Предупреждение 1004</span><span class="sxs-lookup"><span data-stu-id="82fd9-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="82fd9-109">Предупреждение 1005</span><span class="sxs-lookup"><span data-stu-id="82fd9-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="82fd9-110">Неустранимая ошибка 1006</span><span class="sxs-lookup"><span data-stu-id="82fd9-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="82fd9-111">Неустранимая ошибка 1008</span><span class="sxs-lookup"><span data-stu-id="82fd9-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="82fd9-112">Неустранимая ошибка 1001</span><span class="sxs-lookup"><span data-stu-id="82fd9-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Неустранимая>: " <fileName> : <line \#>: предложение синтаксиса типа Object-Type не разрешается в допустимые типы"</span><span class="sxs-lookup"><span data-stu-id="82fd9-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-114">Семантическая ошибка модуля вызова макроса типа объекта.</span><span class="sxs-lookup"><span data-stu-id="82fd9-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="82fd9-115">Предложение СИНТАКСИСа макроса типа OBJECT-TYPE должно разрешаться в тип или подтип, сформированный с помощью спецификации SIZE или Range, которую разрешает SMI или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="82fd9-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="82fd9-116">Если это не так, то сообщается о неустранимой ошибке 1001.</span><span class="sxs-lookup"><span data-stu-id="82fd9-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="82fd9-117">Эта ошибка может возникать при компиляции MIB или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="82fd9-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="82fd9-118">К типам, которые допускаются SMI, используют следующие типы:</span><span class="sxs-lookup"><span data-stu-id="82fd9-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="82fd9-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="82fd9-119">INTEGER</span></span>
-   <span data-ttu-id="82fd9-120">NULL</span><span class="sxs-lookup"><span data-stu-id="82fd9-120">NULL</span></span>
-   <span data-ttu-id="82fd9-121">СТРОКА ОКТЕТА</span><span class="sxs-lookup"><span data-stu-id="82fd9-121">OCTET STRING</span></span>
-   <span data-ttu-id="82fd9-122">ИДЕНТИФИКАТОР ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="82fd9-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="82fd9-123">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="82fd9-123">NetworkAddress</span></span>
-   <span data-ttu-id="82fd9-124">IPAddress</span><span class="sxs-lookup"><span data-stu-id="82fd9-124">IpAddress</span></span>
-   <span data-ttu-id="82fd9-125">Счетчик</span><span class="sxs-lookup"><span data-stu-id="82fd9-125">Counter</span></span>
-   <span data-ttu-id="82fd9-126">Датчик</span><span class="sxs-lookup"><span data-stu-id="82fd9-126">Gauge</span></span>
-   <span data-ttu-id="82fd9-127">Значение TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="82fd9-127">TimeTicks</span></span>
-   <span data-ttu-id="82fd9-128">Непрозрачный</span><span class="sxs-lookup"><span data-stu-id="82fd9-128">Opaque</span></span>
-   <span data-ttu-id="82fd9-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="82fd9-129">DisplayString</span></span>
-   <span data-ttu-id="82fd9-130">фисаддресс</span><span class="sxs-lookup"><span data-stu-id="82fd9-130">PhysAddress</span></span>

<span data-ttu-id="82fd9-131">Типы, разрешенные SMI SNMPv2C:</span><span class="sxs-lookup"><span data-stu-id="82fd9-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="82fd9-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="82fd9-132">INTEGER</span></span>
-   <span data-ttu-id="82fd9-133">СТРОКА ОКТЕТА</span><span class="sxs-lookup"><span data-stu-id="82fd9-133">OCTET STRING</span></span>
-   <span data-ttu-id="82fd9-134">ИДЕНТИФИКАТОР ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="82fd9-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="82fd9-135">BITS</span><span class="sxs-lookup"><span data-stu-id="82fd9-135">BITS</span></span>
-   <span data-ttu-id="82fd9-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="82fd9-136">Integer32</span></span>
-   <span data-ttu-id="82fd9-137">IPAddress</span><span class="sxs-lookup"><span data-stu-id="82fd9-137">IpAddress</span></span>
-   <span data-ttu-id="82fd9-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="82fd9-138">Counter32</span></span>
-   <span data-ttu-id="82fd9-139">Значение TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="82fd9-139">TimeTicks</span></span>
-   <span data-ttu-id="82fd9-140">Непрозрачный</span><span class="sxs-lookup"><span data-stu-id="82fd9-140">Opaque</span></span>
-   <span data-ttu-id="82fd9-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="82fd9-141">Counter64</span></span>
-   <span data-ttu-id="82fd9-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="82fd9-142">Unsigned32</span></span>
-   <span data-ttu-id="82fd9-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="82fd9-143">DisplayString</span></span>
-   <span data-ttu-id="82fd9-144">фисаддресс</span><span class="sxs-lookup"><span data-stu-id="82fd9-144">PhysAddress</span></span>
-   <span data-ttu-id="82fd9-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="82fd9-145">MacAddress</span></span>
-   <span data-ttu-id="82fd9-146">трусвалуе</span><span class="sxs-lookup"><span data-stu-id="82fd9-146">TruthValue</span></span>
-   <span data-ttu-id="82fd9-147">тестандинкр</span><span class="sxs-lookup"><span data-stu-id="82fd9-147">TestAndIncr</span></span>
-   <span data-ttu-id="82fd9-148">аутономаустипе</span><span class="sxs-lookup"><span data-stu-id="82fd9-148">AutonomousType</span></span>
-   <span data-ttu-id="82fd9-149">инстанцепоинтер</span><span class="sxs-lookup"><span data-stu-id="82fd9-149">InstancePointer</span></span>
-   <span data-ttu-id="82fd9-150">вариаблепоинтер</span><span class="sxs-lookup"><span data-stu-id="82fd9-150">VariablePointer</span></span>
-   <span data-ttu-id="82fd9-151">ровпоинтер</span><span class="sxs-lookup"><span data-stu-id="82fd9-151">RowPointer</span></span>
-   <span data-ttu-id="82fd9-152">ровстатус</span><span class="sxs-lookup"><span data-stu-id="82fd9-152">RowStatus</span></span>
-   <span data-ttu-id="82fd9-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="82fd9-153">TimeStamp</span></span>
-   <span data-ttu-id="82fd9-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="82fd9-154">TimeInterval</span></span>
-   <span data-ttu-id="82fd9-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="82fd9-155">DateAndTime</span></span>
-   <span data-ttu-id="82fd9-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="82fd9-156">StorageType</span></span>
-   <span data-ttu-id="82fd9-157">тдомаин</span><span class="sxs-lookup"><span data-stu-id="82fd9-157">Tdomain</span></span>
-   <span data-ttu-id="82fd9-158">таддресс</span><span class="sxs-lookup"><span data-stu-id="82fd9-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="82fd9-159">Неустранимая ошибка 1002</span><span class="sxs-lookup"><span data-stu-id="82fd9-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Неустранимая>: " <fileName> : <line \#>: Недопустимое предложение доступа <clause> "</span><span class="sxs-lookup"><span data-stu-id="82fd9-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-161">Семантическая ошибка модуля вызова макроса типа объекта.</span><span class="sxs-lookup"><span data-stu-id="82fd9-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="82fd9-162">В версии в версии с параметром "макрос" должен быть предложен доступ только для чтения, "только запись", "чтение/запись" или "недоступно".</span><span class="sxs-lookup"><span data-stu-id="82fd9-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="82fd9-163">Для SNMPv2C предложение MAX-ACCESS должно иметь значение "только для чтения", "чтение-создать", "чтение/запись" или "недоступно".</span><span class="sxs-lookup"><span data-stu-id="82fd9-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="82fd9-164">Неустранимая ошибка 1003</span><span class="sxs-lookup"><span data-stu-id="82fd9-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Неустранимая>: " <fileName> : <line \#>: Недопустимое предложение состояния <clause> "</span><span class="sxs-lookup"><span data-stu-id="82fd9-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-166">Семантическая ошибка модуля вызова макроса типа объекта.</span><span class="sxs-lookup"><span data-stu-id="82fd9-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="82fd9-167">В версии с параметром STATUS в качестве условия вызова макроса типа OBJECT должен быть "обязательный", "необязательный", "устаревший" или "устаревший".</span><span class="sxs-lookup"><span data-stu-id="82fd9-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="82fd9-168">Для SNMPv2C предложение STATUS вызова макроса типа OBJECT должно быть "Current", "устарело" или "устарело".</span><span class="sxs-lookup"><span data-stu-id="82fd9-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="82fd9-169">Предупреждение 1004</span><span class="sxs-lookup"><span data-stu-id="82fd9-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> : <line \#>: Object-Type <identifier> , синтаксис которого разрешается в один из типов счетчиков, не заканчивается буквой" "</span><span class="sxs-lookup"><span data-stu-id="82fd9-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-171">Тип объекта — семантическое предупреждение модуля вызова макроса.</span><span class="sxs-lookup"><span data-stu-id="82fd9-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="82fd9-172">Идентификатор объекта счетчика СИНТАКСИСа (в версии/с) или Counter32 и Counter64 (SNMPv2C) должен быть во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="82fd9-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="82fd9-173">Это предупреждение может возникать при компиляции MIB либо SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="82fd9-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="82fd9-174">Предупреждение 1005</span><span class="sxs-lookup"><span data-stu-id="82fd9-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, предупреждение>: " <fileName> : <строка \#>: объект-Type с синтаксисом" Sequence ", должен иметь предложение доступа" недоступно "</span><span class="sxs-lookup"><span data-stu-id="82fd9-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-176">Тип объекта — семантическое предупреждение модуля вызова макроса.</span><span class="sxs-lookup"><span data-stu-id="82fd9-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="82fd9-177">Таблица или концептуальная строка (последовательность или типы объектов последовательности, соответственно) должны иметь значение "недоступно".</span><span class="sxs-lookup"><span data-stu-id="82fd9-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="82fd9-178">Это предупреждение может возникать либо в настоящем, либо в SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="82fd9-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="82fd9-179">Неустранимая ошибка 1006</span><span class="sxs-lookup"><span data-stu-id="82fd9-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Неустранимая>: " <fileName> : <строка \#> объектный тип <identifier> , который имеет синтаксическую последовательность, не имеет предложения index или дополнения"</span><span class="sxs-lookup"><span data-stu-id="82fd9-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-181">Семантическая ошибка модуля вызова макроса типа объекта.</span><span class="sxs-lookup"><span data-stu-id="82fd9-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="82fd9-182">В настоящее время для определения типа объекта должно присутствовать предложение INDEX, синтаксис которого разрешается в тип последовательности.</span><span class="sxs-lookup"><span data-stu-id="82fd9-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="82fd9-183">Для SNMPv2C для объявления концептуальной строки должен присутствовать либо индекс, либо предложение дополнения.</span><span class="sxs-lookup"><span data-stu-id="82fd9-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="82fd9-184">Неустранимая ошибка 1008</span><span class="sxs-lookup"><span data-stu-id="82fd9-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="82fd9-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Неустранимая>: " <fileName> : <line \#>: объект-Type <identifier> , который имеет синтаксис" Sequence ", не был указан"</span><span class="sxs-lookup"><span data-stu-id="82fd9-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="82fd9-186">Семантическая ошибка модуля вызова макроса типа объекта.</span><span class="sxs-lookup"><span data-stu-id="82fd9-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="82fd9-187">ОБЪЕКТный тип с предложением СИНТАКСИСа в качестве типа последовательности должен быть представлен в предложении СИНТАКСИСа только одного вызова типа объекта, который означает объявление таблицы, то есть объект с предложением СИНТАКСИСа в виде последовательности типа.</span><span class="sxs-lookup"><span data-stu-id="82fd9-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="82fd9-188">Параметр <Line \#> ссылается на вторую точку ссылки.</span><span class="sxs-lookup"><span data-stu-id="82fd9-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="82fd9-189">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="82fd9-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



