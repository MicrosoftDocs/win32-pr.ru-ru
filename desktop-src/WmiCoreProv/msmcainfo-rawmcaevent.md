---
description: Содержит событие архитектуры проверки компьютера (MCA). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: d1806b91-43a3-4329-8fe5-de1e4755740f
title: Класс MSMCAInfo_RawMCAEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAEvent
- MSMCAInfo_RawMCAEvent.Active
- MSMCAInfo_RawMCAEvent.Count
- MSMCAInfo_RawMCAEvent.InstanceName
- MSMCAInfo_RawMCAEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: e15af79c67265823e0025849e4c2ef27f690265c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999199"
---
# <a name="msmcainfo_rawmcaevent-class"></a>\_Класс мсмкаинфо равмкаевент

Класс **мсмкаинфо \_ равмкаевент** содержит событие архитектура проверки компьютера (MCA). Этот класс доступен только в 64-разрядных системах Windows.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAInfo_RawMCAEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Члены

Класс **мсмкаинфо \_ равмкаевент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсмкаинфо \_ равмкаевент** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение TRUE, если данный экземпляр класса активен; в противном случае — **значение false**.

</dd> <dt>

**Количество**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число записей об ошибках.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Строка, однозначно идентифицирующая данный экземпляр класса **мсмкаинфо \_ равмкаевент** .

</dd> <dt>

**Записи**
</dt> <dd> <dl> <dt>

Тип данных: **массив \_ записей мсмкаинфо**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив записей об ошибках MCA. Число записей об ошибках MCA в массиве задается свойством **Count** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **мсмкаинфо \_ равмкаевент** является производным от [**WMIEvent**](wmievent.md).

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

 

