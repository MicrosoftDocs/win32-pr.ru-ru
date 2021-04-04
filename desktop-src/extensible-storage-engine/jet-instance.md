---
description: 'Дополнительные сведения: JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 6e1fde3e01c8328d2fdaf6609c6772fda9cd1428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999059"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**Применимо к:** Windows | Windows Server_

## <a name="jet_instance"></a>JET_INSTANCE

Тип данных **JET_INSTANCE** содержит обработчик для экземпляра базы данных, который используется для вызова API Jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Типы данных

JET_INSTANCE

Для указания недопустимого обработчика экземпляра можно использовать **значение NULL** или [JET_instanceNil](./invalid-handle-constants.md) .

### <a name="remarks"></a>Комментарии

Этот маркер получается при создании экземпляра базы данных путем вызова функций [жеткреатеинстанце](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [жетинит](./jetinit-function.md)или [JetInit2](./jetinit2-function.md) .

**Windows XP:**  Явное использование экземпляров поддерживается только в Windows XP и более поздних версиях.

**Windows 2000:**  Для каждого процесса поддерживается только один глобальный экземпляр.

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

[жеткреатеинстанце](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[жетинит](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
