---
description: Класс CIM \_ дискдриве представляет физический диск, отображаемый операционной системой.
ms.assetid: 3a63506e-455e-4108-b0c7-03b2af249d61
ms.tgt_platform: multiple
title: Класс CIM_DiskDrive (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskDrive
- CIM_DiskDrive.Availability
- CIM_DiskDrive.Capabilities
- CIM_DiskDrive.CapabilityDescriptions
- CIM_DiskDrive.Caption
- CIM_DiskDrive.CompressionMethod
- CIM_DiskDrive.ConfigManagerErrorCode
- CIM_DiskDrive.ConfigManagerUserConfig
- CIM_DiskDrive.CreationClassName
- CIM_DiskDrive.DefaultBlockSize
- CIM_DiskDrive.Description
- CIM_DiskDrive.DeviceID
- CIM_DiskDrive.ErrorCleared
- CIM_DiskDrive.ErrorDescription
- CIM_DiskDrive.ErrorMethodology
- CIM_DiskDrive.InstallDate
- CIM_DiskDrive.LastErrorCode
- CIM_DiskDrive.MaxBlockSize
- CIM_DiskDrive.MaxMediaSize
- CIM_DiskDrive.MinBlockSize
- CIM_DiskDrive.Name
- CIM_DiskDrive.NeedsCleaning
- CIM_DiskDrive.NumberOfMediaSupported
- CIM_DiskDrive.PNPDeviceID
- CIM_DiskDrive.PowerManagementCapabilities
- CIM_DiskDrive.PowerManagementSupported
- CIM_DiskDrive.Status
- CIM_DiskDrive.StatusInfo
- CIM_DiskDrive.SystemCreationClassName
- CIM_DiskDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c68e8fc53898220737f473cc0c13f43d7ad471b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262707"
---
# <a name="cim_diskdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="4a231-103">Класс CIM_DiskDrive (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4a231-103">CIM_DiskDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4a231-104">Класс **CIM \_ дискдриве** представляет физический диск, отображаемый операционной системой.</span><span class="sxs-lookup"><span data-stu-id="4a231-104">The **CIM\_DiskDrive** class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="4a231-105">Функции дискового накопителя соответствуют логическим характеристикам управления диска и, в некоторых случаях, могут не отражать физические характеристики устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-105">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="4a231-106">Интерфейс к физическому диску является членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="4a231-106">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="4a231-107">Однако объект, основанный на другом логическом устройстве, не является членом этого класса.</span><span class="sxs-lookup"><span data-stu-id="4a231-107">However, an object based on another logical device is not a member of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4a231-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4a231-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4a231-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4a231-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4a231-110">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4a231-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4a231-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4a231-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a231-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a231-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="4a231-113">Члены</span><span class="sxs-lookup"><span data-stu-id="4a231-113">Members</span></span>

<span data-ttu-id="4a231-114">Класс **CIM \_ дискдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4a231-114">The **CIM\_DiskDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="4a231-115">Методы</span><span class="sxs-lookup"><span data-stu-id="4a231-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="4a231-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="4a231-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4a231-117">Методы</span><span class="sxs-lookup"><span data-stu-id="4a231-117">Methods</span></span>

<span data-ttu-id="4a231-118">Класс **CIM \_ дискдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4a231-118">The **CIM\_DiskDrive** class has these methods.</span></span>



| <span data-ttu-id="4a231-119">Метод</span><span class="sxs-lookup"><span data-stu-id="4a231-119">Method</span></span>                                                                | <span data-ttu-id="4a231-120">Описание</span><span class="sxs-lookup"><span data-stu-id="4a231-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a231-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="4a231-121">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="4a231-122">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="4a231-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4a231-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="4a231-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4a231-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="4a231-125">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="4a231-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="4a231-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="4a231-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4a231-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="4a231-127">Properties</span></span>

<span data-ttu-id="4a231-128">Класс **CIM \_ дискдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4a231-128">The **CIM\_DiskDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4a231-129">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="4a231-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4a231-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="4a231-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-133">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-133">Availability and status of the device.</span></span>

<span data-ttu-id="4a231-134">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4a231-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4a231-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-136">Другое</span><span class="sxs-lookup"><span data-stu-id="4a231-136">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4a231-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="4a231-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-138">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="4a231-138">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4a231-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="4a231-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-140">Работа или полная мощность.</span><span class="sxs-lookup"><span data-stu-id="4a231-140">Running/full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4a231-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="4a231-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-142">Внимание!</span><span class="sxs-lookup"><span data-stu-id="4a231-142">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4a231-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="4a231-143"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-144">Тестирование.</span><span class="sxs-lookup"><span data-stu-id="4a231-144">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4a231-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="4a231-145"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-146">Не применяется</span><span class="sxs-lookup"><span data-stu-id="4a231-146">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4a231-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="4a231-147"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-148">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="4a231-148">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4a231-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="4a231-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-150">Вне сети.</span><span class="sxs-lookup"><span data-stu-id="4a231-150">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4a231-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="4a231-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-152">Не обслуживает.</span><span class="sxs-lookup"><span data-stu-id="4a231-152">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4a231-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="4a231-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-154">"Пониженная функциональность".</span><span class="sxs-lookup"><span data-stu-id="4a231-154">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4a231-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="4a231-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-156">Не установлено.</span><span class="sxs-lookup"><span data-stu-id="4a231-156">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4a231-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="4a231-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-158">Ошибка установки.</span><span class="sxs-lookup"><span data-stu-id="4a231-158">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4a231-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="4a231-159"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-160">Известно, что устройство находится в режиме энергосбережения, но его точное состояние в этом режиме неизвестно.</span><span class="sxs-lookup"><span data-stu-id="4a231-160">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4a231-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="4a231-161"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-162">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="4a231-162">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4a231-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="4a231-163"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-164">Устройство не работает, но его можно быстро включить в полный режим.</span><span class="sxs-lookup"><span data-stu-id="4a231-164">Device is not functioning but could be brought to full power 'quickly'.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4a231-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="4a231-165"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-166">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="4a231-166">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4a231-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="4a231-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-168">Устройство находится в состоянии предупреждения, а также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="4a231-168">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4a231-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="4a231-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-170">приостановлено</span><span class="sxs-lookup"><span data-stu-id="4a231-170">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4a231-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="4a231-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-172">Не готово.</span><span class="sxs-lookup"><span data-stu-id="4a231-172">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4a231-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="4a231-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-174">не настроено.</span><span class="sxs-lookup"><span data-stu-id="4a231-174">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4a231-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="4a231-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-176">Диск недоступен.</span><span class="sxs-lookup"><span data-stu-id="4a231-176">The disk drive is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-177">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="4a231-177">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-178">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4a231-178">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4a231-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-180">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="4a231-180">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-181">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="4a231-181">Capabilities of the media access device.</span></span> <span data-ttu-id="4a231-182">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-182">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4a231-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4a231-183"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-184">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="4a231-184">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4a231-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4a231-185"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-186">Другое</span><span class="sxs-lookup"><span data-stu-id="4a231-186">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="4a231-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="4a231-187"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-188">Последовательный доступ.</span><span class="sxs-lookup"><span data-stu-id="4a231-188">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="4a231-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="4a231-189"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-190">Произвольный доступ.</span><span class="sxs-lookup"><span data-stu-id="4a231-190">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="4a231-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="4a231-191"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-192">Запись.</span><span class="sxs-lookup"><span data-stu-id="4a231-192">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="4a231-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="4a231-193"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-194">Шифрование.</span><span class="sxs-lookup"><span data-stu-id="4a231-194">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="4a231-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="4a231-195"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-196">Сжатие.</span><span class="sxs-lookup"><span data-stu-id="4a231-196">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="4a231-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="4a231-197"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-198">Съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="4a231-198">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="4a231-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="4a231-199"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-200">Очистка вручную.</span><span class="sxs-lookup"><span data-stu-id="4a231-200">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="4a231-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="4a231-201"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-202">Автоматическая очистка.</span><span class="sxs-lookup"><span data-stu-id="4a231-202">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="4a231-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="4a231-203"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-204">ИНТЕЛЛЕКТУАЛЬНое уведомление.</span><span class="sxs-lookup"><span data-stu-id="4a231-204">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="4a231-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="4a231-205"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-206">Различает устройство, которое может получить доступ к обеим сторонам двусторонних носителей с устройства, которое считывает только одну сторону и требует включения носителя.</span><span class="sxs-lookup"><span data-stu-id="4a231-206">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="4a231-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="4a231-207"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-208">Указывает, что носитель не обязательно должен быть явно извлечен с устройства перед обращением к элементу выбора.</span><span class="sxs-lookup"><span data-stu-id="4a231-208">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-209">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="4a231-209">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-210">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="4a231-210">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4a231-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-212">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="4a231-212">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-213">Массив строк произвольной формы, которые содержат подробные пояснения для доступа к функциям устройств, указанным в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="4a231-213">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="4a231-214">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

> [!Note]  
> <span data-ttu-id="4a231-215">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="4a231-215">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="4a231-216">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="4a231-216">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-219">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4a231-219">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-220">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4a231-220">Short textual description of the object.</span></span>

<span data-ttu-id="4a231-221">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-221">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-222">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="4a231-222">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-225">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="4a231-225">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="4a231-226">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="4a231-226">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="4a231-227">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="4a231-227">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="4a231-228">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="4a231-228">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="4a231-229">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-229">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="4a231-230">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="4a231-230">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="4a231-231">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="4a231-231">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="4a231-232">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="4a231-232">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="4a231-233">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="4a231-233">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="4a231-234">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="4a231-234">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="4a231-235">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="4a231-235">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-236">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="4a231-236">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-237">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4a231-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-239">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4a231-239">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-240">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4a231-240">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="4a231-241">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-241">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4a231-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="4a231-242"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4a231-243"> (0)</span><span class="sxs-lookup"><span data-stu-id="4a231-243">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-244">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="4a231-244">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4a231-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="4a231-245"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4a231-246">(1)</span><span class="sxs-lookup"><span data-stu-id="4a231-246">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-247">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="4a231-247">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4a231-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-248"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4a231-249">(2)</span><span class="sxs-lookup"><span data-stu-id="4a231-249">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4a231-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="4a231-250"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4a231-251">(3)</span><span class="sxs-lookup"><span data-stu-id="4a231-251">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-252">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4a231-252">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4a231-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="4a231-253"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4a231-254">(4)</span><span class="sxs-lookup"><span data-stu-id="4a231-254">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-255">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="4a231-255">Device is not working properly.</span></span> <span data-ttu-id="4a231-256">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="4a231-256">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4a231-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="4a231-257"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4a231-258">(5)</span><span class="sxs-lookup"><span data-stu-id="4a231-258">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-259">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="4a231-259">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4a231-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="4a231-260"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4a231-261"> (6)</span><span class="sxs-lookup"><span data-stu-id="4a231-261">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-262">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="4a231-262">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4a231-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="4a231-263"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4a231-264">(7)</span><span class="sxs-lookup"><span data-stu-id="4a231-264">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4a231-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-265"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4a231-266">(8)</span><span class="sxs-lookup"><span data-stu-id="4a231-266">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-267">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-267">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4a231-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-268"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4a231-269">(9)</span><span class="sxs-lookup"><span data-stu-id="4a231-269">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-270">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-270">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4a231-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="4a231-271"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4a231-272">(10)</span><span class="sxs-lookup"><span data-stu-id="4a231-272">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-273">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="4a231-273">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4a231-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-274"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4a231-275">(11)</span><span class="sxs-lookup"><span data-stu-id="4a231-275">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-276">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-276">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4a231-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="4a231-277"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4a231-278">(12)</span><span class="sxs-lookup"><span data-stu-id="4a231-278">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-279">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="4a231-279">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4a231-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-280"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4a231-281">(13)</span><span class="sxs-lookup"><span data-stu-id="4a231-281">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-282">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-282">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4a231-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="4a231-283"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4a231-284">(14)</span><span class="sxs-lookup"><span data-stu-id="4a231-284">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-285">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="4a231-285">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4a231-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="4a231-286"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4a231-287">(15)</span><span class="sxs-lookup"><span data-stu-id="4a231-287">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-288">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="4a231-288">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4a231-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="4a231-289"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4a231-290">(16)</span><span class="sxs-lookup"><span data-stu-id="4a231-290">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-291">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="4a231-291">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4a231-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="4a231-292"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4a231-293">(17)</span><span class="sxs-lookup"><span data-stu-id="4a231-293">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-294">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4a231-294">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4a231-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-295"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4a231-296">(18)</span><span class="sxs-lookup"><span data-stu-id="4a231-296">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-297">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="4a231-297">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4a231-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="4a231-298"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4a231-299">(19)</span><span class="sxs-lookup"><span data-stu-id="4a231-299">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4a231-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="4a231-300"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4a231-301">(20)</span><span class="sxs-lookup"><span data-stu-id="4a231-301">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-302">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="4a231-302">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4a231-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="4a231-303"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4a231-304">(21)</span><span class="sxs-lookup"><span data-stu-id="4a231-304">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-305">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="4a231-305">System failure.</span></span> <span data-ttu-id="4a231-306">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="4a231-306">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4a231-307">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="4a231-307">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4a231-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="4a231-308"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4a231-309">(22)</span><span class="sxs-lookup"><span data-stu-id="4a231-309">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-310">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="4a231-310">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4a231-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="4a231-311"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4a231-312">(23)</span><span class="sxs-lookup"><span data-stu-id="4a231-312">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-313">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="4a231-313">System failure.</span></span> <span data-ttu-id="4a231-314">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="4a231-314">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4a231-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="4a231-315"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4a231-316">(24)</span><span class="sxs-lookup"><span data-stu-id="4a231-316">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-317">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="4a231-317">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4a231-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="4a231-318"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4a231-319">(25)</span><span class="sxs-lookup"><span data-stu-id="4a231-319">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-320">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="4a231-320">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4a231-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="4a231-321"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4a231-322">(26)</span><span class="sxs-lookup"><span data-stu-id="4a231-322">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-323">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="4a231-323">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4a231-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="4a231-324"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4a231-325">(27)</span><span class="sxs-lookup"><span data-stu-id="4a231-325">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-326">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="4a231-326">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4a231-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="4a231-327"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4a231-328">(28)</span><span class="sxs-lookup"><span data-stu-id="4a231-328">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-329">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="4a231-329">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4a231-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="4a231-330"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4a231-331">(29)</span><span class="sxs-lookup"><span data-stu-id="4a231-331">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-332">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="4a231-332">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4a231-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="4a231-333"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4a231-334">(30)</span><span class="sxs-lookup"><span data-stu-id="4a231-334">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-335">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="4a231-335">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4a231-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4a231-336"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4a231-337">1-31</span><span class="sxs-lookup"><span data-stu-id="4a231-337">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-338">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="4a231-338">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-339">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="4a231-339">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-340">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4a231-340">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-342">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4a231-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-343">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4a231-343">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4a231-344">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-345">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4a231-345">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-348">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4a231-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a231-349">Имя класса (или подкласса), используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4a231-349">Name of the class (or subclass) used in the creation of an instance.</span></span> <span data-ttu-id="4a231-350">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="4a231-350">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4a231-351">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-352">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="4a231-352">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-353">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4a231-353">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-355">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="4a231-355">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-356">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="4a231-356">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="4a231-357">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-357">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="4a231-358">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4a231-358">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-359">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4a231-359">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-362">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="4a231-362">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-363">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4a231-363">Textual description of the object.</span></span>

<span data-ttu-id="4a231-364">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-364">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-365">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4a231-365">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-366">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-368">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4a231-368">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a231-369">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-369">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="4a231-370">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-371">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="4a231-371">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-372">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4a231-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-374">Если **значение равно true**, то ошибка, указанная в свойстве **ластерроркоде** , удаляется.</span><span class="sxs-lookup"><span data-stu-id="4a231-374">If **TRUE**, the error reported in the **LastErrorCode** property is cleared.</span></span>

<span data-ttu-id="4a231-375">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-376">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4a231-376">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-377">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-379">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="4a231-379">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="4a231-380">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-380">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-381">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="4a231-381">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-384">Произвольная строка, описывающая тип обнаружения и исправления ошибок, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="4a231-384">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="4a231-385">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-385">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-386">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4a231-386">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-387">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4a231-387">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-389">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="4a231-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-390">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="4a231-390">Date and time when the object was installed.</span></span> <span data-ttu-id="4a231-391">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="4a231-391">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4a231-392">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-393">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="4a231-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-394">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4a231-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-396">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="4a231-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4a231-397">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-398">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="4a231-398">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-399">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4a231-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-401">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="4a231-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-402">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="4a231-402">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="4a231-403">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="4a231-404">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4a231-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-405">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="4a231-405">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-406">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4a231-406">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-408">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="4a231-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-409">Максимальный размер носителя, поддерживаемого устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="4a231-409">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="4a231-410">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="4a231-410">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="4a231-411">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-411">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="4a231-412">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4a231-412">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-413">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="4a231-413">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-414">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4a231-414">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-415">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-416">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="4a231-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-417">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="4a231-417">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="4a231-418">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-418">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="4a231-419">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="4a231-419">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-420">**Name**</span><span class="sxs-lookup"><span data-stu-id="4a231-420">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-423">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="4a231-423">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-424">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="4a231-424">Label by which the object is known.</span></span> <span data-ttu-id="4a231-425">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="4a231-425">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4a231-426">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-426">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-427">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="4a231-427">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-428">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4a231-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-430">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="4a231-430">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="4a231-431">Возможность ручной или автоматической очистки указывается в свойстве массива **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="4a231-431">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="4a231-432">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-432">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-433">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="4a231-433">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-434">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4a231-434">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-435">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-436">Если устройство доступа к носителю поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может быть поддерживается или вставлено.</span><span class="sxs-lookup"><span data-stu-id="4a231-436">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="4a231-437">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-437">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-438">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4a231-438">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-441">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4a231-441">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-442">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-442">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4a231-443">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-443">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4a231-444">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4a231-444">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4a231-445">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="4a231-445">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-446">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4a231-446">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4a231-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-448">Конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="4a231-448">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="4a231-449">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-449">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4a231-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4a231-450"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-451">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="4a231-451">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4a231-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="4a231-452"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-453">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4a231-453">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4a231-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="4a231-454"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-455">Отключена.</span><span class="sxs-lookup"><span data-stu-id="4a231-455">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4a231-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="4a231-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-457">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="4a231-457">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4a231-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="4a231-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-459">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="4a231-459">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4a231-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="4a231-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-461">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="4a231-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4a231-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="4a231-462"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-463">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="4a231-463">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4a231-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="4a231-464"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4a231-465">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="4a231-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-diskdrive.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-466">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="4a231-466">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-467">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4a231-467">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-468">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4a231-469">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="4a231-469">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="4a231-470">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="4a231-470">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="4a231-471">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="4a231-471">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="4a231-472">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="4a231-472">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="4a231-473">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-474">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="4a231-474">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-475">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-477">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="4a231-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-478">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="4a231-478">Current status of the object.</span></span>

<span data-ttu-id="4a231-479">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-479">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4a231-480">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="4a231-480">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4a231-481">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="4a231-481">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4a231-482">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="4a231-482">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4a231-483">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="4a231-483">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4a231-484">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="4a231-484">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4a231-485">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="4a231-485">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4a231-486">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="4a231-486">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4a231-487">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="4a231-487">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4a231-488">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="4a231-488">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4a231-489">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="4a231-489">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4a231-490">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="4a231-490">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4a231-491">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="4a231-491">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4a231-492">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="4a231-492">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-493">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4a231-493">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-494">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4a231-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-495">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-495">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-496">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4a231-496">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4a231-497">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4a231-497">State of the logical device.</span></span> <span data-ttu-id="4a231-498">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="4a231-498">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4a231-499">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-499">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4a231-500">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4a231-500">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4a231-501">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="4a231-501">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4a231-502">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="4a231-502">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4a231-503">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="4a231-503">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4a231-504">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="4a231-504">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4a231-505">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="4a231-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-506">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-508">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4a231-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a231-509">Свойство свойства **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="4a231-509">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="4a231-510">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4a231-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4a231-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a231-512">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4a231-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4a231-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4a231-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4a231-514">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4a231-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4a231-515">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="4a231-515">Scoping system's **Name** property.</span></span>

<span data-ttu-id="4a231-516">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4a231-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a231-517">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a231-517">Remarks</span></span>

<span data-ttu-id="4a231-518">Класс **CIM \_ дискдриве** является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="4a231-518">The **CIM\_DiskDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="4a231-519">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4a231-519">WMI does not implement this class.</span></span> <span data-ttu-id="4a231-520">См. раздел [Классы Win32](win32-provider.md) для классов, производных от **CIM \_ дискдриве**.</span><span class="sxs-lookup"><span data-stu-id="4a231-520">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_DiskDrive**.</span></span>

<span data-ttu-id="4a231-521">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4a231-521">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4a231-522">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4a231-522">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a231-523">Требования</span><span class="sxs-lookup"><span data-stu-id="4a231-523">Requirements</span></span>



| <span data-ttu-id="4a231-524">Требование</span><span class="sxs-lookup"><span data-stu-id="4a231-524">Requirement</span></span> | <span data-ttu-id="4a231-525">Значение</span><span class="sxs-lookup"><span data-stu-id="4a231-525">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a231-526">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a231-526">Minimum supported client</span></span><br/> | <span data-ttu-id="4a231-527">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a231-527">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4a231-528">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a231-528">Minimum supported server</span></span><br/> | <span data-ttu-id="4a231-529">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a231-529">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4a231-530">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4a231-530">Namespace</span></span><br/>                | <span data-ttu-id="4a231-531">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4a231-531">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4a231-532">MOF</span><span class="sxs-lookup"><span data-stu-id="4a231-532">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a231-533"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a231-533"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a231-534">DLL</span><span class="sxs-lookup"><span data-stu-id="4a231-534">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a231-535"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a231-535"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a231-536">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a231-536">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a231-537">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="4a231-537">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

