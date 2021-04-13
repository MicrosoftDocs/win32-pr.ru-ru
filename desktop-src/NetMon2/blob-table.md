---
description: Содержит массив больших двоичных объектов.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Структура BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264372"
---
# <a name="blob_table-structure"></a>Структура таблицы больших двоичных объектов \_

Структура **\_ таблицы больших двоичных объектов** содержит массив больших двоичных объектов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**двнумблобс**
</dt> <dd>

Индикатор, которым следуют многие большие двоичные объекты.

</dd> <dt>

**хблобс**
</dt> <dd>

Обработчик для массива больших двоичных объектов.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




