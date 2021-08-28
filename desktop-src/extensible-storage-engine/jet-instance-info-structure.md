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
ms.openlocfilehash: 6dbeab994d012f031de7620487c754b69d00db3d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472700"
---
# <a name="jet_instance_info-structure"></a>Структура JET_INSTANCE_INFO


_**Применимо к:** Windows | Windows Сервером_

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


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JET_INSTANCE_INFO_W</strong> (Юникод) и <strong>JET_INSTANCE_INFO _A</strong> (ANSI).</p> | 



### <a name="see-also"></a>См. также:

[JET_API_PTR](./jet-api-ptr.md)  
[JET_INSTANCE](./jet-instance.md)  
[жетжетинстанцеинфо](./jetgetinstanceinfo-function.md)  
[жетосснапшотфризе](./jetossnapshotfreeze-function.md)
