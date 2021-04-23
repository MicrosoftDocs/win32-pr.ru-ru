---
description: '&Win32 \_ холодильника \# 32; Класс WMI представляет свойства устройства холодильника.'
ms.assetid: d67ce648-5659-49e5-9427-7c4dbcdfda8c
ms.tgt_platform: multiple
title: Класс Win32_Refrigeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Refrigeration
- Win32_Refrigeration.Reset
- Win32_Refrigeration.SetPowerState
- Win32_Refrigeration.ActiveCooling
- Win32_Refrigeration.Availability
- Win32_Refrigeration.Caption
- Win32_Refrigeration.ConfigManagerErrorCode
- Win32_Refrigeration.ConfigManagerUserConfig
- Win32_Refrigeration.CreationClassName
- Win32_Refrigeration.Description
- Win32_Refrigeration.DeviceID
- Win32_Refrigeration.ErrorCleared
- Win32_Refrigeration.ErrorDescription
- Win32_Refrigeration.InstallDate
- Win32_Refrigeration.LastErrorCode
- Win32_Refrigeration.Name
- Win32_Refrigeration.PNPDeviceID
- Win32_Refrigeration.PowerManagementCapabilities
- Win32_Refrigeration.PowerManagementSupported
- Win32_Refrigeration.Status
- Win32_Refrigeration.StatusInfo
- Win32_Refrigeration.SystemCreationClassName
- Win32_Refrigeration.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23db1490d184cbfe38d6c5b65fa7190273ad2a87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990411"
---
# <a name="win32_refrigeration-class"></a><span data-ttu-id="a541f-103">\_Класс Win32 холодильника</span><span class="sxs-lookup"><span data-stu-id="a541f-103">Win32\_Refrigeration class</span></span>

<span data-ttu-id="a541f-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ холодильника для Win32** представляет свойства устройства холодильника.</span><span class="sxs-lookup"><span data-stu-id="a541f-104">The **Win32\_Refrigeration** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a refrigeration device.</span></span>

<span data-ttu-id="a541f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a541f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a541f-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a541f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a541f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a541f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{464FFAB6-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class Win32_Refrigeration : CIM_Refrigeration
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

## <a name="members"></a><span data-ttu-id="a541f-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a541f-108">Members</span></span>

<span data-ttu-id="a541f-109">Класс **Win32 \_ холодильника** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a541f-109">The **Win32\_Refrigeration** class has these types of members:</span></span>

-   [<span data-ttu-id="a541f-110">Методы</span><span class="sxs-lookup"><span data-stu-id="a541f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="a541f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a541f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a541f-112">Методы</span><span class="sxs-lookup"><span data-stu-id="a541f-112">Methods</span></span>

<span data-ttu-id="a541f-113">Класс **Win32 \_ холодильника** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a541f-113">The **Win32\_Refrigeration** class has these methods.</span></span>



| <span data-ttu-id="a541f-114">Метод</span><span class="sxs-lookup"><span data-stu-id="a541f-114">Method</span></span>            | <span data-ttu-id="a541f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="a541f-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a541f-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="a541f-116">**Reset**</span></span>         | <span data-ttu-id="a541f-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="a541f-117">Not implemented.</span></span> <span data-ttu-id="a541f-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ холодильника**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span><br/>                 |
| <span data-ttu-id="a541f-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="a541f-119">**SetPowerState**</span></span> | <span data-ttu-id="a541f-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="a541f-120">Not implemented.</span></span> <span data-ttu-id="a541f-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ холодильника**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a541f-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="a541f-122">Properties</span></span>

<span data-ttu-id="a541f-123">Класс **Win32 \_ холодильника** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a541f-123">The **Win32\_Refrigeration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a541f-124">**активекулинг**</span><span class="sxs-lookup"><span data-stu-id="a541f-124">**ActiveCooling**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-125">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a541f-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541f-127">При **значении true** устройство охлаждения обеспечивает активное охлаждение, а не пассивное охлаждение.</span><span class="sxs-lookup"><span data-stu-id="a541f-127">If **TRUE**, the cooling device provides active cooling—not passive cooling.</span></span>

<span data-ttu-id="a541f-128">Это свойство наследуется от [**CIM \_ кулингдевице**](cim-coolingdevice.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-128">This property is inherited from [**CIM\_CoolingDevice**](cim-coolingdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-129">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="a541f-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a541f-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-132">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="a541f-132">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-133">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-133">Availability and status of the device.</span></span>

<span data-ttu-id="a541f-134">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a541f-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a541f-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a541f-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="a541f-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="a541f-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="a541f-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-138">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="a541f-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="a541f-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="a541f-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="a541f-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="a541f-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a541f-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="a541f-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="a541f-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="a541f-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="a541f-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="a541f-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="a541f-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="a541f-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a541f-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="a541f-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="a541f-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="a541f-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="a541f-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="a541f-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="a541f-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="a541f-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-149">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="a541f-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="a541f-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="a541f-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-151">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="a541f-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="a541f-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="a541f-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-153">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="a541f-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="a541f-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="a541f-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="a541f-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="a541f-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-156">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="a541f-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="a541f-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="a541f-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-158">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="a541f-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="a541f-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="a541f-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-160">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="a541f-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="a541f-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="a541f-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-162">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="a541f-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="a541f-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="a541f-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-164">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="a541f-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a541f-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a541f-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-168">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a541f-168">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-169">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="a541f-169">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="a541f-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-171">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="a541f-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a541f-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-174">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a541f-174">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-175">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a541f-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="a541f-176">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="a541f-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="a541f-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="a541f-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="a541f-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-179">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="a541f-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="a541f-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="a541f-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="a541f-181">(1)</span><span class="sxs-lookup"><span data-stu-id="a541f-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-182">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="a541f-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a541f-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="a541f-184">(2)</span><span class="sxs-lookup"><span data-stu-id="a541f-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="a541f-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="a541f-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="a541f-186">(3)</span><span class="sxs-lookup"><span data-stu-id="a541f-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-187">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a541f-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a541f-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="a541f-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="a541f-189">(4)</span><span class="sxs-lookup"><span data-stu-id="a541f-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-190">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="a541f-190">Device is not working properly.</span></span> <span data-ttu-id="a541f-191">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="a541f-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="a541f-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="a541f-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="a541f-193">(5)</span><span class="sxs-lookup"><span data-stu-id="a541f-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-194">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="a541f-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="a541f-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="a541f-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="a541f-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="a541f-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-197">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="a541f-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="a541f-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="a541f-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="a541f-199">(7)</span><span class="sxs-lookup"><span data-stu-id="a541f-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="a541f-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="a541f-201">(8)</span><span class="sxs-lookup"><span data-stu-id="a541f-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-202">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="a541f-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="a541f-204">(9)</span><span class="sxs-lookup"><span data-stu-id="a541f-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-205">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="a541f-205">Device is not working properly.</span></span> <span data-ttu-id="a541f-206">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="a541f-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="a541f-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="a541f-208">(10)</span><span class="sxs-lookup"><span data-stu-id="a541f-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-209">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="a541f-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="a541f-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="a541f-211">(11)</span><span class="sxs-lookup"><span data-stu-id="a541f-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-212">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="a541f-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="a541f-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="a541f-214">(12)</span><span class="sxs-lookup"><span data-stu-id="a541f-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-215">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="a541f-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="a541f-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="a541f-217">(13)</span><span class="sxs-lookup"><span data-stu-id="a541f-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-218">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="a541f-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="a541f-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="a541f-220">(14)</span><span class="sxs-lookup"><span data-stu-id="a541f-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-221">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="a541f-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="a541f-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="a541f-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="a541f-223">(15)</span><span class="sxs-lookup"><span data-stu-id="a541f-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-224">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="a541f-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="a541f-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="a541f-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="a541f-226">(16)</span><span class="sxs-lookup"><span data-stu-id="a541f-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-227">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="a541f-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="a541f-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="a541f-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="a541f-229">(17)</span><span class="sxs-lookup"><span data-stu-id="a541f-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-230">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="a541f-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a541f-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="a541f-232">(18)</span><span class="sxs-lookup"><span data-stu-id="a541f-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-233">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="a541f-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="a541f-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="a541f-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="a541f-235">(19)</span><span class="sxs-lookup"><span data-stu-id="a541f-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="a541f-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="a541f-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="a541f-237">(20)</span><span class="sxs-lookup"><span data-stu-id="a541f-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-238">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="a541f-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="a541f-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="a541f-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="a541f-240">(21)</span><span class="sxs-lookup"><span data-stu-id="a541f-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-241">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="a541f-241">System failure.</span></span> <span data-ttu-id="a541f-242">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="a541f-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="a541f-243">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="a541f-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="a541f-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="a541f-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="a541f-245">(22)</span><span class="sxs-lookup"><span data-stu-id="a541f-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-246">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="a541f-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="a541f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="a541f-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="a541f-248">(23)</span><span class="sxs-lookup"><span data-stu-id="a541f-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-249">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="a541f-249">System failure.</span></span> <span data-ttu-id="a541f-250">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="a541f-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="a541f-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="a541f-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="a541f-252">(24)</span><span class="sxs-lookup"><span data-stu-id="a541f-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-253">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="a541f-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a541f-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="a541f-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a541f-255">(25)</span><span class="sxs-lookup"><span data-stu-id="a541f-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-256">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="a541f-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="a541f-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="a541f-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="a541f-258">(26)</span><span class="sxs-lookup"><span data-stu-id="a541f-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-259">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="a541f-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="a541f-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="a541f-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="a541f-261">(27)</span><span class="sxs-lookup"><span data-stu-id="a541f-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-262">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="a541f-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="a541f-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="a541f-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="a541f-264">(28)</span><span class="sxs-lookup"><span data-stu-id="a541f-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-265">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="a541f-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="a541f-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="a541f-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="a541f-267">(29)</span><span class="sxs-lookup"><span data-stu-id="a541f-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-268">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="a541f-268">Device is disabled.</span></span> <span data-ttu-id="a541f-269">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a541f-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="a541f-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="a541f-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="a541f-271">(30)</span><span class="sxs-lookup"><span data-stu-id="a541f-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-272">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="a541f-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="a541f-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="a541f-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="a541f-274">1-31</span><span class="sxs-lookup"><span data-stu-id="a541f-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-275">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="a541f-275">Device is not working properly.</span></span> <span data-ttu-id="a541f-276">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="a541f-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a541f-277">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="a541f-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-278">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a541f-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-280">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a541f-280">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-281">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="a541f-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="a541f-282">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a541f-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-286">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a541f-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a541f-287">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a541f-287">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a541f-288">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="a541f-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="a541f-289">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-290">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a541f-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-293">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="a541f-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-294">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a541f-294">Description of the object.</span></span>

<span data-ttu-id="a541f-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="a541f-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-299">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="a541f-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-300">Уникальный идентификатор устройства холодильника.</span><span class="sxs-lookup"><span data-stu-id="a541f-300">Unique identifier of the refrigeration device.</span></span>

<span data-ttu-id="a541f-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-302">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="a541f-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-303">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a541f-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541f-305">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="a541f-305">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="a541f-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="a541f-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541f-310">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="a541f-310">More information about the error recorded in **LastErrorCode**, and any corrective actions that may be taken.</span></span>

<span data-ttu-id="a541f-311">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-312">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a541f-312">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-313">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a541f-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-315">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="a541f-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-316">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="a541f-316">Date and time the object was installed.</span></span> <span data-ttu-id="a541f-317">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="a541f-317">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a541f-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-319">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="a541f-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-320">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a541f-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541f-322">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="a541f-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="a541f-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-324">**Name**</span><span class="sxs-lookup"><span data-stu-id="a541f-324">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-327">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="a541f-327">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-328">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="a541f-328">Label by which the object is known.</span></span> <span data-ttu-id="a541f-329">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="a541f-329">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a541f-330">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-330">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-331">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="a541f-331">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-332">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-334">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a541f-334">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-335">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-335">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="a541f-336">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-336">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="a541f-337">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="a541f-337">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="a541f-338">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="a541f-338">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-339">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="a541f-339">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a541f-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541f-341">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="a541f-341">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="a541f-342">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-342">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a541f-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a541f-343"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a541f-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="a541f-344"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-345">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="a541f-345">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a541f-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="a541f-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a541f-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="a541f-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-348">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="a541f-348">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="a541f-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="a541f-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-350">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="a541f-350">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="a541f-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="a541f-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-352">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="a541f-352">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="a541f-353">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="a541f-353">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="a541f-354">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-354">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="a541f-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="a541f-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-356">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="a541f-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="a541f-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="a541f-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="a541f-358">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="a541f-358">Timed Power-On Supported</span></span>

<span data-ttu-id="a541f-359">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="a541f-359">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a541f-360">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="a541f-360">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-361">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="a541f-361">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a541f-363">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="a541f-363">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="a541f-364">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="a541f-364">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="a541f-365">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-366">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a541f-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-369">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="a541f-369">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-370">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a541f-370">Current status of the object.</span></span> <span data-ttu-id="a541f-371">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="a541f-371">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a541f-372">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="a541f-372">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a541f-373">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="a541f-373">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a541f-374">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="a541f-374">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a541f-375">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a541f-375">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a541f-376">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a541f-377">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="a541f-377">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a541f-378">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="a541f-378">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a541f-379">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="a541f-379">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a541f-380">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="a541f-380">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a541f-381">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a541f-381">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a541f-382">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a541f-382">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a541f-383">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a541f-383">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a541f-384">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="a541f-384">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a541f-385">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="a541f-385">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a541f-386">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="a541f-386">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a541f-387">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="a541f-387">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a541f-388">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="a541f-388">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a541f-389">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="a541f-389">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a541f-390">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="a541f-390">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-391">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a541f-391">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-393">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="a541f-393">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="a541f-394">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="a541f-394">State of the logical device.</span></span> <span data-ttu-id="a541f-395">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="a541f-395">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="a541f-396">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a541f-397">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="a541f-397">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a541f-398">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="a541f-398">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a541f-399">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="a541f-399">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a541f-400">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="a541f-400">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="a541f-401">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="a541f-401">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a541f-402">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a541f-402">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-405">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a541f-405">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a541f-406">Значение для свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="a541f-406">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="a541f-407">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-407">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="a541f-408">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a541f-408">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a541f-409">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a541f-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a541f-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a541f-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a541f-411">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="a541f-411">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="a541f-412">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="a541f-412">Name of the scoping system.</span></span>

<span data-ttu-id="a541f-413">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="a541f-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a541f-414">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a541f-414">Remarks</span></span>

<span data-ttu-id="a541f-415">Класс **Win32 \_ холодильника** является производным от [**CIM \_ холодильника**](cim-refrigeration.md).</span><span class="sxs-lookup"><span data-stu-id="a541f-415">The **Win32\_Refrigeration** class is derived from [**CIM\_Refrigeration**](cim-refrigeration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a541f-416">Требования</span><span class="sxs-lookup"><span data-stu-id="a541f-416">Requirements</span></span>



| <span data-ttu-id="a541f-417">Требование</span><span class="sxs-lookup"><span data-stu-id="a541f-417">Requirement</span></span> | <span data-ttu-id="a541f-418">Значение</span><span class="sxs-lookup"><span data-stu-id="a541f-418">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a541f-419">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a541f-419">Minimum supported client</span></span><br/> | <span data-ttu-id="a541f-420">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a541f-420">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a541f-421">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a541f-421">Minimum supported server</span></span><br/> | <span data-ttu-id="a541f-422">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a541f-422">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a541f-423">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a541f-423">Namespace</span></span><br/>                | <span data-ttu-id="a541f-424">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a541f-424">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a541f-425">MOF</span><span class="sxs-lookup"><span data-stu-id="a541f-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a541f-426"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a541f-426"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a541f-427">DLL</span><span class="sxs-lookup"><span data-stu-id="a541f-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a541f-428"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a541f-428"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a541f-429">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a541f-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a541f-430">**\_Холодильника CIM**</span><span class="sxs-lookup"><span data-stu-id="a541f-430">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dt>

[<span data-ttu-id="a541f-431">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a541f-431">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
