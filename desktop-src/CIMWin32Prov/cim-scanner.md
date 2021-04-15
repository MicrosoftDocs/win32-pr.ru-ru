---
description: Сканер CIM \_ представляет возможности и управление логическим устройством сканера.
ms.assetid: a881ba20-2922-45c0-b31c-a3fea221d410
ms.tgt_platform: multiple
title: Класс CIM_Scanner
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Scanner
- CIM_Scanner.Availability
- CIM_Scanner.Caption
- CIM_Scanner.ConfigManagerErrorCode
- CIM_Scanner.ConfigManagerUserConfig
- CIM_Scanner.CreationClassName
- CIM_Scanner.Description
- CIM_Scanner.DeviceID
- CIM_Scanner.ErrorCleared
- CIM_Scanner.ErrorDescription
- CIM_Scanner.InstallDate
- CIM_Scanner.LastErrorCode
- CIM_Scanner.Name
- CIM_Scanner.PNPDeviceID
- CIM_Scanner.PowerManagementCapabilities
- CIM_Scanner.PowerManagementSupported
- CIM_Scanner.Status
- CIM_Scanner.StatusInfo
- CIM_Scanner.SystemCreationClassName
- CIM_Scanner.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cf0afb62eccfa289418e3ffeb22ea3a976ce7e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655688"
---
# <a name="cim_scanner-class"></a><span data-ttu-id="9f51e-103">\_Класс сканера CIM</span><span class="sxs-lookup"><span data-stu-id="9f51e-103">CIM\_Scanner class</span></span>

<span data-ttu-id="9f51e-104">**\_ Сканер CIM** представляет возможности и управление логическим устройством сканера.</span><span class="sxs-lookup"><span data-stu-id="9f51e-104">The **CIM\_Scanner** represents the capabilities and management of the scanner logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f51e-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9f51e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9f51e-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9f51e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9f51e-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9f51e-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9f51e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f51e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f51e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{07F12A62-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_Scanner : CIM_LogicalDevice
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
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="9f51e-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9f51e-110">Members</span></span>

<span data-ttu-id="9f51e-111">Класс **" \_ сканер CIM** " имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9f51e-111">The **CIM\_Scanner** class has these types of members:</span></span>

-   [<span data-ttu-id="9f51e-112">Методы</span><span class="sxs-lookup"><span data-stu-id="9f51e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="9f51e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f51e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9f51e-114">Методы</span><span class="sxs-lookup"><span data-stu-id="9f51e-114">Methods</span></span>

<span data-ttu-id="9f51e-115">Класс **\_ сканера CIM** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9f51e-115">The **CIM\_Scanner** class has these methods.</span></span>



| <span data-ttu-id="9f51e-116">Метод</span><span class="sxs-lookup"><span data-stu-id="9f51e-116">Method</span></span>                                                             | <span data-ttu-id="9f51e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9f51e-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f51e-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="9f51e-118">**Reset**</span></span>](reset-method-in-class-cim-scanner.md)                 | <span data-ttu-id="9f51e-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="9f51e-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9f51e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9f51e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9f51e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-scanner.md) | <span data-ttu-id="9f51e-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="9f51e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9f51e-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9f51e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9f51e-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="9f51e-124">Properties</span></span>

<span data-ttu-id="9f51e-125">Класс **\_ сканера CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-125">The **CIM\_Scanner** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9f51e-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="9f51e-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f51e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="9f51e-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-130">Availability and status of the device.</span></span>

<span data-ttu-id="9f51e-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f51e-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9f51e-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f51e-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9f51e-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9f51e-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="9f51e-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9f51e-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="9f51e-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9f51e-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="9f51e-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f51e-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="9f51e-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9f51e-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="9f51e-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9f51e-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="9f51e-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9f51e-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="9f51e-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f51e-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="9f51e-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9f51e-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="9f51e-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9f51e-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="9f51e-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9f51e-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="9f51e-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9f51e-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9f51e-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="9f51e-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="9f51e-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9f51e-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="9f51e-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="9f51e-149">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9f51e-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="9f51e-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9f51e-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="9f51e-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="9f51e-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9f51e-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="9f51e-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="9f51e-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9f51e-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="9f51e-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="9f51e-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9f51e-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="9f51e-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="9f51e-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9f51e-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="9f51e-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="9f51e-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f51e-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9f51e-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-164">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9f51e-164">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-165">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9f51e-165">Short textual description of the object.</span></span>

<span data-ttu-id="9f51e-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f51e-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-167">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9f51e-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f51e-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-170">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f51e-170">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-171">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9f51e-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9f51e-172">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9f51e-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="9f51e-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="9f51e-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-175">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="9f51e-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9f51e-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="9f51e-177">(1)</span><span class="sxs-lookup"><span data-stu-id="9f51e-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-178">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="9f51e-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f51e-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9f51e-180">(2)</span><span class="sxs-lookup"><span data-stu-id="9f51e-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9f51e-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9f51e-182">(3)</span><span class="sxs-lookup"><span data-stu-id="9f51e-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-183">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f51e-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f51e-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9f51e-185">(4)</span><span class="sxs-lookup"><span data-stu-id="9f51e-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-186">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="9f51e-186">Device is not working properly.</span></span> <span data-ttu-id="9f51e-187">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="9f51e-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9f51e-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9f51e-189">(5)</span><span class="sxs-lookup"><span data-stu-id="9f51e-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-190">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="9f51e-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9f51e-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9f51e-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="9f51e-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-193">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="9f51e-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9f51e-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="9f51e-195">(7)</span><span class="sxs-lookup"><span data-stu-id="9f51e-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9f51e-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9f51e-197">(8)</span><span class="sxs-lookup"><span data-stu-id="9f51e-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-198">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9f51e-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9f51e-200">(9)</span><span class="sxs-lookup"><span data-stu-id="9f51e-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-201">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="9f51e-201">Device is not working properly.</span></span> <span data-ttu-id="9f51e-202">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9f51e-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="9f51e-204">(10)</span><span class="sxs-lookup"><span data-stu-id="9f51e-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-205">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="9f51e-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9f51e-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="9f51e-207">(11)</span><span class="sxs-lookup"><span data-stu-id="9f51e-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-208">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9f51e-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9f51e-210">(12)</span><span class="sxs-lookup"><span data-stu-id="9f51e-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-211">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="9f51e-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9f51e-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9f51e-213">(13)</span><span class="sxs-lookup"><span data-stu-id="9f51e-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-214">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9f51e-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9f51e-216">(14)</span><span class="sxs-lookup"><span data-stu-id="9f51e-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-217">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="9f51e-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9f51e-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9f51e-219">(15)</span><span class="sxs-lookup"><span data-stu-id="9f51e-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-220">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="9f51e-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9f51e-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9f51e-222">(16)</span><span class="sxs-lookup"><span data-stu-id="9f51e-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-223">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="9f51e-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9f51e-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9f51e-225">(17)</span><span class="sxs-lookup"><span data-stu-id="9f51e-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-226">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f51e-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f51e-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9f51e-228">(18)</span><span class="sxs-lookup"><span data-stu-id="9f51e-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-229">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="9f51e-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9f51e-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="9f51e-231">(19)</span><span class="sxs-lookup"><span data-stu-id="9f51e-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9f51e-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="9f51e-233">(20)</span><span class="sxs-lookup"><span data-stu-id="9f51e-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-234">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="9f51e-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9f51e-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9f51e-236">(21)</span><span class="sxs-lookup"><span data-stu-id="9f51e-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-237">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="9f51e-237">System failure.</span></span> <span data-ttu-id="9f51e-238">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="9f51e-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="9f51e-239">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="9f51e-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9f51e-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="9f51e-241">(22)</span><span class="sxs-lookup"><span data-stu-id="9f51e-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-242">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="9f51e-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9f51e-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9f51e-244">(23)</span><span class="sxs-lookup"><span data-stu-id="9f51e-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="9f51e-245">System failure.</span></span> <span data-ttu-id="9f51e-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="9f51e-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9f51e-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9f51e-248">(24)</span><span class="sxs-lookup"><span data-stu-id="9f51e-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-249">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="9f51e-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f51e-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f51e-251">(25)</span><span class="sxs-lookup"><span data-stu-id="9f51e-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-252">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="9f51e-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9f51e-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="9f51e-254">(26)</span><span class="sxs-lookup"><span data-stu-id="9f51e-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-255">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="9f51e-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9f51e-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9f51e-257">(27)</span><span class="sxs-lookup"><span data-stu-id="9f51e-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-258">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="9f51e-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9f51e-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9f51e-260">(28)</span><span class="sxs-lookup"><span data-stu-id="9f51e-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-261">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="9f51e-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9f51e-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9f51e-263">(29)</span><span class="sxs-lookup"><span data-stu-id="9f51e-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-264">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="9f51e-264">Device is disabled.</span></span> <span data-ttu-id="9f51e-265">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="9f51e-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9f51e-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9f51e-267">(30)</span><span class="sxs-lookup"><span data-stu-id="9f51e-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-268">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="9f51e-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9f51e-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9f51e-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9f51e-270">1-31</span><span class="sxs-lookup"><span data-stu-id="9f51e-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-271">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="9f51e-271">Device is not working properly.</span></span> <span data-ttu-id="9f51e-272">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="9f51e-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f51e-273">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="9f51e-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9f51e-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-276">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f51e-276">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-277">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9f51e-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9f51e-278">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9f51e-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-282">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f51e-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-283">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9f51e-283">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9f51e-284">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="9f51e-284">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9f51e-285">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-286">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9f51e-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-289">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="9f51e-289">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-290">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9f51e-290">Textual description of the object.</span></span>

<span data-ttu-id="9f51e-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f51e-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f51e-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-295">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f51e-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-296">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-296">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9f51e-297">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-298">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="9f51e-298">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-299">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9f51e-299">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-301">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="9f51e-301">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9f51e-302">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-303">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9f51e-303">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-306">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="9f51e-306">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9f51e-307">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9f51e-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-309">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9f51e-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-311">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="9f51e-311">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-312">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="9f51e-312">Date and time the object was installed.</span></span> <span data-ttu-id="9f51e-313">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="9f51e-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="9f51e-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f51e-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-315">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9f51e-315">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-316">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9f51e-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-318">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="9f51e-318">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9f51e-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-320">**Name**</span><span class="sxs-lookup"><span data-stu-id="9f51e-320">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-323">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="9f51e-323">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-324">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9f51e-324">Label by which the object is known.</span></span> <span data-ttu-id="9f51e-325">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="9f51e-325">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9f51e-326">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f51e-326">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-327">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9f51e-327">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-330">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9f51e-330">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-331">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-331">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="9f51e-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f51e-333">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9f51e-333">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-334">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9f51e-334">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-335">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9f51e-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-337">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="9f51e-337">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="9f51e-338">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-338">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f51e-339"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9f51e-339"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9f51e-340"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="9f51e-340"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f51e-341"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="9f51e-341"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f51e-342"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="9f51e-342"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-343">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="9f51e-343">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9f51e-344"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="9f51e-344"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-345">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="9f51e-345">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9f51e-346"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="9f51e-346"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-347">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="9f51e-347">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="9f51e-348">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="9f51e-348">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="9f51e-349">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9f51e-349">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9f51e-350"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="9f51e-350"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-351">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="9f51e-351">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9f51e-352"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="9f51e-352"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9f51e-353">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="9f51e-353">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9f51e-354">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9f51e-354">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-355">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9f51e-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-357">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="9f51e-357">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9f51e-358">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="9f51e-358">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9f51e-359">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9f51e-359">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9f51e-360">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="9f51e-360">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="9f51e-361">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-361">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-362">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9f51e-362">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-365">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="9f51e-365">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-366">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9f51e-366">Current status of the object.</span></span> <span data-ttu-id="9f51e-367">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9f51e-367">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9f51e-368">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="9f51e-368">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9f51e-369">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="9f51e-369">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9f51e-370">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="9f51e-370">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9f51e-371">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="9f51e-371">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f51e-372">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9f51e-372">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9f51e-373">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="9f51e-373">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9f51e-374">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="9f51e-374">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9f51e-375">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="9f51e-375">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9f51e-376">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="9f51e-376">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9f51e-377">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="9f51e-377">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9f51e-378">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="9f51e-378">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9f51e-379">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="9f51e-379">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9f51e-380">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="9f51e-380">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f51e-381">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9f51e-381">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-382">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9f51e-382">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-384">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9f51e-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-385">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9f51e-385">State of the logical device.</span></span> <span data-ttu-id="9f51e-386">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="9f51e-386">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="9f51e-387">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9f51e-388">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9f51e-388">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9f51e-389">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9f51e-389">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9f51e-390">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="9f51e-390">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9f51e-391">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="9f51e-391">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9f51e-392">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="9f51e-392">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9f51e-393">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="9f51e-393">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-394">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-396">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f51e-396">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-397">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9f51e-397">Scoping system's creation class name.</span></span>

<span data-ttu-id="9f51e-398">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-398">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9f51e-399">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9f51e-399">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9f51e-400">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9f51e-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9f51e-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9f51e-402">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9f51e-402">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9f51e-403">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="9f51e-403">Scoping system's name.</span></span>

<span data-ttu-id="9f51e-404">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9f51e-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f51e-405">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9f51e-405">Remarks</span></span>

<span data-ttu-id="9f51e-406">Класс **\_ сканера CIM** является производным от [**CIM- \_**](cim-logicaldevice.md)класса.</span><span class="sxs-lookup"><span data-stu-id="9f51e-406">The **CIM\_Scanner** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="9f51e-407">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="9f51e-407">WMI does not implement this class.</span></span>

<span data-ttu-id="9f51e-408">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9f51e-408">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9f51e-409">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9f51e-409">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f51e-410">Требования</span><span class="sxs-lookup"><span data-stu-id="9f51e-410">Requirements</span></span>



| <span data-ttu-id="9f51e-411">Требование</span><span class="sxs-lookup"><span data-stu-id="9f51e-411">Requirement</span></span> | <span data-ttu-id="9f51e-412">Значение</span><span class="sxs-lookup"><span data-stu-id="9f51e-412">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f51e-413">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f51e-413">Minimum supported client</span></span><br/> | <span data-ttu-id="9f51e-414">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f51e-414">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9f51e-415">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f51e-415">Minimum supported server</span></span><br/> | <span data-ttu-id="9f51e-416">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9f51e-416">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9f51e-417">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9f51e-417">Namespace</span></span><br/>                | <span data-ttu-id="9f51e-418">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9f51e-418">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9f51e-419">MOF</span><span class="sxs-lookup"><span data-stu-id="9f51e-419">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f51e-420"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9f51e-420"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f51e-421">DLL</span><span class="sxs-lookup"><span data-stu-id="9f51e-421">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f51e-422"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f51e-422"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f51e-423">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f51e-423">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f51e-424">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="9f51e-424">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

