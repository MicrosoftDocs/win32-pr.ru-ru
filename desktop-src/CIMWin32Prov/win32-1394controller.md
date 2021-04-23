---
description: Представляет возможности и Управление контроллером 1394.
ms.assetid: 5297b1d1-65b5-4bb7-add4-9dc07b4ddc6c
ms.tgt_platform: multiple
title: Класс Win32_1394Controller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394Controller
- Win32_1394Controller.Reset
- Win32_1394Controller.SetPowerState
- Win32_1394Controller.Availability
- Win32_1394Controller.Caption
- Win32_1394Controller.ConfigManagerErrorCode
- Win32_1394Controller.ConfigManagerUserConfig
- Win32_1394Controller.CreationClassName
- Win32_1394Controller.Description
- Win32_1394Controller.DeviceID
- Win32_1394Controller.ErrorCleared
- Win32_1394Controller.ErrorDescription
- Win32_1394Controller.InstallDate
- Win32_1394Controller.LastErrorCode
- Win32_1394Controller.Manufacturer
- Win32_1394Controller.MaxNumberControlled
- Win32_1394Controller.Name
- Win32_1394Controller.PNPDeviceID
- Win32_1394Controller.PowerManagementCapabilities
- Win32_1394Controller.PowerManagementSupported
- Win32_1394Controller.ProtocolSupported
- Win32_1394Controller.Status
- Win32_1394Controller.StatusInfo
- Win32_1394Controller.SystemCreationClassName
- Win32_1394Controller.SystemName
- Win32_1394Controller.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c788469e258a79e70bcc8311c26b43e1f24c26e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990735"
---
# <a name="win32_1394controller-class"></a><span data-ttu-id="4151e-103">\_Класс Win32 1394Controller</span><span class="sxs-lookup"><span data-stu-id="4151e-103">Win32\_1394Controller class</span></span>

<span data-ttu-id="4151e-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ 1394Controller для Win32** представляет возможности и Управление контроллером 1394.</span><span class="sxs-lookup"><span data-stu-id="4151e-104">The **Win32\_1394Controller** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management of a 1394 controller.</span></span> <span data-ttu-id="4151e-105">IEEE 1394 — спецификация высокоскоростной последовательной шины.</span><span class="sxs-lookup"><span data-stu-id="4151e-105">IEEE 1394 is a specification for a high-speed serial bus.</span></span>

<span data-ttu-id="4151e-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4151e-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4151e-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4151e-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4151e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4151e-108">Syntax</span></span>

``` syntax
[dynamic, provider("CIMWin32"), UUID("{2A7DC003-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394Controller : CIM_Controller
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

## <a name="members"></a><span data-ttu-id="4151e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="4151e-109">Members</span></span>

<span data-ttu-id="4151e-110">Класс **Win32 \_ 1394Controller** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4151e-110">The **Win32\_1394Controller** class has these types of members:</span></span>

-   [<span data-ttu-id="4151e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="4151e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4151e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4151e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4151e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4151e-113">Methods</span></span>

<span data-ttu-id="4151e-114">Класс **Win32 \_ 1394Controller** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4151e-114">The **Win32\_1394Controller** class has these methods.</span></span>



| <span data-ttu-id="4151e-115">Метод</span><span class="sxs-lookup"><span data-stu-id="4151e-115">Method</span></span>            | <span data-ttu-id="4151e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4151e-116">Description</span></span>                                                                                                                                                                                                |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4151e-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="4151e-117">**Reset**</span></span>         | <span data-ttu-id="4151e-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="4151e-118">Not implemented.</span></span> <span data-ttu-id="4151e-119">Чтобы реализовать этот метод, см. документацию по методу [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ Controller**](cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="4151e-119">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/>                 |
| <span data-ttu-id="4151e-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4151e-120">**SetPowerState**</span></span> | <span data-ttu-id="4151e-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="4151e-121">Not implemented.</span></span> <span data-ttu-id="4151e-122">Чтобы реализовать этот метод, см. документацию по методу [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ Controller**](cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="4151e-122">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Controller**](cim-controller.md) for documentation.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4151e-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="4151e-123">Properties</span></span>

<span data-ttu-id="4151e-124">Класс **Win32 \_ 1394Controller** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4151e-124">The **Win32\_1394Controller** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4151e-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="4151e-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4151e-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="4151e-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-129">Availability and status of the device.</span></span>

<span data-ttu-id="4151e-130">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4151e-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4151e-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4151e-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="4151e-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="4151e-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="4151e-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="4151e-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="4151e-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="4151e-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="4151e-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="4151e-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4151e-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="4151e-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="4151e-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="4151e-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="4151e-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="4151e-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="4151e-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="4151e-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4151e-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="4151e-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="4151e-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="4151e-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="4151e-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="4151e-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="4151e-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="4151e-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="4151e-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="4151e-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="4151e-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="4151e-147">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="4151e-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="4151e-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="4151e-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="4151e-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="4151e-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="4151e-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="4151e-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="4151e-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="4151e-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="4151e-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="4151e-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="4151e-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="4151e-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="4151e-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="4151e-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="4151e-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="4151e-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="4151e-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="4151e-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="4151e-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4151e-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="4151e-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-164">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="4151e-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-165">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4151e-165">Short description of the object.</span></span>

<span data-ttu-id="4151e-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-167">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="4151e-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4151e-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-170">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4151e-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-171">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="4151e-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="4151e-172">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="4151e-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="4151e-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="4151e-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="4151e-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-175">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="4151e-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="4151e-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="4151e-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="4151e-177">(1)</span><span class="sxs-lookup"><span data-stu-id="4151e-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-178">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="4151e-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4151e-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="4151e-180">(2)</span><span class="sxs-lookup"><span data-stu-id="4151e-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="4151e-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="4151e-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="4151e-182">(3)</span><span class="sxs-lookup"><span data-stu-id="4151e-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-183">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4151e-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4151e-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="4151e-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="4151e-185">(4)</span><span class="sxs-lookup"><span data-stu-id="4151e-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-186">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="4151e-186">Device is not working properly.</span></span> <span data-ttu-id="4151e-187">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="4151e-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="4151e-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="4151e-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="4151e-189">(5)</span><span class="sxs-lookup"><span data-stu-id="4151e-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-190">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="4151e-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="4151e-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="4151e-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="4151e-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="4151e-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-193">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="4151e-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="4151e-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="4151e-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="4151e-195">(7)</span><span class="sxs-lookup"><span data-stu-id="4151e-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="4151e-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="4151e-197">(8)</span><span class="sxs-lookup"><span data-stu-id="4151e-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-198">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="4151e-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="4151e-200">(9)</span><span class="sxs-lookup"><span data-stu-id="4151e-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-201">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="4151e-201">Device is not working properly.</span></span> <span data-ttu-id="4151e-202">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="4151e-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="4151e-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="4151e-204">(10)</span><span class="sxs-lookup"><span data-stu-id="4151e-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-205">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="4151e-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="4151e-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="4151e-207">(11)</span><span class="sxs-lookup"><span data-stu-id="4151e-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-208">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="4151e-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="4151e-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="4151e-210">(12)</span><span class="sxs-lookup"><span data-stu-id="4151e-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-211">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="4151e-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="4151e-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="4151e-213">(13)</span><span class="sxs-lookup"><span data-stu-id="4151e-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-214">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="4151e-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="4151e-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="4151e-216">(14)</span><span class="sxs-lookup"><span data-stu-id="4151e-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-217">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="4151e-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="4151e-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="4151e-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="4151e-219">(15)</span><span class="sxs-lookup"><span data-stu-id="4151e-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-220">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="4151e-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="4151e-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="4151e-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="4151e-222">(16)</span><span class="sxs-lookup"><span data-stu-id="4151e-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-223">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="4151e-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="4151e-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="4151e-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="4151e-225">(17)</span><span class="sxs-lookup"><span data-stu-id="4151e-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-226">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="4151e-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4151e-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="4151e-228">(18)</span><span class="sxs-lookup"><span data-stu-id="4151e-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-229">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="4151e-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="4151e-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="4151e-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="4151e-231">(19)</span><span class="sxs-lookup"><span data-stu-id="4151e-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="4151e-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="4151e-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="4151e-233">(20)</span><span class="sxs-lookup"><span data-stu-id="4151e-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-234">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="4151e-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="4151e-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="4151e-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="4151e-236">(21)</span><span class="sxs-lookup"><span data-stu-id="4151e-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-237">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="4151e-237">System failure.</span></span> <span data-ttu-id="4151e-238">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="4151e-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="4151e-239">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="4151e-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="4151e-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="4151e-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="4151e-241">(22)</span><span class="sxs-lookup"><span data-stu-id="4151e-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-242">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="4151e-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="4151e-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="4151e-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="4151e-244">(23)</span><span class="sxs-lookup"><span data-stu-id="4151e-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="4151e-245">System failure.</span></span> <span data-ttu-id="4151e-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="4151e-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="4151e-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="4151e-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="4151e-248">(24)</span><span class="sxs-lookup"><span data-stu-id="4151e-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-249">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="4151e-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4151e-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="4151e-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4151e-251">(25)</span><span class="sxs-lookup"><span data-stu-id="4151e-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-252">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="4151e-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="4151e-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="4151e-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="4151e-254">(26)</span><span class="sxs-lookup"><span data-stu-id="4151e-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-255">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="4151e-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="4151e-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="4151e-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="4151e-257">(27)</span><span class="sxs-lookup"><span data-stu-id="4151e-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-258">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="4151e-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="4151e-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="4151e-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="4151e-260">(28)</span><span class="sxs-lookup"><span data-stu-id="4151e-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-261">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="4151e-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="4151e-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="4151e-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="4151e-263">(29)</span><span class="sxs-lookup"><span data-stu-id="4151e-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-264">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="4151e-264">Device is disabled.</span></span> <span data-ttu-id="4151e-265">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="4151e-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="4151e-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="4151e-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="4151e-267">(30)</span><span class="sxs-lookup"><span data-stu-id="4151e-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-268">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="4151e-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="4151e-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="4151e-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="4151e-270">1-31</span><span class="sxs-lookup"><span data-stu-id="4151e-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-271">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="4151e-271">Device is not working properly.</span></span> <span data-ttu-id="4151e-272">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="4151e-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4151e-273">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="4151e-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4151e-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-276">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4151e-276">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-277">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="4151e-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="4151e-278">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4151e-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-282">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4151e-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4151e-283">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4151e-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="4151e-284">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="4151e-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="4151e-285">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-286">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4151e-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-289">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="4151e-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-290">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4151e-290">Description of the object.</span></span>

<span data-ttu-id="4151e-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="4151e-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-295">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="4151e-295">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-296">Уникальный идентификатор этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="4151e-296">Unique identifier of this controller.</span></span>

<span data-ttu-id="4151e-297">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-298">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="4151e-298">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-299">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4151e-299">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4151e-301">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="4151e-301">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="4151e-302">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-303">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="4151e-303">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4151e-306">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="4151e-306">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="4151e-307">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4151e-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-309">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4151e-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-311">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="4151e-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-312">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="4151e-312">Date and time the object was installed.</span></span> <span data-ttu-id="4151e-313">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="4151e-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="4151e-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-315">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="4151e-315">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-316">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4151e-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4151e-318">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="4151e-318">Last error code reported by the logical device.</span></span>

<span data-ttu-id="4151e-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-320">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="4151e-320">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-323">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="4151e-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-324">Изготовитель контроллера.</span><span class="sxs-lookup"><span data-stu-id="4151e-324">Manufacturer of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="4151e-325">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="4151e-325">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-326">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4151e-326">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-328">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="4151e-328">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-329">Максимальное число напрямую предоставляемых сущностей, которые поддерживаются этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="4151e-329">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="4151e-330">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="4151e-330">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="4151e-331">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-331">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-332">**Name**</span><span class="sxs-lookup"><span data-stu-id="4151e-332">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-335">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="4151e-335">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-336">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="4151e-336">Label by which the object is known.</span></span> <span data-ttu-id="4151e-337">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="4151e-337">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="4151e-338">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-339">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="4151e-339">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-342">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="4151e-342">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-343">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-343">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="4151e-344">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-344">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="4151e-345">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="4151e-345">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="4151e-346">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="4151e-346">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-347">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4151e-347">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4151e-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4151e-349">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="4151e-349">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="4151e-350">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-350">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4151e-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4151e-351"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4151e-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="4151e-352"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4151e-353"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="4151e-353"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4151e-354"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="4151e-354"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-355">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="4151e-355">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4151e-356"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="4151e-356"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-357">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="4151e-357">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4151e-358"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="4151e-358"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-359">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="4151e-359">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="4151e-360">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="4151e-360">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="4151e-361">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="4151e-361">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4151e-362"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="4151e-362"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-363">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="4151e-363">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4151e-364"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="4151e-364"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4151e-365">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="4151e-365">Timed Power-On Supported</span></span>

<span data-ttu-id="4151e-366">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="4151e-366">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4151e-367">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="4151e-367">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-368">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4151e-368">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4151e-370">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="4151e-370">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="4151e-371">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="4151e-371">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="4151e-372">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-372">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-373">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="4151e-373">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-374">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4151e-374">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-376">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4151e-376">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-377">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="4151e-377">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="4151e-378">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-378">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4151e-379">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4151e-379">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4151e-380">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="4151e-380">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="4151e-381">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="4151e-381">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="4151e-382">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="4151e-382">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="4151e-383">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="4151e-383">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="4151e-384">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="4151e-384">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="4151e-385">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="4151e-385">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="4151e-386">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="4151e-386">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="4151e-387">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="4151e-387">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="4151e-388">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="4151e-388">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="4151e-389">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="4151e-389">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="4151e-390">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="4151e-390">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="4151e-391">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="4151e-391">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="4151e-392">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="4151e-392">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="4151e-393">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="4151e-393">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="4151e-394">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="4151e-394">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="4151e-395">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="4151e-395">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="4151e-396">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="4151e-396">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="4151e-397">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="4151e-397">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="4151e-398">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="4151e-398">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="4151e-399">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="4151e-399">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="4151e-400">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="4151e-400">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="4151e-401">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="4151e-401">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="4151e-402">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="4151e-402">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="4151e-403">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="4151e-403">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="4151e-404">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="4151e-404">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="4151e-405">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="4151e-405">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="4151e-406">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="4151e-406">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="4151e-407">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="4151e-407">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="4151e-408">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="4151e-408">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="4151e-409">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="4151e-409">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="4151e-410">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="4151e-410">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="4151e-411">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="4151e-411">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="4151e-412">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="4151e-412">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="4151e-413">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="4151e-413">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="4151e-414">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="4151e-414">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="4151e-415">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="4151e-415">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="4151e-416">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="4151e-416">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="4151e-417">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="4151e-417">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="4151e-418">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="4151e-418">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="4151e-419">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="4151e-419">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="4151e-420">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="4151e-420">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="4151e-421">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="4151e-421">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="4151e-422">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="4151e-422">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="4151e-423">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="4151e-423">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="4151e-424">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="4151e-424">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="4151e-425">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="4151e-425">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4151e-426">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="4151e-426">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-427">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-428">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-429">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="4151e-429">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-430">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="4151e-430">Current status of the object.</span></span> <span data-ttu-id="4151e-431">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="4151e-431">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="4151e-432">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="4151e-432">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="4151e-433">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="4151e-433">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4151e-434">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="4151e-434">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4151e-435">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="4151e-435">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4151e-436">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-436">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4151e-437">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="4151e-437">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4151e-438">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="4151e-438">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4151e-439">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="4151e-439">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4151e-440">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="4151e-440">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4151e-441">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="4151e-441">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4151e-442">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="4151e-442">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4151e-443">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="4151e-443">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4151e-444">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="4151e-444">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4151e-445">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="4151e-445">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4151e-446">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="4151e-446">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4151e-447">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="4151e-447">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4151e-448">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="4151e-448">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4151e-449">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="4151e-449">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4151e-450">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="4151e-450">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-451">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4151e-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-452">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-453">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="4151e-453">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="4151e-454">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4151e-454">State of the logical device.</span></span> <span data-ttu-id="4151e-455">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="4151e-455">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="4151e-456">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-456">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4151e-457">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4151e-457">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4151e-458">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="4151e-458">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4151e-459">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="4151e-459">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4151e-460">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="4151e-460">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="4151e-461">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="4151e-461">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4151e-462">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="4151e-462">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-463">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-465">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4151e-465">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4151e-466">Значение для свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="4151e-466">Value for the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="4151e-467">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-468">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4151e-468">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-469">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4151e-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-470">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4151e-471">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="4151e-471">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="4151e-472">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="4151e-472">Name of the scoping system.</span></span>

<span data-ttu-id="4151e-473">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="4151e-473">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="4151e-474">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="4151e-474">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4151e-475">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4151e-475">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4151e-476">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4151e-476">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4151e-477">Дата и время последнего сброса контроллера.</span><span class="sxs-lookup"><span data-stu-id="4151e-477">Date and time controller was last reset.</span></span> <span data-ttu-id="4151e-478">Это может означать, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="4151e-478">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="4151e-479">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-479">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4151e-480">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4151e-480">Remarks</span></span>

<span data-ttu-id="4151e-481">Класс **Win32 \_ 1394Controller** является производным от [**CIM \_ Controller**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="4151e-481">The **Win32\_1394Controller** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4151e-482">Примеры</span><span class="sxs-lookup"><span data-stu-id="4151e-482">Examples</span></span>

<span data-ttu-id="4151e-483">Следующий пример кода PowerShell извлекает сведения о контроллере.</span><span class="sxs-lookup"><span data-stu-id="4151e-483">The following PowerShell code sample retrieves controller information.</span></span>


```PowerShell
  function Get-Availability {
param ([uint16] $char)
# Helper function to return characterics of the 1394 Controller
# parse and return values
 If ($char -ge 1 -and $char -le 17) {
   switch ($char) {
  1  {"01-Other"}
  2  {"02-Unkown"}
  3  {"03-Running/Full Power"}
  4  {"04-Warning"}
  5  {"05-In Test"}
  6  {"06-Not Applicable"}
  7  {"07-POwer Off"}
  8  {"08-Off  Line"}
  9  {"09-Off Duty"}
  10  {"10-Degraded"}
  11  {"11-Not Installed"}
  12  {"12-InstallError"}
  13  {"13-Power Save - Unknown"}
  14  {"14-Power Save - Low Power Mode"}
  15  {"15-Power Save - Standby"}
  16  {"16-Power Cycle"}
  17  {"17-Power Save - Warning"}
}
}

Else
 {"{0} - invalid code" -f $char}
 Return
 }

# Get Controller information from WMI
$controllers = Get-WMIObject Win32_1394Controller
    # Display Details
"Win32_1394 WMI Information"
"--------------------------"
$count=$controllers.count
if (!$count) {$count++} 
"{0} 1394 controller(s) found" -f $count
""
"Controller {0} - Characteristics" -f ++$i
"--------------------------------"
foreach ($cont in $controllers) {
$avail=Get-Availability($cont.availability)
"Availability                :  {0}" -f $avail
"Caption                     :  {0}" -f $cont.caption
"Config Manager Error Code   :  {0}" -f $cont.ConfigManagerErrorCode
"Config Manager User Config  :  {0}" -f $cont.ConfigManagerUserConfig 
"Creation Class Name         :  {0}" -f $cont.CreationClassName
"Description                 :  {0}" -f $cont.Description
"Device ID                   :  {0}" -f $cont.DeviceID
"Error Cleared               :  {0}" -f $cont.ErrorCleared
"Error Description           :  {0}" -f $cont.ErrorDescription
"InstallDate                 :  {0}" -f $cont.InstallDate 
"Last Error Code             :  {0}" -f $cont.LastErrorCode
"Manufacturer                :  {0}" -f $cont.Manufacturer
"MaxNumberControlled         :  {0}" -f $cont.MaxNumberControlled
"Name                        :  {0}" -f $cont.Name
"PNPDeviceID                 :  {0}" -f $cont.PNPDeviceId
"PowerManagementCapabilities :  {0}" -f $cont.PowerManagementCapabilities
"PowerManagementSupported    :  {0}" -f $cont.PowerManagementSupported
"Protocols Supported         :  {0}" -f $cont.ProtocolsSupported
"Status                      :  {0}" -f $cont.Status
"Status Information          :  {0}" -f $cont.StatusInfo
"System Creation Class Name  :  {0}" -f $cont.SystemCreationClassName
"System Name                 :  {0}" -f $cont.SystemName
"Time of Last Reset          :  {0}" -f $cont.TimeOfLastReset
""
}
```



<span data-ttu-id="4151e-484">Предыдущий пример кода возвращает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="4151e-484">The previous code sample returns the following information:</span></span>

``` syntax
## Win32_1394 WMI Information

1 1394 controller(s) found

## Controller 1 - Characteristics

Availability                :  0 - invalid code
Caption                     :  OHCI Compliant IEEE 1394 Host Controller
Config Manager Error Code   :  0
Config Manager User Config  :  False
Creation Class Name         :  Win32_1394Controller
Description                 :  OHCI Compliant IEEE 1394 Host Controller
Device ID                   :  PCI\VEN_1217&DEV_00F7&SUBSYS_01CC1028&REV_02\4&2FE911E8&0&0CF0
Error Cleared               :
Error Description           :
InstallDate                 :
Last Error Code             :
Manufacturer                :  IEEE 1394 OHCI Compliant Host Controller Vendor
MaxNumberControlled         :
Name                        :  OHCI Compliant IEEE 1394 Host Controller
PNPDeviceID                 :  PCI\VEN_1217&DEV_00F7&SUBSYS_01CC1028&REV_02\4&2FE911E8&0&0CF0
PowerManagementCapabilities :
PowerManagementSupported    :
Protocols Supported         :
Status                      :  OK
Status Information          :
System Creation Class Name  :  Win32_ComputerSystem
System Name                 :  UK0N055
Time of Last Reset          :
```

## <a name="requirements"></a><span data-ttu-id="4151e-485">Требования</span><span class="sxs-lookup"><span data-stu-id="4151e-485">Requirements</span></span>



| <span data-ttu-id="4151e-486">Требование</span><span class="sxs-lookup"><span data-stu-id="4151e-486">Requirement</span></span> | <span data-ttu-id="4151e-487">Значение</span><span class="sxs-lookup"><span data-stu-id="4151e-487">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4151e-488">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4151e-488">Minimum supported client</span></span><br/> | <span data-ttu-id="4151e-489">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4151e-489">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4151e-490">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4151e-490">Minimum supported server</span></span><br/> | <span data-ttu-id="4151e-491">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4151e-491">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4151e-492">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4151e-492">Namespace</span></span><br/>                | <span data-ttu-id="4151e-493">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4151e-493">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4151e-494">MOF</span><span class="sxs-lookup"><span data-stu-id="4151e-494">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4151e-495"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4151e-495"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4151e-496">DLL</span><span class="sxs-lookup"><span data-stu-id="4151e-496">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4151e-497"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4151e-497"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4151e-498">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4151e-498">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4151e-499">**\_Контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="4151e-499">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dt>

[<span data-ttu-id="4151e-500">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="4151e-500">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

