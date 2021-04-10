---
description: '\_Класс WMI "Win32 SerialPort" представляет последовательный порт в компьютерной системе под Windows.'
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Класс Win32_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140978"
---
# <a name="win32_serialport-class"></a><span data-ttu-id="3db88-103">\_Класс Win32 SerialPort</span><span class="sxs-lookup"><span data-stu-id="3db88-103">Win32\_SerialPort class</span></span>

<span data-ttu-id="3db88-104">[Класс WMI](../wmisdk/retrieving-a-class.md) " **Win32 \_ SerialPort** " представляет последовательный порт в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="3db88-104">The **Win32\_SerialPort** [WMI class](../wmisdk/retrieving-a-class.md) represents a serial port on a computer system running Windows.</span></span>

<span data-ttu-id="3db88-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3db88-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3db88-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3db88-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db88-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3db88-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
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
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="3db88-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3db88-108">Members</span></span>

<span data-ttu-id="3db88-109">Класс **Win32 \_ SerialPort** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3db88-109">The **Win32\_SerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="3db88-110">Методы</span><span class="sxs-lookup"><span data-stu-id="3db88-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3db88-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3db88-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3db88-112">Методы</span><span class="sxs-lookup"><span data-stu-id="3db88-112">Methods</span></span>

<span data-ttu-id="3db88-113">Класс **Win32 \_ SerialPort** имеет следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3db88-113">The **Win32\_SerialPort** class has these methods.</span></span>



| <span data-ttu-id="3db88-114">Метод</span><span class="sxs-lookup"><span data-stu-id="3db88-114">Method</span></span>            | <span data-ttu-id="3db88-115">Описание</span><span class="sxs-lookup"><span data-stu-id="3db88-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db88-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="3db88-116">**Reset**</span></span>         | <span data-ttu-id="3db88-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="3db88-117">Not implemented.</span></span> <span data-ttu-id="3db88-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ сериалконтроллер**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/>                 |
| <span data-ttu-id="3db88-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3db88-119">**SetPowerState**</span></span> | <span data-ttu-id="3db88-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="3db88-120">Not implemented.</span></span> <span data-ttu-id="3db88-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ сериалконтроллер**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_SerialController**](cim-serialcontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3db88-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="3db88-122">Properties</span></span>

<span data-ttu-id="3db88-123">Класс **Win32 \_ SerialPort** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3db88-123">The **Win32\_SerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3db88-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="3db88-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3db88-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="3db88-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-128">Availability and status of the device.</span></span>

<span data-ttu-id="3db88-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3db88-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3db88-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3db88-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="3db88-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="3db88-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="3db88-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="3db88-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="3db88-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="3db88-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="3db88-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="3db88-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3db88-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="3db88-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="3db88-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="3db88-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="3db88-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="3db88-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="3db88-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="3db88-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3db88-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="3db88-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="3db88-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="3db88-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="3db88-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="3db88-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="3db88-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="3db88-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="3db88-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="3db88-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="3db88-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="3db88-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="3db88-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="3db88-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="3db88-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="3db88-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="3db88-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="3db88-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="3db88-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="3db88-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="3db88-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="3db88-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-153">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="3db88-153">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="3db88-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="3db88-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-155">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="3db88-155">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="3db88-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="3db88-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-157">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="3db88-157">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="3db88-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="3db88-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-159">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="3db88-159">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-160">**Двоичный**</span><span class="sxs-lookup"><span data-stu-id="3db88-160">**Binary**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-161">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-163">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| фбинари")</span><span class="sxs-lookup"><span data-stu-id="3db88-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-164">Если задано **значение true**, то последовательный порт настроен для передачи двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="3db88-164">If **TRUE**, the serial port is configured for binary data transfer.</span></span> <span data-ttu-id="3db88-165">Так как API Windows не поддерживает передачу в режиме без двоичного режима, это свойство должно иметь **значение true**.</span><span class="sxs-lookup"><span data-stu-id="3db88-165">Because the Windows API does not support nonbinary mode transfers, this property must be **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-166">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="3db88-166">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-167">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3db88-167">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3db88-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-169">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Последовательные порты DMTF \| 004,7 "), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сериалконтроллер**](cim-serialcontroller.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="3db88-169">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.7"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-170">Массив совместимости на уровне микросхемы для контроллера последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-170">Array of chip-level compatibility for the serial controller.</span></span> <span data-ttu-id="3db88-171">Это свойство описывает буферизацию и другие возможности последовательного контроллера, которые могут быть встроенными в оборудование микросхемы.</span><span class="sxs-lookup"><span data-stu-id="3db88-171">This property describes the buffering and other capabilities of the serial controller that may be inherent in the chip hardware.</span></span> <span data-ttu-id="3db88-172">Свойство является перечислимым целым числом.</span><span class="sxs-lookup"><span data-stu-id="3db88-172">The property is an enumerated integer.</span></span>

<span data-ttu-id="3db88-173">Это свойство наследуется от [**CIM \_ сериалконтроллер**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-173">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3db88-174">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3db88-174">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3db88-175">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="3db88-175">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

<span data-ttu-id="3db88-176">**XT/AT-совместимый** (3)</span><span class="sxs-lookup"><span data-stu-id="3db88-176">**XT/AT Compatible** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

<span data-ttu-id="3db88-177">**Совместимость с 16450** (4)</span><span class="sxs-lookup"><span data-stu-id="3db88-177">**16450 Compatible** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

<span data-ttu-id="3db88-178">**Совместимость с 16550** (5)</span><span class="sxs-lookup"><span data-stu-id="3db88-178">**16550 Compatible** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

<span data-ttu-id="3db88-179">**16550A-совместимый** (6)</span><span class="sxs-lookup"><span data-stu-id="3db88-179">**16550A Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="3db88-180">**Совместимость с 8251** (160)</span><span class="sxs-lookup"><span data-stu-id="3db88-180">**8251 Compatible** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

<span data-ttu-id="3db88-181">**8251FIFO-совместимый** (161)</span><span class="sxs-lookup"><span data-stu-id="3db88-181">**8251FIFO Compatible** (161)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-182">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="3db88-182">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-183">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3db88-183">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3db88-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-185">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ сериалконтроллер**](cim-serialcontroller.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="3db88-185">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_SerialController**](cim-serialcontroller.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-186">Массив строк произвольной формы, предоставляющий более подробные объяснения для любых функций последовательного контроллера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="3db88-186">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="3db88-187">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="3db88-187">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="3db88-188">Это свойство наследуется от [**CIM \_ сериалконтроллер**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-188">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-189">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3db88-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-192">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="3db88-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-193">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3db88-193">Short description of the object.</span></span>

<span data-ttu-id="3db88-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-195">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="3db88-195">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-196">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3db88-196">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-198">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3db88-198">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-199">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3db88-199">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="3db88-200">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-200">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="3db88-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="3db88-201"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="3db88-202"> (0)</span><span class="sxs-lookup"><span data-stu-id="3db88-202">(0)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-203">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="3db88-203">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="3db88-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="3db88-204"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="3db88-205">(1)</span><span class="sxs-lookup"><span data-stu-id="3db88-205">(1)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-206">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="3db88-206">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3db88-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-207"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="3db88-208">(2)</span><span class="sxs-lookup"><span data-stu-id="3db88-208">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="3db88-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="3db88-209"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="3db88-210">(3)</span><span class="sxs-lookup"><span data-stu-id="3db88-210">(3)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-211">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3db88-211">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3db88-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="3db88-212"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="3db88-213">(4)</span><span class="sxs-lookup"><span data-stu-id="3db88-213">(4)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-214">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="3db88-214">Device is not working properly.</span></span> <span data-ttu-id="3db88-215">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="3db88-215">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="3db88-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="3db88-216"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="3db88-217">(5)</span><span class="sxs-lookup"><span data-stu-id="3db88-217">(5)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-218">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="3db88-218">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="3db88-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="3db88-219"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="3db88-220"> (6)</span><span class="sxs-lookup"><span data-stu-id="3db88-220">(6)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-221">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="3db88-221">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="3db88-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="3db88-222"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="3db88-223">(7)</span><span class="sxs-lookup"><span data-stu-id="3db88-223">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="3db88-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-224"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="3db88-225">(8)</span><span class="sxs-lookup"><span data-stu-id="3db88-225">(8)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-226">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-226">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="3db88-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-227"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="3db88-228">(9)</span><span class="sxs-lookup"><span data-stu-id="3db88-228">(9)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-229">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="3db88-229">Device is not working properly.</span></span> <span data-ttu-id="3db88-230">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-230">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="3db88-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="3db88-231"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="3db88-232">(10)</span><span class="sxs-lookup"><span data-stu-id="3db88-232">(10)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-233">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="3db88-233">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="3db88-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-234"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="3db88-235">(11)</span><span class="sxs-lookup"><span data-stu-id="3db88-235">(11)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-236">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-236">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="3db88-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="3db88-237"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="3db88-238">(12)</span><span class="sxs-lookup"><span data-stu-id="3db88-238">(12)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-239">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="3db88-239">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="3db88-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-240"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="3db88-241">(13)</span><span class="sxs-lookup"><span data-stu-id="3db88-241">(13)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-242">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-242">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="3db88-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="3db88-243"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="3db88-244">(14)</span><span class="sxs-lookup"><span data-stu-id="3db88-244">(14)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-245">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="3db88-245">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="3db88-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="3db88-246"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="3db88-247">(15)</span><span class="sxs-lookup"><span data-stu-id="3db88-247">(15)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-248">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="3db88-248">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="3db88-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="3db88-249"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="3db88-250">(16)</span><span class="sxs-lookup"><span data-stu-id="3db88-250">(16)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-251">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="3db88-251">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="3db88-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="3db88-252"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="3db88-253">(17)</span><span class="sxs-lookup"><span data-stu-id="3db88-253">(17)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-254">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="3db88-254">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3db88-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-255"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="3db88-256">(18)</span><span class="sxs-lookup"><span data-stu-id="3db88-256">(18)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-257">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="3db88-257">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="3db88-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="3db88-258"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="3db88-259">(19)</span><span class="sxs-lookup"><span data-stu-id="3db88-259">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="3db88-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="3db88-260"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="3db88-261">(20)</span><span class="sxs-lookup"><span data-stu-id="3db88-261">(20)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-262">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="3db88-262">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="3db88-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="3db88-263"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="3db88-264">(21)</span><span class="sxs-lookup"><span data-stu-id="3db88-264">(21)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-265">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="3db88-265">System failure.</span></span> <span data-ttu-id="3db88-266">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="3db88-266">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="3db88-267">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="3db88-267">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="3db88-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="3db88-268"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="3db88-269">(22)</span><span class="sxs-lookup"><span data-stu-id="3db88-269">(22)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-270">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="3db88-270">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="3db88-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="3db88-271"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="3db88-272">(23)</span><span class="sxs-lookup"><span data-stu-id="3db88-272">(23)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-273">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="3db88-273">System failure.</span></span> <span data-ttu-id="3db88-274">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="3db88-274">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="3db88-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="3db88-275"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="3db88-276">(24)</span><span class="sxs-lookup"><span data-stu-id="3db88-276">(24)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-277">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="3db88-277">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3db88-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="3db88-278"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3db88-279">(25)</span><span class="sxs-lookup"><span data-stu-id="3db88-279">(25)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-280">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="3db88-280">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="3db88-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="3db88-281"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="3db88-282">(26)</span><span class="sxs-lookup"><span data-stu-id="3db88-282">(26)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-283">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="3db88-283">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="3db88-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="3db88-284"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="3db88-285">(27)</span><span class="sxs-lookup"><span data-stu-id="3db88-285">(27)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-286">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="3db88-286">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="3db88-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="3db88-287"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="3db88-288">(28)</span><span class="sxs-lookup"><span data-stu-id="3db88-288">(28)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-289">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="3db88-289">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="3db88-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="3db88-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="3db88-291">(29)</span><span class="sxs-lookup"><span data-stu-id="3db88-291">(29)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-292">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="3db88-292">Device is disabled.</span></span> <span data-ttu-id="3db88-293">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3db88-293">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="3db88-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="3db88-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="3db88-295">(30)</span><span class="sxs-lookup"><span data-stu-id="3db88-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-296">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="3db88-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="3db88-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="3db88-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="3db88-298">1-31</span><span class="sxs-lookup"><span data-stu-id="3db88-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-299">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="3db88-299">Device is not working properly.</span></span> <span data-ttu-id="3db88-300">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="3db88-300">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-301">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="3db88-301">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-302">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-304">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3db88-304">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-305">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="3db88-305">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="3db88-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3db88-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-310">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3db88-310">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3db88-311">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="3db88-311">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="3db88-312">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="3db88-312">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="3db88-313">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-314">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3db88-314">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-317">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="3db88-317">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-318">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3db88-318">Description of the object.</span></span>

<span data-ttu-id="3db88-319">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-319">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-320">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="3db88-320">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-323">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ девицемап \\ \\ сериалкомм")</span><span class="sxs-lookup"><span data-stu-id="3db88-323">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-324">Уникальный идентификатор последовательного порта с другими устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="3db88-324">Unique identifier of the serial port with other devices on the system.</span></span>

<span data-ttu-id="3db88-325">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-325">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-326">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="3db88-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-327">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3db88-329">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="3db88-329">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="3db88-330">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3db88-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-332">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3db88-334">Строка свободной формы, предоставляя дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="3db88-334">Free-form string supplying more information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="3db88-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-336">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3db88-336">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-337">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3db88-337">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-339">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="3db88-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-340">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="3db88-340">Date and time the object was installed.</span></span> <span data-ttu-id="3db88-341">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="3db88-341">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="3db88-342">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-343">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="3db88-343">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-344">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3db88-344">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3db88-346">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="3db88-346">Last error code reported by the logical device.</span></span>

<span data-ttu-id="3db88-347">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-347">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-348">**максбаудрате**</span><span class="sxs-lookup"><span data-stu-id="3db88-348">**MaxBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-349">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3db88-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-351">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Последовательные порты DMTF \| 004,6 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" бит в секунду ")</span><span class="sxs-lookup"><span data-stu-id="3db88-351">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Serial Ports\|004.6"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-352">Максимальная скорость (в битах в секунду), поддерживаемая последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="3db88-352">Maximum baud rate (in bits per second) supported by the serial controller.</span></span>

<span data-ttu-id="3db88-353">Это свойство наследуется от [**CIM \_ сериалконтроллер**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-353">This property is inherited from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-354">**максимуминпутбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="3db88-354">**MaximumInputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-355">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3db88-355">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-357">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двмаксркскуеуе"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="3db88-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxRxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-358">Максимальный размер внутреннего входного буфера драйвера последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-358">Maximum size of the serial port driver's internal input buffer.</span></span> <span data-ttu-id="3db88-359">Значение 0 (ноль) указывает, что в последовательном поставщике не предусмотрено максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="3db88-359">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-360">**максимумаутпутбуфферсизе**</span><span class="sxs-lookup"><span data-stu-id="3db88-360">**MaximumOutputBufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-361">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3db88-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-363">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двмаксткскуеуе"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="3db88-363">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwMaxTxQueue"), [**units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-364">Максимальный размер внутреннего выходного буфера драйвера последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-364">Maximum size of the serial port driver's internal output buffer.</span></span> <span data-ttu-id="3db88-365">Значение 0 (ноль) указывает, что в последовательном поставщике не предусмотрено максимальное значение.</span><span class="sxs-lookup"><span data-stu-id="3db88-365">A value of 0 (zero) indicates that no maximum value is imposed by the serial provider.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-366">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="3db88-366">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-367">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3db88-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-369">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="3db88-369">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-370">Максимальное число напрямую предоставляемых сущностей, которые поддерживаются этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="3db88-370">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="3db88-371">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="3db88-371">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="3db88-372">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-372">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-373">**Name**</span><span class="sxs-lookup"><span data-stu-id="3db88-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-374">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-376">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="3db88-376">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-377">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="3db88-377">Label by which the object is known.</span></span> <span data-ttu-id="3db88-378">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="3db88-378">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="3db88-379">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-379">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-380">**осаутодисковеред**</span><span class="sxs-lookup"><span data-stu-id="3db88-380">**OSAutoDiscovered**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-381">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-383">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| оборудования \\ \\ Описание \\ \\ системы \\ \\ мултифунктионадаптер")</span><span class="sxs-lookup"><span data-stu-id="3db88-383">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HARDWARE\\\\DESCRIPTION\\\\SYSTEM\\\\MultifunctionAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-384">Если **значение — true**, экземпляры этого класса были автоматически обнаружены операционной системой.</span><span class="sxs-lookup"><span data-stu-id="3db88-384">If **TRUE**, the instances of this class were automatically discovered by the operating system.</span></span> <span data-ttu-id="3db88-385">Если, например, с помощью панели управления было добавлено оборудование, операционная система находит экземпляры этого класса путем запроса оборудования из экземпляров этого класса.</span><span class="sxs-lookup"><span data-stu-id="3db88-385">If, for example, hardware was added through Control Panel, the operating system finds instances of this class by querying hardware from the instances of this class.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-386">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="3db88-386">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-389">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="3db88-389">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-390">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-390">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="3db88-391">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="3db88-392">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="3db88-392">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="3db88-393">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="3db88-393">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-394">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3db88-394">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3db88-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3db88-396">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="3db88-396">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="3db88-397">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-397">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3db88-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3db88-398"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="3db88-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="3db88-399"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3db88-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="3db88-400"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3db88-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="3db88-401"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-402">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="3db88-402">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="3db88-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="3db88-403"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-404">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="3db88-404">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="3db88-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="3db88-405"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-406">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="3db88-406">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="3db88-407">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="3db88-407">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="3db88-408">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-408">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="3db88-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="3db88-409"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-410">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="3db88-410">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="3db88-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="3db88-411"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-412">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="3db88-412">Timed Power-On Supported</span></span>

<span data-ttu-id="3db88-413">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="3db88-413">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-414">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="3db88-414">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-415">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-415">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3db88-417">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="3db88-417">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="3db88-418">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="3db88-418">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="3db88-419">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-420">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="3db88-420">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-421">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3db88-421">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-422">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-423">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="3db88-423">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-424">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="3db88-424">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="3db88-425">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-425">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="3db88-426">В следующем списке приведены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="3db88-426">The following list shows the possible values.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3db88-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3db88-427"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3db88-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="3db88-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="3db88-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="3db88-429"><span id="EISA"></span><span id="eisa"></span>**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="3db88-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="3db88-430"><span id="ISA"></span><span id="isa"></span>**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="3db88-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="3db88-431"><span id="PCI"></span><span id="pci"></span>**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="3db88-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="3db88-432"><span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3db88-433">ATA или ATAPI</span><span class="sxs-lookup"><span data-stu-id="3db88-433">ATA or ATAPI</span></span>

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="3db88-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="3db88-434"><span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="3db88-435"><span id="1496"></span>**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="3db88-435"><span id="1496"></span>**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="3db88-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="3db88-436"><span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="3db88-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="3db88-437"><span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="3db88-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="3db88-438"><span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="3db88-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="3db88-439"><span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="3db88-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="3db88-440"><span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="3db88-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="3db88-441"><span id="VESA"></span><span id="vesa"></span>**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="3db88-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="3db88-442"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="3db88-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="3db88-443"><span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="3db88-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="3db88-444"><span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="3db88-445"><span id="ESCON"></span><span id="escon"></span>**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="3db88-445"><span id="ESCON"></span><span id="escon"></span>**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="3db88-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="3db88-446"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="3db88-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="3db88-447"><span id="I2C"></span><span id="i2c"></span>**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="3db88-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="3db88-448"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="3db88-449"><span id="HIPPI"></span><span id="hippi"></span>**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="3db88-449"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="3db88-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="3db88-450"><span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="3db88-451"><span id="VME"></span><span id="vme"></span>**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="3db88-451"><span id="VME"></span><span id="vme"></span>**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="3db88-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="3db88-452"><span id="IPI"></span><span id="ipi"></span>**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="3db88-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="3db88-453"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="3db88-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="3db88-454"><span id="RS232"></span><span id="rs232"></span>**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="3db88-455"><span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="3db88-455"><span id="ieee_802.3_10base5"></span>**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="3db88-456"><span id="ieee_802.3_10base2"></span>**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="3db88-456"><span id="ieee_802.3_10base2"></span>**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="3db88-457"><span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="3db88-457"><span id="ieee_802.3_1base5"></span>**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="3db88-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="3db88-458"><span id="ieee_802.3_10broad36"></span>**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="3db88-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="3db88-459"><span id="ieee_802.3_100basevg"></span>**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="3db88-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="3db88-460"><span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="3db88-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="3db88-461"><span id="ansi_x3t9.5_fddi"></span>**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="3db88-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="3db88-462"><span id="MCA"></span><span id="mca"></span>**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="3db88-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="3db88-463"><span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="3db88-464"><span id="IDE"></span><span id="ide"></span>**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="3db88-464"><span id="IDE"></span><span id="ide"></span>**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="3db88-465"><span id="CMD"></span><span id="cmd"></span>**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="3db88-465"><span id="CMD"></span><span id="cmd"></span>**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="3db88-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="3db88-466"><span id="ST506"></span><span id="st506"></span>**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="3db88-467"><span id="DSSI"></span><span id="dssi"></span>**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="3db88-467"><span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="3db88-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="3db88-468"><span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="3db88-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="3db88-469"><span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="3db88-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="3db88-470"><span id="AGP"></span><span id="agp"></span>**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="3db88-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="3db88-471"><span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="3db88-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="3db88-472"><span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="3db88-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="3db88-473"><span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="3db88-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="3db88-474"><span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-475">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="3db88-475">**ProviderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-476">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-476">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-478">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровсубтипе")</span><span class="sxs-lookup"><span data-stu-id="3db88-478">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvSubType")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-479">Тип поставщика услуг связи.</span><span class="sxs-lookup"><span data-stu-id="3db88-479">Communications provider type.</span></span>

<span data-ttu-id="3db88-480">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="3db88-480">The values are:</span></span>

<dl> <dd><span data-ttu-id="3db88-481">"ФАКСИМИЛЬное устройство"</span><span class="sxs-lookup"><span data-stu-id="3db88-481">"FAX Device"</span></span></dd> <dd><span data-ttu-id="3db88-482">Протокол LAT</span><span class="sxs-lookup"><span data-stu-id="3db88-482">"LAT Protocol"</span></span></dd> <dd><span data-ttu-id="3db88-483">"Устройство модема"</span><span class="sxs-lookup"><span data-stu-id="3db88-483">"Modem Device"</span></span></dd> <dd><span data-ttu-id="3db88-484">"Сетевой мост"</span><span class="sxs-lookup"><span data-stu-id="3db88-484">"Network Bridge"</span></span></dd> <dd><span data-ttu-id="3db88-485">"Параллельный порт"</span><span class="sxs-lookup"><span data-stu-id="3db88-485">"Parallel Port"</span></span></dd> <dd><span data-ttu-id="3db88-486">Последовательный порт RS232</span><span class="sxs-lookup"><span data-stu-id="3db88-486">"RS232 Serial Port"</span></span></dd> <dd><span data-ttu-id="3db88-487">"Порт RS422"</span><span class="sxs-lookup"><span data-stu-id="3db88-487">"RS422 Port"</span></span></dd> <dd><span data-ttu-id="3db88-488">"Порт RS423"</span><span class="sxs-lookup"><span data-stu-id="3db88-488">"RS423 Port"</span></span></dd> <dd><span data-ttu-id="3db88-489">"Порт RS449"</span><span class="sxs-lookup"><span data-stu-id="3db88-489">"RS449 Port"</span></span></dd> <dd><span data-ttu-id="3db88-490">"Устройство сканера"</span><span class="sxs-lookup"><span data-stu-id="3db88-490">"Scanner Device"</span></span></dd> <dd><span data-ttu-id="3db88-491">«TCP/IP TelNet»</span><span class="sxs-lookup"><span data-stu-id="3db88-491">"TCP/IP TelNet"</span></span></dd> <dd><span data-ttu-id="3db88-492">"X. 25"</span><span class="sxs-lookup"><span data-stu-id="3db88-492">"X.25"</span></span></dd> <dd><span data-ttu-id="3db88-493">Unspecified</span><span class="sxs-lookup"><span data-stu-id="3db88-493">"Unspecified"</span></span></dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

<span data-ttu-id="3db88-494">**Факсимильное устройство** (факсимильное устройство)</span><span class="sxs-lookup"><span data-stu-id="3db88-494">**FAX Device** ("FAX Device")</span></span>


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

<span data-ttu-id="3db88-495">**Протокол Lat** (протокол LAT)</span><span class="sxs-lookup"><span data-stu-id="3db88-495">**LAT Protocol** ("LAT Protocol")</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

<span data-ttu-id="3db88-496">**Модемное устройство** ("устройство модема")</span><span class="sxs-lookup"><span data-stu-id="3db88-496">**Modem Device** ("Modem Device")</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

<span data-ttu-id="3db88-497">**Сетевой мост** ("сетевой мост")</span><span class="sxs-lookup"><span data-stu-id="3db88-497">**Network Bridge** ("Network Bridge")</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="3db88-498">**Параллельный порт** ("параллельный порт")</span><span class="sxs-lookup"><span data-stu-id="3db88-498">**Parallel Port** ("Parallel Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

<span data-ttu-id="3db88-499">**Последовательный порт RS232** ("последовательный порт RS232")</span><span class="sxs-lookup"><span data-stu-id="3db88-499">**RS232 Serial Port** ("RS232 Serial Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

<span data-ttu-id="3db88-500">**Порт RS422** ("порт RS422")</span><span class="sxs-lookup"><span data-stu-id="3db88-500">**RS422 Port** ("RS422 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

<span data-ttu-id="3db88-501">**Порт RS423** ("порт RS423")</span><span class="sxs-lookup"><span data-stu-id="3db88-501">**RS423 Port** ("RS423 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

<span data-ttu-id="3db88-502">**Порт RS449** ("порт RS449")</span><span class="sxs-lookup"><span data-stu-id="3db88-502">**RS449 Port** ("RS449 Port")</span></span>


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

<span data-ttu-id="3db88-503">**Устройство сканера** ("устройство сканера")</span><span class="sxs-lookup"><span data-stu-id="3db88-503">**Scanner Device** ("Scanner Device")</span></span>


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

<span data-ttu-id="3db88-504">**TCP/IP Telnet** ("TCP/IP Telnet")</span><span class="sxs-lookup"><span data-stu-id="3db88-504">**TCP/IP TelNet** ("TCP/IP TelNet")</span></span>


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

<span data-ttu-id="3db88-505">**X. 25** ("X. 25")</span><span class="sxs-lookup"><span data-stu-id="3db88-505">**X.25** ("X.25")</span></span>


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="3db88-506">Не **указано** ("не указано")</span><span class="sxs-lookup"><span data-stu-id="3db88-506">**Unspecified** ("Unspecified")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-507">**сеттаблебаудрате**</span><span class="sxs-lookup"><span data-stu-id="3db88-507">**SettableBaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-508">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-508">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-509">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-509">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-510">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| SP \_ бод")</span><span class="sxs-lookup"><span data-stu-id="3db88-510">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_BAUD")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-511">Если **значение — true**, скорость передачи может быть изменена для этого последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-511">If **TRUE**, the baud rate can be changed for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-512">**сеттабледатабитс**</span><span class="sxs-lookup"><span data-stu-id="3db88-512">**SettableDataBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-513">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-513">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-514">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-515">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| SP \_ ")</span><span class="sxs-lookup"><span data-stu-id="3db88-515">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_DATABITS")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-516">Если задано **значение true**, для этого последовательного порта можно задать биты данных.</span><span class="sxs-lookup"><span data-stu-id="3db88-516">If **TRUE**, data bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-517">**сеттаблефловконтрол**</span><span class="sxs-lookup"><span data-stu-id="3db88-517">**SettableFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-518">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-518">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-519">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-520">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| SP \_ ")</span><span class="sxs-lookup"><span data-stu-id="3db88-520">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_HANDSHAKING")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-521">Если **значение — true**, управление потоком можно задать для этого последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-521">If **TRUE**, flow control can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-522">**сеттаблепарити**</span><span class="sxs-lookup"><span data-stu-id="3db88-522">**SettableParity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-523">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-523">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-525">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| SP с \_ контролем четности")</span><span class="sxs-lookup"><span data-stu-id="3db88-525">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-526">Если **значение — true**, для этого последовательного порта можно задать четность.</span><span class="sxs-lookup"><span data-stu-id="3db88-526">If **TRUE**, parity can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-527">**сеттаблепаритичекк**</span><span class="sxs-lookup"><span data-stu-id="3db88-527">**SettableParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-528">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-528">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-529">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-530">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| \_ Проверка четности SP \_ ")</span><span class="sxs-lookup"><span data-stu-id="3db88-530">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-531">Если **значение — true**, для этого последовательного порта можно задать проверку четности (если проверка четности поддерживается).</span><span class="sxs-lookup"><span data-stu-id="3db88-531">If **TRUE**, parity checking can be set for this serial port (if parity checking is supported).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-532">**сеттаблерлсд**</span><span class="sxs-lookup"><span data-stu-id="3db88-532">**SettableRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-533">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-533">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-534">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-534">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-535">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| SP \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="3db88-535">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-536">Если задано **значение true**, для этого последовательного порта можно установить обнаружение сигнального сигнала (rlsd) (если параметр rlsd поддерживается).</span><span class="sxs-lookup"><span data-stu-id="3db88-536">If **TRUE**, Received Line Signal Detect (RLSD) can be set for this serial port (if RLSD is supported).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-537">**сеттаблестопбитс**</span><span class="sxs-lookup"><span data-stu-id="3db88-537">**SettableStopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-538">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-538">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-539">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-539">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-540">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двсеттаблепарамс \| SP \_ стопбитс")</span><span class="sxs-lookup"><span data-stu-id="3db88-540">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwSettableParams\|SP\_STOPBITS")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-541">Если задано **значение true**, для этого последовательного порта можно задать биты BITS.</span><span class="sxs-lookup"><span data-stu-id="3db88-541">If **TRUE**, stop bits can be set for this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-542">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="3db88-542">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-543">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-543">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-544">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-544">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-545">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="3db88-545">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-546">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="3db88-546">Current status of the object.</span></span> <span data-ttu-id="3db88-547">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="3db88-547">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3db88-548">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="3db88-548">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3db88-549">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="3db88-549">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3db88-550">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="3db88-550">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3db88-551">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="3db88-551">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3db88-552">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-552">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="3db88-553">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="3db88-553">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="3db88-554">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="3db88-554">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="3db88-555">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="3db88-555">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="3db88-556">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="3db88-556">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3db88-557">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="3db88-557">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="3db88-558">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="3db88-558">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="3db88-559">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="3db88-559">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="3db88-560">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="3db88-560">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3db88-561">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="3db88-561">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="3db88-562">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="3db88-562">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="3db88-563">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="3db88-563">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="3db88-564">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="3db88-564">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="3db88-565">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="3db88-565">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-566">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3db88-566">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-567">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3db88-567">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-568">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-568">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-569">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="3db88-569">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-570">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="3db88-570">State of the logical device.</span></span> <span data-ttu-id="3db88-571">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="3db88-571">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="3db88-572">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-572">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="3db88-573">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="3db88-573">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3db88-574">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="3db88-574">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="3db88-575">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="3db88-575">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="3db88-576">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="3db88-576">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="3db88-577">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="3db88-577">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3db88-578">**Supports16BitMode**</span><span class="sxs-lookup"><span data-stu-id="3db88-578">**Supports16BitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-579">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-579">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-580">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-581">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ 16BITMODE")</span><span class="sxs-lookup"><span data-stu-id="3db88-581">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_16BITMODE")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-582">Если задано **значение true**, в этом последовательном порте поддерживается 16-разрядный режим.</span><span class="sxs-lookup"><span data-stu-id="3db88-582">If **TRUE**, 16-bit mode is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-583">**суппортсдтрдср**</span><span class="sxs-lookup"><span data-stu-id="3db88-583">**SupportsDTRDSR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-584">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-584">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-585">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-585">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-586">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ DTR/DSR")</span><span class="sxs-lookup"><span data-stu-id="3db88-586">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_DTRDSR")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-587">Если задано **значение true**, в этом последовательном порте поддерживаются сигналы терминала (DTR) и готовый набор данных (DSR).</span><span class="sxs-lookup"><span data-stu-id="3db88-587">If **TRUE**, data terminal ready (DTR) and data set ready (DSR) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-588">**суппортселапседтимеаутс**</span><span class="sxs-lookup"><span data-stu-id="3db88-588">**SupportsElapsedTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-589">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-589">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-590">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-591">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ тоталтимеаутс")</span><span class="sxs-lookup"><span data-stu-id="3db88-591">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_TOTALTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-592">Если **значение равно true**, прошедшие тайм-ауты поддерживаются в этом последовательном порте.</span><span class="sxs-lookup"><span data-stu-id="3db88-592">If **TRUE**, elapsed time-outs are supported on this serial port.</span></span> <span data-ttu-id="3db88-593">Прошедшее время ожидания отследится от общего количества времени между передачами данных.</span><span class="sxs-lookup"><span data-stu-id="3db88-593">Elapsed timeouts track the total amount of time between data transmissions.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-594">**суппортсинттимеаутс**</span><span class="sxs-lookup"><span data-stu-id="3db88-594">**SupportsIntTimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-595">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-595">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-596">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-596">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-597">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ инттимеаутс")</span><span class="sxs-lookup"><span data-stu-id="3db88-597">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_INTTIMEOUTS")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-598">Если задано **значение true**, интервалы времени ожидания поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3db88-598">If **TRUE**, interval time-outs are supported.</span></span> <span data-ttu-id="3db88-599">Время ожидания — это количество времени, которое может пройти между поступлением каждого фрагмента данных.</span><span class="sxs-lookup"><span data-stu-id="3db88-599">An interval timeout is the amount of time allowed to elapse between the arrival of each piece of data.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-600">**суппортспаритичекк**</span><span class="sxs-lookup"><span data-stu-id="3db88-600">**SupportsParityCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-601">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-601">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-602">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-602">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-603">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ \_ Проверка четности")</span><span class="sxs-lookup"><span data-stu-id="3db88-603">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_PARITY\_CHECK")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-604">Если задано **значение true**, проверка четности поддерживается для этого последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-604">If **TRUE**, parity checking is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-605">**суппортсрлсд**</span><span class="sxs-lookup"><span data-stu-id="3db88-605">**SupportsRLSD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-606">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-606">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-607">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-607">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-608">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ RLSD")</span><span class="sxs-lookup"><span data-stu-id="3db88-608">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RLSD")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-609">Если **значение — true**, в этом последовательном порте поддерживается полученное определение сигнала (RLSD).</span><span class="sxs-lookup"><span data-stu-id="3db88-609">If **TRUE**, Received Line Signal Detect (RLSD) is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-610">**суппортсртсктс**</span><span class="sxs-lookup"><span data-stu-id="3db88-610">**SupportsRTSCTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-611">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-611">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-612">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-612">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-613">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ RTS/CTS")</span><span class="sxs-lookup"><span data-stu-id="3db88-613">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_RTSCTS")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-614">Если задано **значение true**, для этого последовательного порта поддерживаются сигналы RTS и Clear для отправки (CTS).</span><span class="sxs-lookup"><span data-stu-id="3db88-614">If **TRUE**, ready to send (RTS) and clear to send (CTS) signals are supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-615">**суппортсспеЦиалчарактерс**</span><span class="sxs-lookup"><span data-stu-id="3db88-615">**SupportsSpecialCharacters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-616">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-616">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-617">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-617">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-618">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ спеЦиалчарс")</span><span class="sxs-lookup"><span data-stu-id="3db88-618">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SPECIALCHARS")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-619">**Значение true** показывает, что управляющие символы последовательных портов поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="3db88-619">If **TRUE**, serial port control characters are supported.</span></span> <span data-ttu-id="3db88-620">Эти символы обозначают события, а не данные.</span><span class="sxs-lookup"><span data-stu-id="3db88-620">These characters signal events rather than data.</span></span> <span data-ttu-id="3db88-621">Эти символы не воспроизводятся и задаются драйвером.</span><span class="sxs-lookup"><span data-stu-id="3db88-621">These characters are not displayable and are set by the driver.</span></span> <span data-ttu-id="3db88-622">К ним относятся Еофчар, Еррорчар, Бреакчар, Евентчар, Ксончар и Ксоффчар.</span><span class="sxs-lookup"><span data-stu-id="3db88-622">They include EofChar, ErrorChar, BreakChar, EventChar, XonChar, and XoffChar.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-623">**суппортсксонксофф**</span><span class="sxs-lookup"><span data-stu-id="3db88-623">**SupportsXOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-624">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-624">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-625">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-625">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-626">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ ксонксофф")</span><span class="sxs-lookup"><span data-stu-id="3db88-626">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_XONXOFF")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-627">Если **значение true**, управление потоком XON или XOFF поддерживается для этого последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="3db88-627">If **TRUE**, XON or XOFF flow-control is supported on this serial port.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-628">**суппортсксонксоффсет**</span><span class="sxs-lookup"><span data-stu-id="3db88-628">**SupportsXOnXOffSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-629">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3db88-629">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-630">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-630">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-631">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры обмена данными Win32API \| [**коммпроп**](/windows/win32/api/winbase/ns-winbase-commprop) \| двпровкапабилитиес \| PCF \_ сетксчар")</span><span class="sxs-lookup"><span data-stu-id="3db88-631">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop)\|dwProvCapabilities\|PCF\_SETXCHAR")</span></span>
</dt> </dl>

<span data-ttu-id="3db88-632">Если **значение — true**, поставщик услуг связи поддерживает настройку параметра управления ПОТОКОМ ксонор XOFF.</span><span class="sxs-lookup"><span data-stu-id="3db88-632">If **TRUE**, the communications provider supports configuration of the XONor XOFF flow-control setting.</span></span>

</dd> <dt>

<span data-ttu-id="3db88-633">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="3db88-633">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-634">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-635">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-635">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-636">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3db88-636">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3db88-637">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="3db88-637">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="3db88-638">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-638">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-639">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3db88-639">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-640">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3db88-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-641">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3db88-642">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="3db88-642">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="3db88-643">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="3db88-643">Name of the scoping system.</span></span>

<span data-ttu-id="3db88-644">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="3db88-644">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="3db88-645">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="3db88-645">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3db88-646">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3db88-646">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3db88-647">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3db88-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3db88-648">Дата и время последнего сброса этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="3db88-648">Date and time this controller was last reset.</span></span> <span data-ttu-id="3db88-649">Это может означать, что контроллер был выключен или повторно инициализирован.</span><span class="sxs-lookup"><span data-stu-id="3db88-649">This could mean the controller was powered down, or reinitialized.</span></span>

<span data-ttu-id="3db88-650">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-650">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3db88-651">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3db88-651">Remarks</span></span>

<span data-ttu-id="3db88-652">Класс **Win32 \_ SerialPort** является производным от [**CIM \_ сериалконтроллер**](cim-serialcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="3db88-652">The **Win32\_SerialPort** class is derived from [**CIM\_SerialController**](cim-serialcontroller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3db88-653">Примеры</span><span class="sxs-lookup"><span data-stu-id="3db88-653">Examples</span></span>

<span data-ttu-id="3db88-654">Альтернативный способ получения сведений о последовательных портах (из реестра) см. в разделе [Enumerate ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic Sample.</span><span class="sxs-lookup"><span data-stu-id="3db88-654">For an alternate method of retrieving serial port information (from the registry), see the [Enumerate Ports](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic sample.</span></span>

<span data-ttu-id="3db88-655">Пример PowerShell [Свойства последовательного порта](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) возвращает сведения о последовательных портах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3db88-655">The [List Serial Port Properties](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) PowerShell example returns information about the serial ports installed on a computer.</span></span>

<span data-ttu-id="3db88-656">Следующий пример сценария VBScript возвращает сведения о последовательных портах, установленных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="3db88-656">The following VBScript sample returns information about the serial ports installed on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a><span data-ttu-id="3db88-657">Требования</span><span class="sxs-lookup"><span data-stu-id="3db88-657">Requirements</span></span>



| <span data-ttu-id="3db88-658">Требование</span><span class="sxs-lookup"><span data-stu-id="3db88-658">Requirement</span></span> | <span data-ttu-id="3db88-659">Значение</span><span class="sxs-lookup"><span data-stu-id="3db88-659">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3db88-660">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3db88-660">Minimum supported client</span></span><br/> | <span data-ttu-id="3db88-661">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3db88-661">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3db88-662">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3db88-662">Minimum supported server</span></span><br/> | <span data-ttu-id="3db88-663">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3db88-663">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3db88-664">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3db88-664">Namespace</span></span><br/>                | <span data-ttu-id="3db88-665">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3db88-665">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3db88-666">MOF</span><span class="sxs-lookup"><span data-stu-id="3db88-666">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3db88-667"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3db88-667"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3db88-668">DLL</span><span class="sxs-lookup"><span data-stu-id="3db88-668">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3db88-669"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3db88-669"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db88-670">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3db88-670">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db88-671">**\_СЕРИАЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="3db88-671">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dt>

[<span data-ttu-id="3db88-672">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="3db88-672">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
