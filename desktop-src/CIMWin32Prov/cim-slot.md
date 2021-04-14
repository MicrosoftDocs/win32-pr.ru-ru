---
description: '\_Класс слота CIM представляет соединители, в которые вставляются пакеты.'
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: Класс CIM_Slot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496626"
---
# <a name="cim_slot-class"></a>\_Класс слота CIM

Класс **\_ слота CIM** представляет соединители, в которые вставляются пакеты. Например, физический пакет, который является диском, можно вставить в гнездо SCA, или карту (подкласс [CIM \_ фисикалпаккаже](cim-physicalpackage.md)) можно вставить в 16-, 32-или 64-битный слот расширения на доске размещения. В качестве примеров второго варианта используются разъемы PCI или PCMCIA типа III.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a>Члены

Класс **\_ слота CIM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ слота CIM** имеет следующие свойства.

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

**коннекторпинаут**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Произвольная строка, описывающая конфигурацию ПИН-кода и использование сигнала физическим соединителем.

Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).

</dd> <dt>

**коннектортипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("коннектортипе"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Системный слот DMTF \| 004,2 ")
</dt> </dl>

Тип физического соединителя. Массив задается, чтобы разрешить Описание сочетаний сведений о соединителях. Например, одна запись массива может указывать RS-232, другой DB-25, а третья — в качестве соединителя "папа".

Это свойство наследуется от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).

<dt>

0
</dt> <dd>

Неизвестно

</dd> <dt>

1
</dt> <dd>

Другое

</dd> <dt>

2
</dt> <dd>

Муж.

</dd> <dt>

3
</dt> <dd>

Жен.

</dd> <dt>

4
</dt> <dd>

Экранирование

</dd> <dt>

5
</dt> <dd>

Неэкранированной

</dd> <dt>

6
</dt> <dd>

SCSI (A) с высокой плотностью (50 ПИН-коды)

</dd> <dt>

7
</dt> <dd>

SCSI (A) с низкой плотностью (50 ПИН-коды)

</dd> <dt>

8
</dt> <dd>

SCSI (P) высокой плотности (68 ПИН-кодов)

</dd> <dt>

9
</dt> <dd>

SCSI SCA-I (80 контактов)

</dd> <dt>

10
</dt> <dd>

SCSI SCA-II (80 контактов)

</dd> <dt>

11
</dt> <dd>

Fibre Channel SCSI (DB-9, медный)

</dd> <dt>

12
</dt> <dd>

Fibre Channel SCSI (Fibre)

</dd> <dt>

13
</dt> <dd>

SCSI Fibre Channel SCA-II (40 контактов)

</dd> <dt>

14
</dt> <dd>

SCSI Fibre Channel SCA-II (20 контактов)

</dd> <dt>

15
</dt> <dd>

SCSI Fibre Channel БНК

</dd> <dt>

16
</dt> <dd>

ATA 3-1/2 дюйма (40 контактов)

</dd> <dt>

17
</dt> <dd>

ATA 2-1/2 дюйма (44 контактов)

</dd> <dt>

18
</dt> <dd>

ATA-2

</dd> <dt>

19
</dt> <dd>

ATA-3

</dd> <dt>

20
</dt> <dd>

ATA/66

</dd> <dt>

21
</dt> <dd>

DB-9

</dd> <dt>

22
</dt> <dd>

DB-15

</dd> <dt>

23
</dt> <dd>

DB-25

</dd> <dt>

24
</dt> <dd>

DB-36

</dd> <dt>

25
</dt> <dd>

RS-232C

</dd> <dt>

26
</dt> <dd>

RS-422

</dd> <dt>

27
</dt> <dd>

RS-423

</dd> <dt>

28
</dt> <dd>

RS-485

</dd> <dt>

29
</dt> <dd>

RS-449

</dd> <dt>

30
</dt> <dd>

V. 35

</dd> <dt>

31
</dt> <dd>

X. 21

</dd> <dt>

32
</dt> <dd>

IEEE-488

</dd> <dt>

33
</dt> <dd>

ауи

</dd> <dt>

34
</dt> <dd>

UTP Категория 3

</dd> <dt>

35
</dt> <dd>

UTP Категория 4

</dd> <dt>

36
</dt> <dd>

UTP Категория 5

</dd> <dt>

37
</dt> <dd>

бнк

</dd> <dt>

38
</dt> <dd>

RJ11

</dd> <dt>

39
</dt> <dd>

RJ45

</dd> <dt>

40
</dt> <dd>

Оптоволоконный микрофон

</dd> <dt>

41
</dt> <dd>

Apple АУИ

</dd> <dt>

42
</dt> <dd>

Геопорт Apple

</dd> <dt>

43
</dt> <dd>

PCI

</dd> <dt>

44
</dt> <dd>

ISA

</dd> <dt>

45
</dt> <dd>

ИСПОЛЬЗУЕТ

</dd> <dt>

46
</dt> <dd>

VESA

</dd> <dt>

47
</dt> <dd>

СТАНДАРТ

</dd> <dt>

48
</dt> <dd>

Тип PCMCIA I

</dd> <dt>

49
</dt> <dd>

PCMCIA типа II

</dd> <dt>

50
</dt> <dd>

PCMCIA типа III

</dd> <dt>

51
</dt> <dd>

Порт зв

</dd> <dt>

52
</dt> <dd>

CardBus

</dd> <dt>

53
</dt> <dd>

USB

</dd> <dt>

54
</dt> <dd>

IEEE 1394

</dd> <dt>

55
</dt> <dd>

хиппи

</dd> <dt>

56
</dt> <dd>

ХССДК (6 контактов)

</dd> <dt>

57
</dt> <dd>

гбик

</dd> <dt>

58
</dt> <dd>

DIN

</dd> <dt>

59
</dt> <dd>

Мини-DIN

</dd> <dt>

60
</dt> <dd>

Micro-DIN

</dd> <dt>

61
</dt> <dd>

PS/2

</dd> <dt>

62
</dt> <dd>

Инфракрасная связь

</dd> <dt>

63
</dt> <dd>

HP-ХИЛ

</dd> <dt>

64
</dt> <dd>

Доступ. Bus

</dd> <dt>

65
</dt> <dd>

нубус

</dd> <dt>

66
</dt> <dd>

центроникс

</dd> <dt>

67
</dt> <dd>

Mini-Centronics

</dd> <dt>

68
</dt> <dd>

Тип Mini-Centronics-14

</dd> <dt>

69
</dt> <dd>

Тип Mini-Centronics-20

</dd> <dt>

70
</dt> <dd>

Тип Mini-Centronics-26

</dd> <dt>

71
</dt> <dd>

Мышь шины

</dd> <dt>

72
</dt> <dd>

ADB

</dd> <dt>

73
</dt> <dd>

ИНТЕРФЕЙСА

</dd> <dt>

74
</dt> <dd>

Шина вме

</dd> <dt>

75
</dt> <dd>

VME64

</dd> <dt>

76
</dt> <dd>

Частный

</dd> <dt>

77
</dt> <dd>

Собственный слот карты процессора

</dd> <dt>

78
</dt> <dd>

Собственный слот карты памяти

</dd> <dt>

79
</dt> <dd>

Собственная подплата ввода/вывода

</dd> <dt>

80
</dt> <dd>

PCI-66 МГЦ

</dd> <dt>

81
</dt> <dd>

AGP2X

</dd> <dt>

82
</dt> <dd>

AGP4X

</dd> <dt>

83
</dt> <dd>

PC-98

</dd> <dt>

84
</dt> <dd>

PC-98-Хиресо

</dd> <dt>

85
</dt> <dd>

PC-H98

</dd> <dt>

86
</dt> <dd>

PC-98Note

</dd> <dt>

87
</dt> <dd>

PC-98Full

</dd> <dt>

88
</dt> <dd>

АДАПТЕР SSA SCSI

</dd> <dt>

89
</dt> <dd>

Кольцевая

</dd> <dt>

90
</dt> <dd>

Соединитель IDE платы

</dd> <dt>

91
</dt> <dd>

Разъем флоппи-дисковода

</dd> <dt>

92
</dt> <dd>

9. закрепление двух встроенных

</dd> <dt>

93
</dt> <dd>

25-контактный двойной текст

</dd> <dt>

94
</dt> <dd>

50. закрепление двух встроенных

</dd> <dt>

95
</dt> <dd>

68. закрепление двух встроенных

</dd> <dt>

96
</dt> <dd>

Звуковой разъем на доске

</dd> <dt>

97
</dt> <dd>

Мини-гнездо

</dd> <dt>

98
</dt> <dd>

PCI-X

</dd> <dt>

99
</dt> <dd>

Сбус IEEE 1396-1993 32, бит

</dd> <dt>

100
</dt> <dd>

Сбус IEEE 1396-1993 64, бит

</dd> <dt>

101
</dt> <dd>

MCA

</dd> <dt>

102
</dt> <dd>

гио

</dd> <dt>

103
</dt> <dd>

XIO

</dd> <dt>

104
</dt> <dd>

хио

</dd> <dt>

105
</dt> <dd>

нгио

</dd> <dt>

106
</dt> <dd>

PMC

</dd> <dt>

107
</dt> <dd>

мтрж

</dd> <dt>

108
</dt> <dd>

VF-45

</dd> <dt>

109
</dt> <dd>

Будущие операции ввода-вывода

</dd> <dt>

110
</dt> <dd>

SC

</dd> <dt>

111
</dt> <dd>

SG

</dd> <dt>

112
</dt> <dd>

Электричество

</dd> <dt>

113
</dt> <dd>

Лазер

</dd> <dt>

114
</dt> <dd>

Лента

</dd> <dt>

115
</dt> <dd>

GLM

</dd> <dt>

116
</dt> <dd>

1x9

</dd> <dt>

117
</dt> <dd>

Мини-SG

</dd> <dt>

118
</dt> <dd>

LC

</dd> <dt>

119
</dt> <dd>

хсск

</dd> <dt>

120
</dt> <dd>

ВХДЦИ экранированный (68 контактов)

</dd> <dt>

121
</dt> <dd>

InfiniBand

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

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

**хеигхталловед**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")
</dt> </dl>

Максимальная высота платы адаптера в дюймах, которую можно вставить в слот.

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

**ленгсалловед**
</dt> <dd> <dl> <dt>

Тип данных: **real32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("дюймы")
</dt> </dl>

Максимальная длина платы адаптера в дюймах, которую можно вставить в слот.

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Организация, создавшая физический элемент. Дополнительные сведения см. в описании свойства **Vendor** [**\_ продукта CIM**](cim-product.md).

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**максдатавидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,3 "), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) (" бит ")
</dt> </dl>

Максимальная ширина шины (в битах) карт адаптеров, которые можно вставить в слот.

<dt>

<span id="8"></span>

**8** (0)


</dt> <dd></dd> <dt>

<span id="16"></span>

**16** (1)


</dt> <dd></dd> <dt>

<span id="32"></span>

**32** (2)


</dt> <dd></dd> <dt>

<span id="64"></span>

**64** (3)


</dt> <dd></dd> <dt>

<span id="128"></span>

**128** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Модель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Имя, по которому обычно известен физический элемент.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")
</dt> </dl>

Метка, по которой известен объект. При создании подклассов это свойство может быть переопределено как свойство ключа.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Число**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Номер физического слота, который можно использовать в качестве индекса в таблице системных слотов, чтобы определить, является ли слот физически занятым.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные данные, помимо сведений о тегах актива, которые можно использовать для поиска физического элемента. Одним из примеров являются данные штрих-кода, связанные с элементом, который также имеет тег актива. Обратите внимание, что если доступны только данные с штрих-кодом и они уникальны и могут использоваться в качестве ключа элемента, это свойство будет иметь значение null, а данные штрих-кода будут использоваться в качестве ключа класса в свойстве **Tag** .

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**партнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Номер детали, назначенный Организацией, которая создала или изготовлена физический элемент.

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

**пурпоседескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ область CIM**".**СпеЦиалпурпосе**")
</dt> </dl>

Произвольная строка, описывающая, как этот слот физически уникален и может содержать специальные типы оборудования. Это свойство имеет значение, только если соответствующее логическое свойство **спеЦиалпурпосе** имеет значение **true**.

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Номер, выделенный изготовителем, используемый для распознавания физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Номер единицы хранения для физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**спеЦиалпурпосе**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ область CIM**".**Пурпоседескриптион**")
</dt> </dl>

Если **значение равно true**, слот физически уникален и может содержать специальные типы оборудования (например, разъем для графического процессора). Если **значение — true**, свойство **пурпоседескриптион** должно указывать, как сегмент является уникальным или назначением слота.

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

</dd> <dt>

**суппортшотплуг**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение — true**, слот поддерживает горячее подключение адаптеров.

</dd> <dt>

**Тег**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Произвольная строка, однозначно идентифицирующая физический элемент и служащая в качестве ключа элемента. Это свойство может содержать такие сведения, как тег актива или данные серийного номера. Ключ для [**CIM \_ фисикалелемент**](cim-physicalelement.md) помещается очень высоким в иерархии объектов для независимого обнаружения оборудования или сущности независимо от физического размещения в (или в) шкафов, адаптеров и т. д. Например, съемный компонент, который можно использовать для горячей замены, может быть взят из содержащего его пакета (с областями видимости) и временно не используется. Объект по-прежнему продолжает существовать и даже может быть вставлен в другой контейнер области. Ключом для физического элемента является произвольная строка, которая определяется независимо от размещения или расположения, ориентированного на расположение.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**сермалратинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,11 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" МВт ")
</dt> </dl>

Максимальное рассеяние температуры слота в МВт.

</dd> <dt>

**вккмикседволтажесуппорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,9 ")
</dt> </dl>

Напряжение VCC, поддерживаемое слотом.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5** в (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Версия физического элемента.

Это свойство наследуется от [**CIM \_ фисикалелемент**](cim-physicalelement.md).

</dd> <dt>

**вппмикседволтажесуппорт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Системный слот DMTF \| 004,10 ")
</dt> </dl>

Напряжение VPP, поддерживаемое слотом.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

**3.3 v** (2)


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

**5** в (3)


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

**12** в (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ слота CIM** является производным от [**CIM \_ фисикалконнектор**](cim-physicalconnector.md).

Инструментарий WMI не реализует этот класс. Сведения о классах WMI, производных от **\_ области CIM**, см. в разделе [Классы Win32](win32-provider.md).

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

[**\_ФИСИКАЛКОННЕКТОР CIM**](cim-physicalconnector.md)
</dt> </dl>

 

