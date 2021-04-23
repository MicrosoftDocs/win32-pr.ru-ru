---
description: Класс CIM \_ фисикалмемори представляет устройства памяти низкого уровня, такие как SIMM, модули DIMM, микросхемы памяти и т. д.
ms.assetid: a25c5f00-cd85-42e6-9b26-8e9380b3c73b
ms.tgt_platform: multiple
title: Класс CIM_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalMemory
- CIM_PhysicalMemory.BankLabel
- CIM_PhysicalMemory.Capacity
- CIM_PhysicalMemory.Caption
- CIM_PhysicalMemory.CreationClassName
- CIM_PhysicalMemory.DataWidth
- CIM_PhysicalMemory.Description
- CIM_PhysicalMemory.FormFactor
- CIM_PhysicalMemory.HotSwappable
- CIM_PhysicalMemory.InstallDate
- CIM_PhysicalMemory.InterleavePosition
- CIM_PhysicalMemory.Manufacturer
- CIM_PhysicalMemory.MemoryType
- CIM_PhysicalMemory.Model
- CIM_PhysicalMemory.Name
- CIM_PhysicalMemory.OtherIdentifyingInfo
- CIM_PhysicalMemory.PartNumber
- CIM_PhysicalMemory.PositionInRow
- CIM_PhysicalMemory.PoweredOn
- CIM_PhysicalMemory.Removable
- CIM_PhysicalMemory.Replaceable
- CIM_PhysicalMemory.SerialNumber
- CIM_PhysicalMemory.SKU
- CIM_PhysicalMemory.Speed
- CIM_PhysicalMemory.Status
- CIM_PhysicalMemory.Tag
- CIM_PhysicalMemory.TotalWidth
- CIM_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bd46ebde99ae6c6d9e28975d67563424619db84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896302"
---
# <a name="cim_physicalmemory-class"></a><span data-ttu-id="f61f6-103">\_Класс CIM фисикалмемори</span><span class="sxs-lookup"><span data-stu-id="f61f6-103">CIM\_PhysicalMemory class</span></span>

<span data-ttu-id="f61f6-104">Класс **CIM \_ фисикалмемори** представляет устройства памяти низкого уровня, такие как SIMM, модули DIMM, микросхемы памяти и т. д.</span><span class="sxs-lookup"><span data-stu-id="f61f6-104">The **CIM\_PhysicalMemory** class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f61f6-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f61f6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f61f6-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f61f6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f61f6-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f61f6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f61f6-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f61f6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61f6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f61f6-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B7B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalMemory : CIM_Chip
{
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint16   MemoryType;
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
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="f61f6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f61f6-110">Members</span></span>

<span data-ttu-id="f61f6-111">Класс **CIM \_ фисикалмемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f61f6-111">The **CIM\_PhysicalMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="f61f6-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f61f6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f61f6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f61f6-113">Properties</span></span>

<span data-ttu-id="f61f6-114">Класс **CIM \_ фисикалмемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f61f6-114">The **CIM\_PhysicalMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f61f6-115">**банклабел**</span><span class="sxs-lookup"><span data-stu-id="f61f6-115">**BankLabel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Память DMTF, \| устройство \| 002,4 ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-119">Помеченный банком банк, в котором находится память.</span><span class="sxs-lookup"><span data-stu-id="f61f6-119">Labeled bank in which the memory is located.</span></span> <span data-ttu-id="f61f6-120">Например, "Bank 0" или "Bank A".</span><span class="sxs-lookup"><span data-stu-id="f61f6-120">For example, "Bank 0" or "Bank A".</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-121">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="f61f6-121">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-122">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f61f6-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-124">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,5 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-125">Общая емкость физической памяти в байтах.</span><span class="sxs-lookup"><span data-stu-id="f61f6-125">Total capacity of the physical memory, in bytes.</span></span>

<span data-ttu-id="f61f6-126">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f61f6-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-127">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f61f6-127">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-130">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f61f6-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-131">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f61f6-131">Short textual description of the object.</span></span>

<span data-ttu-id="f61f6-132">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-133">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f61f6-133">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-136">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f61f6-136">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-137">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f61f6-137">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f61f6-138">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f61f6-138">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f61f6-139">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-139">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-140">**DataWidth**</span><span class="sxs-lookup"><span data-stu-id="f61f6-140">**DataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f61f6-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,8 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-144">Ширина данных физической памяти в битах.</span><span class="sxs-lookup"><span data-stu-id="f61f6-144">Data width of the physical memory, in bits.</span></span> <span data-ttu-id="f61f6-145">Ширина данных 0 (ноль) и суммарная ширина 8 означает, что память используется исключительно для обеспечения битов исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="f61f6-145">A data width of 0 (zero) , and a total width of 8, indicates that the memory is solely used to provide error correction bits.</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f61f6-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-149">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f61f6-149">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-150">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f61f6-150">Textual description of the object.</span></span>

<span data-ttu-id="f61f6-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-152">**формфактор**</span><span class="sxs-lookup"><span data-stu-id="f61f6-152">**FormFactor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-153">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f61f6-153">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-155">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("формфактор"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Память DMTF, \| устройство \| 002,6 ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-155">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("FormFactor"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-156">Конструктивный фактор для микросхемы.</span><span class="sxs-lookup"><span data-stu-id="f61f6-156">Implementation form factor for the chip.</span></span> <span data-ttu-id="f61f6-157">Например, можно указать значения SIMM, ТСОП или PGA.</span><span class="sxs-lookup"><span data-stu-id="f61f6-157">For example, values such as SIMM, TSOP, or PGA can be specified.</span></span>

<span data-ttu-id="f61f6-158">Это свойство наследуется [**от \_ микросхемы CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-158">This property is inherited from [**CIM\_Chip**](cim-chip.md).</span></span>

<dt>

<span data-ttu-id="f61f6-159">0</span><span class="sxs-lookup"><span data-stu-id="f61f6-159">0</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-160">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="f61f6-160">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-161">1</span><span class="sxs-lookup"><span data-stu-id="f61f6-161">1</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-162">Другое</span><span class="sxs-lookup"><span data-stu-id="f61f6-162">Other</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-163">2</span><span class="sxs-lookup"><span data-stu-id="f61f6-163">2</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-164">ПАНЕЛЬ</span><span class="sxs-lookup"><span data-stu-id="f61f6-164">SIP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-165">3</span><span class="sxs-lookup"><span data-stu-id="f61f6-165">3</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-166">DIP</span><span class="sxs-lookup"><span data-stu-id="f61f6-166">DIP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-167">4</span><span class="sxs-lookup"><span data-stu-id="f61f6-167">4</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-168">ZIP</span><span class="sxs-lookup"><span data-stu-id="f61f6-168">ZIP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-169">5</span><span class="sxs-lookup"><span data-stu-id="f61f6-169">5</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-170">сож</span><span class="sxs-lookup"><span data-stu-id="f61f6-170">SOJ</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-171">6</span><span class="sxs-lookup"><span data-stu-id="f61f6-171">6</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-172">Частный</span><span class="sxs-lookup"><span data-stu-id="f61f6-172">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-173">7</span><span class="sxs-lookup"><span data-stu-id="f61f6-173">7</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-174">Банк</span><span class="sxs-lookup"><span data-stu-id="f61f6-174">SIMM</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-175">8</span><span class="sxs-lookup"><span data-stu-id="f61f6-175">8</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-176">ДОСТУП</span><span class="sxs-lookup"><span data-stu-id="f61f6-176">DIMM</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-177">9</span><span class="sxs-lookup"><span data-stu-id="f61f6-177">9</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-178">тсоп</span><span class="sxs-lookup"><span data-stu-id="f61f6-178">TSOP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-179">10</span><span class="sxs-lookup"><span data-stu-id="f61f6-179">10</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-180">FCPGA</span><span class="sxs-lookup"><span data-stu-id="f61f6-180">PGA</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-181">11</span><span class="sxs-lookup"><span data-stu-id="f61f6-181">11</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-182">RIMM</span><span class="sxs-lookup"><span data-stu-id="f61f6-182">RIMM</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-183">12</span><span class="sxs-lookup"><span data-stu-id="f61f6-183">12</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-184">содимм</span><span class="sxs-lookup"><span data-stu-id="f61f6-184">SODIMM</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-185">13</span><span class="sxs-lookup"><span data-stu-id="f61f6-185">13</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-186">сримм</span><span class="sxs-lookup"><span data-stu-id="f61f6-186">SRIMM</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-187">14</span><span class="sxs-lookup"><span data-stu-id="f61f6-187">14</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-188">смд</span><span class="sxs-lookup"><span data-stu-id="f61f6-188">SMD</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-189">15</span><span class="sxs-lookup"><span data-stu-id="f61f6-189">15</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-190">ссмп</span><span class="sxs-lookup"><span data-stu-id="f61f6-190">SSMP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-191">16</span><span class="sxs-lookup"><span data-stu-id="f61f6-191">16</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-192">кфп</span><span class="sxs-lookup"><span data-stu-id="f61f6-192">QFP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-193">17</span><span class="sxs-lookup"><span data-stu-id="f61f6-193">17</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-194">ткфп</span><span class="sxs-lookup"><span data-stu-id="f61f6-194">TQFP</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-195">18</span><span class="sxs-lookup"><span data-stu-id="f61f6-195">18</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-196">соик</span><span class="sxs-lookup"><span data-stu-id="f61f6-196">SOIC</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-197">19</span><span class="sxs-lookup"><span data-stu-id="f61f6-197">19</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-198">лкк</span><span class="sxs-lookup"><span data-stu-id="f61f6-198">LCC</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-199">20</span><span class="sxs-lookup"><span data-stu-id="f61f6-199">20</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-200">плкк</span><span class="sxs-lookup"><span data-stu-id="f61f6-200">PLCC</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-201">21</span><span class="sxs-lookup"><span data-stu-id="f61f6-201">21</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-202">BGA</span><span class="sxs-lookup"><span data-stu-id="f61f6-202">BGA</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-203">22</span><span class="sxs-lookup"><span data-stu-id="f61f6-203">22</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-204">фпбга</span><span class="sxs-lookup"><span data-stu-id="f61f6-204">FPBGA</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-205">23</span><span class="sxs-lookup"><span data-stu-id="f61f6-205">23</span></span>
</dt> <dd>

<span data-ttu-id="f61f6-206">LGA</span><span class="sxs-lookup"><span data-stu-id="f61f6-206">LGA</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f61f6-207">**хотсваппабле**</span><span class="sxs-lookup"><span data-stu-id="f61f6-207">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-208">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f61f6-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-210">Если задано **значение true**, пакет может быть горячим заменой.</span><span class="sxs-lookup"><span data-stu-id="f61f6-210">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="f61f6-211">Физический пакет может быть горячим заменой, если элемент может быть заменен физически другим (но эквивалентным) одним во время включения содержащего пакета.</span><span class="sxs-lookup"><span data-stu-id="f61f6-211">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="f61f6-212">Например, компонент вентилятора может быть рассчитан на горячую замену.</span><span class="sxs-lookup"><span data-stu-id="f61f6-212">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="f61f6-213">Все компоненты, доступные для горячей замены, по сути являются съемными и заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="f61f6-213">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="f61f6-214">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-214">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f61f6-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-216">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f61f6-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-218">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-218">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-219">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="f61f6-219">Date and time the object was installed.</span></span> <span data-ttu-id="f61f6-220">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="f61f6-220">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f61f6-221">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-222">**интерлеавепоситион**</span><span class="sxs-lookup"><span data-stu-id="f61f6-222">**InterleavePosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-223">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f61f6-223">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-225">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сопоставленные адреса памяти в формате DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-226">Расположение физической памяти в чередовании.</span><span class="sxs-lookup"><span data-stu-id="f61f6-226">Position of the physical memory in an interleave.</span></span> <span data-ttu-id="f61f6-227">Значение 0 указывает на не чередование, 1 указывает на первую точку, 2 — на вторую и т. д.</span><span class="sxs-lookup"><span data-stu-id="f61f6-227">A value of 0 indicates non-interleaved, 1 indicates the first position, 2 indicates the second position, and so on.</span></span> <span data-ttu-id="f61f6-228">Например, в 2:1 чередование значение 1 указывает, что память находится в четном положении.</span><span class="sxs-lookup"><span data-stu-id="f61f6-228">For example, in a 2:1 interleave, a value of 1 indicates that the memory is in the even position.</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-229">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="f61f6-229">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-232">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f61f6-232">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-233">Имя Организации, ответственной за создание физического элемента.</span><span class="sxs-lookup"><span data-stu-id="f61f6-233">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="f61f6-234">Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-234">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="f61f6-235">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-235">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-236">**меморитипе**</span><span class="sxs-lookup"><span data-stu-id="f61f6-236">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-237">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f61f6-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-239">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. Память DMTF, \| устройство \| 002,9 ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-239">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.9")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-240">Тип физической памяти.</span><span class="sxs-lookup"><span data-stu-id="f61f6-240">Type of physical memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f61f6-241">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f61f6-241">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f61f6-242">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f61f6-242">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="f61f6-243">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="f61f6-243">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="f61f6-244">**Синхронная DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="f61f6-244">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="f61f6-245">**Кэш DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="f61f6-245">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="f61f6-246">**Эдо** (5)</span><span class="sxs-lookup"><span data-stu-id="f61f6-246">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="f61f6-247">**Едрам** (6)</span><span class="sxs-lookup"><span data-stu-id="f61f6-247">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="f61f6-248">**Видеопамять** (7)</span><span class="sxs-lookup"><span data-stu-id="f61f6-248">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="f61f6-249">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="f61f6-249">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="f61f6-250">**ОЗУ** (9)</span><span class="sxs-lookup"><span data-stu-id="f61f6-250">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="f61f6-251">**ПЗУ** (10)</span><span class="sxs-lookup"><span data-stu-id="f61f6-251">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="f61f6-252">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="f61f6-252">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="f61f6-253">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="f61f6-253">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="f61f6-254">**Фепром** (13)</span><span class="sxs-lookup"><span data-stu-id="f61f6-254">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="f61f6-255">**Епром** (14)</span><span class="sxs-lookup"><span data-stu-id="f61f6-255">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="f61f6-256">**Кдрам** (15)</span><span class="sxs-lookup"><span data-stu-id="f61f6-256">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="f61f6-257">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="f61f6-257">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="f61f6-258">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="f61f6-258">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="f61f6-259">**Сграм** (18)</span><span class="sxs-lookup"><span data-stu-id="f61f6-259">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="f61f6-260">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="f61f6-260">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="f61f6-261">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="f61f6-261">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span data-ttu-id="f61f6-262">**DDR2** (21)</span><span class="sxs-lookup"><span data-stu-id="f61f6-262">**DDR2** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span data-ttu-id="f61f6-263">**DDR2 FB-DIMM** (22)</span><span class="sxs-lookup"><span data-stu-id="f61f6-263">**DDR2 FB-DIMM** (22)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f61f6-264">**Модель**</span><span class="sxs-lookup"><span data-stu-id="f61f6-264">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-265">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-267">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f61f6-267">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-268">Имя, по которому обычно известен физический элемент.</span><span class="sxs-lookup"><span data-stu-id="f61f6-268">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="f61f6-269">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-269">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-270">**Name**</span><span class="sxs-lookup"><span data-stu-id="f61f6-270">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-273">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f61f6-273">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-274">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f61f6-274">Label by which the object is known.</span></span> <span data-ttu-id="f61f6-275">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f61f6-275">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f61f6-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-277">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="f61f6-277">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-279">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-280">Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента.</span><span class="sxs-lookup"><span data-stu-id="f61f6-280">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="f61f6-281">Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива.</span><span class="sxs-lookup"><span data-stu-id="f61f6-281">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="f61f6-282">Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .</span><span class="sxs-lookup"><span data-stu-id="f61f6-282">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span> <span data-ttu-id="f61f6-283">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-283">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-284">**партнумбер**</span><span class="sxs-lookup"><span data-stu-id="f61f6-284">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-287">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f61f6-287">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-288">Номер детали, назначенный Организацией, которая создала или изготовлена физический элемент.</span><span class="sxs-lookup"><span data-stu-id="f61f6-288">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="f61f6-289">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-289">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-290">**поситионинров**</span><span class="sxs-lookup"><span data-stu-id="f61f6-290">**PositionInRow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-291">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f61f6-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-293">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сопоставленные адреса памяти в формате DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-293">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device Mapped Addresses\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-294">Расположение физической памяти в строке.</span><span class="sxs-lookup"><span data-stu-id="f61f6-294">Position of the physical memory in a row.</span></span> <span data-ttu-id="f61f6-295">Например, если для формирования 16-битной строки требуется 2 8-разрядное устройство памяти, значение 2 указывает, что память является вторым устройством.</span><span class="sxs-lookup"><span data-stu-id="f61f6-295">For example, if it takes two 8-bit memory devices to form a 16-bit row, then a value of 2 indicates that the memory is the second device.</span></span> <span data-ttu-id="f61f6-296">Значение 0 является недопустимым значением для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f61f6-296">A value of 0 is an invalid value for this property.</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-297">**повередон**</span><span class="sxs-lookup"><span data-stu-id="f61f6-297">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-298">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f61f6-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-300">**Значение true** показывает, что физический элемент включен.</span><span class="sxs-lookup"><span data-stu-id="f61f6-300">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="f61f6-301">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-301">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-302">**Службе**</span><span class="sxs-lookup"><span data-stu-id="f61f6-302">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-303">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f61f6-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-305">Если **значение — true**, этот элемент предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается и из него, без нарушения функций общей упаковки.</span><span class="sxs-lookup"><span data-stu-id="f61f6-305">If **TRUE**, this element is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="f61f6-306">Пакет считается съемным, даже если питание должно быть выключено для выполнения удаления.</span><span class="sxs-lookup"><span data-stu-id="f61f6-306">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="f61f6-307">Если мощность может быть включена и пакет удален, то элемент является съемным и может быть горячей заменой.</span><span class="sxs-lookup"><span data-stu-id="f61f6-307">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="f61f6-308">Например, необновляемая Микросхема процессора является съемной.</span><span class="sxs-lookup"><span data-stu-id="f61f6-308">For example, an ungradable processor chip is removable.</span></span>

<span data-ttu-id="f61f6-309">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-309">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-310">**Заменяемый**</span><span class="sxs-lookup"><span data-stu-id="f61f6-310">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-311">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f61f6-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-313">Если **значение — true**, элемент может быть заменен физически отличающимся.</span><span class="sxs-lookup"><span data-stu-id="f61f6-313">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="f61f6-314">Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок.</span><span class="sxs-lookup"><span data-stu-id="f61f6-314">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="f61f6-315">В этом случае процессор считается заменяемым.</span><span class="sxs-lookup"><span data-stu-id="f61f6-315">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="f61f6-316">Все съемные компоненты по сути являются заменяемыми.</span><span class="sxs-lookup"><span data-stu-id="f61f6-316">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="f61f6-317">Это свойство наследуется от [**CIM \_ фисикалкомпонент**](cim-physicalcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-317">This property is inherited from [**CIM\_PhysicalComponent**](cim-physicalcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-318">**Номер**</span><span class="sxs-lookup"><span data-stu-id="f61f6-318">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-321">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f61f6-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-322">Номер, выделенный изготовителем, используемый для распознавания физического элемента.</span><span class="sxs-lookup"><span data-stu-id="f61f6-322">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="f61f6-323">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-323">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-324">**SKU**</span><span class="sxs-lookup"><span data-stu-id="f61f6-324">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-327">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f61f6-327">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-328">Номер единицы хранения для физического элемента.</span><span class="sxs-lookup"><span data-stu-id="f61f6-328">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="f61f6-329">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-329">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-330">**Скорость**</span><span class="sxs-lookup"><span data-stu-id="f61f6-330">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-331">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f61f6-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-333">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("наносекундах")</span><span class="sxs-lookup"><span data-stu-id="f61f6-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-334">Скорость физической памяти (в наносекундах).</span><span class="sxs-lookup"><span data-stu-id="f61f6-334">Speed of the physical memory, in nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-335">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f61f6-335">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-338">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f61f6-338">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-339">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f61f6-339">Current status of the object.</span></span> <span data-ttu-id="f61f6-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f61f6-341">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f61f6-341">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f61f6-342">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f61f6-342">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f61f6-343">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f61f6-343">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f61f6-344">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f61f6-344">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f61f6-345">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f61f6-345">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f61f6-346">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f61f6-346">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f61f6-347">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f61f6-347">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f61f6-348">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f61f6-348">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f61f6-349">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f61f6-349">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f61f6-350">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f61f6-350">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f61f6-351">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f61f6-351">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f61f6-352">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f61f6-352">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f61f6-353">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f61f6-353">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f61f6-354">**Тег**</span><span class="sxs-lookup"><span data-stu-id="f61f6-354">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-357">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f61f6-357">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-358">Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента.</span><span class="sxs-lookup"><span data-stu-id="f61f6-358">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="f61f6-359">Это свойство может содержать такие сведения, как тег актива или данные серийного номера.</span><span class="sxs-lookup"><span data-stu-id="f61f6-359">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="f61f6-360">Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности, независимо от физического размещения в (или в) шкафов, адаптеров и т. д.</span><span class="sxs-lookup"><span data-stu-id="f61f6-360">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="f61f6-361">Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется.</span><span class="sxs-lookup"><span data-stu-id="f61f6-361">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="f61f6-362">Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области.</span><span class="sxs-lookup"><span data-stu-id="f61f6-362">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="f61f6-363">Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.</span><span class="sxs-lookup"><span data-stu-id="f61f6-363">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="f61f6-364">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-364">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-365">**TotalWidth**</span><span class="sxs-lookup"><span data-stu-id="f61f6-365">**TotalWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-366">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f61f6-366">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-368">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,7 "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" BITS ")</span><span class="sxs-lookup"><span data-stu-id="f61f6-368">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-369">Общая ширина физической памяти в битах, включая биты проверки или исправления ошибок.</span><span class="sxs-lookup"><span data-stu-id="f61f6-369">Total width, in bits, of the physical memory, including check or error correction bits.</span></span> <span data-ttu-id="f61f6-370">Если биты исправления ошибок отсутствуют, значение в этом свойстве должно соответствовать значению, указанному для свойства **Width** .</span><span class="sxs-lookup"><span data-stu-id="f61f6-370">If there are no error correction bits, the value in this property should match that specified for the **DataWidth** property.</span></span>

</dd> <dt>

<span data-ttu-id="f61f6-371">**Version**</span><span class="sxs-lookup"><span data-stu-id="f61f6-371">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f61f6-372">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f61f6-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f61f6-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f61f6-374">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f61f6-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f61f6-375">Версия физического элемента.</span><span class="sxs-lookup"><span data-stu-id="f61f6-375">Version of the physical element.</span></span>

<span data-ttu-id="f61f6-376">Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-376">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f61f6-377">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f61f6-377">Remarks</span></span>

<span data-ttu-id="f61f6-378">Класс **CIM \_ фисикалмемори** является производным от [**\_ микросхемы CIM**](cim-chip.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-378">The **CIM\_PhysicalMemory** class is derived from [**CIM\_Chip**](cim-chip.md).</span></span>

<span data-ttu-id="f61f6-379">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f61f6-379">WMI does not implement this class.</span></span> <span data-ttu-id="f61f6-380">Классы WMI, производные от **CIM \_ фисикалмемори**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f61f6-380">For WMI classes derived from **CIM\_PhysicalMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f61f6-381">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f61f6-381">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f61f6-382">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f61f6-382">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61f6-383">Требования</span><span class="sxs-lookup"><span data-stu-id="f61f6-383">Requirements</span></span>



| <span data-ttu-id="f61f6-384">Требование</span><span class="sxs-lookup"><span data-stu-id="f61f6-384">Requirement</span></span> | <span data-ttu-id="f61f6-385">Значение</span><span class="sxs-lookup"><span data-stu-id="f61f6-385">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f61f6-386">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f61f6-386">Minimum supported client</span></span><br/> | <span data-ttu-id="f61f6-387">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f61f6-387">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f61f6-388">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f61f6-388">Minimum supported server</span></span><br/> | <span data-ttu-id="f61f6-389">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f61f6-389">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f61f6-390">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f61f6-390">Namespace</span></span><br/>                | <span data-ttu-id="f61f6-391">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f61f6-391">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f61f6-392">MOF</span><span class="sxs-lookup"><span data-stu-id="f61f6-392">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f61f6-393"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f61f6-393"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f61f6-394">DLL</span><span class="sxs-lookup"><span data-stu-id="f61f6-394">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f61f6-395"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f61f6-395"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f61f6-396">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f61f6-396">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61f6-397">**Микросхема CIM \_**</span><span class="sxs-lookup"><span data-stu-id="f61f6-397">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> </dl>

 

