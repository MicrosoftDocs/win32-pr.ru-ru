---
description: '\_Класс контроллера CIM является родительским классом для группирования различных устройств, связанных с управлением. Примерами контроллеров являются контроллеры SCSI, USB-контроллеры и последовательные контроллеры.'
ms.assetid: 526d58bb-cdf4-42c2-ae89-7b86d99e2017
ms.tgt_platform: multiple
title: Класс CIM_Controller (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller
- CIM_Controller.Caption
- CIM_Controller.Description
- CIM_Controller.InstallDate
- CIM_Controller.Name
- CIM_Controller.Status
- CIM_Controller.Availability
- CIM_Controller.ConfigManagerErrorCode
- CIM_Controller.ConfigManagerUserConfig
- CIM_Controller.CreationClassName
- CIM_Controller.DeviceID
- CIM_Controller.PowerManagementCapabilities
- CIM_Controller.ErrorCleared
- CIM_Controller.ErrorDescription
- CIM_Controller.LastErrorCode
- CIM_Controller.PNPDeviceID
- CIM_Controller.PowerManagementSupported
- CIM_Controller.StatusInfo
- CIM_Controller.SystemCreationClassName
- CIM_Controller.SystemName
- CIM_Controller.MaxNumberControlled
- CIM_Controller.ProtocolSupported
- CIM_Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b23ef846c118c8d0698660175e4be700ea892055
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262605"
---
# <a name="cim_controller-class-cimwin32-wmi-providers"></a><span data-ttu-id="8685e-104">Класс CIM_Controller (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8685e-104">CIM_Controller class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8685e-105">Класс **\_ контроллера CIM** является родительским классом для группирования различных устройств, связанных с управлением.</span><span class="sxs-lookup"><span data-stu-id="8685e-105">The **CIM\_Controller** class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="8685e-106">Примерами контроллеров являются контроллеры SCSI, USB-контроллеры и последовательные контроллеры.</span><span class="sxs-lookup"><span data-stu-id="8685e-106">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

<span data-ttu-id="8685e-107">Класс **\_ контроллера CIM** является абстракцией для устройств с одним стеком протоколов, которые существуют в основном для обмена данными с устройствами ([**CIM \_ контролледби**](cim-controlledby.md)), а также для их управления или сброса.</span><span class="sxs-lookup"><span data-stu-id="8685e-107">The **CIM\_Controller** class is an abstraction for devices with a single protocol stack, which exist primarily for communication to, and control or reset of, downstream ([**CIM\_ControlledBy**](cim-controlledby.md)) devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8685e-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8685e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8685e-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8685e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8685e-110">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8685e-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8685e-111">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8685e-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8685e-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8685e-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C531-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Controller : CIM_LogicalDevice
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
  uint32   MaxNumberControlled;
  uint16   ProtocolSupported;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="8685e-113">Члены</span><span class="sxs-lookup"><span data-stu-id="8685e-113">Members</span></span>

<span data-ttu-id="8685e-114">Класс **\_ контроллера CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8685e-114">The **CIM\_Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="8685e-115">Методы</span><span class="sxs-lookup"><span data-stu-id="8685e-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="8685e-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="8685e-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8685e-117">Методы</span><span class="sxs-lookup"><span data-stu-id="8685e-117">Methods</span></span>

<span data-ttu-id="8685e-118">Класс **\_ контроллера CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8685e-118">The **CIM\_Controller** class has these methods.</span></span>



| <span data-ttu-id="8685e-119">Метод</span><span class="sxs-lookup"><span data-stu-id="8685e-119">Method</span></span>                                                                | <span data-ttu-id="8685e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8685e-120">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8685e-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="8685e-121">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="8685e-122">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8685e-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="8685e-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="8685e-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="8685e-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8685e-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="8685e-125">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="8685e-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="8685e-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="8685e-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8685e-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="8685e-127">Properties</span></span>

<span data-ttu-id="8685e-128">Класс **\_ контроллера CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8685e-128">The **CIM\_Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8685e-129">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="8685e-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8685e-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="8685e-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-133">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="8685e-133">Availability and status of the device.</span></span>

<span data-ttu-id="8685e-134">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8685e-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8685e-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8685e-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="8685e-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8685e-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="8685e-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8685e-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="8685e-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8685e-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="8685e-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8685e-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="8685e-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8685e-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="8685e-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8685e-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="8685e-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8685e-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="8685e-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8685e-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="8685e-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8685e-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="8685e-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8685e-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="8685e-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8685e-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="8685e-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-148">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="8685e-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8685e-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="8685e-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-150">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="8685e-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8685e-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="8685e-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-152">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="8685e-152">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8685e-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="8685e-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8685e-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="8685e-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-155">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="8685e-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8685e-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="8685e-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-157">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="8685e-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8685e-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="8685e-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-159">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="8685e-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8685e-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="8685e-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-161">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="8685e-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8685e-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="8685e-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-163">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="8685e-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8685e-164">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8685e-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-167">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8685e-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-168">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8685e-168">A short textual description of the object.</span></span>

<span data-ttu-id="8685e-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8685e-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-170">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="8685e-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8685e-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-173">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8685e-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-174">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8685e-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="8685e-175">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8685e-176">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="8685e-176">**This device is working properly.**</span></span> <span data-ttu-id="8685e-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="8685e-177">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8685e-178">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="8685e-178">**This device is not configured correctly.**</span></span> <span data-ttu-id="8685e-179">(1)</span><span class="sxs-lookup"><span data-stu-id="8685e-179">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8685e-180">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-180">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8685e-181">(2)</span><span class="sxs-lookup"><span data-stu-id="8685e-181">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8685e-182">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="8685e-182">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8685e-183">(3)</span><span class="sxs-lookup"><span data-stu-id="8685e-183">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8685e-184">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="8685e-184">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8685e-185">(4)</span><span class="sxs-lookup"><span data-stu-id="8685e-185">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8685e-186">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="8685e-186">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8685e-187">(5)</span><span class="sxs-lookup"><span data-stu-id="8685e-187">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8685e-188">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="8685e-188">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8685e-189"> (6)</span><span class="sxs-lookup"><span data-stu-id="8685e-189">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8685e-190">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="8685e-190">**Cannot filter.**</span></span> <span data-ttu-id="8685e-191">(7)</span><span class="sxs-lookup"><span data-stu-id="8685e-191">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8685e-192">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-192">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8685e-193">(8)</span><span class="sxs-lookup"><span data-stu-id="8685e-193">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8685e-194">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-194">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8685e-195">(9)</span><span class="sxs-lookup"><span data-stu-id="8685e-195">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8685e-196">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="8685e-196">**This device cannot start.**</span></span> <span data-ttu-id="8685e-197">(10)</span><span class="sxs-lookup"><span data-stu-id="8685e-197">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8685e-198">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-198">**This device failed.**</span></span> <span data-ttu-id="8685e-199">(11)</span><span class="sxs-lookup"><span data-stu-id="8685e-199">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8685e-200">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="8685e-200">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8685e-201">(12)</span><span class="sxs-lookup"><span data-stu-id="8685e-201">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8685e-202">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-202">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8685e-203">(13)</span><span class="sxs-lookup"><span data-stu-id="8685e-203">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8685e-204">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="8685e-204">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8685e-205">(14)</span><span class="sxs-lookup"><span data-stu-id="8685e-205">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8685e-206">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="8685e-206">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8685e-207">(15)</span><span class="sxs-lookup"><span data-stu-id="8685e-207">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8685e-208">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="8685e-208">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8685e-209">(16)</span><span class="sxs-lookup"><span data-stu-id="8685e-209">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8685e-210">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="8685e-210">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8685e-211">(17)</span><span class="sxs-lookup"><span data-stu-id="8685e-211">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8685e-212">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-212">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8685e-213">(18)</span><span class="sxs-lookup"><span data-stu-id="8685e-213">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8685e-214">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="8685e-214">**Failure using the VxD loader.**</span></span> <span data-ttu-id="8685e-215">(19)</span><span class="sxs-lookup"><span data-stu-id="8685e-215">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8685e-216">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="8685e-216">**Your registry might be corrupted.**</span></span> <span data-ttu-id="8685e-217">(20)</span><span class="sxs-lookup"><span data-stu-id="8685e-217">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8685e-218">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="8685e-218">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8685e-219">(21)</span><span class="sxs-lookup"><span data-stu-id="8685e-219">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8685e-220">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="8685e-220">**This device is disabled.**</span></span> <span data-ttu-id="8685e-221">(22)</span><span class="sxs-lookup"><span data-stu-id="8685e-221">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8685e-222">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="8685e-222">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8685e-223">(23)</span><span class="sxs-lookup"><span data-stu-id="8685e-223">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8685e-224">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="8685e-224">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8685e-225">(24)</span><span class="sxs-lookup"><span data-stu-id="8685e-225">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8685e-226">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="8685e-226">**Windows is still setting up this device.**</span></span> <span data-ttu-id="8685e-227">(25)</span><span class="sxs-lookup"><span data-stu-id="8685e-227">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8685e-228">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="8685e-228">**Windows is still setting up this device.**</span></span> <span data-ttu-id="8685e-229">(26)</span><span class="sxs-lookup"><span data-stu-id="8685e-229">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8685e-230">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="8685e-230">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8685e-231">(27)</span><span class="sxs-lookup"><span data-stu-id="8685e-231">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8685e-232">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="8685e-232">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8685e-233">(28)</span><span class="sxs-lookup"><span data-stu-id="8685e-233">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8685e-234">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="8685e-234">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8685e-235">(29)</span><span class="sxs-lookup"><span data-stu-id="8685e-235">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8685e-236">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="8685e-236">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8685e-237">(30)</span><span class="sxs-lookup"><span data-stu-id="8685e-237">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8685e-238">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8685e-238">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8685e-239">1-31</span><span class="sxs-lookup"><span data-stu-id="8685e-239">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8685e-240">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="8685e-240">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-241">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8685e-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-242">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-243">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8685e-243">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-244">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="8685e-244">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8685e-245">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-245">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-246">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8685e-246">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-249">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8685e-249">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8685e-250">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8685e-250">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8685e-251">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="8685e-251">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8685e-252">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-252">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-253">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8685e-253">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-254">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-256">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="8685e-256">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-257">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8685e-257">A textual description of the object.</span></span>

<span data-ttu-id="8685e-258">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8685e-258">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-259">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8685e-259">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-260">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-261">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-262">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8685e-262">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8685e-263">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8685e-263">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="8685e-264">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-264">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-265">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="8685e-265">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-266">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8685e-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8685e-268">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="8685e-268">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="8685e-269">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-269">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-270">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8685e-270">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8685e-273">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="8685e-273">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="8685e-274">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-274">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-275">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8685e-275">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-276">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8685e-276">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-278">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="8685e-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-279">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="8685e-279">Indicates when the object was installed.</span></span> <span data-ttu-id="8685e-280">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="8685e-280">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="8685e-281">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8685e-281">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-282">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="8685e-282">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-283">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8685e-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8685e-285">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="8685e-285">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8685e-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-287">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="8685e-287">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-288">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8685e-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-290">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="8685e-290">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-291">Максимальное число непосредственных адресаций сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="8685e-291">Maximum number of directly addressable entities supported by this controller.</span></span> <span data-ttu-id="8685e-292">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="8685e-292">A value of 0 should be used if the number is unknown or unlimited.</span></span>

</dd> <dt>

<span data-ttu-id="8685e-293">**Name**</span><span class="sxs-lookup"><span data-stu-id="8685e-293">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-296">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="8685e-296">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-297">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8685e-297">Label by which the object is known.</span></span> <span data-ttu-id="8685e-298">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="8685e-298">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8685e-299">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8685e-299">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-300">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8685e-300">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-303">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8685e-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-304">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8685e-304">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="8685e-305">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="8685e-305">Example: "\*PNP030b"</span></span>

<span data-ttu-id="8685e-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-307">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8685e-307">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-308">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8685e-308">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8685e-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8685e-310">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="8685e-310">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="8685e-311">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8685e-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8685e-312"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-313">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="8685e-313">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8685e-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="8685e-314"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-315">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="8685e-315">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8685e-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="8685e-316"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-317">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="8685e-317">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8685e-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="8685e-318"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-319">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="8685e-319">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8685e-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="8685e-320"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-321">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="8685e-321">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8685e-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="8685e-322"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-323">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="8685e-323">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="8685e-324">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="8685e-324">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="8685e-325">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="8685e-325">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8685e-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="8685e-326"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-327">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="8685e-327">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8685e-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="8685e-328"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8685e-329">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="8685e-329">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8685e-330">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8685e-330">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-331">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8685e-331">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8685e-333">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="8685e-333">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="8685e-334">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="8685e-334">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="8685e-335">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8685e-335">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="8685e-336">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="8685e-336">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="8685e-337">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-338">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8685e-338">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-339">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8685e-339">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-341">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8685e-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-342">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="8685e-342">The protocol used by the controller to access 'controlled' devices.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8685e-343">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8685e-343">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8685e-344">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="8685e-344">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="8685e-345">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="8685e-345">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="8685e-346">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="8685e-346">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="8685e-347">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="8685e-347">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="8685e-348">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="8685e-348">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="8685e-349">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="8685e-349">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="8685e-350">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="8685e-350">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="8685e-351">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="8685e-351">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="8685e-352">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="8685e-352">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="8685e-353">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="8685e-353">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="8685e-354">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="8685e-354">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="8685e-355">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="8685e-355">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="8685e-356">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="8685e-356">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="8685e-357">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="8685e-357">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="8685e-358">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="8685e-358">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="8685e-359">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="8685e-359">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="8685e-360">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="8685e-360">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="8685e-361">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="8685e-361">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="8685e-362">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="8685e-362">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="8685e-363">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="8685e-363">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="8685e-364">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="8685e-364">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="8685e-365">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="8685e-365">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="8685e-366">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="8685e-366">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="8685e-367">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="8685e-367">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="8685e-368">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="8685e-368">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="8685e-369">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="8685e-369">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="8685e-370">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="8685e-370">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="8685e-371">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="8685e-371">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="8685e-372">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="8685e-372">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="8685e-373">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="8685e-373">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="8685e-374">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="8685e-374">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="8685e-375">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="8685e-375">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="8685e-376">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="8685e-376">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="8685e-377">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="8685e-377">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="8685e-378">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="8685e-378">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="8685e-379">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="8685e-379">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="8685e-380">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="8685e-380">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="8685e-381">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="8685e-381">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="8685e-382">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="8685e-382">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="8685e-383">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="8685e-383">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="8685e-384">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="8685e-384">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="8685e-385">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="8685e-385">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="8685e-386">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="8685e-386">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="8685e-387">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="8685e-387">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="8685e-388">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="8685e-388">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="8685e-389">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="8685e-389">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8685e-390">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8685e-390">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-393">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="8685e-393">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-394">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8685e-394">String that indicates the current status of the object.</span></span> <span data-ttu-id="8685e-395">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="8685e-395">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="8685e-396">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="8685e-396">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="8685e-397">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="8685e-397">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="8685e-398">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="8685e-398">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8685e-399">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="8685e-399">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8685e-400">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="8685e-400">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8685e-401">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8685e-401">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8685e-402">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="8685e-402">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8685e-403">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="8685e-403">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8685e-404">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="8685e-404">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8685e-405">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="8685e-405">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8685e-406">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8685e-406">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8685e-407">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="8685e-407">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8685e-408">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="8685e-408">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8685e-409">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="8685e-409">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8685e-410">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="8685e-410">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8685e-411">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="8685e-411">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8685e-412">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="8685e-412">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8685e-413">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="8685e-413">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8685e-414">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="8685e-414">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8685e-415">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8685e-415">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-416">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8685e-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-418">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8685e-418">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8685e-419">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8685e-419">State of the logical device.</span></span> <span data-ttu-id="8685e-420">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="8685e-420">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="8685e-421">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8685e-422">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8685e-422">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8685e-423">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="8685e-423">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8685e-424">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="8685e-424">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8685e-425">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="8685e-425">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8685e-426">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="8685e-426">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8685e-427">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="8685e-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-430">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8685e-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8685e-431">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="8685e-431">The scoping system's creation class name.</span></span>

<span data-ttu-id="8685e-432">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8685e-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8685e-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8685e-436">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8685e-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8685e-437">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="8685e-437">The scoping system's name.</span></span>

<span data-ttu-id="8685e-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8685e-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8685e-439">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="8685e-439">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8685e-440">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8685e-440">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8685e-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8685e-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8685e-442">Дата и время последнего сброса контроллера (выключен или повторно инициализирован).</span><span class="sxs-lookup"><span data-stu-id="8685e-442">Date and time the controller was last reset (powered down or reinitialized).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8685e-443">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8685e-443">Remarks</span></span>

<span data-ttu-id="8685e-444">Класс **\_ контроллера CIM** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="8685e-444">The **CIM\_Controller** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8685e-445">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="8685e-445">WMI does not implement this class.</span></span> <span data-ttu-id="8685e-446">Классы, производные от **CIM \_ Controller**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8685e-446">For classes derived from **CIM\_Controller**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8685e-447">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8685e-447">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8685e-448">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8685e-448">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8685e-449">Требования</span><span class="sxs-lookup"><span data-stu-id="8685e-449">Requirements</span></span>



| <span data-ttu-id="8685e-450">Требование</span><span class="sxs-lookup"><span data-stu-id="8685e-450">Requirement</span></span> | <span data-ttu-id="8685e-451">Значение</span><span class="sxs-lookup"><span data-stu-id="8685e-451">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8685e-452">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8685e-452">Minimum supported client</span></span><br/> | <span data-ttu-id="8685e-453">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8685e-453">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8685e-454">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8685e-454">Minimum supported server</span></span><br/> | <span data-ttu-id="8685e-455">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8685e-455">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8685e-456">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8685e-456">Namespace</span></span><br/>                | <span data-ttu-id="8685e-457">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8685e-457">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8685e-458">MOF</span><span class="sxs-lookup"><span data-stu-id="8685e-458">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8685e-459"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8685e-459"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8685e-460">DLL</span><span class="sxs-lookup"><span data-stu-id="8685e-460">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8685e-461"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8685e-461"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8685e-462">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8685e-462">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8685e-463">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="8685e-463">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

