---
description: '\_Класс WMI меморидевице для Win32 представляет свойства устройства памяти компьютерной системы и связанных с ним сопоставленных адресов.'
ms.assetid: d609dca5-2f5f-4f23-8fcc-bcc197d6c24b
ms.tgt_platform: multiple
title: Класс Win32_MemoryDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDevice
- Win32_MemoryDevice.Reset
- Win32_MemoryDevice.SetPowerState
- Win32_MemoryDevice.Access
- Win32_MemoryDevice.AdditionalErrorData
- Win32_MemoryDevice.Availability
- Win32_MemoryDevice.BlockSize
- Win32_MemoryDevice.Caption
- Win32_MemoryDevice.ConfigManagerErrorCode
- Win32_MemoryDevice.ConfigManagerUserConfig
- Win32_MemoryDevice.CorrectableError
- Win32_MemoryDevice.CreationClassName
- Win32_MemoryDevice.Description
- Win32_MemoryDevice.DeviceID
- Win32_MemoryDevice.EndingAddress
- Win32_MemoryDevice.ErrorAccess
- Win32_MemoryDevice.ErrorAddress
- Win32_MemoryDevice.ErrorCleared
- Win32_MemoryDevice.ErrorData
- Win32_MemoryDevice.ErrorDataOrder
- Win32_MemoryDevice.ErrorDescription
- Win32_MemoryDevice.ErrorGranularity
- Win32_MemoryDevice.ErrorInfo
- Win32_MemoryDevice.ErrorMethodology
- Win32_MemoryDevice.ErrorResolution
- Win32_MemoryDevice.ErrorTime
- Win32_MemoryDevice.ErrorTransferSize
- Win32_MemoryDevice.InstallDate
- Win32_MemoryDevice.LastErrorCode
- Win32_MemoryDevice.Name
- Win32_MemoryDevice.NumberOfBlocks
- Win32_MemoryDevice.OtherErrorDescription
- Win32_MemoryDevice.PNPDeviceID
- Win32_MemoryDevice.PowerManagementCapabilities
- Win32_MemoryDevice.PowerManagementSupported
- Win32_MemoryDevice.Purpose
- Win32_MemoryDevice.StartingAddress
- Win32_MemoryDevice.Status
- Win32_MemoryDevice.StatusInfo
- Win32_MemoryDevice.SystemCreationClassName
- Win32_MemoryDevice.SystemLevelAddress
- Win32_MemoryDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 277b868f1b92b9f7c6a0c520c77ab76fac6b544d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990419"
---
# <a name="win32_memorydevice-class"></a><span data-ttu-id="470e0-103">\_Класс Win32 меморидевице</span><span class="sxs-lookup"><span data-stu-id="470e0-103">Win32\_MemoryDevice class</span></span>

<span data-ttu-id="470e0-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ меморидевице для Win32** представляет свойства устройства памяти компьютерной системы и связанных с ним сопоставленных адресов.</span><span class="sxs-lookup"><span data-stu-id="470e0-104">The **Win32\_MemoryDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a computer system memory device and its associated mapped addresses.</span></span>

<span data-ttu-id="470e0-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="470e0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="470e0-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="470e0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="470e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="470e0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDevice : Win32_SMBIOSMemory
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

## <a name="members"></a><span data-ttu-id="470e0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="470e0-108">Members</span></span>

<span data-ttu-id="470e0-109">Класс **Win32 \_ меморидевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="470e0-109">The **Win32\_MemoryDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="470e0-110">Методы</span><span class="sxs-lookup"><span data-stu-id="470e0-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="470e0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="470e0-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="470e0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="470e0-112">Methods</span></span>

<span data-ttu-id="470e0-113">Класс **Win32 \_ меморидевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="470e0-113">The **Win32\_MemoryDevice** class has these methods.</span></span>



| <span data-ttu-id="470e0-114">Метод</span><span class="sxs-lookup"><span data-stu-id="470e0-114">Method</span></span>            | <span data-ttu-id="470e0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="470e0-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="470e0-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="470e0-116">**Reset**</span></span>         | <span data-ttu-id="470e0-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="470e0-117">Not implemented.</span></span> <span data-ttu-id="470e0-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/>                 |
| <span data-ttu-id="470e0-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="470e0-119">**SetPowerState**</span></span> | <span data-ttu-id="470e0-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="470e0-120">Not implemented.</span></span> <span data-ttu-id="470e0-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="470e0-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="470e0-122">Properties</span></span>

<span data-ttu-id="470e0-123">Класс **Win32 \_ меморидевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="470e0-123">The **Win32\_MemoryDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="470e0-124">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="470e0-124">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-127">Доступ к носителю доступен.</span><span class="sxs-lookup"><span data-stu-id="470e0-127">Media access available.</span></span>

<span data-ttu-id="470e0-128">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-128">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="470e0-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="470e0-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-130"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="470e0-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-131"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-132">Возможность записи</span><span class="sxs-lookup"><span data-stu-id="470e0-132">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="470e0-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-133"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="470e0-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-134"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-135">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="470e0-135">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-136">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="470e0-136">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="470e0-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32 — сведения об ошибке в памяти \| поставщика синдром"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="470e0-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Vendor Syndrome"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="470e0-139">Массив дополнительных сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="470e0-139">Array of additional error information.</span></span> <span data-ttu-id="470e0-140">Примером является проверка ошибок и исправление ошибки (ECC) синдром или возвращение битов проверки при использовании методологии проверки погрешности на основе контрольной суммы (CRC).</span><span class="sxs-lookup"><span data-stu-id="470e0-140">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a cyclical redundancy check (CRC) based error methodology is used.</span></span> <span data-ttu-id="470e0-141">В последнем случае, если обнаружена Одноразрядная ошибка и известен алгоритм CRC, можно определить точный бит, в котором произошел сбой.</span><span class="sxs-lookup"><span data-stu-id="470e0-141">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, it is possible to determine the exact bit that failed.</span></span> <span data-ttu-id="470e0-142">Этот тип данных (ECC синдром, бит проверки, битные данные четности или другие сведения, предоставленные поставщиком) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="470e0-142">This type of data (ECC Syndrome, Check Bit, Parity Bit data, or other vendor-supplied information) is included in this field.</span></span> <span data-ttu-id="470e0-143">Это свойство используется только в том случае, если свойство **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-143">This property is used only when the **ErrorInfo** property is not equal to 3.</span></span>

<span data-ttu-id="470e0-144">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-144">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-145">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="470e0-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="470e0-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-149">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-149">Availability and status of the device.</span></span>

<span data-ttu-id="470e0-150">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="470e0-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="470e0-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-154">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="470e0-154">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="470e0-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-155"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="470e0-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="470e0-156"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="470e0-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="470e0-157"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="470e0-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="470e0-158"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="470e0-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="470e0-159"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="470e0-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="470e0-160"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="470e0-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="470e0-161"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="470e0-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="470e0-162"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="470e0-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="470e0-163"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="470e0-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="470e0-164"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-165">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="470e0-165">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="470e0-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="470e0-166"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-167">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="470e0-167">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="470e0-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="470e0-168"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-169">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="470e0-169">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="470e0-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="470e0-170"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="470e0-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="470e0-171"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-172">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="470e0-172">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="470e0-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="470e0-173"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-174">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="470e0-174">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="470e0-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="470e0-175"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-176">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="470e0-176">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="470e0-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="470e0-177"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-178">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="470e0-178">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="470e0-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="470e0-179"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-180">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="470e0-180">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-181">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="470e0-181">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-182">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="470e0-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-184">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="470e0-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-185">Размер в байтах блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="470e0-185">Size in bytes of the blocks that form this storage extent.</span></span> <span data-ttu-id="470e0-186">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="470e0-186">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="470e0-187">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-187">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="470e0-188">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="470e0-188">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-189">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="470e0-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-192">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="470e0-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-193">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="470e0-193">Short description of the object a one-line string.</span></span>

<span data-ttu-id="470e0-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-195">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="470e0-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-196">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470e0-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-198">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="470e0-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-199">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="470e0-199">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="470e0-200">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="470e0-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="470e0-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="470e0-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="470e0-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-203">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="470e0-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="470e0-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="470e0-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="470e0-205">(1)</span><span class="sxs-lookup"><span data-stu-id="470e0-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-206">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="470e0-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="470e0-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="470e0-208">(2)</span><span class="sxs-lookup"><span data-stu-id="470e0-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="470e0-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="470e0-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="470e0-210">(3)</span><span class="sxs-lookup"><span data-stu-id="470e0-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-211">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="470e0-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="470e0-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="470e0-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="470e0-213">(4)</span><span class="sxs-lookup"><span data-stu-id="470e0-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-214">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="470e0-214">Device is not working properly.</span></span> <span data-ttu-id="470e0-215">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="470e0-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="470e0-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="470e0-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="470e0-217">(5)</span><span class="sxs-lookup"><span data-stu-id="470e0-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-218">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="470e0-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="470e0-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="470e0-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="470e0-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="470e0-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-221">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="470e0-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="470e0-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="470e0-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="470e0-223">(7)</span><span class="sxs-lookup"><span data-stu-id="470e0-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="470e0-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="470e0-225">(8)</span><span class="sxs-lookup"><span data-stu-id="470e0-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-226">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="470e0-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="470e0-228">(9)</span><span class="sxs-lookup"><span data-stu-id="470e0-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-229">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="470e0-229">Device is not working properly.</span></span> <span data-ttu-id="470e0-230">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="470e0-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="470e0-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="470e0-232">(10)</span><span class="sxs-lookup"><span data-stu-id="470e0-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-233">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="470e0-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="470e0-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="470e0-235">(11)</span><span class="sxs-lookup"><span data-stu-id="470e0-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-236">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="470e0-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="470e0-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="470e0-238">(12)</span><span class="sxs-lookup"><span data-stu-id="470e0-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-239">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="470e0-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="470e0-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="470e0-241">(13)</span><span class="sxs-lookup"><span data-stu-id="470e0-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-242">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="470e0-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="470e0-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="470e0-244">(14)</span><span class="sxs-lookup"><span data-stu-id="470e0-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-245">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="470e0-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="470e0-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="470e0-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="470e0-247">(15)</span><span class="sxs-lookup"><span data-stu-id="470e0-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-248">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="470e0-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="470e0-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="470e0-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="470e0-250">(16)</span><span class="sxs-lookup"><span data-stu-id="470e0-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-251">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="470e0-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="470e0-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="470e0-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="470e0-253">(17)</span><span class="sxs-lookup"><span data-stu-id="470e0-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-254">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="470e0-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="470e0-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="470e0-256">(18)</span><span class="sxs-lookup"><span data-stu-id="470e0-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-257">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="470e0-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="470e0-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="470e0-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="470e0-259">(19)</span><span class="sxs-lookup"><span data-stu-id="470e0-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="470e0-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="470e0-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="470e0-261">(20)</span><span class="sxs-lookup"><span data-stu-id="470e0-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-262">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="470e0-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="470e0-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="470e0-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="470e0-264">(21)</span><span class="sxs-lookup"><span data-stu-id="470e0-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-265">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="470e0-265">System failure.</span></span> <span data-ttu-id="470e0-266">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="470e0-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="470e0-267">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="470e0-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="470e0-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="470e0-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="470e0-269">(22)</span><span class="sxs-lookup"><span data-stu-id="470e0-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-270">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="470e0-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="470e0-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="470e0-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="470e0-272">(23)</span><span class="sxs-lookup"><span data-stu-id="470e0-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-273">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="470e0-273">System failure.</span></span> <span data-ttu-id="470e0-274">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="470e0-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="470e0-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="470e0-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="470e0-276">(24)</span><span class="sxs-lookup"><span data-stu-id="470e0-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-277">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="470e0-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="470e0-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="470e0-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="470e0-279">(25)</span><span class="sxs-lookup"><span data-stu-id="470e0-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-280">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="470e0-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="470e0-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="470e0-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="470e0-282">(26)</span><span class="sxs-lookup"><span data-stu-id="470e0-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-283">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="470e0-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="470e0-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="470e0-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="470e0-285">(27)</span><span class="sxs-lookup"><span data-stu-id="470e0-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-286">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="470e0-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="470e0-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="470e0-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="470e0-288">(28)</span><span class="sxs-lookup"><span data-stu-id="470e0-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-289">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="470e0-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="470e0-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="470e0-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="470e0-291">(29)</span><span class="sxs-lookup"><span data-stu-id="470e0-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-292">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="470e0-292">Device is disabled.</span></span> <span data-ttu-id="470e0-293">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="470e0-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="470e0-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="470e0-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="470e0-295">(30)</span><span class="sxs-lookup"><span data-stu-id="470e0-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-296">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="470e0-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="470e0-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="470e0-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="470e0-298">1-31</span><span class="sxs-lookup"><span data-stu-id="470e0-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-299">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="470e0-299">Device is not working properly.</span></span> <span data-ttu-id="470e0-300">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="470e0-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-301">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="470e0-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-302">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="470e0-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-304">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="470e0-304">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-305">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="470e0-305">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="470e0-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-307">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="470e0-307">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-308">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="470e0-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-310">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный тип ошибки сведений об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="470e0-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-311">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="470e0-311">If **True**, the most recent error was correctable.</span></span> <span data-ttu-id="470e0-312">Это свойство не используется, если значение **errorInfo** равно 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-312">This property is not used if **ErrorInfo** is set to 3.</span></span>

<span data-ttu-id="470e0-313">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-313">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-314">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="470e0-314">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-317">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="470e0-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="470e0-318">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="470e0-318">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="470e0-319">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="470e0-319">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="470e0-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-321">**Описание**</span><span class="sxs-lookup"><span data-stu-id="470e0-321">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-324">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="470e0-324">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-325">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="470e0-325">Description of the object.</span></span>

<span data-ttu-id="470e0-326">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-327">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="470e0-327">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-330">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="470e0-330">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-331">Уникальный идентификатор устройства памяти.</span><span class="sxs-lookup"><span data-stu-id="470e0-331">Unique identifier of the memory device.</span></span>

<span data-ttu-id="470e0-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="470e0-333">Пример: "устройство памяти 1"</span><span class="sxs-lookup"><span data-stu-id="470e0-333">Example: "Memory Device 1"</span></span>

</dd> <dt>

<span data-ttu-id="470e0-334">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="470e0-334">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-335">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="470e0-335">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 19 \| памяти, сопоставленные адреса \| конечного адреса")</span><span class="sxs-lookup"><span data-stu-id="470e0-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Ending Address")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-338">Конечный адрес, на который ссылается приложение или операционная система.</span><span class="sxs-lookup"><span data-stu-id="470e0-338">Ending address referenced by an application or operating system.</span></span> <span data-ttu-id="470e0-339">Этот адрес памяти сопоставляется контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="470e0-339">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="470e0-340">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-340">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="470e0-341">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="470e0-341">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-342">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="470e0-342">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-343">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-345">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядная ошибка со сведениями об ошибке в памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="470e0-345">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Operation")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-346">Тип операции доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="470e0-346">Type of memory access operation that caused the last error.</span></span> <span data-ttu-id="470e0-347">Это свойство допустимо, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-347">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="470e0-348">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-348">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="470e0-349">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-350">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="470e0-351">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-351">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="470e0-352">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-352">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="470e0-353">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="470e0-353">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-354">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="470e0-354">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-355">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="470e0-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-357">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный адрес ошибки в информации об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="470e0-357">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-358">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="470e0-358">Address of the last memory error.</span></span> <span data-ttu-id="470e0-359">Это свойство используется, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-359">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="470e0-360">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-360">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="470e0-361">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="470e0-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-362">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="470e0-362">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-363">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="470e0-363">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-365">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="470e0-365">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="470e0-366">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-367">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="470e0-367">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-368">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="470e0-368">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="470e0-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-370">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="470e0-370">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="470e0-371">Массив данных, полученных из последнего доступа к памяти с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="470e0-371">Array of data captured from the last memory access with an error.</span></span> <span data-ttu-id="470e0-372">Данные занимают первые *n* октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="470e0-372">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="470e0-373">Если **еррортрансферсизе** имеет значение 0 (ноль), это свойство не используется.</span><span class="sxs-lookup"><span data-stu-id="470e0-373">If **ErrorTransferSize** is 0 (zero), then this property is not used.</span></span>

<span data-ttu-id="470e0-374">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-374">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-375">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="470e0-375">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-378">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="470e0-378">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-379">Упорядочивание данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="470e0-379">Ordering for data stored in the **ErrorData** property.</span></span> <span data-ttu-id="470e0-380">Это свойство используется, только если **еррортрансферсизе** имеет значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="470e0-380">This property is used only when **ErrorTransferSize** is 0 (zero).</span></span>

<span data-ttu-id="470e0-381">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-381">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-382">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="470e0-382">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="470e0-383">**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-383">**Least Significant Byte First** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="470e0-384">**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-384">**Most Significant Byte First** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-385">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="470e0-385">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-386">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-388">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="470e0-388">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="470e0-389">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-390">**ерроргрануларити**</span><span class="sxs-lookup"><span data-stu-id="470e0-390">**ErrorGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-391">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-393">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 — \| Детализация ошибок")</span><span class="sxs-lookup"><span data-stu-id="470e0-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|Error Granularity")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-394">Уровень, на котором может быть разрешена ошибка.</span><span class="sxs-lookup"><span data-stu-id="470e0-394">Level where the error can be resolved.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="470e0-395">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-396">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_level"></span><span id="device_level"></span><span id="DEVICE_LEVEL"></span>

<span data-ttu-id="470e0-397">**Уровень устройства** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-397">**Device level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_partition_level"></span><span id="memory_partition_level"></span><span id="MEMORY_PARTITION_LEVEL"></span>

<span data-ttu-id="470e0-398">**Уровень секции памяти** (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-398">**Memory partition level** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-399">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="470e0-399">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-400">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-400">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-402">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**Осереррордескриптион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный тип ошибки сведений об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="470e0-402">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Type")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-403">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="470e0-403">Type of error that occurred most recently.</span></span> <span data-ttu-id="470e0-404">Значения 12-14, указывающие, является ли ошибка исправимой, не используются с этим свойством, но эти сведения находятся в свойстве **корректаблиррор** .</span><span class="sxs-lookup"><span data-stu-id="470e0-404">The values 12-14, indicating whether an error is correctable, are not used with this property, but this information is found in the **CorrectableError** property.</span></span>

<span data-ttu-id="470e0-405">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-405">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="470e0-406">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-406">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-407">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-407">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="470e0-408">**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-408">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="470e0-409">**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-409">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="470e0-410">**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="470e0-410">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="470e0-411">**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="470e0-411">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="470e0-412">**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="470e0-412">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="470e0-413">**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="470e0-413">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="470e0-414">**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="470e0-414">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="470e0-415">**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="470e0-415">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="470e0-416">**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="470e0-416">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_single-bit_error"></span><span id="corrected_single-bit_error"></span><span id="CORRECTED_SINGLE-BIT_ERROR"></span>

<span data-ttu-id="470e0-417">**Исправленная Одноразрядная ошибка** (12)</span><span class="sxs-lookup"><span data-stu-id="470e0-417">**Corrected single-bit error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrected_error"></span><span id="corrected_error"></span><span id="CORRECTED_ERROR"></span>

<span data-ttu-id="470e0-418">**Исправленная ошибка** (13)</span><span class="sxs-lookup"><span data-stu-id="470e0-418">**Corrected error** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Uncorrectable_error"></span><span id="uncorrectable_error"></span><span id="UNCORRECTABLE_ERROR"></span>

<span data-ttu-id="470e0-419">**Неисправимая ошибка** (14)</span><span class="sxs-lookup"><span data-stu-id="470e0-419">**Uncorrectable error** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-420">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="470e0-420">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-423">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 16. \| \| исправление ошибки памяти массива физической памяти")</span><span class="sxs-lookup"><span data-stu-id="470e0-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 16\|Physical Memory Array\|Memory Error Correction")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-424">Типы проверки ошибок, используемые оборудованием памяти.</span><span class="sxs-lookup"><span data-stu-id="470e0-424">Types of error checking used by the memory hardware.</span></span>

<span data-ttu-id="470e0-425">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-425">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="470e0-426">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="470e0-426">The values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="470e0-427">**Другое** ("другое")</span><span class="sxs-lookup"><span data-stu-id="470e0-427">**Other** ("Other")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-428">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="470e0-428">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

<span data-ttu-id="470e0-429">**Четность** ("четность")</span><span class="sxs-lookup"><span data-stu-id="470e0-429">**Parity** ("Parity")</span></span>


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

<span data-ttu-id="470e0-430">**Одноразрядный ECC** (одноразрядный ECC)</span><span class="sxs-lookup"><span data-stu-id="470e0-430">**Single-bit ECC** ("Single-bit ECC")</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

<span data-ttu-id="470e0-431">**Многоразрядный ECC** (Многоразрядный ECC)</span><span class="sxs-lookup"><span data-stu-id="470e0-431">**Multi-bit ECC** ("Multi-bit ECC")</span></span>


</dt> <dd></dd> <dt>




</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="470e0-432">**Нет** ("нет")</span><span class="sxs-lookup"><span data-stu-id="470e0-432">**None** ("None")</span></span>


</dt> <dd></dd> <dt>

<span id="CRC"></span><span id="crc"></span>

<span data-ttu-id="470e0-433">**CRC** ("CRC")</span><span class="sxs-lookup"><span data-stu-id="470e0-433">**CRC** ("CRC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-434">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="470e0-434">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-435">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="470e0-435">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-437">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядная ошибка при \| устранении ошибок в памяти"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="470e0-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Resolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-438">Объем данных, фактически определенный для возникновения ошибки.</span><span class="sxs-lookup"><span data-stu-id="470e0-438">Amount of data actually determined to cause the error.</span></span> <span data-ttu-id="470e0-439">Это свойство не используется, если свойство **errorInfo** имеет значение 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-439">This property is unused when the **ErrorInfo** property is set to 3.</span></span>

<span data-ttu-id="470e0-440">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-440">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="470e0-441">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="470e0-441">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-442">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="470e0-442">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-443">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="470e0-443">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-445">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="470e0-445">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-446">Время, когда произошла последняя ошибка памяти.</span><span class="sxs-lookup"><span data-stu-id="470e0-446">Time that the last memory error occurred.</span></span> <span data-ttu-id="470e0-447">Это свойство допустимо, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-447">This property is valid only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="470e0-448">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-448">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-449">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="470e0-449">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-450">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470e0-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-452">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BITS")</span><span class="sxs-lookup"><span data-stu-id="470e0-452">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-453">Размер данных (содержащих последнюю ошибку), которые передаются.</span><span class="sxs-lookup"><span data-stu-id="470e0-453">Size of the data (containing the last error) being transferred.</span></span> <span data-ttu-id="470e0-454">Если ошибка отсутствует, это свойство имеет значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="470e0-454">This property is set to 0 (zero) if there is no error.</span></span>

<span data-ttu-id="470e0-455">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-455">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-456">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="470e0-456">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-457">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="470e0-457">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-459">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="470e0-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-460">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="470e0-460">Date and time the object was installed.</span></span> <span data-ttu-id="470e0-461">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="470e0-461">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="470e0-462">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-462">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-463">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="470e0-463">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-464">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="470e0-464">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-465">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-466">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="470e0-466">Last error code reported by the logical device.</span></span>

<span data-ttu-id="470e0-467">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-468">**Name**</span><span class="sxs-lookup"><span data-stu-id="470e0-468">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-471">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="470e0-471">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-472">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="470e0-472">Label by which the object is known.</span></span> <span data-ttu-id="470e0-473">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="470e0-473">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="470e0-474">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-474">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-475">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="470e0-475">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-476">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="470e0-476">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-478">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="470e0-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-479">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="470e0-479">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="470e0-480">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="470e0-480">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="470e0-481">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="470e0-481">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="470e0-482">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-482">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="470e0-483">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="470e0-483">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-484">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="470e0-484">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-485">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-485">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-486">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-487">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**ErrorInfo**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" SMBIOS ")</span><span class="sxs-lookup"><span data-stu-id="470e0-487">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-488">Дополнительные сведения о том, что свойство **errorInfo** имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="470e0-488">More information when the **ErrorInfo** property is set to 1.</span></span>

<span data-ttu-id="470e0-489">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-489">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-490">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="470e0-490">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-491">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-493">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="470e0-493">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-494">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-494">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="470e0-495">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="470e0-496">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="470e0-496">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="470e0-497">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="470e0-497">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-498">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="470e0-498">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="470e0-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-500">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="470e0-500">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="470e0-501">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-501">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="470e0-502"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="470e0-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-503"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="470e0-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-504"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="470e0-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-505"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-506">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="470e0-506">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="470e0-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-507"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-508">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="470e0-508">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="470e0-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="470e0-509"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-510">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="470e0-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="470e0-511">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="470e0-511">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="470e0-512">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="470e0-512">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="470e0-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="470e0-513"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-514">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="470e0-514">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="470e0-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="470e0-515"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="470e0-516">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="470e0-516">Timed Power-On Supported</span></span>

<span data-ttu-id="470e0-517">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="470e0-517">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-518">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="470e0-518">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-519">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="470e0-519">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-520">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-520">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-521">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="470e0-521">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="470e0-522">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="470e0-522">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="470e0-523">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-523">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-524">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="470e0-524">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-525">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-525">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-526">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-526">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="470e0-527">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="470e0-527">Free-form string describing the media and its use.</span></span>

<span data-ttu-id="470e0-528">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-528">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-529">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="470e0-529">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-530">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="470e0-530">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-531">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-531">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-532">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 19 \| памяти, сопоставленные адреса \| начальный адрес")</span><span class="sxs-lookup"><span data-stu-id="470e0-532">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 19\|Memory Device Mapped Addresses\|Starting Address")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-533">Начальный адрес, на который ссылается приложение или операционная система.</span><span class="sxs-lookup"><span data-stu-id="470e0-533">Beginning address referenced by an application or the operating system.</span></span> <span data-ttu-id="470e0-534">Этот адрес памяти сопоставляется контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="470e0-534">This memory address is mapped by a memory controller for this memory object.</span></span>

<span data-ttu-id="470e0-535">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-535">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

<span data-ttu-id="470e0-536">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="470e0-536">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-537">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="470e0-537">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-538">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-539">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-540">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="470e0-540">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-541">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="470e0-541">Current status of the object.</span></span> <span data-ttu-id="470e0-542">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="470e0-542">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="470e0-543">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="470e0-543">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="470e0-544">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="470e0-544">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="470e0-545">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="470e0-545">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="470e0-546">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="470e0-546">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="470e0-547">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-547">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="470e0-548">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="470e0-548">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="470e0-549">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="470e0-549">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="470e0-550">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="470e0-550">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="470e0-551">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="470e0-551">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-552">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="470e0-552">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="470e0-553">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="470e0-553">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="470e0-554">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="470e0-554">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="470e0-555">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="470e0-555">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="470e0-556">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="470e0-556">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="470e0-557">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="470e0-557">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="470e0-558">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="470e0-558">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="470e0-559">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="470e0-559">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="470e0-560">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="470e0-560">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-561">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="470e0-561">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-562">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="470e0-562">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-563">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-563">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-564">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="470e0-564">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-565">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="470e0-565">State of the logical device.</span></span> <span data-ttu-id="470e0-566">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="470e0-566">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="470e0-567">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-567">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="470e0-568">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="470e0-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="470e0-569">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="470e0-569">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="470e0-570">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="470e0-570">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="470e0-571">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="470e0-571">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="470e0-572">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="470e0-572">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="470e0-573">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="470e0-573">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-574">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-575">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-575">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-576">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="470e0-576">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="470e0-577">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="470e0-577">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="470e0-578">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-578">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-579">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="470e0-579">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-580">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="470e0-580">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-581">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-582">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 18 \| 32-разрядный адрес ошибки в информации об ошибках памяти \| ")</span><span class="sxs-lookup"><span data-stu-id="470e0-582">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 18\|32-bit Memory Error Information\|Error Address")</span></span>
</dt> </dl>

<span data-ttu-id="470e0-583">Если **значение — true**, сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня.</span><span class="sxs-lookup"><span data-stu-id="470e0-583">If **True**, the address information in the **ErrorAddress** property is a system-level address.</span></span> <span data-ttu-id="470e0-584">Если **значение равно false**, это физический адрес.</span><span class="sxs-lookup"><span data-stu-id="470e0-584">If **FALSE**, it is a physical address.</span></span> <span data-ttu-id="470e0-585">Это свойство используется, только если значение **errorInfo** не равно 3.</span><span class="sxs-lookup"><span data-stu-id="470e0-585">This property is used only when **ErrorInfo** is not set to 3.</span></span>

<span data-ttu-id="470e0-586">Это свойство наследуется из [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-586">This property is inherited from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="470e0-587">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="470e0-587">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="470e0-588">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="470e0-588">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="470e0-589">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="470e0-589">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="470e0-590">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="470e0-590">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="470e0-591">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="470e0-591">Name of the scoping system.</span></span>

<span data-ttu-id="470e0-592">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="470e0-592">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="470e0-593">Комментарии</span><span class="sxs-lookup"><span data-stu-id="470e0-593">Remarks</span></span>

<span data-ttu-id="470e0-594">Класс **Win32 \_ меморидевице** является производным от [**Win32 \_ смбиосмемори**](win32-smbiosmemory.md).</span><span class="sxs-lookup"><span data-stu-id="470e0-594">The **Win32\_MemoryDevice** class is derived from [**Win32\_SMBIOSMemory**](win32-smbiosmemory.md).</span></span>

## <a name="examples"></a><span data-ttu-id="470e0-595">Примеры</span><span class="sxs-lookup"><span data-stu-id="470e0-595">Examples</span></span>

<span data-ttu-id="470e0-596">Образец Perl для [устройств памяти](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Возвращает начальные и конечные адреса для всех устройств памяти, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="470e0-596">The [List Memory Devices](https://Gallery.TechNet.Microsoft.Com/ddc9c2ab-3f88-44fb-935f-98da3bcf5858) Perl sample returns starting and ending addresses for all memory devices installed on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="470e0-597">Требования</span><span class="sxs-lookup"><span data-stu-id="470e0-597">Requirements</span></span>



| <span data-ttu-id="470e0-598">Требование</span><span class="sxs-lookup"><span data-stu-id="470e0-598">Requirement</span></span> | <span data-ttu-id="470e0-599">Значение</span><span class="sxs-lookup"><span data-stu-id="470e0-599">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="470e0-600">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="470e0-600">Minimum supported client</span></span><br/> | <span data-ttu-id="470e0-601">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="470e0-601">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="470e0-602">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="470e0-602">Minimum supported server</span></span><br/> | <span data-ttu-id="470e0-603">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="470e0-603">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="470e0-604">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="470e0-604">Namespace</span></span><br/>                | <span data-ttu-id="470e0-605">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="470e0-605">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="470e0-606">MOF</span><span class="sxs-lookup"><span data-stu-id="470e0-606">MOF</span></span><br/>                      | <dl> <span data-ttu-id="470e0-607"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="470e0-607"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="470e0-608">DLL</span><span class="sxs-lookup"><span data-stu-id="470e0-608">DLL</span></span><br/>                      | <dl> <span data-ttu-id="470e0-609"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="470e0-609"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="470e0-610">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="470e0-610">See also</span></span>

<dl> <dt>

[<span data-ttu-id="470e0-611">**\_Смбиосмемори Win32**</span><span class="sxs-lookup"><span data-stu-id="470e0-611">**Win32\_SMBIOSMemory**</span></span>](win32-smbiosmemory.md)
</dt> <dt>

[<span data-ttu-id="470e0-612">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="470e0-612">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

