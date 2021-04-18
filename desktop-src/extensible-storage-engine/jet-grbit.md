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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105674761"
---
# <a name="jet_grbit"></a>JET_GRBIT


_**Применимо к:** Windows | Windows Server_

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетсетколумн](./jetsetcolumn-function.md)
