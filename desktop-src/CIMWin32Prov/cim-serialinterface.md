---
description: Класс CIM \_ сериалинтерфаце представляет \_ отношение CIM контролледби, указывающее, к каким устройствам осуществляется доступ через последовательный контроллер и характеристики доступа.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: Класс CIM_SerialInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895793"
---
# <a name="cim_serialinterface-class"></a>\_Класс CIM сериалинтерфаце

Класс **CIM \_ сериалинтерфаце** представляет отношение [**CIM \_ контролледби**](cim-controlledby.md) , указывающее, к каким устройствам осуществляется доступ через последовательный контроллер и характеристики доступа.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ сериалинтерфаце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **CIM \_ сериалинтерфаце** имеет следующие свойства.

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

Тип данных: **CIM \_ сериалконтроллер**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

[**\_ Сериалконтроллер CIM**](cim-serialcontroller.md) , описывающий последовательный контроллер.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_** с типом "модель"
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.

</dd> <dt>

**фловконтролинфо**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает поток управления для передаваемых данных.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (2)


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**Ксонксофф** (3)


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**Ксонксофф и RTS/CTS** (5)


</dt> <dd>

Ксонксофф и RTS/CTS

</dd> </dl>

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

</dd> <dt>

**нумберофстопбитс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")
</dt> </dl>

Количество останавливаемых битов для передачи.

</dd> <dt>

**паритинфо**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сведения о параметре четности для передаваемых данных.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Нет** (1)


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

**Даже** (2)


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

**Нечетная** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **CIM \_ сериалинтерфаце** является производным от [**CIM \_ контролледби**](cim-controlledby.md).

Инструментарий WMI не реализует этот класс.

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

[**\_КОНТРОЛЛЕДБИ CIM**](cim-controlledby.md)
</dt> </dl>

 

