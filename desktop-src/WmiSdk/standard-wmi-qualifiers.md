---
description: Ниже перечислены стандартные квалификаторы, относящиеся к инструментарию WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Стандартные квалификаторы WMI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702556"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="d7fc2-103">Стандартные квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="d7fc2-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="d7fc2-104">Ниже перечислены стандартные квалификаторы, относящиеся к инструментарию WMI.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="d7fc2-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Дополнительного соглашения**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-106">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-106">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-107">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-107">Applies to: classes</span></span>

<span data-ttu-id="d7fc2-108">Указывает, что класс содержит измененные квалификаторы, которые локализуются.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="d7fc2-109">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-109">The default is **TRUE**.</span></span>

<span data-ttu-id="d7fc2-110">Связанный класс можно перевести.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-110">The associated class can be translated.</span></span> <span data-ttu-id="d7fc2-111">Для доступа к переведенной версии используйте идентификатор локали для создания имени пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Обход \_ GetObject**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-113">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-114">Область применения: методы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-114">Applies to: methods</span></span>

<span data-ttu-id="d7fc2-115">Указывает, что вызов метода должен передаваться непосредственно в вызов **ексекмесодасинк** поставщика вместо того, чтобы поставщик сначала вызывал вызов **GetObject для проверки пути к объекту** .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="d7fc2-116">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-116">The default is **FALSE**.</span></span> <span data-ttu-id="d7fc2-117">Использование **обхода \_ GetObject** может значительно повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="d7fc2-118">Прежде чем использовать **обход \_ GetObject**, убедитесь, что не выполняются никакие из следующих действий.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="d7fc2-119">Создайте класс, производный от класса.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="d7fc2-120">Переопределите метод с квалификатором **обход \_ GetObject** .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="d7fc2-121">Несоблюдение этих предосторожностей может привести к вызову реализации метода родительского класса вместо дочернего класса.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="d7fc2-122">Дополнительные сведения см. в разделе использование квалификатора обхода неполного \_ объекта.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Ключ CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-124">Тип данных: **\_ логическая модель CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="d7fc2-125">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="d7fc2-125">Applies to: properties</span></span>

<span data-ttu-id="d7fc2-126">Указывает, что связанное свойство является ключевым свойством CIM, но не находится в WMI.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**Цимтипе**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-128">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-129">Область применения: свойства, методы, параметры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="d7fc2-130">Содержит текст, описывающий тип свойства.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**классконтекст**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-132">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-133">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-133">Applies to: classes</span></span>

<span data-ttu-id="d7fc2-134">Указывает, что у класса есть экземпляры, связанные с дополнительной информацией, динамически предоставляемой поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Не рекомендуется**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-136">Тип данных: **\_ логическая модель CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="d7fc2-137">Область применения: свойства, классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-137">Applies to: properties, classes</span></span>

<span data-ttu-id="d7fc2-138">Указывает, что свойство было заменено другим свойством.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Монитор**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-140">Область применения: классы, свойства</span><span class="sxs-lookup"><span data-stu-id="d7fc2-140">Applies to: classes, properties</span></span>

<span data-ttu-id="d7fc2-141">**UUID** связанного класса.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Платформе**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-143">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-143">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-144">Область применения: классы, свойства</span><span class="sxs-lookup"><span data-stu-id="d7fc2-144">Applies to: classes, properties</span></span>

<span data-ttu-id="d7fc2-145">Указывает класс, экземпляры которого создаются динамически.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="d7fc2-146">Значение этого квалификатора должно быть равно **true**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**динпропс**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-148">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-149">Область применения: классы, экземпляры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-149">Applies to: classes, instances</span></span>

<span data-ttu-id="d7fc2-150">Указывает, что экземпляр содержит значения, предоставляемые поставщиками динамических свойств.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="d7fc2-151">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-151">The default is **TRUE**.</span></span>

<span data-ttu-id="d7fc2-152">Этот квалификатор необходимо указать на таком экземпляре.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="d7fc2-153">Допускается только значение **true** .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Префикс**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-155">Тип данных: **\_ логическая модель CIM**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="d7fc2-156">Область применения: экземпляры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-156">Applies to: instances</span></span>

<span data-ttu-id="d7fc2-157">Указывает, что значение этого свойства не может изменяться в течение времени существования экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-158"><span id="ID"></span><span id="id"></span>**УДОСТОВЕРЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-159">Тип данных: **VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="d7fc2-160">Область применения: свойства, параметры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="d7fc2-161">Уникально идентифицирует и последовательность параметра свойства или метода при создании инструкций MOF автоматически.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="d7fc2-162">Этот квалификатор обязателен только для параметров метода.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="d7fc2-163">При создании параметров для метода конструкторы классов должны начинаться с ID (0) для первого параметра и использовать каждое последовательное целое число для каждого последующего параметра.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="d7fc2-164">Если квалификаторы **идентификатора** непреднамеренно опущены, компилятор MOF автоматически создает квалификаторы **идентификатора** .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Применен**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-166">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-166">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-167">Область применения: методы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-167">Applies to: methods</span></span>

<span data-ttu-id="d7fc2-168">Указывает, что метод имеет реализацию, предоставляемую поставщиком.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**Указаны**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-170">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-171">Область применения: экземпляры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-171">Applies to: instances</span></span>

<span data-ttu-id="d7fc2-172">Указывает, что экземпляр содержит значения, предоставленные поставщиком динамических свойств.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="d7fc2-173">Значение передается поставщику свойств в качестве аргумента в метод [**ивбемпропертипровидер::-Property**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Языкового стандарта**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-175">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-176">Область применения: классы или экземпляры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-176">Applies to: classes or instances</span></span>

<span data-ttu-id="d7fc2-177">Задает язык происхождения для класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="d7fc2-178">Дополнительные сведения о значениях языкового стандарта см. в разделе [коды языков](#locale-codes).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**намеспацесекуритисддл**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-180">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-180">Data type: **string array**</span></span>

<span data-ttu-id="d7fc2-181">Область применения: экземпляры пространства имен</span><span class="sxs-lookup"><span data-stu-id="d7fc2-181">Applies to: namespace instances</span></span>

<span data-ttu-id="d7fc2-182">Задает дескриптор безопасности для пространства имен в формате [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="d7fc2-183">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен при создании пространства имен](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="d7fc2-184">Строка SDDL обрабатывается WMI для установления безопасности пространства имен, но не хранится в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="d7fc2-185">Если дескриптор безопасности не указан, используется безопасность по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="d7fc2-186">Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Используемых**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-188">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-188">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-189">Область применения: параметры</span><span class="sxs-lookup"><span data-stu-id="d7fc2-189">Applies to: parameters</span></span>

<span data-ttu-id="d7fc2-190">Указывает, что параметр не является обязательным и имеет правильно настроенное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Права**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-192">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-192">Data type: **string array**</span></span>

<span data-ttu-id="d7fc2-193">Область применения: свойства, методы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-193">Applies to: properties, methods</span></span>

<span data-ttu-id="d7fc2-194">Набор значений, используемых для информирования клиента о том, какие права требуются для создания экземпляров, заполнения свойств или выполнения методов.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="d7fc2-195">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**пропертиконтекст**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-197">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-198">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="d7fc2-198">Applies to: properties</span></span>

<span data-ttu-id="d7fc2-199">Указывает, что свойство экземпляра содержит значения, предоставляемые поставщиками динамических свойств.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="d7fc2-200">Этот квалификатор необходимо указать в таком свойстве.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="d7fc2-201">Значение передается поставщику свойств в качестве аргумента в [**ивбемпропертипровидер::-Property**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Поставщики**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-203">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-204">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-204">Applies to: classes</span></span>

<span data-ttu-id="d7fc2-205">Значением этого квалификатора является имя динамического поставщика, предоставляющего экземпляры класса и обновляющая данные экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="d7fc2-206">Это имя должно быть зарегистрировано в WMI путем создания экземпляра класса [**\_ \_ Win32Provider**](--win32provider.md) со свойством **Name** , содержащим это имя.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="d7fc2-207">Если этот квалификатор задан для класса, экземпляры которого предоставляются динамически, необходимо также указать **динамический** квалификатор.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**рекуиресенкриптион**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-209">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-209">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-210">Область применения: экземпляры пространства имен</span><span class="sxs-lookup"><span data-stu-id="d7fc2-210">Applies to: namespace instances</span></span>

<span data-ttu-id="d7fc2-211">Если задано значение **true**, **рекуиресенкриптион** помечает пространство имен таким образом, чтобы клиентские приложения и сценарии могли подключаться с помощью зашифрованной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="d7fc2-212">Уровень проверки подлинности должен быть установлен на **\_ \_ \_ уровень \_ \_ безопасности RPC C AUTHN Level PKT** в C++.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="d7fc2-213">В скриптах или Visual Basic уровень проверки подлинности должен быть установлен в **вбемаусентикатионлевелпктприваци**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="d7fc2-214">Дополнительные сведения см. в разделе [Настройка дескрипторов безопасности намепаце](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="d7fc2-215">Квалификатор используется в [*MOF*](gloss-m.md) с помощью команды препроцессора пространства имен pragma.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="d7fc2-216">Дополнительные сведения см. в разделе [Установка уровня безопасности процесса по умолчанию с помощью C++](setting-the-default-process-security-level-using-c-.md) или [Установка уровня безопасности процесса по умолчанию с помощью VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="d7fc2-217">Скрипты уровней проверки подлинности определяются в [**вбемаусентикатионлевеленум**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Единый**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-219">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-219">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-220">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-220">Applies to: classes</span></span>

<span data-ttu-id="d7fc2-221">Обозначает класс, который может иметь только один экземпляр и не содержит ключевые свойства.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="d7fc2-222">Допускается только значение **true** (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="d7fc2-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Статически**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-224">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-224">Data type: **boolean**</span></span>

<span data-ttu-id="d7fc2-225">Область применения: методы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-225">Applies to: methods</span></span>

<span data-ttu-id="d7fc2-226">Указывает, может ли метод вызываться с помощью определения класса или его экземпляров.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="d7fc2-227">Метод не может быть вызван из экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Подтип**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-229">Тип данных: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="d7fc2-230">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="d7fc2-230">Applies to: properties</span></span>

<span data-ttu-id="d7fc2-231">Указывает, что свойство типа **\_ DateTime** представляет интервал времени, а не определенное время.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="d7fc2-232">Чтобы указать свойство как интервал, значение этого квалификатора должно быть "Interval".</span><span class="sxs-lookup"><span data-stu-id="d7fc2-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="d7fc2-233">Все остальные значения для этого квалификатора зарезервированы для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-235">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-235">Data type: **string**</span></span>

<span data-ttu-id="d7fc2-236">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-236">Applies to: classes</span></span>

<span data-ttu-id="d7fc2-237">Универсальный уникальный идентификатор, примененный к классу.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**классверсион**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-239">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-239">Data type: **string**</span></span>

<span data-ttu-id="d7fc2-240">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="d7fc2-240">Applies to: classes</span></span>

<span data-ttu-id="d7fc2-241">Номер версии объекта класса.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-241">The version number of the class object.</span></span> <span data-ttu-id="d7fc2-242">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-242">The default is **NULL**.</span></span> <span data-ttu-id="d7fc2-243">Номер версии увеличивается при внесении изменений в класс.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="d7fc2-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**вритепривилежес**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="d7fc2-245">Тип данных: **массив строк**</span><span class="sxs-lookup"><span data-stu-id="d7fc2-245">Data type: **string array**</span></span>

<span data-ttu-id="d7fc2-246">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="d7fc2-246">Applies to: properties</span></span>

<span data-ttu-id="d7fc2-247">Набор значений, указывающий, какие системные привилегии должны быть доступны и включены для успешной операции записи.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d7fc2-248">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7fc2-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="d7fc2-249">Коды языковых стандартов</span><span class="sxs-lookup"><span data-stu-id="d7fc2-249">Locale Codes</span></span>

<span data-ttu-id="d7fc2-250">Код локали имеет вид «MS \_ <Three Digit Language ID> ».</span><span class="sxs-lookup"><span data-stu-id="d7fc2-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="d7fc2-251">Например, английский язык — это MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="d7fc2-252">В следующей таблице перечислены идентификаторы языков.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="d7fc2-253">Язык</span><span class="sxs-lookup"><span data-stu-id="d7fc2-253">Language</span></span>              | <span data-ttu-id="d7fc2-254">Идентификатор языка (шестнадцатеричный)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="d7fc2-255">Арабский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-255">Arabic</span></span>                | <span data-ttu-id="d7fc2-256">401</span><span class="sxs-lookup"><span data-stu-id="d7fc2-256">401</span></span>                       |
| <span data-ttu-id="d7fc2-257">Португальский (Бразилия)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="d7fc2-258">416</span><span class="sxs-lookup"><span data-stu-id="d7fc2-258">416</span></span>                       |
| <span data-ttu-id="d7fc2-259">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="d7fc2-260">804</span><span class="sxs-lookup"><span data-stu-id="d7fc2-260">804</span></span>                       |
| <span data-ttu-id="d7fc2-261">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-261">Chinese (Traditional)</span></span> | <span data-ttu-id="d7fc2-262">404</span><span class="sxs-lookup"><span data-stu-id="d7fc2-262">404</span></span>                       |
| <span data-ttu-id="d7fc2-263">Чешский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-263">Czech</span></span>                 | <span data-ttu-id="d7fc2-264">405</span><span class="sxs-lookup"><span data-stu-id="d7fc2-264">405</span></span>                       |
| <span data-ttu-id="d7fc2-265">Датский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-265">Danish</span></span>                | <span data-ttu-id="d7fc2-266">406</span><span class="sxs-lookup"><span data-stu-id="d7fc2-266">406</span></span>                       |
| <span data-ttu-id="d7fc2-267">Нидерландский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-267">Dutch</span></span>                 | <span data-ttu-id="d7fc2-268">413</span><span class="sxs-lookup"><span data-stu-id="d7fc2-268">413</span></span>                       |
| <span data-ttu-id="d7fc2-269">Английский (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-269">English (default)</span></span>     | <span data-ttu-id="d7fc2-270">409</span><span class="sxs-lookup"><span data-stu-id="d7fc2-270">409</span></span>                       |
| <span data-ttu-id="d7fc2-271">Финский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-271">Finnish</span></span>               | <span data-ttu-id="d7fc2-272">40b</span><span class="sxs-lookup"><span data-stu-id="d7fc2-272">40b</span></span>                       |
| <span data-ttu-id="d7fc2-273">Французский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-273">French</span></span>                | <span data-ttu-id="d7fc2-274">40c</span><span class="sxs-lookup"><span data-stu-id="d7fc2-274">40c</span></span>                       |
| <span data-ttu-id="d7fc2-275">Немецкий</span><span class="sxs-lookup"><span data-stu-id="d7fc2-275">German</span></span>                | <span data-ttu-id="d7fc2-276">407</span><span class="sxs-lookup"><span data-stu-id="d7fc2-276">407</span></span>                       |
| <span data-ttu-id="d7fc2-277">Греческий</span><span class="sxs-lookup"><span data-stu-id="d7fc2-277">Greek</span></span>                 | <span data-ttu-id="d7fc2-278">408</span><span class="sxs-lookup"><span data-stu-id="d7fc2-278">408</span></span>                       |
| <span data-ttu-id="d7fc2-279">Иврит</span><span class="sxs-lookup"><span data-stu-id="d7fc2-279">Hebrew</span></span>                | <span data-ttu-id="d7fc2-280">40d</span><span class="sxs-lookup"><span data-stu-id="d7fc2-280">40d</span></span>                       |
| <span data-ttu-id="d7fc2-281">Венгерский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-281">Hungarian</span></span>             | <span data-ttu-id="d7fc2-282">40e</span><span class="sxs-lookup"><span data-stu-id="d7fc2-282">40e</span></span>                       |
| <span data-ttu-id="d7fc2-283">Итальянский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-283">Italian</span></span>               | <span data-ttu-id="d7fc2-284">410</span><span class="sxs-lookup"><span data-stu-id="d7fc2-284">410</span></span>                       |
| <span data-ttu-id="d7fc2-285">Японский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-285">Japanese</span></span>              | <span data-ttu-id="d7fc2-286">411</span><span class="sxs-lookup"><span data-stu-id="d7fc2-286">411</span></span>                       |
| <span data-ttu-id="d7fc2-287">Корейский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-287">Korean</span></span>                | <span data-ttu-id="d7fc2-288">412</span><span class="sxs-lookup"><span data-stu-id="d7fc2-288">412</span></span>                       |
| <span data-ttu-id="d7fc2-289">Норвежский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-289">Norwegian</span></span>             | <span data-ttu-id="d7fc2-290">414</span><span class="sxs-lookup"><span data-stu-id="d7fc2-290">414</span></span>                       |
| <span data-ttu-id="d7fc2-291">Польский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-291">Polish</span></span>                | <span data-ttu-id="d7fc2-292">415</span><span class="sxs-lookup"><span data-stu-id="d7fc2-292">415</span></span>                       |
| <span data-ttu-id="d7fc2-293">Португальский (Португалия)</span><span class="sxs-lookup"><span data-stu-id="d7fc2-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="d7fc2-294">816</span><span class="sxs-lookup"><span data-stu-id="d7fc2-294">816</span></span>                       |
| <span data-ttu-id="d7fc2-295">русском языке</span><span class="sxs-lookup"><span data-stu-id="d7fc2-295">Russian</span></span>               | <span data-ttu-id="d7fc2-296">419</span><span class="sxs-lookup"><span data-stu-id="d7fc2-296">419</span></span>                       |
| <span data-ttu-id="d7fc2-297">Испанский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-297">Spanish</span></span>               | <span data-ttu-id="d7fc2-298">c0a</span><span class="sxs-lookup"><span data-stu-id="d7fc2-298">c0a</span></span>                       |
| <span data-ttu-id="d7fc2-299">Шведский</span><span class="sxs-lookup"><span data-stu-id="d7fc2-299">Swedish</span></span>               | <span data-ttu-id="d7fc2-300">41D</span><span class="sxs-lookup"><span data-stu-id="d7fc2-300">41D</span></span>                       |
| <span data-ttu-id="d7fc2-301">Турецкий</span><span class="sxs-lookup"><span data-stu-id="d7fc2-301">Turkish</span></span>               | <span data-ttu-id="d7fc2-302">41f</span><span class="sxs-lookup"><span data-stu-id="d7fc2-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="d7fc2-303">Использование квалификатора обхода обходных \_ объектов</span><span class="sxs-lookup"><span data-stu-id="d7fc2-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="d7fc2-304">Использование квалификатора **обхода обходных \_ объектов** в методе может привести к непонятным результатам.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="d7fc2-305">В следующем примере определяются классы **Shape** и **Circle** .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="d7fc2-306">Обратите внимание, что класс **Circle** является производным от класса **Shape** .</span><span class="sxs-lookup"><span data-stu-id="d7fc2-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="d7fc2-307">Следующий вызов метода **ExecMethod** использует объект **Circle** с именем «миЦиркле» для рисования окружности.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="d7fc2-308">В предыдущем сценарии WMI вызывает **GetObject**; обнаруживает, что "Shape. name = ' МиЦиркле '" является **кругом**; и выполняет реализацию **Circle** объекта **дравит**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="d7fc2-309">Однако если в **дравит** используется квалификатор **обхода \_** , WMI не вызывает **GetObject**, не обнаруживает, что «Shape. name = ' миЦиркле '» является **кругом** и выполняет реализацию **Shape** **дравит** вместо **круговой** реализации **дравит**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="d7fc2-310">Следующий вызов метода **ExecMethod** всегда вызывает правильную реализацию **дравит**.</span><span class="sxs-lookup"><span data-stu-id="d7fc2-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="d7fc2-311">Требования</span><span class="sxs-lookup"><span data-stu-id="d7fc2-311">Requirements</span></span>



| <span data-ttu-id="d7fc2-312">Требование</span><span class="sxs-lookup"><span data-stu-id="d7fc2-312">Requirement</span></span> | <span data-ttu-id="d7fc2-313">Значение</span><span class="sxs-lookup"><span data-stu-id="d7fc2-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d7fc2-314">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7fc2-314">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fc2-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7fc2-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d7fc2-316">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7fc2-316">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fc2-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7fc2-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7fc2-318">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7fc2-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7fc2-319">Настройка дескрипторов безопасности Намепаце</span><span class="sxs-lookup"><span data-stu-id="d7fc2-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="d7fc2-320">Квалификаторы WMI</span><span class="sxs-lookup"><span data-stu-id="d7fc2-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="d7fc2-321">Добавление квалификатора</span><span class="sxs-lookup"><span data-stu-id="d7fc2-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

