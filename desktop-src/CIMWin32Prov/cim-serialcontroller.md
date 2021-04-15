---
description: Класс CIM \_ сериалконтроллер представляет возможности и управление логическим устройством с последовательным портом.
ms.assetid: 7d5a96aa-fa6c-4904-8ca1-88ec14748810
ms.tgt_platform: multiple
title: Класс CIM_SerialController (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController
- CIM_SerialController.Availability
- CIM_SerialController.Capabilities
- CIM_SerialController.CapabilityDescriptions
- CIM_SerialController.Caption
- CIM_SerialController.ConfigManagerErrorCode
- CIM_SerialController.ConfigManagerUserConfig
- CIM_SerialController.CreationClassName
- CIM_SerialController.Description
- CIM_SerialController.DeviceID
- CIM_SerialController.ErrorCleared
- CIM_SerialController.ErrorDescription
- CIM_SerialController.InstallDate
- CIM_SerialController.LastErrorCode
- CIM_SerialController.MaxBaudRate
- CIM_SerialController.MaxNumberControlled
- CIM_SerialController.Name
- CIM_SerialController.PNPDeviceID
- CIM_SerialController.PowerManagementCapabilities
- CIM_SerialController.PowerManagementSupported
- CIM_SerialController.ProtocolSupported
- CIM_SerialController.Status
- CIM_SerialController.StatusInfo
- CIM_SerialController.SystemCreationClassName
- CIM_SerialController.SystemName
- CIM_SerialController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e23c9183dabb9b4d9ea25f5f92bd4c8ec6667c04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655829"
---
# <a name="cim_serialcontroller-class-cimwin32-wmi-providers"></a><span data-ttu-id="c035c-103">Класс CIM_SerialController (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c035c-103">CIM_SerialController class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c035c-104">Класс **CIM \_ сериалконтроллер** представляет возможности и управление логическим устройством с последовательным портом.</span><span class="sxs-lookup"><span data-stu-id="c035c-104">The **CIM\_SerialController** class represents the capabilities and management of the serial port logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c035c-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c035c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c035c-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c035c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c035c-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c035c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c035c-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c035c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c035c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c035c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C554-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SerialController : CIM_Controller
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="c035c-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c035c-110">Members</span></span>

<span data-ttu-id="c035c-111">Класс **CIM \_ сериалконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c035c-111">The **CIM\_SerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="c035c-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c035c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c035c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c035c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c035c-114">Методы</span><span class="sxs-lookup"><span data-stu-id="c035c-114">Methods</span></span>

<span data-ttu-id="c035c-115">Класс **CIM \_ сериалконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c035c-115">The **CIM\_SerialController** class has these methods.</span></span>



| <span data-ttu-id="c035c-116">Метод</span><span class="sxs-lookup"><span data-stu-id="c035c-116">Method</span></span>                                                                      | <span data-ttu-id="c035c-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c035c-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c035c-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="c035c-118">**Reset**</span></span>](reset-method-in-class-cim-serialcontroller.md)                 | <span data-ttu-id="c035c-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c035c-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c035c-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c035c-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c035c-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-serialcontroller.md) | <span data-ttu-id="c035c-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="c035c-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c035c-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c035c-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c035c-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="c035c-124">Properties</span></span>

<span data-ttu-id="c035c-125">Класс **CIM \_ сериалконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c035c-125">The **CIM\_SerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c035c-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="c035c-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c035c-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="c035c-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-130">Availability and status of the device.</span></span>

<span data-ttu-id="c035c-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c035c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c035c-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c035c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c035c-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c035c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="c035c-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c035c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="c035c-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c035c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="c035c-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c035c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="c035c-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c035c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="c035c-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c035c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="c035c-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c035c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="c035c-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c035c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="c035c-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c035c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="c035c-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c035c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="c035c-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c035c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="c035c-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="c035c-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c035c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="c035c-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="c035c-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c035c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="c035c-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="c035c-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c035c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="c035c-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c035c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="c035c-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="c035c-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c035c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="c035c-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="c035c-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c035c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="c035c-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="c035c-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c035c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="c035c-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="c035c-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c035c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="c035c-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="c035c-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="c035c-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-162">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c035c-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c035c-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-164">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Последовательные порты DMTF \| 004,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сериалконтроллер**.**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="c035c-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-165">Совместимость на уровне микросхем для контроллера последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="c035c-165">Chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="c035c-166">Это свойство описывает буферизацию и другие возможности последовательного контроллера, которые могут быть встроены в оборудование микросхемы.</span><span class="sxs-lookup"><span data-stu-id="c035c-166">This property describes buffering and other capabilities of the serial controller, that may be inherent in the chip hardware.</span></span> <span data-ttu-id="c035c-167">Это свойство является перечислимым целым числом.</span><span class="sxs-lookup"><span data-stu-id="c035c-167">This property is an enumerated integer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c035c-168">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c035c-168">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c035c-169">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c035c-169">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="c035c-170">**XT/AT-совместимый** (3)</span><span class="sxs-lookup"><span data-stu-id="c035c-170">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="c035c-171">**Совместимость с 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="c035c-171">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="c035c-172">**Совместимость с 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="c035c-172">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="c035c-173">**16550A-совместимый** (6)</span><span class="sxs-lookup"><span data-stu-id="c035c-173">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="c035c-174">**Совместимость с 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="c035c-174">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="c035c-175">**8251FIFO-совместимый** (161)</span><span class="sxs-lookup"><span data-stu-id="c035c-175">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-176">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="c035c-176">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-177">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="c035c-177">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c035c-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-179">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сериалконтроллер**.**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="c035c-179">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SerialController**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-180">Строки свободной формы, содержащие подробные объяснения функций последовательного контроллера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="c035c-180">Free-form strings that provide detailed explanations for the serial controller features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="c035c-181">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="c035c-181">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="c035c-182">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c035c-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-185">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c035c-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-186">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c035c-186">Short textual description of the object.</span></span>

<span data-ttu-id="c035c-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-188">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c035c-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-189">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c035c-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-191">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c035c-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-192">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c035c-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c035c-193">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c035c-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="c035c-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="c035c-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="c035c-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-196">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="c035c-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c035c-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="c035c-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="c035c-198">(1)</span><span class="sxs-lookup"><span data-stu-id="c035c-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-199">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="c035c-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c035c-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c035c-201">(2)</span><span class="sxs-lookup"><span data-stu-id="c035c-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c035c-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="c035c-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c035c-203">(3)</span><span class="sxs-lookup"><span data-stu-id="c035c-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-204">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c035c-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c035c-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="c035c-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c035c-206">(4)</span><span class="sxs-lookup"><span data-stu-id="c035c-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-207">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="c035c-207">Device is not working properly.</span></span> <span data-ttu-id="c035c-208">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="c035c-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c035c-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="c035c-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c035c-210">(5)</span><span class="sxs-lookup"><span data-stu-id="c035c-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-211">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="c035c-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c035c-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="c035c-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c035c-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="c035c-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-214">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="c035c-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c035c-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="c035c-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="c035c-216">(7)</span><span class="sxs-lookup"><span data-stu-id="c035c-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c035c-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c035c-218">(8)</span><span class="sxs-lookup"><span data-stu-id="c035c-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-219">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c035c-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c035c-221">(9)</span><span class="sxs-lookup"><span data-stu-id="c035c-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-222">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="c035c-222">Device is not working properly.</span></span> <span data-ttu-id="c035c-223">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c035c-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="c035c-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="c035c-225">(10)</span><span class="sxs-lookup"><span data-stu-id="c035c-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-226">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="c035c-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c035c-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="c035c-228">(11)</span><span class="sxs-lookup"><span data-stu-id="c035c-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-229">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c035c-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="c035c-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c035c-231">(12)</span><span class="sxs-lookup"><span data-stu-id="c035c-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-232">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="c035c-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c035c-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c035c-234">(13)</span><span class="sxs-lookup"><span data-stu-id="c035c-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-235">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c035c-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="c035c-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c035c-237">(14)</span><span class="sxs-lookup"><span data-stu-id="c035c-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-238">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="c035c-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c035c-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="c035c-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c035c-240">(15)</span><span class="sxs-lookup"><span data-stu-id="c035c-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-241">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="c035c-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c035c-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="c035c-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c035c-243">(16)</span><span class="sxs-lookup"><span data-stu-id="c035c-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-244">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="c035c-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c035c-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="c035c-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c035c-246">(17)</span><span class="sxs-lookup"><span data-stu-id="c035c-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-247">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="c035c-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c035c-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c035c-249">(18)</span><span class="sxs-lookup"><span data-stu-id="c035c-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-250">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="c035c-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c035c-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="c035c-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="c035c-252">(19)</span><span class="sxs-lookup"><span data-stu-id="c035c-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c035c-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="c035c-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="c035c-254">(20)</span><span class="sxs-lookup"><span data-stu-id="c035c-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-255">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="c035c-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c035c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="c035c-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c035c-257">(21)</span><span class="sxs-lookup"><span data-stu-id="c035c-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-258">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="c035c-258">System failure.</span></span> <span data-ttu-id="c035c-259">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="c035c-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="c035c-260">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="c035c-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c035c-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="c035c-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="c035c-262">(22)</span><span class="sxs-lookup"><span data-stu-id="c035c-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-263">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="c035c-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c035c-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="c035c-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c035c-265">(23)</span><span class="sxs-lookup"><span data-stu-id="c035c-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-266">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="c035c-266">System failure.</span></span> <span data-ttu-id="c035c-267">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="c035c-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c035c-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="c035c-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c035c-269">(24)</span><span class="sxs-lookup"><span data-stu-id="c035c-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-270">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="c035c-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c035c-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="c035c-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c035c-272">(25)</span><span class="sxs-lookup"><span data-stu-id="c035c-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-273">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="c035c-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c035c-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="c035c-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="c035c-275">(26)</span><span class="sxs-lookup"><span data-stu-id="c035c-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-276">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="c035c-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c035c-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="c035c-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c035c-278">(27)</span><span class="sxs-lookup"><span data-stu-id="c035c-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-279">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="c035c-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c035c-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="c035c-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c035c-281">(28)</span><span class="sxs-lookup"><span data-stu-id="c035c-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-282">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="c035c-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c035c-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="c035c-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c035c-284">(29)</span><span class="sxs-lookup"><span data-stu-id="c035c-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-285">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="c035c-285">Device is disabled.</span></span> <span data-ttu-id="c035c-286">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c035c-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c035c-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="c035c-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c035c-288">(30)</span><span class="sxs-lookup"><span data-stu-id="c035c-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-289">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="c035c-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c035c-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c035c-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c035c-291">1-31</span><span class="sxs-lookup"><span data-stu-id="c035c-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-292">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="c035c-292">Device is not working properly.</span></span> <span data-ttu-id="c035c-293">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="c035c-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-294">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="c035c-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-295">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c035c-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-297">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c035c-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-298">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c035c-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c035c-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c035c-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-303">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c035c-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c035c-304">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c035c-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c035c-305">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c035c-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c035c-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-307">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c035c-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-310">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c035c-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-311">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c035c-311">Textual description of the object.</span></span>

<span data-ttu-id="c035c-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c035c-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-316">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c035c-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c035c-317">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c035c-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-319">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="c035c-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-320">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c035c-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c035c-322">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="c035c-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c035c-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c035c-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c035c-327">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="c035c-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c035c-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-329">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c035c-329">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-330">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c035c-330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-332">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c035c-332">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-333">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="c035c-333">Date and time the object was installed.</span></span> <span data-ttu-id="c035c-334">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="c035c-334">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="c035c-335">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-336">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c035c-336">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-337">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c035c-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c035c-339">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="c035c-339">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c035c-340">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-340">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-341">**максбаудрате**</span><span class="sxs-lookup"><span data-stu-id="c035c-341">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-342">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c035c-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-344">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Последовательные порты DMTF \| 004,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит в секунду ")</span><span class="sxs-lookup"><span data-stu-id="c035c-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-345">Максимальная скорость в битах в секунду, поддерживаемая последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="c035c-345">Maximum baud rate, in bits-per-second, supported by the serial controller.</span></span>

</dd> <dt>

<span data-ttu-id="c035c-346">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="c035c-346">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-347">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c035c-347">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-349">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="c035c-349">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-350">Максимальное количество напрямую обрабатываемых сущностей, поддерживаемых контроллером.</span><span class="sxs-lookup"><span data-stu-id="c035c-350">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="c035c-351">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="c035c-351">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="c035c-352">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-352">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-353">**Name**</span><span class="sxs-lookup"><span data-stu-id="c035c-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-356">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="c035c-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-357">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c035c-357">Label by which the object is known.</span></span> <span data-ttu-id="c035c-358">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="c035c-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c035c-359">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-360">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c035c-360">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-363">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c035c-363">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-364">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-364">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="c035c-365">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c035c-366">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c035c-366">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="c035c-367">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c035c-367">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-368">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c035c-368">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c035c-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c035c-370">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="c035c-370">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="c035c-371">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-371">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c035c-372"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c035c-372"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c035c-373"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="c035c-373"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c035c-374"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="c035c-374"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c035c-375"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="c035c-375"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-376">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="c035c-376">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c035c-377"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="c035c-377"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-378">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="c035c-378">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c035c-379"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="c035c-379"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-380">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="c035c-380">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="c035c-381">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="c035c-381">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="c035c-382">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c035c-382">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c035c-383"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="c035c-383"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-384">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="c035c-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c035c-385"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="c035c-385"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c035c-386">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="c035c-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-387">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="c035c-387">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-388">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c035c-388">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c035c-390">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="c035c-390">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c035c-391">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="c035c-391">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c035c-392">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c035c-392">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c035c-393">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="c035c-393">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="c035c-394">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-394">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-395">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="c035c-395">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-396">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c035c-396">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-398">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c035c-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-399">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="c035c-399">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="c035c-400">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-400">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="c035c-401">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c035c-401">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c035c-402">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c035c-402">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c035c-403">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c035c-403">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="c035c-404">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="c035c-404">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="c035c-405">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="c035c-405">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="c035c-406">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="c035c-406">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="c035c-407">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="c035c-407">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="c035c-408">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="c035c-408">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="c035c-409">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="c035c-409">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="c035c-410">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="c035c-410">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="c035c-411">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="c035c-411">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="c035c-412">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="c035c-412">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="c035c-413">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="c035c-413">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="c035c-414">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="c035c-414">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="c035c-415">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="c035c-415">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="c035c-416">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="c035c-416">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="c035c-417">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="c035c-417">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="c035c-418">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="c035c-418">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="c035c-419">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="c035c-419">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="c035c-420">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="c035c-420">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="c035c-421">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="c035c-421">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="c035c-422">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="c035c-422">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="c035c-423">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="c035c-423">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="c035c-424">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="c035c-424">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="c035c-425">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="c035c-425">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="c035c-426">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="c035c-426">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="c035c-427">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="c035c-427">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="c035c-428">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="c035c-428">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="c035c-429">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="c035c-429">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="c035c-430">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="c035c-430">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="c035c-431">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="c035c-431">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="c035c-432">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="c035c-432">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="c035c-433">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="c035c-433">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="c035c-434">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="c035c-434">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="c035c-435">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="c035c-435">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="c035c-436">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="c035c-436">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="c035c-437">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="c035c-437">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="c035c-438">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="c035c-438">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="c035c-439">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="c035c-439">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="c035c-440">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="c035c-440">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="c035c-441">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="c035c-441">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="c035c-442">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="c035c-442">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="c035c-443">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="c035c-443">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="c035c-444">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="c035c-444">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="c035c-445">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="c035c-445">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="c035c-446">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="c035c-446">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="c035c-447">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="c035c-447">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="c035c-448">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="c035c-448">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-449">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c035c-449">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-450">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-452">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c035c-452">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-453">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c035c-453">Current status of the object.</span></span> <span data-ttu-id="c035c-454">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-454">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c035c-455">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c035c-455">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c035c-456">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c035c-456">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c035c-457">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c035c-457">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c035c-458">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c035c-458">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c035c-459">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c035c-459">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c035c-460">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c035c-460">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c035c-461">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c035c-461">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c035c-462">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c035c-462">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c035c-463">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c035c-463">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c035c-464">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c035c-464">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c035c-465">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c035c-465">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c035c-466">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c035c-466">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c035c-467">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c035c-467">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-468">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c035c-468">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-469">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c035c-469">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-471">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c035c-471">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c035c-472">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c035c-472">State of the logical device.</span></span> <span data-ttu-id="c035c-473">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="c035c-473">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="c035c-474">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-474">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c035c-475">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c035c-475">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c035c-476">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c035c-476">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c035c-477">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="c035c-477">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c035c-478">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="c035c-478">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c035c-479">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="c035c-479">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c035c-480">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c035c-480">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-483">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c035c-483">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c035c-484">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="c035c-484">Scoping system's creation class name.</span></span>

<span data-ttu-id="c035c-485">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-485">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-486">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c035c-486">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-487">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c035c-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-488">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c035c-489">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c035c-489">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c035c-490">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="c035c-490">Scoping system's name.</span></span>

<span data-ttu-id="c035c-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c035c-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c035c-492">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="c035c-492">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c035c-493">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c035c-493">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c035c-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c035c-494">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c035c-495">Дата и время последнего сброса контроллера, означающее, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="c035c-495">Date and time the controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="c035c-496">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-496">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c035c-497">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c035c-497">Remarks</span></span>

<span data-ttu-id="c035c-498">Класс **CIM \_ сериалконтроллер** является производным от [**\_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-498">The **CIM\_SerialController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="c035c-499">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c035c-499">WMI does not implement this class.</span></span> <span data-ttu-id="c035c-500">Классы WMI, производные от **CIM \_ сериалконтроллер**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c035c-500">For WMI classes derived from **CIM\_SerialController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c035c-501">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c035c-501">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c035c-502">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c035c-502">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c035c-503">Требования</span><span class="sxs-lookup"><span data-stu-id="c035c-503">Requirements</span></span>



| <span data-ttu-id="c035c-504">Требование</span><span class="sxs-lookup"><span data-stu-id="c035c-504">Requirement</span></span> | <span data-ttu-id="c035c-505">Значение</span><span class="sxs-lookup"><span data-stu-id="c035c-505">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c035c-506">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c035c-506">Minimum supported client</span></span><br/> | <span data-ttu-id="c035c-507">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c035c-507">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c035c-508">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c035c-508">Minimum supported server</span></span><br/> | <span data-ttu-id="c035c-509">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c035c-509">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c035c-510">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c035c-510">Namespace</span></span><br/>                | <span data-ttu-id="c035c-511">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c035c-511">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c035c-512">MOF</span><span class="sxs-lookup"><span data-stu-id="c035c-512">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c035c-513"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c035c-513"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c035c-514">DLL</span><span class="sxs-lookup"><span data-stu-id="c035c-514">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c035c-515"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c035c-515"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c035c-516">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c035c-516">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c035c-517">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="c035c-517">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

