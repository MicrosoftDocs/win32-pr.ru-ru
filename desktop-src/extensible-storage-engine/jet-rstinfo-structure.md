---
description: 'Дополнительные сведения: структура JET_RSTINFO'
title: Структура JET_RSTINFO
TOCTitle: JET_RSTINFO Structure
ms:assetid: 2f144d68-dcd9-4d0d-9d9e-a7d2a5c350fe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269216(v=EXCHG.10)
ms:contentKeyID: 32765519
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
ms.openlocfilehash: 3a776c84d89dfc97272c65bb0c0684faba814fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144275"
---
# <a name="jet_rstinfo-structure"></a>Структура JET_RSTINFO


_**Применимо к:** Windows | Windows Server_

## <a name="jet_rstinfo-structure"></a>Структура JET_RSTINFO

Структура **JET_RSTINFO** содержит управляющие данные для процесса восстановления, такие как сведения о перерасположении базы данных, а также возможность управления остановкой восстановления.

**Windows Vista:** Структура **JET_RSTINFO** появилась в Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_RSTMAP* rgrstmap;
      long crstmap;
      JET_LGPOS lgposStop;
      JET_LOGTIME logtimeStop;
      JET_PFNSTATUS pfnStatus;
    } JET_RSTINFO;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер структуры.

**ргрстмап**

Структура, описывающая старый и новый пути к восстановленной базе данных.

**крстмап**

Число записей массива в ргрстмап.

**лгпосстоп**

Позиция журнала для отмены восстановления в. Отмена не будет выполнена.

**логтиместоп**

Зарезервировано для последующего использования.

**пфнстатус**

Функция состояния для создания отчета о состоянии восстановления.

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
<td><p>Реализуется как <strong>JET_RSTINFO_W</strong> (Юникод) и <strong>JET_RSTINFO_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JetInit3](./jetinit3-function.md)
