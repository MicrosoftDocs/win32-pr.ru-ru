---
description: Представляет состояние компонента интерфейса гостевой службы, предоставляющего механизм взаимодействия с виртуальной машиной из интерфейсов управления в системе узла.
ms.assetid: 9A158B42-052B-42B3-8539-00927056306D
title: Класс Msvm_GuestServiceInterfaceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent
- Msvm_GuestServiceInterfaceComponent.Availability
- Msvm_GuestServiceInterfaceComponent.Caption
- Msvm_GuestServiceInterfaceComponent.ConfigManagerErrorCode
- Msvm_GuestServiceInterfaceComponent.ConfigManagerUserConfig
- Msvm_GuestServiceInterfaceComponent.CreationClassName
- Msvm_GuestServiceInterfaceComponent.Description
- Msvm_GuestServiceInterfaceComponent.DeviceID
- Msvm_GuestServiceInterfaceComponent.ErrorCleared
- Msvm_GuestServiceInterfaceComponent.ErrorDescription
- Msvm_GuestServiceInterfaceComponent.InstallDate
- Msvm_GuestServiceInterfaceComponent.LastErrorCode
- Msvm_GuestServiceInterfaceComponent.Name
- Msvm_GuestServiceInterfaceComponent.PNPDeviceID
- Msvm_GuestServiceInterfaceComponent.PowerManagementCapabilities
- Msvm_GuestServiceInterfaceComponent.PowerManagementSupported
- Msvm_GuestServiceInterfaceComponent.Status
- Msvm_GuestServiceInterfaceComponent.StatusInfo
- Msvm_GuestServiceInterfaceComponent.SystemCreationClassName
- Msvm_GuestServiceInterfaceComponent.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4c55417edeee6d9a9fb15c474ba4ee9ca2dd93f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682857"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a><span data-ttu-id="93448-103">\_Класс мсвм гуестсервицеинтерфацекомпонент</span><span class="sxs-lookup"><span data-stu-id="93448-103">Msvm\_GuestServiceInterfaceComponent class</span></span>

<span data-ttu-id="93448-104">Представляет состояние компонента интерфейса гостевой службы, предоставляющего механизм взаимодействия с виртуальной машиной из интерфейсов управления в системе узла.</span><span class="sxs-lookup"><span data-stu-id="93448-104">Represents the state of the guest service interface component, which provides a mechanism to interact with the virtual machine from the management interfaces on the host system.</span></span> <span data-ttu-id="93448-105">Этот класс является производным от [**класса \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .</span><span class="sxs-lookup"><span data-stu-id="93448-105">This class derives from the [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) class.</span></span>

<span data-ttu-id="93448-106">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="93448-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93448-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93448-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponent : CIM_LogicalDevice
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

## <a name="members"></a><span data-ttu-id="93448-108">Члены</span><span class="sxs-lookup"><span data-stu-id="93448-108">Members</span></span>

<span data-ttu-id="93448-109">Класс **мсвм \_ гуестсервицеинтерфацекомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93448-109">The **Msvm\_GuestServiceInterfaceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="93448-110">Методы</span><span class="sxs-lookup"><span data-stu-id="93448-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="93448-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="93448-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="93448-112">Методы</span><span class="sxs-lookup"><span data-stu-id="93448-112">Methods</span></span>

<span data-ttu-id="93448-113">Класс **мсвм \_ гуестсервицеинтерфацекомпонент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="93448-113">The **Msvm\_GuestServiceInterfaceComponent** class has these methods.</span></span>



| <span data-ttu-id="93448-114">Метод</span><span class="sxs-lookup"><span data-stu-id="93448-114">Method</span></span>                                                                               | <span data-ttu-id="93448-115">Описание</span><span class="sxs-lookup"><span data-stu-id="93448-115">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93448-116">**Равен**</span><span class="sxs-lookup"><span data-stu-id="93448-116">**RequestStateChange**</span></span>](requeststatechange-msvm-guestserviceinterfacecomponent.md) | <span data-ttu-id="93448-117">Запрашивает изменение состояния компонента интерфейса гостевой службы на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="93448-117">Requests that the state of the guest service interface component be changed to the specified value.</span></span><br/>                           |
| [<span data-ttu-id="93448-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="93448-118">**Reset**</span></span>](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | <span data-ttu-id="93448-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="93448-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="93448-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="93448-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="93448-121">**SetPowerState**</span></span>](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | <span data-ttu-id="93448-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="93448-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="93448-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="93448-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="93448-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="93448-124">Properties</span></span>

<span data-ttu-id="93448-125">Класс **мсвм \_ гуестсервицеинтерфацекомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93448-125">The **Msvm\_GuestServiceInterfaceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93448-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="93448-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93448-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93448-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-129">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-129">Availability and status of the device.</span></span>



| <span data-ttu-id="93448-130">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-130">Value</span></span>                                                                                                                                                                                                                                                                                                              | <span data-ttu-id="93448-131">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-131">Meaning</span></span>                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="93448-132"><dt>**Другие**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-132"><dt>**Other**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="93448-133"><dt>**Неизвестно**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-133"><dt>**Unknown**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <span data-ttu-id="93448-134"><dt>**Запуск/полная мощность**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-134"><dt>**Running/Full Power**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <span data-ttu-id="93448-135"><dt>**Предупреждение**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-135"><dt>**Warning**</dt> <dt>4 (0x4)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="93448-136"><dt>**В тесте**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-136"><dt>**In Test**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="93448-137"><dt>**Неприменимо**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-137"><dt>**Not Applicable**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <span data-ttu-id="93448-138"><dt>**Выключение**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-138"><dt>**Power Off**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <span data-ttu-id="93448-139"><dt>**Выключено в строке**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-139"><dt>**Off Line**</dt> <dt>8 (0x8)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <span data-ttu-id="93448-140"><dt>**За пределами пошлина**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-140"><dt>**Off Duty**</dt> <dt>9 (0x9)</dt></span></span> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="93448-141"><dt>**Пониженная производительность**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-141"><dt>**Degraded**</dt> <dt>10 (0xA)</dt></span></span> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <span data-ttu-id="93448-142"><dt>**Не установлено**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-142"><dt>**Not Installed**</dt> <dt>11 (0xB)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <span data-ttu-id="93448-143"><dt>**Ошибка установки**</dt> <dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-143"><dt>**Install Error**</dt> <dt>12 (0xC)</dt></span></span> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> <span data-ttu-id="93448-144">Энергосбережение <dt>**— неизвестное**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-144"><dt>**Power Save - Unknown**</dt> <dt>13 (0xD)</dt></span></span> </dl>                             | <span data-ttu-id="93448-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="93448-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span><br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> <span data-ttu-id="93448-146">Энергосбережение <dt>**— режим низкого энергопотребления**</dt> <dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-146"><dt>**Power Save - Low Power Mode**</dt> <dt>14 (0xE)</dt></span></span> </dl> | <span data-ttu-id="93448-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="93448-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span><br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <span data-ttu-id="93448-148"><dt>**Power Save — в режиме ожидания**</dt> <dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-148"><dt>**Power Save - Standby**</dt> <dt>15 (0xF)</dt></span></span> </dl>                             | <span data-ttu-id="93448-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="93448-149">The device is not functioning but could be brought to full power quickly.</span></span><br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <span data-ttu-id="93448-150"><dt>**Цикл питания**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-150"><dt>**Power Cycle**</dt> <dt>16 (0x10)</dt></span></span> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> <span data-ttu-id="93448-151">Энергосбережение <dt>**— предупреждение**</dt> <dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-151"><dt>**Power Save - Warning**</dt> <dt>17 (0x11)</dt></span></span> </dl>                            | <span data-ttu-id="93448-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="93448-152">The device is in a warning state, though also in a power save mode.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="93448-153">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="93448-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-156">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93448-156">Short textual description of the object.</span></span> <span data-ttu-id="93448-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93448-157">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93448-158">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="93448-158">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93448-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93448-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-161">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="93448-161">Win32 Configuration Manager error code.</span></span>



| <span data-ttu-id="93448-162">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-162">Value</span></span>                                                                                | <span data-ttu-id="93448-163">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-163">Meaning</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93448-164"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-164"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="93448-165">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="93448-165">Device is working properly.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="93448-166"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-166"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="93448-167">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="93448-167">Device is not configured correctly.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="93448-168"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-168"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="93448-169">Windows не удается загрузить драйвер для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-169">Windows cannot load the driver for this device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="93448-170"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-170"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="93448-171">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93448-171">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span><br/>                             |
| <dl> <span data-ttu-id="93448-172"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-172"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="93448-173">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="93448-173">Device is not working properly.</span></span> <span data-ttu-id="93448-174">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="93448-174">One of its drivers or the registry might be corrupted.</span></span><br/>                                        |
| <dl> <span data-ttu-id="93448-175"><dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-175"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="93448-176">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="93448-176">Driver for the device requires a resource that Windows cannot manage.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="93448-177"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-177"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="93448-178">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="93448-178">Boot configuration for the device conflicts with other devices.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="93448-179"><dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-179"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="93448-180">Не удается выполнить фильтрацию.</span><span class="sxs-lookup"><span data-stu-id="93448-180">Cannot filter.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="93448-181"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-181"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="93448-182">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-182">Driver loader for the device is missing.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="93448-183"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-183"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="93448-184">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-184">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span><br/>               |
| <dl> <span data-ttu-id="93448-185"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-185"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="93448-186">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="93448-186">Device cannot start.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="93448-187"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-187"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="93448-188">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-188">Device failed.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="93448-189"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-189"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="93448-190">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="93448-190">Device cannot find enough free resources to use.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="93448-191"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-191"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="93448-192">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-192">Windows cannot verify the device's resources.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="93448-193"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-193"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="93448-194">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="93448-194">Device cannot work properly until the computer is restarted.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="93448-195"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-195"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="93448-196">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="93448-196">Device is not working properly due to a possible re-enumeration problem.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="93448-197"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-197"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="93448-198">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="93448-198">Windows cannot identify all of the resources that the device uses.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="93448-199"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-199"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="93448-200">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="93448-200">Device is requesting an unknown resource type.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="93448-201"><dt>18 (0x12)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-201"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="93448-202">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="93448-202">Device drivers must be reinstalled.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="93448-203"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-203"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="93448-204">Сбой при использовании загрузчика VxD.</span><span class="sxs-lookup"><span data-stu-id="93448-204">Failure using the VxD loader.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="93448-205"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-205"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="93448-206">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="93448-206">Registry might be corrupted.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="93448-207"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-207"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="93448-208">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="93448-208">System failure.</span></span> <span data-ttu-id="93448-209">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="93448-209">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="93448-210">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="93448-210">Windows is removing the device.</span></span><br/> |
| <dl> <span data-ttu-id="93448-211"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-211"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="93448-212">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="93448-212">Device is disabled.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="93448-213"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-213"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="93448-214">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="93448-214">System failure.</span></span> <span data-ttu-id="93448-215">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="93448-215">If changing the device driver is ineffective, see the hardware documentation.</span></span><br/>                                 |
| <dl> <span data-ttu-id="93448-216"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-216"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="93448-217">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="93448-217">Device is not present, not working properly, or does not have all of its drivers installed.</span></span><br/>                                   |
| <dl> <span data-ttu-id="93448-218"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-218"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="93448-219">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="93448-219">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="93448-220"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-220"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="93448-221">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="93448-221">Windows is still setting up the device.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="93448-222"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-222"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="93448-223">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="93448-223">Device does not have valid log configuration.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="93448-224"><dt>28 (0x1C)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-224"><dt>28 (0x1C)</dt></span></span> </dl> | <span data-ttu-id="93448-225">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="93448-225">Device drivers are not installed.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="93448-226"><dt>29 (0x1D)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-226"><dt>29 (0x1D)</dt></span></span> </dl> | <span data-ttu-id="93448-227">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="93448-227">Device is disabled; the device firmware did not provide the required resources.</span></span><br/>                                               |
| <dl> <span data-ttu-id="93448-228"><dt>30 (0x1E)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-228"><dt>30 (0x1E)</dt></span></span> </dl> | <span data-ttu-id="93448-229">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="93448-229">Device is using an IRQ resource that another device is using.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="93448-230"><dt>31 (0x1F)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-230"><dt>31 (0x1F)</dt></span></span> </dl> | <span data-ttu-id="93448-231">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="93448-231">Device is not working properly; Windows cannot load the required device drivers.</span></span><br/>                                              |



 

</dd> <dt>

<span data-ttu-id="93448-232">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="93448-232">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-233">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="93448-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93448-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-235">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="93448-235">If **TRUE**, the device is using a user-defined configuration.</span></span>

</dd> <dt>

<span data-ttu-id="93448-236">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="93448-236">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-239">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="93448-239">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="93448-240">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="93448-240">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="93448-241">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93448-241">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-244">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93448-244">Textual description of the object.</span></span> <span data-ttu-id="93448-245">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93448-245">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93448-246">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="93448-246">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-249">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-249">Address or other identifying information to uniquely name the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="93448-250">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="93448-250">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-251">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="93448-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93448-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-253">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="93448-253">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

</dd> <dt>

<span data-ttu-id="93448-254">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="93448-254">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-257">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="93448-257">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

</dd> <dt>

<span data-ttu-id="93448-258">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="93448-258">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-259">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93448-259">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93448-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-261">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="93448-261">Date and time the object was installed.</span></span> <span data-ttu-id="93448-262">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="93448-262">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="93448-263">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93448-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93448-264">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="93448-264">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-265">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="93448-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="93448-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-267">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="93448-267">Last error code reported by the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="93448-268">**Name**</span><span class="sxs-lookup"><span data-stu-id="93448-268">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-269">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-270">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-271">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="93448-271">Label by which the object is known.</span></span> <span data-ttu-id="93448-272">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="93448-272">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="93448-273">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93448-273">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="93448-274">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="93448-274">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-277">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-277">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="93448-278">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="93448-278">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="93448-279">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="93448-279">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-280">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="93448-280">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="93448-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-282">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="93448-282">Array of the specific power-related capabilities of a logical device.</span></span> <span data-ttu-id="93448-283">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="93448-283">This property is inherited from **CIM\_LogicalDevice**.</span></span>



| <span data-ttu-id="93448-284">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-284">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="93448-285">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-285">Meaning</span></span>                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="93448-286"><dt>**Неизвестный**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-286"><dt>**Unknown**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="93448-287"><dt>**Не поддерживается**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-287"><dt>**Not Supported**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="93448-288"><dt>**Отключено**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-288"><dt>**Disabled**</dt> <dt>2 (0x2)</dt></span></span> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="93448-289"><dt>**Включено**</dt> <dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-289"><dt>**Enabled**</dt> <dt>3 (0x3)</dt></span></span> </dl>                                                                                                                                     | <span data-ttu-id="93448-290">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="93448-290">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span><br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <span data-ttu-id="93448-291"><dt>**Режимы энергосбережения, указанные автоматически**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-291"><dt>**Power Saving Modes Entered Automatically**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="93448-292">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="93448-292">The device can change its power state based on usage or other criteria.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <span data-ttu-id="93448-293"><dt>**Состояние питания, устанавливаемое**</dt> <dt>5 (0x5)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-293"><dt>**Power State Settable**</dt> <dt>5 (0x5)</dt></span></span> </dl>                                                                                 | <span data-ttu-id="93448-294">Поддерживается метод [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) .</span><span class="sxs-lookup"><span data-stu-id="93448-294">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method is supported.</span></span> <span data-ttu-id="93448-295">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="93448-295">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="93448-296">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="93448-296">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span><br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <span data-ttu-id="93448-297"><dt>**Поддержка выключения питания**</dt> <dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-297"><dt>**Power Cycling Supported**</dt> <dt>6 (0x6)</dt></span></span> </dl>                                                                     | <span data-ttu-id="93448-298">Метод [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="93448-298">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span><br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <span data-ttu-id="93448-299"><dt>**Поддержка по времени, поддерживаемая**</dt> <dt>7 (0x7)</dt></span><span class="sxs-lookup"><span data-stu-id="93448-299"><dt>**Timed Power On Supported**</dt> <dt>7 (0x7)</dt></span></span> </dl>                                                                 | <span data-ttu-id="93448-300">Метод [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) может быть вызван с параметром *PowerState*, установленным в значение 5 ("цикл электропитания") и *временем* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="93448-300">The [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and *Time* set to a specific date and time, or interval, for power-on.</span></span><br/>                                                                                       |



 

</dd> <dt>

<span data-ttu-id="93448-301">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="93448-301">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-302">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="93448-302">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93448-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-304">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="93448-304">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="93448-305">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="93448-305">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="93448-306">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="93448-306">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="93448-307">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="93448-307">For more information, see the **PowerManagementCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="93448-308">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="93448-308">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-311">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="93448-311">Current status of the object.</span></span> <span data-ttu-id="93448-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="93448-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="93448-313">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="93448-313">Values include the following:</span></span>

<dl><span id="OK"></span><span id="ok"></span><dt>

<span data-ttu-id="93448-314">**'**</span><span class="sxs-lookup"><span data-stu-id="93448-314">**"OK"**</span></span>
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

<span data-ttu-id="93448-315">**План**</span><span class="sxs-lookup"><span data-stu-id="93448-315">**"Error"**</span></span>
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

<span data-ttu-id="93448-316">**Пониженной функциональности**</span><span class="sxs-lookup"><span data-stu-id="93448-316">**"Degraded"**</span></span>
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

<span data-ttu-id="93448-317">**Неизвестный**</span><span class="sxs-lookup"><span data-stu-id="93448-317">**"Unknown"**</span></span>
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

<span data-ttu-id="93448-318">**"Пред Fail"**</span><span class="sxs-lookup"><span data-stu-id="93448-318">**"Pred Fail"**</span></span>
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

<span data-ttu-id="93448-319">**Start**</span><span class="sxs-lookup"><span data-stu-id="93448-319">**"Starting"**</span></span>
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

<span data-ttu-id="93448-320">**Идет**</span><span class="sxs-lookup"><span data-stu-id="93448-320">**"Stopping"**</span></span>
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

<span data-ttu-id="93448-321">**Служеб**</span><span class="sxs-lookup"><span data-stu-id="93448-321">**"Service"**</span></span>
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

<span data-ttu-id="93448-322">**Груз**</span><span class="sxs-lookup"><span data-stu-id="93448-322">**"Stressed"**</span></span>
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

<span data-ttu-id="93448-323">**"Recover"**</span><span class="sxs-lookup"><span data-stu-id="93448-323">**"NonRecover"**</span></span>
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

<span data-ttu-id="93448-324">**"Нет контакта"**</span><span class="sxs-lookup"><span data-stu-id="93448-324">**"No Contact"**</span></span>
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

<span data-ttu-id="93448-325">**"Потеря связи"**</span><span class="sxs-lookup"><span data-stu-id="93448-325">**"Lost Comm"**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93448-326">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="93448-326">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-327">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93448-327">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93448-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-329">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="93448-329">State of the logical device.</span></span> <span data-ttu-id="93448-330">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="93448-330">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span> <span data-ttu-id="93448-331">Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="93448-331">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

<dl> <dt>

<span data-ttu-id="93448-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="93448-332"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1 (0x1))</span></span>
</dt> <dt>

<span data-ttu-id="93448-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="93448-333"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2 (0x2))</span></span>
</dt> <dt>

<span data-ttu-id="93448-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="93448-334"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3 (0x3))</span></span>
</dt> <dt>

<span data-ttu-id="93448-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="93448-335"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (4 (0x4))</span></span>
</dt> <dt>

<span data-ttu-id="93448-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="93448-336"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (5 (0x5))</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="93448-337">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="93448-337">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-340">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="93448-340">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="93448-341">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="93448-341">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93448-342">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93448-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93448-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93448-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93448-344">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="93448-344">Scoping system's name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93448-345">Требования</span><span class="sxs-lookup"><span data-stu-id="93448-345">Requirements</span></span>



| <span data-ttu-id="93448-346">Требование</span><span class="sxs-lookup"><span data-stu-id="93448-346">Requirement</span></span> | <span data-ttu-id="93448-347">Значение</span><span class="sxs-lookup"><span data-stu-id="93448-347">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93448-348">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93448-348">Minimum supported client</span></span><br/> | <span data-ttu-id="93448-349">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="93448-349">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="93448-350">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93448-350">Minimum supported server</span></span><br/> | <span data-ttu-id="93448-351">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="93448-351">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93448-352">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93448-352">Namespace</span></span><br/>                | <span data-ttu-id="93448-353">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="93448-353">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93448-354">MOF</span><span class="sxs-lookup"><span data-stu-id="93448-354">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93448-355"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93448-355"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93448-356">DLL</span><span class="sxs-lookup"><span data-stu-id="93448-356">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93448-357"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93448-357"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93448-358">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93448-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93448-359">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="93448-359">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dt>

[<span data-ttu-id="93448-360">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="93448-360">**CIM\_LogicalDevice**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

