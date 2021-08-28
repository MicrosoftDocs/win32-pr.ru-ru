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
ms.openlocfilehash: 92fa6dffd94d2a1790811881fcdba86665ebb880
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482250"
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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 



### <a name="see-also"></a>См. также:

[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетсетколумн](./jetsetcolumn-function.md)
