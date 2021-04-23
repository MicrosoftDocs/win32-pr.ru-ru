---
description: '\_Класс WMI сксиконтроллер для Win32 представляет контроллер SCSI в компьютерной системе под Windows.'
ms.assetid: 14ed523e-d505-40fa-81d5-3a71eb9f078e
ms.tgt_platform: multiple
title: Класс Win32_SCSIController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIController
- Win32_SCSIController.Reset
- Win32_SCSIController.SetPowerState
- Win32_SCSIController.Availability
- Win32_SCSIController.Caption
- Win32_SCSIController.ConfigManagerErrorCode
- Win32_SCSIController.ConfigManagerUserConfig
- Win32_SCSIController.ControllerTimeouts
- Win32_SCSIController.CreationClassName
- Win32_SCSIController.Description
- Win32_SCSIController.DeviceID
- Win32_SCSIController.DeviceMap
- Win32_SCSIController.DriverName
- Win32_SCSIController.ErrorCleared
- Win32_SCSIController.ErrorDescription
- Win32_SCSIController.HardwareVersion
- Win32_SCSIController.Index
- Win32_SCSIController.InstallDate
- Win32_SCSIController.LastErrorCode
- Win32_SCSIController.Manufacturer
- Win32_SCSIController.MaxDataWidth
- Win32_SCSIController.MaxNumberControlled
- Win32_SCSIController.MaxTransferRate
- Win32_SCSIController.Name
- Win32_SCSIController.PNPDeviceID
- Win32_SCSIController.PowerManagementCapabilities
- Win32_SCSIController.PowerManagementSupported
- Win32_SCSIController.ProtectionManagement
- Win32_SCSIController.ProtocolSupported
- Win32_SCSIController.Status
- Win32_SCSIController.StatusInfo
- Win32_SCSIController.SystemCreationClassName
- Win32_SCSIController.SystemName
- Win32_SCSIController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f8ba77d626ada787ed18fd9855333fa813f3ab7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656053"
---
# <a name="win32_scsicontroller-class"></a><span data-ttu-id="71516-103">\_Класс Win32 сксиконтроллер</span><span class="sxs-lookup"><span data-stu-id="71516-103">Win32\_SCSIController class</span></span>

<span data-ttu-id="71516-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ сксиконтроллер для Win32** представляет контроллер SCSI в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="71516-104">The **Win32\_SCSIController** [WMI class](../wmisdk/retrieving-a-class.md) represents a SCSI controller on a computer system running Windows.</span></span>

<span data-ttu-id="71516-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="71516-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="71516-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="71516-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="71516-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71516-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SCSIController : CIM_SCSIController
{
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  uint32   ControllerTimeouts;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  string   DeviceMap;
  string   DriverName;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   HardwareVersion;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Manufacturer;
  uint32   MaxDataWidth;
  uint32   MaxNumberControlled;
  uint64   MaxTransferRate;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtectionManagement;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="71516-108">Члены</span><span class="sxs-lookup"><span data-stu-id="71516-108">Members</span></span>

<span data-ttu-id="71516-109">Класс **Win32 \_ сксиконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="71516-109">The **Win32\_SCSIController** class has these types of members:</span></span>

-   [<span data-ttu-id="71516-110">Методы</span><span class="sxs-lookup"><span data-stu-id="71516-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="71516-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="71516-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="71516-112">Методы</span><span class="sxs-lookup"><span data-stu-id="71516-112">Methods</span></span>

<span data-ttu-id="71516-113">Класс **Win32 \_ сксиконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="71516-113">The **Win32\_SCSIController** class has these methods.</span></span>



| <span data-ttu-id="71516-114">Метод</span><span class="sxs-lookup"><span data-stu-id="71516-114">Method</span></span>            | <span data-ttu-id="71516-115">Описание</span><span class="sxs-lookup"><span data-stu-id="71516-115">Description</span></span>                                                                                                                                                                                      |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71516-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="71516-116">**Reset**</span></span>         | <span data-ttu-id="71516-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="71516-117">Not implemented.</span></span> <span data-ttu-id="71516-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/>                 |
| <span data-ttu-id="71516-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="71516-119">**SetPowerState**</span></span> | <span data-ttu-id="71516-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="71516-120">Not implemented.</span></span> <span data-ttu-id="71516-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="71516-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="71516-122">Properties</span></span>

<span data-ttu-id="71516-123">Класс **Win32 \_ сксиконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="71516-123">The **Win32\_SCSIController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="71516-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="71516-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71516-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71516-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="71516-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="71516-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-128">Availability and status of the device.</span></span>

<span data-ttu-id="71516-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71516-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71516-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71516-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="71516-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="71516-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="71516-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="71516-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="71516-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="71516-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="71516-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="71516-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="71516-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="71516-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="71516-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="71516-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="71516-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="71516-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="71516-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="71516-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="71516-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71516-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="71516-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="71516-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="71516-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="71516-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="71516-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="71516-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="71516-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="71516-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="71516-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="71516-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="71516-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="71516-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="71516-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="71516-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="71516-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="71516-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="71516-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="71516-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="71516-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="71516-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="71516-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="71516-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="71516-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="71516-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="71516-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="71516-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="71516-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="71516-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="71516-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="71516-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="71516-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="71516-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="71516-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="71516-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="71516-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="71516-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="71516-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="71516-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="71516-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-160">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="71516-160">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-163">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="71516-163">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="71516-164">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="71516-164">Short description of the object.</span></span>

<span data-ttu-id="71516-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71516-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-166">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="71516-166">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-167">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71516-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71516-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-169">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="71516-169">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="71516-170">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="71516-170">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="71516-171">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-171">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="71516-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="71516-172"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="71516-173"> (0)</span><span class="sxs-lookup"><span data-stu-id="71516-173">(0)</span></span>


</dt> <dd>

<span data-ttu-id="71516-174">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="71516-174">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="71516-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="71516-175"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="71516-176">(1)</span><span class="sxs-lookup"><span data-stu-id="71516-176">(1)</span></span>


</dt> <dd>

<span data-ttu-id="71516-177">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="71516-177">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="71516-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-178"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="71516-179">(2)</span><span class="sxs-lookup"><span data-stu-id="71516-179">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="71516-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="71516-180"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="71516-181">(3)</span><span class="sxs-lookup"><span data-stu-id="71516-181">(3)</span></span>


</dt> <dd>

<span data-ttu-id="71516-182">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71516-182">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="71516-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="71516-183"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="71516-184">(4)</span><span class="sxs-lookup"><span data-stu-id="71516-184">(4)</span></span>


</dt> <dd>

<span data-ttu-id="71516-185">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="71516-185">Device is not working properly.</span></span> <span data-ttu-id="71516-186">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="71516-186">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="71516-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="71516-187"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="71516-188">(5)</span><span class="sxs-lookup"><span data-stu-id="71516-188">(5)</span></span>


</dt> <dd>

<span data-ttu-id="71516-189">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="71516-189">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="71516-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="71516-190"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="71516-191"> (6)</span><span class="sxs-lookup"><span data-stu-id="71516-191">(6)</span></span>


</dt> <dd>

<span data-ttu-id="71516-192">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="71516-192">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="71516-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="71516-193"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="71516-194">(7)</span><span class="sxs-lookup"><span data-stu-id="71516-194">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="71516-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-195"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="71516-196">(8)</span><span class="sxs-lookup"><span data-stu-id="71516-196">(8)</span></span>


</dt> <dd>

<span data-ttu-id="71516-197">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-197">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="71516-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-198"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="71516-199">(9)</span><span class="sxs-lookup"><span data-stu-id="71516-199">(9)</span></span>


</dt> <dd>

<span data-ttu-id="71516-200">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="71516-200">Device is not working properly.</span></span> <span data-ttu-id="71516-201">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-201">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="71516-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="71516-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="71516-203">(10)</span><span class="sxs-lookup"><span data-stu-id="71516-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="71516-204">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="71516-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="71516-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="71516-206">(11)</span><span class="sxs-lookup"><span data-stu-id="71516-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="71516-207">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="71516-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="71516-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="71516-209">(12)</span><span class="sxs-lookup"><span data-stu-id="71516-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="71516-210">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="71516-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="71516-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="71516-212">(13)</span><span class="sxs-lookup"><span data-stu-id="71516-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="71516-213">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="71516-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="71516-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="71516-215">(14)</span><span class="sxs-lookup"><span data-stu-id="71516-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="71516-216">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="71516-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="71516-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="71516-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="71516-218">(15)</span><span class="sxs-lookup"><span data-stu-id="71516-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="71516-219">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="71516-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="71516-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="71516-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="71516-221">(16)</span><span class="sxs-lookup"><span data-stu-id="71516-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="71516-222">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="71516-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="71516-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="71516-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="71516-224">(17)</span><span class="sxs-lookup"><span data-stu-id="71516-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="71516-225">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="71516-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="71516-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="71516-227">(18)</span><span class="sxs-lookup"><span data-stu-id="71516-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="71516-228">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="71516-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="71516-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="71516-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="71516-230">(19)</span><span class="sxs-lookup"><span data-stu-id="71516-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="71516-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="71516-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="71516-232">(20)</span><span class="sxs-lookup"><span data-stu-id="71516-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="71516-233">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="71516-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="71516-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="71516-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="71516-235">(21)</span><span class="sxs-lookup"><span data-stu-id="71516-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="71516-236">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="71516-236">System failure.</span></span> <span data-ttu-id="71516-237">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="71516-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="71516-238">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="71516-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="71516-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="71516-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="71516-240">(22)</span><span class="sxs-lookup"><span data-stu-id="71516-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="71516-241">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="71516-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="71516-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="71516-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="71516-243">(23)</span><span class="sxs-lookup"><span data-stu-id="71516-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="71516-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="71516-244">System failure.</span></span> <span data-ttu-id="71516-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="71516-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="71516-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="71516-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="71516-247">(24)</span><span class="sxs-lookup"><span data-stu-id="71516-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="71516-248">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="71516-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="71516-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="71516-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="71516-250">(25)</span><span class="sxs-lookup"><span data-stu-id="71516-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="71516-251">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="71516-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="71516-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="71516-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="71516-253">(26)</span><span class="sxs-lookup"><span data-stu-id="71516-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="71516-254">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="71516-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="71516-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="71516-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="71516-256">(27)</span><span class="sxs-lookup"><span data-stu-id="71516-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="71516-257">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="71516-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="71516-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="71516-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="71516-259">(28)</span><span class="sxs-lookup"><span data-stu-id="71516-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="71516-260">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="71516-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="71516-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="71516-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="71516-262">(29)</span><span class="sxs-lookup"><span data-stu-id="71516-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="71516-263">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="71516-263">Device is disabled.</span></span> <span data-ttu-id="71516-264">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="71516-264">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="71516-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="71516-265"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="71516-266">(30)</span><span class="sxs-lookup"><span data-stu-id="71516-266">(30)</span></span>


</dt> <dd>

<span data-ttu-id="71516-267">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="71516-267">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="71516-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="71516-268"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="71516-269">1-31</span><span class="sxs-lookup"><span data-stu-id="71516-269">(31)</span></span>


</dt> <dd>

<span data-ttu-id="71516-270">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="71516-270">Device is not working properly.</span></span> <span data-ttu-id="71516-271">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="71516-271">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-272">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="71516-272">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-273">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71516-273">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71516-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-275">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="71516-275">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="71516-276">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="71516-276">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="71516-277">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-277">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-278">**контроллертимеаутс**</span><span class="sxs-lookup"><span data-stu-id="71516-278">**ControllerTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-279">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71516-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71516-280">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-281">Число тайм-аутов, произошедших после значения **тимеофластресет** .</span><span class="sxs-lookup"><span data-stu-id="71516-281">Number of time-outs that have occurred after the **TimeOfLastReset** value.</span></span>

<span data-ttu-id="71516-282">Это свойство наследуется от [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-282">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="71516-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-286">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="71516-286">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="71516-287">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71516-287">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="71516-288">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="71516-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="71516-289">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-290">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71516-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-293">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="71516-293">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="71516-294">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="71516-294">Description of the object.</span></span>

<span data-ttu-id="71516-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71516-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="71516-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-299">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ девицемап \\ \\ SCSI")</span><span class="sxs-lookup"><span data-stu-id="71516-299">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi")</span></span>
</dt> </dl>

<span data-ttu-id="71516-300">Уникальный идентификатор контроллера SCSI с другими устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="71516-300">Unique identifier of the SCSI controller with other devices on the system.</span></span>

<span data-ttu-id="71516-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-302">**девицемап**</span><span class="sxs-lookup"><span data-stu-id="71516-302">**DeviceMap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-305">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ девицемап \\ \\ SCSI \| ")</span><span class="sxs-lookup"><span data-stu-id="71516-305">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="71516-306">Порядок, в котором устройства перечислены с помощью этого контроллера SCSI.</span><span class="sxs-lookup"><span data-stu-id="71516-306">Order in which the devices are listed with this SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="71516-307">**Имя_драйвера**</span><span class="sxs-lookup"><span data-stu-id="71516-307">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-310">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ \| портдривер")</span><span class="sxs-lookup"><span data-stu-id="71516-310">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Services\\\\Class\|PortDriver")</span></span>
</dt> </dl>

<span data-ttu-id="71516-311">Имя файла драйвера контроллера SCSI.</span><span class="sxs-lookup"><span data-stu-id="71516-311">Driver file name of the SCSI controller.</span></span>

<span data-ttu-id="71516-312">Пример: Adaptec</span><span class="sxs-lookup"><span data-stu-id="71516-312">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="71516-313">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="71516-313">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-314">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71516-314">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71516-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-315">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-316">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="71516-316">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="71516-317">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-318">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="71516-318">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-321">Строка свободной формы, предоставляя дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="71516-321">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="71516-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-323">**HardwareVersion**</span><span class="sxs-lookup"><span data-stu-id="71516-323">**HardwareVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-326">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Enum \\ \\ root \| хвревисион")</span><span class="sxs-lookup"><span data-stu-id="71516-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|HWRevision")</span></span>
</dt> </dl>

<span data-ttu-id="71516-327">Номер версии оборудования контроллера SCSI.</span><span class="sxs-lookup"><span data-stu-id="71516-327">Hardware version number of the SCSI controller.</span></span>

<span data-ttu-id="71516-328">Пример: "1,25"</span><span class="sxs-lookup"><span data-stu-id="71516-328">Example: "1.25"</span></span>

</dd> <dt>

<span data-ttu-id="71516-329">**Index**</span><span class="sxs-lookup"><span data-stu-id="71516-329">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-330">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71516-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71516-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-332">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ девицемап \\ \\ SCSI \| ")</span><span class="sxs-lookup"><span data-stu-id="71516-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\Scsi\|ScsiPort")</span></span>
</dt> </dl>

<span data-ttu-id="71516-333">Номер индекса контроллера SCSI в системном реестре.</span><span class="sxs-lookup"><span data-stu-id="71516-333">Index number of the SCSI controller in the system registry.</span></span>

<span data-ttu-id="71516-334">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="71516-334">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="71516-335">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="71516-335">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-336">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71516-336">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71516-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-338">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="71516-338">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="71516-339">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="71516-339">Date and time the object was installed.</span></span> <span data-ttu-id="71516-340">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="71516-340">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="71516-341">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71516-341">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-342">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="71516-342">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-343">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71516-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71516-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-345">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="71516-345">Last error code reported by the logical device.</span></span>

<span data-ttu-id="71516-346">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-347">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="71516-347">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-348">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-350">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| система \\ \\ CurrentControlSet \\ \\ Enum \\ \\ root \| произв.")</span><span class="sxs-lookup"><span data-stu-id="71516-350">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Enum\\\\Root\|Mfg")</span></span>
</dt> </dl>

<span data-ttu-id="71516-351">Имя производителя контроллера SCSI.</span><span class="sxs-lookup"><span data-stu-id="71516-351">Name of the SCSI controller manufacturer.</span></span>

<span data-ttu-id="71516-352">Пример: Adaptec</span><span class="sxs-lookup"><span data-stu-id="71516-352">Example: "Adaptec"</span></span>

</dd> <dt>

<span data-ttu-id="71516-353">**максдатавидс**</span><span class="sxs-lookup"><span data-stu-id="71516-353">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-354">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71516-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71516-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-356">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("биты")</span><span class="sxs-lookup"><span data-stu-id="71516-356">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="71516-357">Максимальная ширина данных (в битах), поддерживаемая контроллером SCSI.</span><span class="sxs-lookup"><span data-stu-id="71516-357">Maximum data width (in bits) supported by the SCSI controller.</span></span>

<span data-ttu-id="71516-358">Это свойство наследуется от [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-358">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-359">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="71516-359">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-360">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71516-360">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="71516-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-362">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="71516-362">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="71516-363">Максимальное число напрямую предоставляемых сущностей, которые поддерживаются этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="71516-363">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="71516-364">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="71516-364">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="71516-365">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-365">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-366">**макстрансферрате**</span><span class="sxs-lookup"><span data-stu-id="71516-366">**MaxTransferRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-367">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="71516-367">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="71516-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-369">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="71516-369">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="71516-370">Максимальная скорость передачи (в битах в секунду), поддерживаемая контроллером SCSI.</span><span class="sxs-lookup"><span data-stu-id="71516-370">Maximum transfer rate (in bits per second) supported by the SCSI controller.</span></span>

<span data-ttu-id="71516-371">Это свойство наследуется от [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-371">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<span data-ttu-id="71516-372">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="71516-372">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="71516-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-376">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="71516-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="71516-377">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="71516-377">Label by which the object is known.</span></span> <span data-ttu-id="71516-378">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="71516-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="71516-379">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71516-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-380">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="71516-380">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-383">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="71516-383">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="71516-384">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-384">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="71516-385">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="71516-386">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="71516-386">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="71516-387">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="71516-387">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-388">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="71516-388">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="71516-389">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-389">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-390">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="71516-390">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="71516-391">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-391">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71516-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="71516-392"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="71516-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="71516-393"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="71516-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="71516-394"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="71516-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="71516-395"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="71516-396">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="71516-396">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="71516-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="71516-397"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="71516-398">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="71516-398">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="71516-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="71516-399"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="71516-400">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="71516-400">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="71516-401">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="71516-401">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="71516-402">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="71516-402">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="71516-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="71516-403"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="71516-404">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="71516-404">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="71516-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="71516-405"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="71516-406">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="71516-406">Timed Power-On Supported</span></span>

<span data-ttu-id="71516-407">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="71516-407">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-408">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="71516-408">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-409">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="71516-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="71516-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-411">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="71516-411">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="71516-412">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="71516-412">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="71516-413">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-414">**протектионманажемент**</span><span class="sxs-lookup"><span data-stu-id="71516-414">**ProtectionManagement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-415">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71516-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71516-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-417">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| -контроллер \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="71516-417">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Storage Controller\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="71516-418">Поддержка контроллера SCSI для обеспечения избыточности или защиты от сбоев устройств.</span><span class="sxs-lookup"><span data-stu-id="71516-418">Support of the SCSI controller for redundancy or protection against device failures.</span></span>

<span data-ttu-id="71516-419">Это свойство наследуется от [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-419">This property is inherited from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71516-420">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71516-420">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71516-421">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="71516-421">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span>

<span data-ttu-id="71516-422">Не **защищено** (3)</span><span class="sxs-lookup"><span data-stu-id="71516-422">**Unprotected** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span>

<span data-ttu-id="71516-423">**Защищено** (4)</span><span class="sxs-lookup"><span data-stu-id="71516-423">**Protected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC__SCSI-3_Controller_Command_"></span><span id="protected_through_scc__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="71516-424">**Защищено с помощью SCC (команда контроллера SCSI-3)** (5)</span><span class="sxs-lookup"><span data-stu-id="71516-424">**Protected through SCC (SCSI-3 Controller Command)** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Protected_through_SCC-2__SCSI-3_Controller_Command_"></span><span id="protected_through_scc-2__scsi-3_controller_command_"></span><span id="PROTECTED_THROUGH_SCC-2__SCSI-3_CONTROLLER_COMMAND_"></span>

<span data-ttu-id="71516-425">**Защищено с помощью SCC-2 (команда контроллера SCSI-3)** (6)</span><span class="sxs-lookup"><span data-stu-id="71516-425">**Protected through SCC-2 (SCSI-3 Controller Command)** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-426">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="71516-426">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-427">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71516-427">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71516-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-429">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="71516-429">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="71516-430">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="71516-430">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="71516-431">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-431">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="71516-432">В следующем списке приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="71516-432">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71516-433">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71516-433">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71516-434">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="71516-434">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="71516-435">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="71516-435">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="71516-436">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="71516-436">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="71516-437">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="71516-437">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="71516-438">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="71516-438">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="71516-439">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="71516-439">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="71516-440">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="71516-440">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="71516-441">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="71516-441">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="71516-442">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="71516-442">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="71516-443">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="71516-443">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="71516-444">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="71516-444">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="71516-445">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="71516-445">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="71516-446">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="71516-446">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="71516-447">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="71516-447">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="71516-448">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="71516-448">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="71516-449">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="71516-449">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="71516-450">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="71516-450">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="71516-451">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="71516-451">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="71516-452">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="71516-452">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="71516-453">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="71516-453">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="71516-454">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="71516-454">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="71516-455">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="71516-455">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="71516-456">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="71516-456">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="71516-457">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="71516-457">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="71516-458">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="71516-458">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="71516-459">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="71516-459">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="71516-460">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="71516-460">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="71516-461">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="71516-461">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="71516-462">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="71516-462">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="71516-463">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="71516-463">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="71516-464">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="71516-464">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="71516-465">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="71516-465">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="71516-466">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="71516-466">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="71516-467">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="71516-467">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="71516-468">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="71516-468">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="71516-469">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="71516-469">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="71516-470">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="71516-470">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="71516-471">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="71516-471">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="71516-472">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="71516-472">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="71516-473">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="71516-473">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="71516-474">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="71516-474">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="71516-475">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="71516-475">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="71516-476">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="71516-476">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="71516-477">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="71516-477">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="71516-478">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="71516-478">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="71516-479">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="71516-479">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-480">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="71516-480">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-483">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="71516-483">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="71516-484">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="71516-484">Current status of the object.</span></span> <span data-ttu-id="71516-485">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="71516-485">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="71516-486">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="71516-486">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="71516-487">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="71516-487">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="71516-488">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="71516-488">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="71516-489">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="71516-489">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="71516-490">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="71516-490">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="71516-491">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="71516-491">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="71516-492">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="71516-492">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="71516-493">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="71516-493">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="71516-494">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="71516-494">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71516-495">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="71516-495">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="71516-496">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="71516-496">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="71516-497">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="71516-497">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="71516-498">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="71516-498">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="71516-499">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="71516-499">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="71516-500">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="71516-500">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="71516-501">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="71516-501">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="71516-502">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="71516-502">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="71516-503">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="71516-503">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-504">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="71516-504">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-505">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="71516-505">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="71516-506">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-507">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="71516-507">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="71516-508">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="71516-508">State of the logical device.</span></span> <span data-ttu-id="71516-509">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="71516-509">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="71516-510">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="71516-511">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="71516-511">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="71516-512">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="71516-512">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="71516-513">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="71516-513">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="71516-514">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="71516-514">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="71516-515">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="71516-515">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="71516-516">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="71516-516">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-517">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-518">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-518">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-519">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="71516-519">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="71516-520">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="71516-520">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="71516-521">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-522">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="71516-522">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-523">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="71516-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71516-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71516-525">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="71516-525">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="71516-526">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="71516-526">Name of the scoping system.</span></span>

<span data-ttu-id="71516-527">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="71516-527">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="71516-528">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="71516-528">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71516-529">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="71516-529">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="71516-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="71516-530">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="71516-531">Дата и время последнего сброса этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="71516-531">Date and time this controller was last reset.</span></span> <span data-ttu-id="71516-532">Это может означать, что контроллер был выключен или повторно инициализирован.</span><span class="sxs-lookup"><span data-stu-id="71516-532">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="71516-533">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-533">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="71516-534">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71516-534">Remarks</span></span>

<span data-ttu-id="71516-535">Класс **Win32 \_ сксиконтроллер** является производным от [**CIM \_ сксиконтроллер**](cim-scsicontroller.md).</span><span class="sxs-lookup"><span data-stu-id="71516-535">The **Win32\_SCSIController** class is derived from [**CIM\_SCSIController**](cim-scsicontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71516-536">Требования</span><span class="sxs-lookup"><span data-stu-id="71516-536">Requirements</span></span>



| <span data-ttu-id="71516-537">Требование</span><span class="sxs-lookup"><span data-stu-id="71516-537">Requirement</span></span> | <span data-ttu-id="71516-538">Значение</span><span class="sxs-lookup"><span data-stu-id="71516-538">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71516-539">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="71516-539">Minimum supported client</span></span><br/> | <span data-ttu-id="71516-540">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71516-540">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="71516-541">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="71516-541">Minimum supported server</span></span><br/> | <span data-ttu-id="71516-542">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71516-542">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="71516-543">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="71516-543">Namespace</span></span><br/>                | <span data-ttu-id="71516-544">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="71516-544">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="71516-545">MOF</span><span class="sxs-lookup"><span data-stu-id="71516-545">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71516-546"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="71516-546"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="71516-547">DLL</span><span class="sxs-lookup"><span data-stu-id="71516-547">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71516-548"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71516-548"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71516-549">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71516-549">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71516-550">**\_СКСИКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="71516-550">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dt>

[<span data-ttu-id="71516-551">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="71516-551">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
