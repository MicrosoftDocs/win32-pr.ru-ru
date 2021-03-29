---
description: Абстракция или Эмуляция аппаратной сущности, которая может быть не основана на физическом оборудовании.
ms.assetid: e31c82ed-2da2-4a18-a55e-16931d74f243
title: Класс CIM_LogicalDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice
- CIM_LogicalDevice.SystemCreationClassName
- CIM_LogicalDevice.SystemName
- CIM_LogicalDevice.CreationClassName
- CIM_LogicalDevice.DeviceID
- CIM_LogicalDevice.PowerManagementSupported
- CIM_LogicalDevice.PowerManagementCapabilities
- CIM_LogicalDevice.Availability
- CIM_LogicalDevice.StatusInfo
- CIM_LogicalDevice.LastErrorCode
- CIM_LogicalDevice.ErrorDescription
- CIM_LogicalDevice.ErrorCleared
- CIM_LogicalDevice.OtherIdentifyingInfo
- CIM_LogicalDevice.PowerOnHours
- CIM_LogicalDevice.TotalPowerOnHours
- CIM_LogicalDevice.IdentifyingDescriptions
- CIM_LogicalDevice.AdditionalAvailability
- CIM_LogicalDevice.MaxQuiesceTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 471b10f8d3c8640cfcc4277d0151bdd46d59db86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808392"
---
# <a name="cim_logicaldevice-class-hyper-v-management"></a>Класс CIM_LogicalDevice (Управление Hyper-V)

Абстракция или Эмуляция аппаратной сущности, которая может быть не основана на физическом оборудовании.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Core::Device"), AMENDMENT]
class CIM_LogicalDevice : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  DeviceID;
  boolean PowerManagementSupported;
  uint16  PowerManagementCapabilities[];
  uint16  Availability;
  uint16  StatusInfo;
  uint32  LastErrorCode;
  string  ErrorDescription;
  boolean ErrorCleared;
  string  OtherIdentifyingInfo[];
  uint64  PowerOnHours;
  uint64  TotalPowerOnHours;
  string  IdentifyingDescriptions[];
  uint16  AdditionalAvailability[];
  uint64  MaxQuiesceTime;
};
```

## <a name="members"></a>Члены

Класс **класса \_ CIM** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **класса \_ CIM** имеет следующие методы.



| Метод                                                           | Описание                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**енабледевице**](cim-logicaldevice-enabledevice.md)           | Этот метод является устаревшим. Вместо этого используйте метод **RequestStateChange** .<br/> **Нерекомендуемое описание:** Включает или отключает логическое устройство.<br/>                                                                     |
| [**онлинедевице**](cim-logicaldevice-onlinedevice.md)           | Этот метод является устаревшим. Вместо этого используйте метод **RequestStateChange** .<br/> **Нерекомендуемое описание:** Переводит логическое устройство в режим «в сети», чтобы он мог принимать запросы или в режиме «вне сети», чтобы он больше не мог принимать запросы.<br/> |
| [**куиесцедевице**](cim-logicaldevice-quiescedevice.md)         | Этот метод является устаревшим. Вместо этого используйте метод **RequestStateChange** .<br/> **Нерекомендуемое описание:** Временно приостанавливает действие на логическом устройстве или повторно включает действие.<br/>                            |
| [**Перезапуск**](cim-logicaldevice-reset.md)                         | Сбрасывает логическое устройство.<br/>                                                                                                                                                                                                    |
| [**ресторепропертиес**](cim-logicaldevice-restoreproperties.md) | Восстанавливает предыдущую конфигурацию и состояние логического устройства.<br/>                                                                                                                                                            |
| [**савепропертиес**](cim-logicaldevice-saveproperties.md)       | Сохраняет конфигурацию и состояние логического устройства.<br/>                                                                                                                                                                      |
| [**SetPowerState**](cim-logicaldevice-setpowerstate.md)         | Этот метод является устаревшим. Вместо этого используйте свойство **SetPowerState** класса **CIM \_ поверманажементсервице** .<br/> **Нерекомендуемое описание:** Задает состояние электропитания логического устройства.<br/>                       |



 

### <a name="properties"></a>Свойства

Класс **класса \_ CIM** имеет следующие свойства.

<dl> <dt>

**аддитионалаваилабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ -модель**".**Доступность**)
</dt> </dl>

Массив, содержащий сведения о доступности логического устройства в дополнение к свойству **доступности** .

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Работа/полная мощность** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**В тесте** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Выключение питания** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

Не в **линии** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

Не **обслуживает** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Снижение работоспособности** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Не установлено** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Ошибка установки** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

Энергосбережение **— неизвестно** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

Энергосбережение **— режим низкого энергопотребления** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

Энергосбережение **— ждущий режим** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Цикл электропитания** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

Энергосбережение **— предупреждение** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Приостановлено** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Не готово** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Не настроено** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**Заморожено** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**Доступность**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 006,5 "," MIB. В файле IETF \| Host-Resources-MIB. хрдевицестатус "," MIF. DMTF \| Host Device \| 001,5 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_**-оборудование ".**Аддитионалаваилабилити**")
</dt> </dl>

Содержит сведения о доступности логического устройства.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

**Работа/полная мощность** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

**В тесте** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Выключение питания** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

Не в **линии** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

Не **обслуживает** (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Снижение работоспособности** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

**Не установлено** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

**Ошибка установки** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

Энергосбережение **— неизвестно** (13)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

Энергосбережение **— режим низкого энергопотребления** (14)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

Энергосбережение **— ждущий режим** (15)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Цикл электропитания** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

Энергосбережение **— предупреждение** (17)


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Приостановлено** (18)


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

**Не готово** (19)


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

**Не настроено** (20)


</dt> <dd></dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

**Заморожено** (21)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя класса, используемое для создания экземпляра логического устройства. **Свойство CreationClassName** объединяется с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Уникальный идентификатор логического устройства, например адрес.

</dd> <dt>

**еррорклеаред**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте свойство **OperationalStatus** из класса **CIM \_ манажедсистемелемент** .

**Нерекомендуемое описание:** Указывает, удаляется ли ошибка, сообщаемая свойством **ластерроркоде** .

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ девицееррордата. ErrorDescription")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте свойство **ErrorDescription** класса **CIM \_ девицееррордата** .

**Нерекомендуемое описание:** Дополнительные сведения об ошибке, о которых сообщает свойство **ластерроркоде** .

</dd> <dt>

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ -модель**".**Осеридентифингинфо**")
</dt> </dl>

Массив строк, описывающих элементы массива **осеридентифингинфо** одного индекса.

</dd> <dt>

**ластерроркоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ девицееррордата. ластерроркоде")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого мы используем свойство **ластерроркоде** из класса **CIM \_ девицееррордата** .

**Нерекомендуемое описание:** Последний код ошибки, сообщаемый логическим устройством.

</dd> <dt>

**макскуиесцетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунд")
</dt> </dl>

Это свойство является устаревшим и не должно использоваться.

**Нерекомендуемое описание:** Максимальное время в миллисекундах, в течение которого устройство может оставаться в временно отключенном состоянии (свойства **доступности** и **аддитионалаваилабилити** задано как "21" загружена). Значение "0" указывает, что логическое устройство может оставаться в временно отключенном состоянии в течение неограниченного времени.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ -модель**".**Идентифингдескриптионс**")
</dt> </dl>

Сведения, идентифицирующие логическое устройство, отличное от **DeviceID**.

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ поверманажементкапабилитиес. поверкапабилитиес")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте класс **CIM \_ поверманажементкапабилитиес** .

**Нерекомендуемое описание:** Массив, содержащий возможности управления питанием устройства.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Не поддерживается** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Режимы энергосбережения** записываются автоматически (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Настраиваемое состояние питания** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Поддержка циклов электропитания** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Поддерживается время включения** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ поверманажементкапабилитиес")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте класс **поверманажементкапабилитиес** .

**Нерекомендуемое описание: true** , если логическое устройство может управляться питанием; в противном случае — **значение false**.

</dd> <dt>

**поверонхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Часы"), **Счетчик**
</dt> </dl>

Число последовательных часов, на которое было включено логическое устройство, с момента его последнего цикла питания.

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("[**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md).**EnabledState**"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Рабочее состояние DMTF \| 006,4 ")
</dt> </dl>

Это свойство использовать не рекомендуется. Вместо этого используйте класс **CIM \_ поверманажементкапабилитиес** .

**Нерекомендуемое описание:** Указывает, включено ли логическое устройство или находится в связанном состоянии.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Неприменимо** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Имя класса, используемое для создания экземпляра системы, содержащей логическое устройство. **Системкреатионкласснаме** сочетается с другими ключевыми свойствами этого класса, чтобы уникальным образом идентифицировать экземпляры этого класса и его подклассов.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**")
</dt> </dl>

Имя системы, содержащей логическое устройство.

</dd> <dt>

**тоталповеронхаурс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("Часы"), **Счетчик**
</dt> </dl>

Общее число часов, в течение которых логическое устройство было включено.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 

