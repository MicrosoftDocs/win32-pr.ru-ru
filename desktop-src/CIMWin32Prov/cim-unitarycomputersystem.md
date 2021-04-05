---
description: Класс CIM \_ унитарикомпутерсистем представляет Настольный, мобильный, сетевой компьютер, сервер или другой тип одноузловой системы с одним узлом.
ms.assetid: c696050d-c921-4056-adc7-e4a2e9f4e119
ms.tgt_platform: multiple
title: Класс CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem
- CIM_UnitaryComputerSystem.Caption
- CIM_UnitaryComputerSystem.CreationClassName
- CIM_UnitaryComputerSystem.Description
- CIM_UnitaryComputerSystem.InitialLoadInfo
- CIM_UnitaryComputerSystem.InstallDate
- CIM_UnitaryComputerSystem.LastLoadInfo
- CIM_UnitaryComputerSystem.Name
- CIM_UnitaryComputerSystem.NameFormat
- CIM_UnitaryComputerSystem.PowerManagementCapabilities
- CIM_UnitaryComputerSystem.PowerManagementSupported
- CIM_UnitaryComputerSystem.PowerState
- CIM_UnitaryComputerSystem.PrimaryOwnerContact
- CIM_UnitaryComputerSystem.PrimaryOwnerName
- CIM_UnitaryComputerSystem.ResetCapability
- CIM_UnitaryComputerSystem.Roles
- CIM_UnitaryComputerSystem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e14812fda7971ffe045e8e36752c983cf5350402
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990429"
---
# <a name="cim_unitarycomputersystem-class"></a>\_Класс CIM унитарикомпутерсистем

Класс **CIM \_ унитарикомпутерсистем** представляет Настольный, мобильный, сетевой компьютер, сервер или другой тип одноузловой системы с одним узлом.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8502C526-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_UnitaryComputerSystem : CIM_ComputerSystem
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  string   InitialLoadInfo[];
  datetime InstallDate;
  string   LastLoadInfo;
  string   Name;
  string   NameFormat;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  string   Roles[];
  string   Status;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ унитарикомпутерсистем** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **CIM \_ унитарикомпутерсистем** содержит следующие методы.



| Метод                                                                           | Описание                                                                                                                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**SetPowerState**](setpowerstate-method-in-class-cim-unitarycomputersystem.md) | Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние. Не реализовано инструментарием WMI.<br/> |



 

### <a name="properties"></a>Свойства

Класс **CIM \_ унитарикомпутерсистем** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")
</dt> </dl>

Текстовое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**инитиаллоадинфо**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Данные, необходимые для нахождения устройства начальной загрузки (его ключа) или службы загрузки для запроса запуска операционной системы. Кроме того, можно указать параметры загрузки (то есть путь и параметры).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ластлоадинфо**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Данные, определяющие устройство начальной загрузки (его ключ) или службу загрузки, которая запросила последнюю загрузку операционной системы. Кроме того, можно указать параметры загрузки (то есть путь и параметры).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) и его производные — это объекты верхнего уровня CIM, которые предоставляют область для многочисленных компонентов и нуждаются в уникальных [**\_ системных**](cim-system.md) ключах CIM. Эвристическая эвристика определяется для создания имени **CIM \_ ComputerSystem** в попытке всегда создавать то же системное имя независимо от протокола обнаружения. Это предотвращает проблемы с инвентаризацией и управлением, когда один и тот же ресурс или сущность обнаруживаются несколько раз, но не может быть разрешена в один объект. Это свойство определяет, как системное имя было создано с помощью эвристики подклассов. Эвристический подход описан в спецификации общей модели CIM V2 и предполагает, что документированные правила обходятся для определения и назначения имени. Список значений **намеформат** определяет порядок приоритета для назначения системного имени с помощью нескольких правил, сопоставленных с одним и тем же значением. Обратите внимание, что имя системы **CIM \_** , вычисляемое с помощью эвристического алгоритма, является значением ключа в системе. Другие имена могут назначаться и использоваться для **CIM- \_ ComputerSystem** , которые лучше подходят для бизнеса, используя псевдонимы.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

В эти значения входят:

<dt>

<span id="IP"></span><span id="ip"></span>

**IP-адрес** ("IP")


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Набрать номер** ("набрать")


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** (HID)


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**НВА** ("НВА")


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**Хва** ("Хва")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("x25")


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** (ISDN)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** ("IPX")


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**ДКК** ("ДКК")


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E. 164** ("E. 164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** ("другое")


</dt> <dd></dd> </dl>

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Элементы управления питанием системы DMTF \| 001,2 ")
</dt> </dl>

Массив конкретных возможностей логического устройства, связанных с питанием.

Это свойство наследуется **от \_ CIM**-унаследованной модели.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)


</dt> <dd>

Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)


</dt> <dd>

Устройство может изменить свое состояние электропитания на основе использования или других критериев.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)


</dt> <dd>

Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)


</dt> <dd>

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)


</dt> <dd>

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.

</dd> </dl>

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

**Установлен**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние электропитания компьютерной системы и связанной с ней операционной системы.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd>

Неизвестно.

</dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)


</dt> <dd>

Полная мощность.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)


</dt> <dd>

Система находится в состоянии энергосбережения и по-прежнему работает, но может привести к снижению производительности.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)


</dt> <dd>

Система не работает, но ее можно быстро приступить к полной мощности.

</dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (4)


</dt> <dd>

Известно, что система находится в режиме энергосбережения, но ее точное состояние неизвестно.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)


</dt> <dd>

Цикл электропитания.

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)


</dt> <dd>

Выключение питания.

</dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (7)


</dt> <dd>

Система находится в состоянии предупреждения, а также в режиме энергосбережения.

</dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Энергосбережение **— режим гибернации** (8)


</dt> <dd>

Power Save Гибернация.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Энергосбережение **— мягкое отключение** (9)


</dt> <dd>

Энергосбережение с мягким отключением.

</dd> </dl>

</dd> <dt>

**примарйовнерконтакт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, которая предоставляет сведения о том, как связаться с основным владельцем системы (например, номером телефона, адресом электронной почты и т. д.).

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**примарйовнернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Имя основного владельца системы.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**ресеткапабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Security аппаратная безопасность \| 001,4 ")
</dt> </dl>

Если параметр включен, единая система компьютера может быть сброшена с оборудованием (например, с помощью кнопок питания и сброса). Если отключено, аппаратный сброс не разрешен.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Не реализовано** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Роли**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Роли, которые система играет в среде информационных технологий. Подклассы системы могут переопределять это свойство для определения явных значений ролей. Кроме того, Рабочая группа может описывать эвристику, соглашения и правила для указания ролей. Например, для экземпляра сетевой системы это свойство может содержать строку "Switch" или "Bridge".

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
</dt> </dl>

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ унитарикомпутерсистем** является производным от [**CIM \_ ComputerSystem**](cim-computersystem.md).

Инструментарий WMI не реализует этот класс. Классы WMI, производные от **CIM \_ унитарикомпутерсистем**, см. в разделе [Классы Win32](win32-provider.md).

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> </dl>

 

