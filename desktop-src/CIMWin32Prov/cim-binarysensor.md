---
description: Класс CIM \_ бинарисенсор предоставляет логический вывод.
ms.assetid: 51396a51-78ea-4c49-8dcc-7fb815f334ae
ms.tgt_platform: multiple
title: Класс CIM_BinarySensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BinarySensor
- CIM_BinarySensor.Caption
- CIM_BinarySensor.Description
- CIM_BinarySensor.InstallDate
- CIM_BinarySensor.Name
- CIM_BinarySensor.Status
- CIM_BinarySensor.Availability
- CIM_BinarySensor.ConfigManagerErrorCode
- CIM_BinarySensor.ConfigManagerUserConfig
- CIM_BinarySensor.CreationClassName
- CIM_BinarySensor.DeviceID
- CIM_BinarySensor.PowerManagementCapabilities
- CIM_BinarySensor.ErrorCleared
- CIM_BinarySensor.ErrorDescription
- CIM_BinarySensor.LastErrorCode
- CIM_BinarySensor.PNPDeviceID
- CIM_BinarySensor.PowerManagementSupported
- CIM_BinarySensor.StatusInfo
- CIM_BinarySensor.SystemCreationClassName
- CIM_BinarySensor.SystemName
- CIM_BinarySensor.CurrentReading
- CIM_BinarySensor.ExpectedReading
- CIM_BinarySensor.InterpretationOfFalse
- CIM_BinarySensor.InterpretationOfTrue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0d795f98473c09937571d415e34cf6fcb7f3486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655967"
---
# <a name="cim_binarysensor-class"></a><span data-ttu-id="7d5d5-103">\_Класс CIM бинарисенсор</span><span class="sxs-lookup"><span data-stu-id="7d5d5-103">CIM\_BinarySensor class</span></span>

<span data-ttu-id="7d5d5-104">Класс **CIM \_ Бинарисенсор** предоставляет логический вывод.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-104">The **CIM\_BinarySensor** class provides a Boolean output.</span></span> <span data-ttu-id="7d5d5-105">Свойства **CurrentState** и **поссиблестатес** были добавлены для датчиков, поэтому создание подкласса **CIM \_ бинарисенсор** больше не требуется, хотя он сохраняется для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-105">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="7d5d5-106">Двоичный датчик можно создать, создав датчик с двумя возможными состояниями.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-106">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d5d5-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7d5d5-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7d5d5-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7d5d5-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d5d5-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d5d5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{11140D44-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_BinarySensor : CIM_Sensor
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
  boolean  CurrentReading;
  boolean  ExpectedReading;
  string   InterpretationOfFalse;
  string   InterpretationOfTrue;
};
```

## <a name="members"></a><span data-ttu-id="7d5d5-112">Члены</span><span class="sxs-lookup"><span data-stu-id="7d5d5-112">Members</span></span>

<span data-ttu-id="7d5d5-113">Класс **CIM \_ бинарисенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7d5d5-113">The **CIM\_BinarySensor** class has these types of members:</span></span>

-   [<span data-ttu-id="7d5d5-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7d5d5-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="7d5d5-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d5d5-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7d5d5-116">Методы</span><span class="sxs-lookup"><span data-stu-id="7d5d5-116">Methods</span></span>

<span data-ttu-id="7d5d5-117">Класс **CIM \_ бинарисенсор** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-117">The **CIM\_BinarySensor** class has these methods.</span></span>



| <span data-ttu-id="7d5d5-118">Метод</span><span class="sxs-lookup"><span data-stu-id="7d5d5-118">Method</span></span>                                                                  | <span data-ttu-id="7d5d5-119">Описание</span><span class="sxs-lookup"><span data-stu-id="7d5d5-119">Description</span></span>                                                                                                                                |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d5d5-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-120">**Reset**</span></span>](reset-method-in-class-cim-binarysensor.md)                 | <span data-ttu-id="7d5d5-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="7d5d5-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="7d5d5-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-binarysensor.md) | <span data-ttu-id="7d5d5-124">Определяет требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="7d5d5-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7d5d5-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d5d5-126">Properties</span></span>

<span data-ttu-id="7d5d5-127">Класс **CIM \_ бинарисенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-127">The **CIM\_BinarySensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d5d5-128">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-132">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-132">Availability and status of the device.</span></span>

<span data-ttu-id="7d5d5-133">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d5d5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d5d5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="7d5d5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="7d5d5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="7d5d5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7d5d5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="7d5d5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="7d5d5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="7d5d5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7d5d5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="7d5d5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="7d5d5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="7d5d5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-147">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="7d5d5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-149">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="7d5d5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-151">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-151">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="7d5d5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="7d5d5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-154">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="7d5d5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-156">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="7d5d5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-158">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="7d5d5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-160">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="7d5d5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-162">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7d5d5-163">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-166">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-167">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-167">A short textual description of the object.</span></span>

<span data-ttu-id="7d5d5-168">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-169">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-172">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-173">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="7d5d5-174">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="7d5d5-175">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-175">**This device is working properly.**</span></span> <span data-ttu-id="7d5d5-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-176">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="7d5d5-177">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-177">**This device is not configured correctly.**</span></span> <span data-ttu-id="7d5d5-178">(1)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-178">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7d5d5-179">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-179">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="7d5d5-180">(2)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="7d5d5-181">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-181">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="7d5d5-182">(3)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-182">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7d5d5-183">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-183">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="7d5d5-184">(4)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-184">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="7d5d5-185">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-185">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="7d5d5-186">(5)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-186">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="7d5d5-187">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-187">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="7d5d5-188"> (6)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-188">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="7d5d5-189">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-189">**Cannot filter.**</span></span> <span data-ttu-id="7d5d5-190">(7)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-190">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="7d5d5-191">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-191">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="7d5d5-192">(8)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-192">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="7d5d5-193">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-193">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="7d5d5-194">(9)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-194">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="7d5d5-195">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-195">**This device cannot start.**</span></span> <span data-ttu-id="7d5d5-196">(10)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-196">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="7d5d5-197">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-197">**This device failed.**</span></span> <span data-ttu-id="7d5d5-198">(11)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-198">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="7d5d5-199">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-199">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="7d5d5-200">(12)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-200">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="7d5d5-201">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-201">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="7d5d5-202">(13)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-202">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="7d5d5-203">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-203">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="7d5d5-204">(14)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-204">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="7d5d5-205">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-205">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="7d5d5-206">(15)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-206">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="7d5d5-207">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-207">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="7d5d5-208">(16)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-208">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="7d5d5-209">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-209">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="7d5d5-210">(17)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-210">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7d5d5-211">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-211">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="7d5d5-212">(18)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-212">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="7d5d5-213">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-213">**Failure using the VxD loader.**</span></span> <span data-ttu-id="7d5d5-214">(19)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-214">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="7d5d5-215">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-215">**Your registry might be corrupted.**</span></span> <span data-ttu-id="7d5d5-216">(20)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-216">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="7d5d5-217">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-217">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="7d5d5-218">(21)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-218">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="7d5d5-219">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-219">**This device is disabled.**</span></span> <span data-ttu-id="7d5d5-220">(22)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-220">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="7d5d5-221">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-221">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="7d5d5-222">(23)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-222">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="7d5d5-223">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-223">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="7d5d5-224">(24)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-224">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7d5d5-225">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-225">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7d5d5-226">(25)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-226">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="7d5d5-227">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="7d5d5-228">(26)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-228">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="7d5d5-229">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-229">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="7d5d5-230">(27)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-230">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="7d5d5-231">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-231">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="7d5d5-232">(28)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-232">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="7d5d5-233">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-233">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="7d5d5-234">(29)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-234">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="7d5d5-235">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-235">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="7d5d5-236">(30)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-236">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="7d5d5-237">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-237">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="7d5d5-238">1-31</span><span class="sxs-lookup"><span data-stu-id="7d5d5-238">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d5d5-239">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-239">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-240">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-240">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-241">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-242">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-242">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-243">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-243">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="7d5d5-244">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-244">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-245">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-245">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-246">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-247">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-247">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-248">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-248">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-249">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-249">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7d5d5-250">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-250">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="7d5d5-251">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-251">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-252">**куррентреадинг**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-252">**CurrentReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-253">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-253">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-254">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-254">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-255">Текущее значение, указываемое датчиком.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-255">Current value indicated by the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-256">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-256">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-259">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-259">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-260">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-260">A textual description of the object.</span></span>

<span data-ttu-id="7d5d5-261">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-261">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-262">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-262">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-265">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-265">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-266">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-266">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="7d5d5-267">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-267">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-268">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-268">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-269">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-269">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-271">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-271">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="7d5d5-272">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-273">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-273">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-276">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-276">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="7d5d5-277">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-278">**експектедреадинг**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-278">**ExpectedReading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-279">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-281">Значение "нормального" для датчика.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-281">'Normal' value for the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-282">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-282">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-283">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-283">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-285">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-286">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-286">Indicates when the object was installed.</span></span> <span data-ttu-id="7d5d5-287">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-287">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7d5d5-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-289">**интерпретатионоффалсе**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-289">**InterpretationOfFalse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-292">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-292">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-293">Описание значения "false" из двоичного датчика.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-293">Description of a 'False' value from the binary sensor.</span></span> <span data-ttu-id="7d5d5-294">Эти сведения могут отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-294">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-295">**интерпретатионофтруе**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-295">**InterpretationOfTrue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-298">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-298">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-299">Описание значения "true" из двоичного датчика.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-299">Description of a 'True' value from the binary sensor.</span></span> <span data-ttu-id="7d5d5-300">Эти сведения могут отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-300">This information can be displayed to a user.</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-301">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-301">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-302">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-302">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-304">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-304">Last error code reported by the logical device.</span></span>

<span data-ttu-id="7d5d5-305">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-306">**Name**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-306">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-309">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-309">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-310">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-310">Label by which the object is known.</span></span> <span data-ttu-id="7d5d5-311">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-311">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7d5d5-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-313">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-313">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-316">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-316">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-317">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-317">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="7d5d5-318">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="7d5d5-318">Example: "\*PNP030b"</span></span>

<span data-ttu-id="7d5d5-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-320">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-320">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-321">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="7d5d5-321">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-323">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-323">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="7d5d5-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d5d5-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-325"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-326">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-326">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="7d5d5-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-327"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-328">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-328">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7d5d5-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-329"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-330">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-330">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7d5d5-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-331"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-332">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-332">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="7d5d5-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-333"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-334">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-334">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="7d5d5-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-335"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-336">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="7d5d5-336">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="7d5d5-337">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-337">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="7d5d5-338">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-338">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="7d5d5-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-339"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-340">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="7d5d5-340">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="7d5d5-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-341"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="7d5d5-342">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-342">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7d5d5-343">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-343">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-344">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-344">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-346">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-346">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="7d5d5-347">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="7d5d5-347">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7d5d5-348">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-348">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="7d5d5-349">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="7d5d5-349">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="7d5d5-350">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-351">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-354">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-355">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-355">String that indicates the current status of the object.</span></span> <span data-ttu-id="7d5d5-356">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-356">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7d5d5-357">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="7d5d5-357">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7d5d5-358">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-358">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7d5d5-359">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="7d5d5-359">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7d5d5-360">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-360">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7d5d5-361">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-361">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7d5d5-362">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-362">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7d5d5-363">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="7d5d5-363">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7d5d5-364">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-364">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7d5d5-365">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-365">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7d5d5-366">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-366">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d5d5-367">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-367">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7d5d5-368">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-368">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7d5d5-369">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-369">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7d5d5-370">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-370">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7d5d5-371">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-371">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7d5d5-372">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-372">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7d5d5-373">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-373">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7d5d5-374">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-374">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7d5d5-375">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-375">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d5d5-376">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-376">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-377">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-377">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-379">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="7d5d5-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-380">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-380">State of the logical device.</span></span> <span data-ttu-id="7d5d5-381">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="7d5d5-381">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="7d5d5-382">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7d5d5-383">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-383">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7d5d5-384">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-384">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7d5d5-385">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-385">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7d5d5-386">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-386">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="7d5d5-387">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-387">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d5d5-388">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-388">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-389">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-389">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-391">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-391">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-392">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-392">The scoping system's creation class name.</span></span>

<span data-ttu-id="7d5d5-393">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-393">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d5d5-394">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-394">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d5d5-395">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-395">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-396">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d5d5-396">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d5d5-397">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7d5d5-397">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7d5d5-398">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-398">The scoping system's name.</span></span>

<span data-ttu-id="7d5d5-399">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-399">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d5d5-400">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d5d5-400">Remarks</span></span>

<span data-ttu-id="7d5d5-401">Класс **CIM \_ бинарисенсор** является производным от [**\_ датчика CIM**](cim-sensor.md).</span><span class="sxs-lookup"><span data-stu-id="7d5d5-401">The **CIM\_BinarySensor** class is derived from [**CIM\_Sensor**](cim-sensor.md).</span></span>

<span data-ttu-id="7d5d5-402">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-402">WMI does not implement this class.</span></span>

<span data-ttu-id="7d5d5-403">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-403">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7d5d5-404">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7d5d5-404">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d5d5-405">Требования</span><span class="sxs-lookup"><span data-stu-id="7d5d5-405">Requirements</span></span>



| <span data-ttu-id="7d5d5-406">Требование</span><span class="sxs-lookup"><span data-stu-id="7d5d5-406">Requirement</span></span> | <span data-ttu-id="7d5d5-407">Значение</span><span class="sxs-lookup"><span data-stu-id="7d5d5-407">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5d5-408">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d5d5-408">Minimum supported client</span></span><br/> | <span data-ttu-id="7d5d5-409">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d5d5-409">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d5d5-410">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d5d5-410">Minimum supported server</span></span><br/> | <span data-ttu-id="7d5d5-411">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d5d5-411">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d5d5-412">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d5d5-412">Namespace</span></span><br/>                | <span data-ttu-id="7d5d5-413">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7d5d5-413">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d5d5-414">MOF</span><span class="sxs-lookup"><span data-stu-id="7d5d5-414">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d5d5-415"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d5-415"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d5d5-416">DLL</span><span class="sxs-lookup"><span data-stu-id="7d5d5-416">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d5d5-417"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d5d5-417"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d5d5-418">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d5d5-418">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5d5-419">**\_Датчик CIM**</span><span class="sxs-lookup"><span data-stu-id="7d5d5-419">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> </dl>

 

