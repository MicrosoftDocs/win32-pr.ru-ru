---
description: Текстовые соглашения SNMP сопоставляются с типами, определенными в CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Макрос ТЕКСТОВОГО соглашения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701937"
---
# <a name="textual-convention-macro"></a><span data-ttu-id="2f99e-103">Макрос ТЕКСТОВОГО соглашения</span><span class="sxs-lookup"><span data-stu-id="2f99e-103">TEXTUAL-CONVENTION Macro</span></span>

<span data-ttu-id="2f99e-104">Текстовые соглашения SNMP сопоставляются с типами, определенными в CIM.</span><span class="sxs-lookup"><span data-stu-id="2f99e-104">SNMP textual conventions map to CIM-defined types.</span></span>

> [!Note]  
> <span data-ttu-id="2f99e-105">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2f99e-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="2f99e-106">Следующие правила сопоставления применяются к текстовым соглашениям SNMP:</span><span class="sxs-lookup"><span data-stu-id="2f99e-106">The following mapping rules apply to SNMP textual conventions:</span></span>

-   <span data-ttu-id="2f99e-107">Определение именованного типа в предложении СИНТАКСИСа преобразуется в **\_ синтаксис объекта** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="2f99e-107">The named type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax**.</span></span>
-   <span data-ttu-id="2f99e-108">Используйте следующую таблицу для отображения текстовых соглашений, если предложение СИНТАКСИСа явно ссылается на текстовое обозначение макроса ТЕКСТОВОГО соглашения SNMPv2C или относится к подразумеваемому текстовому правилу.</span><span class="sxs-lookup"><span data-stu-id="2f99e-108">Use the following table to map textual conventions when the SYNTAX clause explicitly refers to a textual convention of a SNMPv2C TEXTUAL-CONVENTION macro, or refers to an implied textual convention.</span></span> <span data-ttu-id="2f99e-109">Значение по умолчанию всегда равно **null**.</span><span class="sxs-lookup"><span data-stu-id="2f99e-109">The default value is always **NULL**.</span></span>



| <span data-ttu-id="2f99e-110">Текстовое соглашение</span><span class="sxs-lookup"><span data-stu-id="2f99e-110">Textual convention</span></span> | <span data-ttu-id="2f99e-111">Тип Variant CIM</span><span class="sxs-lookup"><span data-stu-id="2f99e-111">CIM variant type</span></span> | <span data-ttu-id="2f99e-112">Квалификатор CIM</span><span class="sxs-lookup"><span data-stu-id="2f99e-112">CIM qualifier</span></span>                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f99e-113">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="2f99e-113">DateAndTime</span></span>        | <span data-ttu-id="2f99e-114">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-114">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-115">**текстовое \_ соглашение**: датеандтиме</span><span class="sxs-lookup"><span data-stu-id="2f99e-115">**textual\_convention**: DateAndTime</span></span><br/> <span data-ttu-id="2f99e-116">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-116">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-117">**\_ синтаксис объекта**: датеандтиме</span><span class="sxs-lookup"><span data-stu-id="2f99e-117">**object\_syntax**: DateAndTime</span></span><br/> <span data-ttu-id="2f99e-118">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-118">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="2f99e-119">Строку</span><span class="sxs-lookup"><span data-stu-id="2f99e-119">Displaystring</span></span>      | <span data-ttu-id="2f99e-120">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-120">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-121">**текстовое \_ соглашение**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="2f99e-121">**textual\_convention**: Displaystring</span></span><br/> <span data-ttu-id="2f99e-122">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-122">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-123">**\_ синтаксис объекта**: DisplayString</span><span class="sxs-lookup"><span data-stu-id="2f99e-123">**object\_syntax**: Displaystring</span></span><br/> <span data-ttu-id="2f99e-124">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-124">**cimtype**: string</span></span><br/>   |
| <span data-ttu-id="2f99e-125">MacAddress</span><span class="sxs-lookup"><span data-stu-id="2f99e-125">MacAddress</span></span>         | <span data-ttu-id="2f99e-126">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-126">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-127">**текстовое \_ соглашение**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="2f99e-127">**textual\_convention**: MacAddress</span></span><br/> <span data-ttu-id="2f99e-128">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-128">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-129">**\_ синтаксис объекта**: MacAddress</span><span class="sxs-lookup"><span data-stu-id="2f99e-129">**object\_syntax**: MacAddress</span></span><br/> <span data-ttu-id="2f99e-130">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-130">**cimtype**: string</span></span><br/>         |
| <span data-ttu-id="2f99e-131">фисаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-131">PhysAddress</span></span>        | <span data-ttu-id="2f99e-132">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-132">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-133">**текстовое \_ соглашение**: фисаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-133">**textual\_convention**: PhysAddress</span></span><br/> <span data-ttu-id="2f99e-134">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-134">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-135">**\_ синтаксис объекта**: фисаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-135">**object\_syntax**: PhysAddress</span></span><br/> <span data-ttu-id="2f99e-136">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-136">**cimtype**: string</span></span><br/>       |
| <span data-ttu-id="2f99e-137">снмпудпаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-137">SnmpUDPAddress</span></span>     | <span data-ttu-id="2f99e-138">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-138">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-139">**текстовое \_ соглашение**: снмпудпаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-139">**textual\_convention**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="2f99e-140">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-140">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-141">**\_ синтаксис объекта**: снмпудпаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-141">**object\_syntax**: SnmpUDPAddress</span></span><br/> <span data-ttu-id="2f99e-142">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-142">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="2f99e-143">снмпосиаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-143">SnmpOSIAddress</span></span>     | <span data-ttu-id="2f99e-144">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-144">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-145">**текстовое \_ соглашение**: снмпосиаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-145">**textual\_convention**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="2f99e-146">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-146">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-147">**\_ синтаксис объекта**: снмпосиаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-147">**object\_syntax**: SnmpOSIAddress</span></span><br/> <span data-ttu-id="2f99e-148">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-148">**cimtype**: string</span></span><br/> |
| <span data-ttu-id="2f99e-149">снмпипксаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-149">SnmpIPXAddress</span></span>     | <span data-ttu-id="2f99e-150">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="2f99e-150">**VT\_BSTR**</span></span>     | <span data-ttu-id="2f99e-151">**текстовое \_ соглашение**: снмпипксаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-151">**textual\_convention**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="2f99e-152">**Кодировка**: октетстринг</span><span class="sxs-lookup"><span data-stu-id="2f99e-152">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="2f99e-153">**\_ синтаксис объекта**: снмпипксаддресс</span><span class="sxs-lookup"><span data-stu-id="2f99e-153">**object\_syntax**: SnmpIPXAddress</span></span><br/> <span data-ttu-id="2f99e-154">**Цимтипе**: строка</span><span class="sxs-lookup"><span data-stu-id="2f99e-154">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="2f99e-155">Тип Variant, определенный CIM, и **текстовое \_ соглашение** квалификаторов свойств CIM, **Кодировка**, **\_ синтаксис объекта** и схема **Цимтипе** с использованием базового типа-примитива.</span><span class="sxs-lookup"><span data-stu-id="2f99e-155">The CIM-defined variant type and the CIM property qualifiers **textual\_convention**, **encoding**, **object\_syntax**, and **cimtype** map using the underlying primitive type.</span></span>
-   <span data-ttu-id="2f99e-156">Предложение по ОТОБРАЖЕНию подсказки в ТЕКСТОВОМ СОГЛАШЕНИи SNMPv2C сопоставляется непосредственно с **\_ подсказкой** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="2f99e-156">The DISPLAY-HINT clause of the SNMPv2C TEXTUAL-CONVENTION macro maps verbatim to the CIM property qualifier **display\_hint**.</span></span> <span data-ttu-id="2f99e-157">Этот квалификатор не создается, если не существует макроса с ТЕКСТОВым СОГЛАШЕНИЕм или макрос не содержит предложение подсказки для вывода.</span><span class="sxs-lookup"><span data-stu-id="2f99e-157">This qualifier is not generated if there is no TEXTUAL-CONVENTION macro, or the macro does not contain a DISPLAY-HINT clause.</span></span>

## <a name="example-code"></a><span data-ttu-id="2f99e-158">Пример кода</span><span class="sxs-lookup"><span data-stu-id="2f99e-158">Example Code</span></span>

<span data-ttu-id="2f99e-159">В следующем примере описывается текстовое соглашение о стандарте в стандарте.</span><span class="sxs-lookup"><span data-stu-id="2f99e-159">The following example describes an SNMPv1 textual convention.</span></span>

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

<span data-ttu-id="2f99e-160">В этом примере создаются следующие квалификаторы CIM.</span><span class="sxs-lookup"><span data-stu-id="2f99e-160">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

<span data-ttu-id="2f99e-161">В следующем примере описывается текстовое соглашение SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="2f99e-161">The following example describes an SNMPv2 textual convention.</span></span>

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

<span data-ttu-id="2f99e-162">В этом примере создаются следующие квалификаторы CIM.</span><span class="sxs-lookup"><span data-stu-id="2f99e-162">This example generates the following CIM qualifiers.</span></span>

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




