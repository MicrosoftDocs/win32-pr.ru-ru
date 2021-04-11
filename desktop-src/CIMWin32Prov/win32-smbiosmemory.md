---
description: '\_Абстрактный класс WMI Смбиосмемори Win32 представляет свойства памяти системы компьютера, как показано в интерфейсе System Management BIOS (SMBIOS).'
ms.assetid: 2f609fc6-f0f5-45a5-9f9a-3873da034d49
ms.tgt_platform: multiple
title: Класс Win32_SMBIOSMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SMBIOSMemory
- Win32_SMBIOSMemory.Reset
- Win32_SMBIOSMemory.SetPowerState
- Win32_SMBIOSMemory.Access
- Win32_SMBIOSMemory.AdditionalErrorData
- Win32_SMBIOSMemory.Availability
- Win32_SMBIOSMemory.BlockSize
- Win32_SMBIOSMemory.Caption
- Win32_SMBIOSMemory.ConfigManagerErrorCode
- Win32_SMBIOSMemory.ConfigManagerUserConfig
- Win32_SMBIOSMemory.CorrectableError
- Win32_SMBIOSMemory.CreationClassName
- Win32_SMBIOSMemory.Description
- Win32_SMBIOSMemory.DeviceID
- Win32_SMBIOSMemory.EndingAddress
- Win32_SMBIOSMemory.ErrorAccess
- Win32_SMBIOSMemory.ErrorAddress
- Win32_SMBIOSMemory.ErrorCleared
- Win32_SMBIOSMemory.ErrorData
- Win32_SMBIOSMemory.ErrorDataOrder
- Win32_SMBIOSMemory.ErrorDescription
- Win32_SMBIOSMemory.ErrorInfo
- Win32_SMBIOSMemory.ErrorMethodology
- Win32_SMBIOSMemory.ErrorResolution
- Win32_SMBIOSMemory.ErrorTime
- Win32_SMBIOSMemory.ErrorTransferSize
- Win32_SMBIOSMemory.InstallDate
- Win32_SMBIOSMemory.LastErrorCode
- Win32_SMBIOSMemory.Name
- Win32_SMBIOSMemory.NumberOfBlocks
- Win32_SMBIOSMemory.OtherErrorDescription
- Win32_SMBIOSMemory.PNPDeviceID
- Win32_SMBIOSMemory.PowerManagementCapabilities
- Win32_SMBIOSMemory.PowerManagementSupported
- Win32_SMBIOSMemory.Purpose
- Win32_SMBIOSMemory.StartingAddress
- Win32_SMBIOSMemory.Status
- Win32_SMBIOSMemory.StatusInfo
- Win32_SMBIOSMemory.SystemCreationClassName
- Win32_SMBIOSMemory.SystemLevelAddress
- Win32_SMBIOSMemory.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4dc7a42732dfb00d965f79045254878f690309fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142457"
---
# <a name="win32_smbiosmemory-class"></a><span data-ttu-id="91904-103">\_Класс Win32 смбиосмемори</span><span class="sxs-lookup"><span data-stu-id="91904-103">Win32\_SMBIOSMemory class</span></span>

<span data-ttu-id="91904-104">Абстрактный [класс WMI](../wmisdk/retrieving-a-class.md) **\_ смбиосмемори Win32** представляет свойства памяти системы компьютера, как показано в интерфейсе System Management BIOS (SMBIOS).</span><span class="sxs-lookup"><span data-stu-id="91904-104">The **Win32\_SMBIOSMemory** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a computer system memory as seen through the system management BIOS (SMBIOS) interface.</span></span> <span data-ttu-id="91904-105">Интерфейс SMBIOS не различает временные, временные и Flash-воспоминания.</span><span class="sxs-lookup"><span data-stu-id="91904-105">The SMBIOS interface does not distinguish between nonvolatile, volatile, and flash memories.</span></span> <span data-ttu-id="91904-106">Класс [**\_ памяти CIM**](cim-memory.md) является родительским классом для всех типов памяти.</span><span class="sxs-lookup"><span data-stu-id="91904-106">The [**CIM\_Memory**](cim-memory.md) class is the parent class of all types of memory.</span></span>

<span data-ttu-id="91904-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="91904-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="91904-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="91904-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91904-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91904-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FECB095B-F0FA-11d2-8617-0000F8102E5F}"), AMENDMENT]
class Win32_SMBIOSMemory : CIM_StorageExtent
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
  uint16e  StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="91904-110">Члены</span><span class="sxs-lookup"><span data-stu-id="91904-110">Members</span></span>

<span data-ttu-id="91904-111">Класс **Win32 \_ смбиосмемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="91904-111">The **Win32\_SMBIOSMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="91904-112">Методы</span><span class="sxs-lookup"><span data-stu-id="91904-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="91904-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="91904-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="91904-114">Методы</span><span class="sxs-lookup"><span data-stu-id="91904-114">Methods</span></span>

<span data-ttu-id="91904-115">Класс **Win32 \_ смбиосмемори** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="91904-115">The **Win32\_SMBIOSMemory** class has these methods.</span></span>



| <span data-ttu-id="91904-116">Метод</span><span class="sxs-lookup"><span data-stu-id="91904-116">Method</span></span>            | <span data-ttu-id="91904-117">Описание</span><span class="sxs-lookup"><span data-stu-id="91904-117">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91904-118">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="91904-118">**Reset**</span></span>         | <span data-ttu-id="91904-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="91904-119">Not implemented.</span></span> <span data-ttu-id="91904-120">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-120">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/>                 |
| <span data-ttu-id="91904-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="91904-121">**SetPowerState**</span></span> | <span data-ttu-id="91904-122">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="91904-122">Not implemented.</span></span> <span data-ttu-id="91904-123">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-123">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_StorageExtent**](cim-storageextent.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="91904-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="91904-124">Properties</span></span>

<span data-ttu-id="91904-125">Класс **Win32 \_ смбиосмемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="91904-125">The **Win32\_SMBIOSMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91904-126">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="91904-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91904-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91904-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-129">Тип доступа.</span><span class="sxs-lookup"><span data-stu-id="91904-129">Type of access.</span></span>

<span data-ttu-id="91904-130">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="91904-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="91904-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-132"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="91904-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-133"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="91904-134">Возможность записи</span><span class="sxs-lookup"><span data-stu-id="91904-134">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="91904-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="91904-135"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="91904-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="91904-136"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-137">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="91904-137">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-138">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="91904-138">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="91904-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-140">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32 — сведения об ошибке в памяти \| поставщика синдром"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="91904-140">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="91904-141">Массив октетов, содержащих дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="91904-141">Array of octets that hold additional error information.</span></span> <span data-ttu-id="91904-142">Примером является проверка ошибок и исправление ошибки (ECC) синдром или возвращение битов проверки, если используется методология ошибок на основе CRC.</span><span class="sxs-lookup"><span data-stu-id="91904-142">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="91904-143">В последнем случае, если распознана одна разрядная ошибка и известен алгоритм циклической проверки избыточности (CRC), можно определить точный бит, который не удалось выполнить.</span><span class="sxs-lookup"><span data-stu-id="91904-143">In the latter case, if a single bit error is recognized and the cyclical redundancy check (CRC) algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="91904-144">Этот тип данных (ECC синдром, бит проверки битов или бит четности или другая предоставленная информация поставщика) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="91904-144">This type of data (ECC Syndrome, Check Bit or Parity Bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="91904-145">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-145">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="91904-146">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="91904-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91904-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91904-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-149">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="91904-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="91904-150">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-150">Availability and status of the device.</span></span>

<span data-ttu-id="91904-151">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91904-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="91904-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="91904-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91904-155">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="91904-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="91904-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="91904-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="91904-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="91904-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="91904-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="91904-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="91904-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="91904-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="91904-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="91904-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="91904-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="91904-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91904-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="91904-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="91904-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="91904-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="91904-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="91904-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="91904-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="91904-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="91904-166">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="91904-166">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="91904-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="91904-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="91904-168">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="91904-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="91904-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="91904-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="91904-170">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="91904-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="91904-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="91904-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="91904-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="91904-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="91904-173">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="91904-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="91904-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="91904-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="91904-175">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="91904-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="91904-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="91904-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="91904-177">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="91904-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="91904-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="91904-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="91904-179">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="91904-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="91904-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="91904-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="91904-181">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="91904-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="91904-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-183">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91904-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91904-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-185">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](../wmisdk/standard-qualifiers.md) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="91904-185">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="91904-186">Размер в байтах блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="91904-186">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="91904-187">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="91904-187">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="91904-188">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91904-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="91904-189">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-190">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="91904-190">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-193">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="91904-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="91904-194">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="91904-194">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="91904-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91904-195">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-196">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="91904-196">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91904-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91904-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-199">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91904-199">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91904-200">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="91904-200">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="91904-201">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-201">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="91904-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="91904-202"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="91904-203"> (0)</span><span class="sxs-lookup"><span data-stu-id="91904-203">(0)</span></span>


</dt> <dd>

<span data-ttu-id="91904-204">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="91904-204">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="91904-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="91904-205"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="91904-206">(1)</span><span class="sxs-lookup"><span data-stu-id="91904-206">(1)</span></span>


</dt> <dd>

<span data-ttu-id="91904-207">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="91904-207">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91904-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-208"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="91904-209">(2)</span><span class="sxs-lookup"><span data-stu-id="91904-209">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="91904-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="91904-210"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="91904-211">(3)</span><span class="sxs-lookup"><span data-stu-id="91904-211">(3)</span></span>


</dt> <dd>

<span data-ttu-id="91904-212">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91904-212">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="91904-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="91904-213"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="91904-214">(4)</span><span class="sxs-lookup"><span data-stu-id="91904-214">(4)</span></span>


</dt> <dd>

<span data-ttu-id="91904-215">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="91904-215">Device is not working properly.</span></span> <span data-ttu-id="91904-216">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="91904-216">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="91904-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="91904-217"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="91904-218">(5)</span><span class="sxs-lookup"><span data-stu-id="91904-218">(5)</span></span>


</dt> <dd>

<span data-ttu-id="91904-219">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="91904-219">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="91904-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="91904-220"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="91904-221"> (6)</span><span class="sxs-lookup"><span data-stu-id="91904-221">(6)</span></span>


</dt> <dd>

<span data-ttu-id="91904-222">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="91904-222">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="91904-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="91904-223"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="91904-224">(7)</span><span class="sxs-lookup"><span data-stu-id="91904-224">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="91904-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-225"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="91904-226">(8)</span><span class="sxs-lookup"><span data-stu-id="91904-226">(8)</span></span>


</dt> <dd>

<span data-ttu-id="91904-227">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-227">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="91904-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-228"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="91904-229">(9)</span><span class="sxs-lookup"><span data-stu-id="91904-229">(9)</span></span>


</dt> <dd>

<span data-ttu-id="91904-230">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="91904-230">Device is not working properly.</span></span> <span data-ttu-id="91904-231">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-231">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="91904-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="91904-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="91904-233">(10)</span><span class="sxs-lookup"><span data-stu-id="91904-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="91904-234">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="91904-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="91904-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="91904-236">(11)</span><span class="sxs-lookup"><span data-stu-id="91904-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="91904-237">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="91904-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="91904-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="91904-239">(12)</span><span class="sxs-lookup"><span data-stu-id="91904-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="91904-240">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="91904-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="91904-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="91904-242">(13)</span><span class="sxs-lookup"><span data-stu-id="91904-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="91904-243">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="91904-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="91904-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="91904-245">(14)</span><span class="sxs-lookup"><span data-stu-id="91904-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="91904-246">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="91904-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="91904-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="91904-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="91904-248">(15)</span><span class="sxs-lookup"><span data-stu-id="91904-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="91904-249">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="91904-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="91904-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="91904-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="91904-251">(16)</span><span class="sxs-lookup"><span data-stu-id="91904-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="91904-252">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="91904-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="91904-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="91904-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="91904-254">(17)</span><span class="sxs-lookup"><span data-stu-id="91904-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="91904-255">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="91904-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91904-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="91904-257">(18)</span><span class="sxs-lookup"><span data-stu-id="91904-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="91904-258">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="91904-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="91904-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="91904-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="91904-260">(19)</span><span class="sxs-lookup"><span data-stu-id="91904-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="91904-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="91904-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="91904-262">(20)</span><span class="sxs-lookup"><span data-stu-id="91904-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="91904-263">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="91904-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="91904-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="91904-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="91904-265">(21)</span><span class="sxs-lookup"><span data-stu-id="91904-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="91904-266">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="91904-266">System failure.</span></span> <span data-ttu-id="91904-267">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="91904-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="91904-268">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="91904-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="91904-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="91904-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="91904-270">(22)</span><span class="sxs-lookup"><span data-stu-id="91904-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="91904-271">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="91904-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="91904-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="91904-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="91904-273">(23)</span><span class="sxs-lookup"><span data-stu-id="91904-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="91904-274">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="91904-274">System failure.</span></span> <span data-ttu-id="91904-275">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="91904-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="91904-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="91904-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="91904-277">(24)</span><span class="sxs-lookup"><span data-stu-id="91904-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="91904-278">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="91904-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="91904-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="91904-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="91904-280">(25)</span><span class="sxs-lookup"><span data-stu-id="91904-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="91904-281">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="91904-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="91904-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="91904-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="91904-283">(26)</span><span class="sxs-lookup"><span data-stu-id="91904-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="91904-284">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="91904-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="91904-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="91904-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="91904-286">(27)</span><span class="sxs-lookup"><span data-stu-id="91904-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="91904-287">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="91904-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="91904-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="91904-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="91904-289">(28)</span><span class="sxs-lookup"><span data-stu-id="91904-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="91904-290">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="91904-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="91904-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="91904-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="91904-292">(29)</span><span class="sxs-lookup"><span data-stu-id="91904-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="91904-293">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="91904-293">Device is disabled.</span></span> <span data-ttu-id="91904-294">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="91904-294">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="91904-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="91904-295"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="91904-296">(30)</span><span class="sxs-lookup"><span data-stu-id="91904-296">(30)</span></span>


</dt> <dd>

<span data-ttu-id="91904-297">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="91904-297">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="91904-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="91904-298"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="91904-299">1-31</span><span class="sxs-lookup"><span data-stu-id="91904-299">(31)</span></span>


</dt> <dd>

<span data-ttu-id="91904-300">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="91904-300">Device is not working properly.</span></span> <span data-ttu-id="91904-301">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="91904-301">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-302">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="91904-302">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-303">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="91904-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91904-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-305">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91904-305">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91904-306">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="91904-306">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="91904-307">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-308">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="91904-308">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-309">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="91904-309">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91904-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-311">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32-разрядный тип ошибки сведений об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="91904-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="91904-312">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="91904-312">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="91904-313">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-313">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="91904-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91904-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-317">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="91904-317">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="91904-318">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="91904-318">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="91904-319">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="91904-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="91904-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-321">**Описание**</span><span class="sxs-lookup"><span data-stu-id="91904-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-324">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="91904-324">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="91904-325">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="91904-325">Description of the object.</span></span>

<span data-ttu-id="91904-326">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91904-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="91904-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-330">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="91904-330">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="91904-331">Уникальный идентификатор логического устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-331">Unique identifier of the logical device.</span></span>

<span data-ttu-id="91904-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-333">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="91904-333">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-334">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91904-334">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91904-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-336">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 19 \| памяти, сопоставленные адреса \| конечного адреса")</span><span class="sxs-lookup"><span data-stu-id="91904-336">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="91904-337">Конечный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="91904-337">Ending address, referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="91904-338">Конечный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="91904-338">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="91904-339">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91904-339">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-340">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="91904-340">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-341">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91904-341">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91904-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-343">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32-разрядная ошибка со сведениями об ошибке в памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="91904-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="91904-344">Операция доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="91904-344">Memory access operation that caused the last error.</span></span> <span data-ttu-id="91904-345">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="91904-345">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="91904-346">Если значение **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-346">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91904-347">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-348">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-348">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="91904-349">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="91904-349">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="91904-350">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="91904-350">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="91904-351">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="91904-351">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-352">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="91904-352">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-353">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91904-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91904-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-355">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32-разрядный адрес ошибки в информации об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="91904-355">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="91904-356">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="91904-356">Address of the last memory error.</span></span> <span data-ttu-id="91904-357">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="91904-357">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="91904-358">Если значение **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-358">If **ErrorInfo** is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="91904-359">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91904-359">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-360">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="91904-360">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-361">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="91904-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91904-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-363">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="91904-363">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="91904-364">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-365">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="91904-365">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-366">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="91904-366">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="91904-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-368">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Max**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="91904-368">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**MAX**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="91904-369">Массив данных, захваченных во время последней ошибочной операции доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="91904-369">Array of data captured during the last erroneous memory access.</span></span> <span data-ttu-id="91904-370">Данные занимают первые *n* октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="91904-370">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="91904-371">Если **еррортрансферсизе** имеет значение 0 (ноль), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-371">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="91904-372">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="91904-372">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-373">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91904-373">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91904-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-375">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="91904-375">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="91904-376">Упорядочивание данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="91904-376">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="91904-377">Если **еррортрансферсизе** имеет значение 0 (ноль), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-377">If **ErrorTransferSize** is 0 (zero), then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-378">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="91904-378">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="91904-379">**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-379">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="91904-380">**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-380">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-381">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="91904-381">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-384">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="91904-384">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="91904-385">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-386">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="91904-386">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91904-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="91904-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-389">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ память CIM**](cim-memory.md)".**Осереррордескриптион**"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32-разрядный тип ошибки сведений об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="91904-389">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="91904-390">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="91904-390">Type of error that occurred most recently.</span></span> <span data-ttu-id="91904-391">Значения от 12 до 14 не используются.</span><span class="sxs-lookup"><span data-stu-id="91904-391">The values 12 through 14 are unused.</span></span> <span data-ttu-id="91904-392">Возможность исправления указывается в свойстве **корректаблиррор**.</span><span class="sxs-lookup"><span data-stu-id="91904-392">The ability to be corrected is indicated in the property **CorrectableError**.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91904-393">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-394">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="91904-395">**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="91904-395">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="91904-396">**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="91904-396">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="91904-397">**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="91904-397">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="91904-398">**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="91904-398">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="91904-399">**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="91904-399">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="91904-400">**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="91904-400">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="91904-401">**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="91904-401">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="91904-402">**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="91904-402">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="91904-403">**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="91904-403">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="91904-404">**Исправленная Одноразрядная ошибка** (12)</span><span class="sxs-lookup"><span data-stu-id="91904-404">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="91904-405">**Исправленная ошибка** (13)</span><span class="sxs-lookup"><span data-stu-id="91904-405">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="91904-406">**Неисправимая ошибка** (14)</span><span class="sxs-lookup"><span data-stu-id="91904-406">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-407">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="91904-407">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-408">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-410">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("еррормесодологи"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 16, \| \| исправление ошибки памяти массива физической памяти")</span><span class="sxs-lookup"><span data-stu-id="91904-410">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ErrorMethodology"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="91904-411">Сведения о алгоритмах четности и CRC, а также об ECC или других используемых механизмах.</span><span class="sxs-lookup"><span data-stu-id="91904-411">Details on the parity or CRC algorithms, ECC or other mechanisms used.</span></span>

<span data-ttu-id="91904-412">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-412">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91904-413">**Другое** ("другое")</span><span class="sxs-lookup"><span data-stu-id="91904-413">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-414">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="91904-414">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="91904-415">**Нет** ("нет")</span><span class="sxs-lookup"><span data-stu-id="91904-415">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="91904-416">**Четность** ("четность")</span><span class="sxs-lookup"><span data-stu-id="91904-416">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="91904-417">**Одноразрядный ECC** (одноразрядный ECC)</span><span class="sxs-lookup"><span data-stu-id="91904-417">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="91904-418">**Многоразрядный ECC** (Многоразрядный ECC)</span><span class="sxs-lookup"><span data-stu-id="91904-418">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="91904-419">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="91904-419">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-420">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="91904-420">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-421">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91904-421">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91904-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-423">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32-разрядная ошибка при \| устранении ошибок в памяти"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="91904-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="91904-424">Диапазон в байтах, до которого может быть разрешена Последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="91904-424">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="91904-425">Например, если адреса ошибок разрешаются в бит 11 (то есть на типичном уровне страницы), ошибки могут быть разрешены до 4 КБ, а значение этого свойства равно 4000.</span><span class="sxs-lookup"><span data-stu-id="91904-425">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="91904-426">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-426">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

<span data-ttu-id="91904-427">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91904-427">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-428">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="91904-428">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-429">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="91904-429">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91904-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-431">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="91904-431">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="91904-432">Время, когда произошла последняя ошибка памяти.</span><span class="sxs-lookup"><span data-stu-id="91904-432">Time that the last memory error occurred.</span></span> <span data-ttu-id="91904-433">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="91904-433">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="91904-434">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-434">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="91904-435">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="91904-435">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-436">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91904-436">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91904-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-438">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("BITS")</span><span class="sxs-lookup"><span data-stu-id="91904-438">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="91904-439">Размер передачи данных в битах, вызвавших последнюю ошибку — 0 (ноль) указывает на отсутствие ошибки.</span><span class="sxs-lookup"><span data-stu-id="91904-439">Size of the data transfer in bits that caused the last error—0 (zero) indicates no error.</span></span> <span data-ttu-id="91904-440">Если свойство **errorInfo** равно 3 (ОК), то этому свойству должно быть присвоено значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="91904-440">If the **ErrorInfo** property is equal to 3 (OK), then this property should be set to 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="91904-441">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="91904-441">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-442">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="91904-442">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91904-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-444">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="91904-444">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="91904-445">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="91904-445">Date and time the object was installed.</span></span> <span data-ttu-id="91904-446">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="91904-446">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="91904-447">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91904-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-448">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="91904-448">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-449">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="91904-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="91904-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-451">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="91904-451">Last error code reported by the logical device.</span></span>

<span data-ttu-id="91904-452">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-453">**Name**</span><span class="sxs-lookup"><span data-stu-id="91904-453">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-456">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="91904-456">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="91904-457">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="91904-457">Label by which the object is known.</span></span> <span data-ttu-id="91904-458">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="91904-458">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="91904-459">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91904-459">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-460">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="91904-460">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-461">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91904-461">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91904-462">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-462">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-463">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="91904-463">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="91904-464">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="91904-464">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="91904-465">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="91904-465">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="91904-466">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="91904-466">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="91904-467">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91904-467">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="91904-468">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-468">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-469">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="91904-469">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-470">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-470">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-471">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-471">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-472">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ память CIM**](cim-memory.md)".**ErrorInfo**"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="91904-472">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="91904-473">Произвольная строка, которая предоставляет дополнительные сведения, если свойство **ErrorType** имеет значение 1; в противном случае эта строка не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-473">Free-form string that provides more information if the **ErrorType** property is set to 1; otherwise, this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="91904-474">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="91904-474">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-477">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="91904-477">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="91904-478">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-478">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="91904-479">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="91904-479">Example: "\*PNP030b"</span></span>

<span data-ttu-id="91904-480">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-480">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-481">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="91904-481">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-482">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="91904-482">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="91904-483">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-484">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="91904-484">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="91904-485">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="91904-486"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="91904-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-487"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="91904-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-488"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="91904-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="91904-489"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="91904-490">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="91904-490">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="91904-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="91904-491"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="91904-492">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="91904-492">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="91904-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="91904-493"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="91904-494">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="91904-494">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="91904-495">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="91904-495">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="91904-496">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="91904-496">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="91904-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="91904-497"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="91904-498">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="91904-498">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="91904-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="91904-499"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="91904-500">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="91904-500">Timed Power-On Supported</span></span>

<span data-ttu-id="91904-501">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="91904-501">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-502">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="91904-502">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-503">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="91904-503">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91904-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-504">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-505">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="91904-505">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="91904-506">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="91904-506">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="91904-507">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-508">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="91904-508">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-509">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-509">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-510">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-510">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="91904-511">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="91904-511">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="91904-512">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-512">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-513">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="91904-513">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-514">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91904-514">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91904-515">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-516">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 19 \| памяти, сопоставленные адреса \| начальный адрес")</span><span class="sxs-lookup"><span data-stu-id="91904-516">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="91904-517">Начальный адрес, на который ссылается приложение или операционная система, который сопоставлен контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="91904-517">Beginning address that is referenced by an application or operating system, and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="91904-518">Начальный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="91904-518">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="91904-519">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91904-519">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-520">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="91904-520">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-521">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-522">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-523">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="91904-523">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="91904-524">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="91904-524">Current status of the object.</span></span> <span data-ttu-id="91904-525">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="91904-525">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="91904-526">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="91904-526">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="91904-527">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="91904-527">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="91904-528">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="91904-528">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="91904-529">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="91904-529">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="91904-530">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91904-530">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="91904-531">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="91904-531">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="91904-532">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="91904-532">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="91904-533">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="91904-533">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91904-534">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="91904-534">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-535">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="91904-535">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="91904-536">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="91904-536">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="91904-537">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="91904-537">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="91904-538">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="91904-538">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="91904-539">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="91904-539">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="91904-540">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="91904-540">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="91904-541">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="91904-541">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="91904-542">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="91904-542">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="91904-543">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="91904-543">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-544">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="91904-544">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-545">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="91904-545">Data type: **uint16e**</span></span>
</dt> <dt>

<span data-ttu-id="91904-546">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-546">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-547">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="91904-547">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="91904-548">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="91904-548">State of the logical device.</span></span> <span data-ttu-id="91904-549">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="91904-549">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="91904-550">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="91904-551">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="91904-551">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91904-552">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="91904-552">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="91904-553">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="91904-553">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="91904-554">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="91904-554">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="91904-555">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="91904-555">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="91904-556">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="91904-556">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-557">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-558">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-559">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="91904-559">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="91904-560">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="91904-560">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="91904-561">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-561">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="91904-562">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="91904-562">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-563">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="91904-563">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="91904-564">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-565">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 18 \| 32-разрядный адрес ошибки в информации об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="91904-565">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="91904-566">Если **значение — true**, сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня.</span><span class="sxs-lookup"><span data-stu-id="91904-566">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="91904-567">Если **значение равно false**, это физический адрес.</span><span class="sxs-lookup"><span data-stu-id="91904-567">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="91904-568">Если свойство **errorInfo** равно 3 (ОК), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="91904-568">If the **ErrorInfo** property is equal to 3 (OK), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="91904-569">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="91904-569">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91904-570">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91904-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91904-571">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91904-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91904-572">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="91904-572">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="91904-573">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="91904-573">Name of the scoping system.</span></span>

<span data-ttu-id="91904-574">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="91904-574">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91904-575">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91904-575">Remarks</span></span>

<span data-ttu-id="91904-576">Класс **Win32 \_ смбиосмемори** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="91904-576">The **Win32\_SMBIOSMemory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91904-577">Требования</span><span class="sxs-lookup"><span data-stu-id="91904-577">Requirements</span></span>



| <span data-ttu-id="91904-578">Требование</span><span class="sxs-lookup"><span data-stu-id="91904-578">Requirement</span></span> | <span data-ttu-id="91904-579">Значение</span><span class="sxs-lookup"><span data-stu-id="91904-579">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91904-580">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91904-580">Minimum supported client</span></span><br/> | <span data-ttu-id="91904-581">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91904-581">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91904-582">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91904-582">Minimum supported server</span></span><br/> | <span data-ttu-id="91904-583">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91904-583">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91904-584">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="91904-584">Namespace</span></span><br/>                | <span data-ttu-id="91904-585">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="91904-585">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91904-586">MOF</span><span class="sxs-lookup"><span data-stu-id="91904-586">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91904-587"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91904-587"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91904-588">DLL</span><span class="sxs-lookup"><span data-stu-id="91904-588">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91904-589"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91904-589"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91904-590">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91904-590">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91904-591">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="91904-591">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="91904-592">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="91904-592">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
