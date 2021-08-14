---
title: Структура EDB_RSTMAP (Нтдсбкли. h)
description: Используется с функцией Дсресторерегистер для преобразования резервной копии базы данных в новую базу данных.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP структуры Active Directory
- PEDB_RSTMAP Active Directory указателя на структуру
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c81fe35d8d41818d279df094a57c041b8ea52212d2ce2f0cdc379628f5d5971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191695"
---
# <a name="edb_rstmap-structure"></a>\_Структура EDB рстмап

Структура **EDB \_ рстмап** используется с функцией [**дсресторерегистер**](dsrestoreregister.md) для отображения резервной копии базы данных в новой базе данных.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a>Члены

<dl> <dt>

**сздатабасенаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит имя базы данных при ее резервном копировании.

</dd> <dt>

**сзневдатабасенаме**
</dt> <dd>

Указатель на строку, завершающуюся нулем, которая содержит новое имя базы данных, включая ее новое расположение, если применимо.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Нтдсбкли. h</dt> </dl> |
| Имя в кодировке Юникод и ANSI<br/>   | **EDB \_ РСТМАПВ** (Юникод) и **\_ рстмапа EDB** (ANSI)<br/>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дсресторерегистер**](dsrestoreregister.md)
</dt> <dt>

[Структуры резервного копирования каталога](directory-backup-structures.md)
</dt> </dl>

 

 





