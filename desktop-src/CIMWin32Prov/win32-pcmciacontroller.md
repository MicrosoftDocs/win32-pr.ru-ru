---
description: '&Win32 \_ пкмЦиаконтроллер \# 32; Класс WMI управляет возможностями адаптера интерфейса карты памяти личного компьютера (PCMCIA устройства PC Card).'
ms.assetid: 541f8ebd-e976-425a-817a-72ab151e8b93
ms.tgt_platform: multiple
title: Класс Win32_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PCMCIAController
- Win32_PCMCIAController.Reset
- Win32_PCMCIAController.SetPowerState
- Win32_PCMCIAController.Availability
- Win32_PCMCIAController.Caption
- Win32_PCMCIAController.ConfigManagerErrorCode
- Win32_PCMCIAController.ConfigManagerUserConfig
- Win32_PCMCIAController.CreationClassName
- Win32_PCMCIAController.Description
- Win32_PCMCIAController.DeviceID
- Win32_PCMCIAController.ErrorCleared
- Win32_PCMCIAController.ErrorDescription
- Win32_PCMCIAController.InstallDate
- Win32_PCMCIAController.LastErrorCode
- Win32_PCMCIAController.Manufacturer
- Win32_PCMCIAController.MaxNumberControlled
- Win32_PCMCIAController.Name
- Win32_PCMCIAController.PNPDeviceID
- Win32_PCMCIAController.PowerManagementCapabilities
- Win32_PCMCIAController.PowerManagementSupported
- Win32_PCMCIAController.ProtocolSupported
- Win32_PCMCIAController.Status
- Win32_PCMCIAController.StatusInfo
- Win32_PCMCIAController.SystemCreationClassName
- Win32_PCMCIAController.SystemName
- Win32_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 463be0c3924130ce0e2c0ff84c3852398b6cff99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262747"
---
# <a name="win32_pcmciacontroller-class"></a><span data-ttu-id="740e9-103">\_Класс Win32 пкмЦиаконтроллер</span><span class="sxs-lookup"><span data-stu-id="740e9-103">Win32\_PCMCIAController class</span></span>

<span data-ttu-id="740e9-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ пкмЦиаконтроллер для Win32** управляет возможностями интерфейса адаптера памяти личного компьютера с контроллером контроллера PC Card (PCMCIA).</span><span class="sxs-lookup"><span data-stu-id="740e9-104">The **Win32\_PCMCIAController** [WMI class](../wmisdk/retrieving-a-class.md) manages the capabilities of a Personal Computer Memory Card Interface Adapter (PCMCIA of a PC Card) controller device.</span></span>

<span data-ttu-id="740e9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="740e9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="740e9-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="740e9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="740e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="740e9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{98C7E2C6-D592-11d2-B355-00105A0A323A}"), AMENDMENT]
class Win32_PCMCIAController : CIM_PCMCIAController
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

## <a name="members"></a><span data-ttu-id="740e9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="740e9-108">Members</span></span>

<span data-ttu-id="740e9-109">Класс **Win32 \_ пкмЦиаконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="740e9-109">The **Win32\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="740e9-110">Методы</span><span class="sxs-lookup"><span data-stu-id="740e9-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="740e9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="740e9-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="740e9-112">Методы</span><span class="sxs-lookup"><span data-stu-id="740e9-112">Methods</span></span>

<span data-ttu-id="740e9-113">Класс **Win32 \_ пкмЦиаконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="740e9-113">The **Win32\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="740e9-114">Метод</span><span class="sxs-lookup"><span data-stu-id="740e9-114">Method</span></span>            | <span data-ttu-id="740e9-115">Описание</span><span class="sxs-lookup"><span data-stu-id="740e9-115">Description</span></span>                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="740e9-116">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="740e9-116">**Reset**</span></span>         | <span data-ttu-id="740e9-117">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="740e9-117">Not implemented.</span></span> <span data-ttu-id="740e9-118">Чтобы реализовать этот метод, см. метод [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ пкмЦиаконтроллер**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-118">To implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span><br/>                 |
| <span data-ttu-id="740e9-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="740e9-119">**SetPowerState**</span></span> | <span data-ttu-id="740e9-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="740e9-120">Not implemented.</span></span> <span data-ttu-id="740e9-121">Чтобы реализовать этот метод, см. метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ пкмЦиаконтроллер**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-121">To implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="740e9-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="740e9-122">Properties</span></span>

<span data-ttu-id="740e9-123">Класс **Win32 \_ пкмЦиаконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="740e9-123">The **Win32\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="740e9-124">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="740e9-124">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="740e9-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-127">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="740e9-127">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-128">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-128">Availability and status of the device.</span></span>

<span data-ttu-id="740e9-129">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-129">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="740e9-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="740e9-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="740e9-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="740e9-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="740e9-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="740e9-132"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-133">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="740e9-133">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="740e9-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="740e9-134"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="740e9-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="740e9-135"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="740e9-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="740e9-136"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="740e9-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="740e9-137"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="740e9-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="740e9-138"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="740e9-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="740e9-139"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="740e9-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="740e9-140"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="740e9-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="740e9-141"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="740e9-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="740e9-142"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="740e9-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="740e9-143"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-144">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="740e9-144">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="740e9-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="740e9-145"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-146">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="740e9-146">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="740e9-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="740e9-147"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-148">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="740e9-148">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="740e9-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="740e9-149"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="740e9-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="740e9-150"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-151">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="740e9-151">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="740e9-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="740e9-152"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-153">приостановлено</span><span class="sxs-lookup"><span data-stu-id="740e9-153">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="740e9-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="740e9-154"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-155">Не готово.</span><span class="sxs-lookup"><span data-stu-id="740e9-155">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="740e9-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="740e9-156"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-157">не настроено.</span><span class="sxs-lookup"><span data-stu-id="740e9-157">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="740e9-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="740e9-158"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-159">Состояние.</span><span class="sxs-lookup"><span data-stu-id="740e9-159">Quiesced.</span></span>

<span data-ttu-id="740e9-160">Контроллер PCMCIA недоступен.</span><span class="sxs-lookup"><span data-stu-id="740e9-160">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="740e9-161">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="740e9-161">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-164">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="740e9-164">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-165">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="740e9-165">Short description of the object.</span></span>

<span data-ttu-id="740e9-166">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-166">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-167">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="740e9-167">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="740e9-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-170">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="740e9-170">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-171">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="740e9-171">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="740e9-172">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-172">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="740e9-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="740e9-173"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="740e9-174"> (0)</span><span class="sxs-lookup"><span data-stu-id="740e9-174">(0)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-175">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="740e9-175">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="740e9-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="740e9-176"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="740e9-177">(1)</span><span class="sxs-lookup"><span data-stu-id="740e9-177">(1)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-178">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="740e9-178">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="740e9-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-179"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="740e9-180">(2)</span><span class="sxs-lookup"><span data-stu-id="740e9-180">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="740e9-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="740e9-181"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="740e9-182">(3)</span><span class="sxs-lookup"><span data-stu-id="740e9-182">(3)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-183">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="740e9-183">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="740e9-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="740e9-184"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="740e9-185">(4)</span><span class="sxs-lookup"><span data-stu-id="740e9-185">(4)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-186">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="740e9-186">Device is not working properly.</span></span> <span data-ttu-id="740e9-187">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="740e9-187">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="740e9-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="740e9-188"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="740e9-189">(5)</span><span class="sxs-lookup"><span data-stu-id="740e9-189">(5)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-190">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="740e9-190">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="740e9-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="740e9-191"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="740e9-192"> (6)</span><span class="sxs-lookup"><span data-stu-id="740e9-192">(6)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-193">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="740e9-193">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="740e9-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="740e9-194"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="740e9-195">(7)</span><span class="sxs-lookup"><span data-stu-id="740e9-195">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="740e9-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-196"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="740e9-197">(8)</span><span class="sxs-lookup"><span data-stu-id="740e9-197">(8)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-198">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-198">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="740e9-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-199"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="740e9-200">(9)</span><span class="sxs-lookup"><span data-stu-id="740e9-200">(9)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-201">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="740e9-201">Device is not working properly.</span></span> <span data-ttu-id="740e9-202">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-202">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="740e9-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="740e9-203"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="740e9-204">(10)</span><span class="sxs-lookup"><span data-stu-id="740e9-204">(10)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-205">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="740e9-205">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="740e9-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-206"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="740e9-207">(11)</span><span class="sxs-lookup"><span data-stu-id="740e9-207">(11)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-208">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-208">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="740e9-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="740e9-209"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="740e9-210">(12)</span><span class="sxs-lookup"><span data-stu-id="740e9-210">(12)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-211">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="740e9-211">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="740e9-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-212"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="740e9-213">(13)</span><span class="sxs-lookup"><span data-stu-id="740e9-213">(13)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-214">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-214">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="740e9-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="740e9-215"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="740e9-216">(14)</span><span class="sxs-lookup"><span data-stu-id="740e9-216">(14)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-217">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="740e9-217">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="740e9-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="740e9-218"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="740e9-219">(15)</span><span class="sxs-lookup"><span data-stu-id="740e9-219">(15)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-220">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="740e9-220">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="740e9-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="740e9-221"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="740e9-222">(16)</span><span class="sxs-lookup"><span data-stu-id="740e9-222">(16)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-223">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="740e9-223">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="740e9-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="740e9-224"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="740e9-225">(17)</span><span class="sxs-lookup"><span data-stu-id="740e9-225">(17)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-226">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="740e9-226">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="740e9-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-227"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="740e9-228">(18)</span><span class="sxs-lookup"><span data-stu-id="740e9-228">(18)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-229">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="740e9-229">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="740e9-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="740e9-230"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="740e9-231">(19)</span><span class="sxs-lookup"><span data-stu-id="740e9-231">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="740e9-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="740e9-232"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="740e9-233">(20)</span><span class="sxs-lookup"><span data-stu-id="740e9-233">(20)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-234">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="740e9-234">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="740e9-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="740e9-235"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="740e9-236">(21)</span><span class="sxs-lookup"><span data-stu-id="740e9-236">(21)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-237">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="740e9-237">System failure.</span></span> <span data-ttu-id="740e9-238">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="740e9-238">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="740e9-239">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="740e9-239">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="740e9-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="740e9-240"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="740e9-241">(22)</span><span class="sxs-lookup"><span data-stu-id="740e9-241">(22)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-242">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="740e9-242">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="740e9-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="740e9-243"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="740e9-244">(23)</span><span class="sxs-lookup"><span data-stu-id="740e9-244">(23)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-245">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="740e9-245">System failure.</span></span> <span data-ttu-id="740e9-246">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="740e9-246">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="740e9-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="740e9-247"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="740e9-248">(24)</span><span class="sxs-lookup"><span data-stu-id="740e9-248">(24)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-249">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="740e9-249">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="740e9-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="740e9-250"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="740e9-251">(25)</span><span class="sxs-lookup"><span data-stu-id="740e9-251">(25)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-252">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="740e9-252">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="740e9-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="740e9-253"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="740e9-254">(26)</span><span class="sxs-lookup"><span data-stu-id="740e9-254">(26)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-255">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="740e9-255">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="740e9-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="740e9-256"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="740e9-257">(27)</span><span class="sxs-lookup"><span data-stu-id="740e9-257">(27)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-258">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="740e9-258">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="740e9-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="740e9-259"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="740e9-260">(28)</span><span class="sxs-lookup"><span data-stu-id="740e9-260">(28)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-261">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="740e9-261">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="740e9-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="740e9-262"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="740e9-263">(29)</span><span class="sxs-lookup"><span data-stu-id="740e9-263">(29)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-264">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="740e9-264">Device is disabled.</span></span> <span data-ttu-id="740e9-265">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="740e9-265">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="740e9-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="740e9-266"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="740e9-267">(30)</span><span class="sxs-lookup"><span data-stu-id="740e9-267">(30)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-268">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="740e9-268">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="740e9-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="740e9-269"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="740e9-270">1-31</span><span class="sxs-lookup"><span data-stu-id="740e9-270">(31)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-271">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="740e9-271">Device is not working properly.</span></span> <span data-ttu-id="740e9-272">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="740e9-272">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="740e9-273">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="740e9-273">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-274">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="740e9-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-276">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="740e9-276">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-277">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="740e9-277">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="740e9-278">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-278">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-279">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="740e9-279">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-282">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="740e9-282">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="740e9-283">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="740e9-283">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="740e9-284">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="740e9-284">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="740e9-285">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-285">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-286">**Описание**</span><span class="sxs-lookup"><span data-stu-id="740e9-286">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-287">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-289">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="740e9-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-290">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="740e9-290">Description of the object.</span></span>

<span data-ttu-id="740e9-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-292">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="740e9-292">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-295">Квалификаторы: [**переопределить**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="740e9-295">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-296">Уникальный идентификатор этого устройства с другими периферийными устройствами с помощью самонастраивающийся BIOS.</span><span class="sxs-lookup"><span data-stu-id="740e9-296">Unique identifier of this device with other peripherals using the Plug and Play BIOS.</span></span> <span data-ttu-id="740e9-297">Это свойство является производным [**от \_ CIM**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="740e9-297">This property is derived from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-298">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="740e9-298">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-299">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="740e9-299">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="740e9-301">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="740e9-301">If **TRUE**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="740e9-302">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-302">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-303">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="740e9-303">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-304">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="740e9-306">Дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="740e9-306">More information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="740e9-307">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="740e9-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-309">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="740e9-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-311">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="740e9-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-312">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="740e9-312">Date and time the object was installed.</span></span> <span data-ttu-id="740e9-313">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="740e9-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="740e9-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-315">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="740e9-315">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-316">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="740e9-316">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-317">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="740e9-318">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="740e9-318">Last error code reported by the logical device.</span></span>

<span data-ttu-id="740e9-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-320">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="740e9-320">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-321">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-323">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="740e9-323">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-324">Имя изготовителя PCMCIA Controller.</span><span class="sxs-lookup"><span data-stu-id="740e9-324">Name of the PCMCIA controller manufacturer.</span></span>

<span data-ttu-id="740e9-325">Это свойство наследуется от [**CIM \_ пкмЦиаконтроллер**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-325">This property is inherited from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span>

<span data-ttu-id="740e9-326">Пример: ACME</span><span class="sxs-lookup"><span data-stu-id="740e9-326">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="740e9-327">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="740e9-327">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-328">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="740e9-328">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-330">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="740e9-330">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-331">Максимальное число напрямую предоставляемых сущностей, которые поддерживаются этим контроллером.</span><span class="sxs-lookup"><span data-stu-id="740e9-331">Maximum number of directly addressable entities supportable by this controller.</span></span> <span data-ttu-id="740e9-332">Если число неизвестно, следует использовать значение 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="740e9-332">A value of 0 (zero) should be used if the number is unknown.</span></span>

<span data-ttu-id="740e9-333">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-333">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-334">**Name**</span><span class="sxs-lookup"><span data-stu-id="740e9-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-335">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-337">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="740e9-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-338">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="740e9-338">Label by which the object is known.</span></span> <span data-ttu-id="740e9-339">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="740e9-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="740e9-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-341">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="740e9-341">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-344">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="740e9-344">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-345">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-345">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="740e9-346">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-346">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="740e9-347">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="740e9-347">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="740e9-348">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="740e9-348">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-349">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="740e9-349">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="740e9-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="740e9-351">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="740e9-351">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="740e9-352">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-352">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="740e9-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="740e9-353"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="740e9-354"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="740e9-354"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="740e9-355"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="740e9-355"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="740e9-356"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="740e9-356"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-357">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="740e9-357">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="740e9-358"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="740e9-358"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-359">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="740e9-359">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="740e9-360"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="740e9-360"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-361">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="740e9-361">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="740e9-362">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="740e9-362">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="740e9-363">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-363">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="740e9-364"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="740e9-364"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-365">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="740e9-365">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="740e9-366"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="740e9-366"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="740e9-367">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="740e9-367">Timed Power-On Supported</span></span>

<span data-ttu-id="740e9-368">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="740e9-368">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="740e9-369">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="740e9-369">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-370">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="740e9-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="740e9-372">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="740e9-372">If **TRUE**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="740e9-373">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="740e9-373">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="740e9-374">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-375">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="740e9-375">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-376">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="740e9-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-378">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="740e9-378">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-379">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="740e9-379">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="740e9-380">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-380">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span> <span data-ttu-id="740e9-381">Значения показаны в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="740e9-381">The values are shown in the following list.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="740e9-382">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="740e9-382">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="740e9-383">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="740e9-383">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="740e9-384">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="740e9-384">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="740e9-385">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="740e9-385">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="740e9-386">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="740e9-386">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="740e9-387">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="740e9-387">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="740e9-388">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="740e9-388">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="740e9-389">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="740e9-389">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="740e9-390">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="740e9-390">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="740e9-391">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="740e9-391">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="740e9-392">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="740e9-392">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="740e9-393">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="740e9-393">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="740e9-394">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="740e9-394">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="740e9-395">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="740e9-395">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="740e9-396">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="740e9-396">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="740e9-397">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="740e9-397">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="740e9-398">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="740e9-398">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="740e9-399">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="740e9-399">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="740e9-400">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="740e9-400">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="740e9-401">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="740e9-401">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="740e9-402">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="740e9-402">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="740e9-403">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="740e9-403">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="740e9-404">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="740e9-404">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="740e9-405">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="740e9-405">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="740e9-406">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="740e9-406">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="740e9-407">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="740e9-407">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="740e9-408">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="740e9-408">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="740e9-409">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="740e9-409">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="740e9-410">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="740e9-410">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="740e9-411">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="740e9-411">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="740e9-412">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="740e9-412">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="740e9-413">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="740e9-413">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="740e9-414">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="740e9-414">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="740e9-415">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="740e9-415">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="740e9-416">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="740e9-416">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="740e9-417">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="740e9-417">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="740e9-418">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="740e9-418">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="740e9-419">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="740e9-419">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="740e9-420">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="740e9-420">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="740e9-421">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="740e9-421">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="740e9-422">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="740e9-422">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="740e9-423">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="740e9-423">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="740e9-424">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="740e9-424">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="740e9-425">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="740e9-425">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="740e9-426">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="740e9-426">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="740e9-427">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="740e9-427">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="740e9-428">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="740e9-428">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="740e9-429">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="740e9-429">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-430">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-431">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-432">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="740e9-432">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-433">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="740e9-433">Current status of the object.</span></span> <span data-ttu-id="740e9-434">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="740e9-434">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="740e9-435">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="740e9-435">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="740e9-436">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="740e9-436">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="740e9-437">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="740e9-437">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="740e9-438">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="740e9-438">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="740e9-439">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="740e9-440">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="740e9-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="740e9-441">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="740e9-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="740e9-442">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="740e9-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="740e9-443">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="740e9-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="740e9-444">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="740e9-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="740e9-445">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="740e9-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="740e9-446">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="740e9-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="740e9-447">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="740e9-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="740e9-448">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="740e9-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="740e9-449">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="740e9-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="740e9-450">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="740e9-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="740e9-451">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="740e9-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="740e9-452">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="740e9-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="740e9-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="740e9-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="740e9-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-456">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="740e9-456">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="740e9-457">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="740e9-457">State of the logical device.</span></span> <span data-ttu-id="740e9-458">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="740e9-458">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="740e9-459">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="740e9-460">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="740e9-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="740e9-461">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="740e9-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="740e9-462">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="740e9-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="740e9-463">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="740e9-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="740e9-464">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="740e9-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="740e9-465">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="740e9-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-468">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="740e9-468">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="740e9-469">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="740e9-469">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="740e9-470">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="740e9-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="740e9-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-473">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="740e9-474">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="740e9-474">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="740e9-475">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="740e9-475">Name of the scoping system.</span></span>

<span data-ttu-id="740e9-476">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="740e9-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="740e9-477">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="740e9-477">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="740e9-478">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="740e9-478">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="740e9-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="740e9-479">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="740e9-480">Дата и время последнего сброса контроллера.</span><span class="sxs-lookup"><span data-stu-id="740e9-480">Date and time the controller was last reset.</span></span> <span data-ttu-id="740e9-481">Это может означать, что контроллер был отключен или инициализирован повторно.</span><span class="sxs-lookup"><span data-stu-id="740e9-481">This could mean the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="740e9-482">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-482">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="740e9-483">Комментарии</span><span class="sxs-lookup"><span data-stu-id="740e9-483">Remarks</span></span>

<span data-ttu-id="740e9-484">Класс **Win32 \_ пкмЦиаконтроллер** является производным от [**CIM \_ пкмЦиаконтроллер**](cim-pcmciacontroller.md).</span><span class="sxs-lookup"><span data-stu-id="740e9-484">The **Win32\_PCMCIAController** class is derived from [**CIM\_PCMCIAController**](cim-pcmciacontroller.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="740e9-485">Требования</span><span class="sxs-lookup"><span data-stu-id="740e9-485">Requirements</span></span>



| <span data-ttu-id="740e9-486">Требование</span><span class="sxs-lookup"><span data-stu-id="740e9-486">Requirement</span></span> | <span data-ttu-id="740e9-487">Значение</span><span class="sxs-lookup"><span data-stu-id="740e9-487">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="740e9-488">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="740e9-488">Minimum supported client</span></span><br/> | <span data-ttu-id="740e9-489">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="740e9-489">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="740e9-490">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="740e9-490">Minimum supported server</span></span><br/> | <span data-ttu-id="740e9-491">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="740e9-491">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="740e9-492">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="740e9-492">Namespace</span></span><br/>                | <span data-ttu-id="740e9-493">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="740e9-493">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="740e9-494">MOF</span><span class="sxs-lookup"><span data-stu-id="740e9-494">MOF</span></span><br/>                      | <dl> <span data-ttu-id="740e9-495"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="740e9-495"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="740e9-496">DLL</span><span class="sxs-lookup"><span data-stu-id="740e9-496">DLL</span></span><br/>                      | <dl> <span data-ttu-id="740e9-497"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="740e9-497"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="740e9-498">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="740e9-498">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740e9-499">**\_ПКМЦИАКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="740e9-499">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dt>

[<span data-ttu-id="740e9-500">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="740e9-500">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
