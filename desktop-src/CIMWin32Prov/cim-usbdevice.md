---
description: Класс CIM \_ усбдевице представляет характеристики управления USB-устройства.
ms.assetid: 0ff39701-826a-434b-a628-0af586600a80
ms.tgt_platform: multiple
title: Класс CIM_USBDevice (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.Availability
- CIM_USBDevice.Caption
- CIM_USBDevice.ClassCode
- CIM_USBDevice.ConfigManagerErrorCode
- CIM_USBDevice.ConfigManagerUserConfig
- CIM_USBDevice.CreationClassName
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.Description
- CIM_USBDevice.DeviceID
- CIM_USBDevice.ErrorCleared
- CIM_USBDevice.ErrorDescription
- CIM_USBDevice.InstallDate
- CIM_USBDevice.LastErrorCode
- CIM_USBDevice.Name
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.PNPDeviceID
- CIM_USBDevice.PowerManagementCapabilities
- CIM_USBDevice.PowerManagementSupported
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.Status
- CIM_USBDevice.StatusInfo
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.SystemCreationClassName
- CIM_USBDevice.SystemName
- CIM_USBDevice.USBVersion
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 21b927980716d4ee7ee2e22a352c5c3b34b363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140867"
---
# <a name="cim_usbdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="b30d2-103">Класс CIM_USBDevice (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b30d2-103">CIM_USBDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b30d2-104">Класс **CIM \_ усбдевице** представляет характеристики управления USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-104">The **CIM\_USBDevice** class represents the management characteristics of a USB device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b30d2-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b30d2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b30d2-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b30d2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b30d2-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b30d2-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b30d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30d2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b30d2-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   Availability;
  string   Caption;
  uint8    ClassCode;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint8    CurrentAlternateSettings[];
  uint8    CurrentConfigValue;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint8    NumberOfConfigs;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    ProtocolCode;
  string   Status;
  uint16   StatusInfo;
  uint8    SubclassCode;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   USBVersion;
};
```

## <a name="members"></a><span data-ttu-id="b30d2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b30d2-110">Members</span></span>

<span data-ttu-id="b30d2-111">Класс **CIM \_ усбдевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b30d2-111">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="b30d2-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b30d2-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b30d2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b30d2-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b30d2-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b30d2-114">Methods</span></span>

<span data-ttu-id="b30d2-115">Класс **CIM \_ усбдевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b30d2-115">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="b30d2-116">Метод</span><span class="sxs-lookup"><span data-stu-id="b30d2-116">Method</span></span>                                                               | <span data-ttu-id="b30d2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b30d2-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b30d2-118">**Двухбайтовый**</span><span class="sxs-lookup"><span data-stu-id="b30d2-118">**GetDescriptor**</span></span>](getdescriptor-method-in-class-cim-usbdevice.md) | <span data-ttu-id="b30d2-119">Возвращает дескриптор USB-устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-119">Returns the USB device descriptor.</span></span> <span data-ttu-id="b30d2-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b30d2-120">Not implemented by WMI.</span></span><br/>                                                                    |
| [<span data-ttu-id="b30d2-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b30d2-121">**Reset**</span></span>](reset-method-in-class-cim-usbdevice.md)                 | <span data-ttu-id="b30d2-122">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-122">Requests a reset of the logical device.</span></span> <span data-ttu-id="b30d2-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b30d2-123">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b30d2-124">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b30d2-124">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-usbdevice.md) | <span data-ttu-id="b30d2-125">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="b30d2-125">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b30d2-126">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b30d2-126">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b30d2-127">Свойства</span><span class="sxs-lookup"><span data-stu-id="b30d2-127">Properties</span></span>

<span data-ttu-id="b30d2-128">Класс **CIM \_ усбдевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-128">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b30d2-129">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b30d2-129">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-130">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b30d2-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-132">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b30d2-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-133">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-133">Availability and status of the device.</span></span>

<span data-ttu-id="b30d2-134">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-134">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b30d2-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b30d2-135"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b30d2-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b30d2-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b30d2-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b30d2-137"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-138">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="b30d2-138">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b30d2-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b30d2-139"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b30d2-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b30d2-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b30d2-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b30d2-141"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b30d2-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b30d2-142"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b30d2-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b30d2-143"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b30d2-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b30d2-144"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b30d2-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b30d2-145"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b30d2-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b30d2-146"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b30d2-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b30d2-147"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b30d2-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b30d2-148"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-149">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b30d2-149">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b30d2-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b30d2-150"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-151">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b30d2-151">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b30d2-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b30d2-152"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-153">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b30d2-153">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b30d2-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b30d2-154"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b30d2-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b30d2-155"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-156">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b30d2-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b30d2-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b30d2-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-158">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b30d2-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b30d2-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b30d2-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-160">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b30d2-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b30d2-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b30d2-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-162">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b30d2-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b30d2-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b30d2-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-164">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b30d2-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b30d2-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b30d2-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-168">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b30d2-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-169">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b30d2-169">Short textual description of the object.</span></span>

<span data-ttu-id="b30d2-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b30d2-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-171">**класскоде**</span><span class="sxs-lookup"><span data-stu-id="b30d2-171">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-172">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b30d2-172">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-174">Код класса USB.</span><span class="sxs-lookup"><span data-stu-id="b30d2-174">USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-175">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b30d2-175">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-176">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b30d2-176">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-178">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b30d2-178">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-179">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b30d2-179">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="b30d2-180">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-180">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b30d2-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-181"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b30d2-182"> (0)</span><span class="sxs-lookup"><span data-stu-id="b30d2-182">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-183">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b30d2-183">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b30d2-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-184"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b30d2-185">(1)</span><span class="sxs-lookup"><span data-stu-id="b30d2-185">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-186">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b30d2-186">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b30d2-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-187"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b30d2-188">(2)</span><span class="sxs-lookup"><span data-stu-id="b30d2-188">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b30d2-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-189"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b30d2-190">(3)</span><span class="sxs-lookup"><span data-stu-id="b30d2-190">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-191">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b30d2-191">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b30d2-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-192"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b30d2-193">(4)</span><span class="sxs-lookup"><span data-stu-id="b30d2-193">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-194">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b30d2-194">Device is not working properly.</span></span> <span data-ttu-id="b30d2-195">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b30d2-195">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b30d2-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-196"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b30d2-197">(5)</span><span class="sxs-lookup"><span data-stu-id="b30d2-197">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-198">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b30d2-198">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b30d2-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-199"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b30d2-200"> (6)</span><span class="sxs-lookup"><span data-stu-id="b30d2-200">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-201">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b30d2-201">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b30d2-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-202"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b30d2-203">(7)</span><span class="sxs-lookup"><span data-stu-id="b30d2-203">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b30d2-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-204"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b30d2-205">(8)</span><span class="sxs-lookup"><span data-stu-id="b30d2-205">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-206">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-206">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b30d2-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-207"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b30d2-208">(9)</span><span class="sxs-lookup"><span data-stu-id="b30d2-208">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-209">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b30d2-209">Device is not working properly.</span></span> <span data-ttu-id="b30d2-210">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-210">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b30d2-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-211"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b30d2-212">(10)</span><span class="sxs-lookup"><span data-stu-id="b30d2-212">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-213">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b30d2-213">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b30d2-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-214"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b30d2-215">(11)</span><span class="sxs-lookup"><span data-stu-id="b30d2-215">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-216">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-216">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b30d2-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-217"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b30d2-218">(12)</span><span class="sxs-lookup"><span data-stu-id="b30d2-218">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-219">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b30d2-219">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b30d2-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-220"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b30d2-221">(13)</span><span class="sxs-lookup"><span data-stu-id="b30d2-221">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-222">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-222">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b30d2-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-223"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b30d2-224">(14)</span><span class="sxs-lookup"><span data-stu-id="b30d2-224">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-225">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b30d2-225">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b30d2-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-226"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b30d2-227">(15)</span><span class="sxs-lookup"><span data-stu-id="b30d2-227">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-228">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b30d2-228">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b30d2-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-229"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b30d2-230">(16)</span><span class="sxs-lookup"><span data-stu-id="b30d2-230">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-231">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b30d2-231">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b30d2-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-232"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b30d2-233">(17)</span><span class="sxs-lookup"><span data-stu-id="b30d2-233">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-234">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b30d2-234">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b30d2-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-235"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b30d2-236">(18)</span><span class="sxs-lookup"><span data-stu-id="b30d2-236">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-237">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b30d2-237">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b30d2-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-238"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b30d2-239">(19)</span><span class="sxs-lookup"><span data-stu-id="b30d2-239">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b30d2-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-240"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b30d2-241">(20)</span><span class="sxs-lookup"><span data-stu-id="b30d2-241">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-242">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b30d2-242">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b30d2-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b30d2-244">(21)</span><span class="sxs-lookup"><span data-stu-id="b30d2-244">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b30d2-245">System failure.</span></span> <span data-ttu-id="b30d2-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b30d2-246">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b30d2-247">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b30d2-247">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b30d2-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-248"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b30d2-249">(22)</span><span class="sxs-lookup"><span data-stu-id="b30d2-249">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-250">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b30d2-250">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b30d2-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-251"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b30d2-252">(23)</span><span class="sxs-lookup"><span data-stu-id="b30d2-252">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-253">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b30d2-253">System failure.</span></span> <span data-ttu-id="b30d2-254">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b30d2-254">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b30d2-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-255"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b30d2-256">(24)</span><span class="sxs-lookup"><span data-stu-id="b30d2-256">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-257">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b30d2-257">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b30d2-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-258"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b30d2-259">(25)</span><span class="sxs-lookup"><span data-stu-id="b30d2-259">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-260">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b30d2-260">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b30d2-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-261"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b30d2-262">(26)</span><span class="sxs-lookup"><span data-stu-id="b30d2-262">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-263">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b30d2-263">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b30d2-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-264"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b30d2-265">(27)</span><span class="sxs-lookup"><span data-stu-id="b30d2-265">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-266">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b30d2-266">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b30d2-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-267"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b30d2-268">(28)</span><span class="sxs-lookup"><span data-stu-id="b30d2-268">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-269">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b30d2-269">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b30d2-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-270"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b30d2-271">(29)</span><span class="sxs-lookup"><span data-stu-id="b30d2-271">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-272">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b30d2-272">Device is disabled.</span></span> <span data-ttu-id="b30d2-273">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b30d2-273">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b30d2-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-274"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b30d2-275">(30)</span><span class="sxs-lookup"><span data-stu-id="b30d2-275">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-276">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b30d2-276">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b30d2-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b30d2-277"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b30d2-278">1-31</span><span class="sxs-lookup"><span data-stu-id="b30d2-278">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-279">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b30d2-279">Device is not working properly.</span></span> <span data-ttu-id="b30d2-280">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b30d2-280">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b30d2-281">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b30d2-281">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-282">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b30d2-282">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-284">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b30d2-284">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-285">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b30d2-285">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b30d2-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-287">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b30d2-287">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-290">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b30d2-290">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-291">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b30d2-291">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b30d2-292">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b30d2-292">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b30d2-293">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-293">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-294">**курренталтернатесеттингс**</span><span class="sxs-lookup"><span data-stu-id="b30d2-294">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-295">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b30d2-295">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-297">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ усбдевице**.**Куррентконфигвалуе**")</span><span class="sxs-lookup"><span data-stu-id="b30d2-297">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-298">Альтернативные параметры USB для каждого интерфейса в текущей выбранной конфигурации (указывается свойством **куррентконфигвалуе** ).</span><span class="sxs-lookup"><span data-stu-id="b30d2-298">USB alternate settings for each interface in the currently selected configuration (indicated by the **CurrentConfigValue** property).</span></span> <span data-ttu-id="b30d2-299">Этот массив содержит одну запись для каждого интерфейса в конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b30d2-299">This array has one entry for each interface in the configuration.</span></span> <span data-ttu-id="b30d2-300">Если свойство **куррентконфигвалуе** имеет значение 0 (ноль), которое указывает, что устройство не настроено, массив не определен.</span><span class="sxs-lookup"><span data-stu-id="b30d2-300">If the **CurrentConfigValue** property has a value of 0 (zero), which indicates that the device is not configured, the array is undefined.</span></span> <span data-ttu-id="b30d2-301">Дополнительные сведения о синтаксическом анализе этой строки октета см. в спецификации USB.</span><span class="sxs-lookup"><span data-stu-id="b30d2-301">For more information about parsing this octet string, see the USB specification.</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-302">**куррентконфигвалуе**</span><span class="sxs-lookup"><span data-stu-id="b30d2-302">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-303">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b30d2-303">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-305">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ усбдевице**.**Курренталтернатесеттингс**")</span><span class="sxs-lookup"><span data-stu-id="b30d2-305">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-306">Конфигурация, выбранная в настоящее время для устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-306">Configuration currently selected for the device.</span></span> <span data-ttu-id="b30d2-307">Если значение равно 0 (нулю), устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b30d2-307">If the value is 0 (zero), the device is unconfigured.</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-308">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b30d2-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-311">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b30d2-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-312">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b30d2-312">Textual description of the object.</span></span>

<span data-ttu-id="b30d2-313">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b30d2-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b30d2-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-317">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b30d2-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-318">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b30d2-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-320">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b30d2-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-321">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b30d2-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-323">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b30d2-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b30d2-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b30d2-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-328">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b30d2-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b30d2-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-330">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b30d2-330">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-331">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b30d2-331">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-333">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b30d2-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-334">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b30d2-334">Date and time the object was installed.</span></span> <span data-ttu-id="b30d2-335">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b30d2-335">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b30d2-336">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b30d2-336">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-337">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b30d2-337">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-338">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b30d2-338">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-340">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b30d2-340">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b30d2-341">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-342">**Name**</span><span class="sxs-lookup"><span data-stu-id="b30d2-342">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-343">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-345">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b30d2-345">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-346">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b30d2-346">Label by which the object is known.</span></span> <span data-ttu-id="b30d2-347">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b30d2-347">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b30d2-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b30d2-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-349">**нумберофконфигс**</span><span class="sxs-lookup"><span data-stu-id="b30d2-349">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-350">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b30d2-350">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-352">Количество конфигураций устройств, определенных для устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-352">Number of device configurations that are defined for the device.</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-353">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b30d2-353">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-356">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b30d2-356">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-357">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-357">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b30d2-358">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b30d2-359">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b30d2-359">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-360">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b30d2-360">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-361">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b30d2-361">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-363">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b30d2-363">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b30d2-364">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-364">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b30d2-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b30d2-365"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b30d2-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b30d2-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b30d2-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b30d2-367"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b30d2-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b30d2-368"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-369">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b30d2-369">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b30d2-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b30d2-370"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-371">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b30d2-371">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b30d2-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b30d2-372"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-373">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b30d2-373">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b30d2-374">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b30d2-374">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b30d2-375">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b30d2-375">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b30d2-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b30d2-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-377">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b30d2-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b30d2-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b30d2-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b30d2-379">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b30d2-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b30d2-380">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b30d2-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-381">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b30d2-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-383">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b30d2-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b30d2-384">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b30d2-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b30d2-385">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b30d2-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b30d2-386">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b30d2-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b30d2-387">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-388">**протоколкоде**</span><span class="sxs-lookup"><span data-stu-id="b30d2-388">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-389">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b30d2-389">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-391">Код протокола USB.</span><span class="sxs-lookup"><span data-stu-id="b30d2-391">USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-392">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b30d2-392">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-393">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-395">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b30d2-395">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-396">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b30d2-396">Current status of the object.</span></span> <span data-ttu-id="b30d2-397">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b30d2-397">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b30d2-398">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b30d2-398">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b30d2-399">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b30d2-399">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b30d2-400">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b30d2-400">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b30d2-401">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b30d2-401">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b30d2-402">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b30d2-402">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b30d2-403">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b30d2-403">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b30d2-404">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b30d2-404">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b30d2-405">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b30d2-405">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b30d2-406">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b30d2-406">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b30d2-407">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b30d2-407">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b30d2-408">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b30d2-408">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b30d2-409">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b30d2-409">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b30d2-410">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b30d2-410">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b30d2-411">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b30d2-411">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-412">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b30d2-412">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-414">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b30d2-414">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-415">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b30d2-415">State of the logical device.</span></span> <span data-ttu-id="b30d2-416">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b30d2-416">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b30d2-417">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-417">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b30d2-418">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b30d2-418">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b30d2-419">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b30d2-419">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b30d2-420">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b30d2-420">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b30d2-421">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b30d2-421">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b30d2-422">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b30d2-422">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b30d2-423">**субкласскоде**</span><span class="sxs-lookup"><span data-stu-id="b30d2-423">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-424">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="b30d2-424">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-426">Код подкласса USB.</span><span class="sxs-lookup"><span data-stu-id="b30d2-426">USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-427">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b30d2-427">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-428">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-430">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b30d2-430">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-431">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b30d2-431">Scoping system's creation class name.</span></span>

<span data-ttu-id="b30d2-432">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-432">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-433">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b30d2-433">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b30d2-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-436">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b30d2-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-437">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b30d2-437">Scoping system's name.</span></span>

<span data-ttu-id="b30d2-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b30d2-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b30d2-439">**усбверсион**</span><span class="sxs-lookup"><span data-stu-id="b30d2-439">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b30d2-440">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b30d2-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b30d2-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b30d2-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b30d2-442">Последняя версия USB, поддерживаемая USB-устройством.</span><span class="sxs-lookup"><span data-stu-id="b30d2-442">Latest USB version supported by the USB device.</span></span> <span data-ttu-id="b30d2-443">Это свойство выражается в виде двоичного десятичного числа (BCD), где между второй и третьей цифрами подразумевается десятичная точка.</span><span class="sxs-lookup"><span data-stu-id="b30d2-443">This property is expressed as a binary-coded decimal (BCD) where a decimal point is implied between the second and third digits.</span></span> <span data-ttu-id="b30d2-444">Например, значение 0x201 указывает, что поддерживается версия 2,01.</span><span class="sxs-lookup"><span data-stu-id="b30d2-444">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b30d2-445">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b30d2-445">Remarks</span></span>

<span data-ttu-id="b30d2-446">Класс **CIM \_ усбдевице** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="b30d2-446">The **CIM\_USBDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b30d2-447">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b30d2-447">WMI does not implement this class.</span></span> <span data-ttu-id="b30d2-448">Классы WMI, реализующие **CIM \_ усбдевице**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b30d2-448">For WMI classes that implement **CIM\_USBDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b30d2-449">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b30d2-449">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b30d2-450">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b30d2-450">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b30d2-451">Требования</span><span class="sxs-lookup"><span data-stu-id="b30d2-451">Requirements</span></span>



| <span data-ttu-id="b30d2-452">Требование</span><span class="sxs-lookup"><span data-stu-id="b30d2-452">Requirement</span></span> | <span data-ttu-id="b30d2-453">Значение</span><span class="sxs-lookup"><span data-stu-id="b30d2-453">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b30d2-454">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b30d2-454">Minimum supported client</span></span><br/> | <span data-ttu-id="b30d2-455">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b30d2-455">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b30d2-456">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b30d2-456">Minimum supported server</span></span><br/> | <span data-ttu-id="b30d2-457">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b30d2-457">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b30d2-458">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b30d2-458">Namespace</span></span><br/>                | <span data-ttu-id="b30d2-459">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b30d2-459">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b30d2-460">MOF</span><span class="sxs-lookup"><span data-stu-id="b30d2-460">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b30d2-461"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b30d2-461"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b30d2-462">DLL</span><span class="sxs-lookup"><span data-stu-id="b30d2-462">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b30d2-463"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b30d2-463"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b30d2-464">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b30d2-464">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30d2-465">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="b30d2-465">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

