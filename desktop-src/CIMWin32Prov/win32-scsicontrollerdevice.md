---
description: '\_Класс WMI взаимосвязей Win32 сксиконтроллердевице связывает контроллер с системным интерфейсом (SCSI) и логическим устройством (дисковый накопитель), подключенным к нему.'
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Класс Win32_SCSIControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f703d5a290245b1596801f78c005c565faa45296c3582e4feaad5dc4011787b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834175"
---
# <a name="win32_scsicontrollerdevice-class"></a>\_Класс Win32 сксиконтроллердевице

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ сксиконтроллердевице** связывает контроллер с системным интерфейсом (SCSI) и логическим устройством (дисковый накопитель), подключенным к нему.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сксиконтроллердевице** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ сксиконтроллердевице** имеет следующие свойства.

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

Тип данных: **Win32 \_ сксиконтроллер**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ сксиконтроллер")
</dt> </dl>

Ссылка на [**Win32 \_ сксиконтроллер**](win32-scsicontroller.md) ANTECEDENT представляет контроллер SCSI, связанный с этим устройством.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")
</dt> </dl>

Ссылка Dependent логического устройства [**CIM \_**](cim-logicaldevice.md) представляет логическое устройство, подключенное к контроллеру SCSI.

</dd> <dt>

**неготиатеддатавидс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("биты")
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

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")
</dt> </dl>

Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами. Скорость указывается в битах в секунду. Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

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

Класс **Win32 \_ сксиконтроллердевице** является производным от [**CIM \_ контролледби**](cim-controlledby.md).

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

[**\_КОНТРОЛЛЕДБИ CIM**](cim-controlledby.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
