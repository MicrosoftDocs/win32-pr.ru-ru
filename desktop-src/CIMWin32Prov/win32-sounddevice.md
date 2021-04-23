---
description: Представляет свойства звукового устройства в компьютерной системе под Windows.
ms.assetid: 5471ffe9-60a3-466f-a608-e6268ba73c2b
ms.tgt_platform: multiple
title: Класс Win32_SoundDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SoundDevice
- Win32_SoundDevice.Reset
- Win32_SoundDevice.SetPowerState
- Win32_SoundDevice.Availability
- Win32_SoundDevice.Caption
- Win32_SoundDevice.ConfigManagerErrorCode
- Win32_SoundDevice.ConfigManagerUserConfig
- Win32_SoundDevice.CreationClassName
- Win32_SoundDevice.Description
- Win32_SoundDevice.DeviceID
- Win32_SoundDevice.DMABufferSize
- Win32_SoundDevice.ErrorCleared
- Win32_SoundDevice.ErrorDescription
- Win32_SoundDevice.InstallDate
- Win32_SoundDevice.LastErrorCode
- Win32_SoundDevice.Manufacturer
- Win32_SoundDevice.MPU401Address
- Win32_SoundDevice.Name
- Win32_SoundDevice.PNPDeviceID
- Win32_SoundDevice.PowerManagementCapabilities
- Win32_SoundDevice.PowerManagementSupported
- Win32_SoundDevice.ProductName
- Win32_SoundDevice.Status
- Win32_SoundDevice.StatusInfo
- Win32_SoundDevice.SystemCreationClassName
- Win32_SoundDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73e0ef7cbc71872d26f75311b6d72ac48bbfae8e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142676"
---
# <a name="win32_sounddevice-class"></a><span data-ttu-id="aa318-103">\_Класс Win32 саунддевице</span><span class="sxs-lookup"><span data-stu-id="aa318-103">Win32\_SoundDevice class</span></span>

<span data-ttu-id="aa318-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ саунддевице для Win32** представляет свойства звукового устройства в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="aa318-104">The **Win32\_SoundDevice** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties of a sound device on a computer system running Windows.</span></span>

<span data-ttu-id="aa318-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="aa318-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="aa318-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="aa318-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa318-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa318-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SoundDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  uint16   DMABufferSize;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MPU401Address;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="aa318-108">Члены</span><span class="sxs-lookup"><span data-stu-id="aa318-108">Members</span></span>

<span data-ttu-id="aa318-109">Класс **Win32 \_ саунддевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="aa318-109">The **Win32\_SoundDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="aa318-110">Методы</span><span class="sxs-lookup"><span data-stu-id="aa318-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="aa318-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="aa318-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="aa318-112">Методы</span><span class="sxs-lookup"><span data-stu-id="aa318-112">Methods</span></span>

<span data-ttu-id="aa318-113">Класс **Win32 \_ саунддевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="aa318-113">The **Win32\_SoundDevice** class has these methods.</span></span>



| <span data-ttu-id="aa318-114">Метод</span><span class="sxs-lookup"><span data-stu-id="aa318-114">Method</span></span>            | <span data-ttu-id="aa318-115">Описание</span><span class="sxs-lookup"><span data-stu-id="aa318-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa318-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="aa318-116">**Reset**</span></span>         | <span data-ttu-id="aa318-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="aa318-117">Not implemented.</span></span> <span data-ttu-id="aa318-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="aa318-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="aa318-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="aa318-119">**SetPowerState**</span></span> | <span data-ttu-id="aa318-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="aa318-120">Not implemented.</span></span> <span data-ttu-id="aa318-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="aa318-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="aa318-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="aa318-122">Properties</span></span>

<span data-ttu-id="aa318-123">Класс **Win32 \_ саунддевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="aa318-123">The **Win32\_SoundDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa318-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="aa318-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa318-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="aa318-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-128">Availability and status of the device.</span></span>

<span data-ttu-id="aa318-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa318-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="aa318-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa318-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="aa318-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="aa318-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="aa318-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="aa318-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="aa318-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="aa318-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="aa318-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="aa318-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aa318-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="aa318-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="aa318-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="aa318-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="aa318-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="aa318-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="aa318-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="aa318-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa318-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="aa318-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="aa318-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="aa318-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="aa318-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="aa318-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="aa318-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="aa318-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="aa318-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="aa318-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="aa318-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="aa318-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="aa318-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="aa318-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="aa318-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="aa318-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="aa318-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="aa318-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="aa318-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="aa318-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="aa318-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="aa318-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="aa318-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="aa318-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="aa318-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="aa318-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="aa318-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="aa318-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="aa318-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="aa318-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="aa318-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="aa318-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa318-160">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="aa318-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-163">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="aa318-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-164">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="aa318-164">Short description of the object.</span></span>

<span data-ttu-id="aa318-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa318-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-166">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="aa318-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa318-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-169">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa318-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-170">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="aa318-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="aa318-171">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="aa318-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="aa318-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="aa318-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="aa318-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-174">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="aa318-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="aa318-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="aa318-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="aa318-176">(1)</span><span class="sxs-lookup"><span data-stu-id="aa318-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-177">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="aa318-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa318-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="aa318-179">(2)</span><span class="sxs-lookup"><span data-stu-id="aa318-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="aa318-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="aa318-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="aa318-181">(3)</span><span class="sxs-lookup"><span data-stu-id="aa318-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-182">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa318-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aa318-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="aa318-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="aa318-184">(4)</span><span class="sxs-lookup"><span data-stu-id="aa318-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-185">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="aa318-185">Device is not working properly.</span></span> <span data-ttu-id="aa318-186">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="aa318-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="aa318-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="aa318-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="aa318-188">(5)</span><span class="sxs-lookup"><span data-stu-id="aa318-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-189">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="aa318-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="aa318-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="aa318-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="aa318-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="aa318-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-192">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="aa318-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="aa318-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="aa318-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="aa318-194">(7)</span><span class="sxs-lookup"><span data-stu-id="aa318-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="aa318-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="aa318-196">(8)</span><span class="sxs-lookup"><span data-stu-id="aa318-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-197">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="aa318-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="aa318-199">(9)</span><span class="sxs-lookup"><span data-stu-id="aa318-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-200">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="aa318-200">Device is not working properly.</span></span> <span data-ttu-id="aa318-201">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="aa318-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="aa318-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="aa318-203">(10)</span><span class="sxs-lookup"><span data-stu-id="aa318-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-204">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="aa318-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="aa318-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="aa318-206">(11)</span><span class="sxs-lookup"><span data-stu-id="aa318-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-207">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="aa318-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="aa318-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="aa318-209">(12)</span><span class="sxs-lookup"><span data-stu-id="aa318-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-210">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="aa318-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="aa318-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="aa318-212">(13)</span><span class="sxs-lookup"><span data-stu-id="aa318-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-213">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="aa318-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="aa318-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="aa318-215">(14)</span><span class="sxs-lookup"><span data-stu-id="aa318-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-216">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="aa318-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="aa318-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="aa318-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="aa318-218">(15)</span><span class="sxs-lookup"><span data-stu-id="aa318-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-219">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="aa318-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="aa318-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="aa318-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="aa318-221">(16)</span><span class="sxs-lookup"><span data-stu-id="aa318-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-222">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="aa318-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="aa318-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="aa318-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="aa318-224">(17)</span><span class="sxs-lookup"><span data-stu-id="aa318-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-225">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa318-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa318-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="aa318-227">(18)</span><span class="sxs-lookup"><span data-stu-id="aa318-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-228">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="aa318-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="aa318-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="aa318-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="aa318-230">(19)</span><span class="sxs-lookup"><span data-stu-id="aa318-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="aa318-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="aa318-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="aa318-232">(20)</span><span class="sxs-lookup"><span data-stu-id="aa318-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-233">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="aa318-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="aa318-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="aa318-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="aa318-235">(21)</span><span class="sxs-lookup"><span data-stu-id="aa318-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-236">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="aa318-236">System failure.</span></span> <span data-ttu-id="aa318-237">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="aa318-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="aa318-238">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="aa318-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="aa318-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="aa318-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="aa318-240">(22)</span><span class="sxs-lookup"><span data-stu-id="aa318-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-241">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="aa318-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="aa318-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="aa318-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="aa318-243">(23)</span><span class="sxs-lookup"><span data-stu-id="aa318-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="aa318-244">System failure.</span></span> <span data-ttu-id="aa318-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="aa318-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="aa318-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="aa318-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="aa318-247">(24)</span><span class="sxs-lookup"><span data-stu-id="aa318-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-248">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="aa318-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aa318-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="aa318-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aa318-250">(25)</span><span class="sxs-lookup"><span data-stu-id="aa318-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-251">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="aa318-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="aa318-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="aa318-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="aa318-253">(26)</span><span class="sxs-lookup"><span data-stu-id="aa318-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-254">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="aa318-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="aa318-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="aa318-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="aa318-256">(27)</span><span class="sxs-lookup"><span data-stu-id="aa318-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-257">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="aa318-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="aa318-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="aa318-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="aa318-259">(28)</span><span class="sxs-lookup"><span data-stu-id="aa318-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-260">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="aa318-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="aa318-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="aa318-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="aa318-262">(29)</span><span class="sxs-lookup"><span data-stu-id="aa318-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-263">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="aa318-263">Device is disabled.</span></span> <span data-ttu-id="aa318-264">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="aa318-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="aa318-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="aa318-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="aa318-266">(30)</span><span class="sxs-lookup"><span data-stu-id="aa318-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-267">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="aa318-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="aa318-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="aa318-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="aa318-269">1-31</span><span class="sxs-lookup"><span data-stu-id="aa318-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-270">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="aa318-270">Device is not working properly.</span></span> <span data-ttu-id="aa318-271">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="aa318-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa318-272">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="aa318-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-273">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aa318-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-275">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa318-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-276">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="aa318-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="aa318-277">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="aa318-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-281">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aa318-281">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aa318-282">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="aa318-282">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="aa318-283">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="aa318-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="aa318-284">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-285">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aa318-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-288">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="aa318-288">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-289">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="aa318-289">Description of the object.</span></span>

<span data-ttu-id="aa318-290">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa318-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="aa318-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-294">Квалификаторы: [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**ключ**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ медиаресаурцес \\ \\ Wave \| DeviceID")</span><span class="sxs-lookup"><span data-stu-id="aa318-294">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\control\\\\MediaResources\\\\wave\|DeviceID")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-295">Уникальный идентификатор звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-295">Unique identifier of the sound device.</span></span>

<span data-ttu-id="aa318-296">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-297">**дмабуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="aa318-297">**DMABufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-298">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa318-298">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-300">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("килобайты")</span><span class="sxs-lookup"><span data-stu-id="aa318-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-301">Размер буфера прямого доступа к памяти.</span><span class="sxs-lookup"><span data-stu-id="aa318-301">Size of the Direct Memory Access buffer.</span></span>

<span data-ttu-id="aa318-302">Пример: 4</span><span class="sxs-lookup"><span data-stu-id="aa318-302">Example: 4</span></span>

</dd> <dt>

<span data-ttu-id="aa318-303">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="aa318-303">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-304">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aa318-304">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa318-306">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="aa318-306">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="aa318-307">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-308">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="aa318-308">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa318-311">Строка свободной формы, предоставляя дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="aa318-311">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="aa318-312">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-313">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="aa318-313">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-314">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="aa318-314">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-316">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="aa318-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-317">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="aa318-317">Date and time the object was installed.</span></span> <span data-ttu-id="aa318-318">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="aa318-318">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="aa318-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa318-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-320">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="aa318-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-321">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa318-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa318-323">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="aa318-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="aa318-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-325">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="aa318-325">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-328">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="aa318-328">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-329">Изготовитель звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-329">Manufacturer of the sound device.</span></span>

<span data-ttu-id="aa318-330">Пример: "творческие лаборатории"</span><span class="sxs-lookup"><span data-stu-id="aa318-330">Example: "Creative Labs"</span></span>

</dd> <dt>

<span data-ttu-id="aa318-331">**MPU401Address**</span><span class="sxs-lookup"><span data-stu-id="aa318-331">**MPU401Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-332">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa318-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-333">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-334">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="aa318-334">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-335">Начальный адрес ввода-вывода, назначенный порту MPU-401 звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-335">Starting I/O address assigned to the MPU-401 port of the sound device.</span></span>

<span data-ttu-id="aa318-336">Пример: 300</span><span class="sxs-lookup"><span data-stu-id="aa318-336">Example: 300</span></span>

</dd> <dt>

<span data-ttu-id="aa318-337">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa318-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-340">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="aa318-340">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-341">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="aa318-341">Label by which the object is known.</span></span> <span data-ttu-id="aa318-342">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="aa318-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="aa318-343">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa318-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="aa318-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-347">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="aa318-347">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-348">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-348">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="aa318-349">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="aa318-350">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="aa318-350">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="aa318-351">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="aa318-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-352">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="aa318-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="aa318-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa318-354">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="aa318-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="aa318-355">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-355">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa318-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="aa318-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="aa318-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="aa318-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa318-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="aa318-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa318-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="aa318-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-360">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="aa318-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="aa318-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="aa318-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-362">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="aa318-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="aa318-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="aa318-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-364">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="aa318-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="aa318-365">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="aa318-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="aa318-366">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="aa318-366">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="aa318-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="aa318-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-368">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="aa318-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="aa318-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="aa318-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="aa318-370">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="aa318-370">Timed Power-On Supported</span></span>

<span data-ttu-id="aa318-371">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="aa318-371">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="aa318-372">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="aa318-372">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-373">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="aa318-373">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-374">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa318-375">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="aa318-375">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="aa318-376">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="aa318-376">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="aa318-377">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-378">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="aa318-378">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-381">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32APIные \| структуры мультимедиа \| [**вавеауткапс**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps) \| сзпнаме")</span><span class="sxs-lookup"><span data-stu-id="aa318-381">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Multimedia Structures\|[**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)\|szPname")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-382">Название продукта звукового устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-382">Product name of the sound device.</span></span>

<span data-ttu-id="aa318-383">Пример: "Creative Labs Саундбластер AWE64PNP"</span><span class="sxs-lookup"><span data-stu-id="aa318-383">Example: "Creative Labs SoundBlaster AWE64PNP"</span></span>

</dd> <dt>

<span data-ttu-id="aa318-384">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="aa318-384">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-385">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-387">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="aa318-387">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-388">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="aa318-388">Current status of the object.</span></span> <span data-ttu-id="aa318-389">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="aa318-389">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="aa318-390">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="aa318-390">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="aa318-391">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="aa318-391">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="aa318-392">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="aa318-392">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="aa318-393">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="aa318-393">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="aa318-394">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="aa318-394">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="aa318-395">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="aa318-395">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="aa318-396">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="aa318-396">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="aa318-397">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="aa318-397">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="aa318-398">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="aa318-398">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa318-399">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="aa318-399">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="aa318-400">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="aa318-400">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="aa318-401">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="aa318-401">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="aa318-402">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="aa318-402">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="aa318-403">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="aa318-403">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="aa318-404">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="aa318-404">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="aa318-405">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="aa318-405">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="aa318-406">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="aa318-406">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="aa318-407">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="aa318-407">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa318-408">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="aa318-408">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-409">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="aa318-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-411">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="aa318-411">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="aa318-412">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="aa318-412">State of the logical device.</span></span> <span data-ttu-id="aa318-413">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="aa318-413">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="aa318-414">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="aa318-415">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="aa318-415">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="aa318-416">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="aa318-416">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="aa318-417">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="aa318-417">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="aa318-418">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="aa318-418">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="aa318-419">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="aa318-419">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="aa318-420">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="aa318-420">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-423">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aa318-423">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aa318-424">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="aa318-424">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="aa318-425">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa318-426">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="aa318-426">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa318-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="aa318-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aa318-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="aa318-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa318-429">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="aa318-429">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="aa318-430">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="aa318-430">Name of the scoping system.</span></span>

<span data-ttu-id="aa318-431">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="aa318-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa318-432">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aa318-432">Remarks</span></span>

<span data-ttu-id="aa318-433">Класс **Win32 \_ саунддевице** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="aa318-433">The **Win32\_SoundDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="aa318-434">Примеры</span><span class="sxs-lookup"><span data-stu-id="aa318-434">Examples</span></span>

<span data-ttu-id="aa318-435">Образец PowerShell " [Свойства звуковой карты](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) " извлекает сведения обо всех звуковых картах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="aa318-435">The [List Sound Card Properties](https://Gallery.TechNet.Microsoft.Com/scriptcenter/86550b1a-bb3f-47c3-8056-bbd57e508b7a) PowerShell sample retrieves information about all the sound cards installed in a computer.</span></span>

<span data-ttu-id="aa318-436">Следующий пример сценария VBScript извлекает сведения обо всех звуковых картах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="aa318-436">The following VBScript sample retrieves information about all the sound cards installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SoundDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "DMA Buffer Size: " & objItem.DMABufferSize 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "MPU 401 Address: " & objItem.MPU401Address 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Product Name: " & objItem.ProductName 
    Wscript.Echo "Status Information: " & objItem.StatusInfo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="aa318-437">Требования</span><span class="sxs-lookup"><span data-stu-id="aa318-437">Requirements</span></span>



| <span data-ttu-id="aa318-438">Требование</span><span class="sxs-lookup"><span data-stu-id="aa318-438">Requirement</span></span> | <span data-ttu-id="aa318-439">Значение</span><span class="sxs-lookup"><span data-stu-id="aa318-439">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa318-440">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa318-440">Minimum supported client</span></span><br/> | <span data-ttu-id="aa318-441">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa318-441">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa318-442">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa318-442">Minimum supported server</span></span><br/> | <span data-ttu-id="aa318-443">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa318-443">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa318-444">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aa318-444">Namespace</span></span><br/>                | <span data-ttu-id="aa318-445">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="aa318-445">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa318-446">MOF</span><span class="sxs-lookup"><span data-stu-id="aa318-446">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa318-447"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa318-447"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa318-448">DLL</span><span class="sxs-lookup"><span data-stu-id="aa318-448">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa318-449"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa318-449"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa318-450">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa318-450">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa318-451">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="aa318-451">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="aa318-452">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="aa318-452">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
