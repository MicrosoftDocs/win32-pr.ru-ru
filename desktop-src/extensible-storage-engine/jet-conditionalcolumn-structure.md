---
description: 'Дополнительные сведения: структура JET_CONDITIONALCOLUMN'
title: Структура JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: 870536ff408558332e6a07f91649edb1a17ca2fb0c69ed46fb7171f3505d683e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731154"
---
# <a name="jet_conditionalcolumn-structure"></a>Структура JET_CONDITIONALCOLUMN


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_conditionalcolumn-structure"></a>Структура JET_CONDITIONALCOLUMN

Структура **JET_CONDITIONALCOLUMN** определяет, как выполняется условное индексирование для данного индекса. Условный индекс содержит элемент индекса только для тех строк, которые соответствуют заданному условию. Однако условный столбец не является частью ключа индекса, он только управляет присутствием элемента индекса.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Элементы

**кбструкт**

Это поле должно быть инициализировано в sizeof (JET_CONDITIONALCOLUMN) в байтах.

**сзколумннаме**

Имя столбца, содержащего данные, на которых ядро СУБД выполняет условное индексирование строки.

**грбит** Группа битов, которая предоставляет параметры для условного индекса. Передача нулевых или логических значений (**или** ED) недопустима для **JET_CONDITIONALCOLUMN**. Битовое поле должно быть ровно одним из следующих:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitIndexColumnMustBeNull</p></td>
<td><p>Столбец, указанный параметром <em>сзколумннаме</em> , должен иметь значение NULL для записи индекса, чтобы данная строка отображалась в этом индексе.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexColumnMustBeNonNull</p></td>
<td><p>Столбец, указанный параметром <em>сзколумннаме</em> , должен иметь значение, отличное от NULL, для записи индекса, чтобы данная строка отображалась в этом индексе.</p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a>Remarks

Условный индекс содержит элемент индекса только для тех строк, которые соответствуют заданному условию. Например, столбец может называться "помечен", а если строка помечена, в столбце задается значение, отличное от NULL. В JET_bitIndexColumnMustBeNonNull условном индексе этого столбца будут показаны все отмеченные строки, а в условном индексе JET_bitIndexColumnMustBeNull будут показаны непомеченные строки. Это также удобный способ для удаления флагов и сбора мусора.

### <a name="requirements"></a>Requirements (Требования)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JET_CONDITIONALCOLUMN_W</strong> (Юникод) и <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
