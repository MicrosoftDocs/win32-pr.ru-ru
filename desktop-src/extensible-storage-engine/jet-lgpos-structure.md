---
description: 'Дополнительные сведения: структура JET_LGPOS'
title: Структура JET_LGPOS
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: e3e83786236a95cf2b0c4d77e26e6987334a5b00
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986157"
---
# <a name="jet_lgpos-structure"></a>Структура JET_LGPOS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_lgpos-structure"></a>Структура JET_LGPOS

Структура **JET_LGPOS** содержит данные, которые являются внутренними по отношению к механизму ведения журнала ядра СУБД. Эта структура считается внутренней.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Элементы

**IB**

Поддерживает инфраструктуру ESE и не может использоваться из кода.

**исек**

Поддерживает инфраструктуру ESE и не может использоваться из кода.

**lGeneration**

Поддерживает инфраструктуру ESE и не может использоваться из кода.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
