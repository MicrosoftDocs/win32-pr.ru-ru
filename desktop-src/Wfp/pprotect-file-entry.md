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
ms.openlocfilehash: c9070290170febf08e532b071812600fb0ef8755302a4bd1603858659196d0c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053202"
---
# <a name="pprotect_file_entry-structure"></a>\_ \_ Структура записи файла ппротект

\[Эта структура доступна для использования в операционных системах, указанных в разделе требования. поддержка этой структуры была удалена в Windows Vista и Windows Server 2008. Вместо этого используйте поддерживаемые функции, перечисленные в [функциях WRP](wfp-functions.md) .\]

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                 |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                        |
| Заголовок<br/>                   | <dl> <dt>Сфкфилес. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сфкжетфилес**](sfcgetfiles.md)
</dt> </dl>

 

 




