---
description: Представляет физическое устройство памяти, расположенное в компьютерной системе и доступное операционной системе.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Класс Win32_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e026c3c3d0a29bbbd10ed2b5565708f0bcb0900c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496722"
---
# <a name="win32_physicalmemory-class"></a><span data-ttu-id="231d3-103">\_Класс Win32 фисикалмемори</span><span class="sxs-lookup"><span data-stu-id="231d3-103">Win32\_PhysicalMemory class</span></span>

<span data-ttu-id="231d3-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ фисикалмемори для Win32** представляет физическое устройство памяти, расположенное в компьютерной системе и доступное операционной системе.</span><span class="sxs-lookup"><span data-stu-id="231d3-104">The **Win32\_PhysicalMemory** [WMI class](../wmisdk/retrieving-a-class.md) represents a physical memory device located on a computer system and available to the operating system.</span></span>

<span data-ttu-id="231d3-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="231d3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="231d3-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="231d3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="231d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="231d3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="231d3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="231d3-108">Members</span></span>

<span data-ttu-id="231d3-109">Класс **Win32 \_ фисикалмемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="231d3-109">The **Win32\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="231d3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="231d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="231d3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="231d3-111">Properties</span></span>

<span data-ttu-id="231d3-112">Класс **Win32 \_ фисикалмемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="231d3-112">The **Win32\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="231d3-113">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="231d3-113">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-114">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-116">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17 \| атрибуты")</span><span class="sxs-lookup"><span data-stu-id="231d3-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Attributes")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-117">SMBIOS-Type 17 — атрибуты.</span><span class="sxs-lookup"><span data-stu-id="231d3-117">SMBIOS - Type 17 - Attributes.</span></span> <span data-ttu-id="231d3-118">Представляет ранг.</span><span class="sxs-lookup"><span data-stu-id="231d3-118">Represents the RANK.</span></span>

<span data-ttu-id="231d3-119">Это значение берется из элемента **Attributes** структуры **Memory Device** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-119">This value comes from the **Attributes** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-120">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="231d3-120">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-121">**банклабел**</span><span class="sxs-lookup"><span data-stu-id="231d3-121">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-124">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. Память DMTF, \| устройство \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="231d3-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-125">Физически помеченный банк, в котором находится память.</span><span class="sxs-lookup"><span data-stu-id="231d3-125">Physically labeled bank where the memory is located.</span></span>

<span data-ttu-id="231d3-126">Примеры: "Bank 0", "Bank A"</span><span class="sxs-lookup"><span data-stu-id="231d3-126">Examples: "Bank 0", "Bank A"</span></span>

<span data-ttu-id="231d3-127">Это значение берется из элемента **локатора банка** в структуре **устройств памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-127">This value comes from the **Bank Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-128">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-128">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-129">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="231d3-129">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-130">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="231d3-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-132">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Memory Device \| 002,5 "), [**Units**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="231d3-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-133">Общая емкость физической памяти — в байтах.</span><span class="sxs-lookup"><span data-stu-id="231d3-133">Total capacity of the physical memory—in bytes.</span></span>

<span data-ttu-id="231d3-134">Это значение берется из структуры **памяти устройства** в сведениях о версии SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-134">This value comes from the **Memory Device** structure in the SMBIOS version information.</span></span> <span data-ttu-id="231d3-135">Для SMBIOS версии 2,1 по 2,6 значение берется из элемента **size** .</span><span class="sxs-lookup"><span data-stu-id="231d3-135">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Size** member.</span></span> <span data-ttu-id="231d3-136">Для SMBIOS версии 2.7 + значение берется из элемента **Расширенный размер** .</span><span class="sxs-lookup"><span data-stu-id="231d3-136">For SMBIOS version 2.7+ the value comes from the **Extended Size** member.</span></span>

<span data-ttu-id="231d3-137">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-137">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<span data-ttu-id="231d3-138">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-139">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="231d3-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-142">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="231d3-142">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-143">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="231d3-143">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="231d3-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-145">**конфигуредклоккспид**</span><span class="sxs-lookup"><span data-stu-id="231d3-145">**ConfiguredClockSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-146">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-148">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17 \| настроенная тактовая частота памяти")</span><span class="sxs-lookup"><span data-stu-id="231d3-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured Memory Clock Speed")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-149">Настроенная тактовая частота устройства памяти в мегагерцах (МГц) или 0, если скорость неизвестна.</span><span class="sxs-lookup"><span data-stu-id="231d3-149">The configured clock speed of the memory device, in megahertz (MHz), or 0, if the speed is unknown.</span></span>

<span data-ttu-id="231d3-150">Это значение берется из **настроенной скорости тактовой частоты памяти** в структуре **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-150">This value comes from the **Configured Memory Clock Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-151">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="231d3-151">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-152">**конфигуредволтаже**</span><span class="sxs-lookup"><span data-stu-id="231d3-152">**ConfiguredVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-155">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17 \| настроенное напряжение")</span><span class="sxs-lookup"><span data-stu-id="231d3-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Configured voltage")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-156">Настроенное напряжение для этого устройства, в милливольтах или 0, если напряжение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="231d3-156">Configured voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="231d3-157">Это значение берется из **настроенного элемента питания** структуры **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-157">This value comes from the **Configured voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-158">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="231d3-158">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-159">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="231d3-159">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-162">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="231d3-162">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-163">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="231d3-163">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="231d3-164">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="231d3-164">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="231d3-165">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-165">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-166">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="231d3-166">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-167">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="231d3-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-169">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Memory Device \| 002,8 "), [**Units**](../wmisdk/standard-qualifiers.md) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="231d3-169">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-170">Ширина данных физической памяти — в битах.</span><span class="sxs-lookup"><span data-stu-id="231d3-170">Data width of the physical memory—in bits.</span></span> <span data-ttu-id="231d3-171">Ширина данных 0 (ноль) и общая ширина 8 (восемь) означает, что память используется только для обеспечения битов исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="231d3-171">A data width of 0 (zero) and a total width of 8 (eight) indicates that the memory is used solely to provide error correction bits.</span></span>

<span data-ttu-id="231d3-172">Это значение берется из элемента **ширина данных** структуры **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-172">This value comes from the **Data Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-173">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-173">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-174">**Описание**</span><span class="sxs-lookup"><span data-stu-id="231d3-174">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-177">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="231d3-177">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-178">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="231d3-178">Description of an object.</span></span>

<span data-ttu-id="231d3-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-180">**DeviceLocator**</span><span class="sxs-lookup"><span data-stu-id="231d3-180">**DeviceLocator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-181">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-183">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17 \| Локатор устройств")</span><span class="sxs-lookup"><span data-stu-id="231d3-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Device Locator")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-184">Метка сокета или платы, в которой находится память.</span><span class="sxs-lookup"><span data-stu-id="231d3-184">Label of the socket or circuit board that holds the memory.</span></span>

<span data-ttu-id="231d3-185">Пример: "SIMM 3"</span><span class="sxs-lookup"><span data-stu-id="231d3-185">Example: "SIMM 3"</span></span>

<span data-ttu-id="231d3-186">Это значение берется из элемента **локатора устройства** в структуре **памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-186">This value comes from the **Device Locator** member of the **Memory Device** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-187">**формфактор**</span><span class="sxs-lookup"><span data-stu-id="231d3-187">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-188">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="231d3-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-190">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. Память DMTF, \| устройство \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="231d3-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-191">Конструктивный фактор для микросхемы.</span><span class="sxs-lookup"><span data-stu-id="231d3-191">Implementation form factor for the chip.</span></span>

<span data-ttu-id="231d3-192">Это значение берется **из конструктивного элемента структуры** **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-192">This value comes from the **Form Factor** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-193">Это свойство наследуется [**от \_ микросхемы CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-193">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>



 <span data-ttu-id="231d3-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="231d3-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-195">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="231d3-195">Unknown</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-196">(1)</span><span class="sxs-lookup"><span data-stu-id="231d3-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-197">Другое</span><span class="sxs-lookup"><span data-stu-id="231d3-197">Other</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-198">(2)</span><span class="sxs-lookup"><span data-stu-id="231d3-198">(2)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-199">ПАНЕЛЬ</span><span class="sxs-lookup"><span data-stu-id="231d3-199">SIP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-200">(3)</span><span class="sxs-lookup"><span data-stu-id="231d3-200">(3)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-201">DIP</span><span class="sxs-lookup"><span data-stu-id="231d3-201">DIP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-202">(4)</span><span class="sxs-lookup"><span data-stu-id="231d3-202">(4)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-203">ZIP</span><span class="sxs-lookup"><span data-stu-id="231d3-203">ZIP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-204">(5)</span><span class="sxs-lookup"><span data-stu-id="231d3-204">(5)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-205">сож</span><span class="sxs-lookup"><span data-stu-id="231d3-205">SOJ</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-206"> (6)</span><span class="sxs-lookup"><span data-stu-id="231d3-206">(6)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-207">Частный</span><span class="sxs-lookup"><span data-stu-id="231d3-207">Proprietary</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-208">(7)</span><span class="sxs-lookup"><span data-stu-id="231d3-208">(7)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-209">Банк</span><span class="sxs-lookup"><span data-stu-id="231d3-209">SIMM</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-210">(8)</span><span class="sxs-lookup"><span data-stu-id="231d3-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-211">ДОСТУП</span><span class="sxs-lookup"><span data-stu-id="231d3-211">DIMM</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-212">(9)</span><span class="sxs-lookup"><span data-stu-id="231d3-212">(9)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-213">тсоп</span><span class="sxs-lookup"><span data-stu-id="231d3-213">TSOP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-214">(10)</span><span class="sxs-lookup"><span data-stu-id="231d3-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-215">FCPGA</span><span class="sxs-lookup"><span data-stu-id="231d3-215">PGA</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-216">(11)</span><span class="sxs-lookup"><span data-stu-id="231d3-216">(11)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-217">RIMM</span><span class="sxs-lookup"><span data-stu-id="231d3-217">RIMM</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-218">(12)</span><span class="sxs-lookup"><span data-stu-id="231d3-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-219">содимм</span><span class="sxs-lookup"><span data-stu-id="231d3-219">SODIMM</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-220">(13)</span><span class="sxs-lookup"><span data-stu-id="231d3-220">(13)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-221">сримм</span><span class="sxs-lookup"><span data-stu-id="231d3-221">SRIMM</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-222">(14)</span><span class="sxs-lookup"><span data-stu-id="231d3-222">(14)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-223">смд</span><span class="sxs-lookup"><span data-stu-id="231d3-223">SMD</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-224">(15)</span><span class="sxs-lookup"><span data-stu-id="231d3-224">(15)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-225">ссмп</span><span class="sxs-lookup"><span data-stu-id="231d3-225">SSMP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-226">(16)</span><span class="sxs-lookup"><span data-stu-id="231d3-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-227">кфп</span><span class="sxs-lookup"><span data-stu-id="231d3-227">QFP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-228">(17)</span><span class="sxs-lookup"><span data-stu-id="231d3-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-229">ткфп</span><span class="sxs-lookup"><span data-stu-id="231d3-229">TQFP</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-230">(18)</span><span class="sxs-lookup"><span data-stu-id="231d3-230">(18)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-231">соик</span><span class="sxs-lookup"><span data-stu-id="231d3-231">SOIC</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-232">(19)</span><span class="sxs-lookup"><span data-stu-id="231d3-232">(19)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-233">лкк</span><span class="sxs-lookup"><span data-stu-id="231d3-233">LCC</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-234">(20)</span><span class="sxs-lookup"><span data-stu-id="231d3-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-235">плкк</span><span class="sxs-lookup"><span data-stu-id="231d3-235">PLCC</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-236">(21)</span><span class="sxs-lookup"><span data-stu-id="231d3-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-237">BGA</span><span class="sxs-lookup"><span data-stu-id="231d3-237">BGA</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-238">(22)</span><span class="sxs-lookup"><span data-stu-id="231d3-238">(22)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-239">фпбга</span><span class="sxs-lookup"><span data-stu-id="231d3-239">FPBGA</span></span>

</dd> <dt>



 <span data-ttu-id="231d3-240">(23)</span><span class="sxs-lookup"><span data-stu-id="231d3-240">(23)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-241">LGA</span><span class="sxs-lookup"><span data-stu-id="231d3-241">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="231d3-242">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="231d3-242">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-243">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="231d3-243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231d3-245">Если **значение — true**, этот компонент физического носителя можно заменить физически отличающимся, но эквивалентным, пока содержащий его пакет применялся к питанию.</span><span class="sxs-lookup"><span data-stu-id="231d3-245">If **TRUE**, this physical media component can be replaced with a physically different but equivalent one while the containing package has the power applied.</span></span> <span data-ttu-id="231d3-246">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="231d3-246">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="231d3-247">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="231d3-247">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="231d3-248">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-248">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-249">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="231d3-249">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-250">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="231d3-250">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-251">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-252">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="231d3-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-253">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="231d3-253">Date and time the object is installed.</span></span> <span data-ttu-id="231d3-254">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="231d3-254">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="231d3-255">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-255">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-256">**интерлеаведатадепс**</span><span class="sxs-lookup"><span data-stu-id="231d3-256">**InterleaveDataDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-257">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="231d3-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-259">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| глубина данных SMBIOS типа 20 с \| чередованием")</span><span class="sxs-lookup"><span data-stu-id="231d3-259">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Interleaved Data Depth")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-260">16-разрядное целое число без знака, максимальное количество последовательных строк данных, доступ к которым осуществляется при одном перемещении с устройства памяти с чередованием.</span><span class="sxs-lookup"><span data-stu-id="231d3-260">Unsigned 16-bit integer maximum number of consecutive rows of data that are accessed in a single interleaved transfer from the memory device.</span></span> <span data-ttu-id="231d3-261">Если значение равно 0 (нулю), память не является чередованием.</span><span class="sxs-lookup"><span data-stu-id="231d3-261">If the value is 0 (zero), the memory is not interleaved.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-262">**интерлеавепоситион**</span><span class="sxs-lookup"><span data-stu-id="231d3-262">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-263">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-263">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-265">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Сопоставленные адреса памяти в формате DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="231d3-265">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-266">Расположение физической памяти в чередовании.</span><span class="sxs-lookup"><span data-stu-id="231d3-266">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="231d3-267">Например, в 2:1 чередование значение "1" указывает, что память находится в "четном" положении.</span><span class="sxs-lookup"><span data-stu-id="231d3-267">For example, in a 2:1 interleave, a value of "1" indicates that the memory is in the "even" position.</span></span>

<span data-ttu-id="231d3-268">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-268">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span data-ttu-id="231d3-269">0</span><span class="sxs-lookup"><span data-stu-id="231d3-269">0</span></span>
</dt> <dd>

<span data-ttu-id="231d3-270">Не чередование</span><span class="sxs-lookup"><span data-stu-id="231d3-270">Noninterleaved</span></span>

</dd> <dt>

<span data-ttu-id="231d3-271">1</span><span class="sxs-lookup"><span data-stu-id="231d3-271">1</span></span>
</dt> <dd>

<span data-ttu-id="231d3-272">Первое расположение</span><span class="sxs-lookup"><span data-stu-id="231d3-272">First position</span></span>

</dd> <dt>

<span data-ttu-id="231d3-273">2</span><span class="sxs-lookup"><span data-stu-id="231d3-273">2</span></span>
</dt> <dd>

<span data-ttu-id="231d3-274">Второе расположение</span><span class="sxs-lookup"><span data-stu-id="231d3-274">Second position</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="231d3-275">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="231d3-275">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-276">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-278">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="231d3-278">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-279">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-279">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="231d3-280">Это значение берется из члена структуры **памяти** , **предоставленной производителем** , в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-280">This value comes from the **Manufacturer** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-281">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-281">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-282">**максволтаже**</span><span class="sxs-lookup"><span data-stu-id="231d3-282">**MaxVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-285">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17: \| Максимальное напряжение")</span><span class="sxs-lookup"><span data-stu-id="231d3-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Maximum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-286">Максимальное рабочее напряжение для этого устройства в милливольтах или 0, если напряжение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="231d3-286">The maximum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="231d3-287">Это значение берется из параметра **максимального напряжения** в структуре **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-287">This value comes from the **Maximum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-288">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="231d3-288">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-289">**меморитипе**</span><span class="sxs-lookup"><span data-stu-id="231d3-289">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-290">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="231d3-290">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-292">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. Память DMTF, \| устройство \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="231d3-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-293">Тип физической памяти.</span><span class="sxs-lookup"><span data-stu-id="231d3-293">Type of physical memory.</span></span> <span data-ttu-id="231d3-294">Это значение CIM, сопоставленное со значением SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-294">This is a CIM value that is mapped to the SMBIOS value.</span></span> <span data-ttu-id="231d3-295">Свойство **смбиосмеморитипе** содержит необработанный тип памяти SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-295">The **SMBIOSMemoryType** property contains the raw SMBIOS memory type.</span></span>

<span data-ttu-id="231d3-296">Это значение берется из элемента **типа памяти** структуры **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-296">This value comes from the **Memory Type** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-297">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-297">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="231d3-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="231d3-298"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="231d3-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="231d3-299"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="231d3-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="231d3-300"><span id="DRAM"></span><span id="dram"></span>**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="231d3-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Синхронная DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="231d3-301"><span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="231d3-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Кэш DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="231d3-302"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="231d3-303"><span id="EDO"></span><span id="edo"></span>**Эдо** (5)</span><span class="sxs-lookup"><span data-stu-id="231d3-303"><span id="EDO"></span><span id="edo"></span>**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="231d3-304"><span id="EDRAM"></span><span id="edram"></span>**Едрам** (6)</span><span class="sxs-lookup"><span data-stu-id="231d3-304"><span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="231d3-305"><span id="VRAM"></span><span id="vram"></span>**Видеопамять** (7)</span><span class="sxs-lookup"><span data-stu-id="231d3-305"><span id="VRAM"></span><span id="vram"></span>**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="231d3-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="231d3-306"><span id="SRAM"></span><span id="sram"></span>**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="231d3-307"><span id="RAM"></span><span id="ram"></span>**ОЗУ** (9)</span><span class="sxs-lookup"><span data-stu-id="231d3-307"><span id="RAM"></span><span id="ram"></span>**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="231d3-308"><span id="ROM"></span><span id="rom"></span>**ПЗУ** (10)</span><span class="sxs-lookup"><span data-stu-id="231d3-308"><span id="ROM"></span><span id="rom"></span>**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="231d3-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="231d3-309"><span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="231d3-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="231d3-310"><span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="231d3-311"><span id="FEPROM"></span><span id="feprom"></span>**Фепром** (13)</span><span class="sxs-lookup"><span data-stu-id="231d3-311"><span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="231d3-312"><span id="EPROM"></span><span id="eprom"></span>**Епром** (14)</span><span class="sxs-lookup"><span data-stu-id="231d3-312"><span id="EPROM"></span><span id="eprom"></span>**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="231d3-313"><span id="CDRAM"></span><span id="cdram"></span>**Кдрам** (15)</span><span class="sxs-lookup"><span data-stu-id="231d3-313"><span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="231d3-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="231d3-314"><span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="231d3-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="231d3-315"><span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="231d3-316"><span id="SGRAM"></span><span id="sgram"></span>**Сграм** (18)</span><span class="sxs-lookup"><span data-stu-id="231d3-316"><span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="231d3-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="231d3-317"><span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="231d3-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="231d3-318"><span id="DDR"></span><span id="ddr"></span>**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="231d3-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="231d3-319"><span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-320">DDR2 — может быть недоступна.</span><span class="sxs-lookup"><span data-stu-id="231d3-320">DDR2—May not be available.</span></span>

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="231d3-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="231d3-321"><span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-322">Память DDR2 (FB-DIMM) может быть недоступна.</span><span class="sxs-lookup"><span data-stu-id="231d3-322">DDR2—FB-DIMM,May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-323">24</span><span class="sxs-lookup"><span data-stu-id="231d3-323">24</span></span>
</dt> <dd>

<span data-ttu-id="231d3-324">DDR3 — может быть недоступна.</span><span class="sxs-lookup"><span data-stu-id="231d3-324">DDR3—May not be available.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-325">25</span><span class="sxs-lookup"><span data-stu-id="231d3-325">25</span></span>
</dt> <dd>

<span data-ttu-id="231d3-326">FBD2</span><span class="sxs-lookup"><span data-stu-id="231d3-326">FBD2</span></span>

</dt> <dd></dd> <dt>

<span data-ttu-id="231d3-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span><span class="sxs-lookup"><span data-stu-id="231d3-327"><span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="231d3-328">**минволтаже**</span><span class="sxs-lookup"><span data-stu-id="231d3-328">**MinVoltage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-329">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-331">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 20 \| минимальное напряжение")</span><span class="sxs-lookup"><span data-stu-id="231d3-331">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 20\|Minimum voltage")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-332">Минимальное рабочее напряжение для этого устройства в милливольтах или 0, если напряжение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="231d3-332">The minimum operating voltage for this device, in millivolts, or 0, if the voltage is unknown.</span></span>

<span data-ttu-id="231d3-333">Это значение берется из **минимального напряжения** , входящего в структуру **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-333">This value comes from the **Minimum voltage** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-334">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="231d3-334">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-335">**Модель**</span><span class="sxs-lookup"><span data-stu-id="231d3-335">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-338">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="231d3-338">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-339">Имя физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-339">Name for the physical element.</span></span>

<span data-ttu-id="231d3-340">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-340">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-341">**Name**</span><span class="sxs-lookup"><span data-stu-id="231d3-341">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-344">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="231d3-344">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-345">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="231d3-345">Label for the object.</span></span> <span data-ttu-id="231d3-346">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="231d3-346">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="231d3-347">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-348">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="231d3-348">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231d3-351">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-351">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="231d3-352">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="231d3-352">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="231d3-353">Если только данные штрих-кода доступны и уникальны или могут использоваться в качестве ключа элемента, это свойство имеет **значение NULL** , а данные штрих-кода используются в качестве ключа класса в свойстве Tag.</span><span class="sxs-lookup"><span data-stu-id="231d3-353">If only bar code data is available and unique or able to be used as an element key, this property is be **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="231d3-354">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-355">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="231d3-355">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-356">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-358">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="231d3-358">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-359">Номер детали, назначенный Организацией, ответственной за производство или производство физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-359">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="231d3-360">Это значение берется из **номера части** в структуре **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-360">This value comes from the **Part Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-361">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-361">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-362">**поситионинров**</span><span class="sxs-lookup"><span data-stu-id="231d3-362">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-363">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-363">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-365">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Сопоставленные адреса памяти в формате DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="231d3-365">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-366">Расположение физической памяти в строке.</span><span class="sxs-lookup"><span data-stu-id="231d3-366">Position of the physical memory in a row.</span></span> <span data-ttu-id="231d3-367">Например, если для формирования 16-битной строки требуется 2 8-разрядное устройство памяти, то значение 2 (два) означает, что память является вторым устройством — 0 (нуль) — недопустимое значение для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="231d3-367">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 (two) means that this memory is the second device—0 (zero) is an invalid value for this property.</span></span>

<span data-ttu-id="231d3-368">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-368">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-369">**повередон**</span><span class="sxs-lookup"><span data-stu-id="231d3-369">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-370">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="231d3-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231d3-372">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="231d3-372">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="231d3-373">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-373">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-374">**Службе**</span><span class="sxs-lookup"><span data-stu-id="231d3-374">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-375">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="231d3-375">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231d3-377">Если **значение равно true**, физический компонент является съемным (если он предназначен для извлечения и выхода из физического контейнера, в котором он обычно обнаруживается, без нарушения функции общей упаковки).</span><span class="sxs-lookup"><span data-stu-id="231d3-377">If **TRUE**, a physical component is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="231d3-378">Компонент по-прежнему может быть съемным, если для его удаления необходимо выключить питание.</span><span class="sxs-lookup"><span data-stu-id="231d3-378">A component can still be removable if power must be "off" to perform the removal.</span></span> <span data-ttu-id="231d3-379">Если мощность может быть "on" и компонент удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="231d3-379">If power can be "on" and the component removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="231d3-380">Например, обновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="231d3-380">For example, an upgradable processor chip is removable.</span></span>

<span data-ttu-id="231d3-381">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-381">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-382">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="231d3-382">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-383">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="231d3-383">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="231d3-385">Если **значение — true**, этот компонент физического носителя можно заменить физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="231d3-385">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="231d3-386">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="231d3-386">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="231d3-387">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="231d3-387">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="231d3-388">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="231d3-388">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="231d3-389">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-389">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-390">**Номер**</span><span class="sxs-lookup"><span data-stu-id="231d3-390">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-393">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="231d3-393">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-394">Номер, выделенный изготовителем для обнаружения физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-394">Manufacturer-allocated number to identify the physical element.</span></span>

<span data-ttu-id="231d3-395">Это значение берется из **серийного номера** в структуре **устройств памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-395">This value comes from the **Serial Number** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-396">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-396">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-397">**SKU**</span><span class="sxs-lookup"><span data-stu-id="231d3-397">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-398">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-400">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="231d3-400">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-401">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-401">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="231d3-402">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-402">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-403">**смбиосмеморитипе**</span><span class="sxs-lookup"><span data-stu-id="231d3-403">**SMBIOSMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-404">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-406">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17 \| \_ Тип памяти")</span><span class="sxs-lookup"><span data-stu-id="231d3-406">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Memory\_Type")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-407">Необработанный тип памяти SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-407">The raw SMBIOS memory type.</span></span> <span data-ttu-id="231d3-408">Значение свойства **меморитипе** является значением CIM, сопоставленным со значением SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-408">The value of the **MemoryType** property is a CIM value that is mapped to the SMBIOS value.</span></span>

<span data-ttu-id="231d3-409">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="231d3-409">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="231d3-410">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="231d3-410">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-411">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="231d3-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-413">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("наносекундах")</span><span class="sxs-lookup"><span data-stu-id="231d3-413">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-414">Скорость физической памяти — в наносекундах.</span><span class="sxs-lookup"><span data-stu-id="231d3-414">Speed of the physical memory—in nanoseconds.</span></span>

<span data-ttu-id="231d3-415">Это значение берется из элемента **Speed** структуры **памяти устройства** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-415">This value comes from the **Speed** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-416">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-416">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-417">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="231d3-417">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-420">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="231d3-420">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-421">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="231d3-421">Current status of the object.</span></span> <span data-ttu-id="231d3-422">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="231d3-422">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="231d3-423">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="231d3-423">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="231d3-424">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="231d3-424">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="231d3-425">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="231d3-425">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="231d3-426">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="231d3-426">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="231d3-427">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-427">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="231d3-428">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="231d3-428">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="231d3-429">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="231d3-429">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="231d3-430">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="231d3-430">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="231d3-431">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="231d3-431">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="231d3-432">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="231d3-432">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="231d3-433">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="231d3-433">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="231d3-434">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="231d3-434">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="231d3-435">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="231d3-435">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="231d3-436">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="231d3-436">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="231d3-437">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="231d3-437">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="231d3-438">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="231d3-438">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="231d3-439">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="231d3-439">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="231d3-440">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="231d3-440">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="231d3-441">**Тег**</span><span class="sxs-lookup"><span data-stu-id="231d3-441">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-444">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="231d3-444">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-445">Уникальный идентификатор устройства физической памяти, представленный экземпляром **Win32 \_ фисикалмемори**.</span><span class="sxs-lookup"><span data-stu-id="231d3-445">Unique identifier for the physical memory device that is represented by an instance of **Win32\_PhysicalMemory**.</span></span> <span data-ttu-id="231d3-446">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-446">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="231d3-447">Пример: "физическая память 1"</span><span class="sxs-lookup"><span data-stu-id="231d3-447">Example: "Physical Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="231d3-448">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="231d3-448">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-449">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="231d3-449">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-451">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Memory Device \| 002,7 "), [**Units**](../wmisdk/standard-qualifiers.md) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="231d3-451">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-452">Общая ширина физической памяти в битах, включая биты проверки или исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="231d3-452">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="231d3-453">Если биты исправления ошибок отсутствуют, значение в этом свойстве должно соответствовать значению свойства « **Ширина** данных».</span><span class="sxs-lookup"><span data-stu-id="231d3-453">If there are no error correction bits, the value in this property should match what is specified for the **DataWidth** property.</span></span>

<span data-ttu-id="231d3-454">Это значение берется из **общей ширины** элемента структуры **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-454">This value comes from the **Total Width** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<span data-ttu-id="231d3-455">Это свойство наследуется от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-455">This property is inherited from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="231d3-456">**типедетаил**</span><span class="sxs-lookup"><span data-stu-id="231d3-456">**TypeDetail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-457">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="231d3-457">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-459">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 17 \| сведения о типе")</span><span class="sxs-lookup"><span data-stu-id="231d3-459">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 17\|Type Detail")</span></span>
</dt> </dl>

<span data-ttu-id="231d3-460">Тип представленной физической памяти.</span><span class="sxs-lookup"><span data-stu-id="231d3-460">Type of physical memory represented.</span></span>

<span data-ttu-id="231d3-461">Это значение берется из элемента **сведения о типе** в структуре **устройства памяти** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="231d3-461">This value comes from the **Type Detail** member of the **Memory Device** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="231d3-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Зарезервировано** (1)</span><span class="sxs-lookup"><span data-stu-id="231d3-462"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="231d3-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (2)</span><span class="sxs-lookup"><span data-stu-id="231d3-463"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="231d3-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (4)</span><span class="sxs-lookup"><span data-stu-id="231d3-464"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span data-ttu-id="231d3-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**С быстрой накачки** (8)</span><span class="sxs-lookup"><span data-stu-id="231d3-465"><span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Fast-paged** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span data-ttu-id="231d3-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Статический столбец** (16)</span><span class="sxs-lookup"><span data-stu-id="231d3-466"><span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Static column** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span data-ttu-id="231d3-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Псевдо-static** (32)</span><span class="sxs-lookup"><span data-stu-id="231d3-467"><span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-static** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span data-ttu-id="231d3-468"><span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)</span><span class="sxs-lookup"><span data-stu-id="231d3-468"><span id="RAMBUS"></span><span id="rambus"></span>**RAMBUS** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="231d3-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Синхронный** (128)</span><span class="sxs-lookup"><span data-stu-id="231d3-469"><span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Synchronous** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span data-ttu-id="231d3-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span><span class="sxs-lookup"><span data-stu-id="231d3-470"><span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="231d3-471"><span id="EDO"></span><span id="edo"></span>**Эдо** (512)</span><span class="sxs-lookup"><span data-stu-id="231d3-471"><span id="EDO"></span><span id="edo"></span>**EDO** (512)</span></span>


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span data-ttu-id="231d3-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Окно DRAM** (1024)</span><span class="sxs-lookup"><span data-stu-id="231d3-472"><span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**Window DRAM** (1024)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="231d3-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Кэш DRAM** (2048)</span><span class="sxs-lookup"><span data-stu-id="231d3-473"><span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**Cache DRAM** (2048)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span data-ttu-id="231d3-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Без постоянного** (4096)</span><span class="sxs-lookup"><span data-stu-id="231d3-474"><span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Non-volatile** (4096)</span></span>


</dt> <dd>

<span data-ttu-id="231d3-475">Неизменяемый</span><span class="sxs-lookup"><span data-stu-id="231d3-475">Nonvolatile</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="231d3-476">**Version**</span><span class="sxs-lookup"><span data-stu-id="231d3-476">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="231d3-477">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="231d3-477">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="231d3-478">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="231d3-478">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="231d3-479">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="231d3-479">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="231d3-480">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="231d3-480">Version of the physical element.</span></span>

<span data-ttu-id="231d3-481">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-481">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="231d3-482">Комментарии</span><span class="sxs-lookup"><span data-stu-id="231d3-482">Remarks</span></span>

<span data-ttu-id="231d3-483">Класс **Win32 \_ фисикалмемори** является производным от [**CIM \_ фисикалмемори**](cim-physicalmemory.md).</span><span class="sxs-lookup"><span data-stu-id="231d3-483">The **Win32\_PhysicalMemory** class is derived from [**CIM\_PhysicalMemory**](cim-physicalmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="231d3-484">Примеры</span><span class="sxs-lookup"><span data-stu-id="231d3-484">Examples</span></span>

<span data-ttu-id="231d3-485">Пример " [Get-компутеринфо-запрос компьютера с локального/удаленного компьютера" (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell в коллекции TechNet использует несколько вызовов оборудования и программного обеспечения, включая **Win32 \_ фисикалмемори**, для вывода сведений о локальной или удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="231d3-485">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to display information about a local or remote system.</span></span>

<span data-ttu-id="231d3-486">Пример [серверного отчета](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell в коллекции TechNet использует ряд вызовов к оборудованию и программному обеспечению, включая **Win32 \_ фисикалмемори**, для сбора сведений о сервере и публикации в документе Word.</span><span class="sxs-lookup"><span data-stu-id="231d3-486">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet gallery uses a number of calls to hardware and software, including **Win32\_PhysicalMemory**, to gather server information and publish in Word document.</span></span>

<span data-ttu-id="231d3-487">Следующий пример кода PowerShell извлекает сведения о физической памяти локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="231d3-487">The following PowerShell code sample retrieves information regarding the physical memory of the local computer.</span></span>


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



## <a name="requirements"></a><span data-ttu-id="231d3-488">Требования</span><span class="sxs-lookup"><span data-stu-id="231d3-488">Requirements</span></span>



| <span data-ttu-id="231d3-489">Требование</span><span class="sxs-lookup"><span data-stu-id="231d3-489">Requirement</span></span> | <span data-ttu-id="231d3-490">Значение</span><span class="sxs-lookup"><span data-stu-id="231d3-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="231d3-491">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="231d3-491">Minimum supported client</span></span><br/> | <span data-ttu-id="231d3-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="231d3-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="231d3-493">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="231d3-493">Minimum supported server</span></span><br/> | <span data-ttu-id="231d3-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="231d3-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="231d3-495">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="231d3-495">Namespace</span></span><br/>                | <span data-ttu-id="231d3-496">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="231d3-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="231d3-497">MOF</span><span class="sxs-lookup"><span data-stu-id="231d3-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="231d3-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="231d3-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="231d3-499">DLL</span><span class="sxs-lookup"><span data-stu-id="231d3-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="231d3-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="231d3-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="231d3-501">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="231d3-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231d3-502">**\_ФИСИКАЛМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="231d3-502">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dt>

[<span data-ttu-id="231d3-503">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="231d3-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
