---
description: '\_Класс памяти CIM представляет возможности и управление логическими устройствами, связанными с памятью.'
ms.assetid: ddc72aad-5687-4bc1-b402-e27b27eca9be
ms.tgt_platform: multiple
title: Класс CIM_Memory (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Caption
- CIM_Memory.Description
- CIM_Memory.InstallDate
- CIM_Memory.Name
- CIM_Memory.Status
- CIM_Memory.Availability
- CIM_Memory.ConfigManagerErrorCode
- CIM_Memory.ConfigManagerUserConfig
- CIM_Memory.CreationClassName
- CIM_Memory.DeviceID
- CIM_Memory.PowerManagementCapabilities
- CIM_Memory.ErrorCleared
- CIM_Memory.ErrorDescription
- CIM_Memory.LastErrorCode
- CIM_Memory.PNPDeviceID
- CIM_Memory.PowerManagementSupported
- CIM_Memory.StatusInfo
- CIM_Memory.SystemCreationClassName
- CIM_Memory.SystemName
- CIM_Memory.Access
- CIM_Memory.BlockSize
- CIM_Memory.NumberOfBlocks
- CIM_Memory.Purpose
- CIM_Memory.ErrorMethodology
- CIM_Memory.AdditionalErrorData
- CIM_Memory.CorrectableError
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorAddress
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorInfo
- CIM_Memory.ErrorResolution
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorTransferSize
- CIM_Memory.OtherErrorDescription
- CIM_Memory.StartingAddress
- CIM_Memory.SystemLevelAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35fbb8467337da1ceab044a42533a6ca8628cf63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142043"
---
# <a name="cim_memory-class-cimwin32-wmi-providers"></a><span data-ttu-id="f1efb-103">Класс CIM_Memory (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f1efb-103">CIM_Memory class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f1efb-104">Класс **\_ памяти CIM** представляет возможности и управление логическими устройствами, связанными с памятью.</span><span class="sxs-lookup"><span data-stu-id="f1efb-104">The **CIM\_Memory** class represents the capabilities and management of memory-related logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f1efb-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f1efb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f1efb-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f1efb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f1efb-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f1efb-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f1efb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1efb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1efb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B64-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
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
};
```

## <a name="members"></a><span data-ttu-id="f1efb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f1efb-110">Members</span></span>

<span data-ttu-id="f1efb-111">Класс **\_ памяти CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f1efb-111">The **CIM\_Memory** class has these types of members:</span></span>

-   [<span data-ttu-id="f1efb-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f1efb-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f1efb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1efb-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1efb-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f1efb-114">Methods</span></span>

<span data-ttu-id="f1efb-115">Класс **\_ памяти CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f1efb-115">The **CIM\_Memory** class has these methods.</span></span>



| <span data-ttu-id="f1efb-116">Метод</span><span class="sxs-lookup"><span data-stu-id="f1efb-116">Method</span></span>                                                            | <span data-ttu-id="f1efb-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f1efb-117">Description</span></span>                                                                                                                              |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1efb-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="f1efb-118">**Reset**</span></span>](reset-method-in-class-cim-memory.md)                 | <span data-ttu-id="f1efb-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="f1efb-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f1efb-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="f1efb-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="f1efb-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-memory.md) | <span data-ttu-id="f1efb-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="f1efb-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="f1efb-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="f1efb-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1efb-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1efb-124">Properties</span></span>

<span data-ttu-id="f1efb-125">Класс **\_ памяти CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-125">The **CIM\_Memory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1efb-126">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="f1efb-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1efb-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-129">Описание свойств чтения и записи носителя.</span><span class="sxs-lookup"><span data-stu-id="f1efb-129">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="f1efb-130">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-131">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f1efb-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="f1efb-132">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="f1efb-133">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="f1efb-134">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="f1efb-135">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-136">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="f1efb-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-137">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f1efb-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,18 "," MIF. \|Массив физической памяти DMTF \| 001,13 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1efb-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-140">Массив октетов, содержащих дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="f1efb-140">Array of octets that hold additional error information.</span></span> <span data-ttu-id="f1efb-141">Примером является проверка ошибок и исправление ошибки (ECC) синдром или возвращение битов проверки, если используется методология ошибок на основе CRC.</span><span class="sxs-lookup"><span data-stu-id="f1efb-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="f1efb-142">В последнем случае, если обнаружена Одноразрядная ошибка и известен алгоритм CRC, может быть определен точный бит, который не удалось определить.</span><span class="sxs-lookup"><span data-stu-id="f1efb-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="f1efb-143">Этот тип данных (ECC синдром, Check-bit или данные, поразрядные с контролем четности или другие предоставленные поставщиком сведения) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="f1efb-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="f1efb-144">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-145">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="f1efb-145">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-146">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1efb-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-149">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-149">Availability and status of the device.</span></span>

<span data-ttu-id="f1efb-150">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-150">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1efb-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-151"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="f1efb-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-153"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="f1efb-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-154"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="f1efb-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="f1efb-155"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f1efb-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="f1efb-156"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="f1efb-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="f1efb-157"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="f1efb-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="f1efb-158"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="f1efb-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="f1efb-159"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1efb-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="f1efb-160"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="f1efb-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="f1efb-161"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="f1efb-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="f1efb-162"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="f1efb-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="f1efb-163"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-164">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f1efb-164">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="f1efb-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="f1efb-165"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-166">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="f1efb-166">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="f1efb-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="f1efb-167"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-168">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="f1efb-168">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="f1efb-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="f1efb-169"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="f1efb-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="f1efb-170"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-171">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-171">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="f1efb-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="f1efb-172"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-173">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="f1efb-173">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="f1efb-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="f1efb-174"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-175">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="f1efb-175">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="f1efb-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="f1efb-176"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-177">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="f1efb-177">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="f1efb-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="f1efb-178"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-179">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="f1efb-179">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-180">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="f1efb-180">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-181">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1efb-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-183">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-184">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-184">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="f1efb-185">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="f1efb-185">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="f1efb-186">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="f1efb-186">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="f1efb-187">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1efb-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f1efb-188">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-188">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-189">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f1efb-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-192">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f1efb-192">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-193">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f1efb-193">A short textual description of the object.</span></span>

<span data-ttu-id="f1efb-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-195">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f1efb-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-196">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1efb-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-198">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1efb-198">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-199">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f1efb-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="f1efb-200">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="f1efb-201">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-201">**This device is working properly.**</span></span> <span data-ttu-id="f1efb-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="f1efb-202">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="f1efb-203">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-203">**This device is not configured correctly.**</span></span> <span data-ttu-id="f1efb-204">(1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-204">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1efb-205">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-205">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="f1efb-206">(2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-206">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="f1efb-207">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-207">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="f1efb-208">(3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-208">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f1efb-209">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-209">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="f1efb-210">(4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-210">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="f1efb-211">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-211">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="f1efb-212">(5)</span><span class="sxs-lookup"><span data-stu-id="f1efb-212">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="f1efb-213">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-213">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="f1efb-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="f1efb-214">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="f1efb-215">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-215">**Cannot filter.**</span></span> <span data-ttu-id="f1efb-216">(7)</span><span class="sxs-lookup"><span data-stu-id="f1efb-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="f1efb-217">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-217">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="f1efb-218">(8)</span><span class="sxs-lookup"><span data-stu-id="f1efb-218">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="f1efb-219">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-219">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="f1efb-220">(9)</span><span class="sxs-lookup"><span data-stu-id="f1efb-220">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="f1efb-221">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-221">**This device cannot start.**</span></span> <span data-ttu-id="f1efb-222">(10)</span><span class="sxs-lookup"><span data-stu-id="f1efb-222">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="f1efb-223">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-223">**This device failed.**</span></span> <span data-ttu-id="f1efb-224">(11)</span><span class="sxs-lookup"><span data-stu-id="f1efb-224">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="f1efb-225">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-225">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="f1efb-226">(12)</span><span class="sxs-lookup"><span data-stu-id="f1efb-226">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="f1efb-227">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-227">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="f1efb-228">(13)</span><span class="sxs-lookup"><span data-stu-id="f1efb-228">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="f1efb-229">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-229">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="f1efb-230">(14)</span><span class="sxs-lookup"><span data-stu-id="f1efb-230">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="f1efb-231">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-231">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="f1efb-232">(15)</span><span class="sxs-lookup"><span data-stu-id="f1efb-232">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="f1efb-233">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-233">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="f1efb-234">(16)</span><span class="sxs-lookup"><span data-stu-id="f1efb-234">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="f1efb-235">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-235">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="f1efb-236">(17)</span><span class="sxs-lookup"><span data-stu-id="f1efb-236">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1efb-237">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-237">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="f1efb-238">(18)</span><span class="sxs-lookup"><span data-stu-id="f1efb-238">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="f1efb-239">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-239">**Failure using the VxD loader.**</span></span> <span data-ttu-id="f1efb-240">(19)</span><span class="sxs-lookup"><span data-stu-id="f1efb-240">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="f1efb-241">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-241">**Your registry might be corrupted.**</span></span> <span data-ttu-id="f1efb-242">(20)</span><span class="sxs-lookup"><span data-stu-id="f1efb-242">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="f1efb-243">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-243">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="f1efb-244">(21)</span><span class="sxs-lookup"><span data-stu-id="f1efb-244">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="f1efb-245">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-245">**This device is disabled.**</span></span> <span data-ttu-id="f1efb-246">(22)</span><span class="sxs-lookup"><span data-stu-id="f1efb-246">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="f1efb-247">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-247">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="f1efb-248">(23)</span><span class="sxs-lookup"><span data-stu-id="f1efb-248">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="f1efb-249">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-249">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="f1efb-250">(24)</span><span class="sxs-lookup"><span data-stu-id="f1efb-250">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f1efb-251">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-251">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f1efb-252">(25)</span><span class="sxs-lookup"><span data-stu-id="f1efb-252">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="f1efb-253">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-253">**Windows is still setting up this device.**</span></span> <span data-ttu-id="f1efb-254">(26)</span><span class="sxs-lookup"><span data-stu-id="f1efb-254">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="f1efb-255">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-255">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="f1efb-256">(27)</span><span class="sxs-lookup"><span data-stu-id="f1efb-256">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="f1efb-257">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-257">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="f1efb-258">(28)</span><span class="sxs-lookup"><span data-stu-id="f1efb-258">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="f1efb-259">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-259">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="f1efb-260">(29)</span><span class="sxs-lookup"><span data-stu-id="f1efb-260">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="f1efb-261">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-261">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="f1efb-262">(30)</span><span class="sxs-lookup"><span data-stu-id="f1efb-262">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="f1efb-263">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="f1efb-263">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="f1efb-264">1-31</span><span class="sxs-lookup"><span data-stu-id="f1efb-264">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-265">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="f1efb-265">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-266">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f1efb-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-268">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1efb-268">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-269">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f1efb-269">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="f1efb-270">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-271">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="f1efb-271">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-272">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f1efb-272">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-274">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-274">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-275">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="f1efb-275">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="f1efb-276">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-276">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-277">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f1efb-277">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-280">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f1efb-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-281">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f1efb-281">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f1efb-282">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f1efb-282">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f1efb-283">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-283">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-284">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1efb-284">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-285">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-286">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-287">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f1efb-287">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-288">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f1efb-288">A textual description of the object.</span></span>

<span data-ttu-id="f1efb-289">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-289">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-290">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1efb-290">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-293">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f1efb-293">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-294">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-294">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="f1efb-295">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-295">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-296">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f1efb-296">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-297">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1efb-297">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-299">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,4 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,5 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-299">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-300">Конечный адрес, на который ссылается приложение или операционная система и который сопоставляется контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="f1efb-300">Ending address referenced by an application or operating system and mapped by a memory controller for this memory object.</span></span> <span data-ttu-id="f1efb-301">Конечный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="f1efb-301">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="f1efb-302">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1efb-302">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-303">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="f1efb-303">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-304">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1efb-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-306">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,15 "," MIF. \|Массив физической памяти DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-306">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-307">Операция доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="f1efb-307">Memory access operation that caused the last error.</span></span> <span data-ttu-id="f1efb-308">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-308">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f1efb-309">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-309">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1efb-310">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-310">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-311">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-311">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f1efb-312">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-312">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="f1efb-313">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-313">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="f1efb-314">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="f1efb-314">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-315">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="f1efb-315">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-316">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1efb-316">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-318">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. \|Массив физической памяти DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-319">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="f1efb-319">Address of the last memory error.</span></span> <span data-ttu-id="f1efb-320">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-320">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f1efb-321">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-321">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f1efb-322">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1efb-322">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-323">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="f1efb-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-324">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f1efb-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-326">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="f1efb-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="f1efb-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-328">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="f1efb-328">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-329">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f1efb-329">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-331">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. \|Массив физической памяти DMTF \| 001,12 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f1efb-331">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-332">Данные, захваченные во время последнего ошибочного доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="f1efb-332">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="f1efb-333">Данные занимают первые *n* октетов массива, которые необходимы для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-333">The data occupies the first *n* octets of the array that are necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="f1efb-334">Если **еррортрансферсизе** имеет значение 0, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-334">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-335">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="f1efb-335">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-336">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1efb-336">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-338">Порядок данных, хранящихся в свойстве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-338">Order of data stored in the **ErrorData** property.</span></span> <span data-ttu-id="f1efb-339">Если **еррортрансферсизе** имеет значение 0, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-339">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f1efb-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-341">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f1efb-341">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f1efb-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-342"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-343">Сначала следует наименее значащий байт.</span><span class="sxs-lookup"><span data-stu-id="f1efb-343">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="f1efb-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-344"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-345">Первый значащий байт.</span><span class="sxs-lookup"><span data-stu-id="f1efb-345">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-346">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="f1efb-346">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-349">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="f1efb-349">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="f1efb-350">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-351">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f1efb-351">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-352">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1efb-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-354">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ память CIM**".**Осереррордескриптион**")</span><span class="sxs-lookup"><span data-stu-id="f1efb-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-355">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="f1efb-355">Type of error that occurred most recently.</span></span> <span data-ttu-id="f1efb-356">Значения от 12 до 14 не определены в схеме CIM, так как DMI смешивает семантику типа ошибки и является ли она исправимой.</span><span class="sxs-lookup"><span data-stu-id="f1efb-356">The values 12 through 14 are undefined in the CIM schema because DMI mixes the semantics of the error type and whether it was correctable.</span></span> <span data-ttu-id="f1efb-357">Указывает, является ли ошибка исправимой, указывается в свойстве **корректаблиррор** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-357">Whether an error is correctable is indicated in the **CorrectableError** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1efb-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-358"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-359">Другое</span><span class="sxs-lookup"><span data-stu-id="f1efb-359">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-360"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-361">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="f1efb-361">Unknown.</span></span>

</dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f1efb-362"><span id="OK"></span><span id="ok"></span>**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-362"><span id="OK"></span><span id="ok"></span>**OK** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-363">Все в порядке.</span><span class="sxs-lookup"><span data-stu-id="f1efb-363">OK.</span></span>

</dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="f1efb-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-364"><span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>**Bad Read** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-365">Ошибка чтения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-365">Bad read.</span></span>

</dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="f1efb-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="f1efb-366"><span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>**Parity Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-367">Ошибка четности.</span><span class="sxs-lookup"><span data-stu-id="f1efb-367">Parity error.</span></span>

</dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="f1efb-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="f1efb-368"><span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>**Single-Bit Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-369">Одноразрядная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1efb-369">Single-bit error.</span></span>

</dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="f1efb-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="f1efb-370"><span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>**Double-Bit Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-371">Двойная разрядная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1efb-371">Double-bit error.</span></span>

</dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="f1efb-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="f1efb-372"><span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>**Multi-Bit Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-373">Многоразрядная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1efb-373">Multi-bit error.</span></span>

</dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="f1efb-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="f1efb-374"><span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>**Nibble Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-375">Ошибка погрешности.</span><span class="sxs-lookup"><span data-stu-id="f1efb-375">Nibble error.</span></span>

</dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="f1efb-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="f1efb-376"><span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>**Checksum Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-377">Ошибка контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="f1efb-377">Checksum error.</span></span>

</dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="f1efb-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="f1efb-378"><span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>**CRC Error** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-379">Ошибка CRC.</span><span class="sxs-lookup"><span data-stu-id="f1efb-379">CRC error.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f1efb-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (12)</span><span class="sxs-lookup"><span data-stu-id="f1efb-380"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (12)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-381">Не определено.</span><span class="sxs-lookup"><span data-stu-id="f1efb-381">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f1efb-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (13)</span><span class="sxs-lookup"><span data-stu-id="f1efb-382"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (13)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-383">Не определено.</span><span class="sxs-lookup"><span data-stu-id="f1efb-383">Undefined.</span></span>

</dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="f1efb-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>Не **определено** (14)</span><span class="sxs-lookup"><span data-stu-id="f1efb-384"><span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>**Undefined** (14)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-385">Не определено.</span><span class="sxs-lookup"><span data-stu-id="f1efb-385">Undefined.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-386">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="f1efb-386">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-389">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("еррормесодологи"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Массив физической памяти DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-389">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ErrorMethodology"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-390">Указывает, используются ли алгоритмы четности или CRC, ECC или другие механизмы.</span><span class="sxs-lookup"><span data-stu-id="f1efb-390">Indicates whether parity or CRC algorithms, ECC or other mechanisms are used.</span></span> <span data-ttu-id="f1efb-391">Также можно указать сведения об алгоритме.</span><span class="sxs-lookup"><span data-stu-id="f1efb-391">Details on the algorithm can also be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-392">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="f1efb-392">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-393">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1efb-393">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-395">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,21 "," MIF. \|Массив физической памяти DMTF \| 001,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-395">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-396">Указывает диапазон в байтах, до которого может быть разрешена Последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1efb-396">Specifies the range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="f1efb-397">Например, если адреса ошибок разрешаются в бит 11 (то есть на типичном уровне страницы), ошибки могут быть разрешены до 4 КБ, а значение этого свойства равно 4000.</span><span class="sxs-lookup"><span data-stu-id="f1efb-397">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="f1efb-398">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-398">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="f1efb-399">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1efb-399">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-400">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="f1efb-400">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-401">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1efb-401">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-402">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-403">Дата и время возникновения последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="f1efb-403">Date and time that the last memory error occurred.</span></span> <span data-ttu-id="f1efb-404">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-404">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="f1efb-405">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-405">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-406">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="f1efb-406">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-407">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1efb-407">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-408">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-409">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,16 "," MIF. \|Массив физической памяти DMTF \| 001,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-409">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-410">Размер передачи данных в битах, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="f1efb-410">Size of the data transfer, in bits, that caused the last error.</span></span> <span data-ttu-id="f1efb-411">Значение 0 указывает на отсутствие ошибки.</span><span class="sxs-lookup"><span data-stu-id="f1efb-411">A value of 0 indicates no error.</span></span> <span data-ttu-id="f1efb-412">Если свойство **errorInfo** равно 3 ("ОК"), то этому свойству должно быть присвоено значение 0.</span><span class="sxs-lookup"><span data-stu-id="f1efb-412">If the **ErrorInfo** property is equal to 3 ("OK"), then this property should be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-413">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f1efb-413">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-414">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f1efb-414">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-416">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-416">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-417">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="f1efb-417">Indicates when the object was installed.</span></span> <span data-ttu-id="f1efb-418">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f1efb-418">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f1efb-419">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-419">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-420">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="f1efb-420">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-421">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1efb-421">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-423">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="f1efb-423">Last error code reported by the logical device.</span></span>

<span data-ttu-id="f1efb-424">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-424">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-425">**Name**</span><span class="sxs-lookup"><span data-stu-id="f1efb-425">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-426">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-426">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-427">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-427">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-428">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f1efb-428">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-429">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f1efb-429">Label by which the object is known.</span></span> <span data-ttu-id="f1efb-430">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f1efb-430">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f1efb-431">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-431">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-432">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="f1efb-432">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-433">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1efb-433">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-435">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-435">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-436">Количество последовательных блоков, каждый из которых заблокирует размер значения, содержащегося **в свойстве, которое** формирует экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-436">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="f1efb-437">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-437">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="f1efb-438">Если **значение параметра DataSize равно 1** (один), это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-438">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="f1efb-439">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1efb-439">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="f1efb-440">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-440">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-441">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="f1efb-441">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-442">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-444">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ память CIM**".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="f1efb-444">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Memory**.**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-445">Строка свободной формы, которая предоставляет сведения, если свойство **ErrorType** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="f1efb-445">Free form string that provides information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="f1efb-446">Если значение не равно 1, то эта строка не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-446">If it is not set to 1, then this string has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-447">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="f1efb-447">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-450">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f1efb-450">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-451">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-451">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="f1efb-452">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="f1efb-452">Example: "\*PNP030b"</span></span>

<span data-ttu-id="f1efb-453">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-453">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-454">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="f1efb-454">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-455">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="f1efb-455">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-457">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="f1efb-457">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="f1efb-458">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f1efb-459"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-460">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="f1efb-460">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="f1efb-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-461"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-462">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="f1efb-462">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1efb-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-463"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-464">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="f1efb-464">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f1efb-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-465"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-466">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="f1efb-466">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="f1efb-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-467"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-468">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="f1efb-468">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="f1efb-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="f1efb-469"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-470">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-470">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="f1efb-471">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="f1efb-471">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="f1efb-472">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="f1efb-472">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="f1efb-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="f1efb-473"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-474">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="f1efb-474">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="f1efb-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="f1efb-475"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f1efb-476">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="f1efb-476">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-477">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="f1efb-477">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-478">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f1efb-478">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-480">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-480">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="f1efb-481">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-481">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f1efb-482">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="f1efb-482">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="f1efb-483">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="f1efb-483">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="f1efb-484">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-485">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="f1efb-485">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-486">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-486">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-488">Строка свободной формы, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="f1efb-488">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="f1efb-489">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-490">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f1efb-490">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-491">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1efb-491">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-493">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,3 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-493">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-494">Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для этого объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="f1efb-494">Beginning address, referenced by an application or operating system and mapped by a memory controller, for this memory object.</span></span> <span data-ttu-id="f1efb-495">Начальный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="f1efb-495">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="f1efb-496">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f1efb-496">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-497">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f1efb-497">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-498">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-500">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f1efb-500">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-501">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f1efb-501">String that indicates the current status of the object.</span></span> <span data-ttu-id="f1efb-502">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="f1efb-502">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f1efb-503">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="f1efb-503">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f1efb-504">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="f1efb-504">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f1efb-505">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="f1efb-505">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f1efb-506">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="f1efb-506">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f1efb-507">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f1efb-507">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f1efb-508">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-508">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f1efb-509">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f1efb-509">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f1efb-510">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f1efb-510">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f1efb-511">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f1efb-511">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f1efb-512">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f1efb-512">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-513">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f1efb-513">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f1efb-514">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f1efb-514">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f1efb-515">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f1efb-515">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f1efb-516">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f1efb-516">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f1efb-517">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f1efb-517">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f1efb-518">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f1efb-518">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f1efb-519">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f1efb-519">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f1efb-520">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f1efb-520">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f1efb-521">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f1efb-521">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-522">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="f1efb-522">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-523">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1efb-523">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-525">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="f1efb-525">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-526">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="f1efb-526">State of the logical device.</span></span> <span data-ttu-id="f1efb-527">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="f1efb-527">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="f1efb-528">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-528">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f1efb-529">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f1efb-529">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1efb-530">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f1efb-530">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="f1efb-531">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="f1efb-531">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="f1efb-532">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="f1efb-532">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="f1efb-533">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="f1efb-533">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1efb-534">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f1efb-534">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-536">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-537">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f1efb-537">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-538">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="f1efb-538">The scoping system's creation class name.</span></span>

<span data-ttu-id="f1efb-539">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-539">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-540">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="f1efb-540">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-541">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f1efb-541">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-543">Указывает, является ли информация об адресе в свойстве **еррораддресс** адресом системного уровня (**true**) или физическим адресом (**false**).</span><span class="sxs-lookup"><span data-stu-id="f1efb-543">Indicates whether the address information in the **ErrorAddress** property is a system-level address (**TRUE**) or a physical address (**FALSE**).</span></span> <span data-ttu-id="f1efb-544">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="f1efb-544">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

</dd> <dt>

<span data-ttu-id="f1efb-545">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f1efb-545">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1efb-546">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f1efb-546">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-547">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1efb-547">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1efb-548">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f1efb-548">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f1efb-549">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="f1efb-549">The scoping system's name.</span></span>

<span data-ttu-id="f1efb-550">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="f1efb-550">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1efb-551">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1efb-551">Remarks</span></span>

<span data-ttu-id="f1efb-552">Класс **\_ памяти CIM** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-552">The **CIM\_Memory** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="f1efb-553">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f1efb-553">WMI does not implement this class.</span></span> <span data-ttu-id="f1efb-554">Классы, производные от **\_ памяти CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f1efb-554">For classes that are derived from **CIM\_Memory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f1efb-555">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f1efb-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f1efb-556">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f1efb-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1efb-557">Требования</span><span class="sxs-lookup"><span data-stu-id="f1efb-557">Requirements</span></span>



| <span data-ttu-id="f1efb-558">Требование</span><span class="sxs-lookup"><span data-stu-id="f1efb-558">Requirement</span></span> | <span data-ttu-id="f1efb-559">Значение</span><span class="sxs-lookup"><span data-stu-id="f1efb-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1efb-560">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1efb-560">Minimum supported client</span></span><br/> | <span data-ttu-id="f1efb-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1efb-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1efb-562">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1efb-562">Minimum supported server</span></span><br/> | <span data-ttu-id="f1efb-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1efb-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1efb-564">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1efb-564">Namespace</span></span><br/>                | <span data-ttu-id="f1efb-565">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1efb-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1efb-566">MOF</span><span class="sxs-lookup"><span data-stu-id="f1efb-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1efb-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1efb-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1efb-568">DLL</span><span class="sxs-lookup"><span data-stu-id="f1efb-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1efb-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1efb-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1efb-570">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1efb-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1efb-571">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f1efb-571">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

