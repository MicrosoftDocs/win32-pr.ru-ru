---
description: '\_Класс-дисплей CIM является родительским классом для группирования различных устройств вывода.'
ms.assetid: e7cd03b1-bc43-4eb0-a591-104a0d250e82
ms.tgt_platform: multiple
title: Класс CIM_Display (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Display
- CIM_Display.Availability
- CIM_Display.Caption
- CIM_Display.ConfigManagerErrorCode
- CIM_Display.ConfigManagerUserConfig
- CIM_Display.CreationClassName
- CIM_Display.Description
- CIM_Display.DeviceID
- CIM_Display.ErrorCleared
- CIM_Display.ErrorDescription
- CIM_Display.InstallDate
- CIM_Display.IsLocked
- CIM_Display.LastErrorCode
- CIM_Display.Name
- CIM_Display.PNPDeviceID
- CIM_Display.PowerManagementCapabilities
- CIM_Display.PowerManagementSupported
- CIM_Display.Status
- CIM_Display.StatusInfo
- CIM_Display.SystemCreationClassName
- CIM_Display.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 684ca28891f709d6eda2c030e20ddfaa42ef26bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990602"
---
# <a name="cim_display-class-cimwin32-wmi-providers"></a><span data-ttu-id="dbfcc-103">Класс CIM_Display (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-103">CIM_Display class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dbfcc-104">Класс **- \_ дисплей CIM** является родительским классом для группирования различных устройств вывода.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-104">The **CIM\_Display** class is a parent class for grouping miscellaneous display devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbfcc-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbfcc-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbfcc-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dbfcc-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbfcc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbfcc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCE7-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_Display : CIM_UserDevice
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

## <a name="members"></a><span data-ttu-id="dbfcc-110">Члены</span><span class="sxs-lookup"><span data-stu-id="dbfcc-110">Members</span></span>

<span data-ttu-id="dbfcc-111">Класс **\_ дисплеев CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dbfcc-111">The **CIM\_Display** class has these types of members:</span></span>

-   [<span data-ttu-id="dbfcc-112">Методы</span><span class="sxs-lookup"><span data-stu-id="dbfcc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="dbfcc-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbfcc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dbfcc-114">Методы</span><span class="sxs-lookup"><span data-stu-id="dbfcc-114">Methods</span></span>

<span data-ttu-id="dbfcc-115">Класс **\_ дисплеев CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-115">The **CIM\_Display** class has these methods.</span></span>



| <span data-ttu-id="dbfcc-116">Метод</span><span class="sxs-lookup"><span data-stu-id="dbfcc-116">Method</span></span>                                                                | <span data-ttu-id="dbfcc-117">Описание</span><span class="sxs-lookup"><span data-stu-id="dbfcc-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbfcc-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-118">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="dbfcc-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="dbfcc-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="dbfcc-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="dbfcc-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="dbfcc-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="dbfcc-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbfcc-124">Properties</span></span>

<span data-ttu-id="dbfcc-125">Класс **\_ дисплеев CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-125">The **CIM\_Display** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbfcc-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-130">Availability and status of the device.</span></span>

<span data-ttu-id="dbfcc-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbfcc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbfcc-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="dbfcc-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="dbfcc-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="dbfcc-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dbfcc-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="dbfcc-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="dbfcc-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="dbfcc-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dbfcc-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="dbfcc-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="dbfcc-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="dbfcc-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="dbfcc-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="dbfcc-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="dbfcc-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="dbfcc-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="dbfcc-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="dbfcc-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="dbfcc-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="dbfcc-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbfcc-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-164">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-165">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-165">Short textual description of the object.</span></span>

<span data-ttu-id="dbfcc-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-167">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-170">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-171">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="dbfcc-172">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="dbfcc-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="dbfcc-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-175">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="dbfcc-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="dbfcc-177">(1)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-178">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dbfcc-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="dbfcc-180">(2)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="dbfcc-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="dbfcc-182">(3)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-183">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dbfcc-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="dbfcc-185">(4)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-186">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-186">Device is not working properly.</span></span> <span data-ttu-id="dbfcc-187">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="dbfcc-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="dbfcc-189">(5)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-190">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="dbfcc-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="dbfcc-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-193">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="dbfcc-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="dbfcc-195">(7)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="dbfcc-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="dbfcc-197">(8)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-198">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="dbfcc-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="dbfcc-200">(9)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-201">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-201">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="dbfcc-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-202"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="dbfcc-203">(10)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-203">(10)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-204">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-204">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="dbfcc-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-205"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="dbfcc-206">(11)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-206">(11)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-207">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-207">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="dbfcc-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-208"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="dbfcc-209">(12)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-209">(12)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-210">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-210">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="dbfcc-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-211"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="dbfcc-212">(13)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-212">(13)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-213">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-213">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="dbfcc-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-214"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="dbfcc-215">(14)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-215">(14)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-216">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-216">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="dbfcc-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-217"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="dbfcc-218">(15)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-218">(15)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-219">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-219">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="dbfcc-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-220"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="dbfcc-221">(16)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-221">(16)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-222">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-222">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="dbfcc-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-223"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="dbfcc-224">(17)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-224">(17)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-225">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-225">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dbfcc-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-226"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="dbfcc-227">(18)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-227">(18)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-228">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-228">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="dbfcc-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-229"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="dbfcc-230">(19)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-230">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="dbfcc-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-231"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="dbfcc-232">(20)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-232">(20)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-233">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-233">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="dbfcc-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-234"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="dbfcc-235">(21)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-235">(21)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-236">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-236">System failure.</span></span> <span data-ttu-id="dbfcc-237">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-237">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="dbfcc-238">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-238">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="dbfcc-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-239"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="dbfcc-240">(22)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-240">(22)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-241">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-241">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="dbfcc-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-242"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="dbfcc-243">(23)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-243">(23)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-244">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-244">System failure.</span></span> <span data-ttu-id="dbfcc-245">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-245">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="dbfcc-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-246"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="dbfcc-247">(24)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-247">(24)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-248">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-248">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dbfcc-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-249"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dbfcc-250">(25)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-250">(25)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-251">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-251">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="dbfcc-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-252"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="dbfcc-253">(26)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-253">(26)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-254">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-254">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="dbfcc-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-255"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="dbfcc-256">(27)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-256">(27)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-257">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-257">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="dbfcc-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-258"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="dbfcc-259">(28)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-259">(28)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-260">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-260">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="dbfcc-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-261"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="dbfcc-262">(29)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-262">(29)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-263">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-263">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="dbfcc-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-264"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="dbfcc-265">(30)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-265">(30)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-266">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-266">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="dbfcc-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-267"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="dbfcc-268">1-31</span><span class="sxs-lookup"><span data-stu-id="dbfcc-268">(31)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-269">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-269">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbfcc-270">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-270">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-271">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-271">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-273">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-273">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-274">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-274">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="dbfcc-275">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-275">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-276">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-276">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-279">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-279">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-280">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-280">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dbfcc-281">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-281">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="dbfcc-282">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-283">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-283">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-284">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-286">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-286">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-287">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-287">Textual description of the object.</span></span>

<span data-ttu-id="dbfcc-288">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-289">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-289">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-290">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-292">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-292">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-293">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-293">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="dbfcc-294">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-295">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-295">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-296">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-298">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-298">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="dbfcc-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-300">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-300">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-303">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойствах **ластерроркоде** , которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-303">Free-form string that supplies information about the error recorded in the **LastErrorCode** property corrective actions to perform.</span></span>

<span data-ttu-id="dbfcc-304">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-304">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-305">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-305">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-306">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-306">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-308">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-308">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-309">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-309">Date and time the object was installed.</span></span> <span data-ttu-id="dbfcc-310">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-310">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="dbfcc-311">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-311">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-312">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-312">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-313">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-313">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-315">**Значение true** показывает, что устройство заблокировано, что предотвращает ввод или вывод пользователя.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-315">If **TRUE**, the device is locked, preventing user input or output.</span></span>

<span data-ttu-id="dbfcc-316">Это свойство наследуется от [**CIM \_ усердевице**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-316">This property is inherited from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-317">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-317">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-318">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-320">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-320">Last error code reported by the logical device.</span></span>

<span data-ttu-id="dbfcc-321">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-321">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-322">**Name**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-322">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-323">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-324">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-325">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-325">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-326">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-326">Label by which the object is known.</span></span> <span data-ttu-id="dbfcc-327">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-327">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="dbfcc-328">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-328">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-329">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-329">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-332">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-332">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-333">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-333">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="dbfcc-334">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="dbfcc-335">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="dbfcc-335">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-336">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-336">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-337">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="dbfcc-337">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-339">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-339">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="dbfcc-340">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-340">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbfcc-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-341"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="dbfcc-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dbfcc-343"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-343"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dbfcc-344"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-344"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-345">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-345">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="dbfcc-346"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-346"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-347">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-347">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="dbfcc-348"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-348"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-349">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="dbfcc-349">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="dbfcc-350">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-350">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="dbfcc-351">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-351">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="dbfcc-352"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-352"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-353">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-353">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="dbfcc-354"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-354"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="dbfcc-355">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-355">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="dbfcc-356">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-356">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-357">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-359">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-359">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="dbfcc-360">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="dbfcc-360">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="dbfcc-361">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-361">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="dbfcc-362">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="dbfcc-362">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="dbfcc-363">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-364">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-365">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-367">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-367">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-368">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-368">Current status of the object.</span></span> <span data-ttu-id="dbfcc-369">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="dbfcc-370">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="dbfcc-370">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="dbfcc-371">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-371">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="dbfcc-372">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-372">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="dbfcc-373">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-373">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbfcc-374">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-374">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="dbfcc-375">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-375">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="dbfcc-376">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-376">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="dbfcc-377">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-377">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="dbfcc-378">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-378">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="dbfcc-379">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-379">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="dbfcc-380">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-380">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="dbfcc-381">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-381">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="dbfcc-382">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-382">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbfcc-383">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-383">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-384">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-384">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-386">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="dbfcc-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-387">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-387">State of the logical device.</span></span> <span data-ttu-id="dbfcc-388">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-388">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="dbfcc-389">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-389">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="dbfcc-390">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-390">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="dbfcc-391">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-391">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="dbfcc-392">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-392">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="dbfcc-393">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-393">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="dbfcc-394">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-394">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dbfcc-395">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-395">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-396">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-396">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-398">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-398">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-399">Свойство свойства **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-399">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="dbfcc-400">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-400">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="dbfcc-401">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-401">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbfcc-402">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-402">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbfcc-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbfcc-404">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbfcc-404">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbfcc-405">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-405">Scoping system's **Name** property.</span></span>

<span data-ttu-id="dbfcc-406">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-406">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbfcc-407">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbfcc-407">Remarks</span></span>

<span data-ttu-id="dbfcc-408">Класс **- \_ дисплей CIM** является производным [**от \_ CIM усердевице**](cim-userdevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-408">The **CIM\_Display** class is derived from [**CIM\_UserDevice**](cim-userdevice.md).</span></span>

<span data-ttu-id="dbfcc-409">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-409">WMI does not implement this class.</span></span> <span data-ttu-id="dbfcc-410">Классы, производные **от \_ представления CIM**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="dbfcc-410">For classes derived from **CIM\_Display**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="dbfcc-411">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-411">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbfcc-412">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dbfcc-412">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbfcc-413">Требования</span><span class="sxs-lookup"><span data-stu-id="dbfcc-413">Requirements</span></span>



| <span data-ttu-id="dbfcc-414">Требование</span><span class="sxs-lookup"><span data-stu-id="dbfcc-414">Requirement</span></span> | <span data-ttu-id="dbfcc-415">Значение</span><span class="sxs-lookup"><span data-stu-id="dbfcc-415">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfcc-416">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbfcc-416">Minimum supported client</span></span><br/> | <span data-ttu-id="dbfcc-417">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbfcc-417">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbfcc-418">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbfcc-418">Minimum supported server</span></span><br/> | <span data-ttu-id="dbfcc-419">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbfcc-419">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbfcc-420">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbfcc-420">Namespace</span></span><br/>                | <span data-ttu-id="dbfcc-421">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbfcc-421">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbfcc-422">MOF</span><span class="sxs-lookup"><span data-stu-id="dbfcc-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbfcc-423"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbfcc-423"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbfcc-424">DLL</span><span class="sxs-lookup"><span data-stu-id="dbfcc-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbfcc-425"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbfcc-425"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbfcc-426">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbfcc-426">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbfcc-427">**\_УСЕРДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="dbfcc-427">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> </dl>

 

