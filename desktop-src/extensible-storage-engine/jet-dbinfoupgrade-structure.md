---
description: 'Дополнительные сведения: структура JET_DBINFOUPGRADE'
title: Структура JET_DBINFOUPGRADE
TOCTitle: JET_DBINFOUPGRADE Structure
ms:assetid: dd8a881a-33b5-4314-8cfb-b1d75ad37b21
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294114(v=EXCHG.10)
ms:contentKeyID: 32765728
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
ms.openlocfilehash: 9652b0050805ad116a7087cb2ec4cd146255b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682669"
---
# <a name="jet_dbinfoupgrade-structure"></a>Структура JET_DBINFOUPGRADE


_**Применимо к:** Windows | Windows Server_

## <a name="jet_dbinfoupgrade-structure"></a>Структура JET_DBINFOUPGRADE

Структура **JET_DBINFOUPGRADE** содержит сведения о состоянии обновления базы данных. Это значение извлекается, только если **JET_DBINFOUPGRADE** передано в [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md). Эта структура не является обязательной для текущих версий операционной системы ядра СУБД.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cbFilesizeLow;
      unsigned long cbFilesizeHigh;
      unsigned long cbFreeSpaceRequiredLow;
      unsigned long  cbFreeSpaceRequiredHigh;
      unsigned long csecToUpgrade;
      union {
        unsigned long ulFlags;
        struct {
          unsigned long fUpgradable  :1;
          unsigned long fAlreadyUpgraded  :1;
        };
      };
    } JET_DBINFOUPGRADE;
```

### <a name="members"></a>Элементы

**кбструкт**

Задайте размер структуры **JET_DBINFOUPGRADE** в байтах.

**кбфилесизелов**

Нижний **DWORD** , отражающий текущий размер файла базы данных.

**кбфилесизехигх**

Верхний **DWORD** , отражающий текущий размер файла для базы данных.

**кбфриспацерекуиредлов**

Нижний **DWORD** предполагаемого свободного места на диске, необходимый для обновления на месте.

**кбфриспацерекуиредхигх**

Большой **DWORD** предполагаемого свободного места на диске, необходимый для обновления на месте.

**ксектаупграде**

Предполагаемое время, необходимое для обновления, в секундах.

**улфлагс**

Битовое поле, состоящие из одного или нескольких следующих флагов: **фупградабле**, **фалреадюпградед**.

**фупградабле**

База данных обновляема.

**фалреадюпградед**

База данных обновляется до текущего формата базы данных.

### <a name="remarks"></a>Комментарии

Структура **JET_DBINFOUPGRADE** заполняется вызовом [жетжетдатабасеинфо](./jetgetdatabaseinfo-function.md) или [жетжетдатабасефилеинфо](./jetgetdatabasefileinfo-function.md). Если функция не выполнена, содержимое структуры не определено.

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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжетиндексинфо](./jetgetindexinfo-function.md)  
[жетжетобжектинфо](./jetgetobjectinfo-function.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)  
[жетжеттаблеинфо](./jetgettableinfo-function.md)
