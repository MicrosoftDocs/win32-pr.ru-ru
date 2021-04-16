---
description: Представляет связь между службой и управляемым элементом, на которые может повлиять выполнение.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Класс CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662471"
---
# <a name="cim_serviceaffectselement-class"></a><span data-ttu-id="18e8a-103">\_Класс CIM сервицеаффектселемент</span><span class="sxs-lookup"><span data-stu-id="18e8a-103">CIM\_ServiceAffectsElement class</span></span>

<span data-ttu-id="18e8a-104">Представляет связь между службой и управляемым элементом, на которые может повлиять выполнение.</span><span class="sxs-lookup"><span data-stu-id="18e8a-104">Represents an association between a service and a managed element that might be affected by its execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e8a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="18e8a-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="18e8a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="18e8a-106">Members</span></span>

<span data-ttu-id="18e8a-107">Класс **CIM \_ сервицеаффектселемент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="18e8a-107">The **CIM\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="18e8a-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="18e8a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18e8a-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="18e8a-109">Properties</span></span>

<span data-ttu-id="18e8a-110">Класс **CIM \_ сервицеаффектселемент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="18e8a-110">The **CIM\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="18e8a-111">**аффектеделемент**</span><span class="sxs-lookup"><span data-stu-id="18e8a-111">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18e8a-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="18e8a-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18e8a-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-114">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18e8a-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18e8a-115">Управляемый элемент, затронутый службой.</span><span class="sxs-lookup"><span data-stu-id="18e8a-115">The managed element that is affected by the service.</span></span>

</dd> <dt>

<span data-ttu-id="18e8a-116">**аффектинжелемент**</span><span class="sxs-lookup"><span data-stu-id="18e8a-116">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18e8a-117">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="18e8a-117">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18e8a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="18e8a-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="18e8a-120">Служба, влияющая на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="18e8a-120">The service that is affecting the managed element.</span></span>

</dd> <dt>

<span data-ttu-id="18e8a-121">**елементеффектс**</span><span class="sxs-lookup"><span data-stu-id="18e8a-121">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18e8a-122">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="18e8a-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18e8a-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-124">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сервицеаффектселемент**.**Осерелементеффектсдескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="18e8a-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**OtherElementEffectsDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="18e8a-125">Воздействие на управляемый элемент.</span><span class="sxs-lookup"><span data-stu-id="18e8a-125">The effect on the managed element.</span></span> <span data-ttu-id="18e8a-126">Этот массив соответствует массиву **осерелементеффектсдескриптионс** .</span><span class="sxs-lookup"><span data-stu-id="18e8a-126">This array corresponds to the **OtherElementEffectsDescriptions** array.</span></span>

<span data-ttu-id="18e8a-127">\- Монопольное использование (2): ни одна другая служба не может использовать эту связь с элементом.</span><span class="sxs-lookup"><span data-stu-id="18e8a-127">\- Exclusive Use (2): No other Service may have this association to the element.</span></span>

<span data-ttu-id="18e8a-128">\- Влияние на производительность (3): не рекомендуется в пользу "потребляет", "повышает производительность" или "снижение производительности".</span><span class="sxs-lookup"><span data-stu-id="18e8a-128">\- Performance Impact (3): Deprecated in favor of "Consumes", "Enhances Performance", or "Degrades Performance".</span></span> <span data-ttu-id="18e8a-129">Выполнение службы может повысить или снизить производительность элемента.</span><span class="sxs-lookup"><span data-stu-id="18e8a-129">Execution of the Service may enhance or degrade the performance of the element.</span></span> <span data-ttu-id="18e8a-130">Это может быть побочным действием выполнения или, как следствие, от методов, предоставляемых службой.</span><span class="sxs-lookup"><span data-stu-id="18e8a-130">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="18e8a-131">\- Целостность элементов (4): не рекомендуется в пользу "потребляет", "повышает целостность" или "снижение целостности".</span><span class="sxs-lookup"><span data-stu-id="18e8a-131">\- Element Integrity (4): Deprecated in favor of "Consumes", "Enhances Integrity", or "Degrades Integrity".</span></span> <span data-ttu-id="18e8a-132">Выполнение службы может повысить или снизить целостность элемента.</span><span class="sxs-lookup"><span data-stu-id="18e8a-132">Execution of the Service may enhance or degrade the integrity of the element.</span></span> <span data-ttu-id="18e8a-133">Это может быть побочным действием выполнения или, как следствие, от методов, предоставляемых службой.</span><span class="sxs-lookup"><span data-stu-id="18e8a-133">This may be as a side-effect of execution or as an intended consequence of methods provided by the Service.</span></span>

<span data-ttu-id="18e8a-134">\- Управляет (5). служба управляет элементом.</span><span class="sxs-lookup"><span data-stu-id="18e8a-134">\- Manages (5): The Service manages the element.</span></span>

<span data-ttu-id="18e8a-135">\- Потребление (6): выполнение службы потребляет некоторые или все связанные элементы как следствие выполнения службы.</span><span class="sxs-lookup"><span data-stu-id="18e8a-135">\- Consumes (6): Execution of the Service consumes some or all of the associated element as a consequence of running the Service.</span></span> <span data-ttu-id="18e8a-136">Например, служба может использовать циклы ЦП, что может повлиять на производительность или хранение, что может повлиять на производительность и целостность.</span><span class="sxs-lookup"><span data-stu-id="18e8a-136">For example, the Service may consume CPU cycles, which may affect performance, or Storage which may affect both performance and integrity.</span></span> <span data-ttu-id="18e8a-137">(Например, отсутствие свободного хранилища может привести к снижению целостности, уменьшая возможность сохранения состояния.</span><span class="sxs-lookup"><span data-stu-id="18e8a-137">(For instance, the lack of free storage can degrade integrity by reducing the ability to save state.</span></span> <span data-ttu-id="18e8a-138">) "Использование" может использоваться отдельно или в сочетании с другими значениями (в частности, "снижение производительности" и "снижение целостности").</span><span class="sxs-lookup"><span data-stu-id="18e8a-138">) "Consumes" may be used alone or in conjunction with other values, in particular, "Degrades Performance" and "Degrades Integrity".</span></span>

<span data-ttu-id="18e8a-139">Для отражения служб распределения, которые могут предоставляться службой, следует использовать "Управление", а не "использование".</span><span class="sxs-lookup"><span data-stu-id="18e8a-139">"Manages" and not "Consumes" should be used to reflect allocation services that may be provided by a Service.</span></span>

<span data-ttu-id="18e8a-140">\- Расширяет целостность (7): служба может улучшить целостность связанного элемента.</span><span class="sxs-lookup"><span data-stu-id="18e8a-140">\- Enhances Integrity (7): The Service may enhance integrity of the associated element.</span></span>

<span data-ttu-id="18e8a-141">\- Деградация целостности (8): служба может снизить целостность связанного элемента.</span><span class="sxs-lookup"><span data-stu-id="18e8a-141">\- Degrades Integrity (8): The Service may degrade integrity of the associated element.</span></span>

<span data-ttu-id="18e8a-142">\- Повышение производительности (9): служба может повысить производительность связанного элемента.</span><span class="sxs-lookup"><span data-stu-id="18e8a-142">\- Enhances Performance (9): The Service may enhance performance of the associated element.</span></span>

<span data-ttu-id="18e8a-143">\- Снижение производительности (10): служба может снизить производительность связанного элемента.</span><span class="sxs-lookup"><span data-stu-id="18e8a-143">\- Degrades Performance (10): The Service may degrade performance of the associated element.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="18e8a-144">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="18e8a-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="18e8a-145">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="18e8a-145">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

<span data-ttu-id="18e8a-146">**Эксклюзивное использование** (2)</span><span class="sxs-lookup"><span data-stu-id="18e8a-146">**Exclusive Use** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

<span data-ttu-id="18e8a-147">**Влияние на производительность** (3)</span><span class="sxs-lookup"><span data-stu-id="18e8a-147">**Performance Impact** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

<span data-ttu-id="18e8a-148">**Целостность элементов** (4)</span><span class="sxs-lookup"><span data-stu-id="18e8a-148">**Element Integrity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

<span data-ttu-id="18e8a-149">**Управляет** (5)</span><span class="sxs-lookup"><span data-stu-id="18e8a-149">**Manages** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

<span data-ttu-id="18e8a-150">**Потреблено** (6)</span><span class="sxs-lookup"><span data-stu-id="18e8a-150">**Consumes** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

<span data-ttu-id="18e8a-151">**Улучшенная целостность** (7)</span><span class="sxs-lookup"><span data-stu-id="18e8a-151">**Enhances Integrity** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

<span data-ttu-id="18e8a-152">**Целостность деградаций** (8)</span><span class="sxs-lookup"><span data-stu-id="18e8a-152">**Degrades Integrity** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

<span data-ttu-id="18e8a-153">**Повышает производительность** (9)</span><span class="sxs-lookup"><span data-stu-id="18e8a-153">**Enhances Performance** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

<span data-ttu-id="18e8a-154">Снижение **производительности** (10)</span><span class="sxs-lookup"><span data-stu-id="18e8a-154">**Degrades Performance** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="18e8a-155">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="18e8a-155">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="18e8a-156">**Поставщик зарезервирован** (0x8000.. 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="18e8a-156">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="18e8a-157">**осерелементеффектсдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="18e8a-157">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18e8a-158">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="18e8a-158">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="18e8a-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="18e8a-160">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сервицеаффектселемент**.**Елементеффектс**")</span><span class="sxs-lookup"><span data-stu-id="18e8a-160">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ServiceAffectsElement**.**ElementEffects**")</span></span>
</dt> </dl>

<span data-ttu-id="18e8a-161">Каждый элемент в массиве предоставляет дополнительные сведения для соответствующего элемента в массиве **елементеффектс** .</span><span class="sxs-lookup"><span data-stu-id="18e8a-161">Each item in the array provides additional information for the corresponding item in the **ElementEffects** array.</span></span> <span data-ttu-id="18e8a-162">Для любого элемента в массиве **елементеффектс** , для которого задано значение **other** ("1"), требуется описание.</span><span class="sxs-lookup"><span data-stu-id="18e8a-162">A description is required for any item in the **ElementEffects** array that is set to **Other** ("1").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18e8a-163">Требования</span><span class="sxs-lookup"><span data-stu-id="18e8a-163">Requirements</span></span>



| <span data-ttu-id="18e8a-164">Требование</span><span class="sxs-lookup"><span data-stu-id="18e8a-164">Requirement</span></span> | <span data-ttu-id="18e8a-165">Значение</span><span class="sxs-lookup"><span data-stu-id="18e8a-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18e8a-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18e8a-166">Minimum supported client</span></span><br/> | <span data-ttu-id="18e8a-167">Windows 8</span><span class="sxs-lookup"><span data-stu-id="18e8a-167">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="18e8a-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18e8a-168">Minimum supported server</span></span><br/> | <span data-ttu-id="18e8a-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="18e8a-169">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="18e8a-170">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="18e8a-170">Namespace</span></span><br/>                | <span data-ttu-id="18e8a-171">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="18e8a-171">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="18e8a-172">MOF</span><span class="sxs-lookup"><span data-stu-id="18e8a-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="18e8a-173"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="18e8a-173"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="18e8a-174">DLL</span><span class="sxs-lookup"><span data-stu-id="18e8a-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18e8a-175"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="18e8a-175"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

