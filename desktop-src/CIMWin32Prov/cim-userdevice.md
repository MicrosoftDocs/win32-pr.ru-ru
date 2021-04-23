---
description: Класс CIM \_ усердевице является родительским классом, от которого другие классы, такие как CIM- \_ клавиатура или CIM \_ десктопмонитор, по убыванию. Устройства пользователей — это логические устройства, позволяющие пользователю компьютерной системы вводить, просматривать или слышать данные.
ms.assetid: 311a065a-df9b-4c4b-bdc4-d3de89ce2f3d
ms.tgt_platform: multiple
title: Класс CIM_UserDevice (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.Availability
- CIM_UserDevice.Caption
- CIM_UserDevice.ConfigManagerErrorCode
- CIM_UserDevice.ConfigManagerUserConfig
- CIM_UserDevice.CreationClassName
- CIM_UserDevice.Description
- CIM_UserDevice.DeviceID
- CIM_UserDevice.ErrorCleared
- CIM_UserDevice.ErrorDescription
- CIM_UserDevice.InstallDate
- CIM_UserDevice.IsLocked
- CIM_UserDevice.LastErrorCode
- CIM_UserDevice.Name
- CIM_UserDevice.PNPDeviceID
- CIM_UserDevice.PowerManagementCapabilities
- CIM_UserDevice.PowerManagementSupported
- CIM_UserDevice.Status
- CIM_UserDevice.StatusInfo
- CIM_UserDevice.SystemCreationClassName
- CIM_UserDevice.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b8a91082679c38d7741f9a8d7b43c7f9705333f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140863"
---
# <a name="cim_userdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="0948d-104">Класс CIM_UserDevice (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="0948d-104">CIM_UserDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="0948d-105">Класс **CIM \_ усердевице** является родительским классом, от которого другие классы, такие как [**CIM- \_ Клавиатура**](cim-keyboard.md) или [**CIM \_ десктопмонитор**](cim-desktopmonitor.md), по убыванию.</span><span class="sxs-lookup"><span data-stu-id="0948d-105">The **CIM\_UserDevice** class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="0948d-106">Устройства пользователей — это логические устройства, позволяющие пользователю компьютерной системы вводить, просматривать или слышать данные.</span><span class="sxs-lookup"><span data-stu-id="0948d-106">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0948d-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0948d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0948d-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0948d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0948d-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0948d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0948d-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0948d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0948d-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0948d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C533-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
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
  boolean  IsLocked;
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

## <a name="members"></a><span data-ttu-id="0948d-112">Члены</span><span class="sxs-lookup"><span data-stu-id="0948d-112">Members</span></span>

<span data-ttu-id="0948d-113">Класс **CIM \_ усердевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0948d-113">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="0948d-114">Методы</span><span class="sxs-lookup"><span data-stu-id="0948d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="0948d-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="0948d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0948d-116">Методы</span><span class="sxs-lookup"><span data-stu-id="0948d-116">Methods</span></span>

<span data-ttu-id="0948d-117">Класс **CIM \_ усердевице** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0948d-117">The **CIM\_UserDevice** class has these methods.</span></span>



| <span data-ttu-id="0948d-118">Метод</span><span class="sxs-lookup"><span data-stu-id="0948d-118">Method</span></span>                                                                | <span data-ttu-id="0948d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0948d-119">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0948d-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="0948d-120">**Reset**</span></span>](reset-method-in-class-cim-userdevice.md)                 | <span data-ttu-id="0948d-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="0948d-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0948d-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0948d-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0948d-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-userdevice.md) | <span data-ttu-id="0948d-124">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="0948d-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0948d-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0948d-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0948d-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="0948d-126">Properties</span></span>

<span data-ttu-id="0948d-127">Класс **CIM \_ усердевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0948d-127">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0948d-128">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="0948d-128">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0948d-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-131">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="0948d-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-132">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-132">Availability and status of the device.</span></span>

<span data-ttu-id="0948d-133">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-133">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0948d-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0948d-134"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0948d-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0948d-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0948d-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="0948d-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0948d-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="0948d-137"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0948d-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="0948d-138"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0948d-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="0948d-139"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0948d-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="0948d-140"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0948d-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="0948d-141"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0948d-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="0948d-142"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0948d-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="0948d-143"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0948d-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="0948d-144"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0948d-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="0948d-145"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0948d-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="0948d-146"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-147">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="0948d-147">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0948d-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="0948d-148"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-149">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="0948d-149">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0948d-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="0948d-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-151">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="0948d-151">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0948d-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="0948d-152"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0948d-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="0948d-153"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-154">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="0948d-154">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0948d-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="0948d-155"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-156">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="0948d-156">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0948d-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="0948d-157"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-158">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="0948d-158">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0948d-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="0948d-159"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-160">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="0948d-160">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0948d-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="0948d-161"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-162">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="0948d-162">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0948d-163">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0948d-163">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-166">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0948d-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-167">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0948d-167">Short textual description of the object.</span></span>

<span data-ttu-id="0948d-168">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0948d-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-169">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="0948d-169">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0948d-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-172">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0948d-172">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-173">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0948d-173">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0948d-174">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-174">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0948d-175"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="0948d-175"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0948d-176"> (0)</span><span class="sxs-lookup"><span data-stu-id="0948d-176">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-177">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="0948d-177">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0948d-178"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="0948d-178"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0948d-179">(1)</span><span class="sxs-lookup"><span data-stu-id="0948d-179">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-180">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="0948d-180">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0948d-181"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-181"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0948d-182">(2)</span><span class="sxs-lookup"><span data-stu-id="0948d-182">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0948d-183"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="0948d-183"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0948d-184">(3)</span><span class="sxs-lookup"><span data-stu-id="0948d-184">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-185">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0948d-185">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0948d-186"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="0948d-186"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0948d-187">(4)</span><span class="sxs-lookup"><span data-stu-id="0948d-187">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-188">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0948d-188">Device is not working properly.</span></span> <span data-ttu-id="0948d-189">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0948d-189">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0948d-190"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="0948d-190"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0948d-191">(5)</span><span class="sxs-lookup"><span data-stu-id="0948d-191">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-192">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="0948d-192">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0948d-193"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="0948d-193"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0948d-194"> (6)</span><span class="sxs-lookup"><span data-stu-id="0948d-194">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-195">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="0948d-195">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0948d-196"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="0948d-196"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0948d-197">(7)</span><span class="sxs-lookup"><span data-stu-id="0948d-197">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0948d-198"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-198"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0948d-199">(8)</span><span class="sxs-lookup"><span data-stu-id="0948d-199">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-200">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-200">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0948d-201"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-201"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0948d-202">(9)</span><span class="sxs-lookup"><span data-stu-id="0948d-202">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-203">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-203">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0948d-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="0948d-204"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0948d-205">(10)</span><span class="sxs-lookup"><span data-stu-id="0948d-205">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-206">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="0948d-206">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0948d-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-207"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0948d-208">(11)</span><span class="sxs-lookup"><span data-stu-id="0948d-208">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-209">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-209">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0948d-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="0948d-210"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0948d-211">(12)</span><span class="sxs-lookup"><span data-stu-id="0948d-211">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-212">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="0948d-212">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0948d-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-213"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0948d-214">(13)</span><span class="sxs-lookup"><span data-stu-id="0948d-214">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-215">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-215">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0948d-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="0948d-216"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0948d-217">(14)</span><span class="sxs-lookup"><span data-stu-id="0948d-217">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-218">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="0948d-218">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0948d-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="0948d-219"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0948d-220">(15)</span><span class="sxs-lookup"><span data-stu-id="0948d-220">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-221">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="0948d-221">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0948d-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="0948d-222"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0948d-223">(16)</span><span class="sxs-lookup"><span data-stu-id="0948d-223">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-224">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="0948d-224">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0948d-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="0948d-225"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0948d-226">(17)</span><span class="sxs-lookup"><span data-stu-id="0948d-226">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-227">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0948d-227">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0948d-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-228"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0948d-229">(18)</span><span class="sxs-lookup"><span data-stu-id="0948d-229">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-230">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="0948d-230">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0948d-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="0948d-231"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0948d-232">(19)</span><span class="sxs-lookup"><span data-stu-id="0948d-232">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0948d-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="0948d-233"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0948d-234">(20)</span><span class="sxs-lookup"><span data-stu-id="0948d-234">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-235">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0948d-235">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0948d-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="0948d-236"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0948d-237">(21)</span><span class="sxs-lookup"><span data-stu-id="0948d-237">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-238">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="0948d-238">System failure.</span></span> <span data-ttu-id="0948d-239">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="0948d-239">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0948d-240">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="0948d-240">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0948d-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="0948d-241"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0948d-242">(22)</span><span class="sxs-lookup"><span data-stu-id="0948d-242">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-243">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="0948d-243">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0948d-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="0948d-244"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0948d-245">(23)</span><span class="sxs-lookup"><span data-stu-id="0948d-245">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-246">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="0948d-246">System failure.</span></span> <span data-ttu-id="0948d-247">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="0948d-247">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0948d-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="0948d-248"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0948d-249">(24)</span><span class="sxs-lookup"><span data-stu-id="0948d-249">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-250">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="0948d-250">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0948d-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="0948d-251"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0948d-252">(25)</span><span class="sxs-lookup"><span data-stu-id="0948d-252">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-253">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="0948d-253">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0948d-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="0948d-254"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0948d-255">(26)</span><span class="sxs-lookup"><span data-stu-id="0948d-255">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-256">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="0948d-256">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0948d-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="0948d-257"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0948d-258">(27)</span><span class="sxs-lookup"><span data-stu-id="0948d-258">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-259">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="0948d-259">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0948d-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="0948d-260"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0948d-261">(28)</span><span class="sxs-lookup"><span data-stu-id="0948d-261">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-262">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="0948d-262">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0948d-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="0948d-263"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0948d-264">(29)</span><span class="sxs-lookup"><span data-stu-id="0948d-264">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-265">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="0948d-265">Device is disabled.</span></span> <span data-ttu-id="0948d-266">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0948d-266">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0948d-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="0948d-267"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0948d-268">(30)</span><span class="sxs-lookup"><span data-stu-id="0948d-268">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-269">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="0948d-269">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0948d-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0948d-270"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0948d-271">1-31</span><span class="sxs-lookup"><span data-stu-id="0948d-271">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-272">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0948d-272">Device is not working properly.</span></span> <span data-ttu-id="0948d-273">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="0948d-273">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0948d-274">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="0948d-274">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-275">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0948d-275">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-277">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0948d-277">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-278">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0948d-278">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0948d-279">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-279">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-280">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0948d-280">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-281">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-283">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0948d-283">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0948d-284">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0948d-284">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0948d-285">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="0948d-285">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0948d-286">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-286">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-287">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0948d-287">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-288">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-290">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="0948d-290">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-291">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0948d-291">Textual description of the object.</span></span>

<span data-ttu-id="0948d-292">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0948d-292">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-293">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0948d-293">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-296">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0948d-296">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0948d-297">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-297">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0948d-298">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-299">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="0948d-299">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-300">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0948d-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0948d-302">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="0948d-302">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0948d-303">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-304">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0948d-304">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0948d-307">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="0948d-307">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0948d-308">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-309">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0948d-309">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-310">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0948d-310">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-312">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="0948d-312">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-313">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0948d-313">Date and time the object was installed.</span></span> <span data-ttu-id="0948d-314">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="0948d-314">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0948d-315">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0948d-315">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-316">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="0948d-316">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-317">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0948d-317">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0948d-319">**Значение true** показывает, что устройство заблокировано, что предотвращает ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="0948d-319">If **TRUE**, the device is locked, preventing user input or output.</span></span>

</dd> <dt>

<span data-ttu-id="0948d-320">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="0948d-320">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-321">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0948d-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0948d-323">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="0948d-323">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0948d-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-325">**Name**</span><span class="sxs-lookup"><span data-stu-id="0948d-325">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-328">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="0948d-328">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-329">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="0948d-329">Label by which the object is known.</span></span> <span data-ttu-id="0948d-330">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="0948d-330">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0948d-331">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0948d-331">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-332">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0948d-332">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-333">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-335">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0948d-335">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-336">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-336">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="0948d-337">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-337">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0948d-338">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0948d-338">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0948d-339">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="0948d-339">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-340">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0948d-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0948d-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0948d-342">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="0948d-342">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0948d-343">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-343">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0948d-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0948d-344"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0948d-345"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="0948d-345"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0948d-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="0948d-346"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0948d-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="0948d-347"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-348">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="0948d-348">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0948d-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="0948d-349"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-350">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="0948d-350">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0948d-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="0948d-351"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-352">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="0948d-352">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0948d-353">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="0948d-353">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0948d-354">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0948d-354">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0948d-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="0948d-355"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-356">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="0948d-356">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0948d-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="0948d-357"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0948d-358">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="0948d-358">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0948d-359">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="0948d-359">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-360">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0948d-360">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0948d-362">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="0948d-362">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0948d-363">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="0948d-363">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0948d-364">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0948d-364">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0948d-365">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="0948d-365">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="0948d-366">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-366">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-367">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0948d-367">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-368">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-368">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-370">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="0948d-370">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-371">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0948d-371">Current status of the object.</span></span> <span data-ttu-id="0948d-372">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0948d-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0948d-373">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="0948d-373">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0948d-374">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="0948d-374">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0948d-375">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="0948d-375">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0948d-376">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="0948d-376">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0948d-377">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0948d-377">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0948d-378">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0948d-378">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0948d-379">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0948d-379">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0948d-380">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="0948d-380">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0948d-381">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="0948d-381">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0948d-382">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="0948d-382">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0948d-383">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="0948d-383">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0948d-384">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="0948d-384">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0948d-385">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="0948d-385">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0948d-386">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0948d-386">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0948d-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-389">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0948d-389">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0948d-390">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0948d-390">State of the logical device.</span></span> <span data-ttu-id="0948d-391">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="0948d-391">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0948d-392">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-392">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0948d-393">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0948d-393">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0948d-394">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0948d-394">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0948d-395">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="0948d-395">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0948d-396">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="0948d-396">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0948d-397">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="0948d-397">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0948d-398">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="0948d-398">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-401">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0948d-401">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0948d-402">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="0948d-402">Scoping system's creation class name.</span></span>

<span data-ttu-id="0948d-403">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0948d-404">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0948d-404">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0948d-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0948d-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0948d-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0948d-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0948d-407">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0948d-407">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0948d-408">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="0948d-408">Scoping system's name.</span></span>

<span data-ttu-id="0948d-409">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0948d-409">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0948d-410">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0948d-410">Remarks</span></span>

<span data-ttu-id="0948d-411">Класс **CIM \_ усердевице** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="0948d-411">The **CIM\_UserDevice** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0948d-412">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0948d-412">WMI does not implement this class.</span></span> <span data-ttu-id="0948d-413">Классы WMI, производные от **CIM \_ усердевице**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0948d-413">For WMI classes derived from **CIM\_UserDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0948d-414">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0948d-414">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0948d-415">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0948d-415">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0948d-416">Требования</span><span class="sxs-lookup"><span data-stu-id="0948d-416">Requirements</span></span>



| <span data-ttu-id="0948d-417">Требование</span><span class="sxs-lookup"><span data-stu-id="0948d-417">Requirement</span></span> | <span data-ttu-id="0948d-418">Значение</span><span class="sxs-lookup"><span data-stu-id="0948d-418">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0948d-419">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0948d-419">Minimum supported client</span></span><br/> | <span data-ttu-id="0948d-420">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0948d-420">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0948d-421">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0948d-421">Minimum supported server</span></span><br/> | <span data-ttu-id="0948d-422">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0948d-422">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0948d-423">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0948d-423">Namespace</span></span><br/>                | <span data-ttu-id="0948d-424">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0948d-424">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0948d-425">MOF</span><span class="sxs-lookup"><span data-stu-id="0948d-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0948d-426"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0948d-426"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0948d-427">DLL</span><span class="sxs-lookup"><span data-stu-id="0948d-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0948d-428"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0948d-428"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0948d-429">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0948d-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0948d-430">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="0948d-430">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

