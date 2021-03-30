---
description: 'Дополнительные сведения: JET_COLUMNID'
title: JET_COLUMNID
TOCTitle: JET_COLUMNID
ms:assetid: d6c74c5c-ba61-4e1c-a1b1-495e925b6b68
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294104(v=EXCHG.10)
ms:contentKeyID: 32765719
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
ms.openlocfilehash: be5b8bb64dc9e0fc42055cf5e4d4f67caa7654bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896730"
---
# <a name="jet_columnid"></a>JET_COLUMNID


_**Применимо к:** Windows | Windows Server_

## <a name="jet_columnid"></a>JET_COLUMNID

Тип данных **JET_COLUMNID** определяет столбец в таблице.

```cpp
    typedef unsigned long JET_COLUMNID;
```

### <a name="data-types"></a>Типы данных

JET_COLUMNID

Определяет столбец в таблице.

### <a name="remarks"></a>Комментарии

Идентификаторы столбцов уникальны в пределах одной таблицы. Когда известно, что столбец имеет определенный идентификатор столбца, он всегда будет иметь идентификатор столбца. При восстановлении из резервной копии не изменится значение идентификатора столбца. Однако при удалении одного или нескольких столбцов таблицы, предшествовавших определенному столбцу таблицы, база данных Compact может изменить значение идентификатора столбца.

В некоторых случаях идентификаторы столбцов являются единственным средством идентификации столбцов. При создании временной таблицы ее столбцы не имеют имен, но массив идентификаторов столбцов возвращается функцией Create.

Столбцы в разных таблицах могут иметь один и тот же идентификатор столбца.

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

