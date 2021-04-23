---
description: Класс CIM \_ меморикапаЦити представляет память, которую можно установить на физическом элементе и его минимальной и максимальной конфигурации.
ms.assetid: a962ee38-9281-4a7a-b9d7-b321edb5670d
ms.tgt_platform: multiple
title: Класс CIM_MemoryCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryCapacity
- CIM_MemoryCapacity.Caption
- CIM_MemoryCapacity.Description
- CIM_MemoryCapacity.Name
- CIM_MemoryCapacity.MaximumMemoryCapacity
- CIM_MemoryCapacity.MemoryType
- CIM_MemoryCapacity.MinimumMemoryCapacity
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa63d06187c76c5add433502d012cdb63905795a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262544"
---
# <a name="cim_memorycapacity-class"></a><span data-ttu-id="de319-103">\_Класс CIM меморикапаЦити</span><span class="sxs-lookup"><span data-stu-id="de319-103">CIM\_MemoryCapacity class</span></span>

<span data-ttu-id="de319-104">Класс **CIM \_ меморикапаЦити** представляет память, которую можно установить на физическом элементе и его минимальной и максимальной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="de319-104">The **CIM\_MemoryCapacity** class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="de319-105">Сведения о текущей установленной памяти, а также минимальные и максимальные требования к элементу находятся в экземплярах класса [**CIM \_ фисикалмемори**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="de319-105">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de319-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="de319-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="de319-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="de319-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="de319-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="de319-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="de319-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="de319-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de319-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de319-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryCapacity : CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
  uint64 MaximumMemoryCapacity;
  uint16 MemoryType;
  uint64 MinimumMemoryCapacity;
};
```

## <a name="members"></a><span data-ttu-id="de319-111">Члены</span><span class="sxs-lookup"><span data-stu-id="de319-111">Members</span></span>

<span data-ttu-id="de319-112">Класс **CIM \_ меморикапаЦити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="de319-112">The **CIM\_MemoryCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="de319-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="de319-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de319-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="de319-114">Properties</span></span>

<span data-ttu-id="de319-115">Класс **CIM \_ меморикапаЦити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="de319-115">The **CIM\_MemoryCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de319-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="de319-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de319-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de319-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de319-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de319-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de319-119">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de319-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de319-120">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="de319-120">Short textual description of the object.</span></span>

<span data-ttu-id="de319-121">Это свойство наследуется от [**CIM \_ фисикалкапаЦити**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="de319-121">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="de319-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de319-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de319-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de319-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de319-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de319-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de319-125">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="de319-125">Textual description of the object.</span></span>

<span data-ttu-id="de319-126">Это свойство наследуется от [**CIM \_ фисикалкапаЦити**](cim-physicalcapacity.md).</span><span class="sxs-lookup"><span data-stu-id="de319-126">This property is inherited from [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md).</span></span>

</dd> <dt>

<span data-ttu-id="de319-127">**максимуммеморикапаЦити**</span><span class="sxs-lookup"><span data-stu-id="de319-127">**MaximumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de319-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de319-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de319-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de319-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de319-130">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="de319-130">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="de319-131">Максимальный объем памяти (в килобайтах), который может поддерживаться связанным физическим элементом.</span><span class="sxs-lookup"><span data-stu-id="de319-131">Maximum amount of memory, in kilobytes, that can be supported by the associated physical element.</span></span>

<span data-ttu-id="de319-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="de319-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="de319-133">**меморитипе**</span><span class="sxs-lookup"><span data-stu-id="de319-133">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de319-134">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="de319-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="de319-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de319-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de319-136">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ фисикалмемори**](cim-physicalmemory.md).**Меморитипе**")</span><span class="sxs-lookup"><span data-stu-id="de319-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalMemory**](cim-physicalmemory.md).**MemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="de319-137">Тип памяти, который является частью ключа объекта.</span><span class="sxs-lookup"><span data-stu-id="de319-137">Type of memory, which is part of the object key.</span></span> <span data-ttu-id="de319-138">Значения соответствуют списку возможных типов памяти в классе [**CIM \_ фисикалмемори**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="de319-138">Values correspond to the list of possible memory types in the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="de319-139">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="de319-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="de319-140">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="de319-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="de319-141">**DRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="de319-141">**DRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="de319-142">**Синхронная DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="de319-142">**Synchronous DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span data-ttu-id="de319-143">**Кэш DRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="de319-143">**Cache DRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span data-ttu-id="de319-144">**Эдо** (5)</span><span class="sxs-lookup"><span data-stu-id="de319-144">**EDO** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span data-ttu-id="de319-145">**Едрам** (6)</span><span class="sxs-lookup"><span data-stu-id="de319-145">**EDRAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="de319-146">**Видеопамять** (7)</span><span class="sxs-lookup"><span data-stu-id="de319-146">**VRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="de319-147">**SRAM** (8)</span><span class="sxs-lookup"><span data-stu-id="de319-147">**SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span data-ttu-id="de319-148">**ОЗУ** (9)</span><span class="sxs-lookup"><span data-stu-id="de319-148">**RAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span data-ttu-id="de319-149">**ПЗУ** (10)</span><span class="sxs-lookup"><span data-stu-id="de319-149">**ROM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span data-ttu-id="de319-150">**Flash** (11)</span><span class="sxs-lookup"><span data-stu-id="de319-150">**Flash** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span data-ttu-id="de319-151">**EEPROM** (12)</span><span class="sxs-lookup"><span data-stu-id="de319-151">**EEPROM** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span data-ttu-id="de319-152">**Фепром** (13)</span><span class="sxs-lookup"><span data-stu-id="de319-152">**FEPROM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span data-ttu-id="de319-153">**Епром** (14)</span><span class="sxs-lookup"><span data-stu-id="de319-153">**EPROM** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="de319-154">**Кдрам** (15)</span><span class="sxs-lookup"><span data-stu-id="de319-154">**CDRAM** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="de319-155">**3DRAM** (16)</span><span class="sxs-lookup"><span data-stu-id="de319-155">**3DRAM** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="de319-156">**SDRAM** (17)</span><span class="sxs-lookup"><span data-stu-id="de319-156">**SDRAM** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="de319-157">**Сграм** (18)</span><span class="sxs-lookup"><span data-stu-id="de319-157">**SGRAM** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span data-ttu-id="de319-158">**RDRAM** (19)</span><span class="sxs-lookup"><span data-stu-id="de319-158">**RDRAM** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span data-ttu-id="de319-159">**DDR** (20)</span><span class="sxs-lookup"><span data-stu-id="de319-159">**DDR** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DDR-2"></span><span id="ddr-2"></span>

<span data-ttu-id="de319-160">**DDR-2** (21)</span><span class="sxs-lookup"><span data-stu-id="de319-160">**DDR-2** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="de319-161">**минимуммеморикапаЦити**</span><span class="sxs-lookup"><span data-stu-id="de319-161">**MinimumMemoryCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de319-162">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de319-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de319-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de319-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de319-164">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="de319-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="de319-165">Минимальный объем памяти (в килобайтах), необходимый для правильной работы связанного физического элемента.</span><span class="sxs-lookup"><span data-stu-id="de319-165">Minimum amount of memory, in kilobytes, that is needed for the associated physical element to operate correctly.</span></span>

<span data-ttu-id="de319-166">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="de319-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="de319-167">**Name**</span><span class="sxs-lookup"><span data-stu-id="de319-167">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de319-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="de319-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de319-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de319-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de319-170">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de319-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de319-171">Имя объекта; служит частью ключа объекта.</span><span class="sxs-lookup"><span data-stu-id="de319-171">The name of the object; serves as a part of the object key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de319-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de319-172">Remarks</span></span>

<span data-ttu-id="de319-173">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="de319-173">WMI does not implement this class.</span></span>

<span data-ttu-id="de319-174">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="de319-174">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="de319-175">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="de319-175">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="de319-176">Требования</span><span class="sxs-lookup"><span data-stu-id="de319-176">Requirements</span></span>



| <span data-ttu-id="de319-177">Требование</span><span class="sxs-lookup"><span data-stu-id="de319-177">Requirement</span></span> | <span data-ttu-id="de319-178">Значение</span><span class="sxs-lookup"><span data-stu-id="de319-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de319-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de319-179">Minimum supported client</span></span><br/> | <span data-ttu-id="de319-180">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de319-180">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de319-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de319-181">Minimum supported server</span></span><br/> | <span data-ttu-id="de319-182">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de319-182">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de319-183">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de319-183">Namespace</span></span><br/>                | <span data-ttu-id="de319-184">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="de319-184">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="de319-185">MOF</span><span class="sxs-lookup"><span data-stu-id="de319-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de319-186"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de319-186"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de319-187">DLL</span><span class="sxs-lookup"><span data-stu-id="de319-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de319-188"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de319-188"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de319-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de319-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de319-190">**\_ФИСИКАЛКАПАЦИТИ CIM**</span><span class="sxs-lookup"><span data-stu-id="de319-190">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> </dl>

 

