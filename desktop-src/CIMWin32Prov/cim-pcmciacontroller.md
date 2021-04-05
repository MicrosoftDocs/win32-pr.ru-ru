---
description: Класс CIM \_ пкмЦиаконтроллер представляет возможности и Управление контроллером международной связи с картой памяти персональных компьютеров (PCMCIA).
ms.assetid: 341cbc6c-dd25-4dea-bcce-cd4e3f4d5324
ms.tgt_platform: multiple
title: Класс CIM_PCMCIAController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PCMCIAController
- CIM_PCMCIAController.Availability
- CIM_PCMCIAController.Caption
- CIM_PCMCIAController.ConfigManagerErrorCode
- CIM_PCMCIAController.ConfigManagerUserConfig
- CIM_PCMCIAController.CreationClassName
- CIM_PCMCIAController.Description
- CIM_PCMCIAController.DeviceID
- CIM_PCMCIAController.ErrorCleared
- CIM_PCMCIAController.ErrorDescription
- CIM_PCMCIAController.InstallDate
- CIM_PCMCIAController.LastErrorCode
- CIM_PCMCIAController.Manufacturer
- CIM_PCMCIAController.MaxNumberControlled
- CIM_PCMCIAController.Name
- CIM_PCMCIAController.PNPDeviceID
- CIM_PCMCIAController.PowerManagementCapabilities
- CIM_PCMCIAController.PowerManagementSupported
- CIM_PCMCIAController.ProtocolSupported
- CIM_PCMCIAController.Status
- CIM_PCMCIAController.StatusInfo
- CIM_PCMCIAController.SystemCreationClassName
- CIM_PCMCIAController.SystemName
- CIM_PCMCIAController.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95d05e11dd0c439708c477e3ec776bc7a2c333d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141343"
---
# <a name="cim_pcmciacontroller-class"></a><span data-ttu-id="0f762-103">\_Класс CIM пкмЦиаконтроллер</span><span class="sxs-lookup"><span data-stu-id="0f762-103">CIM\_PCMCIAController class</span></span>

<span data-ttu-id="0f762-104">Класс **CIM \_ пкмЦиаконтроллер** представляет возможности и Управление контроллером международной связи с картой памяти персональных компьютеров (PCMCIA).</span><span class="sxs-lookup"><span data-stu-id="0f762-104">The **CIM\_PCMCIAController** class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f762-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0f762-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0f762-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0f762-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0f762-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0f762-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0f762-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0f762-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f762-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f762-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B5A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PCMCIAController : cim_controller
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

## <a name="members"></a><span data-ttu-id="0f762-110">Члены</span><span class="sxs-lookup"><span data-stu-id="0f762-110">Members</span></span>

<span data-ttu-id="0f762-111">Класс **CIM \_ пкмЦиаконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f762-111">The **CIM\_PCMCIAController** class has these types of members:</span></span>

-   [<span data-ttu-id="0f762-112">Методы</span><span class="sxs-lookup"><span data-stu-id="0f762-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="0f762-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f762-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0f762-114">Методы</span><span class="sxs-lookup"><span data-stu-id="0f762-114">Methods</span></span>

<span data-ttu-id="0f762-115">Класс **CIM \_ пкмЦиаконтроллер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0f762-115">The **CIM\_PCMCIAController** class has these methods.</span></span>



| <span data-ttu-id="0f762-116">Метод</span><span class="sxs-lookup"><span data-stu-id="0f762-116">Method</span></span>                                                                      | <span data-ttu-id="0f762-117">Описание</span><span class="sxs-lookup"><span data-stu-id="0f762-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f762-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="0f762-118">**Reset**</span></span>](reset-method-in-class-cim-pcmciacontroller.md)                 | <span data-ttu-id="0f762-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="0f762-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0f762-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="0f762-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0f762-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-pcmciacontroller.md) | <span data-ttu-id="0f762-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="0f762-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="0f762-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="0f762-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0f762-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f762-124">Properties</span></span>

<span data-ttu-id="0f762-125">Класс **CIM \_ пкмЦиаконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f762-125">The **CIM\_PCMCIAController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f762-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="0f762-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f762-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="0f762-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-130">Availability and status of the device.</span></span> <span data-ttu-id="0f762-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0f762-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0f762-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-133">Другое</span><span class="sxs-lookup"><span data-stu-id="0f762-133">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f762-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0f762-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-135">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="0f762-135">Unknown.</span></span>

</dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0f762-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="0f762-136"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-137">Работа или полная мощность.</span><span class="sxs-lookup"><span data-stu-id="0f762-137">Running or full power.</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0f762-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="0f762-138"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-139">Внимание!</span><span class="sxs-lookup"><span data-stu-id="0f762-139">Warning.</span></span>

</dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0f762-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="0f762-140"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-141">Тестирование.</span><span class="sxs-lookup"><span data-stu-id="0f762-141">Testing.</span></span>

</dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0f762-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="0f762-142"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-143">Не применяется</span><span class="sxs-lookup"><span data-stu-id="0f762-143">Not applicable.</span></span>

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0f762-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="0f762-144"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-145">Выключение питания.</span><span class="sxs-lookup"><span data-stu-id="0f762-145">Power off.</span></span>

</dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0f762-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="0f762-146"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-147">Вне сети.</span><span class="sxs-lookup"><span data-stu-id="0f762-147">Offline.</span></span>

</dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0f762-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="0f762-148"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-149">Не обслуживает.</span><span class="sxs-lookup"><span data-stu-id="0f762-149">Off duty.</span></span>

</dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0f762-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="0f762-150"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-151">"Пониженная функциональность".</span><span class="sxs-lookup"><span data-stu-id="0f762-151">Degraded.</span></span>

</dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0f762-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="0f762-152"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-153">Не установлено.</span><span class="sxs-lookup"><span data-stu-id="0f762-153">Not installed.</span></span>

</dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0f762-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="0f762-154"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-155">Ошибка установки.</span><span class="sxs-lookup"><span data-stu-id="0f762-155">Install error.</span></span>

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0f762-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="0f762-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-157">Известно, что устройство находится в режиме энергосбережения, но его точное состояние в этом режиме неизвестно.</span><span class="sxs-lookup"><span data-stu-id="0f762-157">Device is known to be in a power save mode, but its exact status in this mode is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0f762-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="0f762-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-159">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="0f762-159">Device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0f762-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="0f762-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-161">Устройство не работает, но может быть включено в полную работу.</span><span class="sxs-lookup"><span data-stu-id="0f762-161">Device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0f762-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="0f762-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-163">Цикл электропитания.</span><span class="sxs-lookup"><span data-stu-id="0f762-163">Power cycle.</span></span>

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0f762-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="0f762-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-165">Устройство находится в состоянии предупреждения, а также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="0f762-165">Device is in a warning state and also in a power-save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0f762-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="0f762-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-167">приостановлено</span><span class="sxs-lookup"><span data-stu-id="0f762-167">Paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0f762-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="0f762-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-169">Не готово.</span><span class="sxs-lookup"><span data-stu-id="0f762-169">Not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0f762-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="0f762-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-171">не настроено.</span><span class="sxs-lookup"><span data-stu-id="0f762-171">Not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0f762-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="0f762-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-173">Контроллер PCMCIA недоступен.</span><span class="sxs-lookup"><span data-stu-id="0f762-173">The PCMCIA controller is unavailable.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f762-174">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0f762-174">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-177">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0f762-177">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-178">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0f762-178">Short textual description of the object.</span></span>

<span data-ttu-id="0f762-179">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-180">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="0f762-180">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-181">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f762-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-183">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f762-183">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-184">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0f762-184">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="0f762-185">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-185">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0f762-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="0f762-186"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0f762-187"> (0)</span><span class="sxs-lookup"><span data-stu-id="0f762-187">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-188">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="0f762-188">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0f762-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="0f762-189"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0f762-190">(1)</span><span class="sxs-lookup"><span data-stu-id="0f762-190">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-191">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="0f762-191">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0f762-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-192"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0f762-193">(2)</span><span class="sxs-lookup"><span data-stu-id="0f762-193">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0f762-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="0f762-194"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0f762-195">(3)</span><span class="sxs-lookup"><span data-stu-id="0f762-195">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-196">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f762-196">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0f762-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="0f762-197"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0f762-198">(4)</span><span class="sxs-lookup"><span data-stu-id="0f762-198">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-199">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0f762-199">Device is not working properly.</span></span> <span data-ttu-id="0f762-200">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0f762-200">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0f762-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="0f762-201"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0f762-202">(5)</span><span class="sxs-lookup"><span data-stu-id="0f762-202">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-203">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="0f762-203">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0f762-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="0f762-204"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0f762-205"> (6)</span><span class="sxs-lookup"><span data-stu-id="0f762-205">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-206">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="0f762-206">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0f762-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="0f762-207"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0f762-208">(7)</span><span class="sxs-lookup"><span data-stu-id="0f762-208">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0f762-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-209"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0f762-210">(8)</span><span class="sxs-lookup"><span data-stu-id="0f762-210">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-211">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-211">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0f762-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-212"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0f762-213">(9)</span><span class="sxs-lookup"><span data-stu-id="0f762-213">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-214">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0f762-214">Device is not working properly.</span></span> <span data-ttu-id="0f762-215">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-215">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0f762-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="0f762-216"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0f762-217">(10)</span><span class="sxs-lookup"><span data-stu-id="0f762-217">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-218">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="0f762-218">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0f762-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-219"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0f762-220">(11)</span><span class="sxs-lookup"><span data-stu-id="0f762-220">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-221">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-221">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0f762-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="0f762-222"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0f762-223">(12)</span><span class="sxs-lookup"><span data-stu-id="0f762-223">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-224">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="0f762-224">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0f762-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-225"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0f762-226">(13)</span><span class="sxs-lookup"><span data-stu-id="0f762-226">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-227">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-227">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0f762-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="0f762-228"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0f762-229">(14)</span><span class="sxs-lookup"><span data-stu-id="0f762-229">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-230">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="0f762-230">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0f762-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="0f762-231"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0f762-232">(15)</span><span class="sxs-lookup"><span data-stu-id="0f762-232">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-233">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="0f762-233">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0f762-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="0f762-234"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0f762-235">(16)</span><span class="sxs-lookup"><span data-stu-id="0f762-235">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-236">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="0f762-236">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0f762-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="0f762-237"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0f762-238">(17)</span><span class="sxs-lookup"><span data-stu-id="0f762-238">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-239">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f762-239">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0f762-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-240"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0f762-241">(18)</span><span class="sxs-lookup"><span data-stu-id="0f762-241">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-242">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="0f762-242">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0f762-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="0f762-243"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0f762-244">(19)</span><span class="sxs-lookup"><span data-stu-id="0f762-244">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0f762-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="0f762-245"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0f762-246">(20)</span><span class="sxs-lookup"><span data-stu-id="0f762-246">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-247">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0f762-247">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0f762-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="0f762-248"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0f762-249">(21)</span><span class="sxs-lookup"><span data-stu-id="0f762-249">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-250">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="0f762-250">System failure.</span></span> <span data-ttu-id="0f762-251">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="0f762-251">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0f762-252">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="0f762-252">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0f762-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="0f762-253"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0f762-254">(22)</span><span class="sxs-lookup"><span data-stu-id="0f762-254">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-255">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="0f762-255">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0f762-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="0f762-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0f762-257">(23)</span><span class="sxs-lookup"><span data-stu-id="0f762-257">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-258">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="0f762-258">System failure.</span></span> <span data-ttu-id="0f762-259">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="0f762-259">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0f762-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="0f762-260"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0f762-261">(24)</span><span class="sxs-lookup"><span data-stu-id="0f762-261">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-262">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="0f762-262">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0f762-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="0f762-263"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0f762-264">(25)</span><span class="sxs-lookup"><span data-stu-id="0f762-264">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-265">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="0f762-265">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0f762-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="0f762-266"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0f762-267">(26)</span><span class="sxs-lookup"><span data-stu-id="0f762-267">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-268">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="0f762-268">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0f762-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="0f762-269"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0f762-270">(27)</span><span class="sxs-lookup"><span data-stu-id="0f762-270">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-271">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="0f762-271">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0f762-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="0f762-272"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0f762-273">(28)</span><span class="sxs-lookup"><span data-stu-id="0f762-273">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-274">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="0f762-274">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0f762-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="0f762-275"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0f762-276">(29)</span><span class="sxs-lookup"><span data-stu-id="0f762-276">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-277">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="0f762-277">Device is disabled.</span></span> <span data-ttu-id="0f762-278">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0f762-278">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0f762-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="0f762-279"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0f762-280">(30)</span><span class="sxs-lookup"><span data-stu-id="0f762-280">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-281">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="0f762-281">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0f762-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0f762-282"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0f762-283">1-31</span><span class="sxs-lookup"><span data-stu-id="0f762-283">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-284">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0f762-284">Device is not working properly.</span></span> <span data-ttu-id="0f762-285">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="0f762-285">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f762-286">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="0f762-286">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-287">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0f762-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-288">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-289">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f762-289">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-290">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0f762-290">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0f762-291">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-291">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-292">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0f762-292">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-295">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f762-295">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f762-296">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0f762-296">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="0f762-297">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="0f762-297">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0f762-298">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-299">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f762-299">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-300">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-301">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-302">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="0f762-302">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-303">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0f762-303">Textual description of the object.</span></span>

<span data-ttu-id="0f762-304">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-305">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0f762-305">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-306">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-307">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-308">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f762-308">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f762-309">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-309">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="0f762-310">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-310">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-311">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="0f762-311">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-312">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0f762-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f762-314">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="0f762-314">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="0f762-315">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-315">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-316">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0f762-316">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f762-319">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="0f762-319">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="0f762-320">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-320">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-321">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0f762-321">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-322">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f762-322">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-324">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="0f762-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-325">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0f762-325">Date and time the object was installed.</span></span> <span data-ttu-id="0f762-326">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="0f762-326">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0f762-327">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-327">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-328">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="0f762-328">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-329">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f762-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f762-331">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="0f762-331">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0f762-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-333">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="0f762-333">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-336">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f762-336">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-337">Имя изготовителя PCMCIA Controller.</span><span class="sxs-lookup"><span data-stu-id="0f762-337">Name of the PCMCIA controller manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="0f762-338">**макснумберконтроллед**</span><span class="sxs-lookup"><span data-stu-id="0f762-338">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-339">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f762-339">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-341">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,9 ")</span><span class="sxs-lookup"><span data-stu-id="0f762-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-342">Максимальное количество напрямую обрабатываемых сущностей, поддерживаемых контроллером.</span><span class="sxs-lookup"><span data-stu-id="0f762-342">Maximum number of directly addressable entities supported by the controller.</span></span> <span data-ttu-id="0f762-343">Если число неизвестно или неограниченно, следует использовать значение 0.</span><span class="sxs-lookup"><span data-stu-id="0f762-343">A value of 0 should be used if the number is unknown or unlimited.</span></span>

<span data-ttu-id="0f762-344">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-344">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-345">**Name**</span><span class="sxs-lookup"><span data-stu-id="0f762-345">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-348">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="0f762-348">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-349">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="0f762-349">Label by which the object is known.</span></span> <span data-ttu-id="0f762-350">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="0f762-350">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="0f762-351">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-351">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-352">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0f762-352">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-355">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0f762-355">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-356">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-356">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="0f762-357">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-357">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0f762-358">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0f762-358">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0f762-359">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="0f762-359">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-360">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0f762-360">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0f762-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f762-362">Конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="0f762-362">Specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="0f762-363">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f762-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0f762-364"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-365">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="0f762-365">Unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0f762-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="0f762-366"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-367">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0f762-367">Not supported.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0f762-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="0f762-368"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-369">Отключена.</span><span class="sxs-lookup"><span data-stu-id="0f762-369">Disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0f762-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="0f762-370"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-371">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="0f762-371">Power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0f762-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="0f762-372"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-373">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="0f762-373">Device can change its power state based on use or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0f762-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="0f762-374"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-375">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="0f762-375">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method is supported.</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0f762-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="0f762-376"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-377">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="0f762-377">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0f762-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="0f762-378"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0f762-379">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="0f762-379">The [**SetPowerState**](setpowerstate-method-in-class-cim-pcmciacontroller.md) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0f762-380">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="0f762-380">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-381">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0f762-381">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-382">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-382">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f762-383">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="0f762-383">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="0f762-384">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="0f762-384">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="0f762-385">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="0f762-385">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="0f762-386">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="0f762-386">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="0f762-387">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-387">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-388">**протоколсуппортед**</span><span class="sxs-lookup"><span data-stu-id="0f762-388">**ProtocolSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-389">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f762-389">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-390">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-391">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Порт шины DMTF \| 001,2 "," MIF. \|Диски DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0f762-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Bus Port\|001.2", "MIF.DMTF\|Disks\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-392">Протокол, используемый контроллером для доступа к контролируемым устройствам.</span><span class="sxs-lookup"><span data-stu-id="0f762-392">Protocol used by the controller to access "controlled" devices.</span></span>

<span data-ttu-id="0f762-393">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-393">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="0f762-394">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0f762-394">Values are:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0f762-395">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0f762-395">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f762-396">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0f762-396">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="0f762-397">**EISA** (3)</span><span class="sxs-lookup"><span data-stu-id="0f762-397">**EISA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="0f762-398">**ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="0f762-398">**ISA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="0f762-399">**PCI** (5)</span><span class="sxs-lookup"><span data-stu-id="0f762-399">**PCI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span data-ttu-id="0f762-400">**ATA/ATAPI** (6)</span><span class="sxs-lookup"><span data-stu-id="0f762-400">**ATA/ATAPI** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span data-ttu-id="0f762-401">**Гибкая дискета** (7)</span><span class="sxs-lookup"><span data-stu-id="0f762-401">**Flexible Diskette** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span data-ttu-id="0f762-402">**1496** (8)</span><span class="sxs-lookup"><span data-stu-id="0f762-402">**1496** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span data-ttu-id="0f762-403">**Параллельный интерфейс SCSI** (9)</span><span class="sxs-lookup"><span data-stu-id="0f762-403">**SCSI Parallel Interface** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span data-ttu-id="0f762-404">**Протокол SCSI Fibre Channel** (10)</span><span class="sxs-lookup"><span data-stu-id="0f762-404">**SCSI Fibre Channel Protocol** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span data-ttu-id="0f762-405">**Протокол последовательной шины SCSI** (11)</span><span class="sxs-lookup"><span data-stu-id="0f762-405">**SCSI Serial Bus Protocol** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span data-ttu-id="0f762-406">**Протокол последовательной шины SCSI-2 (1394)** (12)</span><span class="sxs-lookup"><span data-stu-id="0f762-406">**SCSI Serial Bus Protocol-2 (1394)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span data-ttu-id="0f762-407">**Архитектура последовательного хранилища SCSI** (13)</span><span class="sxs-lookup"><span data-stu-id="0f762-407">**SCSI Serial Storage Architecture** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="0f762-408">**VESA** (14)</span><span class="sxs-lookup"><span data-stu-id="0f762-408">**VESA** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="0f762-409">**PCMCIA** (15)</span><span class="sxs-lookup"><span data-stu-id="0f762-409">**PCMCIA** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span data-ttu-id="0f762-410">**Универсальная последовательная шина** (16)</span><span class="sxs-lookup"><span data-stu-id="0f762-410">**Universal Serial Bus** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span data-ttu-id="0f762-411">**Параллельный протокол** (17)</span><span class="sxs-lookup"><span data-stu-id="0f762-411">**Parallel Protocol** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span data-ttu-id="0f762-412">**Ескон** (18)</span><span class="sxs-lookup"><span data-stu-id="0f762-412">**ESCON** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="0f762-413">**Диагностика** (19)</span><span class="sxs-lookup"><span data-stu-id="0f762-413">**Diagnostic** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span data-ttu-id="0f762-414">**I2C** (20)</span><span class="sxs-lookup"><span data-stu-id="0f762-414">**I2C** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="0f762-415">**Мощность** (21)</span><span class="sxs-lookup"><span data-stu-id="0f762-415">**Power** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="0f762-416">**Хиппи** (22)</span><span class="sxs-lookup"><span data-stu-id="0f762-416">**HIPPI** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span data-ttu-id="0f762-417">**Мултибус** (23)</span><span class="sxs-lookup"><span data-stu-id="0f762-417">**MultiBus** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span data-ttu-id="0f762-418">**Вме** (24)</span><span class="sxs-lookup"><span data-stu-id="0f762-418">**VME** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span data-ttu-id="0f762-419">**IPI** (25)</span><span class="sxs-lookup"><span data-stu-id="0f762-419">**IPI** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="0f762-420">**IEEE-488** (26)</span><span class="sxs-lookup"><span data-stu-id="0f762-420">**IEEE-488** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span data-ttu-id="0f762-421">**RS232** (27)</span><span class="sxs-lookup"><span data-stu-id="0f762-421">**RS232** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span data-ttu-id="0f762-422">**IEEE 802,3 10BASE5** (28)</span><span class="sxs-lookup"><span data-stu-id="0f762-422">**IEEE 802.3 10BASE5** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span data-ttu-id="0f762-423">**IEEE 802,3 10BASE2** (29)</span><span class="sxs-lookup"><span data-stu-id="0f762-423">**IEEE 802.3 10BASE2** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span data-ttu-id="0f762-424">**IEEE 802,3 1BASE5** (30)</span><span class="sxs-lookup"><span data-stu-id="0f762-424">**IEEE 802.3 1BASE5** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span data-ttu-id="0f762-425">**IEEE 802,3 10BROAD36** (31)</span><span class="sxs-lookup"><span data-stu-id="0f762-425">**IEEE 802.3 10BROAD36** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span data-ttu-id="0f762-426">**IEEE 802,3 100BASEVG** (32)</span><span class="sxs-lookup"><span data-stu-id="0f762-426">**IEEE 802.3 100BASEVG** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span data-ttu-id="0f762-427">**Маркер IEEE 802,5 Token-Ring** (33)</span><span class="sxs-lookup"><span data-stu-id="0f762-427">**IEEE 802.5 Token-Ring** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span data-ttu-id="0f762-428">**ANSI x3t 9,5 FDDI** (34)</span><span class="sxs-lookup"><span data-stu-id="0f762-428">**ANSI X3T9.5 FDDI** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="0f762-429">**MCA** (35)</span><span class="sxs-lookup"><span data-stu-id="0f762-429">**MCA** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span data-ttu-id="0f762-430">**ESDI** (36)</span><span class="sxs-lookup"><span data-stu-id="0f762-430">**ESDI** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span data-ttu-id="0f762-431">**Интегрированная среда разработки** (37)</span><span class="sxs-lookup"><span data-stu-id="0f762-431">**IDE** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span data-ttu-id="0f762-432">**Cmd** (38)</span><span class="sxs-lookup"><span data-stu-id="0f762-432">**CMD** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span data-ttu-id="0f762-433">**ST506** (39)</span><span class="sxs-lookup"><span data-stu-id="0f762-433">**ST506** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span data-ttu-id="0f762-434">**ДССИ** (40)</span><span class="sxs-lookup"><span data-stu-id="0f762-434">**DSSI** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span data-ttu-id="0f762-435">**QIC2** (41)</span><span class="sxs-lookup"><span data-stu-id="0f762-435">**QIC2** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span data-ttu-id="0f762-436">**Расширенная поддержка ATA/IDE** (42)</span><span class="sxs-lookup"><span data-stu-id="0f762-436">**Enhanced ATA/IDE** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="0f762-437">**AGP** (43)</span><span class="sxs-lookup"><span data-stu-id="0f762-437">**AGP** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span data-ttu-id="0f762-438">**Твирп (двусторонняя ИК-связь)** (44)</span><span class="sxs-lookup"><span data-stu-id="0f762-438">**TWIRP (two-way infrared)** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span data-ttu-id="0f762-439">**FIR (быстрое ИК-соединение)** (45)</span><span class="sxs-lookup"><span data-stu-id="0f762-439">**FIR (fast infrared)** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span data-ttu-id="0f762-440">**Sir (последовательная ИК-связь)** (46)</span><span class="sxs-lookup"><span data-stu-id="0f762-440">**SIR (serial infrared)** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span data-ttu-id="0f762-441">**Ирбус** (47)</span><span class="sxs-lookup"><span data-stu-id="0f762-441">**IrBus** (47)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f762-442">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0f762-442">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-443">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-444">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-445">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="0f762-445">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-446">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0f762-446">Current status of the object.</span></span> <span data-ttu-id="0f762-447">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-447">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0f762-448">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="0f762-448">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0f762-449">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="0f762-449">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0f762-450">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="0f762-450">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0f762-451">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="0f762-451">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f762-452">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0f762-452">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0f762-453">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0f762-453">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0f762-454">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0f762-454">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0f762-455">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="0f762-455">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0f762-456">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="0f762-456">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0f762-457">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="0f762-457">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0f762-458">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="0f762-458">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0f762-459">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="0f762-459">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0f762-460">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="0f762-460">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f762-461">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0f762-461">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-462">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0f762-462">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-463">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-464">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0f762-464">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0f762-465">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0f762-465">State of the logical device.</span></span> <span data-ttu-id="0f762-466">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="0f762-466">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="0f762-467">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-467">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0f762-468">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0f762-468">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0f762-469">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0f762-469">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0f762-470">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="0f762-470">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0f762-471">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="0f762-471">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0f762-472">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="0f762-472">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0f762-473">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="0f762-473">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-474">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-474">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-475">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-476">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f762-476">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f762-477">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="0f762-477">Scoping system's creation class name.</span></span>

<span data-ttu-id="0f762-478">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-478">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-479">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0f762-479">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-480">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0f762-480">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-481">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-481">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f762-482">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0f762-482">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0f762-483">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="0f762-483">Scoping system's name.</span></span>

<span data-ttu-id="0f762-484">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0f762-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f762-485">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="0f762-485">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f762-486">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0f762-486">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0f762-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f762-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0f762-488">Дата и время последнего сброса контроллера, означающее, что контроллер был выключен или повторно инициализирован.</span><span class="sxs-lookup"><span data-stu-id="0f762-488">Date and time this controller was last reset, meaning the controller was powered down or reinitialized.</span></span>

<span data-ttu-id="0f762-489">Это свойство наследуется [**от \_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-489">This property is inherited from [**CIM\_Controller**](cim-controller.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f762-490">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0f762-490">Remarks</span></span>

<span data-ttu-id="0f762-491">Класс **CIM \_ пкмЦиаконтроллер** является производным от [**\_ контроллера CIM**](cim-controller.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-491">The **CIM\_PCMCIAController** class is derived from [**CIM\_Controller**](cim-controller.md).</span></span>

<span data-ttu-id="0f762-492">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0f762-492">WMI does not implement this class.</span></span> <span data-ttu-id="0f762-493">Сведения о классах WMI, которые являются производными от **CIM \_ пкмЦиаконтроллер**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0f762-493">For WMI classes that are derived from **CIM\_PCMCIAController**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0f762-494">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0f762-494">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0f762-495">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0f762-495">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f762-496">Требования</span><span class="sxs-lookup"><span data-stu-id="0f762-496">Requirements</span></span>



| <span data-ttu-id="0f762-497">Требование</span><span class="sxs-lookup"><span data-stu-id="0f762-497">Requirement</span></span> | <span data-ttu-id="0f762-498">Значение</span><span class="sxs-lookup"><span data-stu-id="0f762-498">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f762-499">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f762-499">Minimum supported client</span></span><br/> | <span data-ttu-id="0f762-500">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f762-500">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f762-501">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f762-501">Minimum supported server</span></span><br/> | <span data-ttu-id="0f762-502">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f762-502">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f762-503">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f762-503">Namespace</span></span><br/>                | <span data-ttu-id="0f762-504">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f762-504">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f762-505">MOF</span><span class="sxs-lookup"><span data-stu-id="0f762-505">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f762-506"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f762-506"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f762-507">DLL</span><span class="sxs-lookup"><span data-stu-id="0f762-507">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f762-508"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f762-508"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f762-509">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f762-509">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f762-510">**\_контроллер CIM**</span><span class="sxs-lookup"><span data-stu-id="0f762-510">**cim\_controller**</span></span>](cim-controller.md)
</dt> </dl>

 

