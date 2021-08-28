---
description: 'Дополнительные сведения: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: 7aa3a0331244aa1f5dd07794204d5a94d57aeadb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984177"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_grbit"></a>JET_GRBIT

**JET_GRBIT** тип данных — это группа битов, которая содержит константы, характерные для функций и структур, в которых она используется.

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a>Типы данных

JET_GRBIT

Как правило, константы, используемые в качестве значений для этого типа данных, соответствуют имени элемента API, в котором они используются. Например, все константы, передаваемые в [жетретриевеколумн](./jetretrievecolumn-function.md) , начинаются с "JET_bitRetrieve". Аналогичным образом все константы, передаваемые в [жетсетколумн](./jetsetcolumn-function.md) , начинаются с "JET_bitSet".

Нулевое значение приводит к тому, что параметр игнорируется.

### <a name="remarks"></a>Комментарии

Дополнительные сведения см. в описании конкретной функции или структуры. Параметры обычно передаются в виде набора флагов, которые можно комбинировать.

### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетсетколумн](./jetsetcolumn-function.md)
