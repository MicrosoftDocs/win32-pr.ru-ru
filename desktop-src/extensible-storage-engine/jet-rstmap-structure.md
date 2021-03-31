---
description: 'Дополнительные сведения: структура JET_RSTMAP'
title: Структура JET_RSTMAP
TOCTitle: JET_RSTMAP Structure
ms:assetid: bddf95e4-1bd4-4e3a-ad3e-d01f6564e33b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294077(v=EXCHG.10)
ms:contentKeyID: 32765692
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
ms.openlocfilehash: 646a055230b6476abf70abcde582fc2015cb241c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809065"
---
# <a name="jet_rstmap-structure"></a>Структура JET_RSTMAP


_**Применимо к:** Windows | Windows Server_

## <a name="jet_rstmap-structure"></a>Структура JET_RSTMAP

Структура **JET_RSTMAP** позволяет переназначить пути к файлам базы данных, которые хранятся в журналах транзакций во время восстановления, при использовании функций [жетинит](./jetinit-function.md) и [жетекстерналресторе](./jetexternalrestore-function.md) . Это позволяет перемещать базы данных в автономном режиме или при восстановлении из резервной копии.

```cpp
    typedef struct {
      xRPC_STRING tchar* szDatabaseName;
      xRPC_STRING tchar* szNewDatabaseName;
    } JET_RSTMAP;
```

### <a name="members"></a>Элементы

**сздатабасенаме**

Текущий абсолютный путь к базе данных, связанной с журналами транзакций, которые воспроизводятся во время восстановления.

**сзневдатабасенаме**

Новый абсолютный путь к базе данных.

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
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JET_RSTMAP_W</strong> (Юникод) и <strong>JET_RSTMAP_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жетекстерналресторе](./jetexternalrestore-function.md)  
[жетинит](./jetinit-function.md)
