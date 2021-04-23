---
description: '&Win32 \_ качемемори \# 32; Класс WMI представляет внутреннюю и внешнюю кэш-память в компьютерной системе.'
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Класс Win32_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83a8fefbe1104f24f208d232b8f6bc134efefd83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896289"
---
# <a name="win32_cachememory-class"></a><span data-ttu-id="af7d4-103">\_Класс Win32 качемемори</span><span class="sxs-lookup"><span data-stu-id="af7d4-103">Win32\_CacheMemory class</span></span>

<span data-ttu-id="af7d4-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ качемемори для Win32** представляет внутреннюю и внешнюю кэш-память в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="af7d4-104">The **Win32\_CacheMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents internal and external cache memory on a computer system.</span></span>

<span data-ttu-id="af7d4-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="af7d4-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="af7d4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="af7d4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af7d4-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a><span data-ttu-id="af7d4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="af7d4-108">Members</span></span>

<span data-ttu-id="af7d4-109">Класс **Win32 \_ качемемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="af7d4-109">The **Win32\_CacheMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="af7d4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="af7d4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="af7d4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="af7d4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="af7d4-112">Методы</span><span class="sxs-lookup"><span data-stu-id="af7d4-112">Methods</span></span>

<span data-ttu-id="af7d4-113">Класс **Win32 \_ качемемори** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="af7d4-113">The **Win32\_CacheMemory** class has these methods.</span></span>



| <span data-ttu-id="af7d4-114">Метод</span><span class="sxs-lookup"><span data-stu-id="af7d4-114">Method</span></span>            | <span data-ttu-id="af7d4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="af7d4-115">Description</span></span>                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af7d4-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="af7d4-116">**Reset**</span></span>         | <span data-ttu-id="af7d4-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="af7d4-117">Not implemented.</span></span> <span data-ttu-id="af7d4-118">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ качемемори**](cim-cachememory.md) .</span><span class="sxs-lookup"><span data-stu-id="af7d4-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="af7d4-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="af7d4-119">**SetPowerState**</span></span> | <span data-ttu-id="af7d4-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="af7d4-120">Not implemented.</span></span> <span data-ttu-id="af7d4-121">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ качемемори**](cim-cachememory.md) .</span><span class="sxs-lookup"><span data-stu-id="af7d4-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_CacheMemory**](cim-cachememory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="af7d4-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="af7d4-122">Properties</span></span>

<span data-ttu-id="af7d4-123">Класс **Win32 \_ качемемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-123">The **Win32\_CacheMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af7d4-124">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="af7d4-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-127">Тип доступа.</span><span class="sxs-lookup"><span data-stu-id="af7d4-127">Type of access.</span></span>

<span data-ttu-id="af7d4-128">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="af7d4-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="af7d4-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-132">Возможность записи</span><span class="sxs-lookup"><span data-stu-id="af7d4-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="af7d4-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="af7d4-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-135">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="af7d4-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-136">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="af7d4-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,18 "," MIF. \|Массив физической памяти DMTF \| 001,13 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af7d4-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-139">Массив октетов, содержащих дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="af7d4-139">Array of octets that hold additional error information.</span></span> <span data-ttu-id="af7d4-140">Например, синдром ECC или возврат битовой проверки, если используется методология ошибок на основе CRC.</span><span class="sxs-lookup"><span data-stu-id="af7d4-140">An example is ECC Syndrome or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="af7d4-141">В последнем случае, если обнаружена Одноразрядная ошибка и известен алгоритм CRC, можно определить точный бит, в котором произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="af7d4-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="af7d4-142">Этот тип данных (ECC синдром, бит проверки, битные данные четности или другие предоставленные поставщиком сведения) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="af7d4-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="af7d4-143">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-143">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-144">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-144">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-145">**Ассоциативность**</span><span class="sxs-lookup"><span data-stu-id="af7d4-145">**Associativity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,15 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.15")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-149">Целочисленное перечисление, определяющее ассоциативность системного кэша.</span><span class="sxs-lookup"><span data-stu-id="af7d4-149">An integer enumeration that defines the system cache associativity.</span></span>

<span data-ttu-id="af7d4-150">Это значение берется из элемента **ассоциативности** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-150">This value comes from the **Associativity** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-151">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-151">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-152">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-152">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-153">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-153">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

<span data-ttu-id="af7d4-154">**Прямое сопоставление** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-154">**Direct Mapped** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="af7d4-155">**2-направленный набор-ассоциативный** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-155">**2-way Set-Associative** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="af7d4-156">**4-направленный набор-ассоциативный** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-156">**4-way Set-Associative** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

<span data-ttu-id="af7d4-157">**Полностью ассоциативная** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-157">**Fully Associative** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="af7d4-158">**8-направленное множество-ассоциативное** (7)</span><span class="sxs-lookup"><span data-stu-id="af7d4-158">**8-way Set-Associative** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

<span data-ttu-id="af7d4-159">**16-направленный набор-ассоциативный** (8)</span><span class="sxs-lookup"><span data-stu-id="af7d4-159">**16-way Set-Associative** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-160">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="af7d4-160">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-163">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-164">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-164">Availability and status of the device.</span></span>

<span data-ttu-id="af7d4-165">Это значение берется из элемента **конфигурации кэша** структуры сведений о **кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-165">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-166">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-166">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="af7d4-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-169"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-170">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="af7d4-170">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="af7d4-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-171"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="af7d4-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-172"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af7d4-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-173"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="af7d4-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="af7d4-174"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="af7d4-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="af7d4-175"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="af7d4-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="af7d4-176"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="af7d4-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="af7d4-177"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="af7d4-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="af7d4-178"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="af7d4-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="af7d4-179"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="af7d4-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="af7d4-180"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-181">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-181">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="af7d4-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="af7d4-182"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-183">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="af7d4-183">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="af7d4-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="af7d4-184"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-185">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="af7d4-185">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="af7d4-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="af7d4-186"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="af7d4-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="af7d4-187"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-188">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="af7d4-188">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="af7d4-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="af7d4-189"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-190">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="af7d4-190">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="af7d4-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="af7d4-191"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-192">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="af7d4-192">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="af7d4-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="af7d4-193"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-194">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="af7d4-194">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="af7d4-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="af7d4-195"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-196">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="af7d4-196">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-197">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="af7d4-197">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-198">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af7d4-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-200">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-201">Размер в байтах блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="af7d4-201">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="af7d4-202">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="af7d4-202">If unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="af7d4-203">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-203">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="af7d4-204">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af7d4-204">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-205">**качеспид**</span><span class="sxs-lookup"><span data-stu-id="af7d4-205">**CacheSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-206">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-206">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-208">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| скорость кэша SMBIOS Type 7 \| "), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("наносекундах")</span><span class="sxs-lookup"><span data-stu-id="af7d4-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Cache Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanoseconds")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-209">Скорость кэша.</span><span class="sxs-lookup"><span data-stu-id="af7d4-209">Speed of the cache.</span></span>

<span data-ttu-id="af7d4-210">Это значение берется из элемента **скорость кэширования** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-210">This value comes from the **Cache Speed** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-211">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="af7d4-211">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-212">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-212">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-214">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,9 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-215">Тип кэша.</span><span class="sxs-lookup"><span data-stu-id="af7d4-215">Type of cache.</span></span>

<span data-ttu-id="af7d4-216">Это значение берется из члена **типа системного кэша** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-216">This value comes from the **System Cache Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-217">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-217">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-218">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-218">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-219">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-219">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

<span data-ttu-id="af7d4-220">**Инструкция** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-220">**Instruction** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

<span data-ttu-id="af7d4-221">**Данные** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-221">**Data** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

<span data-ttu-id="af7d4-222">**Единая** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-222">**Unified** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-223">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="af7d4-223">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-226">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="af7d4-226">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-227">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="af7d4-227">Short description of the object a one-line string.</span></span>

<span data-ttu-id="af7d4-228">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-228">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-229">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="af7d4-229">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-230">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-232">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af7d4-232">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-233">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="af7d4-233">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="af7d4-234">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-234">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="af7d4-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-235"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="af7d4-236"> (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-236">(0)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-237">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-237">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="af7d4-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-238"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="af7d4-239">(1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-239">(1)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-240">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-240">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af7d4-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-241"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="af7d4-242">(2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-242">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="af7d4-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-243"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="af7d4-244">(3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-244">(3)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-245">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="af7d4-245">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="af7d4-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-246"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="af7d4-247">(4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-247">(4)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-248">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-248">Device is not working properly.</span></span> <span data-ttu-id="af7d4-249">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="af7d4-249">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="af7d4-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-250"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="af7d4-251">(5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-251">(5)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-252">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="af7d4-252">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="af7d4-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-253"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="af7d4-254"> (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-254">(6)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-255">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="af7d4-255">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="af7d4-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-256"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="af7d4-257">(7)</span><span class="sxs-lookup"><span data-stu-id="af7d4-257">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="af7d4-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-258"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="af7d4-259">(8)</span><span class="sxs-lookup"><span data-stu-id="af7d4-259">(8)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-260">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-260">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="af7d4-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-261"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="af7d4-262">(9)</span><span class="sxs-lookup"><span data-stu-id="af7d4-262">(9)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-263">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-263">Device is not working properly.</span></span> <span data-ttu-id="af7d4-264">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-264">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="af7d4-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-265"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="af7d4-266">(10)</span><span class="sxs-lookup"><span data-stu-id="af7d4-266">(10)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-267">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="af7d4-267">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="af7d4-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-268"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="af7d4-269">(11)</span><span class="sxs-lookup"><span data-stu-id="af7d4-269">(11)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-270">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-270">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="af7d4-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-271"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="af7d4-272">(12)</span><span class="sxs-lookup"><span data-stu-id="af7d4-272">(12)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-273">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="af7d4-273">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="af7d4-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-274"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="af7d4-275">(13)</span><span class="sxs-lookup"><span data-stu-id="af7d4-275">(13)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-276">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-276">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="af7d4-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-277"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="af7d4-278">(14)</span><span class="sxs-lookup"><span data-stu-id="af7d4-278">(14)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-279">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="af7d4-279">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="af7d4-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-280"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="af7d4-281">(15)</span><span class="sxs-lookup"><span data-stu-id="af7d4-281">(15)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-282">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="af7d4-282">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="af7d4-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-283"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="af7d4-284">(16)</span><span class="sxs-lookup"><span data-stu-id="af7d4-284">(16)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-285">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="af7d4-285">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="af7d4-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-286"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="af7d4-287">(17)</span><span class="sxs-lookup"><span data-stu-id="af7d4-287">(17)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-288">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="af7d4-288">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af7d4-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-289"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="af7d4-290">(18)</span><span class="sxs-lookup"><span data-stu-id="af7d4-290">(18)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-291">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="af7d4-291">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="af7d4-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-292"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="af7d4-293">(19)</span><span class="sxs-lookup"><span data-stu-id="af7d4-293">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="af7d4-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-294"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="af7d4-295">(20)</span><span class="sxs-lookup"><span data-stu-id="af7d4-295">(20)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-296">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="af7d4-296">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="af7d4-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-297"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="af7d4-298">(21)</span><span class="sxs-lookup"><span data-stu-id="af7d4-298">(21)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-299">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="af7d4-299">System failure.</span></span> <span data-ttu-id="af7d4-300">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="af7d4-300">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="af7d4-301">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="af7d4-301">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="af7d4-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-302"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="af7d4-303">(22)</span><span class="sxs-lookup"><span data-stu-id="af7d4-303">(22)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-304">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="af7d4-304">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="af7d4-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-305"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="af7d4-306">(23)</span><span class="sxs-lookup"><span data-stu-id="af7d4-306">(23)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-307">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="af7d4-307">System failure.</span></span> <span data-ttu-id="af7d4-308">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="af7d4-308">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="af7d4-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-309"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="af7d4-310">(24)</span><span class="sxs-lookup"><span data-stu-id="af7d4-310">(24)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-311">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="af7d4-311">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="af7d4-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-312"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="af7d4-313">(25)</span><span class="sxs-lookup"><span data-stu-id="af7d4-313">(25)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-314">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="af7d4-314">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="af7d4-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-315"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="af7d4-316">(26)</span><span class="sxs-lookup"><span data-stu-id="af7d4-316">(26)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-317">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="af7d4-317">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="af7d4-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-318"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="af7d4-319">(27)</span><span class="sxs-lookup"><span data-stu-id="af7d4-319">(27)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-320">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="af7d4-320">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="af7d4-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-321"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="af7d4-322">(28)</span><span class="sxs-lookup"><span data-stu-id="af7d4-322">(28)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-323">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="af7d4-323">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="af7d4-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-324"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="af7d4-325">(29)</span><span class="sxs-lookup"><span data-stu-id="af7d4-325">(29)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-326">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="af7d4-326">Device is disabled.</span></span> <span data-ttu-id="af7d4-327">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="af7d4-327">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="af7d4-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-328"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="af7d4-329">(30)</span><span class="sxs-lookup"><span data-stu-id="af7d4-329">(30)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-330">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="af7d4-330">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="af7d4-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="af7d4-331"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="af7d4-332">1-31</span><span class="sxs-lookup"><span data-stu-id="af7d4-332">(31)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-333">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-333">Device is not working properly.</span></span> <span data-ttu-id="af7d4-334">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="af7d4-334">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-335">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="af7d4-335">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-336">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="af7d4-336">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-338">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af7d4-338">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-339">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="af7d4-339">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="af7d4-340">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-341">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="af7d4-341">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-342">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="af7d4-342">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-344">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-345">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="af7d4-345">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="af7d4-346">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-346">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-347">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-347">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-348">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="af7d4-348">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-349">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-351">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af7d4-351">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-352">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="af7d4-352">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="af7d4-353">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="af7d4-353">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="af7d4-354">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-355">**куррентсрам**</span><span class="sxs-lookup"><span data-stu-id="af7d4-355">**CurrentSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-356">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="af7d4-356">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-358">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 7, \| текущий тип SRAM")</span><span class="sxs-lookup"><span data-stu-id="af7d4-358">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Current SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-359">Массив типов памяти (SRAM), используемых для кэш-памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-359">Array of types of Static Random Access Memory (SRAM) being used for the cache memory.</span></span>

<span data-ttu-id="af7d4-360">Это значение берется из **текущего элемента типа SRAM** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-360">This value comes from the **Current SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-361">**Другое** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-361">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-362">**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-362">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="af7d4-363">**Без пакета** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-363">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="af7d4-364">**Пакет** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-364">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="af7d4-365">**Ускорение конвейера** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-365">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="af7d4-366">**Синхронный** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-366">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="af7d4-367">**Асинхронный** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-367">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-368">**Описание**</span><span class="sxs-lookup"><span data-stu-id="af7d4-368">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-371">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="af7d4-371">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-372">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="af7d4-372">Description of the object.</span></span>

<span data-ttu-id="af7d4-373">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-373">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-374">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="af7d4-374">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-375">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-375">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-377">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="af7d4-377">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-378">Уникальный идентификатор кэша, представленного экземпляром **Win32 \_ качемемори**.</span><span class="sxs-lookup"><span data-stu-id="af7d4-378">Unique identifier of the cache represented by an instance of **Win32\_CacheMemory**.</span></span>

<span data-ttu-id="af7d4-379">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="af7d4-380">Пример: "кэш памяти 1"</span><span class="sxs-lookup"><span data-stu-id="af7d4-380">Example: "Cache Memory 1"</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-381">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="af7d4-381">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-382">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af7d4-382">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-384">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,4 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,5 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-385">Конечный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-385">Ending address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="af7d4-386">Конечный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="af7d4-386">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="af7d4-387">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-387">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="af7d4-388">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af7d4-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-389">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="af7d4-389">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-390">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-392">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,15 "," MIF. \|Массив физической памяти DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-393">Операция доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="af7d4-393">Memory access operation that caused the last error.</span></span> <span data-ttu-id="af7d4-394">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="af7d4-394">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="af7d4-395">Если значение **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-395">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-396">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-396">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-397">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-398">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="af7d4-399">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-399">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="af7d4-400">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-400">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="af7d4-401">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-401">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-402">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="af7d4-402">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-403">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af7d4-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-405">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. \|Массив физической памяти DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-406">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-406">Address of the last memory error.</span></span> <span data-ttu-id="af7d4-407">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="af7d4-407">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="af7d4-408">Если значение **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-408">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-409">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-409">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="af7d4-410">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af7d4-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-411">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="af7d4-411">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-412">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="af7d4-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-414">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="af7d4-414">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="af7d4-415">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-416">**ерроркорректтипе**</span><span class="sxs-lookup"><span data-stu-id="af7d4-416">**ErrorCorrectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-417">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-419">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип SMBIOS \| 7 типа \| исправления ошибок")</span><span class="sxs-lookup"><span data-stu-id="af7d4-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Error Correction Type")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-420">Метод исправления ошибок, используемый кэшовой памятью.</span><span class="sxs-lookup"><span data-stu-id="af7d4-420">Error correction method used by the cache memory.</span></span>

<span data-ttu-id="af7d4-421">Это значение берется из элемента **типа исправления ошибок** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-421">This value comes from the **Error Correction Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="af7d4-422">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-422">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-423">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-423">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-424">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-424">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="af7d4-425">**Нет** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-425">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="af7d4-426">**Четность** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-426">**Parity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="af7d4-427">**Одноразрядный ECC** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-427">**Single-bit ECC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="af7d4-428">**Многоразрядный ECC** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-428">**Multi-bit ECC** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-429">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="af7d4-429">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-430">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="af7d4-430">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-432">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. \|Массив физической памяти DMTF \| 001,12 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="af7d4-432">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-433">Массив данных, захваченных во время последней ошибочной операции доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-433">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="af7d4-434">Данные занимают первые *n* октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="af7d4-434">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="af7d4-435">Если **еррортрансферсизе** имеет значение 0 (ноль), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-435">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-436">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-436">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-437">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="af7d4-437">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-438">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-440">Упорядочивание данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="af7d4-440">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="af7d4-441">Если **еррортрансферсизе** имеет значение 0 (ноль), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-441">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-442">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-442">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-443">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-443">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="af7d4-444">**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-444">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="af7d4-445">**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-445">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-446">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="af7d4-446">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-447">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-449">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="af7d4-449">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="af7d4-450">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-450">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-451">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="af7d4-451">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-452">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-452">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-454">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**Осереррордескриптион**")</span><span class="sxs-lookup"><span data-stu-id="af7d4-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-455">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="af7d4-455">Type of error that occurred most recently.</span></span> <span data-ttu-id="af7d4-456">Значения 12-14 в схеме CIM не определены, поскольку в DMI они сочетают семантику типа ошибки и правильность ее выполнения.</span><span class="sxs-lookup"><span data-stu-id="af7d4-456">The values 12-14 are undefined in the CIM schema because in DMI they mix the semantics of the type of error and whether it was correctable or not.</span></span> <span data-ttu-id="af7d4-457">Последнее указывается в свойстве **корректаблиррор**.</span><span class="sxs-lookup"><span data-stu-id="af7d4-457">The latter is indicated in the property **CorrectableError**.</span></span>

<span data-ttu-id="af7d4-458">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-458">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-459">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-460">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-460">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="af7d4-461">**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-461">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="af7d4-462">**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-462">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="af7d4-463">**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-463">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="af7d4-464">**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-464">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="af7d4-465">**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="af7d4-465">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="af7d4-466">**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="af7d4-466">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="af7d4-467">**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="af7d4-467">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="af7d4-468">**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="af7d4-468">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="af7d4-469">**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="af7d4-469">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="af7d4-470">Не **определено** (12)</span><span class="sxs-lookup"><span data-stu-id="af7d4-470">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="af7d4-471">Не **определено** (13)</span><span class="sxs-lookup"><span data-stu-id="af7d4-471">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="af7d4-472">Не **определено** (14)</span><span class="sxs-lookup"><span data-stu-id="af7d4-472">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-473">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="af7d4-473">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-476">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив физической памяти DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-476">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-477">Подробные сведения о алгоритмах четности и CRC, а также об ECC или других используемых механизмах.</span><span class="sxs-lookup"><span data-stu-id="af7d4-477">Details on the parity or CRC algorithms, ECC, or other mechanisms used.</span></span>

<span data-ttu-id="af7d4-478">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-478">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-479">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="af7d4-479">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-480">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af7d4-480">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-482">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,21 "," MIF. \|Массив физической памяти DMTF \| 001,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-482">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-483">Диапазон в байтах, до которого может быть разрешена Последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="af7d4-483">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="af7d4-484">Например, если адреса ошибок разрешаются в бит 11 (то есть на типичном уровне страницы), ошибки могут быть разрешены до 4 КБ, а значение этого свойства равно 4000.</span><span class="sxs-lookup"><span data-stu-id="af7d4-484">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="af7d4-485">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-485">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-486">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-486">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="af7d4-487">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af7d4-487">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-488">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="af7d4-488">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-489">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="af7d4-489">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-491">Время, когда произошла последняя ошибка памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-491">Time that the last memory error occurred.</span></span> <span data-ttu-id="af7d4-492">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="af7d4-492">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="af7d4-493">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-493">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-494">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-494">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-495">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="af7d4-495">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-496">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-498">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,16 "," MIF. \|Массив физической памяти DMTF \| 001,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-498">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-499">Размер передачи данных в битах, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="af7d4-499">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="af7d4-500">0 (ноль) указывает на отсутствие ошибки.</span><span class="sxs-lookup"><span data-stu-id="af7d4-500">0 (zero) indicates no error.</span></span> <span data-ttu-id="af7d4-501">Если свойство **errorInfo** равно 3 (ОК), то этому свойству должно быть присвоено значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="af7d4-501">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

<span data-ttu-id="af7d4-502">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-502">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-503">**флуштимер**</span><span class="sxs-lookup"><span data-stu-id="af7d4-503">**FlushTimer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-504">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-505">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-505">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-506">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Cache \| 003,14 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" секунды ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-506">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.14"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-507">Максимальное количество времени (в секундах), в течение которого изменившиеся строки или контейнеры могут остаться в кэше перед очисткой.</span><span class="sxs-lookup"><span data-stu-id="af7d4-507">Maximum amount of time, in seconds, dirty lines or buckets may remain in the cache before they are flushed.</span></span> <span data-ttu-id="af7d4-508">Значение 0 (ноль) указывает, что очистка кэша не контролируется таймером записи на диск.</span><span class="sxs-lookup"><span data-stu-id="af7d4-508">A value of 0 (zero) indicates that a cache flush is not controlled by a flushing timer.</span></span>

<span data-ttu-id="af7d4-509">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-509">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="af7d4-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-511">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="af7d4-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-513">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-513">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-514">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="af7d4-514">Date and time the object was installed.</span></span> <span data-ttu-id="af7d4-515">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="af7d4-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="af7d4-516">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-517">**инсталледсизе**</span><span class="sxs-lookup"><span data-stu-id="af7d4-517">**InstalledSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-518">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-520">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| Размер установленного SMBIOS типа 7"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="af7d4-520">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Installed Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-521">Текущий размер установленной кэш памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-521">Current size of the installed cache memory.</span></span>

<span data-ttu-id="af7d4-522">Это значение берется из элемента **установленный размер** структуры **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-522">This value comes from the **Installed Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-523">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="af7d4-523">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-524">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-525">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-526">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="af7d4-526">Last error code reported by the logical device.</span></span>

<span data-ttu-id="af7d4-527">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-528">**Уровень**</span><span class="sxs-lookup"><span data-stu-id="af7d4-528">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-529">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-529">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-531">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,2 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-531">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.2")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-532">Уровень кэша.</span><span class="sxs-lookup"><span data-stu-id="af7d4-532">Level of the cache.</span></span>

<span data-ttu-id="af7d4-533">Это значение берется из элемента **конфигурации кэша** структуры сведений о **кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-533">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-534">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-534">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-535"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-536"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span data-ttu-id="af7d4-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Основной** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-537"><span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primary** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span data-ttu-id="af7d4-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Вторичная** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-538"><span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secondary** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span data-ttu-id="af7d4-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Третичная** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-539"><span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Tertiary** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af7d4-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-540"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-541">**линесизе**</span><span class="sxs-lookup"><span data-stu-id="af7d4-541">**LineSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-542">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-543">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-544">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,10 "), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-544">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.10"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-545">Размер (в байтах) одного контейнера или строки кэша.</span><span class="sxs-lookup"><span data-stu-id="af7d4-545">Size, in bytes, of a single cache bucket or line.</span></span>

<span data-ttu-id="af7d4-546">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-546">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-547">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="af7d4-547">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-548">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-548">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-549">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-550">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 7 \| Location")</span><span class="sxs-lookup"><span data-stu-id="af7d4-550">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Location")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-551">Физическое расположение кэшовой памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-551">Physical location of the cache memory.</span></span>

<span data-ttu-id="af7d4-552">Это значение берется из элемента **конфигурации кэша** структуры сведений о **кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-552">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

<span data-ttu-id="af7d4-553">**Внутренний** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-553">**Internal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

<span data-ttu-id="af7d4-554">**Внешний** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-554">**External** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="af7d4-555">**Зарезервировано** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-555">**Reserved** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-556">**Неизвестно** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-556">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-557">**макскачесизе**</span><span class="sxs-lookup"><span data-stu-id="af7d4-557">**MaxCacheSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-558">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af7d4-558">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-559">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-560">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 7: \| максимальный размер кэша"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайтах")</span><span class="sxs-lookup"><span data-stu-id="af7d4-560">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Maximum Cache Size"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-561">Максимальный размер кэша, устанавливаемый для этого конкретного кэша памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-561">Maximum cache size installable to this particular cache memory.</span></span>

<span data-ttu-id="af7d4-562">Это значение берется из параметра **максимального размера кэша** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-562">This value comes from the **Maximum Cache Size** member of the **Cache Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-563">**Name**</span><span class="sxs-lookup"><span data-stu-id="af7d4-563">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-564">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-564">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-565">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-565">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-566">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="af7d4-566">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-567">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="af7d4-567">Label by which the object is known.</span></span> <span data-ttu-id="af7d4-568">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="af7d4-568">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="af7d4-569">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-569">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-570">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="af7d4-570">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-571">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af7d4-571">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-572">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-573">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-573">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-574">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="af7d4-574">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="af7d4-575">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-575">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="af7d4-576">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="af7d4-576">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="af7d4-577">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-577">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="af7d4-578">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af7d4-578">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-579">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="af7d4-579">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-580">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-581">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-582">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="af7d4-582">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-583">Строка произвольной формы, предоставляющая дополнительные сведения, если свойство **ErrorType** имеет значение 1, другое.</span><span class="sxs-lookup"><span data-stu-id="af7d4-583">Free-form string providing more information if the **ErrorType** property is set to 1, Other.</span></span> <span data-ttu-id="af7d4-584">В противном случае эта строка не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-584">Otherwise, this string has no meaning.</span></span>

<span data-ttu-id="af7d4-585">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-585">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-586">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="af7d4-586">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-587">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-588">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-589">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="af7d4-589">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-590">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-590">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="af7d4-591">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="af7d4-592">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="af7d4-592">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-593">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="af7d4-593">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-594">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="af7d4-594">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-595">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-595">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-596">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="af7d4-596">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="af7d4-597">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-597">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-598"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="af7d4-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-599"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="af7d4-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-600"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="af7d4-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-601"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-602">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="af7d4-602">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="af7d4-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-603"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-604">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="af7d4-604">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="af7d4-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-605"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-606">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="af7d4-606">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="af7d4-607">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="af7d4-607">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="af7d4-608">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="af7d4-608">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="af7d4-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-609"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-610">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="af7d4-610">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="af7d4-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="af7d4-611"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="af7d4-612">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="af7d4-612">Timed Power-On Supported</span></span>

<span data-ttu-id="af7d4-613">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="af7d4-613">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-614">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="af7d4-614">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-615">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="af7d4-615">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-616">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-616">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-617">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="af7d4-617">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="af7d4-618">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="af7d4-618">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="af7d4-619">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-619">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-620">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="af7d4-620">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-621">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-621">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-622">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-622">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-623">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="af7d4-623">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="af7d4-624">Это значение берется из элемента **обозначение сокета** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-624">This value comes from the **Socket Designation** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-625">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-625">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-626">**реадполици**</span><span class="sxs-lookup"><span data-stu-id="af7d4-626">**ReadPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-627">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-627">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-628">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-628">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-629">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,13 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-629">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.13")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-630">Политика, которая должна применяться кэшем для обработки запросов на чтение.</span><span class="sxs-lookup"><span data-stu-id="af7d4-630">Policy that shall be employed by the cache for handling read requests.</span></span>

<span data-ttu-id="af7d4-631">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-631">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-632">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-632">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-633">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-633">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="af7d4-634">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-634">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

<span data-ttu-id="af7d4-635">**Упреждающее чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-635">**Read-Ahead** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

<span data-ttu-id="af7d4-636">**Чтение и упреждающее** чтение (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-636">**Read and Read-Ahead** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="af7d4-637">**Определение для операций ввода-вывода** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-637">**Determination Per I/O** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-638">**реплацементполици**</span><span class="sxs-lookup"><span data-stu-id="af7d4-638">**ReplacementPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-639">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-639">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-640">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-640">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-641">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,12 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-641">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.12")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-642">Алгоритм для определения того, какие строки или контейнеры кэша следует использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="af7d4-642">Algorithm to determine which cache lines or buckets should be reused.</span></span>

<span data-ttu-id="af7d4-643">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-643">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-644">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-644">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-645">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-645">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

<span data-ttu-id="af7d4-646">**Наименее недавно использованный (LRU)** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-646">**Least Recently Used (LRU)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

<span data-ttu-id="af7d4-647">**Первым поступил (FIFO)** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-647">**First In First Out (FIFO)** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

<span data-ttu-id="af7d4-648">**Last-First Out (ЛИФО)** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-648">**Last In First Out (LIFO)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

<span data-ttu-id="af7d4-649">**Наименее часто используемые (ЛФУ)** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-649">**Least Frequently Used (LFU)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

<span data-ttu-id="af7d4-650">**Наиболее часто используемые (** 7)</span><span class="sxs-lookup"><span data-stu-id="af7d4-650">**Most Frequently Used (MFU)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

<span data-ttu-id="af7d4-651">**Несколько алгоритмов, зависящих от данных** (8)</span><span class="sxs-lookup"><span data-stu-id="af7d4-651">**Data Dependent Multiple Algorithms** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-652">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="af7d4-652">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-653">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af7d4-653">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-654">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-654">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-655">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,3 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-655">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-656">Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-656">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="af7d4-657">Начальный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="af7d4-657">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="af7d4-658">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-658">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="af7d4-659">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="af7d4-659">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-660">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="af7d4-660">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-661">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-662">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-663">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="af7d4-663">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-664">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="af7d4-664">Current status of the object.</span></span> <span data-ttu-id="af7d4-665">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="af7d4-665">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="af7d4-666">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="af7d4-666">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="af7d4-667">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="af7d4-667">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="af7d4-668">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="af7d4-668">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="af7d4-669">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="af7d4-669">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="af7d4-670">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-670">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="af7d4-671">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="af7d4-671">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="af7d4-672">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="af7d4-672">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="af7d4-673">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="af7d4-673">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="af7d4-674">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="af7d4-674">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-675">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="af7d4-675">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="af7d4-676">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="af7d4-676">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="af7d4-677">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="af7d4-677">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="af7d4-678">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="af7d4-678">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="af7d4-679">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="af7d4-679">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="af7d4-680">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="af7d4-680">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="af7d4-681">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="af7d4-681">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="af7d4-682">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="af7d4-682">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="af7d4-683">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="af7d4-683">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-684">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="af7d4-684">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-685">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-685">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-686">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-686">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-687">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-687">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-688">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="af7d4-688">State of the logical device.</span></span> <span data-ttu-id="af7d4-689">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="af7d4-689">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="af7d4-690">Это значение берется из элемента **конфигурации кэша** структуры сведений о **кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-690">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-691">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-691">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-692">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-692">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-693">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-693">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="af7d4-694">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-694">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="af7d4-695">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-695">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="af7d4-696">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-696">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-697">**суппортедсрам**</span><span class="sxs-lookup"><span data-stu-id="af7d4-697">**SupportedSRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-698">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="af7d4-698">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-699">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-700">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 7 \| поддерживаемый тип SRAM")</span><span class="sxs-lookup"><span data-stu-id="af7d4-700">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 7\|Supported SRAM Type")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-701">Массив поддерживаемых типов статических оперативных памяти (SRAM), которые могут использоваться для кэш-памяти.</span><span class="sxs-lookup"><span data-stu-id="af7d4-701">Array of supported types of Static Random Access Memory (SRAM) that can be used for the cache memory.</span></span>

<span data-ttu-id="af7d4-702">Это значение берется из **поддерживаемого члена типа SRAM** в структуре **сведений о кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-702">This value comes from the **Supported SRAM Type** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-703">**Другое** (0)</span><span class="sxs-lookup"><span data-stu-id="af7d4-703">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-704">**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-704">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

<span data-ttu-id="af7d4-705">**Без пакета** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-705">**Non-Burst** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

<span data-ttu-id="af7d4-706">**Пакет** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-706">**Burst** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

<span data-ttu-id="af7d4-707">**Ускорение конвейера** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-707">**Pipeline Burst** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span data-ttu-id="af7d4-708">**Синхронный** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-708">**Synchronous** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

<span data-ttu-id="af7d4-709">**Асинхронный** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-709">**Asynchronous** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="af7d4-710">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="af7d4-710">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-711">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-711">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-712">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-713">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af7d4-713">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-714">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="af7d4-714">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="af7d4-715">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-715">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-716">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="af7d4-716">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-717">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="af7d4-717">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-718">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-718">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-719">Если **значение — true**, сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня.</span><span class="sxs-lookup"><span data-stu-id="af7d4-719">If **True**, the address information in the property **ErrorAddress** is a system-level address.</span></span> <span data-ttu-id="af7d4-720">Если **значение равно false**, это физический адрес.</span><span class="sxs-lookup"><span data-stu-id="af7d4-720">If **False**, it is a physical address.</span></span> <span data-ttu-id="af7d4-721">Если свойство **errorInfo** равно 3, то это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="af7d4-721">If the **ErrorInfo** property is equal to 3, then this property has no meaning.</span></span>

<span data-ttu-id="af7d4-722">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-722">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-723">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="af7d4-723">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-724">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af7d4-724">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-725">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-725">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-726">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="af7d4-726">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-727">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="af7d4-727">Name of the scoping system.</span></span>

<span data-ttu-id="af7d4-728">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="af7d4-728">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="af7d4-729">**вритеполици**</span><span class="sxs-lookup"><span data-stu-id="af7d4-729">**WritePolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af7d4-730">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af7d4-730">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-731">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af7d4-731">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af7d4-732">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| -системный кэш \| 003,5 ")</span><span class="sxs-lookup"><span data-stu-id="af7d4-732">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Cache\|003.5")</span></span>
</dt> </dl>

<span data-ttu-id="af7d4-733">Определение политики записи.</span><span class="sxs-lookup"><span data-stu-id="af7d4-733">Write policy definition.</span></span>

<span data-ttu-id="af7d4-734">Это значение берется из элемента **конфигурации кэша** структуры сведений о **кэше** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="af7d4-734">This value comes from the **Cache Configuration** member of the **Cache Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="af7d4-735">Это свойство наследуется от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-735">This property is inherited from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="af7d4-736">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="af7d4-736">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af7d4-737">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="af7d4-737">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

<span data-ttu-id="af7d4-738">**Обратная запись** (3)</span><span class="sxs-lookup"><span data-stu-id="af7d4-738">**Write Back** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

<span data-ttu-id="af7d4-739">Сквозная **запись** (4)</span><span class="sxs-lookup"><span data-stu-id="af7d4-739">**Write Through** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

<span data-ttu-id="af7d4-740">**Зависит от адреса** (5)</span><span class="sxs-lookup"><span data-stu-id="af7d4-740">**Varies with Address** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

<span data-ttu-id="af7d4-741">**Определение для операций ввода-вывода** (6)</span><span class="sxs-lookup"><span data-stu-id="af7d4-741">**Determination Per I/O** (6)</span></span>


<span data-ttu-id="af7d4-742"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="af7d4-742"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="af7d4-743">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af7d4-743">Remarks</span></span>

<span data-ttu-id="af7d4-744">Класс **Win32 \_ качемемори** является производным от [**CIM \_ качемемори**](cim-cachememory.md).</span><span class="sxs-lookup"><span data-stu-id="af7d4-744">The **Win32\_CacheMemory** class is derived from [**CIM\_CacheMemory**](cim-cachememory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af7d4-745">Требования</span><span class="sxs-lookup"><span data-stu-id="af7d4-745">Requirements</span></span>



| <span data-ttu-id="af7d4-746">Требование</span><span class="sxs-lookup"><span data-stu-id="af7d4-746">Requirement</span></span> | <span data-ttu-id="af7d4-747">Значение</span><span class="sxs-lookup"><span data-stu-id="af7d4-747">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af7d4-748">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af7d4-748">Minimum supported client</span></span><br/> | <span data-ttu-id="af7d4-749">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af7d4-749">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af7d4-750">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af7d4-750">Minimum supported server</span></span><br/> | <span data-ttu-id="af7d4-751">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af7d4-751">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af7d4-752">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="af7d4-752">Namespace</span></span><br/>                | <span data-ttu-id="af7d4-753">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="af7d4-753">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="af7d4-754">MOF</span><span class="sxs-lookup"><span data-stu-id="af7d4-754">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af7d4-755"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af7d4-755"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="af7d4-756">DLL</span><span class="sxs-lookup"><span data-stu-id="af7d4-756">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af7d4-757"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af7d4-757"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af7d4-758">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af7d4-758">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af7d4-759">**\_КАЧЕМЕМОРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="af7d4-759">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dt>

[<span data-ttu-id="af7d4-760">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="af7d4-760">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

