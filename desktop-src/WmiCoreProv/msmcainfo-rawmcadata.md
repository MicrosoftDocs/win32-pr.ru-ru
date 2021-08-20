---
description: Указывает журналы необработанных проверок компьютеров (MCA). этот класс доступен только в 64-разрядных Windows системах.
ms.assetid: d465ba8d-14b2-4911-ae19-19ebeb32126e
title: Класс MSMCAInfo_RawMCAData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawMCAData
- MSMCAInfo_RawMCAData.Active
- MSMCAInfo_RawMCAData.Count
- MSMCAInfo_RawMCAData.InstanceName
- MSMCAInfo_RawMCAData.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 2b7ac9f8c474a1aee55d0dd70a5a838102aec66bc8b3ba3d867070430c38a3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821868"
---
# <a name="msmcainfo_rawmcadata-class"></a>\_Класс мсмкаинфо равмкадата

**Мсмкаинфо \_ равмкадата** указывает журнал необработанных проверок машин (MCA). этот класс доступен только в 64-разрядных Windows системах.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAInfo_RawMCAData : MSMCAInfo
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Члены

Класс **мсмкаинфо \_ равмкадата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсмкаинфо \_ равмкадата** имеет следующие свойства.

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

Уникальный идентификатор этого экземпляра класса.

</dd> <dt>

**Записи**
</dt> <dd> <dl> <dt>

Тип данных: **массив \_ записей мсмкаинфо**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив записей об ошибках MCA. Число записей об ошибках MCA в массиве задается свойством **Count** .

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **мсмкаинфо \_ равмкадата** является производным от [**мсмкаинфо**](msmcainfo.md).

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

[**мсмкаинфо**](msmcainfo.md)
</dt> </dl>

 

