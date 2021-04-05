---
description: Класс CIM \_ унитарикомпутерсистем представляет Настольный, мобильный, сетевой компьютер, сервер или другой тип одноузловой системы с одним узлом.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: Класс CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990429"
---
# <a name="cim_unitarycomputersystem-class"></a><span data-ttu-id="40b64-103">\_Класс CIM унитарикомпутерсистем</span><span class="sxs-lookup"><span data-stu-id="40b64-103">CIM\_UnitaryComputerSystem class</span></span>

<span data-ttu-id="40b64-104">Класс **CIM \_ унитарикомпутерсистем** представляет Настольный, мобильный, сетевой компьютер, сервер или другой тип одноузловой системы с одним узлом.</span><span class="sxs-lookup"><span data-stu-id="40b64-104">The **CIM\_UnitaryComputerSystem** class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40b64-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="40b64-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="40b64-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="40b64-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="40b64-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="40b64-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="40b64-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="40b64-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b64-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40b64-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="40b64-110">Члены</span><span class="sxs-lookup"><span data-stu-id="40b64-110">Members</span></span>

<span data-ttu-id="40b64-111">Класс **CIM \_ унитарикомпутерсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="40b64-111">The **CIM\_UnitaryComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="40b64-112">Методы</span><span class="sxs-lookup"><span data-stu-id="40b64-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="40b64-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="40b64-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40b64-114">Методы</span><span class="sxs-lookup"><span data-stu-id="40b64-114">Methods</span></span>

<span data-ttu-id="40b64-115">Класс **CIM \_ унитарикомпутерсистем** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="40b64-115">The **CIM\_UnitaryComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="40b64-116">Метод</span><span class="sxs-lookup"><span data-stu-id="40b64-116">Method</span></span>                                                                           | <span data-ttu-id="40b64-117">Описание</span><span class="sxs-lookup"><span data-stu-id="40b64-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40b64-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="40b64-118">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | <span data-ttu-id="40b64-119">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="40b64-119">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="40b64-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="40b64-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="40b64-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="40b64-121">Properties</span></span>

<span data-ttu-id="40b64-122">Класс **CIM \_ унитарикомпутерсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="40b64-122">The **CIM\_UnitaryComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40b64-123">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="40b64-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-126">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="40b64-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="40b64-127">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="40b64-127">Short textual description of the object.</span></span>

<span data-ttu-id="40b64-128">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-129">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="40b64-129">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-132">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="40b64-132">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="40b64-133">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40b64-133">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="40b64-134">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="40b64-134">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="40b64-135">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-135">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-136">**Описание**</span><span class="sxs-lookup"><span data-stu-id="40b64-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-139">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="40b64-139">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="40b64-140">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="40b64-140">Textual description of the object.</span></span>

<span data-ttu-id="40b64-141">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-142">**инитиаллоадинфо**</span><span class="sxs-lookup"><span data-stu-id="40b64-142">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-143">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="40b64-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40b64-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40b64-145">Данные, необходимые для нахождения устройства начальной загрузки (его ключа) или службы загрузки для запроса запуска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="40b64-145">Data needed to find either the initial load device (its key) or the boot service to request the operating system to start.</span></span> <span data-ttu-id="40b64-146">Кроме того, можно указать параметры загрузки (то есть путь и параметры).</span><span class="sxs-lookup"><span data-stu-id="40b64-146">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="40b64-147">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="40b64-147">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-148">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="40b64-148">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-150">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="40b64-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="40b64-151">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="40b64-151">Date and time the object was installed.</span></span> <span data-ttu-id="40b64-152">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="40b64-152">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="40b64-153">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-154">**ластлоадинфо**</span><span class="sxs-lookup"><span data-stu-id="40b64-154">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40b64-157">Данные, определяющие устройство начальной загрузки (его ключ) или службу загрузки, которая запросила последнюю загрузку операционной системы.</span><span class="sxs-lookup"><span data-stu-id="40b64-157">Data that identifies either the initial load device (its key) or the boot service that requested the last operating system load.</span></span> <span data-ttu-id="40b64-158">Кроме того, можно указать параметры загрузки (то есть путь и параметры).</span><span class="sxs-lookup"><span data-stu-id="40b64-158">In addition, the load parameters (that is, a path name and parameters) can also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="40b64-159">**Name**</span><span class="sxs-lookup"><span data-stu-id="40b64-159">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-162">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40b64-162">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="40b64-163">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="40b64-163">Label by which the object is known.</span></span> <span data-ttu-id="40b64-164">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="40b64-164">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="40b64-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-166">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="40b64-166">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40b64-169">Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) и его производные — это объекты верхнего уровня CIM, которые предоставляют область для многочисленных компонентов и нуждаются в уникальных [**\_ системных**](cim-system.md) ключах CIM.</span><span class="sxs-lookup"><span data-stu-id="40b64-169">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of CIM that provide the scope for numerous components and require unique [**CIM\_System**](cim-system.md) keys.</span></span> <span data-ttu-id="40b64-170">Эвристическая эвристика определяется для создания имени **CIM \_ ComputerSystem** в попытке всегда создавать то же системное имя независимо от протокола обнаружения.</span><span class="sxs-lookup"><span data-stu-id="40b64-170">A heuristic is defined to create the **CIM\_ComputerSystem** name in an attempt to always generate the same system name, independent of discovery protocol.</span></span> <span data-ttu-id="40b64-171">Это предотвращает проблемы с инвентаризацией и управлением, когда один и тот же ресурс или сущность обнаруживаются несколько раз, но не может быть разрешена в один объект.</span><span class="sxs-lookup"><span data-stu-id="40b64-171">This prevents inventory and management problems where the same asset or entity is discovered multiple times, but cannot be resolved to a single object.</span></span> <span data-ttu-id="40b64-172">Это свойство определяет, как системное имя было создано с помощью эвристики подклассов.</span><span class="sxs-lookup"><span data-stu-id="40b64-172">This property identifies how the system name was generated by using the subclass heuristic.</span></span> <span data-ttu-id="40b64-173">Эвристический подход описан в спецификации общей модели CIM V2 и предполагает, что документированные правила обходятся для определения и назначения имени.</span><span class="sxs-lookup"><span data-stu-id="40b64-173">The heuristic is outlined in the CIM V2 Common Model specification and assumes that the documented rules are traversed to determine and assign a name.</span></span> <span data-ttu-id="40b64-174">Список значений **намеформат** определяет порядок приоритета для назначения системного имени с помощью нескольких правил, сопоставленных с одним и тем же значением.</span><span class="sxs-lookup"><span data-stu-id="40b64-174">The **NameFormat** values list defines the precedence order for assigning the system name with several rules mapping to the same value.</span></span> <span data-ttu-id="40b64-175">Обратите внимание, что имя системы **CIM \_** , вычисляемое с помощью эвристического алгоритма, является значением ключа в системе.</span><span class="sxs-lookup"><span data-stu-id="40b64-175">Note that the **CIM\_ComputerSystem** name that is calculated using the heuristic is the system's key value.</span></span> <span data-ttu-id="40b64-176">Другие имена могут назначаться и использоваться для **CIM- \_ ComputerSystem** , которые лучше подходят для бизнеса, используя псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="40b64-176">Other names can be assigned and used for the **CIM\_ComputerSystem** that better suit the business, using aliases.</span></span>

<span data-ttu-id="40b64-177">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-177">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="40b64-178">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="40b64-178">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="40b64-179">**IP-адрес** ("IP")</span><span class="sxs-lookup"><span data-stu-id="40b64-179">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="40b64-180">**Набрать номер** ("набрать")</span><span class="sxs-lookup"><span data-stu-id="40b64-180">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="40b64-181">**HID** (HID)</span><span class="sxs-lookup"><span data-stu-id="40b64-181">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="40b64-182">**НВА** ("НВА")</span><span class="sxs-lookup"><span data-stu-id="40b64-182">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="40b64-183">**Хва** ("Хва")</span><span class="sxs-lookup"><span data-stu-id="40b64-183">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="40b64-184">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="40b64-184">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="40b64-185">**ISDN** (ISDN)</span><span class="sxs-lookup"><span data-stu-id="40b64-185">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="40b64-186">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="40b64-186">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="40b64-187">**ДКК** ("ДКК")</span><span class="sxs-lookup"><span data-stu-id="40b64-187">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="40b64-188">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="40b64-188">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="40b64-189">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="40b64-189">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="40b64-190">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="40b64-190">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="40b64-191">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="40b64-191">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40b64-192">**Другое** ("другое")</span><span class="sxs-lookup"><span data-stu-id="40b64-192">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40b64-193">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="40b64-193">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-194">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="40b64-194">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="40b64-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-196">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Элементы управления питанием системы DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="40b64-196">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="40b64-197">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="40b64-197">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="40b64-198">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="40b64-198">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40b64-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="40b64-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="40b64-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="40b64-200"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="40b64-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="40b64-201"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="40b64-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="40b64-202"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-203">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="40b64-203">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="40b64-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="40b64-204"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-205">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="40b64-205">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="40b64-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="40b64-206"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-207">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="40b64-207">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="40b64-208">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="40b64-208">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="40b64-209">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="40b64-209">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="40b64-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="40b64-210"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-211">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="40b64-211">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="40b64-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="40b64-212"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-213">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="40b64-213">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40b64-214">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="40b64-214">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-215">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="40b64-215">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40b64-217">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="40b64-217">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="40b64-218">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="40b64-218">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="40b64-219">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="40b64-219">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="40b64-220">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="40b64-220">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="40b64-221">**Установлен**</span><span class="sxs-lookup"><span data-stu-id="40b64-221">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-222">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40b64-222">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40b64-224">Текущее состояние электропитания компьютерной системы и связанной с ней операционной системы.</span><span class="sxs-lookup"><span data-stu-id="40b64-224">Current power state of the computer system and its associated operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40b64-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="40b64-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-226">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="40b64-226">Unknown.</span></span>

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="40b64-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)</span><span class="sxs-lookup"><span data-stu-id="40b64-227"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-228">Полная мощность.</span><span class="sxs-lookup"><span data-stu-id="40b64-228">Full power.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="40b64-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)</span><span class="sxs-lookup"><span data-stu-id="40b64-229"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-230">Система находится в состоянии энергосбережения и по-прежнему работает, но может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="40b64-230">System is in a power-save state and still functioning, but may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="40b64-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="40b64-231"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-232">Система не работает, но ее можно быстро приступить к полной мощности.</span><span class="sxs-lookup"><span data-stu-id="40b64-232">System is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="40b64-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (4)</span><span class="sxs-lookup"><span data-stu-id="40b64-233"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-234">Известно, что система находится в режиме энергосбережения, но ее точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="40b64-234">System is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="40b64-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)</span><span class="sxs-lookup"><span data-stu-id="40b64-235"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-236">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="40b64-236">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="40b64-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)</span><span class="sxs-lookup"><span data-stu-id="40b64-237"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-238">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="40b64-238">Power off.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="40b64-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (7)</span><span class="sxs-lookup"><span data-stu-id="40b64-239"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-240">Система находится в состоянии предупреждения, а также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="40b64-240">System is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="40b64-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Энергосбережение **— режим гибернации** (8)</span><span class="sxs-lookup"><span data-stu-id="40b64-241"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-242">Power Save Гибернация.</span><span class="sxs-lookup"><span data-stu-id="40b64-242">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="40b64-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Энергосбережение **— мягкое отключение** (9)</span><span class="sxs-lookup"><span data-stu-id="40b64-243"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="40b64-244">Энергосбережение с мягким отключением.</span><span class="sxs-lookup"><span data-stu-id="40b64-244">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40b64-245">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="40b64-245">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-247">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40b64-248">Строка, которая предоставляет сведения о том, как связаться с основным владельцем системы (например, номером телефона, адресом электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="40b64-248">String that provides information on how to reach the primary system owner (for example, phone number, email address, and so on).</span></span>

<span data-ttu-id="40b64-249">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-249">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-250">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="40b64-250">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-253">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="40b64-253">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="40b64-254">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="40b64-254">Name of the primary system owner.</span></span>

<span data-ttu-id="40b64-255">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-255">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-256">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="40b64-256">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="40b64-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-259">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Security аппаратная безопасность \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="40b64-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="40b64-260">Если параметр включен, единая система компьютера может быть сброшена с оборудованием (например, с помощью кнопок питания и сброса).</span><span class="sxs-lookup"><span data-stu-id="40b64-260">If enabled, the unitary computer system can be reset with hardware (for example, with the power and reset buttons).</span></span> <span data-ttu-id="40b64-261">Если отключено, аппаратный сброс не разрешен.</span><span class="sxs-lookup"><span data-stu-id="40b64-261">If disabled, hardware reset is not allowed.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="40b64-262">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="40b64-262">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40b64-263">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="40b64-263">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="40b64-264">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="40b64-264">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="40b64-265">**Включено** (4)</span><span class="sxs-lookup"><span data-stu-id="40b64-265">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="40b64-266">**Не реализовано** (5)</span><span class="sxs-lookup"><span data-stu-id="40b64-266">**Not Implemented** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="40b64-267">**Роли**</span><span class="sxs-lookup"><span data-stu-id="40b64-267">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-268">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="40b64-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="40b64-269">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40b64-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40b64-270">Роли, которые система играет в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="40b64-270">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="40b64-271">Подклассы системы могут переопределять это свойство для определения явных значений ролей.</span><span class="sxs-lookup"><span data-stu-id="40b64-271">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="40b64-272">Кроме того, Рабочая группа может описывать эвристику, соглашения и правила для указания ролей.</span><span class="sxs-lookup"><span data-stu-id="40b64-272">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="40b64-273">Например, для экземпляра сетевой системы это свойство может содержать строку "Switch" или "Bridge".</span><span class="sxs-lookup"><span data-stu-id="40b64-273">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="40b64-274">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-274">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="40b64-275">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="40b64-275">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40b64-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40b64-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40b64-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40b64-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40b64-278">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="40b64-278">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="40b64-279">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="40b64-279">Current status of the object.</span></span> <span data-ttu-id="40b64-280">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="40b64-281">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="40b64-281">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="40b64-282">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="40b64-282">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="40b64-283">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="40b64-283">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="40b64-284">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="40b64-284">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="40b64-285">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="40b64-285">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="40b64-286">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="40b64-286">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="40b64-287">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="40b64-287">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="40b64-288">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="40b64-288">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="40b64-289">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="40b64-289">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="40b64-290">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="40b64-290">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="40b64-291">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="40b64-291">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="40b64-292">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="40b64-292">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="40b64-293">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="40b64-293">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="40b64-294"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="40b64-294"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="40b64-295">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40b64-295">Remarks</span></span>

<span data-ttu-id="40b64-296">Класс **CIM \_ унитарикомпутерсистем** является производным от [**CIM \_ ComputerSystem**](cim-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-296">The **CIM\_UnitaryComputerSystem** class is derived from [**CIM\_ComputerSystem**](cim-computersystem.md).</span></span>

<span data-ttu-id="40b64-297">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="40b64-297">WMI does not implement this class.</span></span> <span data-ttu-id="40b64-298">Классы WMI, производные от **CIM \_ унитарикомпутерсистем**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="40b64-298">For WMI classes derived from **CIM\_UnitaryComputerSystem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="40b64-299">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="40b64-299">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="40b64-300">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="40b64-300">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40b64-301">Требования</span><span class="sxs-lookup"><span data-stu-id="40b64-301">Requirements</span></span>



| <span data-ttu-id="40b64-302">Требование</span><span class="sxs-lookup"><span data-stu-id="40b64-302">Requirement</span></span> | <span data-ttu-id="40b64-303">Значение</span><span class="sxs-lookup"><span data-stu-id="40b64-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40b64-304">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40b64-304">Minimum supported client</span></span><br/> | <span data-ttu-id="40b64-305">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40b64-305">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40b64-306">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40b64-306">Minimum supported server</span></span><br/> | <span data-ttu-id="40b64-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40b64-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40b64-308">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40b64-308">Namespace</span></span><br/>                | <span data-ttu-id="40b64-309">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="40b64-309">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40b64-310">MOF</span><span class="sxs-lookup"><span data-stu-id="40b64-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40b64-311"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40b64-311"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40b64-312">DLL</span><span class="sxs-lookup"><span data-stu-id="40b64-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40b64-313"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40b64-313"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40b64-314">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40b64-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b64-315">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="40b64-315">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> </dl>

 

