---
description: Указывает на недействительную ошибку архитектуры проверки машин (MCA). недопустимая ошибка MCA определяет формат ошибки, который не соответствует спецификациям Windows. этот класс доступен только в 64-разрядных Windows системах.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: Класс MSMCAEvent_InvalidError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 5a42ee7dfcc9864cdd4ca90ba7d66903407352e92224e5ded7a16ace4e053d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821978"
---
# <a name="msmcaevent_invaliderror-class"></a>\_Класс мсмкаевент инвалидеррор

Класс **мсмкаевент \_ инвалидеррор** указывает на недействительную ошибку архитектуры проверки машин (MCA). недопустимая ошибка MCA определяет формат ошибки, который не соответствует спецификациям Windows. этот класс доступен только в 64-разрядных Windows системах.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Члены

Класс **мсмкаевент \_ инвалидеррор** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсмкаевент \_ инвалидеррор** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.

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

Уникальный идентификатор этого экземпляра класса.

</dd> <dt>

**логтоевентлог**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.

</dd> <dt>

**раврекорд**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

массив байтов, содержащий необработанную запись об ошибке, представленную Windows слоем абстракции системы (SAL). Число элементов в массиве задается свойством **size** .

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

Размер необработанной записи об ошибке.

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

Класс **мсмкаевент \_ инвалидеррор** является производным от [**WMIEvent**](wmievent.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2003<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Классы МСМКА](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

