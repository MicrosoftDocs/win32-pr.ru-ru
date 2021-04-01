---
description: 'Дополнительные сведения: структура JET_TABLECREATE2'
title: Структура JET_TABLECREATE2
TOCTitle: JET_TABLECREATE2 Structure
ms:assetid: 2029e684-0d10-44e7-8033-d9cdbdffd7a4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269203(v=EXCHG.10)
ms:contentKeyID: 32765506
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
ms.openlocfilehash: d7ce983d393954c0d82f0d4e43108ff845d31571
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913755"
---
# <a name="jet_tablecreate2-structure"></a>Структура JET_TABLECREATE2


_**Применимо к:** Windows | Windows Server_

## <a name="jet_tablecreate2-structure"></a>Структура JET_TABLECREATE2

Структура **JET_TABLECREATE2** содержит сведения, необходимые для создания таблицы, заполненной столбцами и индексами в базе данных ESE, которая обозначает функцию обратного вызова. Структура **JET_TABLECREATE2** используется [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).

**Windows XP:** Структура **JET_TABLECREATE2** появилась в Windows XP.

```cpp
    typedef struct tagJET_TABLECREATE2 {
      unsigned long cbStruct;
      tchar* szTableName;
      tchar* szTemplateTableName;
      unsigned long ulPages;
      unsigned long ulDensity;
      JET_COLUMNCREATE* rgcolumncreate;
      unsigned long cColumns;
      JET_INDEXCREATE* rgindexcreate;
      unsigned long cIndexes;
      tchar* szCallback;
      JET_CBTYP cbtyp;
      JET_GRBIT grbit;
      JET_TABLEID tableid;
      unsigned long cCreated;
    } JET_TABLECREATE2;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер этой структуры в байтах (для будущего расширения). Он должен иметь значение sizeof (JET_TABLECREATE2) в байтах.

**сзтабленаме**

Имя создаваемой таблицы.

Имя должно соответствовать следующим условиям:

  - Иметь значение меньше JET_cbNameMost, не включая завершающее значение NULL.

<!-- end list -->

  - Состоит из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей квадратной скобки ( \] ), то есть символов ASCII 0x20, 0x22 через 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.

<!-- end list -->

  - Не должно начинаться с пробела.

<!-- end list -->

  - Состоит по крайней мере один символ, не являющийся пробелом.

**сзтемплатетабленаме**

Имя уже существующей таблицы, из которой наследуются базовые DDL (язык описания данных). Использование таблицы шаблонов позволяет легко создавать множество таблиц с одинаковыми столбцами и индексами.

**улпажес**

Начальное число страниц базы данных, выделяемых для таблицы. Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.

**улденсити**

Плотность таблицы в процентных точках. Число должно быть либо 0, либо находиться в диапазоне от 20 до 100. Передача значения 0 означает, что должно использоваться значение по умолчанию. Значение по умолчанию — 80.

**ргколумнкреате**

Массив структур [JET_COLUMNCREATE](./jet-columncreate-structure.md) , каждый из которых соответствует столбцу, создаваемому в новой таблице.

**кколумнс**

число элементов [JET_COLUMNCREATE](./jet-columncreate-structure.md) в **ргколумнкреате**.

**ргиндекскреате**

Массив структур [JET_INDEXCREATE](./jet-indexcreate-structure.md) , каждый из которых соответствует индексу, создаваемому в новой таблице.

**Циндексес**

Число элементов [JET_INDEXCREATE](./jet-indexcreate-structure.md) в **ргиндекскреате**.

**сзкаллбакк**

Функция, которая вызывается во время определенных событий. **кбтип** определяет, когда будет вызвана функция обратного вызова.

Формат **сзкаллбакк** должен быть " \! функция модуля", например "Альфа \! -версия" — бета-функция в модуле с именем "Alpha". Прототип функции должен соответствовать [JET_CALLBACK](./jet-callback-callback-function.md). Дополнительные сведения см. в разделе [JET_CALLBACK](./jet-callback-callback-function.md).

**кбтип**

Описывает тип функции обратного вызова, обозначенной **сзкаллбакк**. Дополнительные сведения см. в разделе [JET_CBTYP](./jet-cbtyp.md). Это битовое поле состоит из одного или нескольких следующих битов.

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
<td><p>JET_cbtypFinalize</p></td>
<td><p>Функция обратного вызова вызывается, когда столбец, который может быть завершен, имеет нулевое значение.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeInsert</p></td>
<td><p>Перед вставкой записи будет вызвана функция обратного вызова.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterInsert</p></td>
<td><p>Функция обратного вызова будет вызываться по завершении вставки записи ядром СУБД.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeReplace</p></td>
<td><p>Функция обратного вызова будет вызвана до изменения записи.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterReplace</p></td>
<td><p>Функция обратного вызова будет вызвана после завершения изменения записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypBeforeDelete</p></td>
<td><p>Перед удалением записи будет вызвана функция обратного вызова.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypAfterDelete</p></td>
<td><p>Функция обратного вызова будет вызвана после удаления записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypUserDefinedDefaultValue</p></td>
<td><p>Функция обратного вызова будет вызываться для вычисления определяемого пользователем значения по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypOnlineDefragCompleted</p></td>
<td><p>Функция обратного вызова будет вызываться после завершения вызова <a href="gg294095(v=exchg.10).md">JetDefragment2</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>Функция обратного вызова будет вызываться, когда необходимо освободить локальное хранилище, связанное с курсором.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>Функция обратного вызова будет вызываться, когда локальное хранилище, связанное с таблицей, должно быть освобождено.</p></td>
</tr>
</tbody>
</table>


**грбит**

Группа битов, содержащая параметры для этого вызова, которые содержат ноль или более следующих значений.

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
<td><p>JET_bitTableCreateFixedDDL</p></td>
<td><p>Параметр JET_bitTableCreateFixedDDL предотвращает выполнение DDL-операций в таблице (например, добавление или удаление столбцов).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Параметр JET_bitTableCreateTemplateTable приводит к тому, что таблица будет таблицей шаблонов. Новые таблицы могут затем указать имя этой таблицы в качестве таблицы шаблонов. Параметр JET_bitTableCreateTemplateTable подразумевает JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Должен использоваться в сочетании с JET_bitTableCreateTemplateTable. Не рекомендуется. Не используется.</p></td>
</tr>
</tbody>
</table>


**TableID**

Поле вывода, которое содержит [JET_TABLEID](./jet-tableid.md) новой таблицы, если вызов API выполнен. Если вызов API завершается неудачей, значение не определено.

**ккреатед**

Поле вывода, содержащее количество объектов, создаваемых при успешности вызова API. Если вызов API завершается неудачей, значение не определено.

Число создаваемых объектов равно сумме столбцов, таблиц и индексов, которые были успешно созданы.

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JET_TABLECREATE2_W</strong> (Юникод) и <strong>JET_TABLECREATE2_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TABLEID](./jet-tableid.md)  
[жеткреатетабле](./jetcreatetable-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JetDefragment2](./jetdefragment2-function.md)
