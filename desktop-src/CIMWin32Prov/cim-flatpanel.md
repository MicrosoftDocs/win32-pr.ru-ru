---
description: Класс CIM \_ флатпанел представляет возможности и управление логическим устройством плоской панели.
ms.assetid: 0c515621-4ff9-42af-a281-ac49af6d96ba
ms.tgt_platform: multiple
title: Класс CIM_FlatPanel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FlatPanel
- CIM_FlatPanel.Availability
- CIM_FlatPanel.Caption
- CIM_FlatPanel.ConfigManagerErrorCode
- CIM_FlatPanel.ConfigManagerUserConfig
- CIM_FlatPanel.CreationClassName
- CIM_FlatPanel.Description
- CIM_FlatPanel.DeviceID
- CIM_FlatPanel.DisplayType
- CIM_FlatPanel.ErrorCleared
- CIM_FlatPanel.ErrorDescription
- CIM_FlatPanel.HorizontalResolution
- CIM_FlatPanel.InstallDate
- CIM_FlatPanel.IsLocked
- CIM_FlatPanel.LastErrorCode
- CIM_FlatPanel.LightSource
- CIM_FlatPanel.Name
- CIM_FlatPanel.PNPDeviceID
- CIM_FlatPanel.PowerManagementCapabilities
- CIM_FlatPanel.PowerManagementSupported
- CIM_FlatPanel.ScanMode
- CIM_FlatPanel.Status
- CIM_FlatPanel.StatusInfo
- CIM_FlatPanel.SupportsColor
- CIM_FlatPanel.SystemCreationClassName
- CIM_FlatPanel.SystemName
- CIM_FlatPanel.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0c399383223734d2f8ebe68528352c229a74bfbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990592"
---
# <a name="cim_flatpanel-class"></a><span data-ttu-id="25309-103">\_Класс CIM флатпанел</span><span class="sxs-lookup"><span data-stu-id="25309-103">CIM\_FlatPanel class</span></span>

<span data-ttu-id="25309-104">Класс **CIM \_ флатпанел** представляет возможности и управление логическим устройством плоской панели.</span><span class="sxs-lookup"><span data-stu-id="25309-104">The **CIM\_FlatPanel** class represents the capabilities and management of the flat panel logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25309-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="25309-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="25309-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="25309-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="25309-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="25309-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="25309-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="25309-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="25309-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25309-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE9-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_FlatPanel : CIM_Display
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DisplayType;
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   HorizontalResolution;
  datetime InstallDate;
  boolean  IsLocked;
  uint32   LastErrorCode;
  uint16   LightSource;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ScanMode;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsColor;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="25309-110">Члены</span><span class="sxs-lookup"><span data-stu-id="25309-110">Members</span></span>

<span data-ttu-id="25309-111">Класс **CIM \_ флатпанел** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="25309-111">The **CIM\_FlatPanel** class has these types of members:</span></span>

-   [<span data-ttu-id="25309-112">Методы</span><span class="sxs-lookup"><span data-stu-id="25309-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="25309-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="25309-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="25309-114">Методы</span><span class="sxs-lookup"><span data-stu-id="25309-114">Methods</span></span>

<span data-ttu-id="25309-115">Класс **CIM \_ флатпанел** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="25309-115">The **CIM\_FlatPanel** class has these methods.</span></span>



| <span data-ttu-id="25309-116">Метод</span><span class="sxs-lookup"><span data-stu-id="25309-116">Method</span></span>                                                               | <span data-ttu-id="25309-117">Описание</span><span class="sxs-lookup"><span data-stu-id="25309-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="25309-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="25309-118">**Reset**</span></span>](reset-method-in-class-cim-flatpanel.md)                 | <span data-ttu-id="25309-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="25309-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="25309-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="25309-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="25309-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-flatpanel.md) | <span data-ttu-id="25309-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="25309-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="25309-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="25309-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="25309-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="25309-124">Properties</span></span>

<span data-ttu-id="25309-125">Класс **CIM \_ флатпанел** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="25309-125">The **CIM\_FlatPanel** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25309-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="25309-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25309-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25309-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="25309-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="25309-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-130">Availability and status of the device.</span></span>

<span data-ttu-id="25309-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25309-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="25309-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="25309-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="25309-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="25309-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="25309-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="25309-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="25309-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="25309-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="25309-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="25309-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="25309-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="25309-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="25309-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="25309-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="25309-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="25309-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="25309-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="25309-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="25309-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="25309-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="25309-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="25309-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="25309-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="25309-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="25309-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="25309-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="25309-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="25309-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="25309-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="25309-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="25309-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="25309-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="25309-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="25309-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="25309-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="25309-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="25309-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="25309-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="25309-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="25309-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="25309-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="25309-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="25309-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="25309-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="25309-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="25309-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="25309-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="25309-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="25309-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="25309-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="25309-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="25309-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="25309-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="25309-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="25309-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="25309-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="25309-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-164">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="25309-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="25309-165">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="25309-165">Short textual description of the object.</span></span>

<span data-ttu-id="25309-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25309-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-167">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="25309-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25309-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25309-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-170">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="25309-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="25309-171">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="25309-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="25309-172">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="25309-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="25309-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="25309-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="25309-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="25309-175">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="25309-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="25309-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="25309-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="25309-177">(1)</span><span class="sxs-lookup"><span data-stu-id="25309-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="25309-178">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="25309-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="25309-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="25309-180">(2)</span><span class="sxs-lookup"><span data-stu-id="25309-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="25309-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="25309-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="25309-182">(3)</span><span class="sxs-lookup"><span data-stu-id="25309-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="25309-183">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25309-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="25309-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="25309-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="25309-185">(4)</span><span class="sxs-lookup"><span data-stu-id="25309-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="25309-186">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="25309-186">Device is not working properly.</span></span> <span data-ttu-id="25309-187">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="25309-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="25309-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="25309-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="25309-189">(5)</span><span class="sxs-lookup"><span data-stu-id="25309-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="25309-190">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="25309-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="25309-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="25309-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="25309-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="25309-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="25309-193">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="25309-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="25309-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="25309-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="25309-195">(7)</span><span class="sxs-lookup"><span data-stu-id="25309-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="25309-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="25309-197">(8)</span><span class="sxs-lookup"><span data-stu-id="25309-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="25309-198">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="25309-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="25309-200">(9)</span><span class="sxs-lookup"><span data-stu-id="25309-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="25309-201">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="25309-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="25309-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="25309-203">(10)</span><span class="sxs-lookup"><span data-stu-id="25309-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="25309-204">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="25309-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="25309-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="25309-206">(11)</span><span class="sxs-lookup"><span data-stu-id="25309-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="25309-207">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="25309-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="25309-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="25309-209">(12)</span><span class="sxs-lookup"><span data-stu-id="25309-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="25309-210">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="25309-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="25309-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="25309-212">(13)</span><span class="sxs-lookup"><span data-stu-id="25309-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="25309-213">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="25309-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="25309-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="25309-215">(14)</span><span class="sxs-lookup"><span data-stu-id="25309-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="25309-216">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="25309-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="25309-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="25309-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="25309-218">(15)</span><span class="sxs-lookup"><span data-stu-id="25309-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="25309-219">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="25309-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="25309-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="25309-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="25309-221">(16)</span><span class="sxs-lookup"><span data-stu-id="25309-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="25309-222">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="25309-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="25309-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="25309-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="25309-224">(17)</span><span class="sxs-lookup"><span data-stu-id="25309-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="25309-225">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="25309-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="25309-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="25309-227">(18)</span><span class="sxs-lookup"><span data-stu-id="25309-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="25309-228">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="25309-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="25309-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="25309-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="25309-230">(19)</span><span class="sxs-lookup"><span data-stu-id="25309-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="25309-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="25309-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="25309-232">(20)</span><span class="sxs-lookup"><span data-stu-id="25309-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="25309-233">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="25309-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="25309-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="25309-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="25309-235">(21)</span><span class="sxs-lookup"><span data-stu-id="25309-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="25309-236">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="25309-236">System failure.</span></span> <span data-ttu-id="25309-237">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="25309-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="25309-238">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="25309-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="25309-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="25309-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="25309-240">(22)</span><span class="sxs-lookup"><span data-stu-id="25309-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="25309-241">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="25309-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="25309-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="25309-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="25309-243">(23)</span><span class="sxs-lookup"><span data-stu-id="25309-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="25309-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="25309-244">System failure.</span></span> <span data-ttu-id="25309-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="25309-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="25309-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="25309-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="25309-247">(24)</span><span class="sxs-lookup"><span data-stu-id="25309-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="25309-248">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="25309-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="25309-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="25309-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="25309-250">(25)</span><span class="sxs-lookup"><span data-stu-id="25309-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="25309-251">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="25309-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="25309-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="25309-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="25309-253">(26)</span><span class="sxs-lookup"><span data-stu-id="25309-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="25309-254">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="25309-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="25309-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="25309-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="25309-256">(27)</span><span class="sxs-lookup"><span data-stu-id="25309-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="25309-257">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="25309-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="25309-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="25309-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="25309-259">(28)</span><span class="sxs-lookup"><span data-stu-id="25309-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="25309-260">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="25309-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="25309-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="25309-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="25309-262">(29)</span><span class="sxs-lookup"><span data-stu-id="25309-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="25309-263">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="25309-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="25309-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="25309-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="25309-265">(30)</span><span class="sxs-lookup"><span data-stu-id="25309-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="25309-266">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="25309-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="25309-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="25309-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="25309-268">1-31</span><span class="sxs-lookup"><span data-stu-id="25309-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="25309-269">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="25309-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-270">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="25309-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-271">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="25309-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25309-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-273">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="25309-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="25309-274">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="25309-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="25309-275">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="25309-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-279">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="25309-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="25309-280">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="25309-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="25309-281">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="25309-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="25309-282">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-283">**Описание**</span><span class="sxs-lookup"><span data-stu-id="25309-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-286">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="25309-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="25309-287">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="25309-287">Textual description of the object.</span></span>

<span data-ttu-id="25309-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25309-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="25309-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-292">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="25309-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="25309-293">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="25309-294">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-295">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="25309-295">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-296">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25309-296">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25309-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-298">Перечисление, описывающее тип представления плоской панели.</span><span class="sxs-lookup"><span data-stu-id="25309-298">Enumeration that describes the type of flat panel display.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="25309-299"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25309-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="25309-300"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>

<span data-ttu-id="25309-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**Пассивный жидкокристаллический матриц** (2)</span><span class="sxs-lookup"><span data-stu-id="25309-301"><span id="Passive_Matrix_LCD"></span><span id="passive_matrix_lcd"></span><span id="PASSIVE_MATRIX_LCD"></span>**Passive Matrix LCD** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>

<span data-ttu-id="25309-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**Активный жидкокристаллический дисплей матрицы** (3)</span><span class="sxs-lookup"><span data-stu-id="25309-302"><span id="Active_Matrix_LCD"></span><span id="active_matrix_lcd"></span><span id="ACTIVE_MATRIX_LCD"></span>**Active Matrix LCD** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>

<span data-ttu-id="25309-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**ЖК-монитор чолестерик** (4)</span><span class="sxs-lookup"><span data-stu-id="25309-303"><span id="Cholesteric_LCD"></span><span id="cholesteric_lcd"></span><span id="CHOLESTERIC_LCD"></span>**Cholesteric LCD** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>

<span data-ttu-id="25309-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Вывод Расэмиссии полей** (5)</span><span class="sxs-lookup"><span data-stu-id="25309-304"><span id="Field_Emission_Display"></span><span id="field_emission_display"></span><span id="FIELD_EMISSION_DISPLAY"></span>**Field Emission Display** (5)</span></span>


</dt> <dd>

<span data-ttu-id="25309-305">Эмиссия полей</span><span class="sxs-lookup"><span data-stu-id="25309-305">Field emission</span></span>

</dd> <dt>

<span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>

<span data-ttu-id="25309-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Луминесцент дисплей** (6)</span><span class="sxs-lookup"><span data-stu-id="25309-306"><span id="Electro_Luminescent_Display"></span><span id="electro_luminescent_display"></span><span id="ELECTRO_LUMINESCENT_DISPLAY"></span>**Electro Luminescent Display** (6)</span></span>


</dt> <dd>

<span data-ttu-id="25309-307">Луминесцент</span><span class="sxs-lookup"><span data-stu-id="25309-307">Electro luminescent</span></span>

</dd> <dt>

<span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>

<span data-ttu-id="25309-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Плазменный дисплей** (7)</span><span class="sxs-lookup"><span data-stu-id="25309-308"><span id="Gas_Plasma"></span><span id="gas_plasma"></span><span id="GAS_PLASMA"></span>**Gas Plasma** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="LED"></span><span id="led"></span>

<span data-ttu-id="25309-309"><span id="LED"></span><span id="led"></span>**Светоиндикатор** (8)</span><span class="sxs-lookup"><span data-stu-id="25309-309"><span id="LED"></span><span id="led"></span>**LED** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-310">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="25309-310">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-311">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="25309-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25309-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-313">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="25309-313">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="25309-314">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-314">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-315">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="25309-315">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-318">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="25309-318">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="25309-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-320">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="25309-320">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-321">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25309-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25309-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-323">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Пиксели")</span><span class="sxs-lookup"><span data-stu-id="25309-323">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="25309-324">Разрешение по горизонтали в пикселях.</span><span class="sxs-lookup"><span data-stu-id="25309-324">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="25309-325">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="25309-325">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-326">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="25309-326">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="25309-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-328">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="25309-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="25309-329">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="25309-329">Date and time the object was installed.</span></span> <span data-ttu-id="25309-330">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="25309-330">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="25309-331">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25309-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-332">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="25309-332">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-333">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="25309-333">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25309-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-334">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-335">**Значение true** показывает, что устройство заблокировано, что предотвращает ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="25309-335">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="25309-336">Это свойство наследуется от [**CIM \_ усердевице**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="25309-336">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-337">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="25309-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-338">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25309-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25309-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-340">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="25309-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="25309-341">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-342">**лигхтсаурце**</span><span class="sxs-lookup"><span data-stu-id="25309-342">**LightSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-343">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25309-343">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25309-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-345">Описание типа отображаемого освещения.</span><span class="sxs-lookup"><span data-stu-id="25309-345">Description of the display illumination type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-346">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="25309-346">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25309-347">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="25309-347">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Backlit"></span><span id="backlit"></span><span id="BACKLIT"></span>

<span data-ttu-id="25309-348">**Подсветка** (2)</span><span class="sxs-lookup"><span data-stu-id="25309-348">**Backlit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Edgelit"></span><span id="edgelit"></span><span id="EDGELIT"></span>

<span data-ttu-id="25309-349">**Еджелит** (3)</span><span class="sxs-lookup"><span data-stu-id="25309-349">**Edgelit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Reflective"></span><span id="reflective"></span><span id="REFLECTIVE"></span>

<span data-ttu-id="25309-350">**Отражающий** (4)</span><span class="sxs-lookup"><span data-stu-id="25309-350">**Reflective** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-351">**Name**</span><span class="sxs-lookup"><span data-stu-id="25309-351">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-354">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="25309-354">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="25309-355">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="25309-355">Label by which the object is known.</span></span> <span data-ttu-id="25309-356">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="25309-356">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="25309-357">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25309-357">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-358">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="25309-358">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-359">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-359">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-361">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="25309-361">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="25309-362">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-362">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="25309-363">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="25309-364">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="25309-364">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="25309-365">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="25309-365">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-366">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="25309-366">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="25309-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-368">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="25309-368">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="25309-369">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-369">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="25309-370"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="25309-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="25309-371"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="25309-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="25309-372"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="25309-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="25309-373"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="25309-374">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="25309-374">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="25309-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="25309-375"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="25309-376">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="25309-376">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="25309-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="25309-377"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="25309-378">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="25309-378">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="25309-379">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="25309-379">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="25309-380">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="25309-380">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="25309-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="25309-381"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="25309-382">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="25309-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="25309-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="25309-383"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="25309-384">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="25309-384">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-385">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="25309-385">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-386">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="25309-386">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25309-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-388">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="25309-388">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="25309-389">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="25309-389">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="25309-390">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="25309-390">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="25309-391">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="25309-391">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="25309-392">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-393">**сканмоде**</span><span class="sxs-lookup"><span data-stu-id="25309-393">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-394">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25309-394">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25309-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-396">Режим сканирования, который указывает на один или два сканирования, например.</span><span class="sxs-lookup"><span data-stu-id="25309-396">Scan mode that indicates single or dual scan, for example.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-397">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="25309-397">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25309-398">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="25309-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Single_Scan"></span><span id="single_scan"></span><span id="SINGLE_SCAN"></span>

<span data-ttu-id="25309-399">**Одиночное сканирование** (2)</span><span class="sxs-lookup"><span data-stu-id="25309-399">**Single Scan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dual_Scan"></span><span id="dual_scan"></span><span id="DUAL_SCAN"></span>

<span data-ttu-id="25309-400">**Двойное сканирование** (3)</span><span class="sxs-lookup"><span data-stu-id="25309-400">**Dual Scan** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-401">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="25309-401">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-402">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-404">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="25309-404">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="25309-405">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="25309-405">Current status of the object.</span></span> <span data-ttu-id="25309-406">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="25309-406">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="25309-407">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="25309-407">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="25309-408">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="25309-408">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="25309-409">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="25309-409">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="25309-410">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="25309-410">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-411">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="25309-411">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="25309-412">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="25309-412">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="25309-413">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="25309-413">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="25309-414">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="25309-414">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="25309-415">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="25309-415">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="25309-416">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="25309-416">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="25309-417">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="25309-417">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="25309-418">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="25309-418">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="25309-419">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="25309-419">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-420">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="25309-420">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-421">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="25309-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="25309-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-423">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="25309-423">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="25309-424">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="25309-424">State of the logical device.</span></span> <span data-ttu-id="25309-425">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="25309-425">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="25309-426">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="25309-427">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="25309-427">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="25309-428">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="25309-428">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="25309-429">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="25309-429">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="25309-430">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="25309-430">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="25309-431">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="25309-431">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="25309-432">**суппортсколор**</span><span class="sxs-lookup"><span data-stu-id="25309-432">**SupportsColor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-433">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="25309-433">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="25309-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25309-435">Если **значение — true**, плоская панель поддерживает отображение цветов.</span><span class="sxs-lookup"><span data-stu-id="25309-435">If **TRUE**, the flat panel supports color display.</span></span>

</dd> <dt>

<span data-ttu-id="25309-436">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="25309-436">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-437">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-438">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-439">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="25309-439">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="25309-440">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="25309-440">Scoping system's creation class name.</span></span>

<span data-ttu-id="25309-441">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-442">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="25309-442">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="25309-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25309-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-445">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="25309-445">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="25309-446">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="25309-446">Scoping system's name.</span></span>

<span data-ttu-id="25309-447">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="25309-447">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="25309-448">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="25309-448">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25309-449">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25309-449">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="25309-450">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="25309-450">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25309-451">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Пиксели")</span><span class="sxs-lookup"><span data-stu-id="25309-451">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="25309-452">Вертикальное разрешение (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="25309-452">Vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25309-453">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25309-453">Remarks</span></span>

<span data-ttu-id="25309-454">Класс **CIM \_ флатпанел** является производным от [**CIM- \_ дисплеев**](cim-display.md).</span><span class="sxs-lookup"><span data-stu-id="25309-454">The **CIM\_FlatPanel** class is derived from [**CIM\_Display**](cim-display.md).</span></span>

<span data-ttu-id="25309-455">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="25309-455">WMI does not implement this class.</span></span>

<span data-ttu-id="25309-456">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="25309-456">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="25309-457">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="25309-457">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="25309-458">Требования</span><span class="sxs-lookup"><span data-stu-id="25309-458">Requirements</span></span>



| <span data-ttu-id="25309-459">Требование</span><span class="sxs-lookup"><span data-stu-id="25309-459">Requirement</span></span> | <span data-ttu-id="25309-460">Значение</span><span class="sxs-lookup"><span data-stu-id="25309-460">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25309-461">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25309-461">Minimum supported client</span></span><br/> | <span data-ttu-id="25309-462">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25309-462">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25309-463">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25309-463">Minimum supported server</span></span><br/> | <span data-ttu-id="25309-464">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25309-464">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25309-465">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="25309-465">Namespace</span></span><br/>                | <span data-ttu-id="25309-466">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="25309-466">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25309-467">MOF</span><span class="sxs-lookup"><span data-stu-id="25309-467">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25309-468"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25309-468"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25309-469">DLL</span><span class="sxs-lookup"><span data-stu-id="25309-469">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25309-470"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25309-470"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25309-471">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25309-471">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25309-472">**\_Отображение CIM**</span><span class="sxs-lookup"><span data-stu-id="25309-472">**CIM\_Display**</span></span>](cim-display.md)
</dt> </dl>

 

