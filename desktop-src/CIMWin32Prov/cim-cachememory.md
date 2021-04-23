---
description: Класс CIM \_ качемемори определяет возможности и управление кэшовой памятью.
ms.assetid: cdf35122-2057-45fa-818b-ce542d8e82b0
ms.tgt_platform: multiple
title: Класс CIM_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CacheMemory
- CIM_CacheMemory.Caption
- CIM_CacheMemory.Description
- CIM_CacheMemory.InstallDate
- CIM_CacheMemory.Name
- CIM_CacheMemory.Status
- CIM_CacheMemory.Availability
- CIM_CacheMemory.ConfigManagerErrorCode
- CIM_CacheMemory.ConfigManagerUserConfig
- CIM_CacheMemory.CreationClassName
- CIM_CacheMemory.DeviceID
- CIM_CacheMemory.PowerManagementCapabilities
- CIM_CacheMemory.ErrorCleared
- CIM_CacheMemory.ErrorDescription
- CIM_CacheMemory.LastErrorCode
- CIM_CacheMemory.PNPDeviceID
- CIM_CacheMemory.PowerManagementSupported
- CIM_CacheMemory.StatusInfo
- CIM_CacheMemory.SystemCreationClassName
- CIM_CacheMemory.SystemName
- CIM_CacheMemory.Access
- CIM_CacheMemory.BlockSize
- CIM_CacheMemory.NumberOfBlocks
- CIM_CacheMemory.Purpose
- CIM_CacheMemory.ErrorMethodology
- CIM_CacheMemory.AdditionalErrorData
- CIM_CacheMemory.CorrectableError
- CIM_CacheMemory.EndingAddress
- CIM_CacheMemory.ErrorAccess
- CIM_CacheMemory.ErrorAddress
- CIM_CacheMemory.ErrorData
- CIM_CacheMemory.ErrorDataOrder
- CIM_CacheMemory.ErrorInfo
- CIM_CacheMemory.ErrorResolution
- CIM_CacheMemory.ErrorTime
- CIM_CacheMemory.ErrorTransferSize
- CIM_CacheMemory.OtherErrorDescription
- CIM_CacheMemory.StartingAddress
- CIM_CacheMemory.SystemLevelAddress
- CIM_CacheMemory.Associativity
- CIM_CacheMemory.CacheType
- CIM_CacheMemory.FlushTimer
- CIM_CacheMemory.Level
- CIM_CacheMemory.LineSize
- CIM_CacheMemory.ReadPolicy
- CIM_CacheMemory.ReplacementPolicy
- CIM_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b7a7add96c523dae6b683d597ba36953c605d28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896130"
---
# <a name="cim_cachememory-class"></a><span data-ttu-id="66874-103">\_Класс CIM качемемори</span><span class="sxs-lookup"><span data-stu-id="66874-103">CIM\_CacheMemory class</span></span>

<span data-ttu-id="66874-104">Класс **CIM \_ качемемори** определяет возможности и управление кэшовой памятью.</span><span class="sxs-lookup"><span data-stu-id="66874-104">The **CIM\_CacheMemory** class defines the capabilities and management of cache memory.</span></span>

<span data-ttu-id="66874-105">Кэш памяти — это выделенная или выделенная память, в которой процессор сначала выполняет поиск данных.</span><span class="sxs-lookup"><span data-stu-id="66874-105">Cache memory is the dedicated or allocated RAM where a processor first searches for data.</span></span> <span data-ttu-id="66874-106">Данные в кэш-памяти быстро доставляются процессору и обычно описываются по сходству с процессором (например, первичным или вторичным кэшем).</span><span class="sxs-lookup"><span data-stu-id="66874-106">Data in cache memory is quickly delivered to the processor and is usually described by its proximity to the processor (for example, primary or secondary cache).</span></span> <span data-ttu-id="66874-107">Дисковый накопитель, который включает ОЗУ, выделенный для хранения самых последних прочитанных или соседних данных диска (для ускорения извлечения), также моделируется как кэш-память.</span><span class="sxs-lookup"><span data-stu-id="66874-107">A disk drive that includes RAM allocated for holding the disk's most recently read or adjacent data (to speed up retrieval) is also modeled as cache memory.</span></span>

> [!Note]  
> <span data-ttu-id="66874-108">Кэш памяти не является буфером операционной системы или уровня приложения; это ОЗУ, выделенный для кэширования данных процессора.</span><span class="sxs-lookup"><span data-stu-id="66874-108">Cache memory is not an operating-system or application-level buffer; it is RAM that has been allocated for caching processor data.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="66874-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="66874-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="66874-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="66874-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="66874-111">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="66874-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="66874-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="66874-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66874-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66874-113">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B65-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CacheMemory : CIM_Memory
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  uint64   NumberOfBlocks;
  string   Purpose;
  string   ErrorMethodology;
  uint8    AdditionalErrorData[];
  boolean  CorrectableError;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint16   ErrorInfo;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  string   OtherErrorDescription;
  uint64   StartingAddress;
  boolean  SystemLevelAddress;
  uint16   Associativity;
  uint16   CacheType;
  uint32   FlushTimer;
  uint16   Level;
  uint32   LineSize;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="66874-114">Члены</span><span class="sxs-lookup"><span data-stu-id="66874-114">Members</span></span>

<span data-ttu-id="66874-115">Класс **CIM \_ качемемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="66874-115">The **CIM\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="66874-116">Методы</span><span class="sxs-lookup"><span data-stu-id="66874-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="66874-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="66874-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="66874-118">Методы</span><span class="sxs-lookup"><span data-stu-id="66874-118">Methods</span></span>

<span data-ttu-id="66874-119">Класс **CIM \_ качемемори** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="66874-119">The **CIM\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="66874-120">Метод</span><span class="sxs-lookup"><span data-stu-id="66874-120">Method</span></span>                                                                 | <span data-ttu-id="66874-121">Описание</span><span class="sxs-lookup"><span data-stu-id="66874-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66874-122">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="66874-122">**Reset**</span></span>](reset-method-in-class-cim-cachememory.md)                 | <span data-ttu-id="66874-123">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="66874-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="66874-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="66874-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="66874-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="66874-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cachememory.md) | <span data-ttu-id="66874-126">Определяет требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="66874-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="66874-127">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="66874-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="66874-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="66874-128">Properties</span></span>

<span data-ttu-id="66874-129">Класс **CIM \_ качемемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="66874-129">The **CIM\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66874-130">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="66874-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-133">Описание свойств чтения и записи носителя.</span><span class="sxs-lookup"><span data-stu-id="66874-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="66874-134">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="66874-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-135">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="66874-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="66874-136">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="66874-137">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="66874-138">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="66874-139">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-140">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="66874-140">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-141">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="66874-141">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="66874-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,18 "," MIF. \|Массив физической памяти DMTF \| 001,13 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="66874-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="66874-144">Массив октетов, содержащих дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="66874-144">Array of octets that hold additional error information.</span></span> <span data-ttu-id="66874-145">Примером является проверка ошибок и исправление ошибки (ECC) синдром или возвращение битов проверки, если используется методология ошибок на основе CRC.</span><span class="sxs-lookup"><span data-stu-id="66874-145">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="66874-146">В последнем случае, если обнаружена Одноразрядная ошибка и известен алгоритм CRC, может быть определен точный бит, который не удалось определить.</span><span class="sxs-lookup"><span data-stu-id="66874-146">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="66874-147">Этот тип данных (ECC синдром, Check-bit или данные, поразрядные с контролем четности или другие предоставленные поставщиком сведения) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="66874-147">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="66874-148">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-148">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-149">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-149">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-150">**Ассоциативность**</span><span class="sxs-lookup"><span data-stu-id="66874-150">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-153">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="66874-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="66874-154">Перечисление, определяющее ассоциативность системного кэша.</span><span class="sxs-lookup"><span data-stu-id="66874-154">Enumeration that defines the system cache associativity.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-155">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-156">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-156">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="66874-157">**Прямое сопоставление** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-157">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="66874-158">**2-направленный набор-ассоциативный** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-158">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="66874-159">**4-направленный набор-ассоциативный** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-159">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="66874-160">**Полностью ассоциативная** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-160">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="66874-161">**8-направленное множество-ассоциативное** (7)</span><span class="sxs-lookup"><span data-stu-id="66874-161">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="66874-162">**16-направленный набор-ассоциативный** (8)</span><span class="sxs-lookup"><span data-stu-id="66874-162">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-163">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="66874-163">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-164">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-166">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="66874-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="66874-167">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="66874-167">Availability and status of the device.</span></span>

<span data-ttu-id="66874-168">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-168">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="66874-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-171"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="66874-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-172"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="66874-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-173"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="66874-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-174"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="66874-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="66874-175"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="66874-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="66874-176"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="66874-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="66874-177"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="66874-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="66874-178"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="66874-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="66874-179"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="66874-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="66874-180"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="66874-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="66874-181"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="66874-182">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-182">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="66874-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="66874-183"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="66874-184">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="66874-184">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="66874-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="66874-185"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="66874-186">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="66874-186">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="66874-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="66874-187"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="66874-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="66874-188"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="66874-189">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="66874-189">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="66874-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="66874-190"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="66874-191">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="66874-191">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="66874-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="66874-192"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="66874-193">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="66874-193">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="66874-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="66874-194"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="66874-195">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="66874-195">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="66874-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="66874-196"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="66874-197">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="66874-197">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-198">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="66874-198">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-199">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66874-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66874-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-201">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="66874-201">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="66874-202">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="66874-202">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="66874-203">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="66874-203">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="66874-204">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="66874-204">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="66874-205">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="66874-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="66874-206">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="66874-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-207">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="66874-207">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-210">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="66874-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="66874-211">Указывает кэширование инструкций, кэширование данных или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="66874-211">Specifies instruction caching, data caching, or both.</span></span> <span data-ttu-id="66874-212">Можно также определить "Other" и "Unknown".</span><span class="sxs-lookup"><span data-stu-id="66874-212">"Other" and "Unknown" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-213">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-213">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-214">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-214">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="66874-215">**Инструкция** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-215">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="66874-216">**Данные** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-216">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="66874-217">**Единая** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-217">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-218">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="66874-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-221">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="66874-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="66874-222">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="66874-222">A short textual description of the object.</span></span>

<span data-ttu-id="66874-223">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66874-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-224">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="66874-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-225">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66874-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66874-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-227">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="66874-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="66874-228">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="66874-228">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="66874-229">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="66874-230">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="66874-230">**This device is working properly.**</span></span> <span data-ttu-id="66874-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="66874-231">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="66874-232">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="66874-232">**This device is not configured correctly.**</span></span> <span data-ttu-id="66874-233">(1)</span><span class="sxs-lookup"><span data-stu-id="66874-233">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="66874-234">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-234">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="66874-235">(2)</span><span class="sxs-lookup"><span data-stu-id="66874-235">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="66874-236">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="66874-236">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="66874-237">(3)</span><span class="sxs-lookup"><span data-stu-id="66874-237">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="66874-238">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="66874-238">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="66874-239">(4)</span><span class="sxs-lookup"><span data-stu-id="66874-239">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="66874-240">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="66874-240">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="66874-241">(5)</span><span class="sxs-lookup"><span data-stu-id="66874-241">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="66874-242">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="66874-242">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="66874-243"> (6)</span><span class="sxs-lookup"><span data-stu-id="66874-243">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="66874-244">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="66874-244">**Cannot filter.**</span></span> <span data-ttu-id="66874-245">(7)</span><span class="sxs-lookup"><span data-stu-id="66874-245">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="66874-246">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-246">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="66874-247">(8)</span><span class="sxs-lookup"><span data-stu-id="66874-247">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="66874-248">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-248">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="66874-249">(9)</span><span class="sxs-lookup"><span data-stu-id="66874-249">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="66874-250">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="66874-250">**This device cannot start.**</span></span> <span data-ttu-id="66874-251">(10)</span><span class="sxs-lookup"><span data-stu-id="66874-251">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="66874-252">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-252">**This device failed.**</span></span> <span data-ttu-id="66874-253">(11)</span><span class="sxs-lookup"><span data-stu-id="66874-253">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="66874-254">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="66874-254">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="66874-255">(12)</span><span class="sxs-lookup"><span data-stu-id="66874-255">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="66874-256">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-256">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="66874-257">(13)</span><span class="sxs-lookup"><span data-stu-id="66874-257">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="66874-258">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="66874-258">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="66874-259">(14)</span><span class="sxs-lookup"><span data-stu-id="66874-259">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="66874-260">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="66874-260">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="66874-261">(15)</span><span class="sxs-lookup"><span data-stu-id="66874-261">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="66874-262">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="66874-262">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="66874-263">(16)</span><span class="sxs-lookup"><span data-stu-id="66874-263">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="66874-264">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="66874-264">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="66874-265">(17)</span><span class="sxs-lookup"><span data-stu-id="66874-265">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="66874-266">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-266">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="66874-267">(18)</span><span class="sxs-lookup"><span data-stu-id="66874-267">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="66874-268">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="66874-268">**Failure using the VxD loader.**</span></span> <span data-ttu-id="66874-269">(19)</span><span class="sxs-lookup"><span data-stu-id="66874-269">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="66874-270">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="66874-270">**Your registry might be corrupted.**</span></span> <span data-ttu-id="66874-271">(20)</span><span class="sxs-lookup"><span data-stu-id="66874-271">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="66874-272">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="66874-272">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="66874-273">(21)</span><span class="sxs-lookup"><span data-stu-id="66874-273">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="66874-274">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="66874-274">**This device is disabled.**</span></span> <span data-ttu-id="66874-275">(22)</span><span class="sxs-lookup"><span data-stu-id="66874-275">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="66874-276">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="66874-276">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="66874-277">(23)</span><span class="sxs-lookup"><span data-stu-id="66874-277">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="66874-278">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="66874-278">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="66874-279">(24)</span><span class="sxs-lookup"><span data-stu-id="66874-279">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="66874-280">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="66874-280">**Windows is still setting up this device.**</span></span> <span data-ttu-id="66874-281">(25)</span><span class="sxs-lookup"><span data-stu-id="66874-281">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="66874-282">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="66874-282">**Windows is still setting up this device.**</span></span> <span data-ttu-id="66874-283">(26)</span><span class="sxs-lookup"><span data-stu-id="66874-283">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="66874-284">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="66874-284">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="66874-285">(27)</span><span class="sxs-lookup"><span data-stu-id="66874-285">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="66874-286">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="66874-286">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="66874-287">(28)</span><span class="sxs-lookup"><span data-stu-id="66874-287">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="66874-288">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="66874-288">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="66874-289">(29)</span><span class="sxs-lookup"><span data-stu-id="66874-289">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="66874-290">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="66874-290">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="66874-291">(30)</span><span class="sxs-lookup"><span data-stu-id="66874-291">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="66874-292">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="66874-292">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="66874-293">1-31</span><span class="sxs-lookup"><span data-stu-id="66874-293">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-294">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="66874-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-295">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66874-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66874-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-297">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="66874-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="66874-298">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="66874-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="66874-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-300">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="66874-300">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-301">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66874-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66874-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-303">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="66874-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="66874-304">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="66874-304">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="66874-305">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-305">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-306">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-306">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="66874-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-310">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66874-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66874-311">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="66874-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="66874-312">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="66874-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="66874-313">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-314">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66874-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-317">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="66874-317">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="66874-318">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="66874-318">A textual description of the object.</span></span>

<span data-ttu-id="66874-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66874-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="66874-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-323">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66874-323">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66874-324">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="66874-324">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="66874-325">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-326">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="66874-326">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-327">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66874-327">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66874-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-329">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,4 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,5 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="66874-329">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="66874-330">Конечный адрес, на который ссылается приложение или операционная система и который сопоставляется контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="66874-330">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="66874-331">Конечный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="66874-331">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="66874-332">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="66874-332">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="66874-333">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-333">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-334">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="66874-334">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-335">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-335">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,15 "," MIF. \|Массив физической памяти DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="66874-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="66874-338">Операция доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="66874-338">Memory access operation that caused the last error.</span></span> <span data-ttu-id="66874-339">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="66874-339">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="66874-340">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-340">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-341">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-341">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-342">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-342">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-343">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-343">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="66874-344">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-344">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="66874-345">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-345">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="66874-346">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-346">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-347">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="66874-347">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-348">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66874-348">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66874-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-350">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. \|Массив физической памяти DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="66874-350">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="66874-351">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="66874-351">Address of the last memory error.</span></span> <span data-ttu-id="66874-352">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="66874-352">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="66874-353">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-353">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-354">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="66874-354">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="66874-355">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-355">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-356">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="66874-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-357">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66874-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66874-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-359">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="66874-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="66874-360">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-361">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="66874-361">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-362">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="66874-362">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="66874-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-364">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. \|Массив физической памяти DMTF \| 001,12 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="66874-364">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="66874-365">Данные, захваченные во время последнего ошибочного доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="66874-365">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="66874-366">Данные занимают первые *n* октетов массива, которые необходимы для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="66874-366">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="66874-367">Если **еррортрансферсизе** имеет значение 0, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-367">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="66874-368">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-368">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-369">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="66874-369">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-370">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-370">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-372">Порядок данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="66874-372">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="66874-373">Если **еррортрансферсизе** имеет значение 0, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-373">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="66874-374">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-374">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="66874-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="66874-376">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-376">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="66874-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-377"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-378">Сначала следует наименее значащий байт.</span><span class="sxs-lookup"><span data-stu-id="66874-378">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="66874-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-379"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-380">Первый значащий байт.</span><span class="sxs-lookup"><span data-stu-id="66874-380">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="66874-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-384">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="66874-384">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="66874-385">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="66874-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-389">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**Осереррордескриптион**")</span><span class="sxs-lookup"><span data-stu-id="66874-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="66874-390">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="66874-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="66874-391">Значения от 12 до 14 не определены в схеме CIM, так как DMI смешивает семантику типа ошибки и является ли она исправимой.</span><span class="sxs-lookup"><span data-stu-id="66874-391">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="66874-392">Указывает, является ли ошибка исправимой, указывается в свойстве **корректаблиррор** .</span><span class="sxs-lookup"><span data-stu-id="66874-392">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<span data-ttu-id="66874-393">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-394"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-395">Другое</span><span class="sxs-lookup"><span data-stu-id="66874-395">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-396"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-397">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-397">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="66874-398"><span id="OK"></span><span id="ok"></span>**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-398"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="66874-399">Все в порядке.</span><span class="sxs-lookup"><span data-stu-id="66874-399">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="66874-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-400"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="66874-401">Ошибка чтения.</span><span class="sxs-lookup"><span data-stu-id="66874-401">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="66874-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-402"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="66874-403">Ошибка четности.</span><span class="sxs-lookup"><span data-stu-id="66874-403">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="66874-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-404"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="66874-405">Одноразрядная ошибка.</span><span class="sxs-lookup"><span data-stu-id="66874-405">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="66874-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="66874-406"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="66874-407">Двойная разрядная ошибка.</span><span class="sxs-lookup"><span data-stu-id="66874-407">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="66874-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="66874-408"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="66874-409">Многоразрядная ошибка.</span><span class="sxs-lookup"><span data-stu-id="66874-409">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="66874-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="66874-410"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="66874-411">Ошибка погрешности.</span><span class="sxs-lookup"><span data-stu-id="66874-411">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="66874-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="66874-412"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="66874-413">Ошибка контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="66874-413">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="66874-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="66874-414"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="66874-415">Ошибка CRC.</span><span class="sxs-lookup"><span data-stu-id="66874-415">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="66874-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (12)</span><span class="sxs-lookup"><span data-stu-id="66874-416"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="66874-417">Не определено.</span><span class="sxs-lookup"><span data-stu-id="66874-417">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="66874-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (13)</span><span class="sxs-lookup"><span data-stu-id="66874-418"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="66874-419">Не определено.</span><span class="sxs-lookup"><span data-stu-id="66874-419">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="66874-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (14)</span><span class="sxs-lookup"><span data-stu-id="66874-420"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="66874-421">Не определено.</span><span class="sxs-lookup"><span data-stu-id="66874-421">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-422">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="66874-422">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-423">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-425">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив физической памяти DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="66874-425">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="66874-426">Указывает, используются ли алгоритмы четности или CRC, ECC или другие механизмы.</span><span class="sxs-lookup"><span data-stu-id="66874-426">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="66874-427">Также можно указать сведения об алгоритме.</span><span class="sxs-lookup"><span data-stu-id="66874-427">Details on the algorithm can also be supplied.</span></span>

<span data-ttu-id="66874-428">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-428">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-429">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="66874-429">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-430">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66874-430">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66874-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-432">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,21 "," MIF. \|Массив физической памяти DMTF \| 001,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="66874-432">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="66874-433">Указывает диапазон в байтах, до которого может быть разрешена Последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="66874-433">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="66874-434">Например, если адреса ошибок разрешаются в бит 11 (то есть на типичном уровне страницы), ошибки могут быть разрешены до 4 КБ, а значение этого свойства равно 4000.</span><span class="sxs-lookup"><span data-stu-id="66874-434">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="66874-435">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-435">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-436">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="66874-436">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="66874-437">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-437">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-438">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="66874-438">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-439">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66874-439">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66874-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-441">Дата и время возникновения последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="66874-441">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="66874-442">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="66874-442">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="66874-443">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-443">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-444">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-444">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-445">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="66874-445">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-446">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66874-446">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66874-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-448">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,16 "," MIF. \|Массив физической памяти DMTF \| 001,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит ")</span><span class="sxs-lookup"><span data-stu-id="66874-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="66874-449">Размер передачи данных в битах, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="66874-449">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="66874-450">Значение 0 указывает на отсутствие ошибки.</span><span class="sxs-lookup"><span data-stu-id="66874-450">A value of 0 indicates no error.</span></span> <span data-ttu-id="66874-451">Если свойство **errorInfo** равно 3 ("ОК"), то этому свойству должно быть присвоено значение 0.</span><span class="sxs-lookup"><span data-stu-id="66874-451">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

<span data-ttu-id="66874-452">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-452">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-453">**флуштимер**</span><span class="sxs-lookup"><span data-stu-id="66874-453">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-454">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66874-454">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66874-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-456">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Cache \| 003,14 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" секунды ")</span><span class="sxs-lookup"><span data-stu-id="66874-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="66874-457">Максимальное количество времени (в секундах), в течение которого изменившиеся строки или контейнеры могут остаться в кэше перед очисткой.</span><span class="sxs-lookup"><span data-stu-id="66874-457">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="66874-458">Значение 0 указывает, что очистка кэша не контролируется таймером записи на диск.</span><span class="sxs-lookup"><span data-stu-id="66874-458">A value of 0 indicates that a cache flush is not controlled by a flushing timer.</span></span>

</dd> <dt>

<span data-ttu-id="66874-459">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="66874-459">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-460">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="66874-460">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="66874-461">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-462">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="66874-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="66874-463">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="66874-463">Indicates when the object was installed.</span></span> <span data-ttu-id="66874-464">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="66874-464">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="66874-465">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66874-465">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-466">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="66874-466">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-467">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66874-467">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66874-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-469">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="66874-469">Last error code reported by the logical device.</span></span>

<span data-ttu-id="66874-470">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-471">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="66874-471">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-472">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-473">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-474">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="66874-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="66874-475">Указывает, является ли это первичным, вторичным или третичным кэшем.</span><span class="sxs-lookup"><span data-stu-id="66874-475">Specifies whether this is the primary, secondary or tertiary cache.</span></span> <span data-ttu-id="66874-476">Можно также определить «other», «Unknown» и «not применимым».</span><span class="sxs-lookup"><span data-stu-id="66874-476">"Other", "Unknown", and "Not Applicable" also can be defined.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-477"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-478">Другое</span><span class="sxs-lookup"><span data-stu-id="66874-478">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-479"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-480">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-480">Unknown.</span></span>

</dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="66874-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Основной** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-481"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd>

<span data-ttu-id="66874-482">Первичная.</span><span class="sxs-lookup"><span data-stu-id="66874-482">Primary.</span></span>

</dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="66874-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Вторичная** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-483"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd>

<span data-ttu-id="66874-484">Вторичной.</span><span class="sxs-lookup"><span data-stu-id="66874-484">Secondary.</span></span>

</dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="66874-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Третичная** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-485"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd>

<span data-ttu-id="66874-486">Третьем.</span><span class="sxs-lookup"><span data-stu-id="66874-486">Tertiary.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="66874-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-487"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="66874-488">Не применяется</span><span class="sxs-lookup"><span data-stu-id="66874-488">Not applicable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-489">**линесизе**</span><span class="sxs-lookup"><span data-stu-id="66874-489">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-490">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66874-490">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="66874-491">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-492">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,10 "), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="66874-492">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="66874-493">Размер (в байтах) одного контейнера или строки кэша.</span><span class="sxs-lookup"><span data-stu-id="66874-493">Size, in bytes, of a single cache bucket or line.</span></span>

</dd> <dt>

<span data-ttu-id="66874-494">**Name**</span><span class="sxs-lookup"><span data-stu-id="66874-494">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-495">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-496">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-497">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="66874-497">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="66874-498">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="66874-498">Label by which the object is known.</span></span> <span data-ttu-id="66874-499">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="66874-499">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="66874-500">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66874-500">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-501">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="66874-501">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-502">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66874-502">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66874-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-504">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="66874-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="66874-505">Количество последовательных блоков, каждый из которых заблокирует размер значения, содержащегося **в свойстве, которое** формирует экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="66874-505">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="66874-506">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="66874-506">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="66874-507">Если **значение параметра DataSize равно 1** (один), это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="66874-507">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="66874-508">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="66874-508">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="66874-509">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="66874-509">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-510">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="66874-510">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-511">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-513">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="66874-513">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="66874-514">Строка свободной формы, которая предоставляет сведения, если свойство **ErrorType** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="66874-514">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="66874-515">Если значение не равно 1, то эта строка не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-515">If it is not set to 1, then this string has no meaning.</span></span>

<span data-ttu-id="66874-516">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-516">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-517">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="66874-517">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-518">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-520">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="66874-520">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="66874-521">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="66874-521">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="66874-522">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="66874-522">Example: "\*PNP030b"</span></span>

<span data-ttu-id="66874-523">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-524">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="66874-524">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-525">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="66874-525">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="66874-526">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-527">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="66874-527">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="66874-528">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="66874-529"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="66874-530">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="66874-530">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="66874-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-531"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-532">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="66874-532">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66874-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-533"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-534">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="66874-534">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="66874-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-535"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="66874-536">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="66874-536">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="66874-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="66874-537"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="66874-538">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="66874-538">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="66874-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-539"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="66874-540">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="66874-540">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="66874-541">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="66874-541">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="66874-542">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="66874-542">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="66874-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-543"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="66874-544">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="66874-544">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="66874-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="66874-545"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="66874-546">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="66874-546">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-547">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="66874-547">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-548">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66874-548">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66874-549">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-549">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-550">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="66874-550">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="66874-551">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="66874-551">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="66874-552">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="66874-552">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="66874-553">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="66874-553">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="66874-554">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-554">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-555">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="66874-555">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-556">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-557">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-557">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-558">Строка свободной формы, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="66874-558">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="66874-559">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="66874-559">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-560">**реадполици**</span><span class="sxs-lookup"><span data-stu-id="66874-560">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-561">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-562">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-563">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="66874-563">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="66874-564">Политика, применяемая кэшем для обработки запросов на чтение.</span><span class="sxs-lookup"><span data-stu-id="66874-564">Policy employed by the cache for handling read requests.</span></span> <span data-ttu-id="66874-565">Если политика чтения определяется отдельно, то есть для каждого запроса, следует указать значение 6 ("определение на операцию ввода-вывода").</span><span class="sxs-lookup"><span data-stu-id="66874-565">If the read policy is determined individually, that is, for each request, then the value 6 ("Determination per I/O") should be specified.</span></span> <span data-ttu-id="66874-566">Значения "Other" и "Unknown" также являются допустимыми.</span><span class="sxs-lookup"><span data-stu-id="66874-566">"Other" and "Unknown" are also valid values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-567"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-568">Другое</span><span class="sxs-lookup"><span data-stu-id="66874-568">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-569"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-570">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-570">Unknown.</span></span>

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="66874-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-571"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read** (3)</span></span>


</dt> <dd>

<span data-ttu-id="66874-572">доступ для чтения;</span><span class="sxs-lookup"><span data-stu-id="66874-572">Read.</span></span>

</dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="66874-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Упреждающее чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-573"><span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>**Read-Ahead** (4)</span></span>


</dt> <dd>

<span data-ttu-id="66874-574">Упреждающее чтение.</span><span class="sxs-lookup"><span data-stu-id="66874-574">Read-ahead.</span></span>

</dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="66874-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Чтение и упреждающее** чтение (5)</span><span class="sxs-lookup"><span data-stu-id="66874-575"><span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>**Read and Read-Ahead** (5)</span></span>


</dt> <dd>

<span data-ttu-id="66874-576">Чтение и чтение с опережением.</span><span class="sxs-lookup"><span data-stu-id="66874-576">Read and read-ahead.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="66874-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Определение для операций ввода-вывода** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-577"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="66874-578">Определение для операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="66874-578">Determination per I/O.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-579">**реплацементполици**</span><span class="sxs-lookup"><span data-stu-id="66874-579">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-580">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-580">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-581">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-582">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="66874-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="66874-583">Целочисленное перечисление, описывающее алгоритм, который определяет, какие строки или контейнеры кэша следует использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="66874-583">Integer enumeration describing the algorithm that determines which cache lines or buckets should be re-used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-584"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-585">Другое</span><span class="sxs-lookup"><span data-stu-id="66874-585">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-586"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-587">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-587">Unknown.</span></span>

</dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="66874-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Наименее недавно использованный (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-588"><span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd>

<span data-ttu-id="66874-589">Наименее недавно использованный (LRU).</span><span class="sxs-lookup"><span data-stu-id="66874-589">Least recently used (LRU).</span></span>

</dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="66874-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**Первым поступил (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-590"><span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>**First In First Out (FIFO)** (4)</span></span>


</dt> <dd>

<span data-ttu-id="66874-591">Первым поступил, первым обслужен (FIFO).</span><span class="sxs-lookup"><span data-stu-id="66874-591">First-in, first-out (FIFO).</span></span>

</dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="66874-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last-First Out (ЛИФО)** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-592"><span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="66874-593">Последнее пошаговое извлечение (ЛИФО).</span><span class="sxs-lookup"><span data-stu-id="66874-593">Last-in, first-out (LIFO).</span></span>

</dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="66874-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Наименее часто используемые (ЛФУ)** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-594"><span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="66874-595">Наименее часто используемые (ЛФУ.)</span><span class="sxs-lookup"><span data-stu-id="66874-595">Least frequently used (LFU.)</span></span>

</dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="66874-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Наиболее часто используемые (** 7)</span><span class="sxs-lookup"><span data-stu-id="66874-596"><span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="66874-597">Наиболее часто используемые (наиболее популярные программные).</span><span class="sxs-lookup"><span data-stu-id="66874-597">Most frequently used (MFU).</span></span>

</dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="66874-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Несколько алгоритмов, зависящих от данных** (8)</span><span class="sxs-lookup"><span data-stu-id="66874-598"><span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd>

<span data-ttu-id="66874-599">Зависящие от данных множественные алгоритмы.</span><span class="sxs-lookup"><span data-stu-id="66874-599">Data-dependent multiple algorithms.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-600">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="66874-600">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-601">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="66874-601">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="66874-602">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-603">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,3 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="66874-603">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="66874-604">Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="66874-604">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="66874-605">Начальный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="66874-605">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="66874-606">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="66874-606">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="66874-607">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-607">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-608">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="66874-608">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-609">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-609">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-610">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-610">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-611">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="66874-611">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="66874-612">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="66874-612">String that indicates the current status of the object.</span></span> <span data-ttu-id="66874-613">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="66874-613">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="66874-614">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="66874-614">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="66874-615">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="66874-615">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="66874-616">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="66874-616">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="66874-617">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="66874-617">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="66874-618">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="66874-618">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="66874-619">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="66874-619">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="66874-620">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="66874-620">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="66874-621">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="66874-621">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="66874-622">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="66874-622">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="66874-623">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="66874-623">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-624">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="66874-624">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="66874-625">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="66874-625">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="66874-626">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="66874-626">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="66874-627">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="66874-627">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="66874-628">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="66874-628">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="66874-629">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="66874-629">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="66874-630">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="66874-630">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="66874-631">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="66874-631">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="66874-632">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="66874-632">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-633">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="66874-633">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-634">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-634">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-635">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-636">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="66874-636">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="66874-637">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="66874-637">State of the logical device.</span></span> <span data-ttu-id="66874-638">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="66874-638">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="66874-639">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-640">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-640">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-641">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-641">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="66874-642">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-642">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="66874-643">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-643">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="66874-644">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-644">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="66874-645">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="66874-645">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-646">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-647">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-648">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66874-648">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66874-649">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="66874-649">The scoping system's creation class name.</span></span>

<span data-ttu-id="66874-650">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-650">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-651">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="66874-651">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-652">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="66874-652">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="66874-653">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-653">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="66874-654">Указывает, является ли информация об адресе в свойстве **еррораддресс** адресом системного уровня (**true**) или физическим адресом (**false**).</span><span class="sxs-lookup"><span data-stu-id="66874-654">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="66874-655">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="66874-655">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="66874-656">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-656">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-657">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="66874-657">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-658">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="66874-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="66874-659">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-659">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-660">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66874-660">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66874-661">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="66874-661">The scoping system's name.</span></span>

<span data-ttu-id="66874-662">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="66874-662">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="66874-663">**вритеполици**</span><span class="sxs-lookup"><span data-stu-id="66874-663">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66874-664">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="66874-664">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="66874-665">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="66874-665">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66874-666">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="66874-666">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="66874-667">Определяет, производится ли в кэше обратная запись или запись в кэш, а также сведения об отдельности для каждого ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="66874-667">Defines whether the cache is write-back or write-through, or whether the information "Varies with Address" or is defined individually for each input/output.</span></span> <span data-ttu-id="66874-668">Можно также указать "Other" и "Unknown".</span><span class="sxs-lookup"><span data-stu-id="66874-668">"Other" and "Unknown" also can be specified.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="66874-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="66874-669"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="66874-670">Другое</span><span class="sxs-lookup"><span data-stu-id="66874-670">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="66874-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="66874-671"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="66874-672">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="66874-672">Unknown.</span></span>

</dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="66874-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Обратная запись** (3)</span><span class="sxs-lookup"><span data-stu-id="66874-673"><span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>**Write Back** (3)</span></span>


</dt> <dd>

<span data-ttu-id="66874-674">Обратная запись.</span><span class="sxs-lookup"><span data-stu-id="66874-674">Write back.</span></span>

</dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="66874-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>Сквозная **запись** (4)</span><span class="sxs-lookup"><span data-stu-id="66874-675"><span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>**Write Through** (4)</span></span>


</dt> <dd>

<span data-ttu-id="66874-676">Запись с помощью.</span><span class="sxs-lookup"><span data-stu-id="66874-676">Write through.</span></span>

</dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="66874-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Зависит от адреса** (5)</span><span class="sxs-lookup"><span data-stu-id="66874-677"><span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>**Varies with Address** (5)</span></span>


</dt> <dd>

<span data-ttu-id="66874-678">Зависит от адреса.</span><span class="sxs-lookup"><span data-stu-id="66874-678">Varies with address.</span></span>

</dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="66874-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Определение для операций ввода-вывода** (6)</span><span class="sxs-lookup"><span data-stu-id="66874-679"><span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>**Determination Per I/O** (6)</span></span>


</dt> <dd>

<span data-ttu-id="66874-680">Определение для операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="66874-680">Determination per I/O.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66874-681">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66874-681">Remarks</span></span>

<span data-ttu-id="66874-682">Класс **CIM \_ качемемори** является производным от [**\_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="66874-682">The **CIM\_CacheMemory** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="66874-683">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="66874-683">WMI does not implement this class.</span></span> <span data-ttu-id="66874-684">Дополнительные сведения о классах, производных от **CIM \_ качемемори**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="66874-684">For more information about classes derived from **CIM\_CacheMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="66874-685">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="66874-685">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="66874-686">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="66874-686">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="66874-687">Требования</span><span class="sxs-lookup"><span data-stu-id="66874-687">Requirements</span></span>



| <span data-ttu-id="66874-688">Требование</span><span class="sxs-lookup"><span data-stu-id="66874-688">Requirement</span></span> | <span data-ttu-id="66874-689">Значение</span><span class="sxs-lookup"><span data-stu-id="66874-689">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66874-690">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66874-690">Minimum supported client</span></span><br/> | <span data-ttu-id="66874-691">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66874-691">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66874-692">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66874-692">Minimum supported server</span></span><br/> | <span data-ttu-id="66874-693">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66874-693">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66874-694">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="66874-694">Namespace</span></span><br/>                | <span data-ttu-id="66874-695">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="66874-695">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66874-696">MOF</span><span class="sxs-lookup"><span data-stu-id="66874-696">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66874-697"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66874-697"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66874-698">DLL</span><span class="sxs-lookup"><span data-stu-id="66874-698">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66874-699"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66874-699"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66874-700">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66874-700">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66874-701">**\_Память CIM**</span><span class="sxs-lookup"><span data-stu-id="66874-701">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

