---
description: Этот класс является классом типа события для события создания файла. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: Класс FileIo_Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984492"
---
# <a name="fileio_create-class"></a>\_Класс FileIo CREATE

Этот класс является классом типа события для события создания файла.

Следующий синтаксис упрощен из MOF-кода.

## <a name="syntax"></a>Синтаксис

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a>Участники

Класс **FileIo \_ CREATE** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **FileIo \_ CREATE** имеет следующие свойства.

<dl> <dt>

**креатеоптионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (4)
</dt> </dl>

Значения, передаваемые в параметрах *креатеоптионс* и *креатедиспоситионс* функции [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**FileAttributes**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (5)
</dt> </dl>

Значение, передаваемое в параметре *FileAttributes* функции [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**Закрыт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (3), Pointer
</dt> </dl>

Идентификатор, который можно использовать для сопоставления операций с одним и тем же открытым экземпляром объекта File между событиями создания и закрытия файла.

</dd> <dt>

**ирпптр**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (1), Pointer
</dt> </dl>

Пакет запроса ввода-вывода. Это свойство определяет действие ввода-вывода.

</dd> <dt>

**опенпас**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (7), Стрингтерминатион ("NullTerminated"), Format ("w")
</dt> </dl>

Путь к файлу.

</dd> <dt>

**ShareAccess**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (6)
</dt> </dl>

Значение, передаваемое в параметре *шареакцесс* функции [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .

</dd> <dt>

**ттид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: Вмидатаид (2), Pointer
</dt> </dl>

Идентификатор потока, который создает файл.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**FileIo**](fileio.md)
</dt> </dl>

 

 
