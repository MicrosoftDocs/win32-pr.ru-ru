---
description: '\_Класс WMI флоппиконтроллер для Win32 представляет возможности и Управление емкостью контроллера гибких дисков.'
ms.assetid: 8c02847c-8329-4adc-b2a5-149b36aead88
ms.tgt_platform: multiple
title: Класс Win32_FloppyController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyController
- Win32_FloppyController.Reset
- Win32_FloppyController.SetPowerState
- Win32_FloppyController.Availability
- Win32_FloppyController.Caption
- Win32_FloppyController.ConfigManagerErrorCode
- Win32_FloppyController.ConfigManagerUserConfig
- Win32_FloppyController.CreationClassName
- Win32_FloppyController.Description
- Win32_FloppyController.DeviceID
- Win32_FloppyController.ErrorCleared
- Win32_FloppyController.ErrorDescription
- Win32_FloppyController.InstallDate
- Win32_FloppyController.LastErrorCode
- Win32_FloppyController.Manufacturer
- Win32_FloppyController.MaxNumberControlled
- Win32_FloppyController.Name
- Win32_FloppyController.PNPDeviceID
- Win32_FloppyController.PowerManagementCapabilities
- Win32_FloppyController.PowerManagementSupported
- Win32_FloppyController.ProtocolSupported
- Win32_FloppyController.Status
- Win32_FloppyController.StatusInfo
- Win32_FloppyController.SystemCreationClassName
- Win32_FloppyController.SystemName
- Win32_FloppyController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7aac44fb8e2b0a91ca3794f234a31cd4c25a4b5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990698"
---
# <a name="win32_floppycontroller-class"></a><span data-ttu-id="d5fb8-103">\_Класс Win32 флоппиконтроллер</span><span class="sxs-lookup"><span data-stu-id="d5fb8-103">Win32\_FloppyController class</span></span>

<span data-ttu-id="d5fb8-104">\[**Win32 \_ Флоппиконтроллер** больше не доступен для использования в Windows 10 и Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="d5fb8-104">\[**Win32\_FloppyController** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="d5fb8-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ флоппиконтроллер для Win32** представляет возможности и Управление емкостью контроллера гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-105">The **Win32\_FloppyController** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a floppy disk drive controller.</span></span>

<span data-ttu-id="d5fb8-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d5fb8-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5fb8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5fb8-108">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{2A7DC003-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyController : CIM_Controller
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
  string   Manufacturer;
  uint32   MaxNumberControlled;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="d5fb8-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d5fb8-109">Members</span></span>

<span data-ttu-id="d5fb8-110">Класс **Win32 \_ флоппиконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5fb8-110">The **Win32\_FloppyController** class has these types of members:</span></span>

-   [<span data-ttu-id="d5fb8-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d5fb8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="d5fb8-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5fb8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d5fb8-113">Методы</span><span class="sxs-lookup"><span data-stu-id="d5fb8-113">Methods</span></span>

<span data-ttu-id="d5fb8-114">Класс **Win32 \_ флоппиконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-114">The **Win32\_FloppyController** class has these methods.</span></span>



| <span data-ttu-id="d5fb8-115">Метод</span><span class="sxs-lookup"><span data-stu-id="d5fb8-115">Method</span></span>            | <span data-ttu-id="d5fb8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d5fb8-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fb8-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-117">**Reset**</span></span>         | <span data-ttu-id="d5fb8-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-118">Not implemented.</span></span> <span data-ttu-id="d5fb8-119">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ Controller**](cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fb8-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="d5fb8-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-120">**SetPowerState**</span></span> | <span data-ttu-id="d5fb8-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-121">Not implemented.</span></span> <span data-ttu-id="d5fb8-122">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ Controller**](cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fb8-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d5fb8-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5fb8-123">Properties</span></span>

<span data-ttu-id="d5fb8-124">Класс **Win32 \_ флоппиконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-124">The **Win32\_FloppyController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5fb8-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-129">Availability and status of the device.</span></span>

<span data-ttu-id="d5fb8-130">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d5fb8-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d5fb8-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d5fb8-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="d5fb8-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d5fb8-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d5fb8-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d5fb8-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d5fb8-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d5fb8-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d5fb8-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d5fb8-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d5fb8-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d5fb8-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d5fb8-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-145">Энергосбережение — неизвестно</span><span class="sxs-lookup"><span data-stu-id="d5fb8-145">Power Save - Unknown</span></span>

<span data-ttu-id="d5fb8-146">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d5fb8-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-148">Энергосбережение — режим низкого энергопотребления</span><span class="sxs-lookup"><span data-stu-id="d5fb8-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="d5fb8-149">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d5fb8-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-151">Энергосбережение — ждущий режим</span><span class="sxs-lookup"><span data-stu-id="d5fb8-151">Power Save - Standby</span></span>

<span data-ttu-id="d5fb8-152">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-152">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d5fb8-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d5fb8-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-155">Энергосбережение — предупреждение</span><span class="sxs-lookup"><span data-stu-id="d5fb8-155">Power Save - Warning</span></span>

<span data-ttu-id="d5fb8-156">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d5fb8-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-158">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d5fb8-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-160">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d5fb8-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-162">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d5fb8-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-164">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d5fb8-165">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-165">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-166">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-168">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-168">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-169">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-169">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d5fb8-170">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-171">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-171">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-174">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-174">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-175">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-175">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d5fb8-176">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-176">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d5fb8-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-177"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="d5fb8-178"> (0)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-178">(0)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-179">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-179">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d5fb8-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-180"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="d5fb8-181">(1)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-181">(1)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-182">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-182">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d5fb8-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-183"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d5fb8-184">(2)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-184">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d5fb8-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-185"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d5fb8-186">(3)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-186">(3)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-187">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-187">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d5fb8-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-188"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d5fb8-189">(4)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-189">(4)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-190">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-190">Device is not working properly.</span></span> <span data-ttu-id="d5fb8-191">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-191">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d5fb8-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-192"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d5fb8-193">(5)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-193">(5)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-194">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-194">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d5fb8-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-195"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d5fb8-196"> (6)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-196">(6)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-197">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-197">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d5fb8-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-198"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="d5fb8-199">(7)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-199">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d5fb8-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-200"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d5fb8-201">(8)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-201">(8)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-202">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-202">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d5fb8-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-203"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d5fb8-204">(9)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-204">(9)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-205">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-205">Device is not working properly.</span></span> <span data-ttu-id="d5fb8-206">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-206">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d5fb8-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-207"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="d5fb8-208">(10)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-208">(10)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-209">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-209">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d5fb8-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-210"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="d5fb8-211">(11)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-211">(11)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-212">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-212">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d5fb8-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-213"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d5fb8-214">(12)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-214">(12)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-215">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-215">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d5fb8-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-216"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d5fb8-217">(13)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-217">(13)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-218">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-218">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d5fb8-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-219"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d5fb8-220">(14)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-220">(14)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-221">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-221">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d5fb8-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-222"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d5fb8-223">(15)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-223">(15)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-224">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-224">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d5fb8-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-225"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d5fb8-226">(16)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-226">(16)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-227">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-227">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d5fb8-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-228"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d5fb8-229">(17)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-229">(17)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-230">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-230">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d5fb8-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-231"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d5fb8-232">(18)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-232">(18)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-233">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-233">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d5fb8-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-234"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="d5fb8-235">(19)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d5fb8-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-236"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="d5fb8-237">(20)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-237">(20)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-238">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-238">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d5fb8-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-239"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d5fb8-240">(21)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-240">(21)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-241">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-241">System failure.</span></span> <span data-ttu-id="d5fb8-242">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-242">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="d5fb8-243">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-243">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d5fb8-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-244"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="d5fb8-245">(22)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-245">(22)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-246">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-246">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d5fb8-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-247"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d5fb8-248">(23)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-248">(23)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-249">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-249">System failure.</span></span> <span data-ttu-id="d5fb8-250">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-250">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d5fb8-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-251"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d5fb8-252">(24)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-252">(24)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-253">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-253">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d5fb8-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d5fb8-255">(25)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-255">(25)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-256">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d5fb8-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-257"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="d5fb8-258">(26)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-258">(26)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-259">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-259">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d5fb8-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-260"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d5fb8-261">(27)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-261">(27)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-262">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-262">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d5fb8-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-263"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d5fb8-264">(28)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-264">(28)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-265">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-265">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d5fb8-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-266"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d5fb8-267">(29)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-267">(29)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-268">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-268">Device is disabled.</span></span> <span data-ttu-id="d5fb8-269">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-269">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d5fb8-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-270"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d5fb8-271">(30)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-271">(30)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-272">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-272">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d5fb8-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-273"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d5fb8-274">1-31</span><span class="sxs-lookup"><span data-stu-id="d5fb8-274">(31)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-275">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-275">Device is not working properly.</span></span> <span data-ttu-id="d5fb8-276">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-276">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d5fb8-277">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-277">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-278">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-278">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-280">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-280">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-281">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-281">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d5fb8-282">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-283">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-283">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-286">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-286">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-287">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-287">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="d5fb8-288">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-288">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="d5fb8-289">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-290">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-290">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-292">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-293">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-293">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-294">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-294">Description of the object.</span></span>

<span data-ttu-id="d5fb8-295">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-296">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-296">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-297">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-299">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-299">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-300">Уникальный идентификатор контроллера флоппи-дисковода.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-300">Unique identifier of the floppy controller.</span></span>

<span data-ttu-id="d5fb8-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-302">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-302">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-303">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-303">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-305">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-305">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="d5fb8-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-307">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-307">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-310">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-310">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="d5fb8-311">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-312">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-312">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-313">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-313">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-315">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-315">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-316">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-316">Date and time the object is installed.</span></span> <span data-ttu-id="d5fb8-317">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-317">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="d5fb8-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-319">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-319">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-320">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-320">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-322">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-322">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d5fb8-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-324">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-324">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-327">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-327">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-328">Имя производителя контроллера флоппи-дисковода.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-328">Name of the floppy controller manufacturer.</span></span>

<span data-ttu-id="d5fb8-329">Пример: "Microsoft"</span><span class="sxs-lookup"><span data-stu-id="d5fb8-329">Example: "Microsoft"</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-330">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-330">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-331">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-331">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-333">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-333">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-334">Максимальное количество напрямую предназначенных для адресации сущностей, поддерживаемых этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-334">Maximum number of directly addressable entities that this controller supports.</span></span> <span data-ttu-id="d5fb8-335">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-335">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="d5fb8-336">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-336">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-337">**Name**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-337">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-340">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-341">Метка для объекта.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-341">Label for the object.</span></span> <span data-ttu-id="d5fb8-342">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-342">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="d5fb8-343">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-343">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-344">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-344">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-347">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-347">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-348">Идентификатор устройства Windows самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-348">Windows Plug and Play device identifier for the logical device.</span></span>

<span data-ttu-id="d5fb8-349">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d5fb8-349">Example: "\*PNP030b"</span></span>

<span data-ttu-id="d5fb8-350">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-351">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-351">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-352">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d5fb8-352">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-354">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-354">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d5fb8-355">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d5fb8-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-356"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d5fb8-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-357"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d5fb8-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-358"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d5fb8-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-359"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-360">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-360">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d5fb8-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-361"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-362">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-362">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d5fb8-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-363"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-364">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fb8-364">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d5fb8-365">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-365">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d5fb8-366">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-366">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d5fb8-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-367"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-368">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d5fb8-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-369"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d5fb8-370">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-370">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d5fb8-371">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-371">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-372">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-372">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-374">Если **значение — true**, устройство может управляться с помощью управления питанием. Это означает, что его можно перевести в режим приостановки и т. д.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-374">If **TRUE**, the device can be power-managed, which means that it can be put into suspend mode, and so on.</span></span> <span data-ttu-id="d5fb8-375">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-375">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="d5fb8-376">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-376">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-377">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-377">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-378">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-378">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-379">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-380">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-380">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-381">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-381">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="d5fb8-382">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-382">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="d5fb8-383">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d5fb8-383">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d5fb8-384">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-384">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d5fb8-385">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-385">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="d5fb8-386">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-386">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="d5fb8-387">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-387">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="d5fb8-388">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-388">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="d5fb8-389">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-389">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="d5fb8-390">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-390">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="d5fb8-391">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-391">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="d5fb8-392">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-392">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="d5fb8-393">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-393">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="d5fb8-394">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-394">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="d5fb8-395">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-395">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="d5fb8-396">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-396">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="d5fb8-397">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-397">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="d5fb8-398">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-398">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="d5fb8-399">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-399">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="d5fb8-400">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-400">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="d5fb8-401">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-401">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="d5fb8-402">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-402">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="d5fb8-403">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-403">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="d5fb8-404">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-404">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="d5fb8-405">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-405">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="d5fb8-406">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-406">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="d5fb8-407">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-407">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="d5fb8-408">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-408">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="d5fb8-409">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-409">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="d5fb8-410">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-410">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="d5fb8-411">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-411">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="d5fb8-412">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-412">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="d5fb8-413">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-413">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="d5fb8-414">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-414">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="d5fb8-415">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-415">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="d5fb8-416">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-416">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="d5fb8-417">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-417">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="d5fb8-418">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-418">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="d5fb8-419">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-419">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="d5fb8-420">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-420">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="d5fb8-421">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-421">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="d5fb8-422">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-422">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="d5fb8-423">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-423">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="d5fb8-424">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-424">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="d5fb8-425">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-425">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="d5fb8-426">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-426">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="d5fb8-427">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-427">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="d5fb8-428">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-428">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="d5fb8-429">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-429">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="d5fb8-430">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-430">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d5fb8-431">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-431">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-432">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-434">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-434">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-435">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-435">Current status of the object.</span></span> <span data-ttu-id="d5fb8-436">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-436">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d5fb8-437">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-437">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d5fb8-438">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="d5fb8-438">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d5fb8-439">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-439">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d5fb8-440">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-440">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d5fb8-441">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-441">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d5fb8-442">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="d5fb8-442">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d5fb8-443">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-443">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d5fb8-444">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-444">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d5fb8-445">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-445">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d5fb8-446">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-446">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d5fb8-447">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-447">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d5fb8-448">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-448">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d5fb8-449">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-449">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d5fb8-450">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-450">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d5fb8-451">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-451">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d5fb8-452">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-452">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d5fb8-453">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-453">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d5fb8-454">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-454">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d5fb8-455">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-455">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-456">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-458">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d5fb8-458">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-459">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-459">State of the logical device.</span></span> <span data-ttu-id="d5fb8-460">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-460">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="d5fb8-461">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-461">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d5fb8-462">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-462">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d5fb8-463">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-463">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d5fb8-464">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-464">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d5fb8-465">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-465">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d5fb8-466">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-466">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d5fb8-467">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-467">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-468">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-469">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-470">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-470">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-471">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-471">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="d5fb8-472">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-472">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-473">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-473">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-476">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-477">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-477">Name of the scoping system.</span></span>

<span data-ttu-id="d5fb8-478">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5fb8-479">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-479">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5fb8-480">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-480">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d5fb8-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5fb8-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d5fb8-482">Дата и время последнего сброса контроллера.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-482">Date and time the controller was last reset.</span></span> <span data-ttu-id="d5fb8-483">Это может означать, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="d5fb8-483">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="d5fb8-484">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="d5fb8-484">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5fb8-485">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5fb8-485">Remarks</span></span>

<span data-ttu-id="d5fb8-486">Класс **Win32 \_ флоппиконтроллер** является производным от [**\_ контроллера CIM**](cim-controller.md) , который является производным от CIM-класса. [**\_**](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="d5fb8-486">The **Win32\_FloppyController** class is derived from [**CIM\_Controller**](cim-controller.md) which derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5fb8-487">Требования</span><span class="sxs-lookup"><span data-stu-id="d5fb8-487">Requirements</span></span>



| <span data-ttu-id="d5fb8-488">Требование</span><span class="sxs-lookup"><span data-stu-id="d5fb8-488">Requirement</span></span> | <span data-ttu-id="d5fb8-489">Значение</span><span class="sxs-lookup"><span data-stu-id="d5fb8-489">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5fb8-490">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5fb8-490">Minimum supported client</span></span><br/> | <span data-ttu-id="d5fb8-491">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5fb8-491">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5fb8-492">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5fb8-492">Minimum supported server</span></span><br/> | <span data-ttu-id="d5fb8-493">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5fb8-493">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5fb8-494">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d5fb8-494">End of client support</span></span><br/>    | <span data-ttu-id="d5fb8-495">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d5fb8-495">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="d5fb8-496">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="d5fb8-496">End of server support</span></span><br/>    | <span data-ttu-id="d5fb8-497">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d5fb8-497">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="d5fb8-498">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d5fb8-498">Namespace</span></span><br/>                | <span data-ttu-id="d5fb8-499">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d5fb8-499">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5fb8-500">MOF</span><span class="sxs-lookup"><span data-stu-id="d5fb8-500">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5fb8-501"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5fb8-501"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5fb8-502">DLL</span><span class="sxs-lookup"><span data-stu-id="d5fb8-502">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5fb8-503"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5fb8-503"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5fb8-504">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5fb8-504">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5fb8-505">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="d5fb8-505">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="d5fb8-506">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="d5fb8-506">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

