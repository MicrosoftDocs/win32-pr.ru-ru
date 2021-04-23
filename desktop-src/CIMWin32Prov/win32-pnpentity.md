---
description: Епресентс свойства устройства самонастраивающийся.
ms.assetid: 621f4410-8d8f-4afa-b0f0-beed263f3a13
ms.tgt_platform: multiple
title: Класс Win32_PnPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity
- Win32_PnPEntity.Reset
- Win32_PnPEntity.SetPowerState
- Win32_PnPEntity.Availability
- Win32_PnPEntity.Caption
- Win32_PnPEntity.ClassGuid
- Win32_PnPEntity.CompatibleID
- Win32_PnPEntity.ConfigManagerErrorCode
- Win32_PnPEntity.ConfigManagerUserConfig
- Win32_PnPEntity.CreationClassName
- Win32_PnPEntity.Description
- Win32_PnPEntity.DeviceID
- Win32_PnPEntity.ErrorCleared
- Win32_PnPEntity.ErrorDescription
- Win32_PnPEntity.HardwareID
- Win32_PnPEntity.InstallDate
- Win32_PnPEntity.LastErrorCode
- Win32_PnPEntity.Manufacturer
- Win32_PnPEntity.Name
- Win32_PnPEntity.PNPClass
- Win32_PnPEntity.PNPDeviceID
- Win32_PnPEntity.PowerManagementCapabilities
- Win32_PnPEntity.PowerManagementSupported
- Win32_PnPEntity.Present
- Win32_PnPEntity.Service
- Win32_PnPEntity.Status
- Win32_PnPEntity.StatusInfo
- Win32_PnPEntity.SystemCreationClassName
- Win32_PnPEntity.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62eaa59944c9b71a1b8b3520969122ab23350bba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141051"
---
# <a name="win32_pnpentity-class"></a><span data-ttu-id="62164-103">\_Класс Win32 пнпентити</span><span class="sxs-lookup"><span data-stu-id="62164-103">Win32\_PnPEntity class</span></span>

<span data-ttu-id="62164-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ пнпентити для Win32** представляет свойства устройства Самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-104">The **Win32\_PnPEntity** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a Plug and Play device.</span></span> <span data-ttu-id="62164-105">Самонастраивающийся сущности отображаются как записи в диспетчер устройств, расположенном в панели управления.</span><span class="sxs-lookup"><span data-stu-id="62164-105">Plug and Play entities are shown as entries in the Device Manager located in Control Panel.</span></span>

<span data-ttu-id="62164-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="62164-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="62164-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="62164-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62164-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62164-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FE28FD98-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPEntity : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  string   ClassGuid;
  string   CompatibleID[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareID[];
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  string   Name;
  string   PNPClass;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  boolean  Present;
  string   Service;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="62164-109">Члены</span><span class="sxs-lookup"><span data-stu-id="62164-109">Members</span></span>

<span data-ttu-id="62164-110">Класс **Win32 \_ пнпентити** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="62164-110">The **Win32\_PnPEntity** class has these types of members:</span></span>

-   [<span data-ttu-id="62164-111">Методы</span><span class="sxs-lookup"><span data-stu-id="62164-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="62164-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="62164-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="62164-113">Методы</span><span class="sxs-lookup"><span data-stu-id="62164-113">Methods</span></span>

<span data-ttu-id="62164-114">Класс **Win32 \_ пнпентити** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="62164-114">The **Win32\_PnPEntity** class has these methods.</span></span>



| <span data-ttu-id="62164-115">Метод</span><span class="sxs-lookup"><span data-stu-id="62164-115">Method</span></span>                                                             | <span data-ttu-id="62164-116">Описание</span><span class="sxs-lookup"><span data-stu-id="62164-116">Description</span></span>                                                                                                                                                                                    |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62164-117">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="62164-117">**Disable**</span></span>](disable-win32-pnpentity.md)                         | <span data-ttu-id="62164-118">Отключает это устройство самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-118">Disables this Plug and Play device.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="62164-119">**Включить**</span><span class="sxs-lookup"><span data-stu-id="62164-119">**Enable**</span></span>](enable-win32-pnpentity.md)                           | <span data-ttu-id="62164-120">Включает это самонастраивающийся устройство.</span><span class="sxs-lookup"><span data-stu-id="62164-120">Enables this Plug and Play device.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="62164-121">**жетдевицепропертиес**</span><span class="sxs-lookup"><span data-stu-id="62164-121">**GetDeviceProperties**</span></span>](getdeviceproperties-win32-pnpentity.md) | <span data-ttu-id="62164-122">Возвращает указанные свойства данного устройства самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-122">Gets the specified properties of this Plug and Play device.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="62164-123">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="62164-123">**Reset**</span></span>                                                          | <span data-ttu-id="62164-124">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="62164-124">Not implemented.</span></span> <span data-ttu-id="62164-125">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="62164-125">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="62164-126">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="62164-126">**SetPowerState**</span></span>                                                  | <span data-ttu-id="62164-127">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="62164-127">Not implemented.</span></span> <span data-ttu-id="62164-128">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="62164-128">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="62164-129">Свойства</span><span class="sxs-lookup"><span data-stu-id="62164-129">Properties</span></span>

<span data-ttu-id="62164-130">Класс **Win32 \_ пнпентити** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="62164-130">The **Win32\_PnPEntity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62164-131">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="62164-131">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-132">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62164-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62164-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-134">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="62164-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="62164-135">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-135">Availability and status of the device.</span></span>

<span data-ttu-id="62164-136">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-136">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62164-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="62164-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62164-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="62164-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="62164-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="62164-139"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="62164-140">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="62164-140">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="62164-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="62164-141"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="62164-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="62164-142"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="62164-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="62164-143"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="62164-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="62164-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="62164-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="62164-145"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="62164-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="62164-146"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="62164-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="62164-147"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="62164-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="62164-148"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="62164-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="62164-149"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="62164-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="62164-150"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="62164-151">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="62164-151">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="62164-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="62164-152"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="62164-153">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="62164-153">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="62164-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="62164-154"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="62164-155">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="62164-155">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="62164-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="62164-156"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="62164-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="62164-157"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="62164-158">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="62164-158">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="62164-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="62164-159"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="62164-160">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="62164-160">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="62164-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="62164-161"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="62164-162">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="62164-162">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="62164-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="62164-163"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="62164-164">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="62164-164">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="62164-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="62164-165"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="62164-166">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="62164-166">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62164-167">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="62164-167">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-170">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="62164-170">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="62164-171">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="62164-171">Short description of the object.</span></span>

<span data-ttu-id="62164-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62164-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-173">**классгуид**</span><span class="sxs-lookup"><span data-stu-id="62164-173">**ClassGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-176">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62164-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62164-177">Глобальный уникальный идентификатор (GUID) этого устройства самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-177">Globally unique identifier (GUID) of this Plug and Play device.</span></span>

</dd> <dt>

<span data-ttu-id="62164-178">**компатиблеид**</span><span class="sxs-lookup"><span data-stu-id="62164-178">**CompatibleID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-179">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="62164-179">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62164-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-181">Определяемая поставщиком строка идентификации, используемая программой установки для сопоставления устройства с INF-файлом.</span><span class="sxs-lookup"><span data-stu-id="62164-181">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="62164-182">У устройства может быть список совместимых кодов, связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="62164-182">A device can have a list of compatible IDs associated with it.</span></span> <span data-ttu-id="62164-183">Совместимые идентификаторы должны быть перечислены в порядке убывания пригодности.</span><span class="sxs-lookup"><span data-stu-id="62164-183">The compatible IDs should be listed in order of decreasing suitability.</span></span> <span data-ttu-id="62164-184">Если программе установки не удается выполнить поиск INF-файла, соответствующего одному из идентификаторов оборудования устройства, для поиска INF-файла используются совместимые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="62164-184">If Setup cannot locate an INF file that matches one of a device's hardware IDs, it uses compatible IDs to locate an INF file.</span></span> <span data-ttu-id="62164-185">Совместимый идентификатор имеет тот же формат, что и **хардвареид**.</span><span class="sxs-lookup"><span data-stu-id="62164-185">A compatible ID has the same format as a **HardwareID**.</span></span> <span data-ttu-id="62164-186">Дополнительные сведения см. в разделе [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="62164-186">For more information, see [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="62164-187">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="62164-187">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-188">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62164-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62164-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-190">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62164-190">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62164-191">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="62164-191">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="62164-192">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-192">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="62164-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="62164-193"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="62164-194"> (0)</span><span class="sxs-lookup"><span data-stu-id="62164-194">(0)</span></span>


</dt> <dd>

<span data-ttu-id="62164-195">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="62164-195">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="62164-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="62164-196"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="62164-197">(1)</span><span class="sxs-lookup"><span data-stu-id="62164-197">(1)</span></span>


</dt> <dd>

<span data-ttu-id="62164-198">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="62164-198">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62164-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-199"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="62164-200">(2)</span><span class="sxs-lookup"><span data-stu-id="62164-200">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="62164-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="62164-201"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="62164-202">(3)</span><span class="sxs-lookup"><span data-stu-id="62164-202">(3)</span></span>


</dt> <dd>

<span data-ttu-id="62164-203">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62164-203">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="62164-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="62164-204"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="62164-205">(4)</span><span class="sxs-lookup"><span data-stu-id="62164-205">(4)</span></span>


</dt> <dd>

<span data-ttu-id="62164-206">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="62164-206">Device is not working properly.</span></span> <span data-ttu-id="62164-207">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="62164-207">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="62164-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="62164-208"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="62164-209">(5)</span><span class="sxs-lookup"><span data-stu-id="62164-209">(5)</span></span>


</dt> <dd>

<span data-ttu-id="62164-210">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="62164-210">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="62164-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="62164-211"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="62164-212"> (6)</span><span class="sxs-lookup"><span data-stu-id="62164-212">(6)</span></span>


</dt> <dd>

<span data-ttu-id="62164-213">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="62164-213">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="62164-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="62164-214"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="62164-215">(7)</span><span class="sxs-lookup"><span data-stu-id="62164-215">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="62164-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-216"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="62164-217">(8)</span><span class="sxs-lookup"><span data-stu-id="62164-217">(8)</span></span>


</dt> <dd>

<span data-ttu-id="62164-218">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-218">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="62164-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-219"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="62164-220">(9)</span><span class="sxs-lookup"><span data-stu-id="62164-220">(9)</span></span>


</dt> <dd>

<span data-ttu-id="62164-221">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="62164-221">Device is not working properly.</span></span> <span data-ttu-id="62164-222">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-222">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="62164-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="62164-223"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="62164-224">(10)</span><span class="sxs-lookup"><span data-stu-id="62164-224">(10)</span></span>


</dt> <dd>

<span data-ttu-id="62164-225">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="62164-225">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="62164-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-226"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="62164-227">(11)</span><span class="sxs-lookup"><span data-stu-id="62164-227">(11)</span></span>


</dt> <dd>

<span data-ttu-id="62164-228">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-228">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="62164-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="62164-229"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="62164-230">(12)</span><span class="sxs-lookup"><span data-stu-id="62164-230">(12)</span></span>


</dt> <dd>

<span data-ttu-id="62164-231">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="62164-231">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="62164-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-232"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="62164-233">(13)</span><span class="sxs-lookup"><span data-stu-id="62164-233">(13)</span></span>


</dt> <dd>

<span data-ttu-id="62164-234">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-234">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="62164-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="62164-235"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="62164-236">(14)</span><span class="sxs-lookup"><span data-stu-id="62164-236">(14)</span></span>


</dt> <dd>

<span data-ttu-id="62164-237">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="62164-237">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="62164-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="62164-238"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="62164-239">(15)</span><span class="sxs-lookup"><span data-stu-id="62164-239">(15)</span></span>


</dt> <dd>

<span data-ttu-id="62164-240">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="62164-240">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="62164-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="62164-241"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="62164-242">(16)</span><span class="sxs-lookup"><span data-stu-id="62164-242">(16)</span></span>


</dt> <dd>

<span data-ttu-id="62164-243">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="62164-243">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="62164-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="62164-244"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="62164-245">(17)</span><span class="sxs-lookup"><span data-stu-id="62164-245">(17)</span></span>


</dt> <dd>

<span data-ttu-id="62164-246">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="62164-246">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62164-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-247"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="62164-248">(18)</span><span class="sxs-lookup"><span data-stu-id="62164-248">(18)</span></span>


</dt> <dd>

<span data-ttu-id="62164-249">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="62164-249">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="62164-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="62164-250"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="62164-251">(19)</span><span class="sxs-lookup"><span data-stu-id="62164-251">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="62164-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="62164-252"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="62164-253">(20)</span><span class="sxs-lookup"><span data-stu-id="62164-253">(20)</span></span>


</dt> <dd>

<span data-ttu-id="62164-254">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="62164-254">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="62164-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="62164-255"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="62164-256">(21)</span><span class="sxs-lookup"><span data-stu-id="62164-256">(21)</span></span>


</dt> <dd>

<span data-ttu-id="62164-257">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="62164-257">System failure.</span></span> <span data-ttu-id="62164-258">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="62164-258">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="62164-259">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="62164-259">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="62164-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="62164-260"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="62164-261">(22)</span><span class="sxs-lookup"><span data-stu-id="62164-261">(22)</span></span>


</dt> <dd>

<span data-ttu-id="62164-262">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="62164-262">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="62164-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="62164-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="62164-264">(23)</span><span class="sxs-lookup"><span data-stu-id="62164-264">(23)</span></span>


</dt> <dd>

<span data-ttu-id="62164-265">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="62164-265">System failure.</span></span> <span data-ttu-id="62164-266">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="62164-266">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="62164-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="62164-267"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="62164-268">(24)</span><span class="sxs-lookup"><span data-stu-id="62164-268">(24)</span></span>


</dt> <dd>

<span data-ttu-id="62164-269">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="62164-269">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="62164-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="62164-270"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="62164-271">(25)</span><span class="sxs-lookup"><span data-stu-id="62164-271">(25)</span></span>


</dt> <dd>

<span data-ttu-id="62164-272">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="62164-272">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="62164-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="62164-273"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="62164-274">(26)</span><span class="sxs-lookup"><span data-stu-id="62164-274">(26)</span></span>


</dt> <dd>

<span data-ttu-id="62164-275">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="62164-275">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="62164-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="62164-276"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="62164-277">(27)</span><span class="sxs-lookup"><span data-stu-id="62164-277">(27)</span></span>


</dt> <dd>

<span data-ttu-id="62164-278">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="62164-278">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="62164-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="62164-279"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="62164-280">(28)</span><span class="sxs-lookup"><span data-stu-id="62164-280">(28)</span></span>


</dt> <dd>

<span data-ttu-id="62164-281">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="62164-281">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="62164-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="62164-282"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="62164-283">(29)</span><span class="sxs-lookup"><span data-stu-id="62164-283">(29)</span></span>


</dt> <dd>

<span data-ttu-id="62164-284">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="62164-284">Device is disabled.</span></span> <span data-ttu-id="62164-285">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="62164-285">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="62164-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="62164-286"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="62164-287">(30)</span><span class="sxs-lookup"><span data-stu-id="62164-287">(30)</span></span>


</dt> <dd>

<span data-ttu-id="62164-288">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="62164-288">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="62164-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="62164-289"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="62164-290">1-31</span><span class="sxs-lookup"><span data-stu-id="62164-290">(31)</span></span>


</dt> <dd>

<span data-ttu-id="62164-291">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="62164-291">Device is not working properly.</span></span> <span data-ttu-id="62164-292">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="62164-292">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62164-293">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="62164-293">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-294">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62164-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62164-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-296">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62164-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62164-297">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="62164-297">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="62164-298">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-299">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="62164-299">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-302">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="62164-302">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="62164-303">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="62164-303">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="62164-304">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="62164-304">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="62164-305">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-306">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62164-306">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-309">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="62164-309">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="62164-310">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="62164-310">Description of the object.</span></span>

<span data-ttu-id="62164-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62164-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-312">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="62164-312">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-315">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62164-315">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62164-316">Идентификатор устройства самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-316">Identifier of the Plug and Play device.</span></span>

<span data-ttu-id="62164-317">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-318">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="62164-318">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-319">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62164-319">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62164-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-321">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="62164-321">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="62164-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-323">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="62164-323">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-326">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="62164-326">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="62164-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-328">**хардвареид**</span><span class="sxs-lookup"><span data-stu-id="62164-328">**HardwareID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-329">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="62164-329">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="62164-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-331">Определяемая поставщиком строка идентификации, используемая программой установки для сопоставления устройства с INF-файлом.</span><span class="sxs-lookup"><span data-stu-id="62164-331">A vendor-defined identification string that Setup uses to match a device to an INF file.</span></span> <span data-ttu-id="62164-332">Как правило, устройство имеет связанный список идентификаторов оборудования.</span><span class="sxs-lookup"><span data-stu-id="62164-332">Normally, a device has an associated list of hardware IDs.</span></span> <span data-ttu-id="62164-333">Исключением является драйвер шины 1394, который не использует идентификаторы оборудования.</span><span class="sxs-lookup"><span data-stu-id="62164-333">An exception is the 1394 bus driver, which does not use hardware IDs.</span></span> <span data-ttu-id="62164-334">Первым ИДЕНТИФИКАТОРом оборудования в списке должен быть идентификатор устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-334">The first hardware ID in the list should be the device ID.</span></span> <span data-ttu-id="62164-335">Остальные идентификаторы должны быть перечислены в порядке убывания пригодности.</span><span class="sxs-lookup"><span data-stu-id="62164-335">The remaining IDs should be listed in order of decreasing suitability.</span></span>

<span data-ttu-id="62164-336">Идентификаторы оборудования отображаются в одном из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="62164-336">Hardware IDs appear in one the following formats:</span></span>

-   <span data-ttu-id="62164-337">Перечислитель перечислителя \\ -Специальный-Device-ID</span><span class="sxs-lookup"><span data-stu-id="62164-337">enumerator\\enumerator-specific-device-ID</span></span>

    <span data-ttu-id="62164-338">Это наиболее распространенный формат для отдельных устройств PnP.</span><span class="sxs-lookup"><span data-stu-id="62164-338">This is the most common format for individual PnP devices.</span></span> <span data-ttu-id="62164-339">Примером перечислителя может быть BIOS или ISAPNP.</span><span class="sxs-lookup"><span data-stu-id="62164-339">An example of an enumerator is the BIOS or ISAPNP.</span></span>

-   <span data-ttu-id="62164-340">\*Идентификатор, зависящий от перечислителя</span><span class="sxs-lookup"><span data-stu-id="62164-340">\*enumerator-specific ID</span></span>

    <span data-ttu-id="62164-341">Звездочка ( \* ) указывает на использование более чем одним перечислителем.</span><span class="sxs-lookup"><span data-stu-id="62164-341">An asterisk (\*) indicates use by more than one enumerator.</span></span>

-   <span data-ttu-id="62164-342">Идентификатор, зависящий от класса устройства</span><span class="sxs-lookup"><span data-stu-id="62164-342">device-class-specific ID</span></span>

    <span data-ttu-id="62164-343">Пользовательский формат.</span><span class="sxs-lookup"><span data-stu-id="62164-343">A custom format.</span></span>

<span data-ttu-id="62164-344">Примеры идентификаторов оборудования:</span><span class="sxs-lookup"><span data-stu-id="62164-344">Examples of Hardware IDs are:</span></span>

<dl> <dd><span data-ttu-id="62164-345">корневой \\ \* PNPOF08</span><span class="sxs-lookup"><span data-stu-id="62164-345">root\\\*PNPOF08</span></span></dd> <dd><span data-ttu-id="62164-346">PC \\ типов ven \_ 1000&DEV \_ 001&СУБСИС \_ 00000000&версия \_ 02</span><span class="sxs-lookup"><span data-stu-id="62164-346">PC\\VEN\_1000&DEV\_001&SUBSYS\_00000000&REV\_02</span></span></dd> </dl>

<span data-ttu-id="62164-347">Дополнительные сведения см. в подразделе [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span><span class="sxs-lookup"><span data-stu-id="62164-347">For more information, see the [Windows Driver Kit](https://developer.microsoft.com/windows/hardware/download-kits-windows-hardware-development).</span></span>

</dd> <dt>

<span data-ttu-id="62164-348">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="62164-348">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-349">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="62164-349">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="62164-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-351">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="62164-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="62164-352">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="62164-352">Date and time the object was installed.</span></span> <span data-ttu-id="62164-353">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="62164-353">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="62164-354">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62164-354">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-355">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="62164-355">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-356">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62164-356">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62164-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-358">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="62164-358">Last error code reported by the logical device.</span></span>

<span data-ttu-id="62164-359">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-360">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="62164-360">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-363">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62164-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62164-364">Имя производителя устройства самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-364">Name of the manufacturer of the Plug and Play device.</span></span>

<span data-ttu-id="62164-365">Пример: ACME</span><span class="sxs-lookup"><span data-stu-id="62164-365">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="62164-366">**Name**</span><span class="sxs-lookup"><span data-stu-id="62164-366">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-369">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="62164-369">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="62164-370">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="62164-370">Label by which the object is known.</span></span> <span data-ttu-id="62164-371">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="62164-371">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="62164-372">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62164-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-373">**пнпкласс**</span><span class="sxs-lookup"><span data-stu-id="62164-373">**PNPClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-376">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62164-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

> [!WARNING]
> <span data-ttu-id="62164-377">Это свойство, несмотря на то, что указано в MOF-файле, фактически не существует в классе.</span><span class="sxs-lookup"><span data-stu-id="62164-377">This property, despite being listed in the MOF file, does not actually exist in the class.</span></span> <span data-ttu-id="62164-378">Это свойство описывается только в целях полноты, а также для уточнения самого MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="62164-378">The property is described here only for the sake of completeness, and to clarify the MOF file itself.</span></span>

 

<span data-ttu-id="62164-379">Имя типа этого самонастраивающийся устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-379">The name of the type of this Plug and Play device.</span></span>

<span data-ttu-id="62164-380">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство отсутствует в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="62164-380">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not in the MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="62164-381">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="62164-381">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-382">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-384">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="62164-384">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="62164-385">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-385">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="62164-386">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-386">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="62164-387">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="62164-387">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="62164-388">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="62164-388">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-389">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="62164-389">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="62164-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-391">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="62164-391">Not implemented.</span></span>

<span data-ttu-id="62164-392">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62164-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="62164-393"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="62164-394">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="62164-394">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="62164-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="62164-395"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="62164-396">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="62164-396">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="62164-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="62164-397"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="62164-398">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="62164-398">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="62164-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="62164-399"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="62164-400">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="62164-400">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="62164-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="62164-401"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="62164-402">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="62164-402">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="62164-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="62164-403"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="62164-404">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="62164-404">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="62164-405">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="62164-405">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="62164-406">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="62164-406">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="62164-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="62164-407"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="62164-408">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="62164-408">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="62164-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="62164-409"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="62164-410">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="62164-410">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="62164-411">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="62164-411">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-412">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62164-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62164-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62164-414">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="62164-414">Not implemented.</span></span>

<span data-ttu-id="62164-415">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-416">**Присутствует**</span><span class="sxs-lookup"><span data-stu-id="62164-416">**Present**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-417">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="62164-417">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62164-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-419">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62164-419">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62164-420">Является ли данное устройство самонастраивающийся в системе в данный момент.</span><span class="sxs-lookup"><span data-stu-id="62164-420">Whether this Plug and Play device is currently in the system.</span></span>

<span data-ttu-id="62164-421">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="62164-421">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="62164-422">**Служба**</span><span class="sxs-lookup"><span data-stu-id="62164-422">**Service**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-423">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-425">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="62164-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="62164-426">Имя службы, которая поддерживает это устройство самонастраивающийся.</span><span class="sxs-lookup"><span data-stu-id="62164-426">Name of the service that supports this Plug and Play device.</span></span> <span data-ttu-id="62164-427">Дополнительные сведения см. в разделе [**Win32 \_ системдриверпнпентити**](win32-systemdriverpnpentity.md).</span><span class="sxs-lookup"><span data-stu-id="62164-427">For more information, see [**Win32\_SystemDriverPnPEntity**](win32-systemdriverpnpentity.md).</span></span>

<span data-ttu-id="62164-428">Пример: "ATAPI"</span><span class="sxs-lookup"><span data-stu-id="62164-428">Example: "atapi"</span></span>

</dd> <dt>

<span data-ttu-id="62164-429">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="62164-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-432">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="62164-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="62164-433">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="62164-433">Current status of the object.</span></span> <span data-ttu-id="62164-434">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="62164-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="62164-435">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="62164-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="62164-436">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="62164-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="62164-437">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="62164-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="62164-438">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="62164-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="62164-439">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="62164-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="62164-440">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="62164-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="62164-441">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="62164-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="62164-442">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="62164-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="62164-443">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="62164-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62164-444">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="62164-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="62164-445">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="62164-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="62164-446">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="62164-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="62164-447">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="62164-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="62164-448">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="62164-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="62164-449">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="62164-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="62164-450">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="62164-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="62164-451">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="62164-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="62164-452">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="62164-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62164-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="62164-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62164-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62164-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-456">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="62164-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="62164-457">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="62164-457">State of the logical device.</span></span> <span data-ttu-id="62164-458">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="62164-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="62164-459">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62164-460">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="62164-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62164-461">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="62164-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="62164-462">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="62164-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="62164-463">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="62164-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="62164-464">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="62164-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="62164-465">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="62164-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-468">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="62164-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="62164-469">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="62164-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="62164-470">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="62164-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="62164-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62164-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="62164-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62164-473">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="62164-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62164-474">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="62164-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="62164-475">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="62164-475">Name of the scoping system.</span></span>

<span data-ttu-id="62164-476">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="62164-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62164-477">Комментарии</span><span class="sxs-lookup"><span data-stu-id="62164-477">Remarks</span></span>

<span data-ttu-id="62164-478">Класс **Win32 \_ пнпентити** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="62164-478">The **Win32\_PnPEntity** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="62164-479">Примеры</span><span class="sxs-lookup"><span data-stu-id="62164-479">Examples</span></span>

<span data-ttu-id="62164-480">Пример [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell в коллекции TechNet использует для получения списка нерабочего оборудования, использующего инструментарий WMI, в **Win32 \_ пнпентити** .</span><span class="sxs-lookup"><span data-stu-id="62164-480">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_PnPEntity** to retrieve a list of non-working hardware using WMI.</span></span>

<span data-ttu-id="62164-481">Следующий пример кода VBScript подключается к группе удаленных компьютеров в том же домене, создавая массив имен удаленных компьютеров, а затем отображая имена самонастраивающийся устройств — экземпляры Win32 \_ пнпентити — на каждом компьютере.</span><span class="sxs-lookup"><span data-stu-id="62164-481">The following VBScript code example connects to a group of remote computers in the same domain by creating an array of remote computer names and then displaying names of the Plug and Play devices—instances of Win32\_PnPEntity—on each computer.</span></span>


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer& "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="62164-482">Требования</span><span class="sxs-lookup"><span data-stu-id="62164-482">Requirements</span></span>



| <span data-ttu-id="62164-483">Требование</span><span class="sxs-lookup"><span data-stu-id="62164-483">Requirement</span></span> | <span data-ttu-id="62164-484">Значение</span><span class="sxs-lookup"><span data-stu-id="62164-484">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62164-485">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62164-485">Minimum supported client</span></span><br/> | <span data-ttu-id="62164-486">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62164-486">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62164-487">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62164-487">Minimum supported server</span></span><br/> | <span data-ttu-id="62164-488">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62164-488">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62164-489">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="62164-489">Namespace</span></span><br/>                | <span data-ttu-id="62164-490">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="62164-490">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62164-491">MOF</span><span class="sxs-lookup"><span data-stu-id="62164-491">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62164-492"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62164-492"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62164-493">DLL</span><span class="sxs-lookup"><span data-stu-id="62164-493">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62164-494"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62164-494"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62164-495">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62164-495">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62164-496">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="62164-496">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="62164-497">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="62164-497">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="62164-498">Подключение к инструментарию WMI на удаленном компьютере</span><span class="sxs-lookup"><span data-stu-id="62164-498">Connecting to WMI on a Remote Computer</span></span>](../wmisdk/connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="62164-499">Задачи WMI: оборудование компьютера</span><span class="sxs-lookup"><span data-stu-id="62164-499">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
