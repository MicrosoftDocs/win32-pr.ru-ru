---
description: Описывает возможности и управление носителями, в котором хранятся данные и позволяет получать данные. Этот супер-класс используется для представления программных и аппаратных RAID-компонентов или необработанного логического экстента физического носителя.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: Класс CIM_StorageExtent (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683428"
---
# <a name="cim_storageextent-class-hyper-v-management"></a><span data-ttu-id="0eb99-104">Класс CIM_StorageExtent (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0eb99-104">CIM_StorageExtent class (Hyper-V management)</span></span>

<span data-ttu-id="0eb99-105">Описывает возможности и управление носителями, в котором хранятся данные и позволяет получать данные.</span><span class="sxs-lookup"><span data-stu-id="0eb99-105">Describes the capabilities and management of media that stores data and allows retrieval of the data.</span></span> <span data-ttu-id="0eb99-106">Этот супер-класс используется для представления программных и аппаратных RAID-компонентов или необработанного логического экстента физического носителя.</span><span class="sxs-lookup"><span data-stu-id="0eb99-106">This super class is used to represent software and hardware RAID components, or a raw logical extent of physical media.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb99-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0eb99-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="0eb99-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0eb99-108">Members</span></span>

<span data-ttu-id="0eb99-109">Класс **CIM \_ сторажеекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0eb99-109">The **CIM\_StorageExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="0eb99-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0eb99-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0eb99-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0eb99-111">Properties</span></span>

<span data-ttu-id="0eb99-112">Класс **CIM \_ сторажеекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0eb99-112">The **CIM\_StorageExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0eb99-113">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="0eb99-113">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0eb99-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-116">Описание поддержки чтения и записи носителя.</span><span class="sxs-lookup"><span data-stu-id="0eb99-116">A description of the read/write support of the media.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0eb99-117">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0eb99-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="0eb99-118">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="0eb99-118">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="0eb99-119">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="0eb99-119">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="0eb99-120">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="0eb99-120">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="0eb99-121">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="0eb99-121">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0eb99-122">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="0eb99-122">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-123">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0eb99-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-125">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Hosting Storage \| 001,4 "," MIB. В файле IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "," MIF. \|Устройства хранения DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0eb99-125">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.4", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF.DMTF\|Storage Devices\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-126">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="0eb99-126">The size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="0eb99-127">Если используются размеры блоков переменных, это свойство должно указывать максимальный размер блока.</span><span class="sxs-lookup"><span data-stu-id="0eb99-127">If variable block sizes are used, then this property should specify the maximum block size.</span></span> <span data-ttu-id="0eb99-128">Если размер блока неизвестен или не является допустимым понятием блока (например, для **CIM \_ аггрегатикстент**, [**\_ памяти CIM**](cim-memory.md) или [**CIM \_ LogicalDisk**](cim-logicaldisk.md)), то этому свойству должно быть присвоено значение 1 (неизвестный).</span><span class="sxs-lookup"><span data-stu-id="0eb99-128">If the block size is unknown or if a block concept is not valid (for example, for **CIM\_AggregateExtent**, [**CIM\_Memory**](cim-memory.md) or [**CIM\_LogicalDisk**](cim-logicaldisk.md)), then this property should be set to "1" (unknow).</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-129">**консумаблеблоккс**</span><span class="sxs-lookup"><span data-stu-id="0eb99-129">**ConsumableBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-130">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0eb99-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-132">Максимальное число блоков, доступных для использования при **\_ разсторажеекстент CIM** с помощью ассоциации класса [**CIM \_ BasedOn**](cim-basedon.md) .</span><span class="sxs-lookup"><span data-stu-id="0eb99-132">The maximum number of blocks, that are available for use when layering **CIM\_StorageExtent** using the [**CIM\_BasedOn**](cim-basedon.md) class association.</span></span> <span data-ttu-id="0eb99-133">Это свойство имеет значение только в том случае, если на экстент хранения ссылается свойство **Antecedent** в объекте **CIM \_ BasedOn** .</span><span class="sxs-lookup"><span data-stu-id="0eb99-133">This property only has meaning when the storage extent is referenced in the **Antecedent** property in a **CIM\_BasedOn** object.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-134">**Организация**</span><span class="sxs-lookup"><span data-stu-id="0eb99-134">**DataOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-135">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0eb99-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-137">Тип организации данных, используемой носителем.</span><span class="sxs-lookup"><span data-stu-id="0eb99-137">The type of data organization used by the media.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0eb99-138">**Другое** (0)</span><span class="sxs-lookup"><span data-stu-id="0eb99-138">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0eb99-139">**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="0eb99-139">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

<span data-ttu-id="0eb99-140">**Фиксированный блок** (2)</span><span class="sxs-lookup"><span data-stu-id="0eb99-140">**Fixed Block** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

<span data-ttu-id="0eb99-141">**Блок переменных** (3)</span><span class="sxs-lookup"><span data-stu-id="0eb99-141">**Variable Block** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

<span data-ttu-id="0eb99-142">**Количество данных ключа** (4)</span><span class="sxs-lookup"><span data-stu-id="0eb99-142">**Count Key Data** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0eb99-143">**Избыточность**</span><span class="sxs-lookup"><span data-stu-id="0eb99-143">**DataRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0eb99-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-146">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажесеттинг**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**Датаредунданцигоал**","**CIM \_ сторажесеттинг**.**Датаредунданцимакс**","**CIM \_ сторажесеттинг**.**Датаредунданцимин**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM\_StorageSetting**.**DataRedundancyMax**", "**CIM\_StorageSetting**.**DataRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-147">Количество полных копий данных, которые в настоящее время хранятся.</span><span class="sxs-lookup"><span data-stu-id="0eb99-147">The number of complete copies of data that are currently maintained.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-148">**делтаресерватион**</span><span class="sxs-lookup"><span data-stu-id="0eb99-148">**DeltaReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-149">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0eb99-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-151">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("процент"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажесеттинг**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**Делтаресерватионгоал**","**CIM \_ сторажесеттинг**.**Делтаресерватионмакс**","**CIM \_ сторажесеттинг**.**Делтаресерватионмин**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-151">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Percentage"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM\_StorageSetting**.**DeltaReservationMax**", "**CIM\_StorageSetting**.**DeltaReservationMin**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-152">Текущее значение для разностного резервирования.</span><span class="sxs-lookup"><span data-stu-id="0eb99-152">The current value for delta reservation.</span></span> <span data-ttu-id="0eb99-153">Это процентное значение, указывающее объем пространства, которое должно быть зарезервировано в реплике для кэширования изменений.</span><span class="sxs-lookup"><span data-stu-id="0eb99-153">This is a percentage that specifies the amount of space that should be reserved in a replica for caching changes.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-154">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="0eb99-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0eb99-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-157">Тип обнаружения и исправления ошибок, поддерживаемый экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="0eb99-157">The type of error detection and correction supported by the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-158">**екстентстатус**</span><span class="sxs-lookup"><span data-stu-id="0eb99-158">**ExtentStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-159">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0eb99-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-161">Дополнительные сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="0eb99-161">Additional status information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0eb99-162">**Другое** (0)</span><span class="sxs-lookup"><span data-stu-id="0eb99-162">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0eb99-163">**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="0eb99-163">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

<span data-ttu-id="0eb99-164">**Нет/нет применимо** (2)</span><span class="sxs-lookup"><span data-stu-id="0eb99-164">**None/Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

<span data-ttu-id="0eb99-165">**Нарушено** (3)</span><span class="sxs-lookup"><span data-stu-id="0eb99-165">**Broken** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

<span data-ttu-id="0eb99-166">**Потерянные данные** (4)</span><span class="sxs-lookup"><span data-stu-id="0eb99-166">**Data Lost** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

<span data-ttu-id="0eb99-167">**Динамическая перенастройка** (5)</span><span class="sxs-lookup"><span data-stu-id="0eb99-167">**Dynamic Reconfig** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

<span data-ttu-id="0eb99-168">**Предоставлено** (6)</span><span class="sxs-lookup"><span data-stu-id="0eb99-168">**Exposed** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

<span data-ttu-id="0eb99-169">**Частично предоставлено** (7)</span><span class="sxs-lookup"><span data-stu-id="0eb99-169">**Fractionally Exposed** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

<span data-ttu-id="0eb99-170">**Частично предоставлено** (8)</span><span class="sxs-lookup"><span data-stu-id="0eb99-170">**Partially Exposed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

<span data-ttu-id="0eb99-171">**Защита отключена** (9)</span><span class="sxs-lookup"><span data-stu-id="0eb99-171">**Protection Disabled** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

<span data-ttu-id="0eb99-172">**Готово** (10)</span><span class="sxs-lookup"><span data-stu-id="0eb99-172">**Readying** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

<span data-ttu-id="0eb99-173">**Перестроение** (11)</span><span class="sxs-lookup"><span data-stu-id="0eb99-173">**Rebuild** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

<span data-ttu-id="0eb99-174">**Повторно вычислить** (12)</span><span class="sxs-lookup"><span data-stu-id="0eb99-174">**Recalculate** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

<span data-ttu-id="0eb99-175">**Запасное использование** (13)</span><span class="sxs-lookup"><span data-stu-id="0eb99-175">**Spare in Use** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

<span data-ttu-id="0eb99-176">**Проверка выполняется** (14)</span><span class="sxs-lookup"><span data-stu-id="0eb99-176">**Verify In Progress** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

<span data-ttu-id="0eb99-177">**Предоставлен доступ по каналу** (15)</span><span class="sxs-lookup"><span data-stu-id="0eb99-177">**In-Band Access Granted** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

<span data-ttu-id="0eb99-178">**Импортировано** (16)</span><span class="sxs-lookup"><span data-stu-id="0eb99-178">**Imported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

<span data-ttu-id="0eb99-179">**Экспортировано** (17)</span><span class="sxs-lookup"><span data-stu-id="0eb99-179">**Exported** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0eb99-180">**Зарезервировано DMTF** (18.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0eb99-180">**DMTF Reserved** (18..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0eb99-181">**Поставщик зарезервирован** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0eb99-181">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0eb99-182">**исбаседонундерлингредунданци**</span><span class="sxs-lookup"><span data-stu-id="0eb99-182">**IsBasedOnUnderlyingRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-183">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0eb99-183">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-185">**значение true** , если базовые экстенты хранения являются членами [**\_ сторажередунданциграуп CIM**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0eb99-185">**true** if the underlying storage extents are members of a [**CIM\_StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup); otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-186">**Name**</span><span class="sxs-lookup"><span data-stu-id="0eb99-186">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0eb99-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-189">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. ИНЦИТС-T10 \| VPD 83, идентификатор ассоциации 0 \| ), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сторажеекстент**.**Намеформат**","**CIM \_ сторажеекстент**.**Наменамеспаце**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-189">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**", "**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-190">Уникальный идентификатор для экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="0eb99-190">A unique identifier for the storage extent.</span></span> <span data-ttu-id="0eb99-191">Свойство **намеформат** задает формат имени для использования в свойстве **Name** .</span><span class="sxs-lookup"><span data-stu-id="0eb99-191">The **NameFormat** property specifies the naming format to use in the **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-192">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="0eb99-192">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-193">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0eb99-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-195">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сторажеекстент**.**Name**","**CIM \_ сторажеекстент**.**Наменамеспаце**","**CIM \_ сторажеекстент**.**Осернамеформат**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-195">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**NameNamespace**", "**CIM\_StorageExtent**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-196">Формат имени для свойства **Name** .</span><span class="sxs-lookup"><span data-stu-id="0eb99-196">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0eb99-197">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0eb99-197">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0eb99-198">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0eb99-198">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

<span data-ttu-id="0eb99-199">**VPD83NAA6** (2)</span><span class="sxs-lookup"><span data-stu-id="0eb99-199">**VPD83NAA6** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

<span data-ttu-id="0eb99-200">**VPD83NAA5** (3)</span><span class="sxs-lookup"><span data-stu-id="0eb99-200">**VPD83NAA5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="0eb99-201">**VPD83Type2** (4)</span><span class="sxs-lookup"><span data-stu-id="0eb99-201">**VPD83Type2** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="0eb99-202">**VPD83Type1** (5)</span><span class="sxs-lookup"><span data-stu-id="0eb99-202">**VPD83Type1** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

<span data-ttu-id="0eb99-203">**VPD83Type0** (6)</span><span class="sxs-lookup"><span data-stu-id="0eb99-203">**VPD83Type0** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="0eb99-204">**Снвм** (7)</span><span class="sxs-lookup"><span data-stu-id="0eb99-204">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="0eb99-205">**Нодеввн** (8)</span><span class="sxs-lookup"><span data-stu-id="0eb99-205">**NodeWWN** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="0eb99-206">**Удаляем** (9)</span><span class="sxs-lookup"><span data-stu-id="0eb99-206">**NAA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="0eb99-207">**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="0eb99-207">**EUI64** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="0eb99-208">**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="0eb99-208">**T10VID** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="0eb99-209">**Имя устройства ОС** (12)</span><span class="sxs-lookup"><span data-stu-id="0eb99-209">**OS Device Name** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0eb99-210">**наменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="0eb99-210">**NameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-211">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0eb99-211">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-213">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. ИНЦИТС-T10 \| VPD 83, идентификатор ассоциации 0 \| ), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сторажеекстент**.**Name**","**CIM \_ сторажеекстент**.**Осернаменамеспаце**","**CIM \_ сторажеекстент**.**Намеформат**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-213">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC.INCITS-T10\| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**Name**", "**CIM\_StorageExtent**.**OtherNameNamespace**", "**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-214">Пространство имен свойства Name.</span><span class="sxs-lookup"><span data-stu-id="0eb99-214">The namespace of the name property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0eb99-215">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0eb99-215">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0eb99-216">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0eb99-216">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="0eb99-217">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="0eb99-217">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="0eb99-218">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="0eb99-218">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="0eb99-219">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="0eb99-219">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="0eb99-220">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="0eb99-220">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="0eb99-221">**Нодеввн** (6)</span><span class="sxs-lookup"><span data-stu-id="0eb99-221">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="0eb99-222">**Снвм** (7)</span><span class="sxs-lookup"><span data-stu-id="0eb99-222">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="0eb99-223">**Пространство имен устройств ОС** (8)</span><span class="sxs-lookup"><span data-stu-id="0eb99-223">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0eb99-224">**носинглепоинтоффаилуре**</span><span class="sxs-lookup"><span data-stu-id="0eb99-224">**NoSinglePointOfFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-225">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0eb99-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-227">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажесеттинг**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**Носинглепоинтоффаилуре**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-227">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-228">**значение true** , если нет ни одной точки сбоя; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0eb99-228">**true** if there are not any single points of failure; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-229">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="0eb99-229">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-230">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0eb99-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-232">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Hosting Storage \| 001,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="0eb99-232">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Host Storage\|001.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-233">Общее число логически смежных блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="0eb99-233">The total number of logically contiguous blocks that form the storage extent.</span></span> <span data-ttu-id="0eb99-234">Общий размер экстента хранения вычисляется **путем умножения на** **нумберофблоккс**.</span><span class="sxs-lookup"><span data-stu-id="0eb99-234">The total size of the storage extent is calculated by multiplying **BlockSize** by **NumberOfBlocks**.</span></span> <span data-ttu-id="0eb99-235">Если размер **блока** равен "1", это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="0eb99-235">If the **BlockSize** is "1", this property is the total size of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-236">**осернамеформат**</span><span class="sxs-lookup"><span data-stu-id="0eb99-236">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0eb99-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-239">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сторажеекстент**.**Намеформат**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-239">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-240">Формат свойства **Name** , если свойство **намеформат** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="0eb99-240">The format of the **Name** property when the **NameFormat** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-241">**осернаменамеспаце**</span><span class="sxs-lookup"><span data-stu-id="0eb99-241">**OtherNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0eb99-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-244">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сторажеекстент**.**Наменамеспаце**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-244">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_StorageExtent**.**NameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-245">Описание пространства имен свойства **Name** , если свойство **наменамеспаце** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="0eb99-245">A description of the namespace of the **Name** property when the **NameNamespace** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-246">**паккажередунданци**</span><span class="sxs-lookup"><span data-stu-id="0eb99-246">**PackageRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-247">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0eb99-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-249">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажесеттинг**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**Паккажередунданцигоал**","**CIM \_ сторажесеттинг**.**Паккажередунданцимакс**","**CIM \_ сторажесеттинг**.**Паккажередунданцимин**")</span><span class="sxs-lookup"><span data-stu-id="0eb99-249">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM\_StorageSetting**.**PackageRedundancyMax**", "**CIM\_StorageSetting**.**PackageRedundancyMin**")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-250">Текущее число физических пакетов, которые могут завершиться сбоем без потери данных.</span><span class="sxs-lookup"><span data-stu-id="0eb99-250">The current number of physical packages that can fail without data loss.</span></span> <span data-ttu-id="0eb99-251">Например, в домене хранилища это может быть число дисковых накопителей.</span><span class="sxs-lookup"><span data-stu-id="0eb99-251">For example, in a storage domain, this might be the number of disk spindles.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-252">**Исходный пул**</span><span class="sxs-lookup"><span data-stu-id="0eb99-252">**Primordial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-253">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0eb99-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-255">**значение true** , если экстент хранения является первичным; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0eb99-255">**true** if the storage extent is primordial; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-256">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="0eb99-256">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0eb99-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-259">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажедескр ")</span><span class="sxs-lookup"><span data-stu-id="0eb99-259">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageDescr")</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-260">Описание использования мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0eb99-260">A description of the media usage.</span></span>

</dd> <dt>

<span data-ttu-id="0eb99-261">**SequentialAccess**</span><span class="sxs-lookup"><span data-stu-id="0eb99-261">**SequentialAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0eb99-262">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0eb99-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0eb99-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0eb99-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0eb99-264">**значение true** , если доступ к хранилищу осуществляется последовательно с помощью объекта [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md) ; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0eb99-264">**true** if storage is sequentially accessed by a [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) object; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0eb99-265">Требования</span><span class="sxs-lookup"><span data-stu-id="0eb99-265">Requirements</span></span>



| <span data-ttu-id="0eb99-266">Требование</span><span class="sxs-lookup"><span data-stu-id="0eb99-266">Requirement</span></span> | <span data-ttu-id="0eb99-267">Значение</span><span class="sxs-lookup"><span data-stu-id="0eb99-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eb99-268">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0eb99-268">Minimum supported client</span></span><br/> | <span data-ttu-id="0eb99-269">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0eb99-269">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0eb99-270">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0eb99-270">Minimum supported server</span></span><br/> | <span data-ttu-id="0eb99-271">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0eb99-271">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0eb99-272">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0eb99-272">Namespace</span></span><br/>                | <span data-ttu-id="0eb99-273">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0eb99-273">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0eb99-274">MOF</span><span class="sxs-lookup"><span data-stu-id="0eb99-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0eb99-275"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0eb99-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0eb99-276">DLL</span><span class="sxs-lookup"><span data-stu-id="0eb99-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0eb99-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0eb99-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0eb99-278">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0eb99-278">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eb99-279">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="0eb99-279">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

