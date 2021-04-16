---
description: Содержит исправленное событие платформы (CPE). Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: b24a390e-293d-4dd4-b747-33c298a5d45f
title: Класс MSMCAInfo_RawCorrectedPlatformEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCorrectedPlatformEvent
- MSMCAInfo_RawCorrectedPlatformEvent.Active
- MSMCAInfo_RawCorrectedPlatformEvent.Count
- MSMCAInfo_RawCorrectedPlatformEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 906587ca9ee153eb93542c3e749e8164e6a5ee7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712611"
---
# <a name="msmcainfo_rawcorrectedplatformevent-class"></a>\_Класс мсмкаинфо равкорректедплатформевент

Класс **мсмкаинфо \_ Равкорректедплатформевент** содержит исправленное событие платформы (CPE). Этот класс доступен только в 64-разрядных системах Windows.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAInfo_RawCorrectedPlatformEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Члены

Класс **мсмкаинфо \_ равкорректедплатформевент** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсмкаинфо \_ равкорректедплатформевент** имеет следующие свойства.

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

**Записи**
</dt> <dd> <dl> <dt>

Тип данных: **массив \_ записей мсмкаинфо**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив записей об ошибках MCA. Число записей об ошибках MCA в массиве задается свойством **Count** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **мсмкаинфо \_ равкорректедплатформевент** является производным от [**WMIEvent**](wmievent.md).

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

 

 




