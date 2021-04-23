---
description: Класс CIM \_ -класса представляет собой аппаратную сущность, которая может быть или не реализована в физическом оборудовании.
ms.assetid: 4f3d38ff-8080-4b53-ae29-82b68558c550
ms.tgt_platform: multiple
title: Класс CIM_LogicalDevice (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.Caption
- CIM_LogicalDevice.Description
- CIM_LogicalDevice.InstallDate
- CIM_LogicalDevice.Name
- CIM_LogicalDevice.Status
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.ConfigManagerErrorCode
- CIM_LogicalDevice.ConfigManagerUserConfig
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.PNPDeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49974b966e1378350e8e5475ef14bb092b3aaea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141701"
---
# <a name="cim_logicaldevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="68acc-103">Класс CIM_LogicalDevice (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="68acc-103">CIM_LogicalDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="68acc-104">Класс **CIM \_** -класса представляет собой аппаратную сущность, которая может быть или не реализована в физическом оборудовании.</span><span class="sxs-lookup"><span data-stu-id="68acc-104">The **CIM\_LogicalDevice** class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68acc-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="68acc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="68acc-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="68acc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="68acc-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="68acc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="68acc-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="68acc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68acc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68acc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C529-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDevice : CIM_LogicalElement
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
};
```

## <a name="members"></a><span data-ttu-id="68acc-110">Члены</span><span class="sxs-lookup"><span data-stu-id="68acc-110">Members</span></span>

<span data-ttu-id="68acc-111">Класс **класса \_ CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="68acc-111">The **CIM\_LogicalDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="68acc-112">Методы</span><span class="sxs-lookup"><span data-stu-id="68acc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="68acc-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="68acc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68acc-114">Методы</span><span class="sxs-lookup"><span data-stu-id="68acc-114">Methods</span></span>

<span data-ttu-id="68acc-115">Класс **класса \_ CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="68acc-115">The **CIM\_LogicalDevice** class has these methods.</span></span>



| <span data-ttu-id="68acc-116">Метод</span><span class="sxs-lookup"><span data-stu-id="68acc-116">Method</span></span>                                                                   | <span data-ttu-id="68acc-117">Описание</span><span class="sxs-lookup"><span data-stu-id="68acc-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68acc-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="68acc-118">**Reset**</span></span>](reset-method-in-class-cim-logicaldevice.md)                 | <span data-ttu-id="68acc-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="68acc-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="68acc-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="68acc-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="68acc-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="68acc-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldevice.md) | <span data-ttu-id="68acc-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="68acc-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="68acc-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="68acc-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68acc-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="68acc-124">Properties</span></span>

<span data-ttu-id="68acc-125">Класс **класса \_ CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="68acc-125">The **CIM\_LogicalDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68acc-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="68acc-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68acc-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="68acc-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="68acc-130">Availability and status of the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68acc-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="68acc-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68acc-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="68acc-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="68acc-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="68acc-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="68acc-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="68acc-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="68acc-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="68acc-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="68acc-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="68acc-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="68acc-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="68acc-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="68acc-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="68acc-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="68acc-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="68acc-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68acc-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="68acc-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="68acc-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="68acc-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="68acc-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="68acc-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="68acc-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="68acc-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="68acc-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="68acc-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="68acc-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="68acc-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="68acc-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="68acc-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="68acc-148">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="68acc-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="68acc-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="68acc-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="68acc-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="68acc-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="68acc-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="68acc-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="68acc-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="68acc-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="68acc-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="68acc-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="68acc-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="68acc-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="68acc-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="68acc-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="68acc-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="68acc-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68acc-160">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="68acc-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-163">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="68acc-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-164">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="68acc-164">A short textual description of the object.</span></span>

<span data-ttu-id="68acc-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68acc-166">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="68acc-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68acc-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-169">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="68acc-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-170">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="68acc-170">Win32 Configuration Manager error code.</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="68acc-171">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="68acc-171">**This device is working properly.**</span></span> <span data-ttu-id="68acc-172"> (0)</span><span class="sxs-lookup"><span data-stu-id="68acc-172">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="68acc-173">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="68acc-173">**This device is not configured correctly.**</span></span> <span data-ttu-id="68acc-174">(1)</span><span class="sxs-lookup"><span data-stu-id="68acc-174">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="68acc-175">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-175">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="68acc-176">(2)</span><span class="sxs-lookup"><span data-stu-id="68acc-176">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="68acc-177">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="68acc-177">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="68acc-178">(3)</span><span class="sxs-lookup"><span data-stu-id="68acc-178">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="68acc-179">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="68acc-179">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="68acc-180">(4)</span><span class="sxs-lookup"><span data-stu-id="68acc-180">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="68acc-181">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="68acc-181">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="68acc-182">(5)</span><span class="sxs-lookup"><span data-stu-id="68acc-182">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="68acc-183">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="68acc-183">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="68acc-184"> (6)</span><span class="sxs-lookup"><span data-stu-id="68acc-184">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="68acc-185">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="68acc-185">**Cannot filter.**</span></span> <span data-ttu-id="68acc-186">(7)</span><span class="sxs-lookup"><span data-stu-id="68acc-186">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="68acc-187">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-187">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="68acc-188">(8)</span><span class="sxs-lookup"><span data-stu-id="68acc-188">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="68acc-189">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-189">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="68acc-190">(9)</span><span class="sxs-lookup"><span data-stu-id="68acc-190">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="68acc-191">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="68acc-191">**This device cannot start.**</span></span> <span data-ttu-id="68acc-192">(10)</span><span class="sxs-lookup"><span data-stu-id="68acc-192">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="68acc-193">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-193">**This device failed.**</span></span> <span data-ttu-id="68acc-194">(11)</span><span class="sxs-lookup"><span data-stu-id="68acc-194">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="68acc-195">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="68acc-195">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="68acc-196">(12)</span><span class="sxs-lookup"><span data-stu-id="68acc-196">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="68acc-197">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-197">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="68acc-198">(13)</span><span class="sxs-lookup"><span data-stu-id="68acc-198">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="68acc-199">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="68acc-199">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="68acc-200">(14)</span><span class="sxs-lookup"><span data-stu-id="68acc-200">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="68acc-201">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="68acc-201">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="68acc-202">(15)</span><span class="sxs-lookup"><span data-stu-id="68acc-202">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="68acc-203">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="68acc-203">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="68acc-204">(16)</span><span class="sxs-lookup"><span data-stu-id="68acc-204">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="68acc-205">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="68acc-205">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="68acc-206">(17)</span><span class="sxs-lookup"><span data-stu-id="68acc-206">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="68acc-207">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-207">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="68acc-208">(18)</span><span class="sxs-lookup"><span data-stu-id="68acc-208">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="68acc-209">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="68acc-209">**Failure using the VxD loader.**</span></span> <span data-ttu-id="68acc-210">(19)</span><span class="sxs-lookup"><span data-stu-id="68acc-210">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="68acc-211">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="68acc-211">**Your registry might be corrupted.**</span></span> <span data-ttu-id="68acc-212">(20)</span><span class="sxs-lookup"><span data-stu-id="68acc-212">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="68acc-213">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="68acc-213">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="68acc-214">(21)</span><span class="sxs-lookup"><span data-stu-id="68acc-214">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="68acc-215">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="68acc-215">**This device is disabled.**</span></span> <span data-ttu-id="68acc-216">(22)</span><span class="sxs-lookup"><span data-stu-id="68acc-216">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="68acc-217">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="68acc-217">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="68acc-218">(23)</span><span class="sxs-lookup"><span data-stu-id="68acc-218">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="68acc-219">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="68acc-219">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="68acc-220">(24)</span><span class="sxs-lookup"><span data-stu-id="68acc-220">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="68acc-221">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="68acc-221">**Windows is still setting up this device.**</span></span> <span data-ttu-id="68acc-222">(25)</span><span class="sxs-lookup"><span data-stu-id="68acc-222">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="68acc-223">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="68acc-223">**Windows is still setting up this device.**</span></span> <span data-ttu-id="68acc-224">(26)</span><span class="sxs-lookup"><span data-stu-id="68acc-224">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="68acc-225">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="68acc-225">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="68acc-226">(27)</span><span class="sxs-lookup"><span data-stu-id="68acc-226">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="68acc-227">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="68acc-227">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="68acc-228">(28)</span><span class="sxs-lookup"><span data-stu-id="68acc-228">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="68acc-229">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="68acc-229">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="68acc-230">(29)</span><span class="sxs-lookup"><span data-stu-id="68acc-230">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="68acc-231">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="68acc-231">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="68acc-232">(30)</span><span class="sxs-lookup"><span data-stu-id="68acc-232">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="68acc-233">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="68acc-233">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="68acc-234">1-31</span><span class="sxs-lookup"><span data-stu-id="68acc-234">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68acc-235">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="68acc-235">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-236">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="68acc-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-238">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="68acc-238">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-239">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="68acc-239">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="68acc-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-241">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-243">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68acc-243">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68acc-244">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="68acc-244">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="68acc-245">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="68acc-245">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-246">**Описание**</span><span class="sxs-lookup"><span data-stu-id="68acc-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-249">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="68acc-249">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-250">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="68acc-250">A textual description of the object.</span></span>

<span data-ttu-id="68acc-251">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68acc-252">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="68acc-252">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-253">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-255">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68acc-255">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68acc-256">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="68acc-256">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-257">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="68acc-257">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-258">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="68acc-258">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-259">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68acc-260">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="68acc-260">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-261">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="68acc-261">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-262">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68acc-264">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="68acc-264">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-265">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68acc-265">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-266">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68acc-266">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-268">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="68acc-268">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-269">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="68acc-269">Indicates when the object was installed.</span></span> <span data-ttu-id="68acc-270">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="68acc-270">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="68acc-271">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-271">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68acc-272">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="68acc-272">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68acc-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68acc-275">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="68acc-275">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-276">**Name**</span><span class="sxs-lookup"><span data-stu-id="68acc-276">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-279">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="68acc-279">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-280">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="68acc-280">Label by which the object is known.</span></span> <span data-ttu-id="68acc-281">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="68acc-281">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="68acc-282">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68acc-283">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="68acc-283">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-286">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="68acc-286">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-287">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="68acc-287">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="68acc-288">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="68acc-288">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="68acc-289">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="68acc-289">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-290">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="68acc-290">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="68acc-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68acc-292">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="68acc-292">Indicates the specific power-related capabilities of the logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68acc-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="68acc-293"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-294">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="68acc-294">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="68acc-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="68acc-295"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-296">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="68acc-296">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="68acc-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="68acc-297"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-298">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="68acc-298">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="68acc-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="68acc-299"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-300">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="68acc-300">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="68acc-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="68acc-301"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-302">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="68acc-302">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="68acc-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="68acc-303"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-304">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="68acc-304">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="68acc-305">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="68acc-305">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="68acc-306">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="68acc-306">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="68acc-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="68acc-307"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-308">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="68acc-308">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="68acc-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="68acc-309"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="68acc-310">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="68acc-310">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68acc-311">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="68acc-311">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="68acc-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="68acc-314">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="68acc-314">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="68acc-315">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="68acc-315">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="68acc-316">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="68acc-316">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="68acc-317">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="68acc-317">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-318">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="68acc-318">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-321">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="68acc-321">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-322">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="68acc-322">String that indicates the current status of the object.</span></span> <span data-ttu-id="68acc-323">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="68acc-323">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="68acc-324">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="68acc-324">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="68acc-325">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="68acc-325">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="68acc-326">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="68acc-326">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="68acc-327">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="68acc-327">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="68acc-328">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="68acc-328">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="68acc-329">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="68acc-330">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="68acc-330">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="68acc-331">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="68acc-331">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="68acc-332">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="68acc-332">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68acc-333">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="68acc-333">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68acc-334">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="68acc-334">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="68acc-335">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="68acc-335">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="68acc-336">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="68acc-336">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="68acc-337">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="68acc-337">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="68acc-338">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="68acc-338">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="68acc-339">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="68acc-339">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="68acc-340">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="68acc-340">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="68acc-341">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="68acc-341">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="68acc-342">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="68acc-342">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68acc-343">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="68acc-343">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68acc-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-346">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="68acc-346">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="68acc-347">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="68acc-347">State of the logical device.</span></span> <span data-ttu-id="68acc-348">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="68acc-348">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="68acc-349">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="68acc-349">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68acc-350">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="68acc-350">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="68acc-351">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="68acc-351">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="68acc-352">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="68acc-352">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="68acc-353">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="68acc-353">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="68acc-354">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="68acc-354">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-357">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68acc-357">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68acc-358">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="68acc-358">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="68acc-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="68acc-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68acc-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68acc-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68acc-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68acc-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68acc-362">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68acc-362">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68acc-363">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="68acc-363">The scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68acc-364">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68acc-364">Remarks</span></span>

<span data-ttu-id="68acc-365">Характеристики логического устройства, которые управляют операцией или конфигурацией, содержатся в объекте **CIM \_** , или связываются с ним.</span><span class="sxs-lookup"><span data-stu-id="68acc-365">Logical device characteristics that manage operation or configuration are contained in, or associated with, the **CIM\_LogicalDevice** object.</span></span> <span data-ttu-id="68acc-366">Например, в качестве рабочих свойств принтера поддерживаются размеры бумаги или обнаруженные ошибки.</span><span class="sxs-lookup"><span data-stu-id="68acc-366">Printer operational properties, for example, are supported paper sizes or detected errors.</span></span> <span data-ttu-id="68acc-367">Например, свойства конфигурации устройства датчика являются пороговыми значениями.</span><span class="sxs-lookup"><span data-stu-id="68acc-367">Sensor device configuration properties, for example, are threshold settings.</span></span> <span data-ttu-id="68acc-368">Для логического устройства могут существовать различные конфигурации, которые содержатся в объектах [**\_ параметров CIM**](cim-setting.md) , связанных с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="68acc-368">Various configurations can exist for a logical device and are contained in the [**CIM\_Setting**](cim-setting.md) objects, which are associated with the logical device.</span></span>

<span data-ttu-id="68acc-369">Класс **CIM \_** -класса является производным от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-369">The **CIM\_LogicalDevice** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="68acc-370">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="68acc-370">WMI does not implement this class.</span></span> <span data-ttu-id="68acc-371">Классы, производные **от \_ CIM**"классического класса", см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="68acc-371">For classes derived from **CIM\_LogicalDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="68acc-372">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="68acc-372">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="68acc-373">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="68acc-373">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="68acc-374">Требования</span><span class="sxs-lookup"><span data-stu-id="68acc-374">Requirements</span></span>



| <span data-ttu-id="68acc-375">Требование</span><span class="sxs-lookup"><span data-stu-id="68acc-375">Requirement</span></span> | <span data-ttu-id="68acc-376">Значение</span><span class="sxs-lookup"><span data-stu-id="68acc-376">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68acc-377">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68acc-377">Minimum supported client</span></span><br/> | <span data-ttu-id="68acc-378">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68acc-378">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68acc-379">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68acc-379">Minimum supported server</span></span><br/> | <span data-ttu-id="68acc-380">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68acc-380">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68acc-381">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68acc-381">Namespace</span></span><br/>                | <span data-ttu-id="68acc-382">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="68acc-382">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68acc-383">MOF</span><span class="sxs-lookup"><span data-stu-id="68acc-383">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68acc-384"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68acc-384"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68acc-385">DLL</span><span class="sxs-lookup"><span data-stu-id="68acc-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68acc-386"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68acc-386"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68acc-387">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68acc-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68acc-388">**\_ЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="68acc-388">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

