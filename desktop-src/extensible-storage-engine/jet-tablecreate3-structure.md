---
description: 'Дополнительные сведения: структура JET_TABLECREATE3'
title: Структура JET_TABLECREATE3
TOCTitle: JET_TABLECREATE3 Structure
ms:assetid: 61909569-e704-494b-a56d-b64d1a2ee157
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269264(v=EXCHG.10)
ms:contentKeyID: 32765566
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64f820b9e9a42099cdb99d8ab8f0756e8fdbb23256917821d05573afd9068017
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979244"
---
# <a name="jet_tablecreate3-structure"></a>Структура JET_TABLECREATE3


_**Применимо к:** Windows | Windows Сервером_

структура **JET_TABLECREATE3** содержит сведения, необходимые для создания таблицы, заполненной столбцами и индексами в базе данных ESE (Extensible служба хранилища Engine), которая обозначает функцию обратного вызова. Структура **JET_TABLECREATE3** используется функцией [JetCreateTableColumnIndex3](./jetcreatetablecolumnindex3-function.md) .

структура **JET_TABLECREATE3** была введена в операционной системе Windows 7.

``` cpp
typedef struct tagJET_TABLECREATE3 {
  unsigned long cbStruct;
  tchar* szTableName;
  tchar* szTemplateTableName;
  unsigned long ulPages;
  unsigned long ulDensity;
  JET_COLUMNCREATE* rgcolumncreate;
  unsigned long cColumns;
    JET_INDEXCREATE2* rgindexcreate;
  unsigned long cIndexes;
  tchar* szCallback;
  JET_CBTYP cbtyp;
  JET_GRBIT grbit;
  JET_TABLEID tableid;
  un  JET_GRBIT grbit;
  JET_SPACEHINTS* pSeqSpacehints;
  JET_SPACEHINTS* pLVSpacehints;
  unsigned long cbSeparateLV;
  JET_TABLEID tableid;
  unsigned long cCreated;
} JET_TABLECREATE3;>
```

### <a name="members"></a>Элементы

**кбструкт**

Размер этой структуры в байтах (для будущего расширения). Он должен иметь значение sizeof (JET_TABLECREATE3) в байтах.

**сзтабленаме**

Имя создаваемой таблицы.

Имя должно соответствовать следующим условиям.

  - Значение должно быть меньше JET_cbNameMost, не включая завершающее значение null.

  - Он должен состоять из следующего набора символов: от 0 до 9, от A до Z, от a до z и всех остальных знаков препинания, кроме восклицательного знака ( \! ), запятой (,), открывающей квадратной скобки ( \[ ) и закрывающей скобки ( \] );

  - Оно не должно начинаться с пробела.

  - Оно должно состоять по крайней мере из одного символа, не являющегося пробелом.

**сзтемплатетабленаме**

Имя существующей таблицы, из которой наследуется базовый язык описания данных (DDL). Использование таблицы шаблонов позволяет легко создавать множество таблиц с одинаковыми столбцами и индексами.

**улпажес**

Начальное число страниц базы данных, выделяемых для таблицы. Указание числа больше единицы может сократить фрагментацию, если в эту таблицу вставлено много строк.

**улденсити**

Плотность таблицы в процентных точках. Число должно быть либо 0, либо находиться в диапазоне от 20 до 100. Передача значения 0 означает, что должно использоваться значение по умолчанию. Значение по умолчанию равно 80.

**ргколумнкреате**

Массив структур [JET_COLUMNCREATE](./jet-columncreate-structure.md) , каждый из которых соответствует столбцу, создаваемому в новой таблице.

**кколумнс**

Число элементов [JET_COLUMNCREATE](./jet-columncreate-structure.md) в параметре *ргколумнкреате* .

**ргиндекскреате**

Массив структур [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , каждый из которых соответствует индексу, создаваемому в новой таблице.

**Циндексес**

Число элементов [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) в параметре *ргиндекскреате* .

**сзкаллбакк**

Функция, которая вызывается во время определенных событий. **кбтип** определяет, когда будет вызвана функция обратного вызова.

Формат **сзкаллбакк** должен быть " \! функция модуля", например "Альфа \! -версия" — бета-функция в модуле с именем "Alpha".

Прототип функции должен соответствовать функции обратного вызова [JET_CALLBACK](./jet-callback-callback-function.md) .

**кбтип**

Описывает тип функции обратного вызова, обозначенной **сзкаллбакк**. Дополнительные сведения см. в разделе [JET_CBTYP](./jet-cbtyp.md).

Это битовое значение состоит из одного или нескольких битовых значений, перечисленных в следующей таблице.

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
<td><p>Функция обратного вызова будет вызываться после завершения вставки записи ядром СУБД.</p></td>
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
<td><p>Функция обратного вызова будет вызвана до удаления записи.</p></td>
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
<td><p>JET_cbtypFreeCursorLS</p></td>
<td><p>Функция обратного вызова будет вызываться, когда необходимо освободить локальное хранилище, связанное с курсором.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbtypFreeTableLS</p></td>
<td><p>Функция обратного вызова будет вызываться, когда локальное хранилище, связанное с таблицей, должно быть освобождено.</p></td>
</tr>
</tbody>
</table>


**грбит**

Группа битов, содержащая ноль или более значений параметров вызова, перечисленных в следующей таблице.

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
<td><p>Предотвращает выполнение DDL-операций в таблице (например, добавление или удаление столбцов).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTableCreateTemplateTable</p></td>
<td><p>Приводит к тому, что таблица будет таблицей шаблонов. Новые таблицы могут затем указать имя этой таблицы в качестве таблицы шаблонов. Параметр JET_bitTableCreateTemplateTable подразумевает JET_bitTableCreateFixedDDL.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTableCreateNoFixedVarColumnsInDerivedTables</p></td>
<td><p>Должен использоваться в сочетании с JET_bitTableCreateTemplateTable. Не рекомендуется. Не используется.</p></td>
</tr>
</tbody>
</table>


**псекспацехинтс**

Указатель на структуру [JET_SPACEHINTS](./jet-spacehints-structure.md) для последовательного индекса по умолчанию.

**псекспацехинтс** был введен в Windows 7.

**плвспацехинтс**

Указатель на структуру [JET_SPACEHINTS](./jet-spacehints-structure.md) для разделенного дерева длинного значения.

**плвспацехинтс** был введен в Windows 7.

**кбсепарателв**

Размер для отделения встроенной функции LV от основной записи. Любая структура с длинным значением c для разделенного дерева LV. Дополнительные сведения см. в разделе NG-value в [JET_SPACEHINTS](./jet-spacehints-structure.md). Столбцы с длинными значениями меньше этого значения могут быть разделены, если запись становится слишком большой.

**кбсепарателв** был введен в Windows 7.

**TableID**

Поле вывода, которое содержит [JET_TABLEID](./jet-tableid.md) новой таблицы, если вызов API выполнен. Если вызов API завершается неудачей, значение не определено. Эта таблица открыта только для использования.

**ккреатед**

Поле вывода, содержащее количество объектов, создаваемых при успешности вызова API. Если вызов API завершается неудачей, значение не определено.

Количество создаваемых объектов равно сумме столбцов, таблиц и индексов, которые были успешно созданы.

### <a name="requirements"></a>Requirements (Требования)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008 или Windows server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JET_TABLECREATE3_W</strong> (Юникод) и <strong>JET_TABLECREATE3_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также раздел

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
