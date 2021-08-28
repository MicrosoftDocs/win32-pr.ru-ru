---
description: 'Дополнительные сведения: структура JET_BKINFO'
title: Структура JET_BKINFO
TOCTitle: JET_BKINFO Structure
ms:assetid: dfaf1d72-1d5f-4777-91c1-6affb735b092
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294120(v=EXCHG.10)
ms:contentKeyID: 32765734
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
ms.openlocfilehash: e859d34a610ddcff0431b7395d11c72b01fb8bb7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985287"
---
# <a name="jet_bkinfo-structure"></a>Структура JET_BKINFO


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_bkinfo-structure"></a>Структура JET_BKINFO

Структура **JET_BKINFO** содержит коллекцию данных о конкретном событии резервного копирования.

```cpp
    typedef struct {
      JET_LGPOS lgposMark;
      union {
        JET_LOGTIME logtimeMark;
        JET_BKLOGTIME bklogtimeMark;
      };
      unsigned long genLow;
      unsigned long genHigh;
    } JET_BKINFO;
```

### <a name="members"></a>Элементы

**лгпосмарк**

Идентификатор этой резервной копии.

**логтимемарк**

Время события резервного копирования.

**бклогтимемарк**

Время события резервного копирования с дополнительными битами для указания резервной копии моментального снимка.

**Windows vista: бклогтимемарк** появился в Windows Vista.

**женлов**

Младший номер создания журнала, связанный с этим событием резервного копирования.

**женхигх**

Старший номер создания журнала, связанный с этим событием резервного копирования.

### <a name="remarks"></a>Комментарии

Эта структура используется в структуре [JET_DBINFOMISC](./jet-dbinfomisc-structure.md) для представления данных о событии резервного копирования базы данных.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[JET_LGPOS](./jet-lgpos-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JET_BKLOGTIME](./jet-bklogtime-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
