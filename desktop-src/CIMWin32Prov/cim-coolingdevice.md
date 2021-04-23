---
description: Класс CIM \_ кулингдевице представляет возможности и управление охлаждающими устройствами.
ms.assetid: ac0f0df4-c174-4306-9325-eaa316ee820a
ms.tgt_platform: multiple
title: Класс CIM_CoolingDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CoolingDevice
- CIM_CoolingDevice.Caption
- CIM_CoolingDevice.Description
- CIM_CoolingDevice.InstallDate
- CIM_CoolingDevice.Name
- CIM_CoolingDevice.Status
- CIM_CoolingDevice.Availability
- CIM_CoolingDevice.ConfigManagerErrorCode
- CIM_CoolingDevice.ConfigManagerUserConfig
- CIM_CoolingDevice.CreationClassName
- CIM_CoolingDevice.DeviceID
- CIM_CoolingDevice.PowerManagementCapabilities
- CIM_CoolingDevice.ErrorCleared
- CIM_CoolingDevice.ErrorDescription
- CIM_CoolingDevice.LastErrorCode
- CIM_CoolingDevice.PNPDeviceID
- CIM_CoolingDevice.PowerManagementSupported
- CIM_CoolingDevice.StatusInfo
- CIM_CoolingDevice.SystemCreationClassName
- CIM_CoolingDevice.SystemName
- CIM_CoolingDevice.ActiveCooling
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f6c480e910cf72a319856942fda28d2139d0a6ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655841"
---
# <a name="cim_coolingdevice-class"></a><span data-ttu-id="c951a-103">\_Класс CIM кулингдевице</span><span class="sxs-lookup"><span data-stu-id="c951a-103">CIM\_CoolingDevice class</span></span>

<span data-ttu-id="c951a-104">Класс **CIM \_ кулингдевице** представляет возможности и управление охлаждающими устройствами.</span><span class="sxs-lookup"><span data-stu-id="c951a-104">The **CIM\_CoolingDevice** class represents the capabilities and management of cooling devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c951a-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c951a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c951a-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c951a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c951a-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c951a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c951a-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c951a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c951a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c951a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979A-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_CoolingDevice : CIM_LogicalDevice
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
  boolean  ActiveCooling;
};
```

## <a name="members"></a><span data-ttu-id="c951a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c951a-110">Members</span></span>

<span data-ttu-id="c951a-111">Класс **CIM \_ кулингдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c951a-111">The **CIM\_CoolingDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="c951a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c951a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c951a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c951a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c951a-114">Методы</span><span class="sxs-lookup"><span data-stu-id="c951a-114">Methods</span></span>

<span data-ttu-id="c951a-115">Класс **CIM \_ кулингдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c951a-115">The **CIM\_CoolingDevice** class has these methods.</span></span>



| <span data-ttu-id="c951a-116">Метод</span><span class="sxs-lookup"><span data-stu-id="c951a-116">Method</span></span>                                                                   | <span data-ttu-id="c951a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c951a-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c951a-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="c951a-118">**Reset**</span></span>](reset-method-in-class-cim-controller.md)                    | <span data-ttu-id="c951a-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c951a-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="c951a-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c951a-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="c951a-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="c951a-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-coolingdevice.md) | <span data-ttu-id="c951a-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="c951a-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="c951a-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="c951a-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c951a-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="c951a-124">Properties</span></span>

<span data-ttu-id="c951a-125">Класс **CIM \_ кулингдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c951a-125">The **CIM\_CoolingDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c951a-126">**активекулинг**</span><span class="sxs-lookup"><span data-stu-id="c951a-126">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-127">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c951a-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c951a-129">Если **значение равно true**, устройство охлаждения обеспечивает охлаждение (в отличие от пассивного).</span><span class="sxs-lookup"><span data-stu-id="c951a-129">If **TRUE**, the cooling device provides active (as opposed to passive) cooling.</span></span>

</dd> <dt>

<span data-ttu-id="c951a-130">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="c951a-130">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c951a-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-133">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="c951a-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-134">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="c951a-134">Availability and status of the device.</span></span>

<span data-ttu-id="c951a-135">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-135">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c951a-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c951a-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c951a-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c951a-137"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="c951a-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="c951a-138"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="c951a-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="c951a-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="c951a-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="c951a-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c951a-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="c951a-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="c951a-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="c951a-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="c951a-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="c951a-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="c951a-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="c951a-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c951a-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="c951a-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="c951a-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="c951a-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="c951a-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="c951a-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="c951a-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="c951a-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-149">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="c951a-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="c951a-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="c951a-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-151">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="c951a-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="c951a-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="c951a-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-153">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="c951a-153">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="c951a-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="c951a-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="c951a-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="c951a-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-156">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="c951a-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="c951a-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="c951a-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-158">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="c951a-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="c951a-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="c951a-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-160">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="c951a-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="c951a-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="c951a-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-162">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="c951a-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="c951a-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="c951a-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-164">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="c951a-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c951a-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c951a-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-168">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="c951a-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-169">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c951a-169">A short textual description of the object.</span></span>

<span data-ttu-id="c951a-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c951a-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-171">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c951a-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c951a-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-174">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c951a-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-175">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c951a-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="c951a-176">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="c951a-177">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="c951a-177">**This device is working properly.**</span></span> <span data-ttu-id="c951a-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="c951a-178">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="c951a-179">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="c951a-179">**This device is not configured correctly.**</span></span> <span data-ttu-id="c951a-180">(1)</span><span class="sxs-lookup"><span data-stu-id="c951a-180">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c951a-181">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-181">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="c951a-182">(2)</span><span class="sxs-lookup"><span data-stu-id="c951a-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="c951a-183">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="c951a-183">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="c951a-184">(3)</span><span class="sxs-lookup"><span data-stu-id="c951a-184">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c951a-185">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="c951a-185">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="c951a-186">(4)</span><span class="sxs-lookup"><span data-stu-id="c951a-186">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="c951a-187">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="c951a-187">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="c951a-188">(5)</span><span class="sxs-lookup"><span data-stu-id="c951a-188">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="c951a-189">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="c951a-189">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="c951a-190"> (6)</span><span class="sxs-lookup"><span data-stu-id="c951a-190">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="c951a-191">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="c951a-191">**Cannot filter.**</span></span> <span data-ttu-id="c951a-192">(7)</span><span class="sxs-lookup"><span data-stu-id="c951a-192">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="c951a-193">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-193">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="c951a-194">(8)</span><span class="sxs-lookup"><span data-stu-id="c951a-194">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="c951a-195">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-195">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="c951a-196">(9)</span><span class="sxs-lookup"><span data-stu-id="c951a-196">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="c951a-197">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="c951a-197">**This device cannot start.**</span></span> <span data-ttu-id="c951a-198">(10)</span><span class="sxs-lookup"><span data-stu-id="c951a-198">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="c951a-199">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-199">**This device failed.**</span></span> <span data-ttu-id="c951a-200">(11)</span><span class="sxs-lookup"><span data-stu-id="c951a-200">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="c951a-201">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="c951a-201">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="c951a-202">(12)</span><span class="sxs-lookup"><span data-stu-id="c951a-202">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="c951a-203">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-203">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="c951a-204">(13)</span><span class="sxs-lookup"><span data-stu-id="c951a-204">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="c951a-205">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="c951a-205">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="c951a-206">(14)</span><span class="sxs-lookup"><span data-stu-id="c951a-206">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="c951a-207">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="c951a-207">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="c951a-208">(15)</span><span class="sxs-lookup"><span data-stu-id="c951a-208">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="c951a-209">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="c951a-209">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="c951a-210">(16)</span><span class="sxs-lookup"><span data-stu-id="c951a-210">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="c951a-211">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="c951a-211">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="c951a-212">(17)</span><span class="sxs-lookup"><span data-stu-id="c951a-212">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c951a-213">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-213">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="c951a-214">(18)</span><span class="sxs-lookup"><span data-stu-id="c951a-214">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="c951a-215">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="c951a-215">**Failure using the VxD loader.**</span></span> <span data-ttu-id="c951a-216">(19)</span><span class="sxs-lookup"><span data-stu-id="c951a-216">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="c951a-217">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="c951a-217">**Your registry might be corrupted.**</span></span> <span data-ttu-id="c951a-218">(20)</span><span class="sxs-lookup"><span data-stu-id="c951a-218">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="c951a-219">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="c951a-219">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="c951a-220">(21)</span><span class="sxs-lookup"><span data-stu-id="c951a-220">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="c951a-221">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="c951a-221">**This device is disabled.**</span></span> <span data-ttu-id="c951a-222">(22)</span><span class="sxs-lookup"><span data-stu-id="c951a-222">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="c951a-223">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="c951a-223">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="c951a-224">(23)</span><span class="sxs-lookup"><span data-stu-id="c951a-224">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="c951a-225">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="c951a-225">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="c951a-226">(24)</span><span class="sxs-lookup"><span data-stu-id="c951a-226">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c951a-227">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="c951a-227">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c951a-228">(25)</span><span class="sxs-lookup"><span data-stu-id="c951a-228">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="c951a-229">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="c951a-229">**Windows is still setting up this device.**</span></span> <span data-ttu-id="c951a-230">(26)</span><span class="sxs-lookup"><span data-stu-id="c951a-230">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="c951a-231">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="c951a-231">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="c951a-232">(27)</span><span class="sxs-lookup"><span data-stu-id="c951a-232">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="c951a-233">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="c951a-233">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="c951a-234">(28)</span><span class="sxs-lookup"><span data-stu-id="c951a-234">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="c951a-235">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="c951a-235">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="c951a-236">(29)</span><span class="sxs-lookup"><span data-stu-id="c951a-236">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="c951a-237">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="c951a-237">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="c951a-238">(30)</span><span class="sxs-lookup"><span data-stu-id="c951a-238">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="c951a-239">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="c951a-239">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="c951a-240">1-31</span><span class="sxs-lookup"><span data-stu-id="c951a-240">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c951a-241">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="c951a-241">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-242">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c951a-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-244">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c951a-244">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-245">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c951a-245">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="c951a-246">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-246">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-247">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c951a-247">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-250">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c951a-250">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c951a-251">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c951a-251">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c951a-252">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="c951a-252">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="c951a-253">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-253">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-254">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c951a-254">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-257">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="c951a-257">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-258">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c951a-258">A textual description of the object.</span></span>

<span data-ttu-id="c951a-259">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c951a-259">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-260">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="c951a-260">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-263">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c951a-263">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c951a-264">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c951a-264">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="c951a-265">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-266">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="c951a-266">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-267">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c951a-267">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c951a-269">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="c951a-269">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="c951a-270">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-271">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="c951a-271">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c951a-274">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="c951a-274">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="c951a-275">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c951a-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-277">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c951a-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-279">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="c951a-279">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-280">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="c951a-280">Indicates when the object was installed.</span></span> <span data-ttu-id="c951a-281">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="c951a-281">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c951a-282">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c951a-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-283">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="c951a-283">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-284">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c951a-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c951a-286">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="c951a-286">Last error code reported by the logical device.</span></span>

<span data-ttu-id="c951a-287">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-288">**Name**</span><span class="sxs-lookup"><span data-stu-id="c951a-288">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-291">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="c951a-291">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-292">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="c951a-292">Label by which the object is known.</span></span> <span data-ttu-id="c951a-293">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="c951a-293">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="c951a-294">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c951a-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-295">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="c951a-295">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-298">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="c951a-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-299">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c951a-299">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="c951a-300">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="c951a-300">Example: "\*PNP030b"</span></span>

<span data-ttu-id="c951a-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-302">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="c951a-302">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-303">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c951a-303">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c951a-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c951a-305">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="c951a-305">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="c951a-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c951a-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c951a-307"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-308">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="c951a-308">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="c951a-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="c951a-309"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-310">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="c951a-310">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c951a-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="c951a-311"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-312">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="c951a-312">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c951a-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="c951a-313"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-314">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="c951a-314">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="c951a-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="c951a-315"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-316">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="c951a-316">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="c951a-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="c951a-317"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-318">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="c951a-318">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="c951a-319">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="c951a-319">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="c951a-320">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="c951a-320">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="c951a-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="c951a-321"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-322">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="c951a-322">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="c951a-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="c951a-323"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="c951a-324">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="c951a-324">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="c951a-325">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="c951a-325">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-326">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c951a-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c951a-328">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="c951a-328">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="c951a-329">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="c951a-329">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c951a-330">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c951a-330">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="c951a-331">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="c951a-331">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="c951a-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-333">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="c951a-333">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-336">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="c951a-336">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-337">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="c951a-337">String that indicates the current status of the object.</span></span> <span data-ttu-id="c951a-338">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="c951a-338">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="c951a-339">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="c951a-339">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="c951a-340">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="c951a-340">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="c951a-341">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="c951a-341">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c951a-342">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="c951a-342">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c951a-343">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="c951a-343">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c951a-344">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c951a-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="c951a-345">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="c951a-345">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="c951a-346">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="c951a-346">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="c951a-347">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="c951a-347">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="c951a-348">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="c951a-348">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c951a-349">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="c951a-349">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="c951a-350">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="c951a-350">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="c951a-351">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="c951a-351">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="c951a-352">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="c951a-352">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c951a-353">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="c951a-353">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="c951a-354">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="c951a-354">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="c951a-355">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="c951a-355">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="c951a-356">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="c951a-356">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="c951a-357">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="c951a-357">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c951a-358">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="c951a-358">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-359">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c951a-359">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-360">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-361">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="c951a-361">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="c951a-362">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="c951a-362">State of the logical device.</span></span> <span data-ttu-id="c951a-363">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="c951a-363">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="c951a-364">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c951a-365">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c951a-365">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c951a-366">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="c951a-366">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="c951a-367">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="c951a-367">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="c951a-368">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="c951a-368">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="c951a-369">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="c951a-369">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c951a-370">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="c951a-370">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-371">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-373">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c951a-373">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c951a-374">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="c951a-374">The scoping system's creation class name.</span></span>

<span data-ttu-id="c951a-375">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="c951a-376">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c951a-376">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c951a-377">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c951a-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c951a-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c951a-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c951a-379">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c951a-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c951a-380">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="c951a-380">The scoping system's name.</span></span>

<span data-ttu-id="c951a-381">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="c951a-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c951a-382">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c951a-382">Remarks</span></span>

<span data-ttu-id="c951a-383">Класс **CIM \_ кулингдевице** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="c951a-383">The **CIM\_CoolingDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="c951a-384">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c951a-384">WMI does not implement this class.</span></span> <span data-ttu-id="c951a-385">Классы, производные от **CIM \_ кулингдевице**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c951a-385">For classes derived from **CIM\_CoolingDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="c951a-386">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c951a-386">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c951a-387">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c951a-387">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c951a-388">Требования</span><span class="sxs-lookup"><span data-stu-id="c951a-388">Requirements</span></span>



| <span data-ttu-id="c951a-389">Требование</span><span class="sxs-lookup"><span data-stu-id="c951a-389">Requirement</span></span> | <span data-ttu-id="c951a-390">Значение</span><span class="sxs-lookup"><span data-stu-id="c951a-390">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c951a-391">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c951a-391">Minimum supported client</span></span><br/> | <span data-ttu-id="c951a-392">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c951a-392">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c951a-393">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c951a-393">Minimum supported server</span></span><br/> | <span data-ttu-id="c951a-394">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c951a-394">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c951a-395">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c951a-395">Namespace</span></span><br/>                | <span data-ttu-id="c951a-396">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c951a-396">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c951a-397">MOF</span><span class="sxs-lookup"><span data-stu-id="c951a-397">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c951a-398"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c951a-398"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c951a-399">DLL</span><span class="sxs-lookup"><span data-stu-id="c951a-399">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c951a-400"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c951a-400"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c951a-401">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c951a-401">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c951a-402">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="c951a-402">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

