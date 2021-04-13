---
description: Класс CIM \_ дискретесенсор имеет набор допустимых строковых значений, которые он может сообщить. Значения перечисляются в свойстве Поссиблевалуес датчика. Дискретный датчик всегда имеет текущее считывание, соответствующее одному из перечисляемых значений.
ms.assetid: 58ab5b4d-ff8b-4981-8f09-c9a255635110
ms.tgt_platform: multiple
title: Класс CIM_DiscreteSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiscreteSensor
- CIM_DiscreteSensor.AcceptableValues
- CIM_DiscreteSensor.Availability
- CIM_DiscreteSensor.Caption
- CIM_DiscreteSensor.ConfigManagerErrorCode
- CIM_DiscreteSensor.ConfigManagerUserConfig
- CIM_DiscreteSensor.CreationClassName
- CIM_DiscreteSensor.CurrentReading
- CIM_DiscreteSensor.Description
- CIM_DiscreteSensor.DeviceID
- CIM_DiscreteSensor.ErrorCleared
- CIM_DiscreteSensor.ErrorDescription
- CIM_DiscreteSensor.InstallDate
- CIM_DiscreteSensor.LastErrorCode
- CIM_DiscreteSensor.Name
- CIM_DiscreteSensor.PNPDeviceID
- CIM_DiscreteSensor.PossibleValues
- CIM_DiscreteSensor.PowerManagementCapabilities
- CIM_DiscreteSensor.PowerManagementSupported
- CIM_DiscreteSensor.Status
- CIM_DiscreteSensor.StatusInfo
- CIM_DiscreteSensor.SystemCreationClassName
- CIM_DiscreteSensor.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5211aa8d840384eaf140c1afbeb2fa9c0680cb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539062"
---
# <a name="cim_discretesensor-class"></a><span data-ttu-id="826c7-105">\_Класс CIM дискретесенсор</span><span class="sxs-lookup"><span data-stu-id="826c7-105">CIM\_DiscreteSensor class</span></span>

<span data-ttu-id="826c7-106">Класс **CIM \_ дискретесенсор** имеет набор допустимых строковых значений, которые он может сообщить.</span><span class="sxs-lookup"><span data-stu-id="826c7-106">The **CIM\_DiscreteSensor** class has a set of legal string values that it can report.</span></span> <span data-ttu-id="826c7-107">Значения перечисляются в свойстве **поссиблевалуес** датчика.</span><span class="sxs-lookup"><span data-stu-id="826c7-107">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="826c7-108">Дискретный датчик всегда имеет текущее считывание, соответствующее одному из перечисляемых значений.</span><span class="sxs-lookup"><span data-stu-id="826c7-108">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

<span data-ttu-id="826c7-109">Учитывая Добавление свойств **CurrentState** и **поссиблестатес** к [**\_ датчику CIM**](cim-sensor.md), подкласс дискретного датчика больше не требуется, однако он сохраняется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="826c7-109">Given the addition of the **CurrentState** and **PossibleStates** properties to [**CIM\_Sensor**](cim-sensor.md), the discrete sensor subclass is no longer necessary; however, it is retained for backward compatibility.</span></span> <span data-ttu-id="826c7-110">Сведения в свойствах **куррентреадинг** и **поссиблевалуес** обычно имеют те же значения и семантику, что и свойства **CurrentState** и **поссиблестатес** , унаследованные от **\_ датчика CIM**.</span><span class="sxs-lookup"><span data-stu-id="826c7-110">Information in the **CurrentReading** and **PossibleValues** properties typically has the same values and semantics as for the **CurrentState** and **PossibleStates** properties, which are inherited from **CIM\_Sensor**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="826c7-111">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="826c7-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="826c7-112">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="826c7-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="826c7-113">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="826c7-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="826c7-114">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="826c7-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="826c7-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="826c7-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{1BF00330-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_DiscreteSensor : CIM_Sensor
{
  string   AcceptableValues[];
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   CurrentReading;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  string   PNPDeviceID;
  string   PossibleValues[];
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="826c7-116">Члены</span><span class="sxs-lookup"><span data-stu-id="826c7-116">Members</span></span>

<span data-ttu-id="826c7-117">Класс **CIM \_ дискретесенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="826c7-117">The **CIM\_DiscreteSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="826c7-118">Методы</span><span class="sxs-lookup"><span data-stu-id="826c7-118">Methods</span></span>](#methods)
-   [<span data-ttu-id="826c7-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="826c7-119">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="826c7-120">Методы</span><span class="sxs-lookup"><span data-stu-id="826c7-120">Methods</span></span>

<span data-ttu-id="826c7-121">Класс **CIM \_ дискретесенсор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="826c7-121">The **CIM\_DiscreteSensor** class has these methods.</span></span>



| <span data-ttu-id="826c7-122">Метод</span><span class="sxs-lookup"><span data-stu-id="826c7-122">Method</span></span>                                                                | <span data-ttu-id="826c7-123">Описание</span><span class="sxs-lookup"><span data-stu-id="826c7-123">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="826c7-124">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="826c7-124">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                 | <span data-ttu-id="826c7-125">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-125">Requests a reset of the logical device.</span></span> <span data-ttu-id="826c7-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="826c7-126">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="826c7-127">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="826c7-127">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-controller.md) | <span data-ttu-id="826c7-128">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="826c7-128">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="826c7-129">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="826c7-129">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="826c7-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="826c7-130">Properties</span></span>

<span data-ttu-id="826c7-131">Класс **CIM \_ дискретесенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="826c7-131">The **CIM\_DiscreteSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="826c7-132">**акцептаблевалуес**</span><span class="sxs-lookup"><span data-stu-id="826c7-132">**AcceptableValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-133">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="826c7-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="826c7-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-135">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="826c7-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-136">Строки в свойстве **поссиблевалуес** считаются приемлемыми (то есть они не являются ошибками).</span><span class="sxs-lookup"><span data-stu-id="826c7-136">Strings in the **PossibleValues** property are considered acceptable (that is, they are not errors).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-137">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="826c7-137">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="826c7-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="826c7-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-141">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-141">Availability and status of the device.</span></span>

<span data-ttu-id="826c7-142">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="826c7-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="826c7-143"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="826c7-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="826c7-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="826c7-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="826c7-145"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="826c7-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="826c7-146"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="826c7-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="826c7-147"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="826c7-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="826c7-148"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="826c7-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="826c7-149"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="826c7-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="826c7-150"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="826c7-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="826c7-151"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="826c7-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="826c7-152"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="826c7-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="826c7-153"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="826c7-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="826c7-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="826c7-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="826c7-155"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-156">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="826c7-156">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="826c7-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="826c7-157"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-158">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="826c7-158">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="826c7-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="826c7-159"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-160">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="826c7-160">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="826c7-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="826c7-161"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="826c7-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="826c7-162"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-163">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="826c7-163">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="826c7-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="826c7-164"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-165">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="826c7-165">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="826c7-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="826c7-166"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-167">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="826c7-167">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="826c7-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="826c7-168"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-169">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="826c7-169">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="826c7-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="826c7-170"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-171">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="826c7-171">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="826c7-172">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="826c7-172">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-175">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="826c7-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-176">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="826c7-176">Short textual description of the object.</span></span>

<span data-ttu-id="826c7-177">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="826c7-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-178">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="826c7-178">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-179">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="826c7-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-181">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="826c7-181">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-182">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="826c7-182">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="826c7-183">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-183">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="826c7-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="826c7-184"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="826c7-185"> (0)</span><span class="sxs-lookup"><span data-stu-id="826c7-185">(0)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-186">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="826c7-186">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="826c7-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="826c7-187"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="826c7-188">(1)</span><span class="sxs-lookup"><span data-stu-id="826c7-188">(1)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-189">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="826c7-189">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="826c7-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-190"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="826c7-191">(2)</span><span class="sxs-lookup"><span data-stu-id="826c7-191">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="826c7-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="826c7-192"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="826c7-193">(3)</span><span class="sxs-lookup"><span data-stu-id="826c7-193">(3)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-194">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="826c7-194">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="826c7-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="826c7-195"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="826c7-196">(4)</span><span class="sxs-lookup"><span data-stu-id="826c7-196">(4)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-197">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="826c7-197">Device is not working properly.</span></span> <span data-ttu-id="826c7-198">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="826c7-198">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="826c7-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="826c7-199"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="826c7-200">(5)</span><span class="sxs-lookup"><span data-stu-id="826c7-200">(5)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-201">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="826c7-201">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="826c7-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="826c7-202"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="826c7-203"> (6)</span><span class="sxs-lookup"><span data-stu-id="826c7-203">(6)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-204">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="826c7-204">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="826c7-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="826c7-205"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="826c7-206">(7)</span><span class="sxs-lookup"><span data-stu-id="826c7-206">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="826c7-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-207"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="826c7-208">(8)</span><span class="sxs-lookup"><span data-stu-id="826c7-208">(8)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-209">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-209">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="826c7-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-210"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="826c7-211">(9)</span><span class="sxs-lookup"><span data-stu-id="826c7-211">(9)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-212">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-212">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="826c7-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="826c7-213"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="826c7-214">(10)</span><span class="sxs-lookup"><span data-stu-id="826c7-214">(10)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-215">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="826c7-215">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="826c7-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-216"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="826c7-217">(11)</span><span class="sxs-lookup"><span data-stu-id="826c7-217">(11)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-218">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-218">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="826c7-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="826c7-219"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="826c7-220">(12)</span><span class="sxs-lookup"><span data-stu-id="826c7-220">(12)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-221">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="826c7-221">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="826c7-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-222"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="826c7-223">(13)</span><span class="sxs-lookup"><span data-stu-id="826c7-223">(13)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-224">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-224">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="826c7-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="826c7-225"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="826c7-226">(14)</span><span class="sxs-lookup"><span data-stu-id="826c7-226">(14)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-227">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="826c7-227">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="826c7-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="826c7-228"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="826c7-229">(15)</span><span class="sxs-lookup"><span data-stu-id="826c7-229">(15)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-230">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="826c7-230">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="826c7-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="826c7-231"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="826c7-232">(16)</span><span class="sxs-lookup"><span data-stu-id="826c7-232">(16)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-233">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="826c7-233">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="826c7-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="826c7-234"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="826c7-235">(17)</span><span class="sxs-lookup"><span data-stu-id="826c7-235">(17)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-236">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="826c7-236">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="826c7-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-237"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="826c7-238">(18)</span><span class="sxs-lookup"><span data-stu-id="826c7-238">(18)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-239">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="826c7-239">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="826c7-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="826c7-240"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="826c7-241">(19)</span><span class="sxs-lookup"><span data-stu-id="826c7-241">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="826c7-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="826c7-242"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="826c7-243">(20)</span><span class="sxs-lookup"><span data-stu-id="826c7-243">(20)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-244">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="826c7-244">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="826c7-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="826c7-245"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="826c7-246">(21)</span><span class="sxs-lookup"><span data-stu-id="826c7-246">(21)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-247">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="826c7-247">System failure.</span></span> <span data-ttu-id="826c7-248">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="826c7-248">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="826c7-249">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="826c7-249">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="826c7-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="826c7-250"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="826c7-251">(22)</span><span class="sxs-lookup"><span data-stu-id="826c7-251">(22)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-252">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="826c7-252">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="826c7-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="826c7-253"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="826c7-254">(23)</span><span class="sxs-lookup"><span data-stu-id="826c7-254">(23)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-255">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="826c7-255">System failure.</span></span> <span data-ttu-id="826c7-256">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="826c7-256">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="826c7-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="826c7-257"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="826c7-258">(24)</span><span class="sxs-lookup"><span data-stu-id="826c7-258">(24)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-259">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="826c7-259">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="826c7-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="826c7-260"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="826c7-261">(25)</span><span class="sxs-lookup"><span data-stu-id="826c7-261">(25)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-262">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="826c7-262">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="826c7-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="826c7-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="826c7-264">(26)</span><span class="sxs-lookup"><span data-stu-id="826c7-264">(26)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-265">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="826c7-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="826c7-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="826c7-266"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="826c7-267">(27)</span><span class="sxs-lookup"><span data-stu-id="826c7-267">(27)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-268">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="826c7-268">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="826c7-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="826c7-269"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="826c7-270">(28)</span><span class="sxs-lookup"><span data-stu-id="826c7-270">(28)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-271">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="826c7-271">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="826c7-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="826c7-272"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="826c7-273">(29)</span><span class="sxs-lookup"><span data-stu-id="826c7-273">(29)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-274">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="826c7-274">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="826c7-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="826c7-275"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="826c7-276">(30)</span><span class="sxs-lookup"><span data-stu-id="826c7-276">(30)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-277">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="826c7-277">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="826c7-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="826c7-278"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="826c7-279">1-31</span><span class="sxs-lookup"><span data-stu-id="826c7-279">(31)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-280">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="826c7-280">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="826c7-281">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="826c7-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-282">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="826c7-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-284">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="826c7-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-285">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="826c7-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="826c7-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="826c7-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-290">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="826c7-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-291">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="826c7-291">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="826c7-292">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="826c7-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="826c7-293">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-294">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="826c7-294">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-295">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-297">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="826c7-297">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-298">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="826c7-298">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="826c7-299">**Описание**</span><span class="sxs-lookup"><span data-stu-id="826c7-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-302">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="826c7-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-303">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="826c7-303">Textual description of the object.</span></span>

<span data-ttu-id="826c7-304">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="826c7-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="826c7-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-308">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="826c7-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-309">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="826c7-310">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-311">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="826c7-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="826c7-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="826c7-314">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="826c7-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="826c7-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="826c7-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="826c7-319">Произвольная строка, в которой содержатся дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="826c7-319">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="826c7-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="826c7-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-322">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="826c7-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-324">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="826c7-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="826c7-325">Date and time when the object was installed.</span></span> <span data-ttu-id="826c7-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="826c7-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="826c7-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="826c7-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-328">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="826c7-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-329">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="826c7-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="826c7-331">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="826c7-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="826c7-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-333">**Name**</span><span class="sxs-lookup"><span data-stu-id="826c7-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-336">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="826c7-336">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-337">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="826c7-337">Label by which the object is known.</span></span> <span data-ttu-id="826c7-338">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="826c7-338">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="826c7-339">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="826c7-339">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-340">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="826c7-340">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-341">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-343">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="826c7-343">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-344">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-344">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="826c7-345">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="826c7-346">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="826c7-346">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="826c7-347">**поссиблевалуес**</span><span class="sxs-lookup"><span data-stu-id="826c7-347">**PossibleValues**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-348">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="826c7-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="826c7-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-350">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="826c7-350">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-351">Перечисляет выходные данные из дискретного датчика.</span><span class="sxs-lookup"><span data-stu-id="826c7-351">Enumerates the string outputs from the discrete sensor.</span></span>

</dd> <dt>

<span data-ttu-id="826c7-352">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="826c7-352">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-353">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="826c7-353">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="826c7-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="826c7-355">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="826c7-355">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="826c7-356">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-356">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="826c7-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="826c7-357"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="826c7-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="826c7-358"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="826c7-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="826c7-359"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="826c7-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="826c7-360"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-361">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="826c7-361">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="826c7-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="826c7-362"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-363">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="826c7-363">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="826c7-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="826c7-364"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-365">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="826c7-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="826c7-366">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="826c7-366">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="826c7-367">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="826c7-367">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="826c7-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="826c7-368"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-369">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="826c7-369">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="826c7-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="826c7-370"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="826c7-371">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="826c7-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="826c7-372">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="826c7-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-373">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="826c7-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="826c7-375">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="826c7-375">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="826c7-376">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="826c7-376">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="826c7-377">Это свойство не указывает, что функции управления питанием в настоящее время включены или включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="826c7-377">This property does not indicate that power management features are currently enabled, or if enabled, what features are supported.</span></span> <span data-ttu-id="826c7-378">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="826c7-378">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="826c7-379">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-379">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-380">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="826c7-380">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-383">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="826c7-383">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-384">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="826c7-384">String that indicates the current status of the object.</span></span> <span data-ttu-id="826c7-385">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="826c7-385">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="826c7-386">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="826c7-386">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="826c7-387">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="826c7-387">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="826c7-388">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="826c7-388">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="826c7-389">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="826c7-389">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="826c7-390">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="826c7-390">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="826c7-391">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="826c7-391">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="826c7-392">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="826c7-392">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="826c7-393">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="826c7-393">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="826c7-394">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="826c7-394">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="826c7-395">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="826c7-395">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="826c7-396">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="826c7-396">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="826c7-397">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="826c7-397">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="826c7-398">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="826c7-398">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="826c7-399">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="826c7-399">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="826c7-400">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="826c7-400">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="826c7-401">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="826c7-401">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="826c7-402">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="826c7-402">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="826c7-403">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="826c7-403">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="826c7-404">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="826c7-404">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="826c7-405">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="826c7-405">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-406">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="826c7-406">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-408">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="826c7-408">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="826c7-409">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="826c7-409">State of the logical device.</span></span> <span data-ttu-id="826c7-410">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="826c7-410">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="826c7-411">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="826c7-412">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="826c7-412">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="826c7-413">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="826c7-413">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="826c7-414">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="826c7-414">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="826c7-415">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="826c7-415">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="826c7-416">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="826c7-416">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="826c7-417">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="826c7-417">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-418">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-420">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="826c7-420">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-421">Свойство свойства **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="826c7-421">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="826c7-422">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-422">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="826c7-423">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="826c7-423">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="826c7-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="826c7-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="826c7-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="826c7-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="826c7-426">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="826c7-426">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="826c7-427">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="826c7-427">Scoping system's **Name** property.</span></span>

<span data-ttu-id="826c7-428">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="826c7-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="826c7-429">Комментарии</span><span class="sxs-lookup"><span data-stu-id="826c7-429">Remarks</span></span>

<span data-ttu-id="826c7-430">Класс **CIM \_ дискретесенсор** является производным от [**\_ датчика CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="826c7-430">The **CIM\_DiscreteSensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="826c7-431">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="826c7-431">WMI does not implement this class.</span></span>

<span data-ttu-id="826c7-432">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="826c7-432">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="826c7-433">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="826c7-433">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="826c7-434">Требования</span><span class="sxs-lookup"><span data-stu-id="826c7-434">Requirements</span></span>



| <span data-ttu-id="826c7-435">Требование</span><span class="sxs-lookup"><span data-stu-id="826c7-435">Requirement</span></span> | <span data-ttu-id="826c7-436">Значение</span><span class="sxs-lookup"><span data-stu-id="826c7-436">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="826c7-437">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="826c7-437">Minimum supported client</span></span><br/> | <span data-ttu-id="826c7-438">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="826c7-438">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="826c7-439">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="826c7-439">Minimum supported server</span></span><br/> | <span data-ttu-id="826c7-440">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="826c7-440">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="826c7-441">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="826c7-441">Namespace</span></span><br/>                | <span data-ttu-id="826c7-442">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="826c7-442">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="826c7-443">MOF</span><span class="sxs-lookup"><span data-stu-id="826c7-443">MOF</span></span><br/>                      | <dl> <span data-ttu-id="826c7-444"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="826c7-444"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="826c7-445">DLL</span><span class="sxs-lookup"><span data-stu-id="826c7-445">DLL</span></span><br/>                      | <dl> <span data-ttu-id="826c7-446"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="826c7-446"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="826c7-447">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="826c7-447">See also</span></span>

<dl> <dt>

[<span data-ttu-id="826c7-448">**\_Датчик CIM**</span><span class="sxs-lookup"><span data-stu-id="826c7-448">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

