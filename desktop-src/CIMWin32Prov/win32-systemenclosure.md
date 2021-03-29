---
description: Представляет свойства, связанные с физическим системным корпусом.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Класс Win32_SystemEnclosure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990761"
---
# <a name="win32_systemenclosure-class"></a>\_Класс Win32 системенклосуре

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ системенклосуре для Win32** представляет свойства, связанные с физическим системным корпусом.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ системенклосуре** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ системенклосуре** содержит следующие методы.



| Метод           | Описание                 |
|:-----------------|:----------------------------|
| **Является совместимым** | Не реализован.<br/> |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ системенклосуре** имеет следующие свойства.

<dl> <dt>

**аудиблеаларм**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, кадр оснащен звуковым сигналом.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

</dd> <dt>

**бреачдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Секуритибреач**")
</dt> </dl>

Произвольная строка, которая предоставляет дополнительные сведения, если свойство **секуритибреач** указывает, что произошло событие, связанное с безопасностью.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

</dd> <dt>

**каблеманажементстратеги**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, содержащая сведения о соединении различных кабелей и их объединении в пакет. Благодаря многим сетям, связанным с хранилищем и кабелям питания Управление кабелями может быть сложной и сложной задачей. Это свойство содержит сведения, помогающие в сборке и службе фрейма.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое описание объекта — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**чассистипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Глобальная таблица физического контейнера DMTF \| 002,1 "), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ шасси CIM**](cim-chassis.md).**Типедескриптионс**")
</dt> </dl>

Массив типов корпуса.

Это значение берется из члена **типа** в структуре **System корпуса или корпуса** в сведениях SMBIOS.

Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Рабочий стол** (3)


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

**Настольный компьютер с низким уровнем профилирования** (4)


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

**Поле пиццы** (5)


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

**Мини-башня** (6)


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

**Башня** (7)


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

**Переносимый** (8)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

**Портативный компьютер** (9)


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

**Записная книжка** (10)


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

**Удержание** (11)


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

**Стыковочный** стыковочный модуль (12)


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

**Все в одном** (13)


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

**Подзаписная книжка** (14)


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

**Экономия пространства** (15)


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

**Поле обеда** (16)


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

**Основной системный корпус** (17)


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

**Корпус расширения** (18)


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

**Корпус** (19)


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

**Корпус расширения шины** (20)


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

**Периферийный корпус** (21)


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

**Корпус для хранения данных** (22)


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

**Корпус для монтажа в стойку** (23)


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

**Компьютер с запечатанным корпусом** (24)

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

**Планшет** (30)

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

**Преобразуемый** (31)

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

**Отсоединяемый** (32)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**куррентрекуиредорпродуцед**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("ампер на 120 вольт")
</dt> </dl>

Ток, необходимый для шасси по адресу 120V. Если питание обеспечивается корпусом, как в случае источника бесперебойного питания (ИБП), это свойство может указывать на ампераже, созданный (в виде отрицательного числа).

Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).

</dd> <dt>

**Depth**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")
</dt> </dl>

Глубина физического пакета — в дюймах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**хеатженератион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("БТУ в час")
</dt> </dl>

Объем тепла, формируемый шасси в БТУ/час.

Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).

</dd> <dt>

**Height**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")
</dt> </dl>

Высота физического пакета — в дюймах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**хотсваппабле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, физический пакет может быть горячим заменой (если можно заменить элемент физически отличающимся, но эквивалентным, пока содержащий его пакет применяет к нему питание). Например, дисковый пакет, вставленный с помощью соединителей SCA, является съемным и может быть горячей заменой. Все пакеты, которые могут быть горячей заменой, по сути своей являются съемными и заменяемыми.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется указывать значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**локкпресент**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, кадр защищен с блокировкой.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя Организации, которая создает физический элемент.

Это значение поступает от **производителя** **системной корпуса или корпуса** в информации SMBIOS.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Модель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Имя, по которому известен физический элемент.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов свойство может быть переопределено как ключевое свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**нумберофповеркордс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество кабелей питания, которые должны быть подключены к корпусу для работы всех компонентов.

Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента. Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива. Имейте в виду, что если доступны только данные штрих-кода и они уникальны или могут использоваться в качестве ключа элемента, это свойство будет иметь **значение NULL** и данные штрих-кода, используемые в качестве ключа класса, в свойстве Tag.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**партнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Номер части, назначаемый Организацией, которая создает или производство физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**повередон**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true** показывает, что физический элемент включен.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Службе**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, физический пакет является съемным (если он предназначен для размещения в физическом контейнере, в котором он обычно обнаруживается, без нарушения функции общей упаковки). Пакет по-прежнему может быть съемным, если для удаления требуется электропитание. Если пакет может быть удален при включенном питании, элемент является съемным и может быть горячей заменой. Например, дополнительный аккумулятор ноутбука является съемным, как и дисковый пакет, вставленный с помощью соединителей приложения конфигурации сервера (SCA). Однако последняя может быть горячей заменой. Экран ноутбука не является съемным или не является избыточным источником питания. Удаление этих компонентов повлияет на функцию общей упаковки или невозможно из-за тесной интеграции пакета.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**Заменяемый**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, этот компонент физического носителя можно заменить физически отличающимся. Например, некоторые компьютерные системы позволяют обновить основную микросхему процессора до одной из более высоких оценок. В этом случае процессор считается заменяемым. Еще один пример — это пакет источника питания, подключенный к скользящим шинам. Все съемные пакеты по сути являются заменяемыми.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**секуритибреач**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Глобальный контейнер DMTF \| 002,12 "), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Бреачдескриптион**")
</dt> </dl>

Состояние физического нарушения рамки.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**Нет нарушений** (3)


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

**Попытки нарушения** (4)


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**Успешное нарушение** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**секуритистатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 3, \| состояние безопасности")
</dt> </dl>

Параметр безопасности для внешних входных данных, например клавиатура, на компьютер.

Это значение берется из элемента **состояние безопасности** в структуре **корпус или корпуса** в информации SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (3)


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

**Внешний интерфейс заблокирован** (4)


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

**Включен внешний интерфейс** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Номер, выделенный изготовителем, используемый для распознавания физического элемента.

Это значение берется из **серийного номера** , входящего в структуру **системы или корпуса** в сведениях SMBIOS.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**сервицедескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицефилософи**")
</dt> </dl>

Массив более подробных объяснений для любой записи в массиве **сервицефилософи** . Имейте в виду, что каждая запись этого массива связана с записью в **сервицефилософи** , расположенной в том же индексе.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

</dd> <dt>

**сервицефилософи**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ фисикалфраме**](cim-physicalframe.md).**Сервицедескриптионс**")
</dt> </dl>

Массив, который содержит сведения о том, будет ли кадр обслуживаться сверху, спереди, сзади или сбоку, независимо от того, есть ли в кадре скользящие лотки или съемные части, а также находится ли кадр в процессе перемещения, например при наличии подвижек.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Служба из верхнего уровня** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Служба с передней части** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Со стороны службы** (4)


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**Служба со стороны** (5)


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**Скользящие лотки** (6)


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

**Съемные стороны** (7)


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**Перемещаемый** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Номер единицы хранения для физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**SMBIOSAssetTag**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| тип SMBIOS 3, \| тег ресурса")
</dt> </dl>

Номер тега ресурса системного корпуса.

Это значение берется из раздела **номер тега актива** в структуре **корпус или корпуса** в информации SMBIOS.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

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

</dd> <dt>

**Тег**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**reoverride**](../wmisdk/standard-qualifiers.md) ("тег"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Уникальный идентификатор системного корпуса.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

Пример: "Системный корпус 1"

</dd> <dt>

**типедескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ шасси CIM**](cim-chassis.md)".**Чассистипес**")
</dt> </dl>

Массив дополнительных сведений о записях массива **чассистипес** . Имейте в виду, что каждая запись этого массива связана с записью в **чассистипес** , расположенной в том же индексе.

Это свойство наследуется от [**CIM- \_ корпуса**](cim-chassis.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Версия физического элемента.

Это значение берется из элемента **Version** корпуса или структуры **корпуса** в информации SMBIOS.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**висиблеаларм**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **true**, оборудование включает видимый сигнал.

Это свойство наследуется от [**CIM \_ фисикалфраме**](cim-physicalframe.md).

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("фунты")
</dt> </dl>

Вес физического пакета в фунтах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> <dt>

**Width**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("дюймы")
</dt> </dl>

Ширина физического пакета в дюймах.

Это свойство наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ системенклосуре** является производным от [**CIM- \_ корпуса**](cim-chassis.md).

## <a name="examples"></a>Примеры

При [сборе многопоточных системных ресурсов с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell в коллекции TechNet используется ряд классов, включая **Win32 \_ системенклосуре**, для получения данных из системы.

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

[**\_Корпус CIM**](cim-chassis.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> <dt>

[Задачи WMI: оборудование компьютера](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
