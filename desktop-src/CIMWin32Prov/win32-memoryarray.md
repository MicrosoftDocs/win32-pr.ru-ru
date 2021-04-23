---
description: '\_Класс WMI меморяррай для Win32 представляет свойства массива памяти компьютерной системы и сопоставленных адресов.'
ms.assetid: 56ff6960-cde3-4e34-b4df-d2993bafaa62
ms.tgt_platform: multiple
title: Класс Win32_MemoryArray
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArray
- Win32_MemoryArray.Reset
- Win32_MemoryArray.SetPowerState
- Win32_MemoryArray.Access
- Win32_MemoryArray.AdditionalErrorData
- Win32_MemoryArray.Availability
- Win32_MemoryArray.BlockSize
- Win32_MemoryArray.Caption
- Win32_MemoryArray.ConfigManagerErrorCode
- Win32_MemoryArray.ConfigManagerUserConfig
- Win32_MemoryArray.CorrectableError
- Win32_MemoryArray.CreationClassName
- Win32_MemoryArray.Description
- Win32_MemoryArray.DeviceID
- Win32_MemoryArray.EndingAddress
- Win32_MemoryArray.ErrorAccess
- Win32_MemoryArray.ErrorAddress
- Win32_MemoryArray.ErrorCleared
- Win32_MemoryArray.ErrorData
- Win32_MemoryArray.ErrorDataOrder
- Win32_MemoryArray.ErrorDescription
- Win32_MemoryArray.ErrorGranularity
- Win32_MemoryArray.ErrorInfo
- Win32_MemoryArray.ErrorMethodology
- Win32_MemoryArray.ErrorResolution
- Win32_MemoryArray.ErrorTime
- Win32_MemoryArray.ErrorTransferSize
- Win32_MemoryArray.InstallDate
- Win32_MemoryArray.LastErrorCode
- Win32_MemoryArray.Name
- Win32_MemoryArray.NumberOfBlocks
- Win32_MemoryArray.OtherErrorDescription
- Win32_MemoryArray.PNPDeviceID
- Win32_MemoryArray.PowerManagementCapabilities
- Win32_MemoryArray.PowerManagementSupported
- Win32_MemoryArray.Purpose
- Win32_MemoryArray.StartingAddress
- Win32_MemoryArray.Status
- Win32_MemoryArray.StatusInfo
- Win32_MemoryArray.SystemCreationClassName
- Win32_MemoryArray.SystemLevelAddress
- Win32_MemoryArray.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c102d383502bec4808b26a87eb2f6d8445b6c2a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262753"
---
# <a name="win32_memoryarray-class"></a><span data-ttu-id="b1758-103">\_Класс Win32 меморяррай</span><span class="sxs-lookup"><span data-stu-id="b1758-103">Win32\_MemoryArray class</span></span>

<span data-ttu-id="b1758-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ меморяррай для Win32** представляет свойства массива памяти компьютерной системы и сопоставленных адресов.</span><span class="sxs-lookup"><span data-stu-id="b1758-104">The **Win32\_MemoryArray** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of the computer system memory array and mapped addresses.</span></span>

<span data-ttu-id="b1758-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b1758-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b1758-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b1758-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1758-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1758-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryArray : Win32_SMBIOSMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorGranularity;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="b1758-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b1758-108">Members</span></span>

<span data-ttu-id="b1758-109">Класс **Win32 \_ меморяррай** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b1758-109">The **Win32\_MemoryArray** class has these types of members:</span></span>

-   [<span data-ttu-id="b1758-110">Методы</span><span class="sxs-lookup"><span data-stu-id="b1758-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b1758-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1758-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b1758-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b1758-112">Methods</span></span>

<span data-ttu-id="b1758-113">Класс **Win32 \_ меморяррай** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b1758-113">The **Win32\_MemoryArray** class has these methods.</span></span>



| <span data-ttu-id="b1758-114">Метод</span><span class="sxs-lookup"><span data-stu-id="b1758-114">Method</span></span>            | <span data-ttu-id="b1758-115">Описание</span><span class="sxs-lookup"><span data-stu-id="b1758-115">Description</span></span>                                                                                                                                                                                                        |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1758-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="b1758-116">**Reset**</span></span>         | <span data-ttu-id="b1758-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="b1758-117">Not implemented.</span></span> <span data-ttu-id="b1758-118">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="b1758-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="b1758-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b1758-119">**SetPowerState**</span></span> | <span data-ttu-id="b1758-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="b1758-120">Not implemented.</span></span> <span data-ttu-id="b1758-121">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="b1758-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b1758-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1758-122">Properties</span></span>

<span data-ttu-id="b1758-123">Класс **Win32 \_ меморяррай** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b1758-123">The **Win32\_MemoryArray** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1758-124">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="b1758-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-127">Тип доступного доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="b1758-127">Type of media access available.</span></span>

<span data-ttu-id="b1758-128">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b1758-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="b1758-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="b1758-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-132">Возможность записи</span><span class="sxs-lookup"><span data-stu-id="b1758-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="b1758-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="b1758-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="b1758-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="b1758-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-135">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="b1758-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-136">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b1758-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b1758-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32 — сведения об ошибке в памяти \| поставщика синдром"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b1758-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1758-139">Массив дополнительных сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="b1758-139">Array of additional error information.</span></span> <span data-ttu-id="b1758-140">Примером является проверка ошибок и исправление (ECC) синдром или возвращение битов проверки, если используется циклическая проверка избыточности (CRC) на основе значения **еррормесодологи** .</span><span class="sxs-lookup"><span data-stu-id="b1758-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based **ErrorMethodology** value is used.</span></span> <span data-ttu-id="b1758-141">В последнем случае, если обнаружена Одноразрядная ошибка и известен алгоритм CRC, можно определить точный бит, в котором произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="b1758-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="b1758-142">Этот тип данных (ECC синдром, бит проверки, битные данные четности или другие сведения, предоставленные поставщиком) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="b1758-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="b1758-143">Это свойство используется только в том случае, если свойство **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="b1758-144">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-145">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b1758-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b1758-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-149">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-149">Availability and status of the device.</span></span>

<span data-ttu-id="b1758-150">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1758-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b1758-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b1758-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-154">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="b1758-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b1758-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b1758-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b1758-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b1758-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1758-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b1758-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b1758-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b1758-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b1758-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b1758-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b1758-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b1758-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1758-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b1758-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b1758-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b1758-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b1758-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b1758-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b1758-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b1758-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-165">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b1758-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b1758-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b1758-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-167">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b1758-167">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b1758-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b1758-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-169">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b1758-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b1758-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b1758-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b1758-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b1758-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-172">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b1758-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b1758-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b1758-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-174">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b1758-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b1758-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b1758-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-176">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b1758-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b1758-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b1758-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-178">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b1758-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b1758-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b1758-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-180">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b1758-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="b1758-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-182">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1758-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-184">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="b1758-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-185">Размер в байтах блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="b1758-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="b1758-186">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="b1758-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="b1758-187">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b1758-188">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1758-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-189">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b1758-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-192">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b1758-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-193">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="b1758-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="b1758-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-195">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b1758-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-196">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1758-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-198">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1758-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-199">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b1758-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b1758-200">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b1758-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b1758-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b1758-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="b1758-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-203">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b1758-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b1758-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b1758-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b1758-205">(1)</span><span class="sxs-lookup"><span data-stu-id="b1758-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-206">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b1758-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1758-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b1758-208">(2)</span><span class="sxs-lookup"><span data-stu-id="b1758-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b1758-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b1758-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b1758-210">(3)</span><span class="sxs-lookup"><span data-stu-id="b1758-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-211">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1758-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1758-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b1758-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b1758-213">(4)</span><span class="sxs-lookup"><span data-stu-id="b1758-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-214">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b1758-214">Device is not working properly.</span></span> <span data-ttu-id="b1758-215">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b1758-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b1758-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b1758-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b1758-217">(5)</span><span class="sxs-lookup"><span data-stu-id="b1758-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-218">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b1758-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b1758-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b1758-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b1758-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="b1758-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-221">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b1758-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b1758-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b1758-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b1758-223">(7)</span><span class="sxs-lookup"><span data-stu-id="b1758-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b1758-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b1758-225">(8)</span><span class="sxs-lookup"><span data-stu-id="b1758-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-226">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b1758-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b1758-228">(9)</span><span class="sxs-lookup"><span data-stu-id="b1758-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-229">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b1758-229">Device is not working properly.</span></span> <span data-ttu-id="b1758-230">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b1758-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b1758-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b1758-232">(10)</span><span class="sxs-lookup"><span data-stu-id="b1758-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-233">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b1758-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b1758-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b1758-235">(11)</span><span class="sxs-lookup"><span data-stu-id="b1758-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-236">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b1758-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b1758-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b1758-238">(12)</span><span class="sxs-lookup"><span data-stu-id="b1758-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-239">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b1758-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b1758-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b1758-241">(13)</span><span class="sxs-lookup"><span data-stu-id="b1758-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-242">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b1758-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b1758-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b1758-244">(14)</span><span class="sxs-lookup"><span data-stu-id="b1758-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-245">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b1758-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b1758-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b1758-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b1758-247">(15)</span><span class="sxs-lookup"><span data-stu-id="b1758-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-248">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b1758-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b1758-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b1758-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b1758-250">(16)</span><span class="sxs-lookup"><span data-stu-id="b1758-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-251">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b1758-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b1758-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b1758-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b1758-253">(17)</span><span class="sxs-lookup"><span data-stu-id="b1758-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-254">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b1758-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1758-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b1758-256">(18)</span><span class="sxs-lookup"><span data-stu-id="b1758-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-257">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b1758-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b1758-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b1758-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b1758-259">(19)</span><span class="sxs-lookup"><span data-stu-id="b1758-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b1758-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b1758-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b1758-261">(20)</span><span class="sxs-lookup"><span data-stu-id="b1758-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-262">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b1758-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b1758-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b1758-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b1758-264">(21)</span><span class="sxs-lookup"><span data-stu-id="b1758-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-265">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b1758-265">System failure.</span></span> <span data-ttu-id="b1758-266">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b1758-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b1758-267">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b1758-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b1758-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b1758-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b1758-269">(22)</span><span class="sxs-lookup"><span data-stu-id="b1758-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-270">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b1758-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b1758-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b1758-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b1758-272">(23)</span><span class="sxs-lookup"><span data-stu-id="b1758-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-273">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b1758-273">System failure.</span></span> <span data-ttu-id="b1758-274">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b1758-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b1758-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b1758-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b1758-276">(24)</span><span class="sxs-lookup"><span data-stu-id="b1758-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-277">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b1758-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1758-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b1758-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1758-279">(25)</span><span class="sxs-lookup"><span data-stu-id="b1758-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-280">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b1758-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b1758-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b1758-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b1758-282">(26)</span><span class="sxs-lookup"><span data-stu-id="b1758-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-283">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b1758-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b1758-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b1758-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b1758-285">(27)</span><span class="sxs-lookup"><span data-stu-id="b1758-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-286">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b1758-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b1758-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b1758-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b1758-288">(28)</span><span class="sxs-lookup"><span data-stu-id="b1758-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-289">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b1758-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b1758-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b1758-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b1758-291">(29)</span><span class="sxs-lookup"><span data-stu-id="b1758-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-292">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b1758-292">Device is disabled.</span></span> <span data-ttu-id="b1758-293">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b1758-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b1758-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b1758-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b1758-295">(30)</span><span class="sxs-lookup"><span data-stu-id="b1758-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-296">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b1758-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b1758-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b1758-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b1758-298">1-31</span><span class="sxs-lookup"><span data-stu-id="b1758-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-299">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b1758-299">Device is not working properly.</span></span> <span data-ttu-id="b1758-300">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b1758-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-301">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b1758-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-302">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b1758-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-304">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1758-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-305">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b1758-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b1758-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-307">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="b1758-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b1758-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-310">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный тип ошибки сведений об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="b1758-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-311">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="b1758-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="b1758-312">Это свойство не используется, если значение **errorInfo** равно 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="b1758-313">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b1758-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-317">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1758-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1758-318">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b1758-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="b1758-319">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b1758-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="b1758-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-321">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b1758-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-324">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b1758-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-325">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b1758-325">Description of the object.</span></span>

<span data-ttu-id="b1758-326">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1758-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-330">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b1758-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-331">Уникальный идентификатор массива памяти.</span><span class="sxs-lookup"><span data-stu-id="b1758-331">Unique identifier of the memory array.</span></span>

<span data-ttu-id="b1758-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1758-333">Пример: "массив памяти 1"</span><span class="sxs-lookup"><span data-stu-id="b1758-333">Example: "Memory Array 1"</span></span>

</dd> <dt>

<span data-ttu-id="b1758-334">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="b1758-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-335">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1758-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 19 \| памяти, сопоставленные адреса \| конечного адреса")</span><span class="sxs-lookup"><span data-stu-id="b1758-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-338">Конечный адрес, на который ссылается приложение или операционная система.</span><span class="sxs-lookup"><span data-stu-id="b1758-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="b1758-339">Этот адрес памяти сопоставляется контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="b1758-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="b1758-340">Это значение берется из структуры **сопоставленного адреса массива памяти** в сведениях о версии SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1758-340">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="b1758-341">Для SMBIOS версии 2,1 по 2,6 значение берется из конечного элемента **адреса** .</span><span class="sxs-lookup"><span data-stu-id="b1758-341">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Ending Address** member.</span></span> <span data-ttu-id="b1758-342">Для SMBIOS версии 2.7 + значение берется из элемента **расширенного конечного адреса** .</span><span class="sxs-lookup"><span data-stu-id="b1758-342">For SMBIOS version 2.7+ the value comes from the **Extended Ending Address** member.</span></span>

<span data-ttu-id="b1758-343">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-343">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b1758-344">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1758-344">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-345">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="b1758-345">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-346">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-346">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-348">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядная ошибка со сведениями об ошибке в памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="b1758-348">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-349">Тип операции доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="b1758-349">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="b1758-350">Это свойство допустимо, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-350">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b1758-351">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-351">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1758-352">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-352">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-353">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-353">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="b1758-354">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="b1758-354">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="b1758-355">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="b1758-355">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="b1758-356">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="b1758-356">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-357">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="b1758-357">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-358">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1758-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-360">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный адрес ошибки в информации об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="b1758-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-361">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="b1758-361">Address of the last memory error.</span></span> <span data-ttu-id="b1758-362">Это свойство используется, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-362">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b1758-363">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-363">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b1758-364">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1758-364">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-365">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b1758-365">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-366">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b1758-366">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-368">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b1758-368">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="b1758-369">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-369">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-370">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="b1758-370">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-371">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b1758-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b1758-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-373">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b1758-373">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b1758-374">Массив данных, полученных из последнего доступа к памяти с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="b1758-374">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="b1758-375">Данные занимают первые *n* октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="b1758-375">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="b1758-376">Если **еррортрансферсизе** имеет значение 0 (ноль), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="b1758-376">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="b1758-377">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-377">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-378">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="b1758-378">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-379">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-379">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-381">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b1758-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-382">Упорядочивание данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="b1758-382">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="b1758-383">Это свойство используется, только если **еррортрансферсизе** имеет значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="b1758-383">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="b1758-384">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-384">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-385">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b1758-385">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="b1758-386">**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-386">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="b1758-387">**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-387">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-388">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b1758-388">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-389">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-391">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="b1758-391">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="b1758-392">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-393">**ерроргрануларити**</span><span class="sxs-lookup"><span data-stu-id="b1758-393">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-394">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-396">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 — \| Детализация ошибок")</span><span class="sxs-lookup"><span data-stu-id="b1758-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-397">Уровень, на котором может быть разрешена ошибка.</span><span class="sxs-lookup"><span data-stu-id="b1758-397">Level where the error can be resolved.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="b1758-398">**1** (другое)</span><span class="sxs-lookup"><span data-stu-id="b1758-398">**1** (Other)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="b1758-399">**2** (неизвестно)</span><span class="sxs-lookup"><span data-stu-id="b1758-399">**2** (Unknown)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="b1758-400">**3** (уровень устройства)</span><span class="sxs-lookup"><span data-stu-id="b1758-400">**3** (Device level)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="b1758-401">**4** (уровень секционирования памяти)</span><span class="sxs-lookup"><span data-stu-id="b1758-401">**4** (Memory partition level)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-402">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b1758-402">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-403">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-405">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**Осереррордескриптион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный тип ошибки сведений об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="b1758-405">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-406">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="b1758-406">Type of error that occurred most recently.</span></span> <span data-ttu-id="b1758-407">Значения 12-14, которые указывают, является ли ошибка исправимой, не используются с этим свойством, но эти сведения находятся в свойстве **корректаблиррор** .</span><span class="sxs-lookup"><span data-stu-id="b1758-407">The values 12-14, which indicate whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="b1758-408">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-408">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1758-409">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-410">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1758-411">**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="b1758-411">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="b1758-412">**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="b1758-412">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="b1758-413">**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="b1758-413">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="b1758-414">**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="b1758-414">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="b1758-415">**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="b1758-415">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="b1758-416">**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="b1758-416">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="b1758-417">**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="b1758-417">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="b1758-418">**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="b1758-418">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="b1758-419">**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="b1758-419">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="b1758-420">**Исправленная Одноразрядная ошибка** (12)</span><span class="sxs-lookup"><span data-stu-id="b1758-420">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="b1758-421">**Исправленная ошибка** (13)</span><span class="sxs-lookup"><span data-stu-id="b1758-421">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="b1758-422">**Неисправимая ошибка** (14)</span><span class="sxs-lookup"><span data-stu-id="b1758-422">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-423">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="b1758-423">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-426">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 16. \| \| исправление ошибки памяти массива физической памяти")</span><span class="sxs-lookup"><span data-stu-id="b1758-426">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-427">Типы проверки ошибок, используемые оборудованием памяти.</span><span class="sxs-lookup"><span data-stu-id="b1758-427">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="b1758-428">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-428">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span> <span data-ttu-id="b1758-429">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="b1758-429">The values are:</span></span>

<dl> <dd><span data-ttu-id="b1758-430">Иной</span><span class="sxs-lookup"><span data-stu-id="b1758-430">"Other"</span></span></dd> <dd><span data-ttu-id="b1758-431">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="b1758-431">"Unknown"</span></span></dd> <dd><span data-ttu-id="b1758-432">"None"</span><span class="sxs-lookup"><span data-stu-id="b1758-432">"None"</span></span></dd> <dd><span data-ttu-id="b1758-433">Суммы</span><span class="sxs-lookup"><span data-stu-id="b1758-433">"Parity"</span></span></dd> <dd><span data-ttu-id="b1758-434">"Одноразрядный код коррекции ошибок"</span><span class="sxs-lookup"><span data-stu-id="b1758-434">"Single-bit ECC"</span></span></dd> <dd><span data-ttu-id="b1758-435">"Многоразрядный ECC"</span><span class="sxs-lookup"><span data-stu-id="b1758-435">"Multi-bit ECC"</span></span></dd> <dd><span data-ttu-id="b1758-436">СУММЫ</span><span class="sxs-lookup"><span data-stu-id="b1758-436">"CRC"</span></span></dd> </dl>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1758-437">**Другое** ("другое")</span><span class="sxs-lookup"><span data-stu-id="b1758-437">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-438">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b1758-438">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b1758-439">**Нет** ("нет")</span><span class="sxs-lookup"><span data-stu-id="b1758-439">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="b1758-440">**Четность** ("четность")</span><span class="sxs-lookup"><span data-stu-id="b1758-440">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="b1758-441">**Одноразрядный ECC** (одноразрядный ECC)</span><span class="sxs-lookup"><span data-stu-id="b1758-441">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="b1758-442">**Многоразрядный ECC** (Многоразрядный ECC)</span><span class="sxs-lookup"><span data-stu-id="b1758-442">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="b1758-443">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="b1758-443">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-444">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="b1758-444">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-445">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1758-445">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-447">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядная ошибка при \| устранении ошибок в памяти"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b1758-447">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-448">Объем данных, фактически определенный для возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="b1758-448">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="b1758-449">Это свойство не используется, если свойство **errorInfo** имеет значение 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-449">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="b1758-450">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-450">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b1758-451">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1758-451">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-452">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="b1758-452">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-453">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1758-453">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-455">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="b1758-455">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-456">Время, когда произошла последняя ошибка памяти.</span><span class="sxs-lookup"><span data-stu-id="b1758-456">Time that the last memory error occurred.</span></span> <span data-ttu-id="b1758-457">Это свойство допустимо, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-457">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b1758-458">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-458">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-459">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="b1758-459">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-460">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1758-460">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-461">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-462">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS")</span><span class="sxs-lookup"><span data-stu-id="b1758-462">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-463">Размер данных (содержащих последнюю ошибку), которые передаются.</span><span class="sxs-lookup"><span data-stu-id="b1758-463">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="b1758-464">Если ошибка отсутствует, это свойство имеет значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="b1758-464">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="b1758-465">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-465">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-466">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1758-466">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-467">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1758-467">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-469">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b1758-469">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-470">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b1758-470">Date and time the object was installed.</span></span> <span data-ttu-id="b1758-471">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b1758-471">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b1758-472">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-472">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-473">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b1758-473">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-474">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b1758-474">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-475">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-476">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b1758-476">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b1758-477">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-478">**Name**</span><span class="sxs-lookup"><span data-stu-id="b1758-478">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-479">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-479">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-481">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b1758-481">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-482">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b1758-482">Label by which the object is known.</span></span> <span data-ttu-id="b1758-483">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="b1758-483">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="b1758-484">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-484">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-485">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="b1758-485">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-486">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1758-486">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-488">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="b1758-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-489">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="b1758-489">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="b1758-490">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="b1758-490">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="b1758-491">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="b1758-491">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="b1758-492">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-492">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="b1758-493">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1758-493">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-494">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="b1758-494">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-495">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-495">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-496">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-496">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-497">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**ErrorInfo**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="b1758-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-498">Дополнительные сведения о том, что свойство **errorInfo** имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="b1758-498">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="b1758-499">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-499">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-500">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b1758-500">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-501">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-502">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-503">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b1758-503">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-504">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-504">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="b1758-505">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-505">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b1758-506">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b1758-506">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b1758-507">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b1758-507">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-508">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b1758-508">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b1758-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-509">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-510">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b1758-510">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b1758-511">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-511">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b1758-512"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b1758-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-513"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1758-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-514"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1758-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b1758-515"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-516">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b1758-516">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b1758-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b1758-517"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-518">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b1758-518">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b1758-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b1758-519"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-520">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b1758-520">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b1758-521">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b1758-521">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b1758-522">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b1758-522">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b1758-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b1758-523"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-524">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b1758-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b1758-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b1758-525"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b1758-526">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="b1758-526">Timed Power-On Supported</span></span>

<span data-ttu-id="b1758-527">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b1758-527">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-528">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b1758-528">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-529">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b1758-529">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-531">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b1758-531">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="b1758-532">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="b1758-532">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="b1758-533">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-533">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-534">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="b1758-534">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-536">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b1758-537">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="b1758-537">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="b1758-538">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-538">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-539">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="b1758-539">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-540">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b1758-540">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-541">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-542">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 19 \| памяти, сопоставленные адреса \| начальный адрес")</span><span class="sxs-lookup"><span data-stu-id="b1758-542">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-543">Начальный адрес, на который ссылается приложение или операционная система.</span><span class="sxs-lookup"><span data-stu-id="b1758-543">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="b1758-544">Этот адрес памяти сопоставляется контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="b1758-544">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="b1758-545">Это значение берется из структуры **сопоставленного адреса массива памяти** в сведениях о версии SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="b1758-545">This value comes from the **Memory Array Mapped Address** structure in the SMBIOS version information.</span></span> <span data-ttu-id="b1758-546">Для SMBIOS версии 2,1 по 2,6 значение берется из элемента **начальный адрес** .</span><span class="sxs-lookup"><span data-stu-id="b1758-546">For SMBIOS versions 2.1 thru 2.6 the value comes from the **Starting Address** member.</span></span> <span data-ttu-id="b1758-547">Для SMBIOS версии 2.7 + значение берется из **расширенного элемента начального адреса** .</span><span class="sxs-lookup"><span data-stu-id="b1758-547">For SMBIOS version 2.7+ the value comes from the **Extended Starting Address** member.</span></span>

<span data-ttu-id="b1758-548">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-548">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="b1758-549">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b1758-549">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-550">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b1758-550">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-551">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-552">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-553">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b1758-553">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-554">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b1758-554">Current status of the object.</span></span> <span data-ttu-id="b1758-555">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="b1758-555">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b1758-556">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="b1758-556">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b1758-557">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="b1758-557">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b1758-558">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="b1758-558">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b1758-559">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="b1758-559">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b1758-560">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-560">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b1758-561">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b1758-561">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1758-562">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b1758-562">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1758-563">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b1758-563">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1758-564">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b1758-564">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-565">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b1758-565">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1758-566">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b1758-566">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1758-567">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b1758-567">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1758-568">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b1758-568">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1758-569">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b1758-569">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1758-570">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b1758-570">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1758-571">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b1758-571">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1758-572">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b1758-572">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1758-573">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b1758-573">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-574">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b1758-574">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-575">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b1758-575">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-576">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-576">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-577">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b1758-577">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-578">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b1758-578">State of the logical device.</span></span> <span data-ttu-id="b1758-579">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b1758-579">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b1758-580">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-580">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b1758-581">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b1758-581">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1758-582">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b1758-582">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b1758-583">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b1758-583">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b1758-584">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b1758-584">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b1758-585">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b1758-585">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b1758-586">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b1758-586">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-587">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-587">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-588">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-589">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1758-589">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1758-590">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="b1758-590">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="b1758-591">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-591">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-592">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="b1758-592">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-593">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b1758-593">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-594">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-594">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-595">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный адрес ошибки в информации об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="b1758-595">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="b1758-596">Если **значение — true**, сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня.</span><span class="sxs-lookup"><span data-stu-id="b1758-596">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="b1758-597">Если **значение равно false**, это физический адрес.</span><span class="sxs-lookup"><span data-stu-id="b1758-597">If **False**, it is a physical address.</span></span> <span data-ttu-id="b1758-598">Это свойство используется, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="b1758-598">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="b1758-599">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-599">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1758-600">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b1758-600">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1758-601">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b1758-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1758-602">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b1758-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1758-603">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b1758-603">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b1758-604">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b1758-604">Name of the scoping system.</span></span>

<span data-ttu-id="b1758-605">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b1758-605">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1758-606">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1758-606">Remarks</span></span>

<span data-ttu-id="b1758-607">Класс **Win32 \_ меморяррай** является производным от [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="b1758-607">The **Win32\_MemoryArray** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1758-608">Требования</span><span class="sxs-lookup"><span data-stu-id="b1758-608">Requirements</span></span>



| <span data-ttu-id="b1758-609">Требование</span><span class="sxs-lookup"><span data-stu-id="b1758-609">Requirement</span></span> | <span data-ttu-id="b1758-610">Значение</span><span class="sxs-lookup"><span data-stu-id="b1758-610">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1758-611">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1758-611">Minimum supported client</span></span><br/> | <span data-ttu-id="b1758-612">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1758-612">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1758-613">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1758-613">Minimum supported server</span></span><br/> | <span data-ttu-id="b1758-614">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1758-614">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1758-615">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b1758-615">Namespace</span></span><br/>                | <span data-ttu-id="b1758-616">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b1758-616">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1758-617">MOF</span><span class="sxs-lookup"><span data-stu-id="b1758-617">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1758-618"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1758-618"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1758-619">DLL</span><span class="sxs-lookup"><span data-stu-id="b1758-619">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1758-620"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1758-620"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1758-621">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1758-621">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1758-622">**\_Смбиосмемори Win32**</span><span class="sxs-lookup"><span data-stu-id="b1758-622">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="b1758-623">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="b1758-623">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

