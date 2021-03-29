---
description: '\_Класс WMI мосербоарддевице для Win32 представляет устройство, которое содержит центральные компоненты компьютерной системы Windows.'
ms.assetid: 2aed5fff-e994-4ce1-8a2e-aadb01adf28d
ms.tgt_platform: multiple
title: Класс Win32_MotherboardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MotherboardDevice
- Win32_MotherboardDevice.Reset
- Win32_MotherboardDevice.SetPowerState
- Win32_MotherboardDevice.Availability
- Win32_MotherboardDevice.Caption
- Win32_MotherboardDevice.ConfigManagerErrorCode
- Win32_MotherboardDevice.ConfigManagerUserConfig
- Win32_MotherboardDevice.CreationClassName
- Win32_MotherboardDevice.Description
- Win32_MotherboardDevice.DeviceID
- Win32_MotherboardDevice.ErrorCleared
- Win32_MotherboardDevice.ErrorDescription
- Win32_MotherboardDevice.InstallDate
- Win32_MotherboardDevice.LastErrorCode
- Win32_MotherboardDevice.Name
- Win32_MotherboardDevice.PNPDeviceID
- Win32_MotherboardDevice.PowerManagementCapabilities
- Win32_MotherboardDevice.PowerManagementSupported
- Win32_MotherboardDevice.PrimaryBusType
- Win32_MotherboardDevice.RevisionNumber
- Win32_MotherboardDevice.SecondaryBusType
- Win32_MotherboardDevice.Status
- Win32_MotherboardDevice.StatusInfo
- Win32_MotherboardDevice.SystemCreationClassName
- Win32_MotherboardDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6df116d1e4bc4e87d7201deb33f57bc8e91320e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807841"
---
# <a name="win32_motherboarddevice-class"></a><span data-ttu-id="07d37-103">\_Класс Win32 мосербоарддевице</span><span class="sxs-lookup"><span data-stu-id="07d37-103">Win32\_MotherboardDevice class</span></span>

<span data-ttu-id="07d37-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ мосербоарддевице для Win32** представляет устройство, которое содержит центральные компоненты компьютерной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="07d37-104">The **Win32\_MotherboardDevice** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device that contains the central components of the Windows computer system.</span></span>

<span data-ttu-id="07d37-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="07d37-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="07d37-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="07d37-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d37-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07d37-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_MotherboardDevice : CIM_LogicalDevice
{
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
  string   PrimaryBusType;
  string   RevisionNumber;
  string   SecondaryBusType;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="07d37-108">Члены</span><span class="sxs-lookup"><span data-stu-id="07d37-108">Members</span></span>

<span data-ttu-id="07d37-109">Класс **Win32 \_ мосербоарддевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="07d37-109">The **Win32\_MotherboardDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="07d37-110">Методы</span><span class="sxs-lookup"><span data-stu-id="07d37-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="07d37-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="07d37-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="07d37-112">Методы</span><span class="sxs-lookup"><span data-stu-id="07d37-112">Methods</span></span>

<span data-ttu-id="07d37-113">Класс **Win32 \_ мосербоарддевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="07d37-113">The **Win32\_MotherboardDevice** class has these methods.</span></span>



| <span data-ttu-id="07d37-114">Метод</span><span class="sxs-lookup"><span data-stu-id="07d37-114">Method</span></span>            | <span data-ttu-id="07d37-115">Описание</span><span class="sxs-lookup"><span data-stu-id="07d37-115">Description</span></span>                                                                                                                                                                                    |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d37-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="07d37-116">**Reset**</span></span>         | <span data-ttu-id="07d37-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="07d37-117">Not implemented.</span></span> <span data-ttu-id="07d37-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="07d37-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/>                 |
| <span data-ttu-id="07d37-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="07d37-119">**SetPowerState**</span></span> | <span data-ttu-id="07d37-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="07d37-120">Not implemented.</span></span> <span data-ttu-id="07d37-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="07d37-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="07d37-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="07d37-122">Properties</span></span>

<span data-ttu-id="07d37-123">Класс **Win32 \_ мосербоарддевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="07d37-123">The **Win32\_MotherboardDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07d37-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="07d37-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07d37-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-127">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="07d37-127">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-128">Availability and status of the device.</span></span>

<span data-ttu-id="07d37-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07d37-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="07d37-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07d37-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="07d37-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="07d37-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="07d37-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="07d37-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="07d37-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="07d37-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="07d37-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="07d37-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="07d37-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="07d37-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="07d37-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="07d37-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="07d37-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="07d37-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="07d37-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="07d37-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07d37-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="07d37-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="07d37-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="07d37-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="07d37-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="07d37-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="07d37-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="07d37-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="07d37-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="07d37-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="07d37-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="07d37-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="07d37-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="07d37-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="07d37-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="07d37-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="07d37-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="07d37-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="07d37-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="07d37-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="07d37-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="07d37-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="07d37-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="07d37-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="07d37-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="07d37-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="07d37-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="07d37-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="07d37-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="07d37-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="07d37-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="07d37-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07d37-160">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="07d37-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-163">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="07d37-163">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-164">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="07d37-164">Short description of the object a one-line string.</span></span>

<span data-ttu-id="07d37-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07d37-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-166">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="07d37-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07d37-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-169">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07d37-169">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-170">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="07d37-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="07d37-171">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="07d37-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="07d37-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="07d37-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="07d37-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-174">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="07d37-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="07d37-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="07d37-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="07d37-176">(1)</span><span class="sxs-lookup"><span data-stu-id="07d37-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-177">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="07d37-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07d37-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="07d37-179">(2)</span><span class="sxs-lookup"><span data-stu-id="07d37-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="07d37-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="07d37-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="07d37-181">(3)</span><span class="sxs-lookup"><span data-stu-id="07d37-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-182">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07d37-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="07d37-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="07d37-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="07d37-184">(4)</span><span class="sxs-lookup"><span data-stu-id="07d37-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-185">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="07d37-185">Device is not working properly.</span></span> <span data-ttu-id="07d37-186">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="07d37-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="07d37-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="07d37-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="07d37-188">(5)</span><span class="sxs-lookup"><span data-stu-id="07d37-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-189">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="07d37-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="07d37-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="07d37-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="07d37-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="07d37-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-192">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="07d37-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="07d37-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="07d37-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="07d37-194">(7)</span><span class="sxs-lookup"><span data-stu-id="07d37-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="07d37-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="07d37-196">(8)</span><span class="sxs-lookup"><span data-stu-id="07d37-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-197">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="07d37-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="07d37-199">(9)</span><span class="sxs-lookup"><span data-stu-id="07d37-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-200">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="07d37-200">Device is not working properly.</span></span> <span data-ttu-id="07d37-201">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="07d37-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="07d37-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="07d37-203">(10)</span><span class="sxs-lookup"><span data-stu-id="07d37-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-204">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="07d37-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="07d37-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="07d37-206">(11)</span><span class="sxs-lookup"><span data-stu-id="07d37-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-207">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="07d37-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="07d37-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="07d37-209">(12)</span><span class="sxs-lookup"><span data-stu-id="07d37-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-210">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="07d37-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="07d37-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="07d37-212">(13)</span><span class="sxs-lookup"><span data-stu-id="07d37-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-213">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="07d37-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="07d37-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="07d37-215">(14)</span><span class="sxs-lookup"><span data-stu-id="07d37-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-216">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="07d37-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="07d37-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="07d37-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="07d37-218">(15)</span><span class="sxs-lookup"><span data-stu-id="07d37-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-219">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="07d37-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="07d37-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="07d37-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="07d37-221">(16)</span><span class="sxs-lookup"><span data-stu-id="07d37-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-222">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="07d37-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="07d37-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="07d37-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="07d37-224">(17)</span><span class="sxs-lookup"><span data-stu-id="07d37-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-225">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="07d37-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07d37-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="07d37-227">(18)</span><span class="sxs-lookup"><span data-stu-id="07d37-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-228">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="07d37-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="07d37-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="07d37-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="07d37-230">(19)</span><span class="sxs-lookup"><span data-stu-id="07d37-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="07d37-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="07d37-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="07d37-232">(20)</span><span class="sxs-lookup"><span data-stu-id="07d37-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-233">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="07d37-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="07d37-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="07d37-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="07d37-235">(21)</span><span class="sxs-lookup"><span data-stu-id="07d37-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-236">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="07d37-236">System failure.</span></span> <span data-ttu-id="07d37-237">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="07d37-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="07d37-238">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="07d37-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="07d37-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="07d37-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="07d37-240">(22)</span><span class="sxs-lookup"><span data-stu-id="07d37-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-241">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="07d37-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="07d37-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="07d37-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="07d37-243">(23)</span><span class="sxs-lookup"><span data-stu-id="07d37-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="07d37-244">System failure.</span></span> <span data-ttu-id="07d37-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="07d37-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="07d37-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="07d37-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="07d37-247">(24)</span><span class="sxs-lookup"><span data-stu-id="07d37-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-248">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="07d37-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="07d37-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="07d37-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="07d37-250">(25)</span><span class="sxs-lookup"><span data-stu-id="07d37-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-251">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="07d37-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="07d37-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="07d37-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="07d37-253">(26)</span><span class="sxs-lookup"><span data-stu-id="07d37-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-254">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="07d37-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="07d37-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="07d37-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="07d37-256">(27)</span><span class="sxs-lookup"><span data-stu-id="07d37-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-257">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="07d37-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="07d37-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="07d37-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="07d37-259">(28)</span><span class="sxs-lookup"><span data-stu-id="07d37-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-260">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="07d37-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="07d37-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="07d37-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="07d37-262">(29)</span><span class="sxs-lookup"><span data-stu-id="07d37-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-263">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="07d37-263">Device is disabled.</span></span> <span data-ttu-id="07d37-264">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="07d37-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="07d37-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="07d37-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="07d37-266">(30)</span><span class="sxs-lookup"><span data-stu-id="07d37-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-267">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="07d37-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="07d37-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="07d37-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="07d37-269">1-31</span><span class="sxs-lookup"><span data-stu-id="07d37-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-270">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="07d37-270">Device is not working properly.</span></span> <span data-ttu-id="07d37-271">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="07d37-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07d37-272">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="07d37-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-273">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="07d37-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-275">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07d37-275">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-276">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="07d37-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="07d37-277">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-278">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="07d37-278">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-279">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-281">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="07d37-281">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="07d37-282">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07d37-282">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="07d37-283">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="07d37-283">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="07d37-284">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-285">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07d37-285">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-286">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-288">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="07d37-288">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-289">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="07d37-289">Description of the object.</span></span>

<span data-ttu-id="07d37-290">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07d37-290">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-291">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="07d37-291">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-292">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-294">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="07d37-294">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-295">Уникальный идентификатор этой материнской платы.</span><span class="sxs-lookup"><span data-stu-id="07d37-295">Unique identifier of this motherboard.</span></span>

<span data-ttu-id="07d37-296">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-297">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="07d37-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-298">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="07d37-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07d37-300">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="07d37-300">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="07d37-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="07d37-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07d37-305">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="07d37-305">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="07d37-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-307">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="07d37-307">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-308">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="07d37-308">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-310">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="07d37-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-311">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="07d37-311">Date and time the object was installed.</span></span> <span data-ttu-id="07d37-312">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="07d37-312">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="07d37-313">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07d37-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-314">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="07d37-314">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-315">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07d37-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07d37-317">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="07d37-317">Last error code reported by the logical device.</span></span>

<span data-ttu-id="07d37-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-319">**Name**</span><span class="sxs-lookup"><span data-stu-id="07d37-319">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-322">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="07d37-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-323">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="07d37-323">Label by which the object is known.</span></span> <span data-ttu-id="07d37-324">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="07d37-324">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="07d37-325">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07d37-325">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-326">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="07d37-326">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-327">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-329">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="07d37-329">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-330">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-330">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="07d37-331">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="07d37-332">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="07d37-332">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="07d37-333">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="07d37-333">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-334">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="07d37-334">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="07d37-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07d37-336">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="07d37-336">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="07d37-337">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-337">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07d37-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="07d37-338"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="07d37-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="07d37-339"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="07d37-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="07d37-340"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="07d37-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="07d37-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-342">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="07d37-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="07d37-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="07d37-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-344">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="07d37-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="07d37-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="07d37-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-346">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="07d37-346">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="07d37-347">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="07d37-347">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="07d37-348">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="07d37-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="07d37-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="07d37-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-350">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="07d37-350">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="07d37-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="07d37-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="07d37-352">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="07d37-352">Timed Power-On Supported</span></span>

<span data-ttu-id="07d37-353">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="07d37-353">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="07d37-354">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="07d37-354">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-355">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="07d37-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07d37-357">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="07d37-357">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="07d37-358">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="07d37-358">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="07d37-359">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-360">**примарибустипе**</span><span class="sxs-lookup"><span data-stu-id="07d37-360">**PrimaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-363">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ \\ \\ Описание оборудования \\ \\ System \\ \\ мултифунктионадаптер \| идентификатор")</span><span class="sxs-lookup"><span data-stu-id="07d37-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-364">Тип основной Шины материнской платы.</span><span class="sxs-lookup"><span data-stu-id="07d37-364">Primary bus type of the motherboard.</span></span>

<span data-ttu-id="07d37-365">Пример: PCI</span><span class="sxs-lookup"><span data-stu-id="07d37-365">Example: "PCI"</span></span>

</dd> <dt>

<span data-ttu-id="07d37-366">**RevisionNumber**</span><span class="sxs-lookup"><span data-stu-id="07d37-366">**RevisionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-369">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ \\ \\ Description \\ \\ System описания системы")</span><span class="sxs-lookup"><span data-stu-id="07d37-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-370">Номер редакции материнской платы.</span><span class="sxs-lookup"><span data-stu-id="07d37-370">Revision number of the motherboard.</span></span>

<span data-ttu-id="07d37-371">Пример: "00"</span><span class="sxs-lookup"><span data-stu-id="07d37-371">Example: "00"</span></span>

</dd> <dt>

<span data-ttu-id="07d37-372">**секондарибустипе**</span><span class="sxs-lookup"><span data-stu-id="07d37-372">**SecondaryBusType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-375">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ локальный \_ компьютер \\ \\ \\ \\ Описание оборудования \\ \\ System \\ \\ мултифунктионадаптер \| идентификатор")</span><span class="sxs-lookup"><span data-stu-id="07d37-375">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\HARDWARE\\\\DESCRIPTION\\\\System\\\\MultifunctionAdapter\|Identifier")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-376">Тип дополнительной шины материнской платы.</span><span class="sxs-lookup"><span data-stu-id="07d37-376">Secondary bus type of the motherboard.</span></span>

<span data-ttu-id="07d37-377">Пример: "ISA"</span><span class="sxs-lookup"><span data-stu-id="07d37-377">Example: "ISA"</span></span>

</dd> <dt>

<span data-ttu-id="07d37-378">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="07d37-378">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-381">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="07d37-381">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-382">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="07d37-382">Current status of the object.</span></span> <span data-ttu-id="07d37-383">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="07d37-383">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="07d37-384">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="07d37-384">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="07d37-385">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="07d37-385">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="07d37-386">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="07d37-386">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="07d37-387">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="07d37-387">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="07d37-388">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="07d37-388">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="07d37-389">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="07d37-389">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="07d37-390">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="07d37-390">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="07d37-391">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="07d37-391">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="07d37-392">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="07d37-392">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07d37-393">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="07d37-393">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="07d37-394">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="07d37-394">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="07d37-395">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="07d37-395">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="07d37-396">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="07d37-396">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="07d37-397">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="07d37-397">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="07d37-398">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="07d37-398">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="07d37-399">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="07d37-399">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="07d37-400">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="07d37-400">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="07d37-401">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="07d37-401">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07d37-402">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="07d37-402">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-403">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="07d37-403">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-405">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="07d37-405">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="07d37-406">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="07d37-406">State of the logical device.</span></span> <span data-ttu-id="07d37-407">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="07d37-407">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="07d37-408">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="07d37-409">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="07d37-409">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="07d37-410">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="07d37-410">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="07d37-411">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="07d37-411">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="07d37-412">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="07d37-412">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="07d37-413">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="07d37-413">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="07d37-414">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="07d37-414">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-417">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="07d37-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="07d37-418">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="07d37-418">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="07d37-419">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="07d37-420">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="07d37-420">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07d37-421">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="07d37-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07d37-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="07d37-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07d37-423">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="07d37-423">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="07d37-424">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="07d37-424">Name of the scoping system.</span></span>

<span data-ttu-id="07d37-425">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="07d37-425">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07d37-426">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07d37-426">Remarks</span></span>

<span data-ttu-id="07d37-427">Класс **Win32 \_ мосербоарддевице** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="07d37-427">The **Win32\_MotherboardDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="07d37-428">Примеры</span><span class="sxs-lookup"><span data-stu-id="07d37-428">Examples</span></span>

<span data-ttu-id="07d37-429">В следующих примерах кода [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) и [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) извлекается информация о материнской плате.</span><span class="sxs-lookup"><span data-stu-id="07d37-429">The following [JavaScript](https://Gallery.TechNet.Microsoft.Com/05bbadf8-1356-43a6-82fc-fcab40233fe5) and [PowerShell](https://Gallery.TechNet.Microsoft.Com/cb520044-836e-425c-8c12-a9586d1c0e6e) code samples retrieve motherboard information.</span></span>

<span data-ttu-id="07d37-430">В следующем примере кода VBScript извлекаются сведения о материнской плате.</span><span class="sxs-lookup"><span data-stu-id="07d37-430">The following VBScript code sample retrieves motherboard information.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_MotherboardDevice") 
 
For Each objItem in colItems 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Primary Bus Type: " & objItem.PrimaryBusType 
    Wscript.Echo "Secondary Bus Type: " & objItem.SecondaryBusType 
    Wscript.Echo 
Next 
```



## <a name="requirements"></a><span data-ttu-id="07d37-431">Требования</span><span class="sxs-lookup"><span data-stu-id="07d37-431">Requirements</span></span>



| <span data-ttu-id="07d37-432">Требование</span><span class="sxs-lookup"><span data-stu-id="07d37-432">Requirement</span></span> | <span data-ttu-id="07d37-433">Значение</span><span class="sxs-lookup"><span data-stu-id="07d37-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07d37-434">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07d37-434">Minimum supported client</span></span><br/> | <span data-ttu-id="07d37-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07d37-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07d37-436">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07d37-436">Minimum supported server</span></span><br/> | <span data-ttu-id="07d37-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07d37-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07d37-438">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="07d37-438">Namespace</span></span><br/>                | <span data-ttu-id="07d37-439">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07d37-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07d37-440">MOF</span><span class="sxs-lookup"><span data-stu-id="07d37-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07d37-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07d37-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07d37-442">DLL</span><span class="sxs-lookup"><span data-stu-id="07d37-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d37-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d37-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d37-444">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07d37-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d37-445">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="07d37-445">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="07d37-446">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="07d37-446">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

