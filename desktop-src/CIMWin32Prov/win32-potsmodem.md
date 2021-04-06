---
description: '\_Класс WMI потсмодем инструментария Win32 представляет службы и характеристики модема простой старой телефонной службы (POTS) в компьютерной системе под Windows.'
ms.assetid: 24589942-e2c3-477e-8179-59ae4a4aa85a
ms.tgt_platform: multiple
title: Класс Win32_POTSModem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModem
- Win32_POTSModem.Reset
- Win32_POTSModem.SetPowerState
- Win32_POTSModem.AnswerMode
- Win32_POTSModem.AttachedTo
- Win32_POTSModem.Availability
- Win32_POTSModem.BlindOff
- Win32_POTSModem.BlindOn
- Win32_POTSModem.Caption
- Win32_POTSModem.CompatibilityFlags
- Win32_POTSModem.CompressionInfo
- Win32_POTSModem.CompressionOff
- Win32_POTSModem.CompressionOn
- Win32_POTSModem.ConfigManagerErrorCode
- Win32_POTSModem.ConfigManagerUserConfig
- Win32_POTSModem.ConfigurationDialog
- Win32_POTSModem.CountriesSupported
- Win32_POTSModem.CountrySelected
- Win32_POTSModem.CreationClassName
- Win32_POTSModem.CurrentPasswords
- Win32_POTSModem.DCB
- Win32_POTSModem.Default
- Win32_POTSModem.Description
- Win32_POTSModem.DeviceID
- Win32_POTSModem.DeviceLoader
- Win32_POTSModem.DeviceType
- Win32_POTSModem.DialType
- Win32_POTSModem.DriverDate
- Win32_POTSModem.ErrorCleared
- Win32_POTSModem.ErrorControlForced
- Win32_POTSModem.ErrorControlInfo
- Win32_POTSModem.ErrorControlOff
- Win32_POTSModem.ErrorControlOn
- Win32_POTSModem.ErrorDescription
- Win32_POTSModem.FlowControlHard
- Win32_POTSModem.FlowControlOff
- Win32_POTSModem.FlowControlSoft
- Win32_POTSModem.InactivityScale
- Win32_POTSModem.InactivityTimeout
- Win32_POTSModem.Index
- Win32_POTSModem.IndexEx
- Win32_POTSModem.InstallDate
- Win32_POTSModem.LastErrorCode
- Win32_POTSModem.MaxBaudRateToPhone
- Win32_POTSModem.MaxBaudRateToSerialPort
- Win32_POTSModem.MaxNumberOfPasswords
- Win32_POTSModem.Model
- Win32_POTSModem.ModemInfPath
- Win32_POTSModem.ModemInfSection
- Win32_POTSModem.ModulationBell
- Win32_POTSModem.ModulationCCITT
- Win32_POTSModem.ModulationScheme
- Win32_POTSModem.Name
- Win32_POTSModem.PNPDeviceID
- Win32_POTSModem.PortSubClass
- Win32_POTSModem.PowerManagementCapabilities
- Win32_POTSModem.PowerManagementSupported
- Win32_POTSModem.Prefix
- Win32_POTSModem.Properties
- Win32_POTSModem.ProviderName
- Win32_POTSModem.Pulse
- Win32_POTSModem.Reset
- Win32_POTSModem.ResponsesKeyName
- Win32_POTSModem.RingsBeforeAnswer
- Win32_POTSModem.SpeakerModeDial
- Win32_POTSModem.SpeakerModeOff
- Win32_POTSModem.SpeakerModeOn
- Win32_POTSModem.SpeakerModeSetup
- Win32_POTSModem.SpeakerVolumeHigh
- Win32_POTSModem.SpeakerVolumeInfo
- Win32_POTSModem.SpeakerVolumeLow
- Win32_POTSModem.SpeakerVolumeMed
- Win32_POTSModem.Status
- Win32_POTSModem.StatusInfo
- Win32_POTSModem.StringFormat
- Win32_POTSModem.SupportsCallback
- Win32_POTSModem.SupportsSynchronousConnect
- Win32_POTSModem.SystemCreationClassName
- Win32_POTSModem.SystemName
- Win32_POTSModem.Terminator
- Win32_POTSModem.TimeOfLastReset
- Win32_POTSModem.Tone
- Win32_POTSModem.VoiceSwitchFeature
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6ec9634c5ee86d6819bf8f7a45dd521276565903
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895950"
---
# <a name="win32_potsmodem-class"></a><span data-ttu-id="419de-103">\_Класс Win32 потсмодем</span><span class="sxs-lookup"><span data-stu-id="419de-103">Win32\_POTSModem class</span></span>

<span data-ttu-id="419de-104">Класс **WMI \_ потсмодем** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет службы и характеристики модема простой старой телефонной службы (POTS) в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="419de-104">The **Win32\_POTSModem** [WMI class](../wmisdk/retrieving-a-class.md) represents the services and characteristics of a Plain Old Telephone Service (POTS) modem on a computer system running Windows.</span></span>

<span data-ttu-id="419de-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="419de-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="419de-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="419de-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="419de-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="419de-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModem : CIM_PotsModem
{
  uint16   AnswerMode;
  string   AttachedTo;
  uint16   Availability;
  string   BlindOff;
  string   BlindOn;
  string   Caption;
  string   CompatibilityFlags;
  uint16   CompressionInfo;
  string   CompressionOff;
  string   CompressionOn;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   ConfigurationDialog;
  string   CountriesSupported[];
  string   CountrySelected;
  string   CreationClassName;
  string   CurrentPasswords[];
  uint8    DCB[];
  uint8    Default[];
  string   Description;
  string   DeviceID;
  string   DeviceLoader;
  string   DeviceType;
  uint16   DialType;
  datetime DriverDate;
  boolean  ErrorCleared;
  string   ErrorControlForced;
  uint16   ErrorControlInfo;
  string   ErrorControlOff;
  string   ErrorControlOn;
  string   ErrorDescription;
  string   FlowControlHard;
  string   FlowControlOff;
  string   FlowControlSoft;
  string   InactivityScale;
  uint32   InactivityTimeout;
  uint32   Index;
  string   IndexEx;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRateToPhone;
  uint32   MaxBaudRateToSerialPort;
  uint16   MaxNumberOfPasswords;
  string   Model;
  string   ModemInfPath;
  string   ModemInfSection;
  string   ModulationBell;
  string   ModulationCCITT;
  uint16   ModulationScheme;
  string   Name;
  string   PNPDeviceID;
  string   PortSubClass;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Prefix;
  uint8    Properties[];
  string   ProviderName;
  string   Pulse;
  string   Reset;
  string   ResponsesKeyName;
  uint8    RingsBeforeAnswer;
  string   SpeakerModeDial;
  string   SpeakerModeOff;
  string   SpeakerModeOn;
  string   SpeakerModeSetup;
  string   SpeakerVolumeHigh;
  uint16   SpeakerVolumeInfo;
  string   SpeakerVolumeLow;
  string   SpeakerVolumeMed;
  string   Status;
  uint16   StatusInfo;
  string   StringFormat;
  boolean  SupportsCallback;
  boolean  SupportsSynchronousConnect;
  string   SystemCreationClassName;
  string   SystemName;
  string   Terminator;
  datetime TimeOfLastReset;
  string   Tone;
  string   VoiceSwitchFeature;
};
```

## <a name="members"></a><span data-ttu-id="419de-108">Члены</span><span class="sxs-lookup"><span data-stu-id="419de-108">Members</span></span>

<span data-ttu-id="419de-109">Класс **Win32 \_ потсмодем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="419de-109">The **Win32\_POTSModem** class has these types of members:</span></span>

-   [<span data-ttu-id="419de-110">Методы</span><span class="sxs-lookup"><span data-stu-id="419de-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="419de-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="419de-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="419de-112">Методы</span><span class="sxs-lookup"><span data-stu-id="419de-112">Methods</span></span>

<span data-ttu-id="419de-113">Класс **Win32 \_ потсмодем** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="419de-113">The **Win32\_POTSModem** class has these methods.</span></span>



| <span data-ttu-id="419de-114">Метод</span><span class="sxs-lookup"><span data-stu-id="419de-114">Method</span></span>            | <span data-ttu-id="419de-115">Описание</span><span class="sxs-lookup"><span data-stu-id="419de-115">Description</span></span>                                                                                                                                                                            |
|:------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="419de-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="419de-116">**Reset**</span></span>         | <span data-ttu-id="419de-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="419de-117">Not implemented.</span></span> <span data-ttu-id="419de-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/>                 |
| <span data-ttu-id="419de-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="419de-119">**SetPowerState**</span></span> | <span data-ttu-id="419de-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="419de-120">Not implemented.</span></span> <span data-ttu-id="419de-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PotsModem**](cim-potsmodem.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="419de-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="419de-122">Properties</span></span>

<span data-ttu-id="419de-123">Класс **Win32 \_ потсмодем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="419de-123">The **Win32\_POTSModem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="419de-124">**ансвермоде**</span><span class="sxs-lookup"><span data-stu-id="419de-124">**AnswerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-127">Текущий параметр автоматического ответа или ответного вызова для модема.</span><span class="sxs-lookup"><span data-stu-id="419de-127">Current auto-answer or callback setting for the modem.</span></span>

<span data-ttu-id="419de-128">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-128">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-129">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-129">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-130">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-130">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="419de-131">**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-131">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Answer"></span><span id="manual_answer"></span><span id="MANUAL_ANSWER"></span>

<span data-ttu-id="419de-132">**Ответ вручную** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-132">**Manual Answer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer"></span><span id="auto_answer"></span><span id="AUTO_ANSWER"></span>

<span data-ttu-id="419de-133">**Автоматический ответ** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-133">**Auto Answer** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto_Answer_with_Call-Back"></span><span id="auto_answer_with_call-back"></span><span id="AUTO_ANSWER_WITH_CALL-BACK"></span>

<span data-ttu-id="419de-134">**Автоматический ответ с обратным вызовом** (5)</span><span class="sxs-lookup"><span data-stu-id="419de-134">**Auto Answer with Call-Back** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-135">**AttachedTo**</span><span class="sxs-lookup"><span data-stu-id="419de-135">**AttachedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-138">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| аттачедто")</span><span class="sxs-lookup"><span data-stu-id="419de-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|AttachedTo")</span></span>
</dt> </dl>

<span data-ttu-id="419de-139">Порт, к которому подключен POTS-модем.</span><span class="sxs-lookup"><span data-stu-id="419de-139">Port to which the POTS modem is attached.</span></span>

<span data-ttu-id="419de-140">Пример: "COM1"</span><span class="sxs-lookup"><span data-stu-id="419de-140">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="419de-141">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="419de-141">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-142">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-144">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="419de-144">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="419de-145">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-145">Availability and status of the device.</span></span>

<span data-ttu-id="419de-146">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-146">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-147"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="419de-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-149"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="419de-150">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="419de-150">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="419de-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="419de-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="419de-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="419de-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="419de-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="419de-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="419de-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="419de-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="419de-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="419de-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="419de-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="419de-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="419de-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="419de-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="419de-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="419de-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="419de-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="419de-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="419de-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="419de-161">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="419de-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="419de-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="419de-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="419de-163">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="419de-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="419de-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="419de-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="419de-165">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="419de-165">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="419de-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="419de-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="419de-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="419de-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="419de-168">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="419de-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="419de-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="419de-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="419de-170">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="419de-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="419de-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="419de-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="419de-172">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="419de-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="419de-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="419de-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="419de-174">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="419de-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="419de-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="419de-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="419de-176">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="419de-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-177">**блиндофф**</span><span class="sxs-lookup"><span data-stu-id="419de-177">**BlindOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-180">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| блиндофф")</span><span class="sxs-lookup"><span data-stu-id="419de-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOff")</span></span>
</dt> </dl>

<span data-ttu-id="419de-181">Командная строка, используемая для обнаружения гудка в наборе перед набором номера.</span><span class="sxs-lookup"><span data-stu-id="419de-181">Command string used to detect a dial tone before dialing.</span></span>

<span data-ttu-id="419de-182">Пример: X4</span><span class="sxs-lookup"><span data-stu-id="419de-182">Example: "X4"</span></span>

</dd> <dt>

<span data-ttu-id="419de-183">**блиндон**</span><span class="sxs-lookup"><span data-stu-id="419de-183">**BlindOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-186">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| блиндон")</span><span class="sxs-lookup"><span data-stu-id="419de-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|BlindOn")</span></span>
</dt> </dl>

<span data-ttu-id="419de-187">Командная строка, используемая для набираемого номера.</span><span class="sxs-lookup"><span data-stu-id="419de-187">Command string used to dial whether or not there is a dial tone.</span></span>

<span data-ttu-id="419de-188">Пример: "X3"</span><span class="sxs-lookup"><span data-stu-id="419de-188">Example: "X3"</span></span>

</dd> <dt>

<span data-ttu-id="419de-189">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="419de-189">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-190">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-192">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="419de-192">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="419de-193">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="419de-193">Short description of the object.</span></span>

<span data-ttu-id="419de-194">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="419de-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-195">**CompatibilityFlags**</span><span class="sxs-lookup"><span data-stu-id="419de-195">**CompatibilityFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-198">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| компатибилитифлагс")</span><span class="sxs-lookup"><span data-stu-id="419de-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|CompatibilityFlags")</span></span>
</dt> </dl>

<span data-ttu-id="419de-199">Все протоколы модемного подключения, с которыми совместимо это модемное устройство.</span><span class="sxs-lookup"><span data-stu-id="419de-199">All modem connection protocols with which this modem device is compatible.</span></span>

</dd> <dt>

<span data-ttu-id="419de-200">**компрессионинфо**</span><span class="sxs-lookup"><span data-stu-id="419de-200">**CompressionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-201">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-203">Характеристики сжатия данных модема.</span><span class="sxs-lookup"><span data-stu-id="419de-203">Data compression characteristics of the modem.</span></span>

<span data-ttu-id="419de-204">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-204">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-205"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-206"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="419de-207">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="419de-207">Unknown</span></span>

</dd> <dt>

<span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>

<span data-ttu-id="419de-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**Без сжатия** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-208"><span id="No_Compression"></span><span id="no_compression"></span><span id="NO_COMPRESSION"></span>**No Compression** (2)</span></span>


</dt> <dd>

<span data-ttu-id="419de-209">Другое</span><span class="sxs-lookup"><span data-stu-id="419de-209">Other</span></span>

</dd> <dt>

<span id="MNP_5"></span><span id="mnp_5"></span>

<span data-ttu-id="419de-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-210"><span id="MNP_5"></span><span id="mnp_5"></span>**MNP 5** (3)</span></span>


</dt> <dd>

<span data-ttu-id="419de-211">Без сжатия</span><span class="sxs-lookup"><span data-stu-id="419de-211">No Compression</span></span>

</dd> <dt>

<span id="V.42bis"></span><span id="v.42bis"></span><span id="V.42BIS"></span>

<span data-ttu-id="419de-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V. 42bis** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-212"><span id="v.42bis"></span><span id="V.42BIS"></span>**V.42bis** (4)</span></span>


</dt> <dd>

<span data-ttu-id="419de-213">MNP 5</span><span class="sxs-lookup"><span data-stu-id="419de-213">MNP 5</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="419de-214"><span id="5"></span>**5.0**</span><span class="sxs-lookup"><span data-stu-id="419de-214"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="419de-215">V. 42bis</span><span class="sxs-lookup"><span data-stu-id="419de-215">V.42bis</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-216">**компрессионофф**</span><span class="sxs-lookup"><span data-stu-id="419de-216">**CompressionOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-219">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ \\ \\ класса Control \| Compression \_ Off")</span><span class="sxs-lookup"><span data-stu-id="419de-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="419de-220">Строка команды, используемая для отключения аппаратного сжатия данных.</span><span class="sxs-lookup"><span data-stu-id="419de-220">Command string used to disable hardware data compression.</span></span>

<span data-ttu-id="419de-221">Пример: "S46 = 136"</span><span class="sxs-lookup"><span data-stu-id="419de-221">Example: "S46=136"</span></span>

</dd> <dt>

<span data-ttu-id="419de-222">**компрессионон**</span><span class="sxs-lookup"><span data-stu-id="419de-222">**CompressionOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-223">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-223">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-225">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ элемент управления \\ \\ \| Compression класса \_ On")</span><span class="sxs-lookup"><span data-stu-id="419de-225">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Compression\_On")</span></span>
</dt> </dl>

<span data-ttu-id="419de-226">Командная строка, используемая для включения аппаратного сжатия данных.</span><span class="sxs-lookup"><span data-stu-id="419de-226">Command string used to enable hardware data compression.</span></span>

<span data-ttu-id="419de-227">Пример: "S46 = 138"</span><span class="sxs-lookup"><span data-stu-id="419de-227">Example: "S46=138"</span></span>

</dd> <dt>

<span data-ttu-id="419de-228">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="419de-228">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-229">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="419de-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="419de-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-231">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="419de-231">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="419de-232">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="419de-232">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="419de-233">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-233">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="419de-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="419de-234"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="419de-235"> (0)</span><span class="sxs-lookup"><span data-stu-id="419de-235">(0)</span></span>


</dt> <dd>

<span data-ttu-id="419de-236">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="419de-236">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="419de-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="419de-237"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="419de-238">(1)</span><span class="sxs-lookup"><span data-stu-id="419de-238">(1)</span></span>


</dt> <dd>

<span data-ttu-id="419de-239">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="419de-239">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="419de-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-240"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="419de-241">(2)</span><span class="sxs-lookup"><span data-stu-id="419de-241">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="419de-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="419de-242"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="419de-243">(3)</span><span class="sxs-lookup"><span data-stu-id="419de-243">(3)</span></span>


</dt> <dd>

<span data-ttu-id="419de-244">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="419de-244">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="419de-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="419de-245"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="419de-246">(4)</span><span class="sxs-lookup"><span data-stu-id="419de-246">(4)</span></span>


</dt> <dd>

<span data-ttu-id="419de-247">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="419de-247">Device is not working properly.</span></span> <span data-ttu-id="419de-248">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="419de-248">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="419de-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="419de-249"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="419de-250">(5)</span><span class="sxs-lookup"><span data-stu-id="419de-250">(5)</span></span>


</dt> <dd>

<span data-ttu-id="419de-251">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="419de-251">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="419de-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="419de-252"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="419de-253"> (6)</span><span class="sxs-lookup"><span data-stu-id="419de-253">(6)</span></span>


</dt> <dd>

<span data-ttu-id="419de-254">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="419de-254">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="419de-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="419de-255"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="419de-256">(7)</span><span class="sxs-lookup"><span data-stu-id="419de-256">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="419de-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-257"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="419de-258">(8)</span><span class="sxs-lookup"><span data-stu-id="419de-258">(8)</span></span>


</dt> <dd>

<span data-ttu-id="419de-259">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-259">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="419de-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-260"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="419de-261">(9)</span><span class="sxs-lookup"><span data-stu-id="419de-261">(9)</span></span>


</dt> <dd>

<span data-ttu-id="419de-262">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="419de-262">Device is not working properly.</span></span> <span data-ttu-id="419de-263">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-263">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="419de-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="419de-264"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="419de-265">(10)</span><span class="sxs-lookup"><span data-stu-id="419de-265">(10)</span></span>


</dt> <dd>

<span data-ttu-id="419de-266">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="419de-266">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="419de-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-267"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="419de-268">(11)</span><span class="sxs-lookup"><span data-stu-id="419de-268">(11)</span></span>


</dt> <dd>

<span data-ttu-id="419de-269">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-269">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="419de-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="419de-270"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="419de-271">(12)</span><span class="sxs-lookup"><span data-stu-id="419de-271">(12)</span></span>


</dt> <dd>

<span data-ttu-id="419de-272">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="419de-272">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="419de-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-273"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="419de-274">(13)</span><span class="sxs-lookup"><span data-stu-id="419de-274">(13)</span></span>


</dt> <dd>

<span data-ttu-id="419de-275">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-275">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="419de-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="419de-276"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="419de-277">(14)</span><span class="sxs-lookup"><span data-stu-id="419de-277">(14)</span></span>


</dt> <dd>

<span data-ttu-id="419de-278">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="419de-278">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="419de-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="419de-279"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="419de-280">(15)</span><span class="sxs-lookup"><span data-stu-id="419de-280">(15)</span></span>


</dt> <dd>

<span data-ttu-id="419de-281">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="419de-281">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="419de-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="419de-282"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="419de-283">(16)</span><span class="sxs-lookup"><span data-stu-id="419de-283">(16)</span></span>


</dt> <dd>

<span data-ttu-id="419de-284">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="419de-284">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="419de-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="419de-285"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="419de-286">(17)</span><span class="sxs-lookup"><span data-stu-id="419de-286">(17)</span></span>


</dt> <dd>

<span data-ttu-id="419de-287">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="419de-287">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="419de-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-288"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="419de-289">(18)</span><span class="sxs-lookup"><span data-stu-id="419de-289">(18)</span></span>


</dt> <dd>

<span data-ttu-id="419de-290">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="419de-290">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="419de-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="419de-291"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="419de-292">(19)</span><span class="sxs-lookup"><span data-stu-id="419de-292">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="419de-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="419de-293"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="419de-294">(20)</span><span class="sxs-lookup"><span data-stu-id="419de-294">(20)</span></span>


</dt> <dd>

<span data-ttu-id="419de-295">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="419de-295">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="419de-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="419de-296"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="419de-297">(21)</span><span class="sxs-lookup"><span data-stu-id="419de-297">(21)</span></span>


</dt> <dd>

<span data-ttu-id="419de-298">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="419de-298">System failure.</span></span> <span data-ttu-id="419de-299">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="419de-299">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="419de-300">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="419de-300">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="419de-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="419de-301"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="419de-302">(22)</span><span class="sxs-lookup"><span data-stu-id="419de-302">(22)</span></span>


</dt> <dd>

<span data-ttu-id="419de-303">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="419de-303">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="419de-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="419de-304"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="419de-305">(23)</span><span class="sxs-lookup"><span data-stu-id="419de-305">(23)</span></span>


</dt> <dd>

<span data-ttu-id="419de-306">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="419de-306">System failure.</span></span> <span data-ttu-id="419de-307">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="419de-307">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="419de-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="419de-308"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="419de-309">(24)</span><span class="sxs-lookup"><span data-stu-id="419de-309">(24)</span></span>


</dt> <dd>

<span data-ttu-id="419de-310">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="419de-310">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="419de-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="419de-311"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="419de-312">(25)</span><span class="sxs-lookup"><span data-stu-id="419de-312">(25)</span></span>


</dt> <dd>

<span data-ttu-id="419de-313">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="419de-313">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="419de-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="419de-314"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="419de-315">(26)</span><span class="sxs-lookup"><span data-stu-id="419de-315">(26)</span></span>


</dt> <dd>

<span data-ttu-id="419de-316">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="419de-316">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="419de-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="419de-317"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="419de-318">(27)</span><span class="sxs-lookup"><span data-stu-id="419de-318">(27)</span></span>


</dt> <dd>

<span data-ttu-id="419de-319">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="419de-319">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="419de-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="419de-320"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="419de-321">(28)</span><span class="sxs-lookup"><span data-stu-id="419de-321">(28)</span></span>


</dt> <dd>

<span data-ttu-id="419de-322">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="419de-322">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="419de-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="419de-323"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="419de-324">(29)</span><span class="sxs-lookup"><span data-stu-id="419de-324">(29)</span></span>


</dt> <dd>

<span data-ttu-id="419de-325">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="419de-325">Device is disabled.</span></span> <span data-ttu-id="419de-326">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="419de-326">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="419de-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="419de-327"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="419de-328">(30)</span><span class="sxs-lookup"><span data-stu-id="419de-328">(30)</span></span>


</dt> <dd>

<span data-ttu-id="419de-329">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="419de-329">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="419de-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="419de-330"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="419de-331">1-31</span><span class="sxs-lookup"><span data-stu-id="419de-331">(31)</span></span>


</dt> <dd>

<span data-ttu-id="419de-332">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="419de-332">Device is not working properly.</span></span> <span data-ttu-id="419de-333">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="419de-333">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-334">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="419de-334">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-335">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="419de-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="419de-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-337">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="419de-337">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="419de-338">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="419de-338">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="419de-339">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-340">**конфигуратиондиалог**</span><span class="sxs-lookup"><span data-stu-id="419de-340">**ConfigurationDialog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-341">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-343">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| конфигдиалог")</span><span class="sxs-lookup"><span data-stu-id="419de-343">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ConfigDialog")</span></span>
</dt> </dl>

<span data-ttu-id="419de-344">Строка инициализации модема.</span><span class="sxs-lookup"><span data-stu-id="419de-344">Modem initialization string.</span></span> <span data-ttu-id="419de-345">Это свойство состоит из командных строк из других свойств этого класса.</span><span class="sxs-lookup"><span data-stu-id="419de-345">This property is made up of command strings from other properties of this class.</span></span>

</dd> <dt>

<span data-ttu-id="419de-346">**каунтриессуппортед**</span><span class="sxs-lookup"><span data-stu-id="419de-346">**CountriesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-347">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="419de-347">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="419de-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-349">Массив стран или регионов, в которых может действовать модем.</span><span class="sxs-lookup"><span data-stu-id="419de-349">Array of countries/regions in which the modem can operate.</span></span>

<span data-ttu-id="419de-350">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-350">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-351">**каунтриселектед**</span><span class="sxs-lookup"><span data-stu-id="419de-351">**CountrySelected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-352">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-354">Страна или регион, для которых в настоящее время программируется модем.</span><span class="sxs-lookup"><span data-stu-id="419de-354">Country/region for which the modem is currently programmed.</span></span> <span data-ttu-id="419de-355">Если поддерживается несколько стран или регионов, это свойство определяет, какая из них выбрана в данный момент для использования.</span><span class="sxs-lookup"><span data-stu-id="419de-355">When multiple countries/regions are supported, this property defines which one is currently selected for use.</span></span>

<span data-ttu-id="419de-356">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-356">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-357">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="419de-357">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-358">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-360">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="419de-360">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="419de-361">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="419de-361">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="419de-362">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="419de-362">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="419de-363">Это свойство наследуется [**от \_ CIM**](cim-logicalfile.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicalfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-364">**куррентпассвордс**</span><span class="sxs-lookup"><span data-stu-id="419de-364">**CurrentPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-365">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="419de-365">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="419de-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-367">Список паролей, определенных в данный момент для модема.</span><span class="sxs-lookup"><span data-stu-id="419de-367">List of currently defined passwords for the modem.</span></span> <span data-ttu-id="419de-368">Этот массив можно оставить пустым по соображениям безопасности.</span><span class="sxs-lookup"><span data-stu-id="419de-368">This array may be left blank for security reasons.</span></span>

<span data-ttu-id="419de-369">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-369">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-370">**DCB**</span><span class="sxs-lookup"><span data-stu-id="419de-370">**DCB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-371">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="419de-371">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="419de-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-373">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры связи Win32API \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span><span class="sxs-lookup"><span data-stu-id="419de-373">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)")</span></span>
</dt> </dl>

<span data-ttu-id="419de-374">Параметры управления для устройства последовательного подключения (в данном случае это модемное устройство).</span><span class="sxs-lookup"><span data-stu-id="419de-374">Control settings for a serial communications device, in this case, the modem device.</span></span>

</dd> <dt>

<span data-ttu-id="419de-375">**По умолчанию**</span><span class="sxs-lookup"><span data-stu-id="419de-375">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-376">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="419de-376">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="419de-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-378">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс управления \| по умолчанию")</span><span class="sxs-lookup"><span data-stu-id="419de-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Default")</span></span>
</dt> </dl>

<span data-ttu-id="419de-379">При **значении true** этот модем POTS является модемом по умолчанию в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="419de-379">If **TRUE**, this POTS modem is the default modem on the computer system running Windows.</span></span>

</dd> <dt>

<span data-ttu-id="419de-380">**Описание**</span><span class="sxs-lookup"><span data-stu-id="419de-380">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-381">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-383">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="419de-383">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="419de-384">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="419de-384">Description of the object.</span></span>

<span data-ttu-id="419de-385">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="419de-385">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-386">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="419de-386">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-389">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="419de-389">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="419de-390">Уникальный идентификатор этого POTS модема с других устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="419de-390">Unique identifier of this POTS modem from other devices on the system.</span></span>

<span data-ttu-id="419de-391">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-391">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-392">**девицелоадер**</span><span class="sxs-lookup"><span data-stu-id="419de-392">**DeviceLoader**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-393">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-395">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| загрузчик")</span><span class="sxs-lookup"><span data-stu-id="419de-395">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DevLoader")</span></span>
</dt> </dl>

<span data-ttu-id="419de-396">Имя загрузчика устройства для модема.</span><span class="sxs-lookup"><span data-stu-id="419de-396">Name of the device loader for the modem.</span></span> <span data-ttu-id="419de-397">Загрузчик устройства загружает драйверы и перечислители устройств и управляет ими для данного устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-397">A device loader loads and manages device drivers and enumerators for a given device.</span></span>

</dd> <dt>

<span data-ttu-id="419de-398">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="419de-398">**DeviceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-401">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| типа устройства")</span><span class="sxs-lookup"><span data-stu-id="419de-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DeviceType")</span></span>
</dt> </dl>

<span data-ttu-id="419de-402">Физический тип модема.</span><span class="sxs-lookup"><span data-stu-id="419de-402">Physical type of the modem.</span></span>

<span data-ttu-id="419de-403">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="419de-403">The values are:</span></span>

<dl> <dd><span data-ttu-id="419de-404">"Нуль Modem"</span><span class="sxs-lookup"><span data-stu-id="419de-404">"Null Modem"</span></span></dd> <dd><span data-ttu-id="419de-405">"Внутренний модем"</span><span class="sxs-lookup"><span data-stu-id="419de-405">"Internal Modem"</span></span></dd> <dd><span data-ttu-id="419de-406">"Внешний модем"</span><span class="sxs-lookup"><span data-stu-id="419de-406">"External Modem"</span></span></dd> <dd><span data-ttu-id="419de-407">"PCMCIA Modem"</span><span class="sxs-lookup"><span data-stu-id="419de-407">"PCMCIA Modem"</span></span></dd> <dd><span data-ttu-id="419de-408">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="419de-408">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Null_Modem"></span><span id="null_modem"></span><span id="NULL_MODEM"></span>

<span data-ttu-id="419de-409">**Нуль-модем** ("нуль-модем")</span><span class="sxs-lookup"><span data-stu-id="419de-409">**Null Modem** ("Null Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Internal_Modem"></span><span id="internal_modem"></span><span id="INTERNAL_MODEM"></span>

<span data-ttu-id="419de-410">**Внутренний модем** ("внутренний модем")</span><span class="sxs-lookup"><span data-stu-id="419de-410">**Internal Modem** ("Internal Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="External_Modem"></span><span id="external_modem"></span><span id="EXTERNAL_MODEM"></span>

<span data-ttu-id="419de-411">**Внешний модем** ("внешний модем")</span><span class="sxs-lookup"><span data-stu-id="419de-411">**External Modem** ("External Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Modem"></span><span id="pcmcia_modem"></span><span id="PCMCIA_MODEM"></span>

<span data-ttu-id="419de-412">**PCMCIA-модем** ("PCMCIA-модем")</span><span class="sxs-lookup"><span data-stu-id="419de-412">**PCMCIA Modem** ("PCMCIA Modem")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-413">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="419de-413">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-414">**диалтипе**</span><span class="sxs-lookup"><span data-stu-id="419de-414">**DialType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-415">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-415">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-416">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-417">Тип используемого метода набора номера.</span><span class="sxs-lookup"><span data-stu-id="419de-417">Type of dialing method used.</span></span>

<span data-ttu-id="419de-418">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-418">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-419">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-419">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Tone"></span><span id="tone"></span><span id="TONE"></span>

<span data-ttu-id="419de-420">**Тон** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-420">**Tone** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Pulse"></span><span id="pulse"></span><span id="PULSE"></span>

<span data-ttu-id="419de-421">**Импульс** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-421">**Pulse** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-422">**дривердате**</span><span class="sxs-lookup"><span data-stu-id="419de-422">**DriverDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-423">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="419de-423">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="419de-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-425">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| дривердате")</span><span class="sxs-lookup"><span data-stu-id="419de-425">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="419de-426">Дата драйвера модема.</span><span class="sxs-lookup"><span data-stu-id="419de-426">Date of the modem driver.</span></span>

</dd> <dt>

<span data-ttu-id="419de-427">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="419de-427">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-428">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="419de-428">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="419de-429">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-430">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="419de-430">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="419de-431">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-431">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-432">**еррорконтролфорцед**</span><span class="sxs-lookup"><span data-stu-id="419de-432">**ErrorControlForced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-433">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-434">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-434">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-435">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \| ErrorControl \_ forced")</span><span class="sxs-lookup"><span data-stu-id="419de-435">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Forced")</span></span>
</dt> </dl>

<span data-ttu-id="419de-436">Командная строка, используемая для включения контроля исправления ошибок при установлении соединения.</span><span class="sxs-lookup"><span data-stu-id="419de-436">Command string used to enable error correction control when establishing a connection.</span></span> <span data-ttu-id="419de-437">Это повышает надежность подключения.</span><span class="sxs-lookup"><span data-stu-id="419de-437">This increases the reliability of the connection.</span></span>

<span data-ttu-id="419de-438">Пример: "+ Q5S36 = 4S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="419de-438">Example: "+Q5S36=4S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="419de-439">**еррорконтролинфо**</span><span class="sxs-lookup"><span data-stu-id="419de-439">**ErrorControlInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-440">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-440">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-441">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-442">Характеристики исправления ошибок модема.</span><span class="sxs-lookup"><span data-stu-id="419de-442">Error correction characteristics of the modem.</span></span>

<span data-ttu-id="419de-443">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-443">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-444">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-444">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-445">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-445">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error_Correction"></span><span id="no_error_correction"></span><span id="NO_ERROR_CORRECTION"></span>

<span data-ttu-id="419de-446">**Без исправления ошибок** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-446">**No Error Correction** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MNP_4"></span><span id="mnp_4"></span>

<span data-ttu-id="419de-447">**MNP 4** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-447">**MNP 4** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LAPM"></span><span id="lapm"></span>

<span data-ttu-id="419de-448">**Лапм** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-448">**LAPM** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-449">**еррорконтролофф**</span><span class="sxs-lookup"><span data-stu-id="419de-449">**ErrorControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-450">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-452">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \| ErrorControl \_ Off")</span><span class="sxs-lookup"><span data-stu-id="419de-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="419de-453">Командная строка, используемая для отключения управления ошибками.</span><span class="sxs-lookup"><span data-stu-id="419de-453">Command string used to disable error control.</span></span>

<span data-ttu-id="419de-454">Пример: "+ Q6S36 = 3S48 = 128"</span><span class="sxs-lookup"><span data-stu-id="419de-454">Example: "+Q6S36=3S48=128"</span></span>

</dd> <dt>

<span data-ttu-id="419de-455">**еррорконтролон**</span><span class="sxs-lookup"><span data-stu-id="419de-455">**ErrorControlOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-456">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-456">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-458">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| ErrorControl \_ On")</span><span class="sxs-lookup"><span data-stu-id="419de-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ErrorControl\_On")</span></span>
</dt> </dl>

<span data-ttu-id="419de-459">Командная строка, используемая для включения управления ошибками.</span><span class="sxs-lookup"><span data-stu-id="419de-459">Command string used to enable error control.</span></span>

<span data-ttu-id="419de-460">Пример: "+ Q5S36 = 7S48 = 7"</span><span class="sxs-lookup"><span data-stu-id="419de-460">Example: "+Q5S36=7S48=7"</span></span>

</dd> <dt>

<span data-ttu-id="419de-461">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="419de-461">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-462">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-463">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-463">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-464">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="419de-464">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="419de-465">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-465">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-466">**фловконтролхард**</span><span class="sxs-lookup"><span data-stu-id="419de-466">**FlowControlHard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-467">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-467">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-468">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-468">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-469">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| фловконтрол \_ Hard")</span><span class="sxs-lookup"><span data-stu-id="419de-469">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Hard")</span></span>
</dt> </dl>

<span data-ttu-id="419de-470">Командная строка, используемая для включения аппаратного управления потоком.</span><span class="sxs-lookup"><span data-stu-id="419de-470">Command string used to enable hardware flow control.</span></span> <span data-ttu-id="419de-471">Управление потоком состоит из сигналов, передаваемых между компьютерами и проверяющих готовность обоих компьютеров к передаче или получению данных.</span><span class="sxs-lookup"><span data-stu-id="419de-471">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="419de-472">Пример: "&K1"</span><span class="sxs-lookup"><span data-stu-id="419de-472">Example: "&K1"</span></span>

</dd> <dt>

<span data-ttu-id="419de-473">**фловконтролофф**</span><span class="sxs-lookup"><span data-stu-id="419de-473">**FlowControlOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-476">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ класс управления Win32Registry системы CurrentControlSet \\ \\ \\ \\ \| фловконтрол \_ Off")</span><span class="sxs-lookup"><span data-stu-id="419de-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Off")</span></span>
</dt> </dl>

<span data-ttu-id="419de-477">Командная строка, используемая для отключения управления потоком.</span><span class="sxs-lookup"><span data-stu-id="419de-477">Command string used to disable flow control.</span></span> <span data-ttu-id="419de-478">Управление потоком состоит из сигналов, передаваемых между компьютерами и проверяющих готовность обоих компьютеров к передаче или получению данных.</span><span class="sxs-lookup"><span data-stu-id="419de-478">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="419de-479">Пример: "&K0"</span><span class="sxs-lookup"><span data-stu-id="419de-479">Example: "&K0"</span></span>

</dd> <dt>

<span data-ttu-id="419de-480">**фловконтролсофт**</span><span class="sxs-lookup"><span data-stu-id="419de-480">**FlowControlSoft**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-481">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-482">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-483">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| фловконтрол \_ Soft")</span><span class="sxs-lookup"><span data-stu-id="419de-483">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|FlowControl\_Soft")</span></span>
</dt> </dl>

<span data-ttu-id="419de-484">Командная строка, используемая для включения управления потоком программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="419de-484">Command string used to enable software flow control.</span></span> <span data-ttu-id="419de-485">Управление потоком состоит из сигналов, передаваемых между компьютерами и проверяющих готовность обоих компьютеров к передаче или получению данных.</span><span class="sxs-lookup"><span data-stu-id="419de-485">Flow control consists of signals sent between computers that verify that both computers are ready to transmit or receive data.</span></span>

<span data-ttu-id="419de-486">Пример: "&априорной оценкой K2"</span><span class="sxs-lookup"><span data-stu-id="419de-486">Example: "&K2"</span></span>

</dd> <dt>

<span data-ttu-id="419de-487">**инактивитискале**</span><span class="sxs-lookup"><span data-stu-id="419de-487">**InactivityScale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-488">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-488">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-489">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-490">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| инактивитискале")</span><span class="sxs-lookup"><span data-stu-id="419de-490">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InactivityScale")</span></span>
</dt> </dl>

<span data-ttu-id="419de-491">Множитель, используемый со свойством **инактивититимеаут** для вычисления периода ожидания соединения.</span><span class="sxs-lookup"><span data-stu-id="419de-491">Multiplier used with the **InactivityTimeout** property to calculate the timeout period of a connection.</span></span>

</dd> <dt>

<span data-ttu-id="419de-492">**InactivityTimeout**</span><span class="sxs-lookup"><span data-stu-id="419de-492">**InactivityTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-493">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="419de-493">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="419de-494">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-494">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-495">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="419de-495">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="419de-496">Ограничение времени (в секундах) автоматического отключения телефонной линии, если обмен данными не выполняется.</span><span class="sxs-lookup"><span data-stu-id="419de-496">Time limit (in seconds) for automatic disconnection of the phone line, if no data is exchanged.</span></span> <span data-ttu-id="419de-497">Значение 0 (ноль) указывает, что эта функция имеется, но не включена.</span><span class="sxs-lookup"><span data-stu-id="419de-497">A value of 0 (zero) indicates that this feature is present but not enabled.</span></span>

<span data-ttu-id="419de-498">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-498">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-499">**Index**</span><span class="sxs-lookup"><span data-stu-id="419de-499">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-500">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="419de-500">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="419de-501">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-501">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-502">Номер индекса для этого модема POTS.</span><span class="sxs-lookup"><span data-stu-id="419de-502">Index number for this POTS modem.</span></span>

<span data-ttu-id="419de-503">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="419de-503">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="419de-504">**индексекс**</span><span class="sxs-lookup"><span data-stu-id="419de-504">**IndexEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-505">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-506">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-506">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-507">Идентификатор экземпляра устройства для этого модема POTS.</span><span class="sxs-lookup"><span data-stu-id="419de-507">The device instance ID for this POTS modem.</span></span>

<span data-ttu-id="419de-508">Пример: "1&08"</span><span class="sxs-lookup"><span data-stu-id="419de-508">Example: "1&08"</span></span>

<span data-ttu-id="419de-509">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство доступно начиная с Windows Server 2016 и Windows 10.</span><span class="sxs-lookup"><span data-stu-id="419de-509">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is available beginning with Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="419de-510">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="419de-510">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-511">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="419de-511">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="419de-512">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-512">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-513">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="419de-513">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="419de-514">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="419de-514">Date and time the object was installed.</span></span> <span data-ttu-id="419de-515">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="419de-515">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="419de-516">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="419de-516">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-517">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="419de-517">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-518">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="419de-518">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="419de-519">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-520">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="419de-520">Last error code reported by the logical device.</span></span>

<span data-ttu-id="419de-521">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-521">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-522">**максбаудратетофоне**</span><span class="sxs-lookup"><span data-stu-id="419de-522">**MaxBaudRateToPhone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-523">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="419de-523">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="419de-524">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-524">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-525">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="419de-525">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="419de-526">Максимальная настраиваемая скорость связи для доступа к телефонной системе.</span><span class="sxs-lookup"><span data-stu-id="419de-526">Maximum settable communication speed for accessing the phone system.</span></span>

<span data-ttu-id="419de-527">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-527">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-528">**максбаудратетосериалпорт**</span><span class="sxs-lookup"><span data-stu-id="419de-528">**MaxBaudRateToSerialPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-529">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="419de-529">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="419de-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-531">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="419de-531">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="419de-532">Максимальная настраиваемая скорость обмена данными с COM-портом для внешнего модема.</span><span class="sxs-lookup"><span data-stu-id="419de-532">Maximum settable communication speed to the COM port for an external modem.</span></span> <span data-ttu-id="419de-533">Введите 0 (ноль), если это не применимо.</span><span class="sxs-lookup"><span data-stu-id="419de-533">Enter 0 (zero) if not applicable.</span></span>

<span data-ttu-id="419de-534">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-534">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-535">**макснумберофпассвордс**</span><span class="sxs-lookup"><span data-stu-id="419de-535">**MaxNumberOfPasswords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-536">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-538">Число паролей, определяемых в самом модеме.</span><span class="sxs-lookup"><span data-stu-id="419de-538">Number of passwords definable in the modem itself.</span></span> <span data-ttu-id="419de-539">Если эта функция не поддерживается, введите 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="419de-539">If this feature is not supported, enter 0 (zero).</span></span>

<span data-ttu-id="419de-540">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-540">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-541">**Модель**</span><span class="sxs-lookup"><span data-stu-id="419de-541">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-542">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-543">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-544">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| системная \\ \\ \\ \\ \\ \\ модель управления классом CurrentControlSet \| ")</span><span class="sxs-lookup"><span data-stu-id="419de-544">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Model")</span></span>
</dt> </dl>

<span data-ttu-id="419de-545">Модель этого модема POTS.</span><span class="sxs-lookup"><span data-stu-id="419de-545">Model of this POTS modem.</span></span>

<span data-ttu-id="419de-546">Пример: "Спортстер 56K External"</span><span class="sxs-lookup"><span data-stu-id="419de-546">Example: "Sportster 56K External"</span></span>

</dd> <dt>

<span data-ttu-id="419de-547">**модеминфпас**</span><span class="sxs-lookup"><span data-stu-id="419de-547">**ModemInfPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-548">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-549">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-550">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| инфпас")</span><span class="sxs-lookup"><span data-stu-id="419de-550">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfPath")</span></span>
</dt> </dl>

<span data-ttu-id="419de-551">Путь к INF-файлу модема.</span><span class="sxs-lookup"><span data-stu-id="419de-551">Path to this modem's .inf file.</span></span> <span data-ttu-id="419de-552">Этот файл содержит сведения об инициализации модема и его драйвера.</span><span class="sxs-lookup"><span data-stu-id="419de-552">This file contains initialization information for the modem and its driver.</span></span>

<span data-ttu-id="419de-553">Пример: "C: \\ Windows \\ INF"</span><span class="sxs-lookup"><span data-stu-id="419de-553">Example: "C:\\Windows\\INF"</span></span>

</dd> <dt>

<span data-ttu-id="419de-554">**модеминфсектион**</span><span class="sxs-lookup"><span data-stu-id="419de-554">**ModemInfSection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-555">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-555">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-556">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-556">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-557">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| инфсектион")</span><span class="sxs-lookup"><span data-stu-id="419de-557">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|InfSection")</span></span>
</dt> </dl>

<span data-ttu-id="419de-558">Имя раздела в INF-файле модема, который содержит сведения о модеме.</span><span class="sxs-lookup"><span data-stu-id="419de-558">Name of the section in the modem's .inf file that contains information about the modem.</span></span>

</dd> <dt>

<span data-ttu-id="419de-559">**модулатионбелл**</span><span class="sxs-lookup"><span data-stu-id="419de-559">**ModulationBell**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-560">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-560">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-561">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-561">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-562">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| модуляция \_ Bell")</span><span class="sxs-lookup"><span data-stu-id="419de-562">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_Bell")</span></span>
</dt> </dl>

<span data-ttu-id="419de-563">Командная строка, используемая для указания модему использования модуляций Bell для 300 и 1200 бит/с.</span><span class="sxs-lookup"><span data-stu-id="419de-563">Command string used to instruct the modem to use Bell modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="419de-564">Пример: "B1"</span><span class="sxs-lookup"><span data-stu-id="419de-564">Example: "B1"</span></span>

</dd> <dt>

<span data-ttu-id="419de-565">**модулатионкЦитт**</span><span class="sxs-lookup"><span data-stu-id="419de-565">**ModulationCCITT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-566">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-567">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-568">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| модуляция \_ CCITT")</span><span class="sxs-lookup"><span data-stu-id="419de-568">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Modulation\_CCITT")</span></span>
</dt> </dl>

<span data-ttu-id="419de-569">Командная строка, используемая для указания модему использования модуляций CCITT для 300 и 1200 бит/с.</span><span class="sxs-lookup"><span data-stu-id="419de-569">Command string used to instruct the modem to use CCITT modulations for 300 and 1200 bps.</span></span>

<span data-ttu-id="419de-570">Пример: B0</span><span class="sxs-lookup"><span data-stu-id="419de-570">Example: "B0"</span></span>

</dd> <dt>

<span data-ttu-id="419de-571">**модулатионсчеме**</span><span class="sxs-lookup"><span data-stu-id="419de-571">**ModulationScheme**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-572">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-572">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-573">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-574">Схема модуляции модема.</span><span class="sxs-lookup"><span data-stu-id="419de-574">Modulation scheme of the modem.</span></span>

<span data-ttu-id="419de-575">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-575">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-576">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-576">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-577">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-577">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="419de-578">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-578">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_103"></span><span id="bell_103"></span><span id="BELL_103"></span>

<span data-ttu-id="419de-579">**Звонок 103** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-579">**Bell 103** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bell_212A"></span><span id="bell_212a"></span><span id="BELL_212A"></span>

<span data-ttu-id="419de-580">**Колокольчик 212A** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-580">**Bell 212A** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="V.22bis"></span><span id="v.22bis"></span><span id="V.22BIS"></span>

<span data-ttu-id="419de-581">**V. 22bis** (5)</span><span class="sxs-lookup"><span data-stu-id="419de-581">**V.22bis** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32"></span><span id="v.32"></span>

<span data-ttu-id="419de-582">**V. 32** (6)</span><span class="sxs-lookup"><span data-stu-id="419de-582">**V.32** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="V.32bis"></span><span id="v.32bis"></span><span id="V.32BIS"></span>

<span data-ttu-id="419de-583">**V. 32bis** (7)</span><span class="sxs-lookup"><span data-stu-id="419de-583">**V.32bis** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="V.turbo"></span><span id="v.turbo"></span><span id="V.TURBO"></span>

<span data-ttu-id="419de-584">**V. Turbo** (8)</span><span class="sxs-lookup"><span data-stu-id="419de-584">**V.turbo** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="V.FC"></span><span id="v.fc"></span>

<span data-ttu-id="419de-585">**V. FC** (9)</span><span class="sxs-lookup"><span data-stu-id="419de-585">**V.FC** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34"></span><span id="v.34"></span>

<span data-ttu-id="419de-586">**V. 34** (10)</span><span class="sxs-lookup"><span data-stu-id="419de-586">**V.34** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="V.34bis"></span><span id="v.34bis"></span><span id="V.34BIS"></span>

<span data-ttu-id="419de-587">**V. 34bis** (11)</span><span class="sxs-lookup"><span data-stu-id="419de-587">**V.34bis** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-588">**Name**</span><span class="sxs-lookup"><span data-stu-id="419de-588">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-589">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-590">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-590">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-591">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="419de-591">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="419de-592">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="419de-592">Label by which the object is known.</span></span> <span data-ttu-id="419de-593">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="419de-593">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="419de-594">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="419de-594">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-595">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="419de-595">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-596">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-596">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-597">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-597">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-598">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="419de-598">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="419de-599">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-599">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="419de-600">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-600">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="419de-601">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="419de-601">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="419de-602">**портсубкласс**</span><span class="sxs-lookup"><span data-stu-id="419de-602">**PortSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-603">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-604">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-604">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-605">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| портсубкласс"), **value** ("параллельный порт", "последовательный порт", "модем")</span><span class="sxs-lookup"><span data-stu-id="419de-605">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|PortSubClass"), **Value** ("Parallel Port", "Serial Port", "Modem")</span></span>
</dt> </dl>

<span data-ttu-id="419de-606">Определение порта, используемого для этого модема.</span><span class="sxs-lookup"><span data-stu-id="419de-606">Definition of the port used for this modem.</span></span>

<dt>



 <span data-ttu-id="419de-607">("00")</span><span class="sxs-lookup"><span data-stu-id="419de-607">("00")</span></span>


</dt> <dd>

<span data-ttu-id="419de-608">Parallel Port (Параллельный порт)</span><span class="sxs-lookup"><span data-stu-id="419de-608">Parallel Port</span></span>

</dd> <dt>



 <span data-ttu-id="419de-609">("01")</span><span class="sxs-lookup"><span data-stu-id="419de-609">("01")</span></span>


</dt> <dd>

<span data-ttu-id="419de-610">Последовательный порт</span><span class="sxs-lookup"><span data-stu-id="419de-610">Serial Port</span></span>

</dd> <dt>



 <span data-ttu-id="419de-611">("02")</span><span class="sxs-lookup"><span data-stu-id="419de-611">("02")</span></span>


</dt> <dd>

<span data-ttu-id="419de-612">Modem (Модем)</span><span class="sxs-lookup"><span data-stu-id="419de-612">Modem</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-613">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="419de-613">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-614">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="419de-614">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="419de-615">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-615">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-616">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="419de-616">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="419de-617">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-617">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-618"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="419de-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-619"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="419de-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-620"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="419de-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-621"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="419de-622">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="419de-622">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="419de-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="419de-623"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="419de-624">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="419de-624">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="419de-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="419de-625"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="419de-626">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="419de-626">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="419de-627">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="419de-627">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="419de-628">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="419de-628">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="419de-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="419de-629"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="419de-630">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="419de-630">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="419de-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="419de-631"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="419de-632">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="419de-632">Timed Power-On Supported</span></span>

<span data-ttu-id="419de-633">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="419de-633">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-634">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="419de-634">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-635">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="419de-635">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="419de-636">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-636">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-637">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="419de-637">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="419de-638">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="419de-638">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="419de-639">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-639">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-640">**Prefix**</span><span class="sxs-lookup"><span data-stu-id="419de-640">**Prefix**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-641">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-641">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-642">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-642">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-643">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ управления \\ \\ \| префиксом класса")</span><span class="sxs-lookup"><span data-stu-id="419de-643">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Prefix")</span></span>
</dt> </dl>

<span data-ttu-id="419de-644">Префикс, используемый для доступа к внешней линии.</span><span class="sxs-lookup"><span data-stu-id="419de-644">Dialing prefix used to access an outside line.</span></span>

</dd> <dt>

<span data-ttu-id="419de-645">**Свойства**</span><span class="sxs-lookup"><span data-stu-id="419de-645">**Properties**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-646">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="419de-646">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="419de-647">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-647">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-648">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ \\ \\ Свойства класса элемента управления Win32Registry System CurrentControlSet \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="419de-648">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Properties")</span></span>
</dt> </dl>

<span data-ttu-id="419de-649">Список всех свойств (и их значений) для этого модема.</span><span class="sxs-lookup"><span data-stu-id="419de-649">List of all the properties (and their values) for this modem.</span></span>

</dd> <dt>

<span data-ttu-id="419de-650">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="419de-650">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-651">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-652">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-653">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| providerName")</span><span class="sxs-lookup"><span data-stu-id="419de-653">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ProviderName")</span></span>
</dt> </dl>

<span data-ttu-id="419de-654">Сетевой путь к компьютеру, на котором находятся службы модема.</span><span class="sxs-lookup"><span data-stu-id="419de-654">Network path to the computer that provides the modem services.</span></span>

</dd> <dt>

<span data-ttu-id="419de-655">**Ритм**</span><span class="sxs-lookup"><span data-stu-id="419de-655">**Pulse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-656">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-656">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-657">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-657">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-658">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| Pulse")</span><span class="sxs-lookup"><span data-stu-id="419de-658">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Pulse")</span></span>
</dt> </dl>

<span data-ttu-id="419de-659">Командная строка, используемая для указания модему использования импульсного режима для набора.</span><span class="sxs-lookup"><span data-stu-id="419de-659">Command string used to instruct the modem to use pulse mode for dialing.</span></span> <span data-ttu-id="419de-660">Импульсный набор необходим для телефонных линий, которые не могут поддерживать тоновый набор.</span><span class="sxs-lookup"><span data-stu-id="419de-660">Pulse dialing is necessary for phone lines that are unable to handle tone dialing.</span></span>

<span data-ttu-id="419de-661">Пример: "P"</span><span class="sxs-lookup"><span data-stu-id="419de-661">Example: "P"</span></span>

</dd> <dt>

<span data-ttu-id="419de-662">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="419de-662">**Reset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-663">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-663">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-664">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-664">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-665">Квалификаторы: [**переопределить**](../wmisdk/standard-qualifiers.md) (сбросить), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| rereset")</span><span class="sxs-lookup"><span data-stu-id="419de-665">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Reset), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Reset")</span></span>
</dt> </dl>

<span data-ttu-id="419de-666">Командная строка, используемая для сброса модема при следующем вызове.</span><span class="sxs-lookup"><span data-stu-id="419de-666">Command string used to reset the modem for the next call.</span></span>

<span data-ttu-id="419de-667">Пример: "AT&F"</span><span class="sxs-lookup"><span data-stu-id="419de-667">Example: "AT&F"</span></span>

</dd> <dt>

<span data-ttu-id="419de-668">**респонсескэйнаме**</span><span class="sxs-lookup"><span data-stu-id="419de-668">**ResponsesKeyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-669">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-669">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-670">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-670">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-671">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| респонсескэйнаме")</span><span class="sxs-lookup"><span data-stu-id="419de-671">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|ResponsesKeyName")</span></span>
</dt> </dl>

<span data-ttu-id="419de-672">Ответ. Этот модем может сообщить операционной системе о процессе подключения.</span><span class="sxs-lookup"><span data-stu-id="419de-672">Response this modem might report to the operating system during the connection process.</span></span> <span data-ttu-id="419de-673">Первые два символа указывают тип ответа.</span><span class="sxs-lookup"><span data-stu-id="419de-673">The first two characters specify the type of response.</span></span> <span data-ttu-id="419de-674">Два второго символа указывают сведения о выполняемом подключении.</span><span class="sxs-lookup"><span data-stu-id="419de-674">The second two characters specify information about the connection being made.</span></span> <span data-ttu-id="419de-675">Два второго символа используются только для выполнения согласования или для соединения с кодами откликов.</span><span class="sxs-lookup"><span data-stu-id="419de-675">The second two characters are used only for Negotiation Progress or Connect response codes.</span></span> <span data-ttu-id="419de-676">Следующие восемь символов указывают скорость линии модем-модема, согласованную в битах в секунду (бит/с).</span><span class="sxs-lookup"><span data-stu-id="419de-676">The next eight characters specify the modem-to-modem line speed negotiated in bits per second (bps).</span></span> <span data-ttu-id="419de-677">Символы представляют собой 32-разрядный длинный целочисленный формат без знака (байт и слово в обратных).</span><span class="sxs-lookup"><span data-stu-id="419de-677">The characters represent a 32-bit unsigned long integer format (byte and word reversed).</span></span> <span data-ttu-id="419de-678">Последние восемь символов указывают на то, что модем переводится на другой порт или скорость связи с терминальным оборудованием (DTE).</span><span class="sxs-lookup"><span data-stu-id="419de-678">The last eight characters indicate that the modem is changing to a different port or Data Terminal Equipment (DTE) speed.</span></span> <span data-ttu-id="419de-679">Обычно это поле не используется, так как модемы подключаются к заблокированной скорости порта независимо от скорости передачи данных между модемом или устройством связи (DCE).</span><span class="sxs-lookup"><span data-stu-id="419de-679">Usually this field is not used because modems make connections at a locked port speed regardless of the modem-to-modem or Data Communications Equipment (DCE) speed.</span></span>

</dd> <dt>

<span data-ttu-id="419de-680">**рингсбефореансвер**</span><span class="sxs-lookup"><span data-stu-id="419de-680">**RingsBeforeAnswer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-681">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="419de-681">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="419de-682">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-682">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-683">Число звонков перед ответом модема на входящий вызов.</span><span class="sxs-lookup"><span data-stu-id="419de-683">Number of rings before the modem answers an incoming call.</span></span>

<span data-ttu-id="419de-684">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-684">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-685">**спеакермодедиал**</span><span class="sxs-lookup"><span data-stu-id="419de-685">**SpeakerModeDial**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-686">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-687">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-688">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодедиал")</span><span class="sxs-lookup"><span data-stu-id="419de-688">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeDial")</span></span>
</dt> </dl>

<span data-ttu-id="419de-689">Командная строка, используемая для включения динамика модема после набора номера и отключения динамика при установке соединения.</span><span class="sxs-lookup"><span data-stu-id="419de-689">Command string used to turn the modem speaker on after dialing a number, and turning the speaker off when a connection has been established.</span></span>

<span data-ttu-id="419de-690">Пример: "M1"</span><span class="sxs-lookup"><span data-stu-id="419de-690">Example: "M1"</span></span>

</dd> <dt>

<span data-ttu-id="419de-691">**спеакермодеофф**</span><span class="sxs-lookup"><span data-stu-id="419de-691">**SpeakerModeOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-692">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-693">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-693">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-694">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодеофф")</span><span class="sxs-lookup"><span data-stu-id="419de-694">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOff")</span></span>
</dt> </dl>

<span data-ttu-id="419de-695">Командная строка, используемая для выключения динамика модема.</span><span class="sxs-lookup"><span data-stu-id="419de-695">Command string used to turn the modem speaker off.</span></span>

<span data-ttu-id="419de-696">Пример: M0</span><span class="sxs-lookup"><span data-stu-id="419de-696">Example: "M0"</span></span>

</dd> <dt>

<span data-ttu-id="419de-697">**спеакермодеон**</span><span class="sxs-lookup"><span data-stu-id="419de-697">**SpeakerModeOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-698">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-699">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-699">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-700">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодеон")</span><span class="sxs-lookup"><span data-stu-id="419de-700">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeOn")</span></span>
</dt> </dl>

<span data-ttu-id="419de-701">Командная строка, используемая для включения динамика модема.</span><span class="sxs-lookup"><span data-stu-id="419de-701">Command string used to turn the modem speaker on.</span></span>

<span data-ttu-id="419de-702">Пример: "m2"</span><span class="sxs-lookup"><span data-stu-id="419de-702">Example: "M2"</span></span>

</dd> <dt>

<span data-ttu-id="419de-703">**спеакермодесетуп**</span><span class="sxs-lookup"><span data-stu-id="419de-703">**SpeakerModeSetup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-704">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-705">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-705">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-706">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакермодесетуп")</span><span class="sxs-lookup"><span data-stu-id="419de-706">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerModeSetup")</span></span>
</dt> </dl>

<span data-ttu-id="419de-707">Командная строка, указывающая модему на необходимость включения динамика (до установления подключения).</span><span class="sxs-lookup"><span data-stu-id="419de-707">Command string used to instruct the modem to turn the speaker on (until a connection is established).</span></span>

<span data-ttu-id="419de-708">Пример: "M3"</span><span class="sxs-lookup"><span data-stu-id="419de-708">Example: "M3"</span></span>

</dd> <dt>

<span data-ttu-id="419de-709">**спеакерволумехигх**</span><span class="sxs-lookup"><span data-stu-id="419de-709">**SpeakerVolumeHigh**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-710">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-711">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-711">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-712">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| спеакерволуме \_ High")</span><span class="sxs-lookup"><span data-stu-id="419de-712">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_High")</span></span>
</dt> </dl>

<span data-ttu-id="419de-713">Командная строка, используемая для настройки динамика модема на самый большой том.</span><span class="sxs-lookup"><span data-stu-id="419de-713">Command string used to set the modem speaker to the highest volume.</span></span>

<span data-ttu-id="419de-714">Пример: "L3"</span><span class="sxs-lookup"><span data-stu-id="419de-714">Example: "L3"</span></span>

</dd> <dt>

<span data-ttu-id="419de-715">**спеакерволумеинфо**</span><span class="sxs-lookup"><span data-stu-id="419de-715">**SpeakerVolumeInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-716">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-716">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-717">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-717">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-718">Описывает уровень громкости звуковых тонов с модема.</span><span class="sxs-lookup"><span data-stu-id="419de-718">Describes the volume level of the audible tones from the modem.</span></span>

<span data-ttu-id="419de-719">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-719">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-720">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="419de-720">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-721">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-721">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="419de-722">**Не поддерживается** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-722">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="419de-723">**Высокий** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-723">**High** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="419de-724">**Средний** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-724">**Medium** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="419de-725">**Низкий** (5)</span><span class="sxs-lookup"><span data-stu-id="419de-725">**Low** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="419de-726">**Выкл** . (6)</span><span class="sxs-lookup"><span data-stu-id="419de-726">**Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="419de-727">**Авто** (7)</span><span class="sxs-lookup"><span data-stu-id="419de-727">**Auto** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-728">**спеакерволумелов**</span><span class="sxs-lookup"><span data-stu-id="419de-728">**SpeakerVolumeLow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-729">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-729">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-730">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-730">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-731">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ класс \| спеакерволуме \_ Low")</span><span class="sxs-lookup"><span data-stu-id="419de-731">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Low")</span></span>
</dt> </dl>

<span data-ttu-id="419de-732">Командная строка, используемая для настройки динамика модема на самый низкий том.</span><span class="sxs-lookup"><span data-stu-id="419de-732">Command string used to set the modem speaker to the lowest volume.</span></span>

<span data-ttu-id="419de-733">Пример: "L1"</span><span class="sxs-lookup"><span data-stu-id="419de-733">Example: "L1"</span></span>

</dd> <dt>

<span data-ttu-id="419de-734">**спеакерволумемед**</span><span class="sxs-lookup"><span data-stu-id="419de-734">**SpeakerVolumeMed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-735">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-735">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-736">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-736">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-737">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| спеакерволуме \_ MED")</span><span class="sxs-lookup"><span data-stu-id="419de-737">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|SpeakerVolume\_Med")</span></span>
</dt> </dl>

<span data-ttu-id="419de-738">Командная строка, используемая для настройки динамика модема на средний том.</span><span class="sxs-lookup"><span data-stu-id="419de-738">Command string used to set the modem speaker to a medium volume.</span></span>

<span data-ttu-id="419de-739">Пример: "L2"</span><span class="sxs-lookup"><span data-stu-id="419de-739">Example: "L2"</span></span>

</dd> <dt>

<span data-ttu-id="419de-740">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="419de-740">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-741">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-741">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-742">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-742">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-743">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="419de-743">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="419de-744">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="419de-744">Current status of the object.</span></span> <span data-ttu-id="419de-745">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="419de-745">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="419de-746">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="419de-746">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="419de-747">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="419de-747">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="419de-748">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="419de-748">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="419de-749">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="419de-749">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="419de-750">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="419de-750">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="419de-751">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="419de-751">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="419de-752">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="419de-752">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="419de-753">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="419de-753">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="419de-754">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="419de-754">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-755">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="419de-755">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="419de-756">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="419de-756">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="419de-757">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="419de-757">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="419de-758">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="419de-758">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="419de-759">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="419de-759">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="419de-760">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="419de-760">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="419de-761">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="419de-761">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="419de-762">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="419de-762">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="419de-763">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="419de-763">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-764">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="419de-764">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-765">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="419de-765">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="419de-766">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-766">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-767">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="419de-767">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="419de-768">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="419de-768">State of the logical device.</span></span> <span data-ttu-id="419de-769">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="419de-769">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="419de-770">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-770">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="419de-771">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="419de-771">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="419de-772">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="419de-772">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="419de-773">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="419de-773">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="419de-774">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="419de-774">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="419de-775">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="419de-775">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-776">**StringFormat**</span><span class="sxs-lookup"><span data-stu-id="419de-776">**StringFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-777">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-777">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-778">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-778">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-779">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \_ \| структуры устройств Win32 API Line \| линедевкапс \| двстрингформат")</span><span class="sxs-lookup"><span data-stu-id="419de-779">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Line Device Structures\|LINEDEVCAPS\|dwStringFormat")</span></span>
</dt> </dl>

<span data-ttu-id="419de-780">Тип символов, используемых для текста, передаваемого через модем.</span><span class="sxs-lookup"><span data-stu-id="419de-780">Type of characters used for text passed through the modem.</span></span>

<span data-ttu-id="419de-781">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="419de-781">The values are:</span></span>

<dl> <dd><span data-ttu-id="419de-782">"Формат строки ASCII"</span><span class="sxs-lookup"><span data-stu-id="419de-782">"ASCII string format"</span></span></dd> <dd><span data-ttu-id="419de-783">"Формат строки DBCS"</span><span class="sxs-lookup"><span data-stu-id="419de-783">"DBCS string format"</span></span></dd> <dd><span data-ttu-id="419de-784">"Формат строки Юникода"</span><span class="sxs-lookup"><span data-stu-id="419de-784">"UNICODE string format"</span></span></dd> </dl>

<dt>

<span id="ASCII_string_format"></span><span id="ascii_string_format"></span><span id="ASCII_STRING_FORMAT"></span>

<span data-ttu-id="419de-785">**Формат строки ASCII** (формат строкового формата ASCII)</span><span class="sxs-lookup"><span data-stu-id="419de-785">**ASCII string format** ("ASCII string format")</span></span>


</dt> <dd></dd> <dt>

<span id="DBCS_string_format"></span><span id="dbcs_string_format"></span><span id="DBCS_STRING_FORMAT"></span>

<span data-ttu-id="419de-786">**Формат строки DBCS** (формат строки DBCS)</span><span class="sxs-lookup"><span data-stu-id="419de-786">**DBCS string format** ("DBCS string format")</span></span>


</dt> <dd></dd> <dt>

<span id="UNICODE_string_format"></span><span id="unicode_string_format"></span><span id="UNICODE_STRING_FORMAT"></span>

<span data-ttu-id="419de-787">**Формат строки Юникода** ("формат строки Юникода")</span><span class="sxs-lookup"><span data-stu-id="419de-787">**UNICODE string format** ("UNICODE string format")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="419de-788">**суппортскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="419de-788">**SupportsCallback**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-789">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="419de-789">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="419de-790">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-790">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-791">Если **значение равно true**, модем поддерживает обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="419de-791">If **TRUE**, the modem supports callback.</span></span>

<span data-ttu-id="419de-792">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-792">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-793">**суппортссинчронаусконнект**</span><span class="sxs-lookup"><span data-stu-id="419de-793">**SupportsSynchronousConnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-794">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="419de-794">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="419de-795">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-795">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-796">При **значении true** синхронное, а также асинхронное взаимодействие поддерживается.</span><span class="sxs-lookup"><span data-stu-id="419de-796">If **TRUE**, synchronous, as well as asynchronous, communication is supported.</span></span>

<span data-ttu-id="419de-797">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-797">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-798">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="419de-798">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-799">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-799">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-800">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-800">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-801">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="419de-801">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="419de-802">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="419de-802">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="419de-803">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-803">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-804">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="419de-804">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-805">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-805">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-806">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-806">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-807">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="419de-807">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="419de-808">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="419de-808">Name of the scoping system.</span></span>

<span data-ttu-id="419de-809">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="419de-809">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-810">**Признак конца**</span><span class="sxs-lookup"><span data-stu-id="419de-810">**Terminator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-811">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-811">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-812">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-812">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-813">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ элемент управления \\ \\ \| признак конца класса")</span><span class="sxs-lookup"><span data-stu-id="419de-813">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Terminator")</span></span>
</dt> </dl>

<span data-ttu-id="419de-814">Строка, обозначающая конец строки команды.</span><span class="sxs-lookup"><span data-stu-id="419de-814">String that marks the end of a command string.</span></span>

<span data-ttu-id="419de-815">Пример: "<CR"</span><span class="sxs-lookup"><span data-stu-id="419de-815">Example: "<cr"</span></span>

</dd> <dt>

<span data-ttu-id="419de-816">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="419de-816">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-817">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="419de-817">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="419de-818">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-818">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="419de-819">Дата и время последнего сброса модема.</span><span class="sxs-lookup"><span data-stu-id="419de-819">Date and time the modem was last reset.</span></span>

<span data-ttu-id="419de-820">Это свойство наследуется от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-820">This property is inherited from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

</dd> <dt>

<span data-ttu-id="419de-821">**Тон**</span><span class="sxs-lookup"><span data-stu-id="419de-821">**Tone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-822">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-822">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-823">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-823">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-824">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| тоновый")</span><span class="sxs-lookup"><span data-stu-id="419de-824">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|Tone")</span></span>
</dt> </dl>

<span data-ttu-id="419de-825">Командная строка, предопределяющая модему использовать тоновый режим для набора номера.</span><span class="sxs-lookup"><span data-stu-id="419de-825">Command string that instructs the modem to use tone mode for dialing.</span></span> <span data-ttu-id="419de-826">Телефонная линия должна поддерживать тоновый набор.</span><span class="sxs-lookup"><span data-stu-id="419de-826">The phone line must support tone dialing.</span></span>

<span data-ttu-id="419de-827">Пример: "T"</span><span class="sxs-lookup"><span data-stu-id="419de-827">Example: "T"</span></span>

</dd> <dt>

<span data-ttu-id="419de-828">**воицесвитчфеатуре**</span><span class="sxs-lookup"><span data-stu-id="419de-828">**VoiceSwitchFeature**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="419de-829">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="419de-829">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="419de-830">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="419de-830">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="419de-831">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \| воицесвитчфеатуре")</span><span class="sxs-lookup"><span data-stu-id="419de-831">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\Class\|VoiceSwitchFeature")</span></span>
</dt> </dl>

<span data-ttu-id="419de-832">Командные строки, используемые для активации возможностей голоса на голосовом модеме.</span><span class="sxs-lookup"><span data-stu-id="419de-832">Command strings used to activate the voice capabilities of a voice modem.</span></span>

<span data-ttu-id="419de-833">Пример: "AT + V"</span><span class="sxs-lookup"><span data-stu-id="419de-833">Example: "AT+V"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="419de-834">Комментарии</span><span class="sxs-lookup"><span data-stu-id="419de-834">Remarks</span></span>

<span data-ttu-id="419de-835">Класс **Win32 \_ потсмодем** является производным от [**CIM \_ потсмодем**](cim-potsmodem.md).</span><span class="sxs-lookup"><span data-stu-id="419de-835">The **Win32\_POTSModem** class is derived from [**CIM\_PotsModem**](cim-potsmodem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="419de-836">Требования</span><span class="sxs-lookup"><span data-stu-id="419de-836">Requirements</span></span>



| <span data-ttu-id="419de-837">Требование</span><span class="sxs-lookup"><span data-stu-id="419de-837">Requirement</span></span> | <span data-ttu-id="419de-838">Значение</span><span class="sxs-lookup"><span data-stu-id="419de-838">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="419de-839">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="419de-839">Minimum supported client</span></span><br/> | <span data-ttu-id="419de-840">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="419de-840">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="419de-841">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="419de-841">Minimum supported server</span></span><br/> | <span data-ttu-id="419de-842">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="419de-842">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="419de-843">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="419de-843">Namespace</span></span><br/>                | <span data-ttu-id="419de-844">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="419de-844">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="419de-845">MOF</span><span class="sxs-lookup"><span data-stu-id="419de-845">MOF</span></span><br/>                      | <dl> <span data-ttu-id="419de-846"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="419de-846"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="419de-847">DLL</span><span class="sxs-lookup"><span data-stu-id="419de-847">DLL</span></span><br/>                      | <dl> <span data-ttu-id="419de-848"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="419de-848"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="419de-849">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="419de-849">See also</span></span>

<dl> <dt>

[<span data-ttu-id="419de-850">**\_ПОТСМОДЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="419de-850">**CIM\_PotsModem**</span></span>](cim-potsmodem.md)
</dt> <dt>

[<span data-ttu-id="419de-851">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="419de-851">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
