---
description: Класс CIM \_ потсмодем представляет устройство, которое преобразует двоичные данные в звуковые модуляции для передачи на основе звука, подключаясь к сети "Обычная старая телефонная система" (POTS).
ms.assetid: 2740f305-769d-464c-910a-998522f5121b
ms.tgt_platform: multiple
title: Класс CIM_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_POTSModem
- CIM_POTSModem.AnswerMode
- CIM_POTSModem.Availability
- CIM_POTSModem.Caption
- CIM_POTSModem.CompressionInfo
- CIM_POTSModem.ConfigManagerErrorCode
- CIM_POTSModem.ConfigManagerUserConfig
- CIM_POTSModem.CountriesSupported
- CIM_POTSModem.CountrySelected
- CIM_POTSModem.CreationClassName
- CIM_POTSModem.CurrentPasswords
- CIM_POTSModem.Description
- CIM_POTSModem.DeviceID
- CIM_POTSModem.DialType
- CIM_POTSModem.ErrorCleared
- CIM_POTSModem.ErrorControlInfo
- CIM_POTSModem.ErrorDescription
- CIM_POTSModem.InactivityTimeout
- CIM_POTSModem.InstallDate
- CIM_POTSModem.LastErrorCode
- CIM_POTSModem.MaxBaudRateToPhone
- CIM_POTSModem.MaxBaudRateToSerialPort
- CIM_POTSModem.MaxNumberOfPasswords
- CIM_POTSModem.ModulationScheme
- CIM_POTSModem.Name
- CIM_POTSModem.PNPDeviceID
- CIM_POTSModem.PowerManagementCapabilities
- CIM_POTSModem.PowerManagementSupported
- CIM_POTSModem.RingsBeforeAnswer
- CIM_POTSModem.SpeakerVolumeInfo
- CIM_POTSModem.Status
- CIM_POTSModem.StatusInfo
- CIM_POTSModem.SupportsCallback
- CIM_POTSModem.SupportsSynchronousConnect
- CIM_POTSModem.SystemCreationClassName
- CIM_POTSModem.SystemName
- CIM_POTSModem.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7fbaeedd1de4006dfdccbcec313a7428d7b7f03
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990622"
---
# <a name="cim_potsmodem-class"></a><span data-ttu-id="24368-103">\_Класс CIM потсмодем</span><span class="sxs-lookup"><span data-stu-id="24368-103">CIM\_POTSModem class</span></span>

<span data-ttu-id="24368-104">Класс **CIM \_ потсмодем** представляет устройство, которое преобразует двоичные данные в звуковые модуляции для передачи на основе звука, подключаясь к сети "Обычная старая телефонная система" (POTS).</span><span class="sxs-lookup"><span data-stu-id="24368-104">The **CIM\_POTSModem** class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24368-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="24368-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="24368-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="24368-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="24368-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="24368-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="24368-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="24368-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="24368-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24368-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C546-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_POTSModem : CIM_LogicalDevice
{
  uint16   AnswerMode;
  uint16   Availability;
  string   Caption;
  uint16   CompressionInfo;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  string   Description;
  string   DeviceID;
  uint16   DialType;
  boolean  ErrorCleared;
  uint16   ErrorControlInfo;
  string   ErrorDescription;
  uint32   InactivityTimeout;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint8    RingsBeforeAnswer;
  uint16   SpeakerVolumeInfo;
  string   Status;
  uint16   StatusInfo;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="24368-110">Члены</span><span class="sxs-lookup"><span data-stu-id="24368-110">Members</span></span>

<span data-ttu-id="24368-111">Класс **CIM \_ потсмодем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="24368-111">The **CIM\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="24368-112">Методы</span><span class="sxs-lookup"><span data-stu-id="24368-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="24368-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="24368-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24368-114">Методы</span><span class="sxs-lookup"><span data-stu-id="24368-114">Methods</span></span>

<span data-ttu-id="24368-115">Класс **CIM \_ потсмодем** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="24368-115">The **CIM\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="24368-116">Метод</span><span class="sxs-lookup"><span data-stu-id="24368-116">Method</span></span>                                                               | <span data-ttu-id="24368-117">Описание</span><span class="sxs-lookup"><span data-stu-id="24368-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24368-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="24368-118">**Reset**</span></span>](reset-method-in-class-cim-potsmodem.md)                 | <span data-ttu-id="24368-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="24368-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="24368-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="24368-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="24368-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-potsmodem.md) | <span data-ttu-id="24368-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="24368-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="24368-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="24368-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="24368-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="24368-124">Properties</span></span>

<span data-ttu-id="24368-125">Класс **CIM \_ потсмодем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="24368-125">The **CIM\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="24368-126">**ансвермоде**</span><span class="sxs-lookup"><span data-stu-id="24368-126">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-129">Текущий параметр автоматического ответа или обратного вызова для модема.</span><span class="sxs-lookup"><span data-stu-id="24368-129">Current auto-answer or call-back setting for the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-130">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-131">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="24368-132">**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-132">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="24368-133">**Ответ вручную** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-133">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="24368-134">**Автоматический ответ** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-134">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="24368-135">**Автоматический ответ с обратным вызовом** (5)</span><span class="sxs-lookup"><span data-stu-id="24368-135">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-136">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="24368-136">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-139">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="24368-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="24368-140">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-140">Availability and status of the device.</span></span>

<span data-ttu-id="24368-141">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-141">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-142"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-143"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="24368-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-144"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="24368-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-145"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="24368-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="24368-146"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="24368-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="24368-147"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="24368-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="24368-148"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="24368-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="24368-149"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="24368-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="24368-150"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="24368-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="24368-151"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="24368-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="24368-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="24368-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="24368-153"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="24368-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="24368-154"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="24368-155">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="24368-155">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="24368-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="24368-156"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="24368-157">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="24368-157">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="24368-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="24368-158"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="24368-159">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="24368-159">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="24368-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="24368-160"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="24368-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="24368-161"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="24368-162">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="24368-162">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="24368-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="24368-163"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="24368-164">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="24368-164">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="24368-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="24368-165"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="24368-166">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="24368-166">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="24368-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="24368-167"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="24368-168">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="24368-168">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="24368-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="24368-169"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="24368-170">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="24368-170">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-171">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="24368-171">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-174">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="24368-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="24368-175">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="24368-175">Short textual description of the object.</span></span>

<span data-ttu-id="24368-176">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24368-176">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-177">**компрессионинфо**</span><span class="sxs-lookup"><span data-stu-id="24368-177">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-178">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-178">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-180">Характеристики сжатия данных модема.</span><span class="sxs-lookup"><span data-stu-id="24368-180">Data compression characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-181">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-182">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="24368-183">**Без сжатия** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-183">**No Compression** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="24368-184">**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-184">**MNP 5** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="24368-185">**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-185">**V.42bis** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-186">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="24368-186">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-187">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24368-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24368-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-189">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="24368-189">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="24368-190">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="24368-190">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="24368-191">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-191">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="24368-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="24368-192"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="24368-193"> (0)</span><span class="sxs-lookup"><span data-stu-id="24368-193">(0)</span></span>


</dt> <dd>

<span data-ttu-id="24368-194">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="24368-194">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="24368-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="24368-195"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="24368-196">(1)</span><span class="sxs-lookup"><span data-stu-id="24368-196">(1)</span></span>


</dt> <dd>

<span data-ttu-id="24368-197">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="24368-197">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="24368-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-198"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="24368-199">(2)</span><span class="sxs-lookup"><span data-stu-id="24368-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="24368-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="24368-200"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="24368-201">(3)</span><span class="sxs-lookup"><span data-stu-id="24368-201">(3)</span></span>


</dt> <dd>

<span data-ttu-id="24368-202">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24368-202">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="24368-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="24368-203"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="24368-204">(4)</span><span class="sxs-lookup"><span data-stu-id="24368-204">(4)</span></span>


</dt> <dd>

<span data-ttu-id="24368-205">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="24368-205">Device is not working properly.</span></span> <span data-ttu-id="24368-206">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="24368-206">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="24368-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="24368-207"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="24368-208">(5)</span><span class="sxs-lookup"><span data-stu-id="24368-208">(5)</span></span>


</dt> <dd>

<span data-ttu-id="24368-209">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="24368-209">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="24368-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="24368-210"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="24368-211"> (6)</span><span class="sxs-lookup"><span data-stu-id="24368-211">(6)</span></span>


</dt> <dd>

<span data-ttu-id="24368-212">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="24368-212">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="24368-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="24368-213"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="24368-214">(7)</span><span class="sxs-lookup"><span data-stu-id="24368-214">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="24368-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-215"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="24368-216">(8)</span><span class="sxs-lookup"><span data-stu-id="24368-216">(8)</span></span>


</dt> <dd>

<span data-ttu-id="24368-217">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-217">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="24368-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-218"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="24368-219">(9)</span><span class="sxs-lookup"><span data-stu-id="24368-219">(9)</span></span>


</dt> <dd>

<span data-ttu-id="24368-220">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="24368-220">Device is not working properly.</span></span> <span data-ttu-id="24368-221">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-221">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="24368-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="24368-222"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="24368-223">(10)</span><span class="sxs-lookup"><span data-stu-id="24368-223">(10)</span></span>


</dt> <dd>

<span data-ttu-id="24368-224">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="24368-224">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="24368-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-225"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="24368-226">(11)</span><span class="sxs-lookup"><span data-stu-id="24368-226">(11)</span></span>


</dt> <dd>

<span data-ttu-id="24368-227">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-227">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="24368-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="24368-228"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="24368-229">(12)</span><span class="sxs-lookup"><span data-stu-id="24368-229">(12)</span></span>


</dt> <dd>

<span data-ttu-id="24368-230">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="24368-230">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="24368-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-231"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="24368-232">(13)</span><span class="sxs-lookup"><span data-stu-id="24368-232">(13)</span></span>


</dt> <dd>

<span data-ttu-id="24368-233">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-233">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="24368-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="24368-234"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="24368-235">(14)</span><span class="sxs-lookup"><span data-stu-id="24368-235">(14)</span></span>


</dt> <dd>

<span data-ttu-id="24368-236">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="24368-236">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="24368-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="24368-237"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="24368-238">(15)</span><span class="sxs-lookup"><span data-stu-id="24368-238">(15)</span></span>


</dt> <dd>

<span data-ttu-id="24368-239">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="24368-239">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="24368-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="24368-240"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="24368-241">(16)</span><span class="sxs-lookup"><span data-stu-id="24368-241">(16)</span></span>


</dt> <dd>

<span data-ttu-id="24368-242">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="24368-242">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="24368-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="24368-243"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="24368-244">(17)</span><span class="sxs-lookup"><span data-stu-id="24368-244">(17)</span></span>


</dt> <dd>

<span data-ttu-id="24368-245">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="24368-245">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="24368-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-246"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="24368-247">(18)</span><span class="sxs-lookup"><span data-stu-id="24368-247">(18)</span></span>


</dt> <dd>

<span data-ttu-id="24368-248">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="24368-248">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="24368-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="24368-249"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="24368-250">(19)</span><span class="sxs-lookup"><span data-stu-id="24368-250">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="24368-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="24368-251"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="24368-252">(20)</span><span class="sxs-lookup"><span data-stu-id="24368-252">(20)</span></span>


</dt> <dd>

<span data-ttu-id="24368-253">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="24368-253">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="24368-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="24368-254"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="24368-255">(21)</span><span class="sxs-lookup"><span data-stu-id="24368-255">(21)</span></span>


</dt> <dd>

<span data-ttu-id="24368-256">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="24368-256">System failure.</span></span> <span data-ttu-id="24368-257">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="24368-257">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="24368-258">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="24368-258">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="24368-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="24368-259"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="24368-260">(22)</span><span class="sxs-lookup"><span data-stu-id="24368-260">(22)</span></span>


</dt> <dd>

<span data-ttu-id="24368-261">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="24368-261">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="24368-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="24368-262"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="24368-263">(23)</span><span class="sxs-lookup"><span data-stu-id="24368-263">(23)</span></span>


</dt> <dd>

<span data-ttu-id="24368-264">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="24368-264">System failure.</span></span> <span data-ttu-id="24368-265">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="24368-265">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="24368-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="24368-266"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="24368-267">(24)</span><span class="sxs-lookup"><span data-stu-id="24368-267">(24)</span></span>


</dt> <dd>

<span data-ttu-id="24368-268">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="24368-268">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="24368-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="24368-269"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="24368-270">(25)</span><span class="sxs-lookup"><span data-stu-id="24368-270">(25)</span></span>


</dt> <dd>

<span data-ttu-id="24368-271">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="24368-271">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="24368-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="24368-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="24368-273">(26)</span><span class="sxs-lookup"><span data-stu-id="24368-273">(26)</span></span>


</dt> <dd>

<span data-ttu-id="24368-274">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="24368-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="24368-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="24368-275"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="24368-276">(27)</span><span class="sxs-lookup"><span data-stu-id="24368-276">(27)</span></span>


</dt> <dd>

<span data-ttu-id="24368-277">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="24368-277">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="24368-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="24368-278"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="24368-279">(28)</span><span class="sxs-lookup"><span data-stu-id="24368-279">(28)</span></span>


</dt> <dd>

<span data-ttu-id="24368-280">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="24368-280">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="24368-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="24368-281"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="24368-282">(29)</span><span class="sxs-lookup"><span data-stu-id="24368-282">(29)</span></span>


</dt> <dd>

<span data-ttu-id="24368-283">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="24368-283">Device is disabled.</span></span> <span data-ttu-id="24368-284">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="24368-284">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="24368-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="24368-285"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="24368-286">(30)</span><span class="sxs-lookup"><span data-stu-id="24368-286">(30)</span></span>


</dt> <dd>

<span data-ttu-id="24368-287">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="24368-287">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="24368-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="24368-288"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="24368-289">1-31</span><span class="sxs-lookup"><span data-stu-id="24368-289">(31)</span></span>


</dt> <dd>

<span data-ttu-id="24368-290">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="24368-290">Device is not working properly.</span></span> <span data-ttu-id="24368-291">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="24368-291">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-292">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="24368-292">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-293">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="24368-293">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24368-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-295">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="24368-295">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="24368-296">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="24368-296">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="24368-297">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-297">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-298">**каунтриессуппортед**</span><span class="sxs-lookup"><span data-stu-id="24368-298">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-299">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="24368-299">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24368-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-301">Страны или регионы, в которых может действовать модем.</span><span class="sxs-lookup"><span data-stu-id="24368-301">Countries or regions in which the modem can operate.</span></span>

</dd> <dt>

<span data-ttu-id="24368-302">**каунтриселектед**</span><span class="sxs-lookup"><span data-stu-id="24368-302">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-303">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-305">Страна или регион, для которых в настоящее время программируется модем.</span><span class="sxs-lookup"><span data-stu-id="24368-305">Country or region for which the modem is currently programmed.</span></span> <span data-ttu-id="24368-306">Если поддерживается несколько стран или регионов, это свойство определяет, какая из них выбрана в данный момент для использования.</span><span class="sxs-lookup"><span data-stu-id="24368-306">When multiple countries or regions are supported, this property defines which one is currently selected for use.</span></span>

</dd> <dt>

<span data-ttu-id="24368-307">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="24368-307">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-310">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24368-310">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24368-311">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="24368-311">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="24368-312">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="24368-312">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="24368-313">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-313">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-314">**куррентпассвордс**</span><span class="sxs-lookup"><span data-stu-id="24368-314">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-315">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="24368-315">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="24368-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-317">Определенные в данный момент пароли для модема.</span><span class="sxs-lookup"><span data-stu-id="24368-317">Currently defined passwords for the modem.</span></span> <span data-ttu-id="24368-318">Этот массив можно оставить пустым по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="24368-318">This array can be left blank for security reasons.</span></span>

</dd> <dt>

<span data-ttu-id="24368-319">**Описание**</span><span class="sxs-lookup"><span data-stu-id="24368-319">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-322">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="24368-322">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="24368-323">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="24368-323">Textual description of the object.</span></span>

<span data-ttu-id="24368-324">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24368-324">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-325">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="24368-325">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-328">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24368-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24368-329">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-329">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="24368-330">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-331">**диалтипе**</span><span class="sxs-lookup"><span data-stu-id="24368-331">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-332">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-332">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-334">Тип используемого набора номера.</span><span class="sxs-lookup"><span data-stu-id="24368-334">Type of dialing that is used.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-335">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-335">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="24368-336">**Тон** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-336">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="24368-337">**Импульс** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-337">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-338">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="24368-338">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-339">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="24368-339">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24368-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-341">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="24368-341">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="24368-342">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-342">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-343">**еррорконтролинфо**</span><span class="sxs-lookup"><span data-stu-id="24368-343">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-344">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-346">Характеристики исправления ошибок модема.</span><span class="sxs-lookup"><span data-stu-id="24368-346">Error correction characteristics of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-347">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-347">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-348">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-348">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="24368-349">**Без исправления ошибок** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-349">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="24368-350">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-350">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="24368-351">**Лапм** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-351">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-352">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="24368-352">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-355">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="24368-355">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="24368-356">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-356">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-357">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="24368-357">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-358">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24368-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24368-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-360">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="24368-360">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="24368-361">Ограничение времени (в секундах) автоматического отключения телефонной линии, если обмен данными не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24368-361">Time limit (in seconds) for automatic disconnection of the phone line if no data is exchanged.</span></span> <span data-ttu-id="24368-362">Значение 0 (ноль) указывает, что эта функция имеется, но не включена.</span><span class="sxs-lookup"><span data-stu-id="24368-362">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="24368-363">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="24368-363">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-364">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="24368-364">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24368-365">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-366">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="24368-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="24368-367">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="24368-367">Date and time the object was installed.</span></span> <span data-ttu-id="24368-368">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="24368-368">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="24368-369">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24368-369">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-370">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="24368-370">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-371">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24368-371">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24368-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-373">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="24368-373">Last error code reported by the logical device.</span></span>

<span data-ttu-id="24368-374">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-375">**максбаудратетофоне**</span><span class="sxs-lookup"><span data-stu-id="24368-375">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-376">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24368-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24368-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-378">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="24368-378">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="24368-379">Максимальная настраиваемая скорость связи для доступа к телефонной системе.</span><span class="sxs-lookup"><span data-stu-id="24368-379">Maximum settable communication speed for accessing the phone system.</span></span>

</dd> <dt>

<span data-ttu-id="24368-380">**максбаудратетосериалпорт**</span><span class="sxs-lookup"><span data-stu-id="24368-380">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-381">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="24368-381">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="24368-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-383">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="24368-383">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="24368-384">Максимальная настраиваемая скорость обмена данными с COM-портом для внешнего модема.</span><span class="sxs-lookup"><span data-stu-id="24368-384">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="24368-385">Введите 0 (ноль), если это не применимо.</span><span class="sxs-lookup"><span data-stu-id="24368-385">Enter 0 (zero) if not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="24368-386">**макснумберофпассвордс**</span><span class="sxs-lookup"><span data-stu-id="24368-386">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-387">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-387">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-389">Максимальное число паролей, определяемое самим модемом.</span><span class="sxs-lookup"><span data-stu-id="24368-389">Maximum number of passwords definable in the modem itself.</span></span> <span data-ttu-id="24368-390">Если эта функция не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="24368-390">If this feature is not supported, enter 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="24368-391">**модулатионсчеме**</span><span class="sxs-lookup"><span data-stu-id="24368-391">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-392">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-393">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-394">Схема модуляции модема.</span><span class="sxs-lookup"><span data-stu-id="24368-394">Modulation scheme of the modem.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-395">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-395">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-396">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-396">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="24368-397">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-397">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="24368-398">**Звонок 103** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-398">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="24368-399">**Колокольчик 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-399">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="24368-400">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="24368-400">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="24368-401">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="24368-401">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="24368-402">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="24368-402">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="24368-403">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="24368-403">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="24368-404">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="24368-404">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="24368-405">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="24368-405">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="24368-406">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="24368-406">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-407">**Name**</span><span class="sxs-lookup"><span data-stu-id="24368-407">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-408">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-409">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-410">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="24368-410">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="24368-411">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="24368-411">Label by which the object is known.</span></span> <span data-ttu-id="24368-412">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="24368-412">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="24368-413">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24368-413">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-414">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="24368-414">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-417">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="24368-417">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="24368-418">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-418">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="24368-419">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="24368-420">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="24368-420">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="24368-421">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="24368-421">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-422">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="24368-422">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="24368-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-424">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="24368-424">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="24368-425">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-425">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-426"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="24368-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-427"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="24368-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-428"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="24368-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-429"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="24368-430">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="24368-430">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="24368-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="24368-431"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="24368-432">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="24368-432">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="24368-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="24368-433"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="24368-434">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="24368-434">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="24368-435">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="24368-435">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="24368-436">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="24368-436">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="24368-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="24368-437"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="24368-438">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="24368-438">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="24368-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="24368-439"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="24368-440">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="24368-440">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-441">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="24368-441">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-442">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="24368-442">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24368-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-444">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="24368-444">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="24368-445">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="24368-445">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="24368-446">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="24368-446">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="24368-447">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="24368-447">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="24368-448">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-449">**рингсбефореансвер**</span><span class="sxs-lookup"><span data-stu-id="24368-449">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-450">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="24368-450">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="24368-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-451">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-452">Число звонков перед ответом модема на входящий вызов.</span><span class="sxs-lookup"><span data-stu-id="24368-452">Number of rings before the modem answers an incoming call.</span></span>

</dd> <dt>

<span data-ttu-id="24368-453">**спеакерволумеинфо**</span><span class="sxs-lookup"><span data-stu-id="24368-453">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-455">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-456">Уровень громкости звуковых тонов модема.</span><span class="sxs-lookup"><span data-stu-id="24368-456">Volume level of the audible tones from the modem.</span></span> <span data-ttu-id="24368-457">Например, можно сообщить о высоком, среднем или низком объеме.</span><span class="sxs-lookup"><span data-stu-id="24368-457">For example, high, medium, or low volume can be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-458">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="24368-458">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-459">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-459">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="24368-460">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-460">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="24368-461">**Высокий** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-461">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="24368-462">**Средний** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-462">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="24368-463">**Низкий** (5)</span><span class="sxs-lookup"><span data-stu-id="24368-463">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="24368-464">**Выкл** . (6)</span><span class="sxs-lookup"><span data-stu-id="24368-464">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="24368-465">**Авто** (7)</span><span class="sxs-lookup"><span data-stu-id="24368-465">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-466">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="24368-466">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-467">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-469">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="24368-469">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="24368-470">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="24368-470">Current status of the object.</span></span> <span data-ttu-id="24368-471">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="24368-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="24368-472">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="24368-472">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="24368-473">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="24368-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="24368-474">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="24368-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="24368-475">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="24368-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-476">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="24368-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="24368-477">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="24368-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="24368-478">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="24368-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="24368-479">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="24368-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="24368-480">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="24368-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="24368-481">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="24368-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="24368-482">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="24368-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="24368-483">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="24368-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="24368-484">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="24368-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="24368-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-486">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="24368-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="24368-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-488">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="24368-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="24368-489">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="24368-489">State of the logical device.</span></span> <span data-ttu-id="24368-490">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="24368-490">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="24368-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="24368-492">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="24368-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="24368-493">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="24368-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="24368-494">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="24368-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="24368-495">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="24368-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="24368-496">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="24368-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="24368-497">**суппортскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="24368-497">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-498">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="24368-498">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24368-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-499">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-500">Если **значение равно true**, модем поддерживает обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="24368-500">If **TRUE**, the modem supports call-back.</span></span>

</dd> <dt>

<span data-ttu-id="24368-501">**суппортссинчронаусконнект**</span><span class="sxs-lookup"><span data-stu-id="24368-501">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-502">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="24368-502">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="24368-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-503">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-504">При **значении true** синхронное, а также асинхронное взаимодействие поддерживается.</span><span class="sxs-lookup"><span data-stu-id="24368-504">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

</dd> <dt>

<span data-ttu-id="24368-505">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="24368-505">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-506">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-506">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-507">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-507">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-508">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24368-508">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24368-509">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="24368-509">Scoping system's creation class name.</span></span>

<span data-ttu-id="24368-510">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-510">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-511">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="24368-511">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-512">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="24368-512">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24368-513">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24368-514">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="24368-514">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="24368-515">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="24368-515">Scoping system's name.</span></span>

<span data-ttu-id="24368-516">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="24368-516">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="24368-517">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="24368-517">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24368-518">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="24368-518">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="24368-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="24368-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="24368-520">Дата и время последнего сброса этого контроллера.</span><span class="sxs-lookup"><span data-stu-id="24368-520">Date and time this controller was last reset.</span></span> <span data-ttu-id="24368-521">Это может означать, что контроллер был выключен или повторно инициализирован.</span><span class="sxs-lookup"><span data-stu-id="24368-521">This could mean the controller was powered down, or reinitialized.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24368-522">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24368-522">Remarks</span></span>

<span data-ttu-id="24368-523">Класс **CIM \_ потсмодем** является производным от [**CIM \_**](cim-logicaldevice.md)-класса.</span><span class="sxs-lookup"><span data-stu-id="24368-523">The **CIM\_POTSModem** class is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="24368-524">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="24368-524">WMI does not implement this class.</span></span> <span data-ttu-id="24368-525">Классы WMI, производные от **CIM \_ потсмодем**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="24368-525">For WMI classes derived from **CIM\_POTSModem**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="24368-526">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="24368-526">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="24368-527">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="24368-527">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="24368-528">Требования</span><span class="sxs-lookup"><span data-stu-id="24368-528">Requirements</span></span>



| <span data-ttu-id="24368-529">Требование</span><span class="sxs-lookup"><span data-stu-id="24368-529">Requirement</span></span> | <span data-ttu-id="24368-530">Значение</span><span class="sxs-lookup"><span data-stu-id="24368-530">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24368-531">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24368-531">Minimum supported client</span></span><br/> | <span data-ttu-id="24368-532">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24368-532">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24368-533">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24368-533">Minimum supported server</span></span><br/> | <span data-ttu-id="24368-534">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24368-534">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24368-535">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="24368-535">Namespace</span></span><br/>                | <span data-ttu-id="24368-536">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="24368-536">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24368-537">MOF</span><span class="sxs-lookup"><span data-stu-id="24368-537">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24368-538"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24368-538"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24368-539">DLL</span><span class="sxs-lookup"><span data-stu-id="24368-539">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24368-540"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24368-540"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24368-541">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24368-541">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24368-542">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="24368-542">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

