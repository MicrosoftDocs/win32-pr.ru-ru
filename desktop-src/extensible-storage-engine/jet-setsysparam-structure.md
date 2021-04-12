---
description: 'Дополнительные сведения: структура JET_SETSYSPARAM'
title: Структура JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342992"
---
# <a name="jet_setsysparam-structure"></a>Структура JET_SETSYSPARAM


_**Применимо к:** Windows | Windows Server_

## <a name="jet_setsysparam-structure"></a>Структура JET_SETSYSPARAM

Массив структур **JET_SETSYSPARAM** указывает конкретный набор глобальных системных параметров, которые задаются в качестве аргумента при использовании функции [жетенаблемултиинстанце](./jetenablemultiinstance-function.md) .

**Windows XP:** Эта структура появилась в Windows XP.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Элементы

**paramid**

Идентификатор системного параметра, который будет установлен.

Полный список системных параметров и их свойств см. в разделе [расширяемые системные параметры](./extensible-storage-engine-system-parameters.md) подсистемы хранилища.

**lParam**

Необязательное значение, устанавливаемое для выбранного системного параметра, если этот системный параметр имеет целочисленный тип.

**SZ**

Необязательное значение, устанавливаемое для выбранного системного параметра, если этот системный параметр имеет строковый тип.

**Err**

Ошибка, полученная в результате вызова метода [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с указанными ранее параметрами.

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
<td><p>Реализуется как <strong>JET_ SETSYSPARAM_W</strong> (Юникод) и <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[Параметры расширяемой системы подсистемы хранилища](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[жетенаблемултиинстанце](./jetenablemultiinstance-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)
