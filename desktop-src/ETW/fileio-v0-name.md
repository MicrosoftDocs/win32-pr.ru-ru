---
description: '\_ \_ Класс имен FileIo v0 является более старой версией класса типов событий для событий файлового ввода-вывода. Следующий синтаксис упрощен из MOF-кода.'
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Класс FileIo_V0_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 11a85c182511a866d3fb76f291b0a73ed0541fdee34b7e6f74c036b5446792db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041864"
---
# <a name="fileio_v0_name-class"></a>FileIo \_ v0 \_ имя класса

Класс **\_ \_ имен FileIo v0** является более старой версией класса типов событий для событий файлового ввода-вывода.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ имен FileIo v0** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **FileIo \_ v0 \_ Name** имеет следующие свойства.

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

**Windows Server 2003:** Чтобы получить букву диска для пути к имени файла, используйте значение свойства **FileObject** для сопоставлений с соответствующим событием [**\_ TypeGroup1 дискио**](diskio-typegroup1.md) . В событии **дискио \_ TypeGroup1** используйте значения свойств **дискнумбер** и **ByteOffset** для сопоставлений с соответствующим событием [**системконфиг \_ логдиск**](systemconfig-logdisk.md) . Свойство **дривелеттерстринг** содержит букву диска.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**FileIo \_ v0**](fileio-v0.md)
</dt> </dl>

 

 




