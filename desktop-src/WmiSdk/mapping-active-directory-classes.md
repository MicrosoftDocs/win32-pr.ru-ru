---
description: Содержит правила сопоставления классов WMI с Active Directory.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Сопоставление классов Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712337"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="0dcea-103">Сопоставление классов Active Directory</span><span class="sxs-lookup"><span data-stu-id="0dcea-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="0dcea-104">Поскольку Active Directory имеет широкий спектр возможных объектов, Инструментарий WMI не может создать прямое сопоставление «один к одному».</span><span class="sxs-lookup"><span data-stu-id="0dcea-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="0dcea-105">Вместо этого поставщик служб каталогов использует правила для сопоставления классов между двумя технологиями.</span><span class="sxs-lookup"><span data-stu-id="0dcea-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="0dcea-106">В этом разделе рассматриваются следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="0dcea-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="0dcea-107">Классы сопоставления</span><span class="sxs-lookup"><span data-stu-id="0dcea-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="0dcea-108">Сопоставление атрибутов</span><span class="sxs-lookup"><span data-stu-id="0dcea-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="0dcea-109">Классы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="0dcea-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="0dcea-110">Дополнительные сведения о поддержке и установке этого компонента в определенной операционной системе см. в статье [доступность компонентов WMI в операционной системе](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="0dcea-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="0dcea-111">Классы сопоставления</span><span class="sxs-lookup"><span data-stu-id="0dcea-111">Mapping Classes</span></span>

<span data-ttu-id="0dcea-112">В следующем списке описываются рекомендации, которые поставщик служб каталогов использует для соответствия классов Active Directory классам WMI:</span><span class="sxs-lookup"><span data-stu-id="0dcea-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="0dcea-113">Каждый абстрактный класс в схеме Active Directory сопоставляется с одним абстрактным классом в схеме WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="0dcea-114">В схеме WMI каждый абстрактный класс имеет префикс DS \_ .</span><span class="sxs-lookup"><span data-stu-id="0dcea-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="0dcea-115">Например, класс **Person** из схемы Active Directory сопоставляется с классом WMI **\_ Person лица DS** .</span><span class="sxs-lookup"><span data-stu-id="0dcea-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="0dcea-116">Каждый неабстрактный класс из схемы Active Directory сопоставляется со следующими двумя классами в схеме WMI:</span><span class="sxs-lookup"><span data-stu-id="0dcea-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="0dcea-117">Первый сопоставленный класс имеет префикс ADS \_ .</span><span class="sxs-lookup"><span data-stu-id="0dcea-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="0dcea-118">Это абстрактные классы, которые сопоставляются в соответствии с приведенными ниже правилами.</span><span class="sxs-lookup"><span data-stu-id="0dcea-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="0dcea-119">Второй сопоставленный класс является неабстрактным классом с \_ префиксом имени DS.</span><span class="sxs-lookup"><span data-stu-id="0dcea-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="0dcea-120">Этот класс является производным от \_ абстрактного класса ADS с добавлением квалификатора [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="0dcea-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="0dcea-121">Например, класс **User** из схемы Active Directory сопоставляется с двумя классами.</span><span class="sxs-lookup"><span data-stu-id="0dcea-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="0dcea-122">Первым классом является абстрактный класс **ADS \_** , сопоставленный в соответствии с правилами ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="0dcea-123">Второй класс является неабстрактным классом **\_ пользователя DS** .</span><span class="sxs-lookup"><span data-stu-id="0dcea-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="0dcea-124">Он является производным **от \_ пользователя ADS** и имеет добавленный квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="0dcea-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="0dcea-125">Если не указано иное, имя сопоставленного класса является искаженным значением свойства **LDAP-отображаемое имя** в классе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0dcea-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="0dcea-126">Если в классе Active Directory имеется свойство **подкласса** , то сопоставленный WMI класс является производным от указанного класса.</span><span class="sxs-lookup"><span data-stu-id="0dcea-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="0dcea-127">Если свойство **подкласса** не задано, то сопоставляемый WMI класс является производным от класса **\_ \_ корневого \_ класса DS LDAP** , как указано в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="0dcea-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="0dcea-128">Этот класс имеет свойство ключа **адсипас** с типом **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="0dcea-129">Это уникальный путь ADSI, идентифицирующий этот экземпляр.</span><span class="sxs-lookup"><span data-stu-id="0dcea-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="0dcea-130">Active Directory поддерживает только одно наследование, поэтому это работает.</span><span class="sxs-lookup"><span data-stu-id="0dcea-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="0dcea-131">Для каждого класса создается **динамический** квалификатор типа **VT \_ bool**, а флаг Set имеет значение `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` **true** .</span><span class="sxs-lookup"><span data-stu-id="0dcea-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="0dcea-132">Это Стандартный квалификатор WMI, указывающий, что экземпляры этого класса предоставляются динамически.</span><span class="sxs-lookup"><span data-stu-id="0dcea-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="0dcea-133">Если класс не является абстрактным, поставщик создает квалификатор [**поставщика**](/windows/desktop/api/Provider/nl-provider-provider) типа " **VT \_ BSTR bool** " и флаг квалификатора `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` "поставщик экземпляра DS" для каждого класса.</span><span class="sxs-lookup"><span data-stu-id="0dcea-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="0dcea-134">Это Стандартный квалификатор WMI, указывающий имя поставщика, динамически предоставляющее экземпляры этого класса.</span><span class="sxs-lookup"><span data-stu-id="0dcea-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="0dcea-135">Остальные свойства ADSI сопоставляются с квалификаторами и свойствами класса в соответствии со следующими таблицами.</span><span class="sxs-lookup"><span data-stu-id="0dcea-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="0dcea-136">Все квалификаторы сопоставляются со значением флага квалификатора `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .</span><span class="sxs-lookup"><span data-stu-id="0dcea-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="0dcea-137">Ниже перечислены сведения о сопоставлении для класса Active Directory, в котором показаны квалификатор WMI и тип квалификатора WMI для каждого свойства Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0dcea-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="0dcea-138">**Common-Name**</span><span class="sxs-lookup"><span data-stu-id="0dcea-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-139">**CN** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0dcea-140">Сопоставляется непосредственно со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="0dcea-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-141">**По умолчанию — объект — Категория**</span><span class="sxs-lookup"><span data-stu-id="0dcea-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-142">**Дефаултобжекткатегори** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0dcea-143">Сопоставляется непосредственно со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="0dcea-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-144">**Дескриптор безопасности по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="0dcea-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-145">**Дефаултсекуритидескриптор** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0dcea-146">Сопоставляется непосредственно со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="0dcea-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-147">**Идентификатор, управляющий**</span><span class="sxs-lookup"><span data-stu-id="0dcea-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-148">**GovernsId** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0dcea-149">Сопоставляется из строкового представления OID; Например, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="0dcea-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-150">**Объектный класс**</span><span class="sxs-lookup"><span data-stu-id="0dcea-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-151">Н/Д</span><span class="sxs-lookup"><span data-stu-id="0dcea-151">N/A</span></span>

<span data-ttu-id="0dcea-152">Не сопоставлено.</span><span class="sxs-lookup"><span data-stu-id="0dcea-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-153">**Объект-класс-категория**</span><span class="sxs-lookup"><span data-stu-id="0dcea-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-154">**ObjectClassCategory** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="0dcea-155">Сопоставляется непосредственно с целочисленным значением.</span><span class="sxs-lookup"><span data-stu-id="0dcea-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="0dcea-156">Кроме того, если значение является абстрактным (2), то также создается стандартный квалификатор CIM **\_ логического типа VT** , называемый **"абстрактным"** квалификатором.</span><span class="sxs-lookup"><span data-stu-id="0dcea-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-157">**RDN-АТРИ-ID**</span><span class="sxs-lookup"><span data-stu-id="0dcea-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-158">**рднаттид** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="0dcea-159">Сопоставляется из строкового представления значения OID; Например, "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="0dcea-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="0dcea-160">Кроме того, указанное здесь свойство помечено как стандартный **индексированный** квалификатор CIM со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-161">**Только система**</span><span class="sxs-lookup"><span data-stu-id="0dcea-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-162">**Системонли** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="0dcea-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="0dcea-163">Сопоставляется непосредственно с логическим значением.</span><span class="sxs-lookup"><span data-stu-id="0dcea-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="0dcea-164">Ниже перечислены свойства класса Active Directory, сопоставленные со свойствами класса WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="0dcea-165">**Может содержать**</span><span class="sxs-lookup"><span data-stu-id="0dcea-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-166">Каждое свойство в этом списке сопоставляется со свойством WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-167">**Должен содержать**</span><span class="sxs-lookup"><span data-stu-id="0dcea-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-168">Каждое свойство в этом списке сопоставляется со свойством WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="0dcea-169">Для каждого из них создается стандартный квалификатор CIM, **отличный от \_ null** .</span><span class="sxs-lookup"><span data-stu-id="0dcea-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-170">**System — может содержать**</span><span class="sxs-lookup"><span data-stu-id="0dcea-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-171">Каждое свойство в этом списке сопоставляется со свойством WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="0dcea-172">Кроме того, каждое свойство дополняется квалификатором **системы** и устанавливается в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0dcea-173">**System — должно содержать**</span><span class="sxs-lookup"><span data-stu-id="0dcea-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="0dcea-174">Каждое свойство в этом списке сопоставляется со свойством WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="0dcea-175">Для каждого из них создается стандартный квалификатор CIM, **отличный от \_ null** .</span><span class="sxs-lookup"><span data-stu-id="0dcea-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="0dcea-176">Кроме того, каждое свойство дополняется квалификатором **системы** и устанавливается в **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="0dcea-177">Сопоставление атрибутов</span><span class="sxs-lookup"><span data-stu-id="0dcea-177">Mapping Attributes</span></span>

<span data-ttu-id="0dcea-178">Поставщик служб каталогов сопоставляет каждый атрибут класса Active Directory только с одним свойством соответствующего класса WMI в соответствии с правилами в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0dcea-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="0dcea-179">Как правило, поставщик служб каталогов именует свойство WMI как искаженную версию значения **LDAP-отображаемого имени** атрибута Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0dcea-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="0dcea-180">Если Active Directory свойство **имеет** **значение false**, то это свойство WMI объединяется с оператором или с **\_ \_ массивом флагов CIM**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="0dcea-181">Обратите внимание, что каждое свойство помечено квалификатором **VT \_ BSTR** , **адсинтакс**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="0dcea-182">Он представляет базовый синтаксис Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0dcea-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="0dcea-183">В следующей таблице приведено сопоставление синтаксиса Active Directory с типом данных свойства WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="0dcea-184">Active Directory, элемент</span><span class="sxs-lookup"><span data-stu-id="0dcea-184">Active Directory element</span></span>                                      | <span data-ttu-id="0dcea-185">Тип данных WMI</span><span class="sxs-lookup"><span data-stu-id="0dcea-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="0dcea-186">**Точка доступа**</span><span class="sxs-lookup"><span data-stu-id="0dcea-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="0dcea-187">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0dcea-188">**Логическая**</span><span class="sxs-lookup"><span data-stu-id="0dcea-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="0dcea-189">**\_логическое значение CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="0dcea-190">**Строка без учета регистра**</span><span class="sxs-lookup"><span data-stu-id="0dcea-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="0dcea-191">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0dcea-192">**Строка с учетом регистра**</span><span class="sxs-lookup"><span data-stu-id="0dcea-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="0dcea-193">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0dcea-194">**Различающееся имя**</span><span class="sxs-lookup"><span data-stu-id="0dcea-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="0dcea-195">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0dcea-196">**DN — двоичные данные**</span><span class="sxs-lookup"><span data-stu-id="0dcea-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="0dcea-197">Внедренный объект класса **DN \_ с \_ двоичными данными** , определенными ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="0dcea-198">**DN-строка**</span><span class="sxs-lookup"><span data-stu-id="0dcea-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="0dcea-199">Внедренный объект класса **DN \_ со \_ строкой** , определенной ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="0dcea-200">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="0dcea-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="0dcea-201">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="0dcea-202">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="0dcea-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="0dcea-203">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="0dcea-204">**Целочисленный тип**</span><span class="sxs-lookup"><span data-stu-id="0dcea-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="0dcea-205">**\_SINT32 CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="0dcea-206">**ларжеинтежер**</span><span class="sxs-lookup"><span data-stu-id="0dcea-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="0dcea-207">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0dcea-208">Дескриптор безопасности</span><span class="sxs-lookup"><span data-stu-id="0dcea-208">Security Descriptor</span></span>                                           | <span data-ttu-id="0dcea-209">Внедренный объект класса **Uint8Array** , определенный ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0dcea-210">Числовая строка</span><span class="sxs-lookup"><span data-stu-id="0dcea-210">Numeric String</span></span>                                                | <span data-ttu-id="0dcea-211">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0dcea-212">Идентификатор объекта</span><span class="sxs-lookup"><span data-stu-id="0dcea-212">Object ID</span></span>                                                     | <span data-ttu-id="0dcea-213">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0dcea-214">Строка октета</span><span class="sxs-lookup"><span data-stu-id="0dcea-214">Octet String</span></span>                                                  | <span data-ttu-id="0dcea-215">Внедренный объект класса **Uint8Array** , определенный ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0dcea-216">ИЛИ имя</span><span class="sxs-lookup"><span data-stu-id="0dcea-216">OR Name</span></span>                                                       | <span data-ttu-id="0dcea-217">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0dcea-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="0dcea-218">Presentation-Address</span></span>                                          | <span data-ttu-id="0dcea-219">Внедренный объект класса **Uint8Array** , определенный ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0dcea-220">Строка варианта печати</span><span class="sxs-lookup"><span data-stu-id="0dcea-220">Print Case String</span></span>                                             | <span data-ttu-id="0dcea-221">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="0dcea-222">Ссылка на реплику</span><span class="sxs-lookup"><span data-stu-id="0dcea-222">Replica Link</span></span>                                                  | <span data-ttu-id="0dcea-223">Внедренный объект класса **Uint8Array** , определенный ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="0dcea-224">**Строка (SID)**</span><span class="sxs-lookup"><span data-stu-id="0dcea-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="0dcea-225">Внедренный объект класса **Uint8Array** , определенный ниже.</span><span class="sxs-lookup"><span data-stu-id="0dcea-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="0dcea-226">Время</span><span class="sxs-lookup"><span data-stu-id="0dcea-226">Time</span></span>                                                          | <span data-ttu-id="0dcea-227">**\_Дата и время CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="0dcea-228">Время кодирования в формате UTC</span><span class="sxs-lookup"><span data-stu-id="0dcea-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="0dcea-229">**\_Дата и время CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="0dcea-230">Строка в Юникоде</span><span class="sxs-lookup"><span data-stu-id="0dcea-230">Unicode String</span></span>                                                | <span data-ttu-id="0dcea-231">**\_строка CIM**</span><span class="sxs-lookup"><span data-stu-id="0dcea-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="0dcea-232">Синтаксис строки октета, который ссылается на массив значений **Uint8** , представляет проблему при сопоставлении с WMI, поскольку Инструментарий WMI допускает свойства типа **Uint8** и массивы **Uint8**, тогда как Active Directory допускает свойства типа String октета, а также массивы строк октета.</span><span class="sxs-lookup"><span data-stu-id="0dcea-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="0dcea-233">В следующем примере показан класс поставщика служб каталогов, который используется для отображения массива свойств типа строки октета.</span><span class="sxs-lookup"><span data-stu-id="0dcea-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="0dcea-234">WMI сопоставляет все строки октета Active Directory значения свойств с внедренными экземплярами **Uint8Array**.</span><span class="sxs-lookup"><span data-stu-id="0dcea-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="0dcea-235">Аналогичным образом WMI сопоставляет массивы строк октета с массивами внедренных объектов **Uint8Array** .</span><span class="sxs-lookup"><span data-stu-id="0dcea-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="0dcea-236">В следующем примере показаны классы, сопоставленные инструментарием WMI для DN-Binary и DN-String значений свойств DS.</span><span class="sxs-lookup"><span data-stu-id="0dcea-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="0dcea-237">В следующей таблице показано, как WMI сопоставляет остальные свойства интерфейса Active Directory атрибутов с квалификаторами свойств WMI.</span><span class="sxs-lookup"><span data-stu-id="0dcea-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="0dcea-238">Атрибут Active Directory — имя свойства</span><span class="sxs-lookup"><span data-stu-id="0dcea-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="0dcea-239">Квалификатор WMI</span><span class="sxs-lookup"><span data-stu-id="0dcea-239">WMI Qualifier</span></span>       | <span data-ttu-id="0dcea-240">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0dcea-240">Data type</span></span>    | <span data-ttu-id="0dcea-241">Сведения о сопоставлении</span><span class="sxs-lookup"><span data-stu-id="0dcea-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="0dcea-242">**Синтаксис атрибута**</span><span class="sxs-lookup"><span data-stu-id="0dcea-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="0dcea-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="0dcea-243">**AttributeSyntax**</span></span> | <span data-ttu-id="0dcea-244">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0dcea-244">**VT\_BSTR**</span></span> | <span data-ttu-id="0dcea-245">Сопоставляется из строкового представления OID.</span><span class="sxs-lookup"><span data-stu-id="0dcea-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="0dcea-246">**Common-Name**</span><span class="sxs-lookup"><span data-stu-id="0dcea-246">**Common-Name**</span></span>                          | <span data-ttu-id="0dcea-247">**CN**</span><span class="sxs-lookup"><span data-stu-id="0dcea-247">**CN**</span></span>              | <span data-ttu-id="0dcea-248">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0dcea-248">**VT\_BSTR**</span></span> | <span data-ttu-id="0dcea-249">Сопоставляется со строковым значением.</span><span class="sxs-lookup"><span data-stu-id="0dcea-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="0dcea-250">**Только система**</span><span class="sxs-lookup"><span data-stu-id="0dcea-250">**System-Only**</span></span>                          | <span data-ttu-id="0dcea-251">**Система**</span><span class="sxs-lookup"><span data-stu-id="0dcea-251">**System**</span></span>          | <span data-ttu-id="0dcea-252">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="0dcea-252">**VT\_BOOL**</span></span> | <span data-ttu-id="0dcea-253">Сопоставляется из логического значения.</span><span class="sxs-lookup"><span data-stu-id="0dcea-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="0dcea-254">WMI сопоставляет все квалификаторы Active Directory с `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` разновидностями квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="0dcea-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="0dcea-255">Классы ассоциаций</span><span class="sxs-lookup"><span data-stu-id="0dcea-255">Association Classes</span></span>

<span data-ttu-id="0dcea-256">Служба каталогов по сути является иерархическим хранилищем объектов.</span><span class="sxs-lookup"><span data-stu-id="0dcea-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="0dcea-257">Эти объекты, которые могут отображаться на неконечном уровне иерархии, называются контейнерами.</span><span class="sxs-lookup"><span data-stu-id="0dcea-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="0dcea-258">Структура этой иерархии дополнительно управляется свойствами "ПОСС-старший" и "System-ПОСС-превосходно" класса в схеме.</span><span class="sxs-lookup"><span data-stu-id="0dcea-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="0dcea-259">Вместе они указывают набор классов, экземпляры которых могут содержаться в экземпляре класса контейнера.</span><span class="sxs-lookup"><span data-stu-id="0dcea-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="0dcea-260">В приведенном ниже примере моделируется Ассоциация CIM как экземпляры [**\_ \_ \_ вложенности класса**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment)static класса Association DS.</span><span class="sxs-lookup"><span data-stu-id="0dcea-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="0dcea-261">Поставщик класса взаимосвязей поддерживает методы [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) и [**креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) .</span><span class="sxs-lookup"><span data-stu-id="0dcea-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 

