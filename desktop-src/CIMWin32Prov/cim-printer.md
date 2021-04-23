---
description: '\_Класс Printer CIM представляет возможности и управление логическим устройством принтера.'
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: Класс CIM_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c673d6c58e6235e782a718b3b258a15790046eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142763"
---
# <a name="cim_printer-class"></a><span data-ttu-id="dee50-103">\_Класс принтера CIM</span><span class="sxs-lookup"><span data-stu-id="dee50-103">CIM\_Printer class</span></span>

<span data-ttu-id="dee50-104">Класс **\_ Printer CIM** представляет возможности и управление логическим устройством принтера.</span><span class="sxs-lookup"><span data-stu-id="dee50-104">The **CIM\_Printer** class represents the capabilities and management of the printer logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dee50-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="dee50-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dee50-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dee50-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dee50-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dee50-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dee50-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dee50-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee50-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dee50-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="dee50-110">Члены</span><span class="sxs-lookup"><span data-stu-id="dee50-110">Members</span></span>

<span data-ttu-id="dee50-111">Класс **« \_ принтер CIM** » имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dee50-111">The **CIM\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="dee50-112">Методы</span><span class="sxs-lookup"><span data-stu-id="dee50-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="dee50-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dee50-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dee50-114">Методы</span><span class="sxs-lookup"><span data-stu-id="dee50-114">Methods</span></span>

<span data-ttu-id="dee50-115">Класс **\_ Printer модели CIM** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="dee50-115">The **CIM\_Printer** class has these methods.</span></span>



| <span data-ttu-id="dee50-116">Метод</span><span class="sxs-lookup"><span data-stu-id="dee50-116">Method</span></span>                                                             | <span data-ttu-id="dee50-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dee50-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dee50-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="dee50-118">**Reset**</span></span>](reset-method-in-class-cim-printer.md)                 | <span data-ttu-id="dee50-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="dee50-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="dee50-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="dee50-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dee50-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-printer.md) | <span data-ttu-id="dee50-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="dee50-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="dee50-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="dee50-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dee50-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="dee50-124">Properties</span></span>

<span data-ttu-id="dee50-125">Класс **\_ принтера CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dee50-125">The **CIM\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dee50-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="dee50-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="dee50-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-130">Availability and status of the device.</span></span>

<span data-ttu-id="dee50-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dee50-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-135">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="dee50-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dee50-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dee50-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dee50-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dee50-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dee50-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dee50-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dee50-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dee50-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dee50-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dee50-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-146">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="dee50-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dee50-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-148">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="dee50-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dee50-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-150">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="dee50-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dee50-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dee50-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-153">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="dee50-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dee50-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-155">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="dee50-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dee50-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-157">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="dee50-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dee50-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-159">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="dee50-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dee50-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-161">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="dee50-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-162">**аваилаблежобшитс**</span><span class="sxs-lookup"><span data-stu-id="dee50-162">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-163">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-165">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. рекуиреджобшитс")</span><span class="sxs-lookup"><span data-stu-id="dee50-165">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-166">Описывает все листы заданий, доступные на принтере.</span><span class="sxs-lookup"><span data-stu-id="dee50-166">Describes all of the job sheets that are available on the printer.</span></span> <span data-ttu-id="dee50-167">Это также можно использовать для описания баннера, который принтер может предоставить в начале каждого задания, или для описания других параметров, заданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="dee50-167">This can also be used to describe the banner that a printer might provide at the beginning of each job, or can describe other user specified options.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-168">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="dee50-168">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-169">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dee50-169">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-171">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ принтер CIM**". Капабилитидескриптионс "," CIM \_ PrintJob. Finished "," CIM \_ Принтсервице. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="dee50-171">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-172">Возможности принтера.</span><span class="sxs-lookup"><span data-stu-id="dee50-172">Printer capabilities.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="dee50-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Цветная печать** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-175"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="dee50-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Дуплексная печать** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-176"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="dee50-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Копии** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-177"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="dee50-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Параметры сортировки** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-178"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="dee50-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Сшивание** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-179"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="dee50-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Прозрачная печать** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-180"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="dee50-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Дырокол** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-181"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="dee50-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Покрытие** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-182"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="dee50-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-183"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="dee50-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Черно-белая печать** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-184"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="dee50-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Одна сторона** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-185"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-186">Одна сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-186">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="dee50-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>Двусторонняя **сторона** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-187"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-188">Двусторонняя длинная сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-188">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="dee50-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>Двусторонняя **короткая сторона** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-189"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-190">Двусторонняя короткая сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-190">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="dee50-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Книжная** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-191"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="dee50-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Альбомная** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-192"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="dee50-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Обратная книжная** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-193"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="dee50-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Обратная альбомная** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-194"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="dee50-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Высокое качество** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-195"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-196">Высокое качество</span><span class="sxs-lookup"><span data-stu-id="dee50-196">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="dee50-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Нормальное качество** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-197"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-198">Нормальное качество</span><span class="sxs-lookup"><span data-stu-id="dee50-198">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="dee50-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Низкое качество** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-199"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-200">Низкое качество</span><span class="sxs-lookup"><span data-stu-id="dee50-200">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-201">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="dee50-201">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-202">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-202">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-204">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ принтер CIM**".**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="dee50-204">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-205">Строки произвольной формы, содержащие подробные объяснения для любой из возможностей принтера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="dee50-205">Free-form strings that provide detailed explanations for any of the printer features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="dee50-206">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="dee50-206">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="dee50-207">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dee50-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-210">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dee50-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-211">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dee50-211">Short textual description of the object.</span></span>

<span data-ttu-id="dee50-212">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dee50-212">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-213">**чарсетссуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-213">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-214">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-216">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. CharSet"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Принтер IETF — MIB. пртлокализатиончарактерсет ")</span><span class="sxs-lookup"><span data-stu-id="dee50-216">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-217">Доступные наборы символов для вывода текста, связанного с управлением принтером.</span><span class="sxs-lookup"><span data-stu-id="dee50-217">Available character sets for the output of text related to managing the printer.</span></span> <span data-ttu-id="dee50-218">Строки, предоставленные в этом свойстве, должны соответствовать семантике и синтаксису, заданному в разделе 4.1.2 ("параметр charset") в RFC 2046 (MIME Part 2), и содержатся в реестре набора символов IANA.</span><span class="sxs-lookup"><span data-stu-id="dee50-218">Strings provided in this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="dee50-219">Примеры: UTF-8, US-ASCII и ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="dee50-219">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="dee50-220">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dee50-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-221">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-223">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dee50-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-224">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dee50-224">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dee50-225">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dee50-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="dee50-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dee50-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-228">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="dee50-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dee50-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="dee50-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dee50-230">(1)</span><span class="sxs-lookup"><span data-stu-id="dee50-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-231">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="dee50-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dee50-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dee50-233">(2)</span><span class="sxs-lookup"><span data-stu-id="dee50-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dee50-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="dee50-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dee50-235">(3)</span><span class="sxs-lookup"><span data-stu-id="dee50-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-236">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dee50-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dee50-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dee50-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dee50-238">(4)</span><span class="sxs-lookup"><span data-stu-id="dee50-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-239">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dee50-239">Device is not working properly.</span></span> <span data-ttu-id="dee50-240">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dee50-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dee50-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="dee50-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dee50-242">(5)</span><span class="sxs-lookup"><span data-stu-id="dee50-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-243">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="dee50-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dee50-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="dee50-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dee50-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-246">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="dee50-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dee50-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="dee50-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dee50-248">(7)</span><span class="sxs-lookup"><span data-stu-id="dee50-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dee50-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dee50-250">(8)</span><span class="sxs-lookup"><span data-stu-id="dee50-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-251">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dee50-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dee50-253">(9)</span><span class="sxs-lookup"><span data-stu-id="dee50-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-254">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dee50-254">Device is not working properly.</span></span> <span data-ttu-id="dee50-255">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-255">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dee50-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="dee50-256"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dee50-257">(10)</span><span class="sxs-lookup"><span data-stu-id="dee50-257">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-258">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="dee50-258">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dee50-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-259"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dee50-260">(11)</span><span class="sxs-lookup"><span data-stu-id="dee50-260">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-261">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-261">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dee50-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="dee50-262"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dee50-263">(12)</span><span class="sxs-lookup"><span data-stu-id="dee50-263">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-264">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="dee50-264">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dee50-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-265"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dee50-266">(13)</span><span class="sxs-lookup"><span data-stu-id="dee50-266">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-267">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-267">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dee50-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="dee50-268"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dee50-269">(14)</span><span class="sxs-lookup"><span data-stu-id="dee50-269">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-270">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="dee50-270">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dee50-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="dee50-271"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dee50-272">(15)</span><span class="sxs-lookup"><span data-stu-id="dee50-272">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-273">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="dee50-273">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dee50-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dee50-274"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dee50-275">(16)</span><span class="sxs-lookup"><span data-stu-id="dee50-275">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-276">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="dee50-276">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dee50-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="dee50-277"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dee50-278">(17)</span><span class="sxs-lookup"><span data-stu-id="dee50-278">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-279">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="dee50-279">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dee50-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-280"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dee50-281">(18)</span><span class="sxs-lookup"><span data-stu-id="dee50-281">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-282">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dee50-282">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dee50-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="dee50-283"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dee50-284">(19)</span><span class="sxs-lookup"><span data-stu-id="dee50-284">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dee50-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dee50-285"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dee50-286">(20)</span><span class="sxs-lookup"><span data-stu-id="dee50-286">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-287">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dee50-287">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dee50-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="dee50-288"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dee50-289">(21)</span><span class="sxs-lookup"><span data-stu-id="dee50-289">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-290">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dee50-290">System failure.</span></span> <span data-ttu-id="dee50-291">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dee50-291">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dee50-292">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="dee50-292">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dee50-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="dee50-293"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dee50-294">(22)</span><span class="sxs-lookup"><span data-stu-id="dee50-294">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-295">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dee50-295">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dee50-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="dee50-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dee50-297">(23)</span><span class="sxs-lookup"><span data-stu-id="dee50-297">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-298">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dee50-298">System failure.</span></span> <span data-ttu-id="dee50-299">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dee50-299">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dee50-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="dee50-300"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dee50-301">(24)</span><span class="sxs-lookup"><span data-stu-id="dee50-301">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-302">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="dee50-302">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dee50-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dee50-303"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dee50-304">(25)</span><span class="sxs-lookup"><span data-stu-id="dee50-304">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-305">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dee50-305">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dee50-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dee50-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dee50-307">(26)</span><span class="sxs-lookup"><span data-stu-id="dee50-307">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-308">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dee50-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dee50-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="dee50-309"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dee50-310">(27)</span><span class="sxs-lookup"><span data-stu-id="dee50-310">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-311">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="dee50-311">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dee50-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="dee50-312"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dee50-313">(28)</span><span class="sxs-lookup"><span data-stu-id="dee50-313">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-314">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="dee50-314">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dee50-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="dee50-315"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dee50-316">(29)</span><span class="sxs-lookup"><span data-stu-id="dee50-316">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-317">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dee50-317">Device is disabled.</span></span> <span data-ttu-id="dee50-318">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dee50-318">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dee50-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dee50-319"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dee50-320">(30)</span><span class="sxs-lookup"><span data-stu-id="dee50-320">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-321">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="dee50-321">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dee50-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dee50-322"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dee50-323">1-31</span><span class="sxs-lookup"><span data-stu-id="dee50-323">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-324">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dee50-324">Device is not working properly.</span></span> <span data-ttu-id="dee50-325">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dee50-325">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-326">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dee50-326">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-327">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dee50-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-329">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dee50-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-330">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="dee50-330">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dee50-331">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-332">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dee50-332">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-335">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dee50-335">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dee50-336">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dee50-336">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dee50-337">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="dee50-337">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dee50-338">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-338">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-339">**курренткапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dee50-339">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-340">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dee50-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-342">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="dee50-342">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-343">Завершения и другие возможности принтера, используемые в данный момент.</span><span class="sxs-lookup"><span data-stu-id="dee50-343">Finishings and other capabilities of the printer that are currently in use.</span></span> <span data-ttu-id="dee50-344">Каждая запись в этом свойстве также должна быть указана в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="dee50-344">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="dee50-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Цветная печать** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-347"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="dee50-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Дуплексная печать** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-348"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="dee50-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Копии** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-349"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="dee50-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Параметры сортировки** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-350"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="dee50-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Сшивание** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-351"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="dee50-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Прозрачная печать** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-352"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="dee50-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Дырокол** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-353"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="dee50-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Покрытие** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-354"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="dee50-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-355"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="dee50-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Черно-белая печать** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-356"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="dee50-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Одна сторона** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-357"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-358">Одна сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-358">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="dee50-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>Двусторонняя **сторона** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-359"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-360">Двусторонняя длинная сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-360">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="dee50-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>Двусторонняя **короткая сторона** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-361"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-362">Двусторонняя короткая сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-362">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="dee50-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Книжная** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-363"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="dee50-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Альбомная** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-364"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="dee50-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Обратная книжная** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-365"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="dee50-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Обратная альбомная** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-366"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="dee50-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Высокое качество** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-367"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-368">Высокое качество</span><span class="sxs-lookup"><span data-stu-id="dee50-368">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="dee50-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Нормальное качество** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-369"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-370">Нормальное качество</span><span class="sxs-lookup"><span data-stu-id="dee50-370">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="dee50-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Низкое качество** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-371"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-372">Низкое качество</span><span class="sxs-lookup"><span data-stu-id="dee50-372">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-373">**куррентчарсет**</span><span class="sxs-lookup"><span data-stu-id="dee50-373">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-376">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Чарсетссуппортед**")</span><span class="sxs-lookup"><span data-stu-id="dee50-376">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-377">Текущая кодировка, используемая для вывода текста, относящегося к управлению принтером.</span><span class="sxs-lookup"><span data-stu-id="dee50-377">Current character set used for the output of text relating to management of the printer.</span></span> <span data-ttu-id="dee50-378">Кодировка, описываемая этим свойством, также должна быть указана в свойстве **чарсетссуппортед** .</span><span class="sxs-lookup"><span data-stu-id="dee50-378">The character set described by this property should also be listed in the **CharsetsSupported** property.</span></span> <span data-ttu-id="dee50-379">Строка, заданная этим свойством, должна соответствовать семантике и синтаксису, заданным в разделе 4.1.2 ("параметр charset") в стандарте RFC 2046 (MIME Part 2), и содержится в реестре набора символов IANA.</span><span class="sxs-lookup"><span data-stu-id="dee50-379">The string specified by this property should conform to the semantics and syntax specified by section 4.1.2 ("Charset parameter") in RFC 2046 (MIME Part 2), and contained in the IANA character-set registry.</span></span> <span data-ttu-id="dee50-380">Примеры: UTF-8, US-ASCII и ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="dee50-380">Examples include "utf-8", "us-ascii", and "iso-8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="dee50-381">**куррентлангуаже**</span><span class="sxs-lookup"><span data-stu-id="dee50-381">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-382">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-384">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**". Лангуажессуппортед "," CIM \_ Printer. куррентмиметипе ")</span><span class="sxs-lookup"><span data-stu-id="dee50-384">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.CurrentMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-385">Используется текущий язык принтера; язык также должен быть указан в свойстве **лангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="dee50-385">Current printer language being used; the language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-386">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-386">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-387">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-387">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="dee50-388">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-388">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="dee50-389">**Хпгл** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-389">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="dee50-390">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-390">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="dee50-391">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-391">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="dee50-392">**Пспринтер** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-392">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="dee50-393">**ИПДС** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-393">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="dee50-394">**Ппдс** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-394">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="dee50-395">**Ескапеп** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-395">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="dee50-396">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-396">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="dee50-397">**Ддиф** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-397">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="dee50-398">**Перенажатие** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-398">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="dee50-399">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-399">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="dee50-400">**Данные линии** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-400">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="dee50-401">**Модка** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-401">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="dee50-402">**Реджис** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-402">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="dee50-403">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-403">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="dee50-404">**Спдл** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-404">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="dee50-405">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-405">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="dee50-406">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-406">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="dee50-407">**ИГП** (22)</span><span class="sxs-lookup"><span data-stu-id="dee50-407">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="dee50-408">**Кодев** (23)</span><span class="sxs-lookup"><span data-stu-id="dee50-408">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="dee50-409">**Дскдсе** (24)</span><span class="sxs-lookup"><span data-stu-id="dee50-409">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="dee50-410">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="dee50-410">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="dee50-411">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="dee50-411">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="dee50-412">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="dee50-412">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="dee50-413">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="dee50-413">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="dee50-414">**КПАП** (29)</span><span class="sxs-lookup"><span data-stu-id="dee50-414">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="dee50-415">**Декппл** (30)</span><span class="sxs-lookup"><span data-stu-id="dee50-415">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="dee50-416">**Простой текст** (31)</span><span class="sxs-lookup"><span data-stu-id="dee50-416">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="dee50-417">**Нпап** (32)</span><span class="sxs-lookup"><span data-stu-id="dee50-417">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="dee50-418">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="dee50-418">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="dee50-419">**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="dee50-419">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="dee50-420">**Пинвритер** (35)</span><span class="sxs-lookup"><span data-stu-id="dee50-420">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="dee50-421">**НПДЛ** (36)</span><span class="sxs-lookup"><span data-stu-id="dee50-421">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="dee50-422">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="dee50-422">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="dee50-423">**Автоматически** (38)</span><span class="sxs-lookup"><span data-stu-id="dee50-423">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="dee50-424">**Страницы** (39)</span><span class="sxs-lookup"><span data-stu-id="dee50-424">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="dee50-425">**LIP** (40)</span><span class="sxs-lookup"><span data-stu-id="dee50-425">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="dee50-426">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="dee50-426">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="dee50-427">**Диагностика** (42)</span><span class="sxs-lookup"><span data-stu-id="dee50-427">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="dee50-428">**Cap** (43)</span><span class="sxs-lookup"><span data-stu-id="dee50-428">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="dee50-429">**Без** (44)</span><span class="sxs-lookup"><span data-stu-id="dee50-429">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="dee50-430">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="dee50-430">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="dee50-431">**Хранять** (46)</span><span class="sxs-lookup"><span data-stu-id="dee50-431">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="dee50-432">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="dee50-432">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-433">**куррентмиметипе**</span><span class="sxs-lookup"><span data-stu-id="dee50-433">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-436">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Куррентлангуаже**")</span><span class="sxs-lookup"><span data-stu-id="dee50-436">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-437">Тип MIME, используемый принтером в настоящее время, если свойство **куррентлангуаже** имеет значение, указывающее, что используется тип MIME.</span><span class="sxs-lookup"><span data-stu-id="dee50-437">Mime type currently in use by the printer when the **CurrentLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-438">**куррентнатураллангуаже**</span><span class="sxs-lookup"><span data-stu-id="dee50-438">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-439">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-440">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-440">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-441">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Натураллангуажессуппортед**")</span><span class="sxs-lookup"><span data-stu-id="dee50-441">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-442">Текущий язык, используемый принтером для управления.</span><span class="sxs-lookup"><span data-stu-id="dee50-442">Current language in use by the printer for management.</span></span> <span data-ttu-id="dee50-443">Язык, указанный здесь, также должен быть указан в **натураллангуажессуппортед**.</span><span class="sxs-lookup"><span data-stu-id="dee50-443">The language listed here should also be listed in **NaturalLanguagesSupported**.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-444">**куррентпапертипе**</span><span class="sxs-lookup"><span data-stu-id="dee50-444">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-447">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Папертипесаваилабле**")</span><span class="sxs-lookup"><span data-stu-id="dee50-447">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-448">Тип бумаги, используемый принтером в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="dee50-448">Paper type currently in use by the printer.</span></span> <span data-ttu-id="dee50-449">Строка должна быть выражена в форме, заданной в приложении для печати документов ISO/IEC 10175 (DPA), которое также суммируется в приложении C из RFC 1759 (версия-MIB принтера).</span><span class="sxs-lookup"><span data-stu-id="dee50-449">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-450">**дефаулткапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dee50-450">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-451">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dee50-451">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-453">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="dee50-453">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-454">Окончания по умолчанию и другие возможности принтера.</span><span class="sxs-lookup"><span data-stu-id="dee50-454">Default finishings and other capabilities of the printer.</span></span> <span data-ttu-id="dee50-455">Каждая запись в этом свойстве также должна быть указана в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="dee50-455">Each entry in this property should also be listed in the **Capabilities** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="dee50-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Цветная печать** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-458"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="dee50-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Дуплексная печать** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-459"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="dee50-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Копии** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-460"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="dee50-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Параметры сортировки** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-461"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="dee50-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Сшивание** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-462"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="dee50-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Прозрачная печать** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-463"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="dee50-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Дырокол** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-464"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="dee50-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Покрытие** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-465"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="dee50-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-466"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="dee50-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Черно-белая печать** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-467"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="dee50-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Одна сторона** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-468"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-469">Одна сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-469">One-sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="dee50-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>Двусторонняя **сторона** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-470"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-471">Двусторонняя длинная сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-471">Two-sided long edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="dee50-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>Двусторонняя **короткая сторона** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-472"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-473">Двусторонняя короткая сторона</span><span class="sxs-lookup"><span data-stu-id="dee50-473">Two-sided short edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="dee50-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Книжная** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-474"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="dee50-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Альбомная** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-475"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="dee50-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Обратная книжная** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-476"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="dee50-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Обратная альбомная** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-477"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="dee50-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Высокое качество** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-478"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-479">Высокое качество</span><span class="sxs-lookup"><span data-stu-id="dee50-479">Quality high</span></span>

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="dee50-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Нормальное качество** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-480"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-481">Нормальное качество</span><span class="sxs-lookup"><span data-stu-id="dee50-481">Quality normal</span></span>

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="dee50-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Низкое качество** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-482"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-483">Низкое качество</span><span class="sxs-lookup"><span data-stu-id="dee50-483">Quality low</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-484">**дефаулткопиес**</span><span class="sxs-lookup"><span data-stu-id="dee50-484">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-485">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-485">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-487">Количество копий, которое будет выдавать одно задание, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="dee50-487">Number of copies that a single job will produce, unless otherwise specified.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-488">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="dee50-488">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-489">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-489">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-490">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-490">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-491">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**". Лангуажессуппортед "," CIM \_ Printer. дефаултмиметипе ")</span><span class="sxs-lookup"><span data-stu-id="dee50-491">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_Printer.DefaultMimeType")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-492">Язык принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dee50-492">Default printer language.</span></span> <span data-ttu-id="dee50-493">Язык также должен быть указан в свойстве **лангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="dee50-493">The language should also be listed in the **LanguagesSupported** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-494">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-494">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-495">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-495">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="dee50-496">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-496">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="dee50-497">**Хпгл** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-497">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="dee50-498">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-498">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="dee50-499">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-499">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="dee50-500">**Пспринтер** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-500">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="dee50-501">**ИПДС** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-501">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="dee50-502">**Ппдс** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-502">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="dee50-503">**Ескапеп** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-503">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="dee50-504">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-504">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="dee50-505">**Ддиф** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-505">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="dee50-506">**Перенажатие** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-506">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="dee50-507">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-507">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="dee50-508">**Данные линии** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-508">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="dee50-509">**Модка** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-509">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="dee50-510">**Реджис** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-510">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="dee50-511">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-511">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="dee50-512">**Спдл** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-512">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="dee50-513">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-513">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="dee50-514">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-514">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="dee50-515">**ИГП** (22)</span><span class="sxs-lookup"><span data-stu-id="dee50-515">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="dee50-516">**Кодев** (23)</span><span class="sxs-lookup"><span data-stu-id="dee50-516">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="dee50-517">**Дскдсе** (24)</span><span class="sxs-lookup"><span data-stu-id="dee50-517">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="dee50-518">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="dee50-518">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="dee50-519">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="dee50-519">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="dee50-520">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="dee50-520">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="dee50-521">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="dee50-521">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="dee50-522">**КПАП** (29)</span><span class="sxs-lookup"><span data-stu-id="dee50-522">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="dee50-523">**Декппл** (30)</span><span class="sxs-lookup"><span data-stu-id="dee50-523">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="dee50-524">**Простой текст** (31)</span><span class="sxs-lookup"><span data-stu-id="dee50-524">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="dee50-525">**Нпап** (32)</span><span class="sxs-lookup"><span data-stu-id="dee50-525">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="dee50-526">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="dee50-526">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="dee50-527">**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="dee50-527">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="dee50-528">**Пинвритер** (35)</span><span class="sxs-lookup"><span data-stu-id="dee50-528">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="dee50-529">**НПДЛ** (36)</span><span class="sxs-lookup"><span data-stu-id="dee50-529">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="dee50-530">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="dee50-530">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="dee50-531">**Автоматически** (38)</span><span class="sxs-lookup"><span data-stu-id="dee50-531">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="dee50-532">**Страницы** (39)</span><span class="sxs-lookup"><span data-stu-id="dee50-532">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="dee50-533">**LIP** (40)</span><span class="sxs-lookup"><span data-stu-id="dee50-533">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="dee50-534">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="dee50-534">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="dee50-535">**Диагностика** (42)</span><span class="sxs-lookup"><span data-stu-id="dee50-535">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="dee50-536">**Cap** (43)</span><span class="sxs-lookup"><span data-stu-id="dee50-536">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="dee50-537">**Без** (44)</span><span class="sxs-lookup"><span data-stu-id="dee50-537">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="dee50-538">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="dee50-538">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="dee50-539">**Хранять** (46)</span><span class="sxs-lookup"><span data-stu-id="dee50-539">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="dee50-540">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="dee50-540">**MIME** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-541">**дефаултмиметипе**</span><span class="sxs-lookup"><span data-stu-id="dee50-541">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-542">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-543">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-544">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="dee50-544">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-545">Тип MIME по умолчанию, используемый принтером, если свойство **DefaultLanguage** имеет значение, указывающее, что используется тип MIME.</span><span class="sxs-lookup"><span data-stu-id="dee50-545">Default mime type used by the printer when the **DefaultLanguage** property is set to indicate that a mime type is in use.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-546">**дефаултнумберуп**</span><span class="sxs-lookup"><span data-stu-id="dee50-546">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-547">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-547">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-549">Количество страниц на печатном потоке, которые принтер будет отображать на одном листе мультимедиа, если в задании не указано иное.</span><span class="sxs-lookup"><span data-stu-id="dee50-549">Number of print-stream pages that the printer will render onto a single media sheet, unless a job specifies otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-550">**дефаултпапертипе**</span><span class="sxs-lookup"><span data-stu-id="dee50-550">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-551">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-551">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-552">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-552">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-553">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Папертипесаваилабле**")</span><span class="sxs-lookup"><span data-stu-id="dee50-553">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-554">Тип бумаги, который будет использоваться принтером, если в PrintJob не указан определенный тип.</span><span class="sxs-lookup"><span data-stu-id="dee50-554">Paper type that the printer will use if PrintJob does not specify a particular type.</span></span> <span data-ttu-id="dee50-555">Строка должна быть выражена в форме, заданной в приложении для печати документов ISO/IEC 10175 (DPA), которое также суммируется в приложении C из RFC 1759 (версия-MIB принтера).</span><span class="sxs-lookup"><span data-stu-id="dee50-555">The string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-556">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dee50-556">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-557">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-557">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-558">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-558">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-559">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="dee50-559">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-560">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dee50-560">Textual description of the object.</span></span>

<span data-ttu-id="dee50-561">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dee50-561">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-562">**детектедеррорстате**</span><span class="sxs-lookup"><span data-stu-id="dee50-562">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-563">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-563">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-564">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-564">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-565">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Ерроринформатион**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. \|Принтер IETF — MIB. хрпринтердетектедеррорстате ")</span><span class="sxs-lookup"><span data-stu-id="dee50-565">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-566">Сведения об ошибках принтера.</span><span class="sxs-lookup"><span data-stu-id="dee50-566">Printer error information.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-567">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-567">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-568">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-568">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="dee50-569">**Без ошибок** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-569">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="dee50-570">**Мало бумаги** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-570">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="dee50-571">**Нет бумаги** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-571">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="dee50-572">**Низкий тонер** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-572">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="dee50-573">**Нет тонера** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-573">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="dee50-574">**Открыта дверца** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-574">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="dee50-575">**Застревание бумаги** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-575">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="dee50-576">**Вне сети** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-576">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="dee50-577">**Запрошенная служба** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-577">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="dee50-578">**Выходной лоток полон** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-578">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-579">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dee50-579">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-580">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-581">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-581">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-582">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dee50-582">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dee50-583">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-583">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="dee50-584">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-584">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-585">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="dee50-585">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-586">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dee50-586">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-587">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-587">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-588">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="dee50-588">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="dee50-589">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-589">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-590">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dee50-590">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-591">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-591">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-592">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-592">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-593">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="dee50-593">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="dee50-594">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-594">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-595">**ерроринформатион**</span><span class="sxs-lookup"><span data-stu-id="dee50-595">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-596">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-596">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-597">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dee50-597">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dee50-598">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**".**Детектедеррорстате**")</span><span class="sxs-lookup"><span data-stu-id="dee50-598">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-599">Массив, предоставляющий дополнительные сведения о текущем состоянии ошибки, указанные в свойстве **детектедеррорстате** .</span><span class="sxs-lookup"><span data-stu-id="dee50-599">Array that provides supplemental information for the current error state, indicated in the **DetectedErrorState** property.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-600">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="dee50-600">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-601">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-601">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-602">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-603">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. хоризонталресолутион"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей на дюйм")</span><span class="sxs-lookup"><span data-stu-id="dee50-603">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-604">Разрешение по горизонтали в пикселях на дюйм.</span><span class="sxs-lookup"><span data-stu-id="dee50-604">Horizontal resolution in pixels-per-inch.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-605">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dee50-605">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-606">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dee50-606">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-607">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-608">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="dee50-608">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-609">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="dee50-609">Date and time the object was installed.</span></span> <span data-ttu-id="dee50-610">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="dee50-610">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dee50-611">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dee50-611">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-612">**жобкаунтсинцеластресет**</span><span class="sxs-lookup"><span data-stu-id="dee50-612">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-613">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-613">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-614">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-614">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-615">Квалификаторы: **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="dee50-615">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="dee50-616">Задания принтера, обработанные с момента последнего сброса.</span><span class="sxs-lookup"><span data-stu-id="dee50-616">Printer jobs processed since the last reset.</span></span> <span data-ttu-id="dee50-617">Эти задания могут быть обработаны из одной или нескольких очередей печати.</span><span class="sxs-lookup"><span data-stu-id="dee50-617">These jobs can be processed from one or more print queues.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-618">**лангуажессуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-618">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-619">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dee50-619">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-620">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-620">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-621">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Принтер IETF — MIB. пртинтерпретерлангфамили "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**". Миметипессуппортед "," CIM \_ PrintJob. Language "," CIM \_ Принтсервице. лангуажессуппортед ")</span><span class="sxs-lookup"><span data-stu-id="dee50-621">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-622">Языки печати, изначально поддерживаемые.</span><span class="sxs-lookup"><span data-stu-id="dee50-622">Print languages that are natively supported.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-623">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-623">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-624">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-624">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="dee50-625">**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-625">**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="dee50-626">**Хпгл** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-626">**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="dee50-627">**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-627">**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="dee50-628">**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-628">**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="dee50-629">**Пспринтер** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-629">**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="dee50-630">**ИПДС** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-630">**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="dee50-631">**Ппдс** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-631">**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="dee50-632">**Ескапеп** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-632">**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="dee50-633">**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-633">**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="dee50-634">**Ддиф** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-634">**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="dee50-635">**Перенажатие** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-635">**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="dee50-636">**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-636">**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="dee50-637">**Данные линии** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-637">**Line Data** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="dee50-638">**Модка** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-638">**MODCA** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="dee50-639">**Реджис** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-639">**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="dee50-640">**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-640">**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="dee50-641">**Спдл** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-641">**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="dee50-642">**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-642">**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="dee50-643">**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-643">**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="dee50-644">**ИГП** (22)</span><span class="sxs-lookup"><span data-stu-id="dee50-644">**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="dee50-645">**Кодев** (23)</span><span class="sxs-lookup"><span data-stu-id="dee50-645">**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="dee50-646">**Дскдсе** (24)</span><span class="sxs-lookup"><span data-stu-id="dee50-646">**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="dee50-647">**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="dee50-647">**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="dee50-648">**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="dee50-648">**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="dee50-649">**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="dee50-649">**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="dee50-650">**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="dee50-650">**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="dee50-651">**КПАП** (29)</span><span class="sxs-lookup"><span data-stu-id="dee50-651">**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="dee50-652">**Декппл** (30)</span><span class="sxs-lookup"><span data-stu-id="dee50-652">**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="dee50-653">**Простой текст** (31)</span><span class="sxs-lookup"><span data-stu-id="dee50-653">**Simple Text** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="dee50-654">**Нпап** (32)</span><span class="sxs-lookup"><span data-stu-id="dee50-654">**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="dee50-655">**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="dee50-655">**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="dee50-656">**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="dee50-656">**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="dee50-657">**Пинвритер** (35)</span><span class="sxs-lookup"><span data-stu-id="dee50-657">**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="dee50-658">**НПДЛ** (36)</span><span class="sxs-lookup"><span data-stu-id="dee50-658">**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="dee50-659">**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="dee50-659">**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="dee50-660">**Автоматически** (38)</span><span class="sxs-lookup"><span data-stu-id="dee50-660">**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="dee50-661">**Страницы** (39)</span><span class="sxs-lookup"><span data-stu-id="dee50-661">**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="dee50-662">**LIP** (40)</span><span class="sxs-lookup"><span data-stu-id="dee50-662">**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="dee50-663">**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="dee50-663">**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="dee50-664">**Диагностика** (42)</span><span class="sxs-lookup"><span data-stu-id="dee50-664">**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="dee50-665">**Cap** (43)</span><span class="sxs-lookup"><span data-stu-id="dee50-665">**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="dee50-666">**Без** (44)</span><span class="sxs-lookup"><span data-stu-id="dee50-666">**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="dee50-667">**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="dee50-667">**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="dee50-668">**Хранять** (46)</span><span class="sxs-lookup"><span data-stu-id="dee50-668">**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="dee50-669">**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="dee50-669">**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="dee50-670">**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="dee50-670">**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="dee50-671">**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="dee50-671">**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="dee50-672">**Пклксл** (50)</span><span class="sxs-lookup"><span data-stu-id="dee50-672">**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-673">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dee50-673">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-674">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-674">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-675">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-675">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-676">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="dee50-676">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dee50-677">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-677">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-678">**маркингтечнологи**</span><span class="sxs-lookup"><span data-stu-id="dee50-678">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-679">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-679">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-680">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-680">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-681">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Принтер IETF — MIB. пртмаркермарктеч ")</span><span class="sxs-lookup"><span data-stu-id="dee50-681">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-682">Маркировка технологии, используемой принтером.</span><span class="sxs-lookup"><span data-stu-id="dee50-682">Marking technology used by the printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-683">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-683">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-684">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-684">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="dee50-685">**Светоиндикатор електрофотографик** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-685">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="dee50-686">**Електрофотографик лазерный** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-686">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="dee50-687">**Електрофотографик** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-687">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="dee50-688">**Влияние перемещения головной точки на матрицу 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-688">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="dee50-689">**Влияние перемещения головной точки на матрицу 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-689">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="dee50-690">**Влияние перемещения головной точки на другую матрицу** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-690">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="dee50-691">**Полностью сформированный головной заголовк влияния** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-691">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="dee50-692">**Полоса влияния** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-692">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="dee50-693">**Воздействие на другое** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-693">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="dee50-694">**Струйный акуеаус** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-694">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="dee50-695">**Сплошная струйная** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-695">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="dee50-696">**Струйная** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-696">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="dee50-697">**Перо** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-697">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="dee50-698">**Перенос тепла** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-698">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="dee50-699">**С учетом температуры** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-699">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="dee50-700">**Рассеяние тепла** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-700">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="dee50-701">**Прочая температура** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-701">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="dee50-702">**Електроеросион** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-702">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="dee50-703">**Статические** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-703">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="dee50-704">**Фотограф микрофишей** (22)</span><span class="sxs-lookup"><span data-stu-id="dee50-704">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="dee50-705">**Фотографический автомат** (23)</span><span class="sxs-lookup"><span data-stu-id="dee50-705">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="dee50-706">**Фотографическая другая** (24)</span><span class="sxs-lookup"><span data-stu-id="dee50-706">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="dee50-707">**Литий-спуск** (25)</span><span class="sxs-lookup"><span data-stu-id="dee50-707">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="dee50-708">**ебеам** (26)</span><span class="sxs-lookup"><span data-stu-id="dee50-708">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="dee50-709">**Типесеттер** (27)</span><span class="sxs-lookup"><span data-stu-id="dee50-709">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-710">**макскопиес**</span><span class="sxs-lookup"><span data-stu-id="dee50-710">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-711">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-711">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-712">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-712">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-713">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. копий")</span><span class="sxs-lookup"><span data-stu-id="dee50-713">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-714">Максимальное количество копий, которое может быть создано принтером из одного задания.</span><span class="sxs-lookup"><span data-stu-id="dee50-714">Maximum number of copies that can be produced by the printer from a single job.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-715">**макснумберуп**</span><span class="sxs-lookup"><span data-stu-id="dee50-715">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-716">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-716">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-717">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-717">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-718">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. нумберуп")</span><span class="sxs-lookup"><span data-stu-id="dee50-718">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-719">Максимальное количество страниц в потоке печати, которое принтер может визуализировать на одном листе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="dee50-719">Maximum number of print-stream pages that the printer can render onto a single media sheet.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-720">**макссизесуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-720">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-721">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-721">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-722">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-722">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-723">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. жобсизе"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("килобайты")</span><span class="sxs-lookup"><span data-stu-id="dee50-723">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.JobSize"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-724">Большое задание (в виде потока байтов), которое принтер будет принимать в виде единиц в килобайтах.</span><span class="sxs-lookup"><span data-stu-id="dee50-724">Largest job (as a byte stream) that the printer will accept in units of kilobytes.</span></span> <span data-ttu-id="dee50-725">Значение 0 (ноль) указывает, что ограничение не задано.</span><span class="sxs-lookup"><span data-stu-id="dee50-725">A value of 0 (zero) indicates that no limit has been set.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-726">**миметипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-726">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-727">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-727">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-728">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-728">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-729">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ принтер**". Лангуажессуппортед "," CIM \_ PrintJob. миметипес "," CIM \_ Принтсервице. миметипессуппортед ")</span><span class="sxs-lookup"><span data-stu-id="dee50-729">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Printer**.LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-730">Строки произвольной формы, предоставляющие подробные объяснения типов MIME, поддерживаемых принтером.</span><span class="sxs-lookup"><span data-stu-id="dee50-730">Free-form strings that provide detailed explanations of mime types that are supported by the printer.</span></span> <span data-ttu-id="dee50-731">Если для этого свойства предоставлены данные, то значение 47 ("MIME") должно быть включено в свойство **лангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="dee50-731">If data is provided for this property, then the value 47 ("Mime"), should be included in the **LanguagesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-732">**Name**</span><span class="sxs-lookup"><span data-stu-id="dee50-732">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-733">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-733">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-734">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-734">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-735">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="dee50-735">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-736">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dee50-736">Label by which the object is known.</span></span> <span data-ttu-id="dee50-737">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="dee50-737">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dee50-738">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dee50-738">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-739">**натураллангуажессуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-739">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-740">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-740">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-741">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-741">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-742">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. пртлокализатионлангуаже "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ PrintJob. натураллангуаже ")</span><span class="sxs-lookup"><span data-stu-id="dee50-742">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-743">Доступные языки для строк, используемых принтером для выходных данных управления.</span><span class="sxs-lookup"><span data-stu-id="dee50-743">Available languages for strings used by the printer for management information output.</span></span> <span data-ttu-id="dee50-744">Строки должны соответствовать стандарту RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="dee50-744">The strings should conform to RFC 1766.</span></span> <span data-ttu-id="dee50-745">Например, EN используется для английского языка.</span><span class="sxs-lookup"><span data-stu-id="dee50-745">For example, "en" is used for English.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-746">**паперсизессуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-746">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-747">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dee50-747">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-748">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-748">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-749">Поддерживаемые типы бумаги.</span><span class="sxs-lookup"><span data-stu-id="dee50-749">Types of paper supported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-750">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-750">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-751">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-751">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="dee50-752">**A** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-752">**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="dee50-753">**Б** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-753">**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="dee50-754">**C** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-754">**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="dee50-755">**D** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-755">**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="dee50-756">**E** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-756">**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="dee50-757">**Letter** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-757">**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="dee50-758">**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="dee50-758">**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="dee50-759">**Na-10x13-конверт** (9)</span><span class="sxs-lookup"><span data-stu-id="dee50-759">**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="dee50-760">**Конверт Na-9x12** (10)</span><span class="sxs-lookup"><span data-stu-id="dee50-760">**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="dee50-761">**Na-Number-10-конверт** (11)</span><span class="sxs-lookup"><span data-stu-id="dee50-761">**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="dee50-762">**Конверт Na-7x9** (12)</span><span class="sxs-lookup"><span data-stu-id="dee50-762">**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="dee50-763">**Конверт Na-9x11** (13)</span><span class="sxs-lookup"><span data-stu-id="dee50-763">**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="dee50-764">**Конверт Na-10x14** (14)</span><span class="sxs-lookup"><span data-stu-id="dee50-764">**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="dee50-765">**Na-Number-9-конверт** (15)</span><span class="sxs-lookup"><span data-stu-id="dee50-765">**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="dee50-766">**Na-6x9-конверт** (16)</span><span class="sxs-lookup"><span data-stu-id="dee50-766">**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="dee50-767">**Конверт Na-10x15** (17)</span><span class="sxs-lookup"><span data-stu-id="dee50-767">**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="dee50-768">**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="dee50-768">**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="dee50-769">**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="dee50-769">**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="dee50-770">**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="dee50-770">**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="dee50-771">**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="dee50-771">**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="dee50-772">**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="dee50-772">**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="dee50-773">**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="dee50-773">**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="dee50-774">**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="dee50-774">**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="dee50-775">**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="dee50-775">**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="dee50-776">**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="dee50-776">**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="dee50-777">**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="dee50-777">**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="dee50-778">**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="dee50-778">**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="dee50-779">**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="dee50-779">**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="dee50-780">**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="dee50-780">**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="dee50-781">**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="dee50-781">**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="dee50-782">**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="dee50-782">**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="dee50-783">**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="dee50-783">**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="dee50-784">**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="dee50-784">**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="dee50-785">**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="dee50-785">**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="dee50-786">**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="dee50-786">**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="dee50-787">**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="dee50-787">**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="dee50-788">**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="dee50-788">**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="dee50-789">**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="dee50-789">**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="dee50-790">**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="dee50-790">**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="dee50-791">**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="dee50-791">**C2C3** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="dee50-792">**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="dee50-792">**C4** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="dee50-793">**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="dee50-793">**C5** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="dee50-794">**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="dee50-794">**C6** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="dee50-795">**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="dee50-795">**C7** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="dee50-796">**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="dee50-796">**C8** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="dee50-797">**Назначенный ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="dee50-797">**ISO-Designated** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="dee50-798">**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="dee50-798">**JIS B0** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="dee50-799">**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="dee50-799">**JIS B1** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="dee50-800">**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="dee50-800">**JIS B2** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="dee50-801">**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="dee50-801">**JIS B3** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="dee50-802">**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="dee50-802">**JIS B4** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="dee50-803">**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="dee50-803">**JIS B5** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="dee50-804">**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="dee50-804">**JIS B6** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="dee50-805">**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="dee50-805">**JIS B7** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="dee50-806">**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="dee50-806">**JIS B8** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="dee50-807">**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="dee50-807">**JIS B9** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="dee50-808">**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="dee50-808">**JIS B10** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="dee50-809">**Na-Letter** (59)</span><span class="sxs-lookup"><span data-stu-id="dee50-809">**NA-Letter** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="dee50-810">**Na-Legal** (60)</span><span class="sxs-lookup"><span data-stu-id="dee50-810">**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="dee50-811">**Конверт B4** (61)</span><span class="sxs-lookup"><span data-stu-id="dee50-811">**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="dee50-812">**Конверт B5** (62)</span><span class="sxs-lookup"><span data-stu-id="dee50-812">**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="dee50-813">**Конверт C3** (63)</span><span class="sxs-lookup"><span data-stu-id="dee50-813">**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="dee50-814">**Конверт C4** (64)</span><span class="sxs-lookup"><span data-stu-id="dee50-814">**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="dee50-815">**Конверт C5** (65)</span><span class="sxs-lookup"><span data-stu-id="dee50-815">**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="dee50-816">**Конверт C6** (66)</span><span class="sxs-lookup"><span data-stu-id="dee50-816">**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="dee50-817">**Назначено-Длинный конверт** (67)</span><span class="sxs-lookup"><span data-stu-id="dee50-817">**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="dee50-818">**Конверт монарх** (68)</span><span class="sxs-lookup"><span data-stu-id="dee50-818">**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="dee50-819">**Executive** (69)</span><span class="sxs-lookup"><span data-stu-id="dee50-819">**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="dee50-820">**Фолио** (70)</span><span class="sxs-lookup"><span data-stu-id="dee50-820">**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="dee50-821">**Счет** (71)</span><span class="sxs-lookup"><span data-stu-id="dee50-821">**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="dee50-822">**Главная книга** (72)</span><span class="sxs-lookup"><span data-stu-id="dee50-822">**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="dee50-823">**Куарто** (73)</span><span class="sxs-lookup"><span data-stu-id="dee50-823">**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-824">**папертипесаваилабле**</span><span class="sxs-lookup"><span data-stu-id="dee50-824">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-825">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dee50-825">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-826">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-826">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-827">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. рекуиредпапертипе", "CIM \_ Принтсервице. папертипесаваилабле"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Принтер IETF — MIB. пртинпутмедианаме ")</span><span class="sxs-lookup"><span data-stu-id="dee50-827">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-828">Строки произвольной формы, указывающие типы бумаги, доступные для принтера в данный момент.</span><span class="sxs-lookup"><span data-stu-id="dee50-828">Free-form strings that specify the types of paper that are currently available for the printer.</span></span> <span data-ttu-id="dee50-829">Каждая строка должна быть выражена в форме, заданной в приложении для печати документов ISO/IEC 10175 (DPA), которое также суммируется в приложении C из RFC 1759 (версия-MIB принтера).</span><span class="sxs-lookup"><span data-stu-id="dee50-829">Each string should be expressed in the form specified by ISO/IEC 10175 Document Printing Application (DPA), which is also summarized in Appendix C of RFC 1759 (Printer MIB).</span></span> <span data-ttu-id="dee50-830">Примерами допустимых строк являются "ISO-A4-цветные" и "Na-10x14-конверт".</span><span class="sxs-lookup"><span data-stu-id="dee50-830">Examples of valid strings are "iso-a4-colored" and "na-10x14-envelope".</span></span> <span data-ttu-id="dee50-831">По определению размер бумаги, который доступен и указан в свойстве **папертипесаваилабле** , также должен присутствовать в свойстве **паперсизессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="dee50-831">By definition, a paper size that is available and listed in the **PaperTypesAvailable** property should also appear in the **PaperSizesSupported** property.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-832">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dee50-832">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-833">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-834">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-834">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-835">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dee50-835">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-836">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-836">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="dee50-837">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-837">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dee50-838">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dee50-838">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dee50-839">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dee50-839">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-840">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dee50-840">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dee50-841">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-841">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-842">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="dee50-842">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dee50-843">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-843">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dee50-844"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dee50-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-845"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dee50-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-846"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dee50-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-847"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-848">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="dee50-848">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dee50-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-849"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-850">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="dee50-850">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dee50-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-851"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-852">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="dee50-852">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dee50-853">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="dee50-853">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dee50-854">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="dee50-854">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dee50-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-855"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-856">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="dee50-856">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dee50-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-857"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dee50-858">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="dee50-858">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-859">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="dee50-859">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-860">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dee50-860">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-861">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-861">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-862">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="dee50-862">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="dee50-863">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="dee50-863">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="dee50-864">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="dee50-864">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="dee50-865">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="dee50-865">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="dee50-866">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-866">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-867">**принтерстатус**</span><span class="sxs-lookup"><span data-stu-id="dee50-867">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-868">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-868">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-869">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-869">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-870">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Принтер IETF — MIB. хрпринтерстатус ")</span><span class="sxs-lookup"><span data-stu-id="dee50-870">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-871">Сведения о состоянии для принтера, кроме указанного в свойстве **доступности** .</span><span class="sxs-lookup"><span data-stu-id="dee50-871">Status information, beyond that specified in the **Availability** property, for a printer.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-872">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-872">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-873">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-873">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="dee50-874">**Бездействие** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-874">**Idle** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="dee50-875">**Печать** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-875">**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="dee50-876">**Прогрев** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-876">**Warmup** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="dee50-877">**Печать остановлена** (6)</span><span class="sxs-lookup"><span data-stu-id="dee50-877">**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="dee50-878">**Вне сети** (7)</span><span class="sxs-lookup"><span data-stu-id="dee50-878">**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-879">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dee50-879">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-880">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-880">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-881">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-881">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-882">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="dee50-882">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-883">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dee50-883">Current status of the object.</span></span> <span data-ttu-id="dee50-884">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dee50-884">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dee50-885">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="dee50-885">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dee50-886">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="dee50-886">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dee50-887">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="dee50-887">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dee50-888">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="dee50-888">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-889">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="dee50-889">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dee50-890">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="dee50-890">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dee50-891">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="dee50-891">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dee50-892">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="dee50-892">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dee50-893">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="dee50-893">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dee50-894">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="dee50-894">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dee50-895">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="dee50-895">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dee50-896">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="dee50-896">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dee50-897">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="dee50-897">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-898">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dee50-898">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-899">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dee50-899">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-900">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-900">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-901">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dee50-901">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-902">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dee50-902">State of the logical device.</span></span> <span data-ttu-id="dee50-903">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="dee50-903">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dee50-904">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-904">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dee50-905">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dee50-905">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dee50-906">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dee50-906">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dee50-907">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dee50-907">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dee50-908">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="dee50-908">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dee50-909">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="dee50-909">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dee50-910">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="dee50-910">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-911">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-911">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-912">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-913">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dee50-913">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dee50-914">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="dee50-914">Scoping system's creation class name.</span></span>

<span data-ttu-id="dee50-915">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-915">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-916">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dee50-916">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-917">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dee50-917">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-918">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-918">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-919">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dee50-919">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dee50-920">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="dee50-920">Scoping system's name.</span></span>

<span data-ttu-id="dee50-921">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dee50-921">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dee50-922">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="dee50-922">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-923">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dee50-923">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-924">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-924">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee50-925">Время последнего сброса принтера.</span><span class="sxs-lookup"><span data-stu-id="dee50-925">Time of last printer reset.</span></span>

</dd> <dt>

<span data-ttu-id="dee50-926">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="dee50-926">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee50-927">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee50-927">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee50-928">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dee50-928">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee50-929">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. хоризонталресолутион"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("пикселей на дюйм")</span><span class="sxs-lookup"><span data-stu-id="dee50-929">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="dee50-930">Разрешение по вертикали в пикселях на дюйм.</span><span class="sxs-lookup"><span data-stu-id="dee50-930">Vertical resolution in pixels-per-inch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dee50-931">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dee50-931">Remarks</span></span>

<span data-ttu-id="dee50-932">Класс **\_ принтера CIM** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="dee50-932">The **CIM\_Printer** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dee50-933">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="dee50-933">WMI does not implement this class.</span></span> <span data-ttu-id="dee50-934">Сведения о классах WMI, производных от модели CIM, см. в разделе [Классы Win32](win32-provider.md). **\_**</span><span class="sxs-lookup"><span data-stu-id="dee50-934">For WMI classed derived from **CIM\_Printer**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dee50-935">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="dee50-935">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dee50-936">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dee50-936">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee50-937">Требования</span><span class="sxs-lookup"><span data-stu-id="dee50-937">Requirements</span></span>



| <span data-ttu-id="dee50-938">Требование</span><span class="sxs-lookup"><span data-stu-id="dee50-938">Requirement</span></span> | <span data-ttu-id="dee50-939">Значение</span><span class="sxs-lookup"><span data-stu-id="dee50-939">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee50-940">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dee50-940">Minimum supported client</span></span><br/> | <span data-ttu-id="dee50-941">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dee50-941">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dee50-942">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dee50-942">Minimum supported server</span></span><br/> | <span data-ttu-id="dee50-943">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dee50-943">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dee50-944">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dee50-944">Namespace</span></span><br/>                | <span data-ttu-id="dee50-945">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dee50-945">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dee50-946">MOF</span><span class="sxs-lookup"><span data-stu-id="dee50-946">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dee50-947"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dee50-947"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dee50-948">DLL</span><span class="sxs-lookup"><span data-stu-id="dee50-948">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee50-949"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee50-949"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee50-950">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dee50-950">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee50-951">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="dee50-951">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

