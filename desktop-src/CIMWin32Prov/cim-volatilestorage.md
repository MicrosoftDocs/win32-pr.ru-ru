---
description: Класс CIM \_ волатилестораже представляет возможности и управление энергозависимым хранилищем.
ms.assetid: c2f7e11e-d7e4-4709-be55-1c94a0b14010
ms.tgt_platform: multiple
title: Класс CIM_VolatileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolatileStorage
- CIM_VolatileStorage.Access
- CIM_VolatileStorage.AdditionalErrorData
- CIM_VolatileStorage.Availability
- CIM_VolatileStorage.BlockSize
- CIM_VolatileStorage.Cacheable
- CIM_VolatileStorage.CacheType
- CIM_VolatileStorage.Caption
- CIM_VolatileStorage.ConfigManagerErrorCode
- CIM_VolatileStorage.ConfigManagerUserConfig
- CIM_VolatileStorage.CorrectableError
- CIM_VolatileStorage.CreationClassName
- CIM_VolatileStorage.Description
- CIM_VolatileStorage.DeviceID
- CIM_VolatileStorage.EndingAddress
- CIM_VolatileStorage.ErrorAccess
- CIM_VolatileStorage.ErrorAddress
- CIM_VolatileStorage.ErrorCleared
- CIM_VolatileStorage.ErrorData
- CIM_VolatileStorage.ErrorDataOrder
- CIM_VolatileStorage.ErrorDescription
- CIM_VolatileStorage.ErrorInfo
- CIM_VolatileStorage.ErrorMethodology
- CIM_VolatileStorage.ErrorResolution
- CIM_VolatileStorage.ErrorTime
- CIM_VolatileStorage.ErrorTransferSize
- CIM_VolatileStorage.InstallDate
- CIM_VolatileStorage.LastErrorCode
- CIM_VolatileStorage.Name
- CIM_VolatileStorage.NumberOfBlocks
- CIM_VolatileStorage.OtherErrorDescription
- CIM_VolatileStorage.PNPDeviceID
- CIM_VolatileStorage.PowerManagementCapabilities
- CIM_VolatileStorage.PowerManagementSupported
- CIM_VolatileStorage.Purpose
- CIM_VolatileStorage.StartingAddress
- CIM_VolatileStorage.Status
- CIM_VolatileStorage.StatusInfo
- CIM_VolatileStorage.SystemCreationClassName
- CIM_VolatileStorage.SystemLevelAddress
- CIM_VolatileStorage.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 99add7401d92d82385a4182e466de8b28ad4fc09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895505"
---
# <a name="cim_volatilestorage-class"></a><span data-ttu-id="347d2-103">\_Класс CIM волатилестораже</span><span class="sxs-lookup"><span data-stu-id="347d2-103">CIM\_VolatileStorage class</span></span>

<span data-ttu-id="347d2-104">Класс **CIM \_ волатилестораже** представляет возможности и управление энергозависимым хранилищем.</span><span class="sxs-lookup"><span data-stu-id="347d2-104">The **CIM\_VolatileStorage** class represents the capabilities and management of volatile storage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="347d2-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="347d2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="347d2-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="347d2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="347d2-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="347d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="347d2-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="347d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="347d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="347d2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36851DFE-F0FE-11d2-8617-0000F8102E5F}"), AMENDMENT]
class CIM_VolatileStorage : CIM_Memory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Availability;
  uint64   BlockSize;
  boolean  Cacheable;
  uint16   CacheType;
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
  uint16   StatusInfo;
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="347d2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="347d2-110">Members</span></span>

<span data-ttu-id="347d2-111">Класс **CIM \_ волатилестораже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="347d2-111">The **CIM\_VolatileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="347d2-112">Методы</span><span class="sxs-lookup"><span data-stu-id="347d2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="347d2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="347d2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="347d2-114">Методы</span><span class="sxs-lookup"><span data-stu-id="347d2-114">Methods</span></span>

<span data-ttu-id="347d2-115">Класс **CIM \_ волатилестораже** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="347d2-115">The **CIM\_VolatileStorage** class has these methods.</span></span>



| <span data-ttu-id="347d2-116">Метод</span><span class="sxs-lookup"><span data-stu-id="347d2-116">Method</span></span>                                                                     | <span data-ttu-id="347d2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="347d2-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="347d2-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="347d2-118">**Reset**</span></span>](reset-method-in-class-cim-volatilestorage.md)                 | <span data-ttu-id="347d2-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="347d2-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="347d2-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="347d2-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="347d2-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volatilestorage.md) | <span data-ttu-id="347d2-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="347d2-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="347d2-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="347d2-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="347d2-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="347d2-124">Properties</span></span>

<span data-ttu-id="347d2-125">Класс **CIM \_ волатилестораже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="347d2-125">The **CIM\_VolatileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="347d2-126">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="347d2-126">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-129">Чтение и запись свойств носителя.</span><span class="sxs-lookup"><span data-stu-id="347d2-129">Read/write properties of the media.</span></span>

<span data-ttu-id="347d2-130">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-130">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-131">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="347d2-131">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="347d2-132">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-132">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="347d2-133">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-133">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="347d2-134">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-134">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="347d2-135">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-135">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-136">**аддитионалеррордата**</span><span class="sxs-lookup"><span data-stu-id="347d2-136">**AdditionalErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-137">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="347d2-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="347d2-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,18 "," MIF. \|Массив физической памяти DMTF \| 001,13 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="347d2-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.18", "MIF.DMTF\|Physical Memory Array\|001.13"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="347d2-140">Дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="347d2-140">Additional error information.</span></span> <span data-ttu-id="347d2-141">Примером является проверка ошибок и исправление ошибки (ECC) синдром или возвращение битов проверки, если используется методология ошибок на основе CRC.</span><span class="sxs-lookup"><span data-stu-id="347d2-141">An example is Error Checking and Correcting (ECC) Syndrome, or the return of the check bits if a CRC-based error methodology is used.</span></span> <span data-ttu-id="347d2-142">В последнем случае, если обнаружена Одноразрядная ошибка и известен алгоритм CRC, может быть определен точный бит, который не удалось определить.</span><span class="sxs-lookup"><span data-stu-id="347d2-142">In the latter case, if a single-bit error is recognized and the CRC algorithm is known, the exact bit that failed can be determined.</span></span> <span data-ttu-id="347d2-143">Этот тип данных (ECC синдром, Check-bit или данные, поразрядные с контролем четности или другие предоставленные поставщиком сведения) включен в это поле.</span><span class="sxs-lookup"><span data-stu-id="347d2-143">This type of data (ECC Syndrome, check-bit or parity-bit data, or other vendor supplied information) is included in this field.</span></span> <span data-ttu-id="347d2-144">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-144">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-145">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-145">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-146">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="347d2-146">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-147">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-149">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="347d2-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-150">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-150">Availability and status of the device.</span></span>

<span data-ttu-id="347d2-151">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-151">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="347d2-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-153"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="347d2-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-154"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-155">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="347d2-155">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="347d2-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-156"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="347d2-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="347d2-157"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="347d2-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="347d2-158"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="347d2-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="347d2-159"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="347d2-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="347d2-160"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="347d2-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="347d2-161"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="347d2-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="347d2-162"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="347d2-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="347d2-163"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="347d2-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="347d2-164"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="347d2-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="347d2-165"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-166">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="347d2-166">The device is known to be in a power-save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="347d2-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="347d2-167"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-168">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="347d2-168">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="347d2-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="347d2-169"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-170">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="347d2-170">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="347d2-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="347d2-171"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="347d2-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="347d2-172"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-173">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="347d2-173">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="347d2-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="347d2-174"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-175">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="347d2-175">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="347d2-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="347d2-176"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-177">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="347d2-177">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="347d2-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="347d2-178"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-179">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="347d2-179">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="347d2-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="347d2-180"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-181">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="347d2-181">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-182">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="347d2-182">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-183">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="347d2-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-185">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="347d2-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-186">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="347d2-186">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="347d2-187">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="347d2-187">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="347d2-188">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="347d2-188">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="347d2-189">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-189">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="347d2-190">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="347d2-190">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-191">**Кэшируемые**</span><span class="sxs-lookup"><span data-stu-id="347d2-191">**Cacheable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-192">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="347d2-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-194">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сведения о памяти системного ресурса DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-195">Если **значение равно true**, то эта память может быть кэширована.</span><span class="sxs-lookup"><span data-stu-id="347d2-195">If **TRUE**, this memory can be cached.</span></span>

</dd> <dt>

<span data-ttu-id="347d2-196">**CacheType**</span><span class="sxs-lookup"><span data-stu-id="347d2-196">**CacheType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-197">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-199">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сведения о памяти системного ресурса DMTF \| 001,6 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource Memory Info\|001.6")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-200">Тип кэша, совместимый с памятью.</span><span class="sxs-lookup"><span data-stu-id="347d2-200">Cache type that is compatible with the memory.</span></span> <span data-ttu-id="347d2-201">Если свойство **cacheed** имеет значение **false**, то это свойство не имеет значения и должно иметь значение 4 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="347d2-201">If the **Cacheable** property is set to **FALSE**, then this property does not have meaning and should be set to 4 ("Not Applicable").</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="347d2-202">**Другое** (0)</span><span class="sxs-lookup"><span data-stu-id="347d2-202">**Other** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-203">**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-203">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Back"></span><span id="write-back"></span><span id="WRITE-BACK"></span>

<span data-ttu-id="347d2-204">**Обратная запись** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-204">**Write-Back** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Write-Through"></span><span id="write-through"></span><span id="WRITE-THROUGH"></span>

<span data-ttu-id="347d2-205">Сквозная **запись** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-205">**Write-Through** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="347d2-206">**Неприменимо** (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-206">**Not Applicable** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-207">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="347d2-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-210">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="347d2-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-211">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="347d2-211">Short textual description of the object.</span></span>

<span data-ttu-id="347d2-212">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-213">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="347d2-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-214">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="347d2-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-216">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="347d2-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-217">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="347d2-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="347d2-218">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="347d2-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="347d2-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="347d2-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="347d2-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-221">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="347d2-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="347d2-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="347d2-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="347d2-223">(1)</span><span class="sxs-lookup"><span data-stu-id="347d2-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-224">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="347d2-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="347d2-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="347d2-226">(2)</span><span class="sxs-lookup"><span data-stu-id="347d2-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="347d2-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="347d2-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="347d2-228">(3)</span><span class="sxs-lookup"><span data-stu-id="347d2-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-229">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="347d2-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="347d2-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="347d2-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="347d2-231">(4)</span><span class="sxs-lookup"><span data-stu-id="347d2-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-232">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="347d2-232">Device is not working properly.</span></span> <span data-ttu-id="347d2-233">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="347d2-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="347d2-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="347d2-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="347d2-235">(5)</span><span class="sxs-lookup"><span data-stu-id="347d2-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-236">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="347d2-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="347d2-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="347d2-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="347d2-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="347d2-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-239">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="347d2-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="347d2-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="347d2-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="347d2-241">(7)</span><span class="sxs-lookup"><span data-stu-id="347d2-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="347d2-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="347d2-243">(8)</span><span class="sxs-lookup"><span data-stu-id="347d2-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-244">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="347d2-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="347d2-246">(9)</span><span class="sxs-lookup"><span data-stu-id="347d2-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-247">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="347d2-247">Device is not working properly.</span></span> <span data-ttu-id="347d2-248">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="347d2-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="347d2-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="347d2-250">(10)</span><span class="sxs-lookup"><span data-stu-id="347d2-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-251">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="347d2-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="347d2-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="347d2-253">(11)</span><span class="sxs-lookup"><span data-stu-id="347d2-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-254">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="347d2-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="347d2-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="347d2-256">(12)</span><span class="sxs-lookup"><span data-stu-id="347d2-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-257">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="347d2-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="347d2-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="347d2-259">(13)</span><span class="sxs-lookup"><span data-stu-id="347d2-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-260">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="347d2-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="347d2-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="347d2-262">(14)</span><span class="sxs-lookup"><span data-stu-id="347d2-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-263">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="347d2-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="347d2-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="347d2-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="347d2-265">(15)</span><span class="sxs-lookup"><span data-stu-id="347d2-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-266">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="347d2-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="347d2-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="347d2-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="347d2-268">(16)</span><span class="sxs-lookup"><span data-stu-id="347d2-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-269">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="347d2-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="347d2-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="347d2-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="347d2-271">(17)</span><span class="sxs-lookup"><span data-stu-id="347d2-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-272">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="347d2-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="347d2-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="347d2-274">(18)</span><span class="sxs-lookup"><span data-stu-id="347d2-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-275">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="347d2-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="347d2-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="347d2-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="347d2-277">(19)</span><span class="sxs-lookup"><span data-stu-id="347d2-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="347d2-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="347d2-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="347d2-279">(20)</span><span class="sxs-lookup"><span data-stu-id="347d2-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-280">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="347d2-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="347d2-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="347d2-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="347d2-282">(21)</span><span class="sxs-lookup"><span data-stu-id="347d2-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-283">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="347d2-283">System failure.</span></span> <span data-ttu-id="347d2-284">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="347d2-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="347d2-285">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="347d2-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="347d2-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="347d2-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="347d2-287">(22)</span><span class="sxs-lookup"><span data-stu-id="347d2-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-288">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="347d2-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="347d2-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="347d2-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="347d2-290">(23)</span><span class="sxs-lookup"><span data-stu-id="347d2-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-291">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="347d2-291">System failure.</span></span> <span data-ttu-id="347d2-292">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="347d2-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="347d2-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="347d2-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="347d2-294">(24)</span><span class="sxs-lookup"><span data-stu-id="347d2-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-295">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="347d2-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="347d2-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="347d2-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="347d2-297">(25)</span><span class="sxs-lookup"><span data-stu-id="347d2-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-298">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="347d2-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="347d2-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="347d2-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="347d2-300">(26)</span><span class="sxs-lookup"><span data-stu-id="347d2-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-301">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="347d2-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="347d2-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="347d2-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="347d2-303">(27)</span><span class="sxs-lookup"><span data-stu-id="347d2-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-304">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="347d2-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="347d2-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="347d2-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="347d2-306">(28)</span><span class="sxs-lookup"><span data-stu-id="347d2-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-307">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="347d2-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="347d2-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="347d2-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="347d2-309">(29)</span><span class="sxs-lookup"><span data-stu-id="347d2-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-310">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="347d2-310">Device is disabled.</span></span> <span data-ttu-id="347d2-311">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="347d2-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="347d2-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="347d2-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="347d2-313">(30)</span><span class="sxs-lookup"><span data-stu-id="347d2-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-314">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="347d2-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="347d2-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="347d2-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="347d2-316">1-31</span><span class="sxs-lookup"><span data-stu-id="347d2-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-317">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="347d2-317">Device is not working properly.</span></span> <span data-ttu-id="347d2-318">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="347d2-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-319">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="347d2-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-320">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="347d2-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-322">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="347d2-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-323">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="347d2-323">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="347d2-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-325">**корректаблиррор**</span><span class="sxs-lookup"><span data-stu-id="347d2-325">**CorrectableError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-326">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="347d2-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-328">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-329">**Значение true** показывает, что последняя ошибка была исправлена.</span><span class="sxs-lookup"><span data-stu-id="347d2-329">If **TRUE**, the most recent error was correctable.</span></span> <span data-ttu-id="347d2-330">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-330">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-331">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-331">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="347d2-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-335">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="347d2-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="347d2-336">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="347d2-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="347d2-337">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="347d2-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="347d2-338">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-339">**Описание**</span><span class="sxs-lookup"><span data-stu-id="347d2-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-342">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="347d2-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-343">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="347d2-343">Textual description of the object.</span></span>

<span data-ttu-id="347d2-344">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="347d2-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-348">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="347d2-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="347d2-349">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-349">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="347d2-350">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-351">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="347d2-351">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-352">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="347d2-352">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-354">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,4 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,5 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="347d2-354">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.4", "MIF.DMTF\|Memory Device Mapped Addresses\|001.5"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-355">Конечный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="347d2-355">Ending address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="347d2-356">Конечный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="347d2-356">The ending address is specified in kilobytes.</span></span>

<span data-ttu-id="347d2-357">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-357">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="347d2-358">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="347d2-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-359">**ерроракцесс**</span><span class="sxs-lookup"><span data-stu-id="347d2-359">**ErrorAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-360">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-362">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,15 "," MIF. \|Массив физической памяти DMTF \| 001,10 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.15", "MIF.DMTF\|Physical Memory Array\|001.10")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-363">Операция доступа к памяти, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="347d2-363">Memory access operation that caused the last error.</span></span> <span data-ttu-id="347d2-364">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="347d2-364">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="347d2-365">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-365">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-366">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-366">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="347d2-367">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-367">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-368">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-368">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="347d2-369">**Чтение** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-369">**Read** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="347d2-370">**Запись** (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-370">**Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

<span data-ttu-id="347d2-371">**Частичная запись** (5)</span><span class="sxs-lookup"><span data-stu-id="347d2-371">**Partial Write** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-372">**еррораддресс**</span><span class="sxs-lookup"><span data-stu-id="347d2-372">**ErrorAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-373">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="347d2-373">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-375">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,19 "," MIF. DMTF \| Memory Device \| 002,20 "," MIF. \|Массив физической памяти DMTF \| 001,14 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.19", "MIF.DMTF\|Memory Device\|002.20", "MIF.DMTF\|Physical Memory Array\|001.14")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-376">Адрес последней ошибки памяти.</span><span class="sxs-lookup"><span data-stu-id="347d2-376">Address of the last memory error.</span></span> <span data-ttu-id="347d2-377">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="347d2-377">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="347d2-378">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-378">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-379">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-379">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="347d2-380">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="347d2-380">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-381">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="347d2-381">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-382">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="347d2-382">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-384">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="347d2-384">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="347d2-385">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-386">**ErrorData**</span><span class="sxs-lookup"><span data-stu-id="347d2-386">**ErrorData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-387">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="347d2-387">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="347d2-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-389">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Device \| 002,17 "," MIF. \|Массив физической памяти DMTF \| 001,12 "), [**максимум**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="347d2-389">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.17", "MIF.DMTF\|Physical Memory Array\|001.12"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="347d2-390">Данные, захваченные во время последнего ошибочного доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="347d2-390">Data captured during the last erroneous memory access.</span></span> <span data-ttu-id="347d2-391">Данные занимают первые *n* октетов массива, необходимых для хранения числа битов, заданных свойством **еррортрансферсизе** .</span><span class="sxs-lookup"><span data-stu-id="347d2-391">The data occupies the first *n* octets of the array necessary to hold the number of bits specified by the **ErrorTransferSize** property.</span></span> <span data-ttu-id="347d2-392">Если **еррортрансферсизе** имеет значение 0, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-392">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="347d2-393">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-393">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-394">**еррордатаордер**</span><span class="sxs-lookup"><span data-stu-id="347d2-394">**ErrorDataOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-395">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-395">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-397">Упорядочивание данных, хранящихся в массиве **ErrorData** .</span><span class="sxs-lookup"><span data-stu-id="347d2-397">Ordering for data stored in the **ErrorData** array.</span></span> <span data-ttu-id="347d2-398">Если **еррортрансферсизе** имеет значение 0, это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-398">If **ErrorTransferSize** is 0, then this property has no meaning.</span></span>

<span data-ttu-id="347d2-399">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-399">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="347d2-400"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-401">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="347d2-401">Unknown.</span></span>

</dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="347d2-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Наименьший значащий байт первым** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-402"><span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>**Least Significant Byte First** (1)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-403">Сначала следует наименее значащий байт.</span><span class="sxs-lookup"><span data-stu-id="347d2-403">Least significant byte first.</span></span>

</dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

<span data-ttu-id="347d2-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Первый старший байт** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-404"><span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>**Most Significant Byte First** (2)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-405">Первый значащий байт.</span><span class="sxs-lookup"><span data-stu-id="347d2-405">Most significant byte first.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-406">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="347d2-406">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-407">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-408">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-409">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="347d2-409">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="347d2-410">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-410">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-411">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="347d2-411">**ErrorInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-412">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-414">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,12 "," MIF. \|Массив физической памяти DMTF \| 001,8 "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**Осереррордескриптион**")</span><span class="sxs-lookup"><span data-stu-id="347d2-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.12", "MIF.DMTF\|Physical Memory Array\|001.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**OtherErrorDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-415">Тип ошибки, которая возникла в последнее время.</span><span class="sxs-lookup"><span data-stu-id="347d2-415">Type of error that occurred most recently.</span></span> <span data-ttu-id="347d2-416">Значения 12-14 не определены в схеме CIM, так как семантика типа ошибки и вне зависимости от того, были ли они исправлены, смешиваются в DMI.</span><span class="sxs-lookup"><span data-stu-id="347d2-416">The values 12-14 are undefined in the CIM schema since the semantics of the type of error and whether or not it was correctable are mixed in DMI.</span></span> <span data-ttu-id="347d2-417">Свойство **корректаблиррор** указывает, было ли оно исправлено.</span><span class="sxs-lookup"><span data-stu-id="347d2-417">The **CorrectableError** property indicates whether it was correctable.</span></span>

<span data-ttu-id="347d2-418">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-418">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="347d2-419">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-419">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-420">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-420">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="347d2-421">**ОК** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-421">**OK** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

<span data-ttu-id="347d2-422">**Неправильное чтение** (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-422">**Bad Read** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

<span data-ttu-id="347d2-423">**Ошибка четности** (5)</span><span class="sxs-lookup"><span data-stu-id="347d2-423">**Parity Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

<span data-ttu-id="347d2-424">**Одноразрядная ошибка** (6)</span><span class="sxs-lookup"><span data-stu-id="347d2-424">**Single-Bit Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

<span data-ttu-id="347d2-425">**Ошибка в двух битах** (7)</span><span class="sxs-lookup"><span data-stu-id="347d2-425">**Double-Bit Error** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

<span data-ttu-id="347d2-426">**Многоразрядная ошибка** (8)</span><span class="sxs-lookup"><span data-stu-id="347d2-426">**Multi-Bit Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

<span data-ttu-id="347d2-427">**Ошибка в погрешностях** (9)</span><span class="sxs-lookup"><span data-stu-id="347d2-427">**Nibble Error** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

<span data-ttu-id="347d2-428">**Ошибка контрольной суммы** (10)</span><span class="sxs-lookup"><span data-stu-id="347d2-428">**Checksum Error** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

<span data-ttu-id="347d2-429">**Ошибка CRC** (11)</span><span class="sxs-lookup"><span data-stu-id="347d2-429">**CRC Error** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="347d2-430">Не **определено** (12)</span><span class="sxs-lookup"><span data-stu-id="347d2-430">**Undefined** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="347d2-431">Не **определено** (13)</span><span class="sxs-lookup"><span data-stu-id="347d2-431">**Undefined** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="347d2-432">Не **определено** (14)</span><span class="sxs-lookup"><span data-stu-id="347d2-432">**Undefined** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-433">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="347d2-433">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-436">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив физической памяти DMTF \| 001,7 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-436">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Memory Array\|001.7")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-437">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="347d2-437">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="347d2-438">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-438">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-439">**еррорресолутион**</span><span class="sxs-lookup"><span data-stu-id="347d2-439">**ErrorResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-440">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="347d2-440">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-442">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,21 "," MIF. \|Массив физической памяти DMTF \| 001,15 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="347d2-442">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.21", "MIF.DMTF\|Physical Memory Array\|001.15"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-443">Диапазон в байтах, до которого может быть разрешена Последняя ошибка.</span><span class="sxs-lookup"><span data-stu-id="347d2-443">Range, in bytes, to which the last error can be resolved.</span></span> <span data-ttu-id="347d2-444">Например, если адреса ошибок разрешаются в бит 11 (то есть на типичном уровне страницы), ошибки могут быть разрешены до 4 КБ, а значение этого свойства равно 4000.</span><span class="sxs-lookup"><span data-stu-id="347d2-444">For example, if error addresses are resolved to bit 11 (that is, on a typical page basis), then errors can be resolved to 4 KB boundaries and this property is set to 4000.</span></span> <span data-ttu-id="347d2-445">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-445">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-446">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-446">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="347d2-447">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="347d2-447">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-448">**ErrorTime**</span><span class="sxs-lookup"><span data-stu-id="347d2-448">**ErrorTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-449">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="347d2-449">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-450">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-451">Время, когда произошла последняя ошибка памяти.</span><span class="sxs-lookup"><span data-stu-id="347d2-451">Time that the last memory error occurred.</span></span> <span data-ttu-id="347d2-452">Тип ошибки описан в свойстве **errorInfo** .</span><span class="sxs-lookup"><span data-stu-id="347d2-452">The type of error is described by the **ErrorInfo** property.</span></span> <span data-ttu-id="347d2-453">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-453">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-454">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-454">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-455">**еррортрансферсизе**</span><span class="sxs-lookup"><span data-stu-id="347d2-455">**ErrorTransferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-456">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="347d2-456">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-458">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Memory Device \| 002,16 "," MIF. \|Массив физической памяти DMTF \| 001,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит ")</span><span class="sxs-lookup"><span data-stu-id="347d2-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Device\|002.16", "MIF.DMTF\|Physical Memory Array\|001.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-459">Размер передачи данных в битах, которая привела к последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="347d2-459">Size of the data transfer in bits that caused the last error.</span></span> <span data-ttu-id="347d2-460">значение 0 указывает на отсутствие ошибки.</span><span class="sxs-lookup"><span data-stu-id="347d2-460">0 indicates no error.</span></span> <span data-ttu-id="347d2-461">Если свойство **errorInfo** равно 3, «ОК», то этому свойству должно быть присвоено значение 0.</span><span class="sxs-lookup"><span data-stu-id="347d2-461">If the **ErrorInfo** property is equal to 3, "OK", then this property should be set to 0.</span></span>

<span data-ttu-id="347d2-462">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-462">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-463">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="347d2-463">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-464">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="347d2-464">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-466">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="347d2-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-467">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="347d2-467">Date and time the object was installed.</span></span> <span data-ttu-id="347d2-468">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="347d2-468">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="347d2-469">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-469">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-470">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="347d2-470">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-471">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="347d2-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-473">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="347d2-473">Last error code reported by the logical device.</span></span>

<span data-ttu-id="347d2-474">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-475">**Name**</span><span class="sxs-lookup"><span data-stu-id="347d2-475">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-476">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-478">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="347d2-478">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-479">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="347d2-479">Label by which the object is known.</span></span> <span data-ttu-id="347d2-480">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="347d2-480">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="347d2-481">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-481">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-482">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="347d2-482">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-483">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="347d2-483">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-484">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-484">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-485">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="347d2-485">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-486">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="347d2-486">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="347d2-487">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="347d2-487">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="347d2-488">Если **значение параметра DataSize равно 1** (один), то это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="347d2-488">If the value of **BlockSize** is 1 (one), then this property is the total size of the storage extent.</span></span>

<span data-ttu-id="347d2-489">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-489">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="347d2-490">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="347d2-490">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-491">**осереррордескриптион**</span><span class="sxs-lookup"><span data-stu-id="347d2-491">**OtherErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-492">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-492">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-493">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-493">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-494">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ память CIM**](cim-memory.md)".**ErrorInfo**")</span><span class="sxs-lookup"><span data-stu-id="347d2-494">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Memory**](cim-memory.md).**ErrorInfo**")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-495">Произвольная строка, которая предоставляет дополнительные сведения, если свойство **ErrorType** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="347d2-495">Free-form string that provides additional information if the **ErrorType** property is set to 1 ("Other").</span></span> <span data-ttu-id="347d2-496">Если значение, отличное от 1 (одно), эта строка не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-496">If a value other than 1 (one), this string has no meaning.</span></span>

<span data-ttu-id="347d2-497">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-497">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-498">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="347d2-498">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-499">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-500">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-500">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-501">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="347d2-501">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-502">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-502">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="347d2-503">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="347d2-504">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="347d2-504">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="347d2-505">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="347d2-505">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-506">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="347d2-506">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="347d2-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-508">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="347d2-508">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="347d2-509">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-509">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="347d2-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="347d2-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-511"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="347d2-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-512"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="347d2-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-513"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-514">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="347d2-514">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="347d2-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-515"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-516">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="347d2-516">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="347d2-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="347d2-517"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-518">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="347d2-518">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="347d2-519">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="347d2-519">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="347d2-520">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="347d2-520">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="347d2-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="347d2-521"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-522">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="347d2-522">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="347d2-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="347d2-523"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="347d2-524">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="347d2-524">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-525">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="347d2-525">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-526">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="347d2-526">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-527">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-528">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="347d2-528">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="347d2-529">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="347d2-529">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="347d2-530">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="347d2-530">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="347d2-531">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="347d2-531">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="347d2-532">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-532">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-533">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="347d2-533">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-534">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-534">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-535">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-535">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-536">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="347d2-536">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="347d2-537">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-537">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-538">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="347d2-538">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-539">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="347d2-539">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-540">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-540">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-541">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Массив памяти DMTF, сопоставленный адресам \| 001,3 "," MIF. \|Сопоставленные адреса памяти \| в формате DMTF 001,4 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="347d2-541">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Array Mapped Addresses\|001.3", "MIF.DMTF\|Memory Device Mapped Addresses\|001.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-542">Начальный адрес, на который ссылается приложение или операционная система, сопоставленный контроллером памяти для объекта памяти.</span><span class="sxs-lookup"><span data-stu-id="347d2-542">Beginning address, referenced by an application or operating system and mapped by a memory controller, for the memory object.</span></span> <span data-ttu-id="347d2-543">Начальный адрес указывается в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="347d2-543">The starting address is specified in kilobytes.</span></span>

<span data-ttu-id="347d2-544">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-544">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="347d2-545">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="347d2-545">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-546">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="347d2-546">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-547">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-549">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="347d2-549">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-550">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="347d2-550">Current status of the object.</span></span> <span data-ttu-id="347d2-551">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-551">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="347d2-552">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="347d2-552">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="347d2-553">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="347d2-553">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="347d2-554">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="347d2-554">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="347d2-555">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="347d2-555">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-556">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="347d2-556">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="347d2-557">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="347d2-557">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="347d2-558">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="347d2-558">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="347d2-559">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="347d2-559">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="347d2-560">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="347d2-560">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="347d2-561">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="347d2-561">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="347d2-562">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="347d2-562">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="347d2-563">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="347d2-563">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="347d2-564">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="347d2-564">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-565">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="347d2-565">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-566">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="347d2-566">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-567">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-568">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="347d2-568">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="347d2-569">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="347d2-569">State of the logical device.</span></span> <span data-ttu-id="347d2-570">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="347d2-570">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="347d2-571">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-571">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="347d2-572">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="347d2-572">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="347d2-573">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="347d2-573">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="347d2-574">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="347d2-574">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="347d2-575">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="347d2-575">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="347d2-576">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="347d2-576">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="347d2-577">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="347d2-577">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-578">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-579">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-580">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="347d2-580">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="347d2-581">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="347d2-581">Scoping system's creation class name.</span></span>

<span data-ttu-id="347d2-582">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-582">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-583">**системлевеладдресс**</span><span class="sxs-lookup"><span data-stu-id="347d2-583">**SystemLevelAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-584">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="347d2-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-585">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-585">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="347d2-586">Если **значение — true**, сведения об адресе в свойстве **еррораддресс** являются адресом системного уровня; Если **значение равно false**, это физический адрес.</span><span class="sxs-lookup"><span data-stu-id="347d2-586">If **TRUE**, the address information in the **ErrorAddress** property is a system-level address; if **FALSE**, it is a physical address.</span></span> <span data-ttu-id="347d2-587">Если свойство **errorInfo** равно 3 ("ОК"), это свойство не имеет смысла.</span><span class="sxs-lookup"><span data-stu-id="347d2-587">If the **ErrorInfo** property is equal to 3 ("OK"), then this property has no meaning.</span></span>

<span data-ttu-id="347d2-588">Это свойство наследуется [**от \_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-588">This property is inherited from [**CIM\_Memory**](cim-memory.md).</span></span>

</dd> <dt>

<span data-ttu-id="347d2-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="347d2-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="347d2-590">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="347d2-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="347d2-591">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="347d2-591">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="347d2-592">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="347d2-592">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="347d2-593">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="347d2-593">Scoping system's name.</span></span>

<span data-ttu-id="347d2-594">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="347d2-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="347d2-595">Комментарии</span><span class="sxs-lookup"><span data-stu-id="347d2-595">Remarks</span></span>

<span data-ttu-id="347d2-596">Класс **CIM \_ волатилестораже** является производным от [**\_ памяти CIM**](cim-memory.md).</span><span class="sxs-lookup"><span data-stu-id="347d2-596">The **CIM\_VolatileStorage** class is derived from [**CIM\_Memory**](cim-memory.md).</span></span>

<span data-ttu-id="347d2-597">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="347d2-597">WMI does not implement this class.</span></span>

<span data-ttu-id="347d2-598">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="347d2-598">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="347d2-599">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="347d2-599">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="347d2-600">Требования</span><span class="sxs-lookup"><span data-stu-id="347d2-600">Requirements</span></span>



| <span data-ttu-id="347d2-601">Требование</span><span class="sxs-lookup"><span data-stu-id="347d2-601">Requirement</span></span> | <span data-ttu-id="347d2-602">Значение</span><span class="sxs-lookup"><span data-stu-id="347d2-602">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="347d2-603">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="347d2-603">Minimum supported client</span></span><br/> | <span data-ttu-id="347d2-604">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="347d2-604">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="347d2-605">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="347d2-605">Minimum supported server</span></span><br/> | <span data-ttu-id="347d2-606">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="347d2-606">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="347d2-607">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="347d2-607">Namespace</span></span><br/>                | <span data-ttu-id="347d2-608">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="347d2-608">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="347d2-609">MOF</span><span class="sxs-lookup"><span data-stu-id="347d2-609">MOF</span></span><br/>                      | <dl> <span data-ttu-id="347d2-610"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="347d2-610"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="347d2-611">DLL</span><span class="sxs-lookup"><span data-stu-id="347d2-611">DLL</span></span><br/>                      | <dl> <span data-ttu-id="347d2-612"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="347d2-612"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="347d2-613">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="347d2-613">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347d2-614">**\_Память CIM**</span><span class="sxs-lookup"><span data-stu-id="347d2-614">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> </dl>

 

