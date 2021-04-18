---
description: Структура, используемая функцией Сфкжетфилес.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Структура PPROTECT_FILE_ENTRY (Сфкфилес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702301"
---
# <a name="pprotect_file_entry-structure"></a>\_ \_ Структура записи файла ппротект

\[Эта структура доступна для использования в операционных системах, указанных в разделе требования. Поддержка этой структуры была удалена в Windows Vista и Windows Server 2008. Вместо этого используйте поддерживаемые функции, перечисленные в [функциях WRP](wfp-functions.md) .\]

Структура, используемая функцией [**сфкжетфилес**](sfcgetfiles.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a>Члены

<dl> <dt>

**SourceFileName**
</dt> <dd>

Указатель на строковое значение, содержащее имя файла исходного файла. Это значение будет **равно NULL** , если файл не переименовывается при установке.

</dd> <dt>

**FileName**
</dt> <dd>

Указатель на строковое значение, содержащее имя файла назначения плюс полный путь к файлу.

</dd> <dt>

**инфнаме**
</dt> <dd>

Указатель на строковое значение, содержащее имя файла INF, который предоставляет сведения о макете. При использовании макета по умолчанию этот параметр может иметь **значение NULL** .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                 |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                        |
| Header<br/>                   | <dl> <dt>Сфкфилес. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сфкжетфилес**](sfcgetfiles.md)
</dt> </dl>

 

 




