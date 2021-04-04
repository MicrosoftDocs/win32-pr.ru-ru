---
description: 'Дополнительные сведения: структура JET_CONVERT'
title: Структура JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: c4e39548b6bcb0a4742b926c1b618b9cc899c2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897953"
---
# <a name="jet_convert-structure"></a>Структура JET_CONVERT


_**Применимо к:** Windows | Windows Server_

## <a name="jet_convert-structure"></a>Структура JET_CONVERT

Структура **JET_CONVERT** содержит имя более ранней библиотеки DLL версии ESE, которая используется для чтения баз данных, созданных с использованием более ранней версии. Кроме того, предоставляются другие флаги для управления природой преобразования.

**Windows Server 2003:** Функция в [жеткомпакт](./jetcompact-function.md) , которая выполнила преобразование, была удалена из продукта в Windows Server 2003. Она поддерживается только в Windows 2000 и Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Элементы

**сзолддлл**

Имя, включая сведения о пути, к более ранней версии библиотеки DLL ESE.

**ффлагс**

Зарезервировано для системного использования.

**фсчемачанжесонли**

Зарезервировано для системного использования.

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
<td><p>Реализуется как <strong>JET_CONVERT_W</strong> (Юникод) и <strong>JET_CONVERT_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[жеткомпакт](./jetcompact-function.md)
