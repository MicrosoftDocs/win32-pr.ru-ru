---
description: Указывает на запись, исправленную проверку компьютера MCA (CMC) или исправленную ошибку платформы (CPE). этот класс доступен только в 64-разрядных Windows системах.
ms.assetid: 4edbca20-2525-4e35-ab79-8cf421343144
title: Класс MSMCAInfo_Entry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_Entry
- MSMCAInfo_Entry.Data
- MSMCAInfo_Entry.Length
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8f6146d629678c1ee209738095fea901f0edb865bccb9aff2d4eeab02d18e773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640909"
---
# <a name="msmcainfo_entry-class"></a>\_Класс записи мсмкаинфо

Класс **\_ записи мсмкаинфо** указывает на запись, исправленную проверку компьютера (CMC) или исправленную ошибку платформы (CPE). этот класс доступен только в 64-разрядных Windows системах.

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class MSMCAInfo_Entry : MSMCAInfo
{
  uint8  Data[];
  uint32 Length;
};
```

## <a name="members"></a>Члены

Класс **\_ записи мсмкаинфо** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ записи мсмкаинфо** имеет следующие свойства.

<dl> <dt>

**Data**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив целых чисел, содержащий полную запись об ошибке MCA, сообщаемую уровнем абстрагирования системы (SAL). SAL — это код, записываемый в ПЗУ, который вызывается операционной системой для выполнения операций, зависящих от платформы. Он аналогичен BIOS на платформе x86.

</dd> <dt>

**Длина**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число байтов в записи об ошибке.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ записи мсмкаинфо** является производным от [**мсмкаинфо**](msmcainfo.md).

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

 

 




