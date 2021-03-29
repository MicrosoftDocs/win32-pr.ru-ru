---
description: 'Дополнительные сведения: JET_DBID'
title: JET_DBID
TOCTitle: JET_DBID
ms:assetid: 516acb79-aa75-4609-81b6-3b2e4e0c95af
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269248(v=EXCHG.10)
ms:contentKeyID: 32765550
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
ms.openlocfilehash: fe3a8ccd813ececcb42388c7d577f78e9055d5b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809682"
---
# <a name="jet_dbid"></a>JET_DBID


_**Применимо к:** Windows | Windows Server_

## <a name="jet_dbid"></a>JET_DBID

Тип данных **JET_DBID** содержит обработчик для базы данных. Для управления схемой базы данных используется маркер базы данных. Его также можно использовать для управления таблицами в этой базе данных.

```cpp
    typedef unsigned long JET_DBID;
```

### <a name="data-types"></a>Типы данных

JET_DBID

Обработчик для базы данных.

Значение JET_dbidNil указывает, что маркер является недопустимым.

### <a name="remarks"></a>Комментарии

Маркер базы данных создается с помощью вызова [жеткреатедатабасе](./jetcreatedatabase-function.md) или [жетопендатабасе](./jetopendatabase-function.md).

Маркер базы данных может быть явно закрыт [жетклоседатабасе](./jetclosedatabase-function.md) или неявно закрыт [жетендсессион](./jetendsession-function.md) или [жеттерм](./jetterm-function.md).

Маркер базы данных может использоваться только в том сеансе, в котором он был создан. Наличие маркера базы данных соответствует логическому открытию базы данных. Логическое открытие отличается от физического открытия базы данных, что происходит при присоединении базы данных к системе.

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

[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жетендсессион](./jetendsession-function.md)
