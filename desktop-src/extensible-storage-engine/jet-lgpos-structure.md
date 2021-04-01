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
ms.openlocfilehash: 25f00c73a4bb922a8152335babe222b539c70ade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081193"
---
# <a name="jet_lgpos-structure"></a>Структура JET_LGPOS


_**Применимо к:** Windows | Windows Server_

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

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
