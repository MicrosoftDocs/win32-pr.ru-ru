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
ms.openlocfilehash: c7e404a1195332b508de22fc0a26dfebb96eba29f487f08505987edcc72b6cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523024"
---
# <a name="msvm_guestserviceinterfacecomponent-class"></a>\_Класс мсвм гуестсервицеинтерфацекомпонент

Представляет состояние компонента интерфейса гостевой службы, предоставляющего механизм взаимодействия с виртуальной машиной из интерфейсов управления в системе узла. Этот класс является производным от [**класса \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) .

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **мсвм \_ гуестсервицеинтерфацекомпонент** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ гуестсервицеинтерфацекомпонент** содержит следующие методы.



| Метод                                                                               | Описание                                                                                                                              |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Равен**](requeststatechange-msvm-guestserviceinterfacecomponent.md) | Запрашивает изменение состояния компонента интерфейса гостевой службы на указанное значение.<br/>                           |
| [**Перезапуск**](/windows/desktop/CIMWin32Prov/reset-method-in-class-cim-logicaldevice)                        | Запрашивает сброс логического устройства. Не реализовано инструментарием WMI.<br/>                                                               |
| [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-logicaldevice)        | Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние. Не реализовано инструментарием WMI.<br/> |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ гуестсервицеинтерфацекомпонент** имеет следующие свойства.

<dl> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Доступность и состояние устройства.



| Значение                                                                                                                                                                                                                                                                                                              | Значение                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Другие**</dt> <dt>1 (0x1)</dt> </dl>                                                                                          |                                                                                                             |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Неизвестно**</dt> <dt>2 (0x2)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span><dl> <dt>**Запуск/полная мощность**</dt> <dt>3 (0x3)</dt> </dl>                                      |                                                                                                             |
| <span id="Warning"></span><span id="warning"></span><span id="WARNING"></span><dl> <dt>**Предупреждение**</dt> <dt>4 (0x4)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <dt>**В тесте**</dt> <dt>5 (0x5)</dt> </dl>                                                                                  |                                                                                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**Неприменимо**</dt> <dt>6 (0x6)</dt> </dl>                                                      |                                                                                                             |
| <span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span><dl> <dt>**Выключение**</dt> <dt>7 (0x7)</dt> </dl>                                                                          |                                                                                                             |
| <span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span><dl> <dt>**Выключено в строке**</dt> <dt>8 (0x8)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span><dl> <dt>**За пределами пошлина**</dt> <dt>9 (0x9)</dt> </dl>                                                                              |                                                                                                             |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <dt>**Пониженная производительность**</dt> <dt>10 (0xA)</dt> </dl>                                                                             |                                                                                                             |
| <span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span><dl> <dt>**Не установлено**</dt> <dt>11 (0xB)</dt> </dl>                                                         |                                                                                                             |
| <span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span><dl> <dt>**Ошибка установки**</dt> <dt>12 (0xC)</dt> </dl>                                                         |                                                                                                             |
| <span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span><dl> Энергосбережение <dt>**— неизвестное**</dt> <dt>13 (0xD)</dt> </dl>                             | Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.<br/>                 |
| <span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span><dl> Энергосбережение <dt>**— режим низкого энергопотребления**</dt> <dt>14 (0xE)</dt> </dl> | Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.<br/> |
| <span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span><dl> <dt>**Power Save — в режиме ожидания**</dt> <dt>15 (0xF)</dt> </dl>                             | Устройство не работает, но его можно быстро включить в полную работу.<br/>                        |
| <span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span><dl> <dt>**Цикл питания**</dt> <dt>16 (0x10)</dt> </dl>                                                                |                                                                                                             |
| <span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span><dl> Энергосбережение <dt>**— предупреждение**</dt> <dt>17 (0x11)</dt> </dl>                            | Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.<br/>                              |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое текстовое описание объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**конфигманажерерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код ошибки Win32 Configuration Manager.



| Значение                                                                                | Значение                                                                                                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Устройство работает правильно.<br/>                                                                                                   |
| <dl> <dt>1 (0x1)</dt> </dl>   | Устройство настроено неправильно.<br/>                                                                                           |
| <dl> <dt>2 (0x2)</dt> </dl>   | Windows не удается загрузить драйвер для этого устройства.<br/>                                                                               |
| <dl> <dt>3 (0x3)</dt> </dl>   | Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.<br/>                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | Устройство работает неправильно. Один из драйверов или реестр может быть поврежден.<br/>                                        |
| <dl> <dt>5 (0x5)</dt> </dl>   | драйверу для устройства требуется ресурс, который Windows не может управляться.<br/>                                                         |
| <dl> <dt>6 (0x6)</dt> </dl>   | Конфигурация загрузки для устройства конфликтует с другими устройствами.<br/>                                                               |
| <dl> <dt>7 (0x7)</dt> </dl>   | Не удается выполнить фильтрацию.<br/>                                                                                                                |
| <dl> <dt>8 (0x8)</dt> </dl>   | Отсутствует загрузчик драйверов для устройства.<br/>                                                                                      |
| <dl> <dt>9 (0x9)</dt> </dl>   | Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.<br/>               |
| <dl> <dt>10 (0xA)</dt> </dl>  | Не удается запустить устройство.<br/>                                                                                                          |
| <dl> <dt>11 (0xB)</dt> </dl>  | Сбой устройства.<br/>                                                                                                                |
| <dl> <dt>12 (0xC)</dt> </dl>  | Устройству не удается найти достаточно свободных ресурсов для использования.<br/>                                                                              |
| <dl> <dt>13 (0xD)</dt> </dl>  | Windows не может проверить ресурсы устройства.<br/>                                                                                 |
| <dl> <dt>14 (0xE)</dt> </dl>  | Устройство не может работать должным образом, пока компьютер не будет перезагружен.<br/>                                                                  |
| <dl> <dt>15 (0xF)</dt> </dl>  | Устройство не работает должным образом из-за возможной проблемы повторного перечисления.<br/>                                                      |
| <dl> <dt>16 (0x10)</dt> </dl> | Windows не удается найти все ресурсы, используемые устройством.<br/>                                                            |
| <dl> <dt>17 (0x11)</dt> </dl> | Устройство запрашивает неизвестный тип ресурса.<br/>                                                                                |
| <dl> <dt>18 (0x12)</dt> </dl> | Необходимо переустановить драйверы устройств.<br/>                                                                                           |
| <dl> <dt>19 (0x13)</dt> </dl> | Сбой при использовании загрузчика VxD.<br/>                                                                                                 |
| <dl> <dt>20 (0x14)</dt> </dl> | Реестр может быть поврежден.<br/>                                                                                                  |
| <dl> <dt>21 (0x15)</dt> </dl> | Сбой системы. Если изменение драйвера устройства неэффективно, см. документацию по оборудованию. Windows удаляет устройство.<br/> |
| <dl> <dt>22 (0x16)</dt> </dl> | Устройство отключено.<br/>                                                                                                           |
| <dl> <dt>23 (0x17)</dt> </dl> | Сбой системы. Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.<br/>                                 |
| <dl> <dt>24 (0x18)</dt> </dl> | Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.<br/>                                   |
| <dl> <dt>25 (0x19)</dt> </dl> | Windows все еще настраивает устройство.<br/>                                                                                       |
| <dl> <dt>26 (0x1A)</dt> </dl> | Windows все еще настраивает устройство.<br/>                                                                                       |
| <dl> <dt>27 (0x1B)</dt> </dl> | Устройство не имеет допустимой конфигурации журнала.<br/>                                                                                 |
| <dl> <dt>28 (0x1C)</dt> </dl> | Драйверы устройств не установлены.<br/>                                                                                             |
| <dl> <dt>29 (0x1D)</dt> </dl> | Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.<br/>                                               |
| <dl> <dt>30 (0x1E)</dt> </dl> | Устройство использует ресурс IRQ, который используется другим устройством.<br/>                                                                 |
| <dl> <dt>31 (0x1F)</dt> </dl> | Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.<br/>                                              |



 

</dd> <dt>

**конфигманажерусерконфиг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, устройство использует определяемую пользователем конфигурацию.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текстовое описание объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес или другие идентифицирующие сведения для уникального имени логического устройства.

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ластерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Код последней ошибки, сообщаемый логическим устройством.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.

Пример: " \* PNP030b"

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив конкретных возможностей логического устройства, связанных с питанием. Это свойство наследуется **от \_ CIM**-унаследованной модели.



| Значение                                                                                                                                                                                                                                                                                                                                                                 | Значение                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Неизвестный**</dt> <dt>0 (0x0)</dt> </dl>                                                                                                                                     |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Не поддерживается**</dt> <dt>1 (0x1)</dt> </dl>                                                                                                             |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Отключено**</dt> <dt>2 (0x2)</dt> </dl>                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                      |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Включено**</dt> <dt>3 (0x3)</dt> </dl>                                                                                                                                     | Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.<br/>                                                                                                                                                                                               |
| <span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span><dl> <dt>**Режимы энергосбережения, указанные автоматически**</dt> <dt>4 (0x4)</dt> </dl> | Устройство может изменить свое состояние электропитания на основе использования или других критериев.<br/>                                                                                                                                                                                                                                                   |
| <span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span><dl> <dt>**Состояние питания, устанавливаемое**</dt> <dt>5 (0x5)</dt> </dl>                                                                                 | Поддерживается метод [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) . Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).<br/> |
| <span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span><dl> <dt>**Поддержка выключения питания**</dt> <dt>6 (0x6)</dt> </dl>                                                                     | Метод [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").<br/>                                                                                                                                                            |
| <span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span><dl> <dt>**Поддержка по времени, поддерживаемая**</dt> <dt>7 (0x7)</dt> </dl>                                                                 | Метод [**SetPowerState**](/windows/desktop/CIMWin32Prov/setpowerstate-method-in-class-cim-controller) может быть вызван с параметром *PowerState*, установленным в значение 5 ("цикл электропитания") и *временем* , установленным на определенную дату и время (или интервал) для включения питания.<br/>                                                                                       |



 

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения. Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .

Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются. Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

В эти значения входят:

<dl><span id="OK"></span><span id="ok"></span><dt>

**'**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**План**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**Пониженной функциональности**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**Неизвестный**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**"Пред Fail"**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**Start**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**Идет**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**Служеб**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**Груз**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"Recover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**"Нет контакта"**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**"Потеря связи"**
</dt> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Состояние логического устройства. Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо"). Это свойство наследуется [**от \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)-унаследованной модели.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1 (0x1))
</dt> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2 (0x2))
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3 (0x3))
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (4 (0x4))
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (5 (0x5))
</dt> </dl>

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя класса создания системы области.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя системы области.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> <dt>

[**Модель \_ CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)
</dt> </dl>

 

