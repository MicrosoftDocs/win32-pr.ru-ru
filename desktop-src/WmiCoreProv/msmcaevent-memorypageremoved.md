---
description: Указывает, что страница памяти была удалена из системы из-за избыточной проверки ошибок оборудования и ошибок коррекции (ECC). этот класс доступен только в 64-разрядных Windows системах.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: Класс MSMCAEvent_MemoryPageRemoved
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: d8229848cf1113736e3b9a4e37cd9493b8c724c58c384387536cded4742ca3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558471"
---
# <a name="msmcaevent_memorypageremoved-class"></a>\_Класс мсмкаевент меморипажеремовед

Класс **мсмкаевент \_ меморипажеремовед** указывает на то, что страница памяти была удалена из системы в связи с избыточной проверкой ошибок оборудования и исправлением ошибок (ECC). этот класс доступен только в 64-разрядных Windows системах.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a>Члены

Класс **мсмкаевент \_ меморипажеремовед** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсмкаевент \_ меморипажеремовед** имеет следующие свойства.

<dl> <dt>

**Активен**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

**Значение true**, если данный экземпляр класса активен; в противном случае — **false**.

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

**PhysicalAddress**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Адрес страницы памяти, которая была удалена.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **мсмкаевент \_ меморипажеремовед** является производным от [**WMIEvent**](wmievent.md).

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

 

