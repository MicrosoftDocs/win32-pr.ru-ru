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
ms.openlocfilehash: d6210853e22fda5085980c2fb285411ba431bb43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692516"
---
# <a name="jet_signature-structure"></a>Структура JET_SIGNATURE


_**Применимо к:** Windows | Windows Server_

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

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)
