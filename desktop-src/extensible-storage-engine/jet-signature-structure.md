---
description: 'Дополнительные сведения: структура JET_SIGNATURE'
title: Структура JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: 456eadecbaba7295753a18ec2ca739f5e3fc8391
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987827"
---
# <a name="jet_signature-structure"></a>Структура JET_SIGNATURE


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_signature-structure"></a>Структура JET_SIGNATURE

Структура **JET_SIGNATURE** содержит сведения, однозначно определяющие базу данных.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Элементы

**улрандом**

Номер, назначенный случайным образом.

**логтимекреате**

[JET_LOGTIME](./jet-logtime-structure.md) во время выполнения [жеткреатедатабасе](./jetcreatedatabase-function.md) .

**сзкомпутернаме**

Необязательное строковое значение NetBIOS-имени компьютера. Это значение не может быть задано.

### <a name="remarks"></a>Комментарии

Его можно найти в качестве элемента [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)
