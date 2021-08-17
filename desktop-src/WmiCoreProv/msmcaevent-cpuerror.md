---
description: Представляет событие ошибки ЦП. этот класс доступен только в 64-разрядных Windows системах.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: Класс MSMCAEvent_CPUError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 42542f9e32bee31e44df65c0d0ade3d337e3fe395315fe28d6fd8b1c66b3b8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926877"
---
# <a name="msmcaevent_cpuerror-class"></a>\_Класс мсмкаевент кпуеррор

Класс **мсмкаевент \_ кпуеррор** представляет событие ошибки ЦП. этот класс доступен только в 64-разрядных Windows системах.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Члены

Класс **мсмкаевент \_ кпуеррор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсмкаевент \_ кпуеррор** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true**, если данный экземпляр класса активен; в противном случае — **false**.

</dd> <dt>

**аддитионалеррорс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число дополнительных ошибок в записи MCA.

</dd> <dt>

**Загрузки**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

ЦП, сообщающий об ошибке. Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.

</dd> <dt>

**еррорсеверити**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Степень серьезности ошибки, о которой сообщается.



| Значение                                                                                                | Значение                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Восстанавливается<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Аварий<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Исправимая<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Уникальный идентификатор для этого экземпляра класса.

</dd> <dt>

**Уровень**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **вмимиссингдата** (-1)
</dt> </dl>

Уровень кэша, буфер перевода (TLB) или структура Micro-архитектуры, в которой произошла ошибка. Значение 0 (ноль) обозначает первый уровень.

</dd> <dt>

**логтоевентлог**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если значение равно нулю, это событие не заносится в журнал системных событий.

</dd> <dt>

**раврекорд**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив байтов, содержащий необработанную запись об ошибке. Число элементов в массиве, которое указывает свойство **size** .

</dd> <dt>

**RecordId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор записи записи об ошибке для этой ошибки.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Размер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Размер необработанной записи об ошибке в байтах.

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип сообщения журнала событий. эти сообщения соответствуют кодам сообщений журнала событий, используемых для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **мсмкаевент \_ кпуеррор** является производным от [**WMIEvent**](wmievent.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Классы МСМКА](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

