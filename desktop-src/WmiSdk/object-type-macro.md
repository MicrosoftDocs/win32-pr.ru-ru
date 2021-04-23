---
description: Макрос OBJECT-TYPE содержит обязательные и необязательные предложения, описывающие основные характеристики объекта MIB. Поставщик SNMP преобразует MIB в соответствующие части макроса типа OBJECT-TYPE.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Макрос типа OBJECT-TYPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143393"
---
# <a name="object-type-macro"></a><span data-ttu-id="a0a61-104">Макрос типа OBJECT-TYPE</span><span class="sxs-lookup"><span data-stu-id="a0a61-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="a0a61-105">Макрос OBJECT-TYPE содержит обязательные и необязательные предложения, описывающие основные характеристики объекта MIB.</span><span class="sxs-lookup"><span data-stu-id="a0a61-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="a0a61-106">Поставщик SNMP преобразует MIB в соответствующие части макроса типа OBJECT-TYPE.</span><span class="sxs-lookup"><span data-stu-id="a0a61-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="a0a61-107">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a0a61-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="a0a61-108">Компоненты</span><span class="sxs-lookup"><span data-stu-id="a0a61-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="a0a61-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Объект MIB</span><span class="sxs-lookup"><span data-stu-id="a0a61-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-110">Объект, который содержит большую часть рассматриваемых данных.</span><span class="sxs-lookup"><span data-stu-id="a0a61-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Дескриптор объекта</span><span class="sxs-lookup"><span data-stu-id="a0a61-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-112">Уникальное имя или дескриптор объекта, определяющие каждый объект MIB.</span><span class="sxs-lookup"><span data-stu-id="a0a61-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="a0a61-113">Каждый дескриптор объекта MIB полностью сопоставляется с именем свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="a0a61-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="a0a61-114">Например, **ifIndex** преобразуется в **ifIndex**.</span><span class="sxs-lookup"><span data-stu-id="a0a61-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Предложение СИНТАКСИСа](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="a0a61-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-116">Определяет данные и тип объекта MIB.</span><span class="sxs-lookup"><span data-stu-id="a0a61-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Предложение INDEX](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="a0a61-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-118">Определяет ключ для выбора уникальной строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="a0a61-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Предложение дополнения</span><span class="sxs-lookup"><span data-stu-id="a0a61-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-120">Указывает, что указанная коллекция таблиц может считаться расширением другой коллекции таблиц и может заменить предложение INDEX в SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="a0a61-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="a0a61-121">Коллекции, на которые ссылается предложение дополнения, можно сочетать с другой коллекцией таблиц для формирования одной коллекции.</span><span class="sxs-lookup"><span data-stu-id="a0a61-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="a0a61-122">Результирующая коллекция использует свойства первичного ключа, заданные в последней коллекции таблиц в цепочке.</span><span class="sxs-lookup"><span data-stu-id="a0a61-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="a0a61-123">В этом случае предыдущие правила сопоставления, заданные для предложения INDEX, применяются к последней коллекции таблиц в цепочке.</span><span class="sxs-lookup"><span data-stu-id="a0a61-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="a0a61-124">Затем Коллекция объектов сопоставляется с одним определением класса CIM.</span><span class="sxs-lookup"><span data-stu-id="a0a61-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT — предложение IDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="a0a61-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-126">Содержит уникальный идентификатор объекта для объекта MIB.</span><span class="sxs-lookup"><span data-stu-id="a0a61-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="a0a61-127">Этот идентификатор объекта сопоставляется с **\_ идентификатором объекта** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="a0a61-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Предложения доступа и MAX-ACCESS](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="a0a61-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-129">Определите права доступа к объекту MIB.</span><span class="sxs-lookup"><span data-stu-id="a0a61-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Предложение DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a0a61-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-131">Предоставляет текстовое описание объекта, которое сопоставляется с **описанием** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="a0a61-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="a0a61-132">Это предложение может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="a0a61-132">This clause may be empty.</span></span>

<span data-ttu-id="a0a61-133">Каждая **Таблица** и объект **записи** в определении таблицы SNMP также содержат предложение Description, которое также может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="a0a61-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="a0a61-134">Предложения "Таблица" и "Описание записи" объединяются, а результат сопоставляется с **описанием** квалификатора класса CIM.</span><span class="sxs-lookup"><span data-stu-id="a0a61-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Предложение STATUS</span><span class="sxs-lookup"><span data-stu-id="a0a61-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-136">Указывает, должен ли быть поддерживаемый объект.</span><span class="sxs-lookup"><span data-stu-id="a0a61-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="a0a61-137">Если значение предложения STATUS **устарело**, поставщик отклоняет объект MIB из сопоставления.</span><span class="sxs-lookup"><span data-stu-id="a0a61-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="a0a61-138">В противном случае предложение STATUS сопоставляется с **состоянием** квалификатора свойства CIM.</span><span class="sxs-lookup"><span data-stu-id="a0a61-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="a0a61-139">Для версии в версии, предпочтительным **является либо** обязательное, либо **необязательное**, но квалификатор может содержать какое **-либо другое** значение.</span><span class="sxs-lookup"><span data-stu-id="a0a61-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="a0a61-140">Для SNMPv2C предпочтительным значением **Status** является **Current** или **устарело**, но квалификатор может содержать какое-либо другое значение.</span><span class="sxs-lookup"><span data-stu-id="a0a61-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Предложение ДЕФВАЛ</span><span class="sxs-lookup"><span data-stu-id="a0a61-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-142">Присваивает значение по умолчанию переменной в строке логической таблицы и сопоставляется со строкой квалификатора свойства CIM **дефвал**.</span><span class="sxs-lookup"><span data-stu-id="a0a61-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Предложение REFERENCE</span><span class="sxs-lookup"><span data-stu-id="a0a61-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-144">Ссылается на другой документ, содержащий дополнительные сведения об объекте.</span><span class="sxs-lookup"><span data-stu-id="a0a61-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="a0a61-145">Это предложение сопоставляется со **ссылкой** на КВАЛИФИКАТОР свойства CIM, которая относится к типу String.</span><span class="sxs-lookup"><span data-stu-id="a0a61-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="a0a61-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Предложение UNITs</span><span class="sxs-lookup"><span data-stu-id="a0a61-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="a0a61-147">Предоставляет точное определение того, что представляет объект.</span><span class="sxs-lookup"><span data-stu-id="a0a61-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="a0a61-148">Это предложение соответствует **единицам** квалификатора свойства CIM, которые имеют тип String.</span><span class="sxs-lookup"><span data-stu-id="a0a61-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0a61-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0a61-149">Remarks</span></span>

<span data-ttu-id="a0a61-150">Макрос OBJECT-TYPE описывает основные характеристики отдельного объекта MIB.</span><span class="sxs-lookup"><span data-stu-id="a0a61-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="a0a61-151">Набор макросов типа OBJECT можно рассматривать как группу связанных объектов.</span><span class="sxs-lookup"><span data-stu-id="a0a61-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="a0a61-152">В SNMPv2C используйте макрос OBJECT-GROUP, чтобы формально сгруппировать наборы связанных объектов в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="a0a61-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="a0a61-153">Однако для создания коллекций в настоящее время не существует формального механизма.</span><span class="sxs-lookup"><span data-stu-id="a0a61-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="a0a61-154">В целях поставщика SNMP макрос группы объектов игнорируется, но вы можете создавать связи группирования и создавать коллекции.</span><span class="sxs-lookup"><span data-stu-id="a0a61-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 



