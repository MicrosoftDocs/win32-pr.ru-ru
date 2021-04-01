---
description: '\_Класс WMI хеатпипе для Win32 представляет свойства устройства охлаждения теплоотвода.'
ms.assetid: c6e24cb2-e29a-4cd5-af62-b8e48a5936f9
ms.tgt_platform: multiple
title: Класс Win32_HeatPipe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_HeatPipe
- Win32_HeatPipe.Reset
- Win32_HeatPipe.SetPowerState
- Win32_HeatPipe.ActiveCooling
- Win32_HeatPipe.Availability
- Win32_HeatPipe.Caption
- Win32_HeatPipe.ConfigManagerErrorCode
- Win32_HeatPipe.ConfigManagerUserConfig
- Win32_HeatPipe.CreationClassName
- Win32_HeatPipe.Description
- Win32_HeatPipe.DeviceID
- Win32_HeatPipe.ErrorCleared
- Win32_HeatPipe.ErrorDescription
- Win32_HeatPipe.InstallDate
- Win32_HeatPipe.LastErrorCode
- Win32_HeatPipe.Name
- Win32_HeatPipe.PNPDeviceID
- Win32_HeatPipe.PowerManagementCapabilities
- Win32_HeatPipe.PowerManagementSupported
- Win32_HeatPipe.Status
- Win32_HeatPipe.StatusInfo
- Win32_HeatPipe.SystemCreationClassName
- Win32_HeatPipe.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f89b8f059a5c80f4d40c70007d8870211e79f93f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072504"
---
# <a name="win32_heatpipe-class"></a><span data-ttu-id="2483c-103">\_Класс Win32 хеатпипе</span><span class="sxs-lookup"><span data-stu-id="2483c-103">Win32\_HeatPipe class</span></span>

<span data-ttu-id="2483c-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ хеатпипе для Win32** представляет свойства устройства охлаждения теплоотвода.</span><span class="sxs-lookup"><span data-stu-id="2483c-104">The **Win32\_HeatPipe** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the properties of a heat pipe cooling device.</span></span>

<span data-ttu-id="2483c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2483c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2483c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2483c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB7-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_HeatPipe : CIM_HeatPipe
{
  boolean  ActiveCooling;
  uint16   Availability;
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
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="2483c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="2483c-107">Members</span></span>

<span data-ttu-id="2483c-108">Класс **Win32 \_ хеатпипе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2483c-108">The **Win32\_HeatPipe** class has these types of members:</span></span>

-   [<span data-ttu-id="2483c-109">Методы</span><span class="sxs-lookup"><span data-stu-id="2483c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2483c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2483c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2483c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2483c-111">Methods</span></span>

<span data-ttu-id="2483c-112">Класс **Win32 \_ хеатпипе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2483c-112">The **Win32\_HeatPipe** class has these methods.</span></span>



| <span data-ttu-id="2483c-113">Метод</span><span class="sxs-lookup"><span data-stu-id="2483c-113">Method</span></span>            | <span data-ttu-id="2483c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2483c-114">Description</span></span>                                                                                                                                                                                            |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2483c-115">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="2483c-115">**Reset**</span></span>         | <span data-ttu-id="2483c-116">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2483c-116">Not implemented.</span></span> <span data-ttu-id="2483c-117">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ хеатпипе**](cim-heatpipe.md) .</span><span class="sxs-lookup"><span data-stu-id="2483c-117">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="2483c-118">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2483c-118">**SetPowerState**</span></span> | <span data-ttu-id="2483c-119">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="2483c-119">Not implemented.</span></span> <span data-ttu-id="2483c-120">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ хеатпипе**](cim-heatpipe.md) .</span><span class="sxs-lookup"><span data-stu-id="2483c-120">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_HeatPipe**](cim-heatpipe.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2483c-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="2483c-121">Properties</span></span>

<span data-ttu-id="2483c-122">Класс **Win32 \_ хеатпипе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2483c-122">The **Win32\_HeatPipe** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2483c-123">**активекулинг**</span><span class="sxs-lookup"><span data-stu-id="2483c-123">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-124">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2483c-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2483c-126">Если **значение равно true**, устройство охлаждения предоставляет активное охлаждение, не пассивное.</span><span class="sxs-lookup"><span data-stu-id="2483c-126">If **TRUE**, the cooling device provides active cooling not passive.</span></span>

<span data-ttu-id="2483c-127">Это свойство наследуется от [**CIM \_ кулингдевице**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-127">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-128">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="2483c-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2483c-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="2483c-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-132">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-132">Availability and status of the device.</span></span>

<span data-ttu-id="2483c-133">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2483c-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2483c-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2483c-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="2483c-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2483c-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="2483c-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-137">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="2483c-137">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2483c-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="2483c-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2483c-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="2483c-139"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2483c-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="2483c-140"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2483c-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="2483c-141"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2483c-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="2483c-142"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2483c-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="2483c-143"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2483c-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="2483c-144"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2483c-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="2483c-145"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2483c-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="2483c-146"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2483c-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="2483c-147"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-148">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="2483c-148">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2483c-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="2483c-149"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-150">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="2483c-150">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2483c-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="2483c-151"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-152">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="2483c-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2483c-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="2483c-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2483c-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="2483c-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-155">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="2483c-155">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2483c-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="2483c-156"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-157">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="2483c-157">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2483c-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="2483c-158"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-159">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="2483c-159">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2483c-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="2483c-160"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-161">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="2483c-161">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2483c-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="2483c-162"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-163">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="2483c-163">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2483c-164">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2483c-164">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-165">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-167">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2483c-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-168">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="2483c-168">Short description of the object a one-line string.</span></span>

<span data-ttu-id="2483c-169">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-169">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-170">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="2483c-170">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2483c-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-173">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2483c-173">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-174">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2483c-174">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="2483c-175">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-175">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2483c-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="2483c-176"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2483c-177"> (0)</span><span class="sxs-lookup"><span data-stu-id="2483c-177">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-178">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="2483c-178">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2483c-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="2483c-179"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2483c-180">(1)</span><span class="sxs-lookup"><span data-stu-id="2483c-180">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-181">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="2483c-181">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2483c-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-182"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2483c-183">(2)</span><span class="sxs-lookup"><span data-stu-id="2483c-183">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2483c-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="2483c-184"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2483c-185">(3)</span><span class="sxs-lookup"><span data-stu-id="2483c-185">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-186">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2483c-186">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2483c-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="2483c-187"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2483c-188">(4)</span><span class="sxs-lookup"><span data-stu-id="2483c-188">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-189">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="2483c-189">Device is not working properly.</span></span> <span data-ttu-id="2483c-190">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="2483c-190">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2483c-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="2483c-191"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2483c-192">(5)</span><span class="sxs-lookup"><span data-stu-id="2483c-192">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-193">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="2483c-193">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2483c-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="2483c-194"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2483c-195"> (6)</span><span class="sxs-lookup"><span data-stu-id="2483c-195">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-196">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="2483c-196">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2483c-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="2483c-197"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2483c-198">(7)</span><span class="sxs-lookup"><span data-stu-id="2483c-198">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2483c-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-199"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2483c-200">(8)</span><span class="sxs-lookup"><span data-stu-id="2483c-200">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-201">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-201">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2483c-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-202"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2483c-203">(9)</span><span class="sxs-lookup"><span data-stu-id="2483c-203">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-204">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="2483c-204">Device is not working properly.</span></span> <span data-ttu-id="2483c-205">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-205">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2483c-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="2483c-206"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2483c-207">(10)</span><span class="sxs-lookup"><span data-stu-id="2483c-207">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-208">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="2483c-208">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2483c-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-209"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2483c-210">(11)</span><span class="sxs-lookup"><span data-stu-id="2483c-210">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-211">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-211">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2483c-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="2483c-212"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2483c-213">(12)</span><span class="sxs-lookup"><span data-stu-id="2483c-213">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-214">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="2483c-214">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2483c-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-215"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2483c-216">(13)</span><span class="sxs-lookup"><span data-stu-id="2483c-216">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-217">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-217">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2483c-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="2483c-218"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2483c-219">(14)</span><span class="sxs-lookup"><span data-stu-id="2483c-219">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-220">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="2483c-220">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2483c-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="2483c-221"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2483c-222">(15)</span><span class="sxs-lookup"><span data-stu-id="2483c-222">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-223">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="2483c-223">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2483c-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="2483c-224"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2483c-225">(16)</span><span class="sxs-lookup"><span data-stu-id="2483c-225">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-226">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="2483c-226">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2483c-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="2483c-227"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2483c-228">(17)</span><span class="sxs-lookup"><span data-stu-id="2483c-228">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-229">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="2483c-229">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2483c-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-230"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2483c-231">(18)</span><span class="sxs-lookup"><span data-stu-id="2483c-231">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-232">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="2483c-232">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2483c-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="2483c-233"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2483c-234">(19)</span><span class="sxs-lookup"><span data-stu-id="2483c-234">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2483c-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="2483c-235"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2483c-236">(20)</span><span class="sxs-lookup"><span data-stu-id="2483c-236">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-237">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="2483c-237">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2483c-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="2483c-238"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2483c-239">(21)</span><span class="sxs-lookup"><span data-stu-id="2483c-239">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-240">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="2483c-240">System failure.</span></span> <span data-ttu-id="2483c-241">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="2483c-241">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2483c-242">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="2483c-242">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2483c-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="2483c-243"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2483c-244">(22)</span><span class="sxs-lookup"><span data-stu-id="2483c-244">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-245">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="2483c-245">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2483c-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="2483c-246"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2483c-247">(23)</span><span class="sxs-lookup"><span data-stu-id="2483c-247">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-248">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="2483c-248">System failure.</span></span> <span data-ttu-id="2483c-249">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="2483c-249">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2483c-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="2483c-250"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2483c-251">(24)</span><span class="sxs-lookup"><span data-stu-id="2483c-251">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-252">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="2483c-252">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2483c-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="2483c-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2483c-254">(25)</span><span class="sxs-lookup"><span data-stu-id="2483c-254">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-255">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="2483c-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2483c-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="2483c-256"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2483c-257">(26)</span><span class="sxs-lookup"><span data-stu-id="2483c-257">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-258">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="2483c-258">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2483c-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="2483c-259"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2483c-260">(27)</span><span class="sxs-lookup"><span data-stu-id="2483c-260">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-261">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="2483c-261">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2483c-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="2483c-262"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2483c-263">(28)</span><span class="sxs-lookup"><span data-stu-id="2483c-263">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-264">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="2483c-264">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2483c-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="2483c-265"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2483c-266">(29)</span><span class="sxs-lookup"><span data-stu-id="2483c-266">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-267">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="2483c-267">Device is disabled.</span></span> <span data-ttu-id="2483c-268">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2483c-268">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2483c-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="2483c-269"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2483c-270">(30)</span><span class="sxs-lookup"><span data-stu-id="2483c-270">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-271">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="2483c-271">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2483c-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="2483c-272"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2483c-273">1-31</span><span class="sxs-lookup"><span data-stu-id="2483c-273">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-274">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="2483c-274">Device is not working properly.</span></span> <span data-ttu-id="2483c-275">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="2483c-275">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2483c-276">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="2483c-276">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-277">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2483c-277">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-279">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2483c-279">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-280">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="2483c-280">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2483c-281">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-281">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-282">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2483c-282">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-283">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-284">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-285">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2483c-285">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2483c-286">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2483c-286">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2483c-287">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="2483c-287">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="2483c-288">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-288">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-289">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2483c-289">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-292">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="2483c-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-293">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2483c-293">Description of the object.</span></span>

<span data-ttu-id="2483c-294">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-294">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-295">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2483c-295">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-298">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="2483c-298">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-299">Уникальный идентификатор теплового канала.</span><span class="sxs-lookup"><span data-stu-id="2483c-299">Unique identifier of the heat pipe.</span></span>

<span data-ttu-id="2483c-300">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-301">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="2483c-301">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-302">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2483c-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2483c-304">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="2483c-304">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="2483c-305">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-306">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2483c-306">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2483c-309">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="2483c-309">More information about the error that is recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="2483c-310">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-311">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2483c-311">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-312">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2483c-312">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-314">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="2483c-314">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-315">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="2483c-315">Date and time the object was installed.</span></span> <span data-ttu-id="2483c-316">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="2483c-316">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2483c-317">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-317">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-318">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="2483c-318">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-319">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2483c-319">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2483c-321">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="2483c-321">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2483c-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-323">**Name**</span><span class="sxs-lookup"><span data-stu-id="2483c-323">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-326">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="2483c-326">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-327">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="2483c-327">Label by which the object is known.</span></span> <span data-ttu-id="2483c-328">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="2483c-328">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2483c-329">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-329">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-330">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2483c-330">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-333">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2483c-333">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-334">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-334">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2483c-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2483c-336">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2483c-336">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2483c-337">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="2483c-337">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-338">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="2483c-338">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2483c-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2483c-340">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="2483c-340">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2483c-341">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-341">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2483c-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2483c-342"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2483c-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="2483c-343"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-344">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="2483c-344">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2483c-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="2483c-345"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2483c-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="2483c-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-347">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="2483c-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2483c-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="2483c-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-349">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="2483c-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2483c-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="2483c-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-351">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="2483c-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2483c-352">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="2483c-352">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="2483c-353">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="2483c-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2483c-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="2483c-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-355">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="2483c-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2483c-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="2483c-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2483c-357">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="2483c-357">Timed Power-On Supported</span></span>

<span data-ttu-id="2483c-358">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="2483c-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2483c-359">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="2483c-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-360">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2483c-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2483c-362">Если **значение — true**, Управление питанием устройства может осуществляться в режиме приостановки и т. д.</span><span class="sxs-lookup"><span data-stu-id="2483c-362">If **TRUE**, the device can be power-managed put into suspend mode, and so on.</span></span> <span data-ttu-id="2483c-363">Свойство не указывает на то, что функции управления питанием включены в настоящее время, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="2483c-363">The property does not indicate that power management features are enabled currently, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="2483c-364">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-365">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2483c-365">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-366">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-368">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="2483c-368">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-369">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2483c-369">Current status of the object.</span></span> <span data-ttu-id="2483c-370">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="2483c-370">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2483c-371">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="2483c-371">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2483c-372">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="2483c-372">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2483c-373">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="2483c-373">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2483c-374">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="2483c-374">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2483c-375">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-375">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2483c-376">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="2483c-376">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2483c-377">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="2483c-377">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2483c-378">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="2483c-378">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2483c-379">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="2483c-379">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2483c-380">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="2483c-380">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2483c-381">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="2483c-381">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2483c-382">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="2483c-382">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2483c-383">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="2483c-383">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2483c-384">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="2483c-384">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2483c-385">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="2483c-385">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2483c-386">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="2483c-386">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2483c-387">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="2483c-387">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2483c-388">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="2483c-388">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2483c-389">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2483c-389">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-390">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2483c-390">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-392">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2483c-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2483c-393">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="2483c-393">State of the logical device.</span></span> <span data-ttu-id="2483c-394">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="2483c-394">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2483c-395">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-395">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2483c-396">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="2483c-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2483c-397">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="2483c-397">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2483c-398">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="2483c-398">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2483c-399">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="2483c-399">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2483c-400">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="2483c-400">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2483c-401">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="2483c-401">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-402">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-404">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2483c-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2483c-405">Значение для свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="2483c-405">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="2483c-406">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2483c-407">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2483c-407">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2483c-408">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2483c-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2483c-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2483c-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2483c-410">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2483c-410">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2483c-411">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="2483c-411">Name of the scoping system.</span></span>

<span data-ttu-id="2483c-412">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="2483c-412">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2483c-413">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2483c-413">Remarks</span></span>

<span data-ttu-id="2483c-414">Класс **Win32 \_ хеатпипе** является производным от [**CIM \_ хеатпипе**](cim-heatpipe.md).</span><span class="sxs-lookup"><span data-stu-id="2483c-414">The **Win32\_HeatPipe** class is derived from [**CIM\_HeatPipe**](cim-heatpipe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2483c-415">Требования</span><span class="sxs-lookup"><span data-stu-id="2483c-415">Requirements</span></span>



| <span data-ttu-id="2483c-416">Требование</span><span class="sxs-lookup"><span data-stu-id="2483c-416">Requirement</span></span> | <span data-ttu-id="2483c-417">Значение</span><span class="sxs-lookup"><span data-stu-id="2483c-417">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2483c-418">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2483c-418">Minimum supported client</span></span><br/> | <span data-ttu-id="2483c-419">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2483c-419">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2483c-420">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2483c-420">Minimum supported server</span></span><br/> | <span data-ttu-id="2483c-421">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2483c-421">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2483c-422">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2483c-422">Namespace</span></span><br/>                | <span data-ttu-id="2483c-423">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2483c-423">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2483c-424">MOF</span><span class="sxs-lookup"><span data-stu-id="2483c-424">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2483c-425"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2483c-425"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2483c-426">DLL</span><span class="sxs-lookup"><span data-stu-id="2483c-426">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2483c-427"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2483c-427"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2483c-428">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2483c-428">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2483c-429">**\_ХЕАТПИПЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="2483c-429">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dt>

[<span data-ttu-id="2483c-430">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="2483c-430">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

