---
description: Описывает ошибки поставщика WMI SNMP с 1031 по 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Ошибки с 1031 по 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664003"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="91119-103">Ошибки с 1031 по 1040</span><span class="sxs-lookup"><span data-stu-id="91119-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="91119-104">Описывает ошибки поставщика WMI SNMP с 1031 по 1040.</span><span class="sxs-lookup"><span data-stu-id="91119-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="91119-105">Предупреждение 1031</span><span class="sxs-lookup"><span data-stu-id="91119-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="91119-106">Неустранимая ошибка 1032</span><span class="sxs-lookup"><span data-stu-id="91119-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="91119-107">Неустранимая ошибка 1033</span><span class="sxs-lookup"><span data-stu-id="91119-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="91119-108">Предупреждение 1034</span><span class="sxs-lookup"><span data-stu-id="91119-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="91119-109">Предупреждение 1036</span><span class="sxs-lookup"><span data-stu-id="91119-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="91119-110">Неустранимая ошибка 1037</span><span class="sxs-lookup"><span data-stu-id="91119-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="91119-111">Неустранимая ошибка 1038</span><span class="sxs-lookup"><span data-stu-id="91119-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="91119-112">Неустранимая ошибка 1039</span><span class="sxs-lookup"><span data-stu-id="91119-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="91119-113">Неустранимая ошибка 1040</span><span class="sxs-lookup"><span data-stu-id="91119-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="91119-114">Предупреждение 1031</span><span class="sxs-lookup"><span data-stu-id="91119-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="91119-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, предупреждение>: " <fileName> : <line \#>: Стандартный символ <identifier> должен быть импортирован из модуля <identifier> . Предполагается стандартное определение ".**</span><span class="sxs-lookup"><span data-stu-id="91119-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="91119-116">ИМПОРТИРУЕТ семантическое предупреждение для модуля раздела, характерное для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-117">Если идентификатор SNMP, известный компилятору, находится в разделе IMPORTs, то модуль, из которого он импортируется, должен быть одним из стандартных модулей.</span><span class="sxs-lookup"><span data-stu-id="91119-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="91119-118">Некоторые часто используемые ИМПОРТы — "предполагаемый набор знаний" в части компилятора.</span><span class="sxs-lookup"><span data-stu-id="91119-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="91119-119">Компилятору не нужно требовать доступ к другим информационным модулям для их устранения.</span><span class="sxs-lookup"><span data-stu-id="91119-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="91119-120">Встроенные ИМПОРТы в стандартных и SNMPv2C описаны в следующих таблицах.</span><span class="sxs-lookup"><span data-stu-id="91119-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="91119-121">**Встроенные операции импорта в энергоязыке**</span><span class="sxs-lookup"><span data-stu-id="91119-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="91119-122">Класс импорта</span><span class="sxs-lookup"><span data-stu-id="91119-122">Import Class</span></span> | <span data-ttu-id="91119-123">Модуль</span><span class="sxs-lookup"><span data-stu-id="91119-123">Module</span></span>      | <span data-ttu-id="91119-124">Экземпляры</span><span class="sxs-lookup"><span data-stu-id="91119-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="91119-125">Значение ASN. 1</span><span class="sxs-lookup"><span data-stu-id="91119-125">ASN.1 Value</span></span>  | <span data-ttu-id="91119-126">RFC1155 — SMI</span><span class="sxs-lookup"><span data-stu-id="91119-126">RFC1155-SMI</span></span> | <span data-ttu-id="91119-127">Интернет, каталог, управление, экспериментальный, частный, предприятия</span><span class="sxs-lookup"><span data-stu-id="91119-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="91119-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="91119-128">RFC1213-MIB</span></span> | <span data-ttu-id="91119-129">MIB-II и IP-адрес, интерфейсы, передача</span><span class="sxs-lookup"><span data-stu-id="91119-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="91119-130">ASN. 1 тип</span><span class="sxs-lookup"><span data-stu-id="91119-130">ASN.1 Type</span></span>   | <span data-ttu-id="91119-131">RFC1155 — SMI</span><span class="sxs-lookup"><span data-stu-id="91119-131">RFC1155-SMI</span></span> | <span data-ttu-id="91119-132">NetworkAddress, IpAddress, Counter, датчик, значение TIMETICKS, непрозрачный</span><span class="sxs-lookup"><span data-stu-id="91119-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="91119-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="91119-133">RFC1213-MIB</span></span> | <span data-ttu-id="91119-134">DisplayString, Фисаддресс</span><span class="sxs-lookup"><span data-stu-id="91119-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="91119-135">Сомакрос ASN. 1</span><span class="sxs-lookup"><span data-stu-id="91119-135">ASN.1 Macro</span></span>  | <span data-ttu-id="91119-136">RFC — 1212</span><span class="sxs-lookup"><span data-stu-id="91119-136">RFC-1212</span></span>    | <span data-ttu-id="91119-137">OBJECT-TYPE</span><span class="sxs-lookup"><span data-stu-id="91119-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="91119-138">RFC — 1215</span><span class="sxs-lookup"><span data-stu-id="91119-138">RFC-1215</span></span>    | <span data-ttu-id="91119-139">ТИП ЛОВУШКИ</span><span class="sxs-lookup"><span data-stu-id="91119-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="91119-140">**Встроенные ИМПОРТы SNMPv2C**</span><span class="sxs-lookup"><span data-stu-id="91119-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="91119-141">Класс импорта</span><span class="sxs-lookup"><span data-stu-id="91119-141">Import Class</span></span>       | <span data-ttu-id="91119-142">Модуль</span><span class="sxs-lookup"><span data-stu-id="91119-142">Module</span></span>      | <span data-ttu-id="91119-143">Экземпляры</span><span class="sxs-lookup"><span data-stu-id="91119-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91119-144">Значение ASN. 1</span><span class="sxs-lookup"><span data-stu-id="91119-144">ASN.1 Value</span></span>        | <span data-ttu-id="91119-145">SNMPv2 — SMI</span><span class="sxs-lookup"><span data-stu-id="91119-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="91119-146">org, DoD, Интернет, каталог, руководства, MIB-2, передача, экспериментальные, частные, предприятия, безопасность, SNMPv2, Снмпдомаинс, Снмппроксис, Снмпмодулес</span><span class="sxs-lookup"><span data-stu-id="91119-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="91119-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="91119-147">SNMPv2-TM</span></span>   | <span data-ttu-id="91119-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="91119-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="91119-149">Идентификация объектов</span><span class="sxs-lookup"><span data-stu-id="91119-149">Object Identity</span></span>    | <span data-ttu-id="91119-150">SNMPv2 — SMI</span><span class="sxs-lookup"><span data-stu-id="91119-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="91119-151">зеродотзеро</span><span class="sxs-lookup"><span data-stu-id="91119-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="91119-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="91119-152">SNMPv2-TM</span></span>   | <span data-ttu-id="91119-153">Снмпудпдомаин, Снмпклнсдомаин, Смнпконсдомаин, Снмпддпдомаин, Снмпипксдомаин, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="91119-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="91119-154">ASN. 1 тип</span><span class="sxs-lookup"><span data-stu-id="91119-154">ASN.1 Type</span></span>         | <span data-ttu-id="91119-155">SNMPv2 — SMI</span><span class="sxs-lookup"><span data-stu-id="91119-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="91119-156">Integer32, IpAddress, Counter32, значение TIMETICKS, непрозрачный, Counter64, Unsigned32, значение Gauge32</span><span class="sxs-lookup"><span data-stu-id="91119-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="91119-157">Сомакрос ASN. 1</span><span class="sxs-lookup"><span data-stu-id="91119-157">ASN.1 Macro</span></span>        | <span data-ttu-id="91119-158">SNMPv2 — SMI</span><span class="sxs-lookup"><span data-stu-id="91119-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="91119-159">ИДЕНТИФИКАТОР МОДУЛЯ, ОБЪЕКТНО-УДОСТОВЕРЕНИЕ, ОБЪЕКТ-ТИП, ТИП УВЕДОМЛЕНИЯ</span><span class="sxs-lookup"><span data-stu-id="91119-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="91119-160">SNMPv2-CONF</span><span class="sxs-lookup"><span data-stu-id="91119-160">SNMPv2-CONF</span></span> | <span data-ttu-id="91119-161">ОБЪЕКТ-ГРУППА, УВЕДОМЛЕНИЕ-ГРУППА, МОДУЛЬ-СООТВЕТСТВИЕ, ВОЗМОЖНОСТИ АГЕНТА</span><span class="sxs-lookup"><span data-stu-id="91119-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="91119-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="91119-162">SNMPv2-TC</span></span>   | <span data-ttu-id="91119-163">ТЕКСТОВОЕ СОГЛАШЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="91119-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="91119-164">Текстовое соглашение</span><span class="sxs-lookup"><span data-stu-id="91119-164">Textual Convention</span></span> | <span data-ttu-id="91119-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="91119-165">SNMPv2-TC</span></span>   | <span data-ttu-id="91119-166">DisplayString, Фисаддресс, MacAddress, Трусвалуе, Тестандинкр, Аутономаустипе, Инстанцепоинтер, Вариаблепоинтер, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span><span class="sxs-lookup"><span data-stu-id="91119-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="91119-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="91119-167">SNMPv2-TM</span></span>   | <span data-ttu-id="91119-168">Снмпудпаддресс, Снмпосиаддресс, Снмпнбпаддресс, Снмпипксаддресс</span><span class="sxs-lookup"><span data-stu-id="91119-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="91119-169">Неустранимая ошибка 1032</span><span class="sxs-lookup"><span data-stu-id="91119-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="91119-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Неустранимая>: " <fileName><строка \#>: повторяющееся значение <value> в перечислении"**</span><span class="sxs-lookup"><span data-stu-id="91119-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-171">Семантическая ошибка модуля в перечислении, относящаяся к неограниченному или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-172">Дублирующихся значений не должно быть.</span><span class="sxs-lookup"><span data-stu-id="91119-172">There must not be any duplicate values.</span></span> <span data-ttu-id="91119-173">Параметр <Line \#> — это расположение повторения имени и значения.</span><span class="sxs-lookup"><span data-stu-id="91119-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="91119-174">Неустранимая ошибка 1033</span><span class="sxs-lookup"><span data-stu-id="91119-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="91119-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Неустранимая>: " <fileName><строка \#>: повторяющееся имя <identifier> в перечислении"**</span><span class="sxs-lookup"><span data-stu-id="91119-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-176">Семантическая ошибка модуля в перечислении, относящаяся к неограниченному или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-177">Дублирующихся имен не должно быть.</span><span class="sxs-lookup"><span data-stu-id="91119-177">There must not be any duplicate names.</span></span> <span data-ttu-id="91119-178">Параметр <Line \#> — это расположение повторения имени и значения.</span><span class="sxs-lookup"><span data-stu-id="91119-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="91119-179">Предупреждение 1034</span><span class="sxs-lookup"><span data-stu-id="91119-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="91119-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, предупреждение>: " <fileName><line \#>: значение 0, запрещенное в перечислении"**</span><span class="sxs-lookup"><span data-stu-id="91119-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-181">Семантическое предупреждение модуля в перечислении, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-182">Рекомендуется, чтобы именованное значение нуль не применялось в перечислении.</span><span class="sxs-lookup"><span data-stu-id="91119-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="91119-183">Предупреждение 1036</span><span class="sxs-lookup"><span data-stu-id="91119-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="91119-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, предупреждение> " <fileName><line \#>: значение в перечислении не разрешается в положительное целое"**</span><span class="sxs-lookup"><span data-stu-id="91119-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-185">Семантическое предупреждение модуля в перечислении, характерное для неограниченного или SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-186">Отрицательное значение недопустимо в перечислении.</span><span class="sxs-lookup"><span data-stu-id="91119-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="91119-187">Неустранимая ошибка 1037</span><span class="sxs-lookup"><span data-stu-id="91119-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="91119-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Неустранимая>: " <fileName><строка \#>: идентификатор <identifier> не разрешается в строку октета или непрозрачные типы"**</span><span class="sxs-lookup"><span data-stu-id="91119-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-189">Семантическая ошибка модуля в спецификации размера, характерная для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-190">Символ, используемый в спецификации размера, должен разрешаться в строку ОКТЕТа или непрозрачность.</span><span class="sxs-lookup"><span data-stu-id="91119-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="91119-191">Неустранимая ошибка 1038</span><span class="sxs-lookup"><span data-stu-id="91119-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="91119-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> не разрешает тип целого числа или типа датчика"**</span><span class="sxs-lookup"><span data-stu-id="91119-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-193">Семантическая ошибка модуля в спецификации диапазона.</span><span class="sxs-lookup"><span data-stu-id="91119-193">Module semantic error in range specification.</span></span> <span data-ttu-id="91119-194">Эта ошибка может возникать в SNMPv2C или с.</span><span class="sxs-lookup"><span data-stu-id="91119-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="91119-195">В стандарте, символ, используемый в спецификации диапазона, должен разрешаться в ЦЕЛОе число или датчик.</span><span class="sxs-lookup"><span data-stu-id="91119-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="91119-196">В SNMPv2C символ, используемый в спецификации диапазона, должен разрешаться в целые числа, значение Gauge32, integer32 или Unsigned32.</span><span class="sxs-lookup"><span data-stu-id="91119-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="91119-197">Неустранимая ошибка 1039</span><span class="sxs-lookup"><span data-stu-id="91119-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="91119-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Неустранимая>: <fileName><строка \#>: отрицательное значение используется в спецификации размера "**</span><span class="sxs-lookup"><span data-stu-id="91119-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-199">Семантическая ошибка модуля в спецификации размера, характерная для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-200">Любое значение, используемое при указании размера, не должно быть отрицательным.</span><span class="sxs-lookup"><span data-stu-id="91119-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="91119-201">Неустранимая ошибка 1040</span><span class="sxs-lookup"><span data-stu-id="91119-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="91119-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Неустранимая>: " <fileName><line \#>: идентификатор <identifier> в спецификации размера не разрешается в неотрицательное целочисленное значение"**</span><span class="sxs-lookup"><span data-stu-id="91119-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="91119-203">Семантическая ошибка модуля в спецификации Range или size, характерная для не SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="91119-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="91119-204">Любой символ, используемый при указании значения в спецификации размера, разрешается в неотрицательное значение.</span><span class="sxs-lookup"><span data-stu-id="91119-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



