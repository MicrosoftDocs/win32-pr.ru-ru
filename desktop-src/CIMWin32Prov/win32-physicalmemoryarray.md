---
description: '&Win32 \_ фисикалмеморяррай \# 160; Класс WMI представляет сведения о физической памяти компьютерной системы. Сюда входит количество устройств памяти, объем доступной памяти и тип памяти&\# 8212, например системную или видеопамять.'
ms.assetid: 6b553230-e1fc-46e6-b13a-02fbbd34034d
ms.tgt_platform: multiple
title: Класс Win32_PhysicalMemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryArray
- Win32_PhysicalMemoryArray.IsCompatible
- Win32_PhysicalMemoryArray.Caption
- Win32_PhysicalMemoryArray.CreationClassName
- Win32_PhysicalMemoryArray.Depth
- Win32_PhysicalMemoryArray.Description
- Win32_PhysicalMemoryArray.Height
- Win32_PhysicalMemoryArray.HotSwappable
- Win32_PhysicalMemoryArray.InstallDate
- Win32_PhysicalMemoryArray.Location
- Win32_PhysicalMemoryArray.Manufacturer
- Win32_PhysicalMemoryArray.MaxCapacity
- Win32_PhysicalMemoryArray.MaxCapacityEx
- Win32_PhysicalMemoryArray.MemoryDevices
- Win32_PhysicalMemoryArray.MemoryErrorCorrection
- Win32_PhysicalMemoryArray.Model
- Win32_PhysicalMemoryArray.Name
- Win32_PhysicalMemoryArray.OtherIdentifyingInfo
- Win32_PhysicalMemoryArray.PartNumber
- Win32_PhysicalMemoryArray.PoweredOn
- Win32_PhysicalMemoryArray.Removable
- Win32_PhysicalMemoryArray.Replaceable
- Win32_PhysicalMemoryArray.SerialNumber
- Win32_PhysicalMemoryArray.SKU
- Win32_PhysicalMemoryArray.Status
- Win32_PhysicalMemoryArray.Tag
- Win32_PhysicalMemoryArray.Use
- Win32_PhysicalMemoryArray.Version
- Win32_PhysicalMemoryArray.Weight
- Win32_PhysicalMemoryArray.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8a585b0399f7015113b02ff48dbeb85956c9e62b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990795"
---
# <a name="win32_physicalmemoryarray-class"></a><span data-ttu-id="d9f18-104">\_Класс Win32 фисикалмеморяррай</span><span class="sxs-lookup"><span data-stu-id="d9f18-104">Win32\_PhysicalMemoryArray class</span></span>

<span data-ttu-id="d9f18-105">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ фисикалмеморяррай для Win32** представляет сведения о физической памяти компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="d9f18-105">The **Win32\_PhysicalMemoryArray** [WMI class](../wmisdk/retrieving-a-class.md) represents details about the computer system physical memory.</span></span> <span data-ttu-id="d9f18-106">Сюда входит количество устройств памяти, объем доступной памяти и тип памяти, например системную или видеопамять.</span><span class="sxs-lookup"><span data-stu-id="d9f18-106">This includes the number of memory devices, memory capacity available, and memory type—for example, system or video memory.</span></span>

<span data-ttu-id="d9f18-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d9f18-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d9f18-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="d9f18-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f18-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9f18-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B99-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemoryArray : CIM_PhysicalPackage
{
  string   Caption;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   Location;
  string   Manufacturer;
  uint32   MaxCapacity;
  uint64   MaxCapacityEx;
  uint16   MemoryDevices;
  uint16   MemoryErrorCorrection;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  uint16   Use;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="d9f18-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d9f18-110">Members</span></span>

<span data-ttu-id="d9f18-111">Класс **Win32 \_ фисикалмеморяррай** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9f18-111">The **Win32\_PhysicalMemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="d9f18-112">Методы</span><span class="sxs-lookup"><span data-stu-id="d9f18-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d9f18-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9f18-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d9f18-114">Методы</span><span class="sxs-lookup"><span data-stu-id="d9f18-114">Methods</span></span>

<span data-ttu-id="d9f18-115">Класс **Win32 \_ фисикалмеморяррай** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d9f18-115">The **Win32\_PhysicalMemoryArray** class has these methods.</span></span>



| <span data-ttu-id="d9f18-116">Метод</span><span class="sxs-lookup"><span data-stu-id="d9f18-116">Method</span></span>           | <span data-ttu-id="d9f18-117">Описание</span><span class="sxs-lookup"><span data-stu-id="d9f18-117">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="d9f18-118">**Является совместимым**</span><span class="sxs-lookup"><span data-stu-id="d9f18-118">**IsCompatible**</span></span> | <span data-ttu-id="d9f18-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="d9f18-119">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d9f18-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9f18-120">Properties</span></span>

<span data-ttu-id="d9f18-121">Класс **Win32 \_ фисикалмеморяррай** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9f18-121">The **Win32\_PhysicalMemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9f18-122">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d9f18-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-125">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d9f18-125">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-126">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="d9f18-126">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="d9f18-127">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-128">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d9f18-128">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-131">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d9f18-131">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-132">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d9f18-132">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d9f18-133">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="d9f18-133">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d9f18-134">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-134">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-135">**Depth**</span><span class="sxs-lookup"><span data-stu-id="d9f18-135">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-136">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="d9f18-136">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-138">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="d9f18-138">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-139">Глубина физического пакета — в дюймах.</span><span class="sxs-lookup"><span data-stu-id="d9f18-139">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="d9f18-140">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-140">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-141">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9f18-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-144">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d9f18-144">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-145">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d9f18-145">Description of the object.</span></span>

<span data-ttu-id="d9f18-146">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-147">**Height**</span><span class="sxs-lookup"><span data-stu-id="d9f18-147">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-148">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="d9f18-148">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-150">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="d9f18-150">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-151">Высота физического пакета — в дюймах.</span><span class="sxs-lookup"><span data-stu-id="d9f18-151">Height of the physical package—in inches.</span></span>

<span data-ttu-id="d9f18-152">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-152">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-153">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="d9f18-153">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-154">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9f18-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-156">Если **значение равно true**, физический пакет может быть горячей заменой (если можно заменить элемент физически отличающимся, но эквивалентным ему, пока содержащий его пакет применяет к нему питание).</span><span class="sxs-lookup"><span data-stu-id="d9f18-156">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it, is "on").</span></span> <span data-ttu-id="d9f18-157">Например, пакет диска, вставленный с помощью соединителей SCA, является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="d9f18-157">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="d9f18-158">Все пакеты, которые могут быть горячей заменой, по сути своей являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="d9f18-158">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="d9f18-159">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-159">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-160">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d9f18-160">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-161">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d9f18-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-163">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d9f18-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-164">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="d9f18-164">Date and time the object was installed.</span></span> <span data-ttu-id="d9f18-165">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="d9f18-165">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d9f18-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-167">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="d9f18-167">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-168">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9f18-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-170">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 16 \| Location")</span><span class="sxs-lookup"><span data-stu-id="d9f18-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-171">Физическое расположение массива памяти.</span><span class="sxs-lookup"><span data-stu-id="d9f18-171">Physical location of the memory array.</span></span>

<span data-ttu-id="d9f18-172">Это значение берется из элемента **Location** структуры **массива физической памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d9f18-172">This value comes from the **Location** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d9f18-173">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="d9f18-173">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d9f18-174">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d9f18-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d9f18-175">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d9f18-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_board_or_motherboard"></span><span id="system_board_or_motherboard"></span><span id="SYSTEM_BOARD_OR_MOTHERBOARD"></span>

<span data-ttu-id="d9f18-176">**Системная плата или материнская** плата (3)</span><span class="sxs-lookup"><span data-stu-id="d9f18-176">**System board or motherboard** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_add-on_card"></span><span id="isa_add-on_card"></span><span id="ISA_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-177">**Карта расширения ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="d9f18-177">**ISA add-on card** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_add-on_card"></span><span id="eisa_add-on_card"></span><span id="EISA_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-178">**Плата надстройки EISA** (5)</span><span class="sxs-lookup"><span data-stu-id="d9f18-178">**EISA add-on card** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_add-on_card"></span><span id="pci_add-on_card"></span><span id="PCI_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-179">**Карта расширения PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="d9f18-179">**PCI add-on card** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_add-on_card"></span><span id="mca_add-on_card"></span><span id="MCA_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-180">**Карточка надстройки MCA** (7)</span><span class="sxs-lookup"><span data-stu-id="d9f18-180">**MCA add-on card** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_add-on_card"></span><span id="pcmcia_add-on_card"></span><span id="PCMCIA_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-181">**Карта расширения PCMCIA** (8)</span><span class="sxs-lookup"><span data-stu-id="d9f18-181">**PCMCIA add-on card** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_add-on_card"></span><span id="proprietary_add-on_card"></span><span id="PROPRIETARY_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-182">**Специальная карта расширения** (9)</span><span class="sxs-lookup"><span data-stu-id="d9f18-182">**Proprietary add-on card** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="d9f18-183">**Нубус** (10)</span><span class="sxs-lookup"><span data-stu-id="d9f18-183">**NuBus** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C20_add-on_card"></span><span id="pc-98_c20_add-on_card"></span><span id="PC-98_C20_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-184">**Карточка надстройки PC-98/C20** (11)</span><span class="sxs-lookup"><span data-stu-id="d9f18-184">**PC-98/C20 add-on card** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_C24_add-on_card"></span><span id="pc-98_c24_add-on_card"></span><span id="PC-98_C24_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-185">**Карточка надстройки PC-98/C24** (12)</span><span class="sxs-lookup"><span data-stu-id="d9f18-185">**PC-98/C24 add-on card** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_E_add-on_card"></span><span id="pc-98_e_add-on_card"></span><span id="PC-98_E_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-186">**Карта расширения PC-98/E** (13)</span><span class="sxs-lookup"><span data-stu-id="d9f18-186">**PC-98/E add-on card** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98_Local_bus_add-on_card"></span><span id="pc-98_local_bus_add-on_card"></span><span id="PC-98_LOCAL_BUS_ADD-ON_CARD"></span>

<span data-ttu-id="d9f18-187">**Карта расширения PC-98/локальной шины** (14)</span><span class="sxs-lookup"><span data-stu-id="d9f18-187">**PC-98/Local bus add-on card** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9f18-188">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="d9f18-188">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-191">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d9f18-191">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-192">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="d9f18-192">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="d9f18-193">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-193">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-194">**MaxCapacity**</span><span class="sxs-lookup"><span data-stu-id="d9f18-194">**MaxCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-195">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9f18-195">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-197">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 16 \| Максимальная емкость")</span><span class="sxs-lookup"><span data-stu-id="d9f18-197">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Maximum Capacity")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-198">Вместо этого используйте свойство **макскапаЦитекс** .</span><span class="sxs-lookup"><span data-stu-id="d9f18-198">Use the **MaxCapacityEx** property instead.</span></span>

<span data-ttu-id="d9f18-199">Это значение берется из элемента **максимальной емкости** структуры **массива физической памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d9f18-199">This value comes from the **Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d9f18-200">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Максимальный размер памяти (в байтах), устанавливаемый для этого конкретного массива памяти.</span><span class="sxs-lookup"><span data-stu-id="d9f18-200">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** Maximum memory size (in bytes) installable for this particular memory array.</span></span> <span data-ttu-id="d9f18-201">Если размер неизвестен, свойству присваивается значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="d9f18-201">If the size is unknown, the property is given a value of 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-202">**макскапаЦитекс**</span><span class="sxs-lookup"><span data-stu-id="d9f18-202">**MaxCapacityEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-203">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9f18-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-205">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 16 \| Расширенная максимальная емкость"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="d9f18-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Extended Maximum Capacity"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-206">Максимальный размер памяти (в килобайтах), устанавливаемый для этого конкретного массива памяти.</span><span class="sxs-lookup"><span data-stu-id="d9f18-206">Maximum memory size (in kilobytes) installable for this particular memory array.</span></span> <span data-ttu-id="d9f18-207">Если размер неизвестен, свойству присваивается значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="d9f18-207">If the size is unknown, the property is given a value of 0 (zero).</span></span>

<span data-ttu-id="d9f18-208">Это значение берется из **расширенной максимальной емкости** в структуре **массива физической памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d9f18-208">This value comes from the **Extended Maximum Capacity** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d9f18-209">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d9f18-209">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-210">**меморидевицес**</span><span class="sxs-lookup"><span data-stu-id="d9f18-210">**MemoryDevices**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9f18-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-213">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 16: \| число устройств памяти")</span><span class="sxs-lookup"><span data-stu-id="d9f18-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Number of Memory Devices")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-214">Число физических слотов или сокетов, доступных в этом массиве памяти.</span><span class="sxs-lookup"><span data-stu-id="d9f18-214">Number of physical slots or sockets available in this memory array.</span></span>

<span data-ttu-id="d9f18-215">Это значение берется из **числа устройств памяти** в структуре **массива физической памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d9f18-215">This value comes from the **Number of Memory Devices** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-216">**меморерроркорректион**</span><span class="sxs-lookup"><span data-stu-id="d9f18-216">**MemoryErrorCorrection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-217">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9f18-217">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-219">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \| исправление ошибки памяти SMBIOS типа 16")</span><span class="sxs-lookup"><span data-stu-id="d9f18-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-220">Тип исправления ошибок, используемый массивом памяти.</span><span class="sxs-lookup"><span data-stu-id="d9f18-220">Type of error correction used by the memory array.</span></span>

<span data-ttu-id="d9f18-221">Это значение берется из элемента **исправления ошибок памяти** в структуре **массива физической памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d9f18-221">This value comes from the **Memory Error Correction** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d9f18-222">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="d9f18-222">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d9f18-223">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d9f18-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d9f18-224">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d9f18-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d9f18-225">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="d9f18-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="d9f18-226">**Четность** (4)</span><span class="sxs-lookup"><span data-stu-id="d9f18-226">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="d9f18-227">**Одноразрядный ECC** (5)</span><span class="sxs-lookup"><span data-stu-id="d9f18-227">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="d9f18-228">**Многоразрядный ECC** (6)</span><span class="sxs-lookup"><span data-stu-id="d9f18-228">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="d9f18-229">**CRC** (7)</span><span class="sxs-lookup"><span data-stu-id="d9f18-229">**CRC** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9f18-230">**Модель**</span><span class="sxs-lookup"><span data-stu-id="d9f18-230">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-233">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d9f18-233">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-234">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="d9f18-234">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="d9f18-235">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-236">**Name**</span><span class="sxs-lookup"><span data-stu-id="d9f18-236">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-239">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="d9f18-239">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-240">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d9f18-240">Label by which the object is known.</span></span> <span data-ttu-id="d9f18-241">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="d9f18-241">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d9f18-242">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-243">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="d9f18-243">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-245">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-246">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для обнаружения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="d9f18-246">Additional data, beyond asset tag information, that could be used to identify a physical element.</span></span> <span data-ttu-id="d9f18-247">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="d9f18-247">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="d9f18-248">Обратите внимание, что если доступны только данные штрих-кода и они уникальны или могут использоваться в качестве ключа элемента, это свойство будет иметь **значение NULL** и данные штрих-кода, используемые в качестве ключа класса, в свойстве Tag.</span><span class="sxs-lookup"><span data-stu-id="d9f18-248">Note that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="d9f18-249">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-249">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-250">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="d9f18-250">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-253">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="d9f18-253">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-254">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="d9f18-254">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="d9f18-255">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-255">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-256">**повередон**</span><span class="sxs-lookup"><span data-stu-id="d9f18-256">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-257">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9f18-257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-259">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="d9f18-259">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="d9f18-260">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-260">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-261">**Службе**</span><span class="sxs-lookup"><span data-stu-id="d9f18-261">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-262">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9f18-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-264">Если **значение равно true**, физический пакет является съемным (если он предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается, без нарушения функции общей упаковки).</span><span class="sxs-lookup"><span data-stu-id="d9f18-264">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="d9f18-265">Пакет по-прежнему может быть съемным, если необходимо отключить питание, чтобы выполнить удаление.</span><span class="sxs-lookup"><span data-stu-id="d9f18-265">A package can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="d9f18-266">Если Power может быть "on", а пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="d9f18-266">If power can be "on" and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="d9f18-267">Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей SCA.</span><span class="sxs-lookup"><span data-stu-id="d9f18-267">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="d9f18-268">Однако последняя может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="d9f18-268">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="d9f18-269">Дисплей ноутбука не является съемным или не является избыточным источником питания.</span><span class="sxs-lookup"><span data-stu-id="d9f18-269">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="d9f18-270">Удаление этих компонентов повлияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.</span><span class="sxs-lookup"><span data-stu-id="d9f18-270">Removing these components would affect the function of the overall packaging or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="d9f18-271">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-271">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-272">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="d9f18-272">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-273">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d9f18-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-275">Если **значение — true**, этот компонент физического носителя можно заменить физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="d9f18-275">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="d9f18-276">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="d9f18-276">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="d9f18-277">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="d9f18-277">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="d9f18-278">Еще один пример — это пакет источника питания, подключенный к скользящим шинам.</span><span class="sxs-lookup"><span data-stu-id="d9f18-278">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="d9f18-279">Все съемные пакеты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="d9f18-279">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="d9f18-280">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-280">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-281">**Номер**</span><span class="sxs-lookup"><span data-stu-id="d9f18-281">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-284">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d9f18-284">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-285">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="d9f18-285">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="d9f18-286">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-287">**SKU**</span><span class="sxs-lookup"><span data-stu-id="d9f18-287">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-290">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d9f18-290">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-291">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="d9f18-291">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="d9f18-292">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-293">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d9f18-293">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-296">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d9f18-296">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-297">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d9f18-297">Current status of the object.</span></span> <span data-ttu-id="d9f18-298">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="d9f18-298">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d9f18-299">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="d9f18-299">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d9f18-300">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="d9f18-300">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d9f18-301">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="d9f18-301">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d9f18-302">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d9f18-302">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d9f18-303">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d9f18-304">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d9f18-304">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d9f18-305">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d9f18-305">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d9f18-306">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d9f18-306">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d9f18-307">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d9f18-307">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d9f18-308">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d9f18-308">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d9f18-309">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d9f18-309">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d9f18-310">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d9f18-310">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d9f18-311">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d9f18-311">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d9f18-312">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d9f18-312">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d9f18-313">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d9f18-313">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d9f18-314">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d9f18-314">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d9f18-315">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d9f18-315">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d9f18-316">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d9f18-316">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9f18-317">**Тег**</span><span class="sxs-lookup"><span data-stu-id="d9f18-317">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-320">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d9f18-320">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-321">Уникальный идентификатор массива физической памяти.</span><span class="sxs-lookup"><span data-stu-id="d9f18-321">Unique identifier of the physical memory array.</span></span>

<span data-ttu-id="d9f18-322">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-322">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="d9f18-323">Пример: "массив физической памяти 1"</span><span class="sxs-lookup"><span data-stu-id="d9f18-323">Example: "Physical Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-324">**Использование**</span><span class="sxs-lookup"><span data-stu-id="d9f18-324">**Use**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-325">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d9f18-325">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-327">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 16 \| use")</span><span class="sxs-lookup"><span data-stu-id="d9f18-327">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Use")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-328">Использование памяти в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="d9f18-328">How memory is used in the computer system.</span></span>

<span data-ttu-id="d9f18-329">Это значение берется из элемента **use** структуры **массива физической памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d9f18-329">This value comes from the **Use** member of the **Physical Memory Array** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d9f18-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="d9f18-330"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d9f18-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d9f18-331"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d9f18-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d9f18-332"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>

<span data-ttu-id="d9f18-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**Системная память** (3)</span><span class="sxs-lookup"><span data-stu-id="d9f18-333"><span id="System_memory"></span><span id="system_memory"></span><span id="SYSTEM_MEMORY"></span>**System memory** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>

<span data-ttu-id="d9f18-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Видеопамять** (4)</span><span class="sxs-lookup"><span data-stu-id="d9f18-334"><span id="Video_memory"></span><span id="video_memory"></span><span id="VIDEO_MEMORY"></span>**Video memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>

<span data-ttu-id="d9f18-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Флэш-память** (5)</span><span class="sxs-lookup"><span data-stu-id="d9f18-335"><span id="Flash_memory"></span><span id="flash_memory"></span><span id="FLASH_MEMORY"></span>**Flash memory** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>

<span data-ttu-id="d9f18-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Энергонезависимые ОЗУ** (6)</span><span class="sxs-lookup"><span data-stu-id="d9f18-336"><span id="Non-volatile_RAM"></span><span id="non-volatile_ram"></span><span id="NON-VOLATILE_RAM"></span>**Non-volatile RAM** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d9f18-337">Энергонезависимая ОЗУ</span><span class="sxs-lookup"><span data-stu-id="d9f18-337">Nonvolatile RAM</span></span>

</dd> <dt>

<span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>

<span data-ttu-id="d9f18-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Память кэша** (7)</span><span class="sxs-lookup"><span data-stu-id="d9f18-338"><span id="Cache_memory"></span><span id="cache_memory"></span><span id="CACHE_MEMORY"></span>**Cache memory** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d9f18-339">**Version**</span><span class="sxs-lookup"><span data-stu-id="d9f18-339">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9f18-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-342">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="d9f18-342">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-343">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="d9f18-343">Version of the physical element.</span></span>

<span data-ttu-id="d9f18-344">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-344">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-345">**Weight**</span><span class="sxs-lookup"><span data-stu-id="d9f18-345">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-346">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="d9f18-346">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-348">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("фунты")</span><span class="sxs-lookup"><span data-stu-id="d9f18-348">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-349">Вес физического пакета в фунтах.</span><span class="sxs-lookup"><span data-stu-id="d9f18-349">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="d9f18-350">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-350">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d9f18-351">**Width**</span><span class="sxs-lookup"><span data-stu-id="d9f18-351">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9f18-352">Тип данных: **real32**</span><span class="sxs-lookup"><span data-stu-id="d9f18-352">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9f18-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9f18-354">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")</span><span class="sxs-lookup"><span data-stu-id="d9f18-354">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="d9f18-355">Ширина физического пакета в дюймах.</span><span class="sxs-lookup"><span data-stu-id="d9f18-355">Width of the physical package in inches.</span></span>

<span data-ttu-id="d9f18-356">Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-356">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9f18-357">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9f18-357">Remarks</span></span>

<span data-ttu-id="d9f18-358">Класс **Win32 \_ фисикалмеморяррай** является производным от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="d9f18-358">The **Win32\_PhysicalMemoryArray** class is derived from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d9f18-359">Примеры</span><span class="sxs-lookup"><span data-stu-id="d9f18-359">Examples</span></span>

<span data-ttu-id="d9f18-360">Следующий пример PowerShell извлекает количество слотов памяти и объем памяти, установленной на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="d9f18-360">The following PowerShell sample retrieves the number of memory slots and the amount of memory installed on a target computer.</span></span>


```PowerShell
$strComputer = Read-Host "Enter Computer Name"
 $colSlots = Get-WmiObject -Class "win32_PhysicalMemoryArray" -namespace "root\CIMV2" `
 -computerName $strComputer
 $colRAM = Get-WmiObject -Class "win32_PhysicalMemory" -namespace "root\CIMV2" `
 -computerName $strComputer

Foreach ($objSlot In $colSlots){
      "Total Number of DIMM Slots: " + $objSlot.MemoryDevices
 }
 Foreach ($objRAM In $colRAM) {
      "Memory Installed: " + $objRAM.DeviceLocator
      "Memory Size: " + ($objRAM.Capacity / 1GB) + " GB"
 }
```



<span data-ttu-id="d9f18-361">Следующий пример кода VBScript возвращает сведения о физической памяти, установленной на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d9f18-361">The following VBScript code sample returns information about the physical memory installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_PhysicalMemoryArray") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Maximum Capacity: " & objItem.MaxCapacity 
    Wscript.Echo "Memory Devices: " & objItem.MemoryDevices 
    Wscript.Echo "Memory Error Correction: " & objItem.MemoryErrorCorrection 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d9f18-362">Требования</span><span class="sxs-lookup"><span data-stu-id="d9f18-362">Requirements</span></span>



| <span data-ttu-id="d9f18-363">Требование</span><span class="sxs-lookup"><span data-stu-id="d9f18-363">Requirement</span></span> | <span data-ttu-id="d9f18-364">Значение</span><span class="sxs-lookup"><span data-stu-id="d9f18-364">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f18-365">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9f18-365">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f18-366">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9f18-366">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9f18-367">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9f18-367">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f18-368">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9f18-368">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9f18-369">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9f18-369">Namespace</span></span><br/>                | <span data-ttu-id="d9f18-370">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d9f18-370">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9f18-371">MOF</span><span class="sxs-lookup"><span data-stu-id="d9f18-371">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9f18-372"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9f18-372"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9f18-373">DLL</span><span class="sxs-lookup"><span data-stu-id="d9f18-373">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9f18-374"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9f18-374"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9f18-375">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9f18-375">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f18-376">**\_ФИСИКАЛПАККАЖЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="d9f18-376">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dt>

[<span data-ttu-id="d9f18-377">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="d9f18-377">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d9f18-378">**\_Меморяррайлокатион Win32**</span><span class="sxs-lookup"><span data-stu-id="d9f18-378">**Win32\_MemoryArrayLocation**</span></span>](win32-memoryarraylocation.md)
</dt> </dl>

 

 
