---
description: '\_Класс WMI взаимосвязей Win32 1394ControllerDevice связывает с контроллером высокоскоростной последовательной шины (IEEE 1394 Firewire) и \_ подключенным к нему экземпляром CIM.'
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Класс Win32_1394ControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4877c5e1088e2cf801987d2729d02f64075fc73d1d48daba1fc83b20041c1758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918114"
---
# <a name="win32_1394controllerdevice-class"></a>\_Класс Win32 1394ControllerDevice

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ 1394ControllerDevice** связывает с контроллером высокоскоростной последовательной шины (IEEE 1394 Firewire) и подключенным к нему экземпляром [**\_ CIM**](cim-logicaldevice.md) . Эта последовательная шина обеспечивает улучшенное подключение для широкого спектра устройств, включая аудио-и видеокомпоненты, периферийные устройства хранения, другие компьютеры и портативные устройства. Стандарт IEEE 1394 реализован в индустрии бытовой электроники и предоставляет совместимый с самонастраивающийся интерфейс расширения.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ 1394ControllerDevice** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ 1394ControllerDevice** имеет следующие свойства.

<dl> <dt>

**акцессстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, является ли контроллер активной командой или доступом к устройству. Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.

Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Активно** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Неактивно** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ 1394Controller**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")
</dt> </dl>

Ссылка на Win32 \_ 1394Controller Antecedent представляет контроллер 1394, связанный с этим устройством.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")
</dt> </dl>

\_Зависимая ссылка на модель CIM представляет собой CIM, \_ подключенный к контроллеру 1394.

</dd> <dt>

**неготиатеддатавидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")
</dt> </dl>

Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами. Ширина данных указывается в битах. Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).

Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).

</dd> <dt>

**неготиатедспид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")
</dt> </dl>

Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами. Скорость указывается в битах в секунду. Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).

</dd> <dt>

**нумберофхардресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число жестких сбросов, выданных контроллером. При жесткой сбросе устройство возвращается в состояние инициализации или загрузки. Все внутренние сведения о состоянии устройства и данные теряются.

Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).

</dd> <dt>

**нумберофсофтресетс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Количество мягких сбросов, выданных контроллером. При мягком сбросе текущее состояние и данные устройства не полностью очищаются. Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.

Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ 1394ControllerDevice** является производным от [**CIM \_ контролледби**](cim-controlledby.md).

## <a name="examples"></a>Примеры

Следующий пример кода PowerShell извлекает сведения об устройстве контроллера 1394.


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



Предыдущий пример кода возвращает следующие сведения:

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_КОНТРОЛЛЕДБИ CIM**](cim-controlledby.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

