---
description: FileIo_V1_Name Class — этот класс является классом типа события для событий файлового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: Класс FileIo_V1_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 62069f8a462499dfbfd9cfa368b9f5985d4775e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106552"
---
# <a name="fileio_v1_name-class"></a>\_ \_ Класс имен FileIo v1

Этот класс является классом типа события для событий файлового ввода-вывода.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ имен FileIo v1** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ имен FileIo v1** имеет следующие свойства.

<dl> <dt>

FileName
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Полный путь к файлу, не включая букву диска.

</dd> <dt>

Закрыт
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Сопоставьте значение этого указателя со значением указателя **FileObject** в событии [**дискио \_ TypeGroup1**](diskio-typegroup1.md) , чтобы определить тип операции ввода-вывода.

</dd> </dl>

## <a name="remarks"></a>Remarks

**Windows Server 2003:** Чтобы получить букву диска для пути к имени файла, используйте значение свойства **FileObject** для сопоставлений с соответствующим событием [ \_ TypeGroup1 дискио](diskio-typegroup1.md) . В \_ событии дискио TypeGroup1 используйте значения свойств **Дискнумбер** и **ByteOffset** для сопоставления с соответствующим событием [системконфиг \_ логдиск](systemconfig-logdisk.md) (**ByteOffset** сопоставляется с **стартоффсет**). Свойство **дривелеттерстринг** содержит букву диска.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 




