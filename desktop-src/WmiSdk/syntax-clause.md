---
description: Содержит предложение СИНТАКСИСа, определяющее данные и тип для объекта MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Предложение СИНТАКСИСа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703252"
---
# <a name="syntax-clause"></a><span data-ttu-id="98d7f-103">Предложение СИНТАКСИСа</span><span class="sxs-lookup"><span data-stu-id="98d7f-103">SYNTAX Clause</span></span>

<span data-ttu-id="98d7f-104">Макрос [Object-Type](object-type-macro.md) содержит предложение синтаксиса, определяющее данные и тип для объекта MIB.</span><span class="sxs-lookup"><span data-stu-id="98d7f-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="98d7f-105">Хотя поставщик SNMP следит за общими правилами сопоставления предложений СИНТАКСИСа, поставщик также соответствует правилам, характерным для нескольких типов данных.</span><span class="sxs-lookup"><span data-stu-id="98d7f-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="98d7f-106">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="98d7f-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="98d7f-107">Следующие правила сопоставления применяются ко всем типам данных, описанным в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="98d7f-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="98d7f-108">Текстовое представление предложения СИНТАКСИСа сопоставляется с **текстовым \_ правилом** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="98d7f-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="98d7f-109">Определение именованного типа в предложении СИНТАКСИСа соответствует **\_ синтаксису объекта** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="98d7f-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="98d7f-110">Это сопоставление различается в зависимости от типа данных.</span><span class="sxs-lookup"><span data-stu-id="98d7f-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="98d7f-111">Дополнительные сведения см. в описании сопоставления.</span><span class="sxs-lookup"><span data-stu-id="98d7f-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="98d7f-112">Тип SNMP, используемый при кодировании кадров протокола в Юникоде и SNMPv2C, соответствует **кодировке** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="98d7f-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="98d7f-113">Квалификатор свойства CIM **Цимтипе** содержит текстовое представление, которое форматирует базовое значение протокола CIM.</span><span class="sxs-lookup"><span data-stu-id="98d7f-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="98d7f-114">В следующей таблице перечислены типы данных, имеющие определенные правила, которые управляют поведением сопоставления поставщика.</span><span class="sxs-lookup"><span data-stu-id="98d7f-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="98d7f-115">Тип данных SNMP</span><span class="sxs-lookup"><span data-stu-id="98d7f-115">SNMP data type</span></span>                                     | <span data-ttu-id="98d7f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="98d7f-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="98d7f-117">Тип-примитив</span><span class="sxs-lookup"><span data-stu-id="98d7f-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="98d7f-118">Один из основных типов данных, определенных в структуре документов по управлению данными (SMI) RFC 1213 и RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="98d7f-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="98d7f-119">Текстовое соглашение</span><span class="sxs-lookup"><span data-stu-id="98d7f-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="98d7f-120">Определение типа, созданное с помощью явного использования макроса **ТЕКСТОВОГО соглашения** SNMPv2c или созданного с помощью именованного типа.</span><span class="sxs-lookup"><span data-stu-id="98d7f-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="98d7f-121">Текстовое соглашение назначает имя и, в некоторых случаях, диапазон значений для существующего типа данных.</span><span class="sxs-lookup"><span data-stu-id="98d7f-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="98d7f-122">Именованный тип</span><span class="sxs-lookup"><span data-stu-id="98d7f-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="98d7f-123">Именованная ссылка на тип-примитив, текстовое соглашение или тип с ограничением.</span><span class="sxs-lookup"><span data-stu-id="98d7f-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="98d7f-124">Тип с ограничениями</span><span class="sxs-lookup"><span data-stu-id="98d7f-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="98d7f-125">Тип-примитив, именованный тип или текстовое соглашение, ограниченное некоторыми механизмами подтипов, определенными в документах SMI RFC 1213 и RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="98d7f-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="98d7f-126">Тип-примитив</span><span class="sxs-lookup"><span data-stu-id="98d7f-126">Primitive Type</span></span>

<span data-ttu-id="98d7f-127">Тип-примитив является одним из основных типов данных, определенных в структуре документов по управлению данными (SMI) RFC 1213 и RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="98d7f-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="98d7f-128">Типы-примитивы SNMP сопоставляются с типами, определенными в CIM.</span><span class="sxs-lookup"><span data-stu-id="98d7f-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="98d7f-129">В следующей таблице приведено сопоставление, которое происходит, когда предложение СИНТАКСИСа явно ссылается на примитивный тип для.</span><span class="sxs-lookup"><span data-stu-id="98d7f-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="98d7f-130">Квалификаторы **текстового \_ соглашения**, **кодировки** и **\_ СИНТАКСИСа объектов** всегда совпадают с типом MIB, а значение по умолчанию всегда равно **null**.</span><span class="sxs-lookup"><span data-stu-id="98d7f-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="98d7f-131">Тип MIB</span><span class="sxs-lookup"><span data-stu-id="98d7f-131">MIB type</span></span>         | <span data-ttu-id="98d7f-132">Тип Variant CIM</span><span class="sxs-lookup"><span data-stu-id="98d7f-132">CIM variant type</span></span> | <span data-ttu-id="98d7f-133">значение Цимтипе</span><span class="sxs-lookup"><span data-stu-id="98d7f-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="98d7f-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="98d7f-134">INTEGER</span></span>          | <span data-ttu-id="98d7f-135">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-135">VT\_I4</span></span>           | <span data-ttu-id="98d7f-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-136">**sint32**</span></span>    |
| <span data-ttu-id="98d7f-137">октетстринг</span><span class="sxs-lookup"><span data-stu-id="98d7f-137">OCTETSTRING</span></span>      | <span data-ttu-id="98d7f-138">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-138">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-139">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-139">**string**</span></span>    |
| <span data-ttu-id="98d7f-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="98d7f-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="98d7f-141">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-141">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-142">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-142">**string**</span></span>    |
| <span data-ttu-id="98d7f-143">NULL</span><span class="sxs-lookup"><span data-stu-id="98d7f-143">NULL</span></span>             | <span data-ttu-id="98d7f-144">VT \_ null</span><span class="sxs-lookup"><span data-stu-id="98d7f-144">VT\_NULL</span></span>         | <span data-ttu-id="98d7f-145">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="98d7f-145">Not supported</span></span> |
| <span data-ttu-id="98d7f-146">IPAddress</span><span class="sxs-lookup"><span data-stu-id="98d7f-146">IpAddress</span></span>        | <span data-ttu-id="98d7f-147">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-147">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-148">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-148">**string**</span></span>    |
| <span data-ttu-id="98d7f-149">Счетчик</span><span class="sxs-lookup"><span data-stu-id="98d7f-149">Counter</span></span>          | <span data-ttu-id="98d7f-150">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-150">VT\_I4</span></span>           | <span data-ttu-id="98d7f-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-151">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-152">Датчик</span><span class="sxs-lookup"><span data-stu-id="98d7f-152">Gauge</span></span>            | <span data-ttu-id="98d7f-153">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-153">VT\_I4</span></span>           | <span data-ttu-id="98d7f-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-154">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-155">Значение TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="98d7f-155">TimeTicks</span></span>        | <span data-ttu-id="98d7f-156">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-156">VT\_I4</span></span>           | <span data-ttu-id="98d7f-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-157">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-158">Непрозрачный</span><span class="sxs-lookup"><span data-stu-id="98d7f-158">Opaque</span></span>           | <span data-ttu-id="98d7f-159">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-159">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-160">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-160">**string**</span></span>    |
| <span data-ttu-id="98d7f-161">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="98d7f-161">NetworkAddress</span></span>   | <span data-ttu-id="98d7f-162">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-162">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-163">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-163">**string**</span></span>    |



 

<span data-ttu-id="98d7f-164">Поставщик игнорирует Макрос OBJECT-TYPE, если предложение СИНТАКСИСа ссылается на **null** либо явно, либо с помощью присваивания именованного типа.</span><span class="sxs-lookup"><span data-stu-id="98d7f-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="98d7f-165">В следующей таблице приведено сопоставление, которое происходит, когда предложение СИНТАКСИСа явно ссылается на примитивный тип для SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="98d7f-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="98d7f-166">Квалификаторы **текстового \_ соглашения**, **кодировки** и **\_ СИНТАКСИСа объектов** всегда совпадают с типом MIB, а значение по умолчанию всегда равно **null**.</span><span class="sxs-lookup"><span data-stu-id="98d7f-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="98d7f-167">Тип MIB</span><span class="sxs-lookup"><span data-stu-id="98d7f-167">MIB type</span></span>          | <span data-ttu-id="98d7f-168">Тип Variant CIM</span><span class="sxs-lookup"><span data-stu-id="98d7f-168">CIM variant type</span></span> | <span data-ttu-id="98d7f-169">значение Цимтипе</span><span class="sxs-lookup"><span data-stu-id="98d7f-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="98d7f-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="98d7f-170">INTEGER</span></span>           | <span data-ttu-id="98d7f-171">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-171">VT\_I4</span></span>           | <span data-ttu-id="98d7f-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-172">**sint32**</span></span>    |
| <span data-ttu-id="98d7f-173">СТРОКА ОКТЕТА</span><span class="sxs-lookup"><span data-stu-id="98d7f-173">OCTET STRING</span></span>      | <span data-ttu-id="98d7f-174">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-174">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-175">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-175">**string**</span></span>    |
| <span data-ttu-id="98d7f-176">ИДЕНТИФИКАТОР ОБЪЕКТА</span><span class="sxs-lookup"><span data-stu-id="98d7f-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="98d7f-177">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-177">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-178">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-178">**string**</span></span>    |
| <span data-ttu-id="98d7f-179">IPAddress</span><span class="sxs-lookup"><span data-stu-id="98d7f-179">IpAddress</span></span>         | <span data-ttu-id="98d7f-180">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-180">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-181">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-181">**string**</span></span>    |
| <span data-ttu-id="98d7f-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="98d7f-182">Counter32</span></span>         | <span data-ttu-id="98d7f-183">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-183">VT\_I4</span></span>           | <span data-ttu-id="98d7f-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-184">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-185">Значение Gauge32</span><span class="sxs-lookup"><span data-stu-id="98d7f-185">Gauge32</span></span>           | <span data-ttu-id="98d7f-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-186">VT\_I4</span></span>           | <span data-ttu-id="98d7f-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-187">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="98d7f-188">Unsigned32</span></span>        | <span data-ttu-id="98d7f-189">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-189">VT\_I4</span></span>           | <span data-ttu-id="98d7f-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-190">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="98d7f-191">Integer32</span></span>         | <span data-ttu-id="98d7f-192">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-192">VT\_I4</span></span>           | <span data-ttu-id="98d7f-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-193">**sint32**</span></span>    |
| <span data-ttu-id="98d7f-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="98d7f-194">Counter64</span></span>         | <span data-ttu-id="98d7f-195">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-195">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="98d7f-196">**uint64**</span></span>    |
| <span data-ttu-id="98d7f-197">Значение TIMETICKS</span><span class="sxs-lookup"><span data-stu-id="98d7f-197">TimeTicks</span></span>         | <span data-ttu-id="98d7f-198">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="98d7f-198">VT\_I4</span></span>           | <span data-ttu-id="98d7f-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="98d7f-199">**uint32**</span></span>    |
| <span data-ttu-id="98d7f-200">Непрозрачный</span><span class="sxs-lookup"><span data-stu-id="98d7f-200">Opaque</span></span>            | <span data-ttu-id="98d7f-201">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-201">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-202">**string**</span><span class="sxs-lookup"><span data-stu-id="98d7f-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="98d7f-203">Именованный тип</span><span class="sxs-lookup"><span data-stu-id="98d7f-203">Named Type</span></span>

<span data-ttu-id="98d7f-204">Именованные типы SNMP сопоставляются с типами, определенными в CIM.</span><span class="sxs-lookup"><span data-stu-id="98d7f-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="98d7f-205">Если предложение СИНТАКСИСа ссылается на [тип-примитив](#primitive-type), [текстовое соглашение](textual-convention-macro.md)или [тип с ограничением](#constrained-type) по наследованию типа, используйте эти типы для определения того, какие процедуры сопоставления применяются.</span><span class="sxs-lookup"><span data-stu-id="98d7f-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="98d7f-206">Если, через наследование правил назначения типов, вы обнаружите определение типа с ограничением:</span><span class="sxs-lookup"><span data-stu-id="98d7f-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="98d7f-207">Кроме того, при последующем наследовании вы сталкиваетесь с одним из текстовых соглашений, перечисленных в [макросе ТЕКСТОВОГО соглашения](textual-convention-macro.md), а затем примените правила сопоставления для ограниченных типов и текстовых соглашений.</span><span class="sxs-lookup"><span data-stu-id="98d7f-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="98d7f-208">В противном случае при возникновении одного из типов-примитивов, перечисленных в таблице типов-примитивов, примените правила сопоставления для типов-примитивов и ограниченных типов.</span><span class="sxs-lookup"><span data-stu-id="98d7f-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="98d7f-209">Если вы сталкиваетесь с одним из текстовых соглашений, перечисленных в [ \_ макросе текстового](textual-convention-macro.md)соглашения, примените правила сопоставления для текстовых соглашений.</span><span class="sxs-lookup"><span data-stu-id="98d7f-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="98d7f-210">При возникновении одного из типов-примитивов, перечисленных в таблице типов-примитивов, примените правила сопоставления для типов-примитивов.</span><span class="sxs-lookup"><span data-stu-id="98d7f-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="98d7f-211">Классы, содержащие типы свойств, которые не соответствуют приведенным выше сопоставлениям, недопустимы.</span><span class="sxs-lookup"><span data-stu-id="98d7f-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="98d7f-212">В этом случае поставщик возвращает ошибку, если и когда поставщик запрашивает получение определения класса во время выполнения функции получения экземпляра.</span><span class="sxs-lookup"><span data-stu-id="98d7f-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="98d7f-213">Тип с ограничениями</span><span class="sxs-lookup"><span data-stu-id="98d7f-213">Constrained Type</span></span>

<span data-ttu-id="98d7f-214">Тип с ограничением — это примитивный тип, именованный тип или текстовое соглашение, ограниченное некоторыми механизмами поднабора, определенными в документах SMI RFC 1213 и RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="98d7f-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="98d7f-215">При вводе подтипа требуются дополнительные квалификаторы CIM для указания значений подтипов.</span><span class="sxs-lookup"><span data-stu-id="98d7f-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="98d7f-216">Определение именованного типа в предложении СИНТАКСИСа непосредственно сопоставляет **\_ синтаксис объекта** квалификатора свойства CIM, но не включает ограничения подтипа.</span><span class="sxs-lookup"><span data-stu-id="98d7f-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="98d7f-217">Подтипы могут следовать любому из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="98d7f-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="98d7f-218">ЦЕЛОе число с перечислением</span><span class="sxs-lookup"><span data-stu-id="98d7f-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="98d7f-219">В **перечислении** квалификаторов свойств CIM указываются перечисляемые значения.</span><span class="sxs-lookup"><span data-stu-id="98d7f-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="98d7f-220">Этот квалификатор представлен в виде строки, содержащей разделенный запятыми список 32-разрядных целых чисел со знаком.</span><span class="sxs-lookup"><span data-stu-id="98d7f-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="98d7f-221">В следующей таблице перечислены типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="98d7f-221">The following table lists the mapping types.</span></span> <span data-ttu-id="98d7f-222">Значение по умолчанию всегда равно **null**.</span><span class="sxs-lookup"><span data-stu-id="98d7f-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="98d7f-223">Ограниченный тип MIB</span><span class="sxs-lookup"><span data-stu-id="98d7f-223">Constrained MIB type</span></span> | <span data-ttu-id="98d7f-224">Тип Variant CIM</span><span class="sxs-lookup"><span data-stu-id="98d7f-224">CIM variant type</span></span> | <span data-ttu-id="98d7f-225">Квалификаторы CIM</span><span class="sxs-lookup"><span data-stu-id="98d7f-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d7f-226">ЦЕЛОе число с перечислением</span><span class="sxs-lookup"><span data-stu-id="98d7f-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="98d7f-227">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="98d7f-227">VT\_BSTR</span></span>         | <span data-ttu-id="98d7f-228">**текстовое \_ соглашение**: енумератединтежер</span><span class="sxs-lookup"><span data-stu-id="98d7f-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="98d7f-229">**Кодировка**: целое число</span><span class="sxs-lookup"><span data-stu-id="98d7f-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="98d7f-230">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="98d7f-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="98d7f-231">BITS</span><span class="sxs-lookup"><span data-stu-id="98d7f-231">BITS</span></span>

    <span data-ttu-id="98d7f-232">**Биты** квалификатора свойства CIM определяют перечисляемые значения.</span><span class="sxs-lookup"><span data-stu-id="98d7f-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="98d7f-233">Этот квалификатор представлен в виде строки, содержащей разделенный запятыми список 32-разрядных целых чисел со знаком.</span><span class="sxs-lookup"><span data-stu-id="98d7f-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="98d7f-234">В следующей таблице перечислены типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="98d7f-234">The following table lists the mapping types.</span></span> <span data-ttu-id="98d7f-235">Значение по умолчанию всегда равно **null**.</span><span class="sxs-lookup"><span data-stu-id="98d7f-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="98d7f-236">Ограниченный тип MIB</span><span class="sxs-lookup"><span data-stu-id="98d7f-236">Constrained MIB type</span></span> | <span data-ttu-id="98d7f-237">Тип Variant CIM</span><span class="sxs-lookup"><span data-stu-id="98d7f-237">CIM variant type</span></span>      | <span data-ttu-id="98d7f-238">Квалификаторы CIM</span><span class="sxs-lookup"><span data-stu-id="98d7f-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d7f-239">BITS</span><span class="sxs-lookup"><span data-stu-id="98d7f-239">BITS</span></span>                 | <span data-ttu-id="98d7f-240">VT \_ массив \| VT \_</span><span class="sxs-lookup"><span data-stu-id="98d7f-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="98d7f-241">**текстовое \_ соглашение**: BITS</span><span class="sxs-lookup"><span data-stu-id="98d7f-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="98d7f-242">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="98d7f-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="98d7f-243">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="98d7f-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="98d7f-244">Переменная длина</span><span class="sxs-lookup"><span data-stu-id="98d7f-244">Variable-length</span></span>

    <span data-ttu-id="98d7f-245">Если предложение СИНТАКСИСа ссылается на тип-примитив, именованный тип или текстовое соглашение, которое поддается подтипу в виде строки ОКТЕТа переменной длины или непрозрачности, **переменная \_** квалификатора свойства CIM определяет минимальное, максимальное и фиксированное значения длины, связанные с определением типа.</span><span class="sxs-lookup"><span data-stu-id="98d7f-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="98d7f-246">Этот квалификатор реализуется в виде строки в следующем формате, где значения переменной длины представляются как 32-разрядные целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="98d7f-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="98d7f-247">Фиксированная длина</span><span class="sxs-lookup"><span data-stu-id="98d7f-247">Fixed-length</span></span>

    <span data-ttu-id="98d7f-248">Если предложение СИНТАКСИСа ссылается на тип-примитив, именованный тип или текстовое соглашение, которое подписывается как строка ОКТЕТа фиксированной длины или непрозрачность, **фиксированная \_ Длина** квалификатора свойства CIM указывает значение фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="98d7f-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="98d7f-249">Этот квалификатор представляется как 32-разрядное целочисленное значение без знака.</span><span class="sxs-lookup"><span data-stu-id="98d7f-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="98d7f-250">Диапазон</span><span class="sxs-lookup"><span data-stu-id="98d7f-250">Range</span></span>

    <span data-ttu-id="98d7f-251">Если предложение СИНТАКСИСа ссылается на тип-примитив, именованный тип или текстовое соглашение, которое подписывается в виде ЦЕЛОго числа или датчика с фиксированным значением или типа, то **\_ значение переменной** квалификатора свойства CIM указывает диапазон и фиксированные значения, связанные с определением типа.</span><span class="sxs-lookup"><span data-stu-id="98d7f-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="98d7f-252">Этот квалификатор реализуется в виде строки в следующем формате, где значения диапазона и фиксированной длины представляются как 32-разрядные целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="98d7f-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="98d7f-253">Пример кода</span><span class="sxs-lookup"><span data-stu-id="98d7f-253">Example Code</span></span>

<span data-ttu-id="98d7f-254">В следующем примере описывается подтип перечислимого ЦЕЛОго числа.</span><span class="sxs-lookup"><span data-stu-id="98d7f-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="98d7f-255">В этом примере сопоставляется:</span><span class="sxs-lookup"><span data-stu-id="98d7f-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="98d7f-256">В следующем примере кода описывается подтип BITS.</span><span class="sxs-lookup"><span data-stu-id="98d7f-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="98d7f-257">Следующий пример кода сопоставляется с:</span><span class="sxs-lookup"><span data-stu-id="98d7f-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="98d7f-258">В следующем примере кода описывается подтип переменной длины.</span><span class="sxs-lookup"><span data-stu-id="98d7f-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="98d7f-259">В этом примере сопоставляется:</span><span class="sxs-lookup"><span data-stu-id="98d7f-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="98d7f-260">В следующем примере описывается подтип фиксированной длины.</span><span class="sxs-lookup"><span data-stu-id="98d7f-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="98d7f-261">В этом примере сопоставляется:</span><span class="sxs-lookup"><span data-stu-id="98d7f-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="98d7f-262">В следующем примере описывается подтип диапазона.</span><span class="sxs-lookup"><span data-stu-id="98d7f-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="98d7f-263">В этом примере сопоставляется:</span><span class="sxs-lookup"><span data-stu-id="98d7f-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 




