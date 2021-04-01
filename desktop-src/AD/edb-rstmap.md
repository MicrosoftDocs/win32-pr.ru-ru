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
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071741"
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

## <a name="requirements"></a>Требования



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

 

 





