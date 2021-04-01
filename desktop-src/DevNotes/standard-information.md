---
description: Содержит стандартный атрибут сведений. Этот атрибут имеется в каждой записи базового файла и должен быть резидентным.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Структура STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072337"
---
# <a name="standard_information-structure"></a>Стандартная \_ информационная структура

\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]

Содержит стандартный атрибут сведений. Этот атрибут имеется в каждой записи базового файла и должен быть резидентным.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a>Члены

<dl> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**OwnerId**
</dt> <dd>

Идентификатор владельца файла из индекса безопасности.

</dd> <dt>

**секуритид**
</dt> <dd>

Идентификатор безопасности для файла.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Обратите внимание, что для этой структуры нет связанного файла заголовка.

Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Основная таблица файлов](master-file-table.md)
</dt> </dl>

 

 
