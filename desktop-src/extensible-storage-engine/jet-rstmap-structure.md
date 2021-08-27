---
description: 'Дополнительные сведения: структура JET_RSTMAP'
title: Структура JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f3813be8e1ea076a401ce5cdabef3e454b98c1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983587"
---
# <a name="jet_rstmap-structure"></a>Структура JET_RSTMAP


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_rstmap-structure"></a>Структура JET_RSTMAP

Структура **JET_RSTMAP** позволяет переназначить пути к файлам базы данных, которые хранятся в журналах транзакций во время восстановления, при использовании функций [жетинит](./jetinit-function.md) и [жетекстерналресторе](./jetexternalrestore-function.md) . Это позволяет перемещать базы данных в автономном режиме или при восстановлении из резервной копии.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Элементы

**сздатабасенаме**

Текущий абсолютный путь к базе данных, связанной с журналами транзакций, которые воспроизводятся во время восстановления.

**сзневдатабасенаме**

Новый абсолютный путь к базе данных.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_RSTMAP_W</strong> (Юникод) и <strong>JET_RSTMAP_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[жетекстерналресторе](./jetexternalrestore-function.md)  
[жетинит](./jetinit-function.md)
