---
description: 'Дополнительные сведения: структура JET_INDEXID'
title: Структура JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
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
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713150"
---
# <a name="jet_indexid-structure"></a>Структура JET_INDEXID


_**Применимо к:** Windows | Windows Server_

## <a name="jet_indexid-structure"></a>Структура JET_INDEXID

Структура **JET_INDEXID** содержит идентификатор индекса. Идентификатор индекса — это указание, которое используется для ускорения выбора текущего индекса с помощью [жетсеткуррентиндекс](./jetsetcurrentindex-function.md). Это наиболее полезно при наличии очень большого количества индексов в таблице. Идентификатор индекса можно получить с помощью [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер идентификатора индекса в байтах.

Это фактический размер идентификатора индекса, возвращаемого в выходном буфере из [жетжетиндексинфо](./jetgetindexinfo-function.md) или [жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md).

**ргбиндексид**

Непрозрачный большой двоичный объект данных, используемый ядром для быстрого обнаружения индекса в его кэше схемы.

Не пытайтесь интерпретировать большой двоичный объект данных. Размер не является установленным.

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

[жетжетиндексинфо](./jetgetindexinfo-function.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)  
[жетжеттаблеинфо](./jetgettableinfo-function.md)  
[жетсеткуррентиндекс](./jetsetcurrentindex-function.md)
