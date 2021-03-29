---
description: 'Дополнительные сведения: структура JET_INSTANCE_INFO'
title: Структура JET_INSTANCE_INFO
TOCTitle: JET_INSTANCE_INFO Structure
ms:assetid: 8cdd2e48-f1bb-465b-aefc-ffe441bf88a1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269331(v=EXCHG.10)
ms:contentKeyID: 32765621
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd07d11a8b30e75f30bc5bfcaa3aca665baf1209
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912999"
---
# <a name="jet_instance_info-structure"></a>Структура JET_INSTANCE_INFO


_**Применимо к:** Windows | Windows Server_

## <a name="jet_instance_info-structure"></a>Структура JET_INSTANCE_INFO

Структура **JET_INSTANCE_INFO** получает сведения о выполняемых экземплярах базы данных при использовании с функциями [жетжетинстанцеинфо](./jetgetinstanceinfo-function.md) и [жетосснапшотфризе](./jetossnapshotfreeze-function.md) .

```cpp
    typedef struct _JET_INSTANCE_INFO {
      JET_INSTANCE hInstanceId;
      tchar* szInstanceName;
      JET_API_PTR cDatabases;
      tchar** szDatabaseFileName;
      tchar** szDatabaseDisplayName;
      tchar** szDatabaseSLVFileName;
    } JET_INSTANCE_INFO;
```

### <a name="members"></a>Элементы

**хинстанцеид**

[JET_INSTANCE](./jet-instance.md) заданного экземпляра.

**сзинстанценаме**

Имя экземпляра базы данных. Это значение может быть **равно NULL** , если у экземпляра нет имени.

**cDatabase**

Число баз данных, присоединенных к экземпляру базы данных. Кроме того, **CDatabase** содержит размер массивов строк, возвращаемых в **сздатабасефиленаме**, **сздатабаседисплайнаме** и **сздатабасеслвфиленаме**.

**сздатабасефиленаме**

Массив строк, содержащий имя файла базы данных, присоединенной к экземпляру базы данных. Массив содержит элементы **CDatabase** .

**сздатабаседисплайнаме**

Массив строк, содержащий отображаемое имя базы данных. В настоящее время строка может иметь значение NULL. Массив содержит элементы **CDatabase** .

**сздатабасеслвфиленаме**

Массив строк, содержащий имя файла файла SLV, присоединенного к экземпляру базы данных. Массив содержит элементы **CDatabase** . Файлы SLV не поддерживаются, поэтому это поле следует игнорировать.

### <a name="remarks"></a>Комментарии

К каждому экземпляру базы данных может быть присоединено несколько баз данных.

Для данной структуры **JET_INSTANCE_INFO** массив строк, возвращаемых для баз данных, находится в том же порядке. Например, "Сздатабаседисплайнаме \[ i \] " и "сздатабасефиленаме \[ i \] " ссылаются на одну и ту же базу данных.

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
<td><p>Реализуется как <strong>JET_INSTANCE_INFO_W</strong> (Юникод) и <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетжетинстанцеинфо](./jetgetinstanceinfo-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)
