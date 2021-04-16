---
description: 'Дополнительные сведения: JET_API_PTR'
title: JET_API_PTR
TOCTitle: JET_API_PTR
ms:assetid: 27b1eeec-1707-4edb-a4b2-2619190c21e7
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269209(v=EXCHG.10)
ms:contentKeyID: 32765512
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
ms.openlocfilehash: 687f28fcba3d20c5b72a3089d3a442dd97e2dfb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712737"
---
# <a name="jet_api_ptr"></a>JET_API_PTR


_**Применимо к:** Windows | Windows Server_

## <a name="jet_api_ptr"></a>JET_API_PTR

**JET_API_PTR** тип данных содержит целое число или значение указателя.

```cpp
    #if defined(_WIN64)
        typedef unsigned __int64 JET_API_PTR;
    #elif !defined(__midl) && (defined(_X86_) || defined(_M_IX86)) && _MSC_VER >= 1300
        typedef __w64 unsigned long JET_API_PTR;
    #else
        typedef unsigned long JET_API_PTR;
    #endif
```

### <a name="data-types"></a>Типы данных

JET_API_PTR

Как и **DWORD_PTR** тип данных, **JET_API_PTR** тип данных определяется как 4 байта на 32-разрядном компьютере и 8 байт на 64-разрядном компьютере.

### <a name="remarks"></a>Комментарии

Тип данных **JET_API_PTR** используется для определения следующих типов данных:

  - [JET_HANDLE](./jet-handle.md)

  - [JET_INSTANCE](./jet-instance.md)

  - [JET_SESID](./jet-sesid.md)

  - [JET_TABLEID](./jet-tableid.md)

  - [JET_LS](./jet-ls.md)

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
