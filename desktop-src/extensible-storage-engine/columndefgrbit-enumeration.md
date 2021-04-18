---
description: Дополнительные сведения о перечислении Колумндефгрбит
title: Перечисление Колумндефгрбит
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711332"
---
# <a name="columndefgrbit-enumeration"></a>Перечисление Колумндефгрбит

Параметры структуры JET_COLUMNDEF.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
```

## <a name="members"></a>Члены

<table>
<thead>
<tr class="header">
<th></th>
<th>Имя участника</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Нет</td>
<td>Параметры по умолчанию.</td>
</tr>
<tr class="even">
<td></td>
<td>колумнфиксед</td>
<td>Столбец будет исправлен. Он всегда будет использовать один и тот же объем пространства в строке независимо от объема данных, сохраняемых в столбце. Колумнфиксед нельзя использовать с Колумнтагжед. Этот бит не может использоваться с длинными значениями (то есть JET_coltyp. LongText и JET_coltyp. Лонгбинари).</td>
</tr>
<tr class="odd">
<td></td>
<td>колумнтагжед</td>
<td>Столбец будет помечен как. Помеченные столбцы не занимают место в базе данных, если они не содержат данных. Этот бит нельзя использовать с Колумнфиксед.</td>
</tr>
<tr class="even">
<td></td>
<td>колумннотнулл</td>
<td>Для этого столбца никогда не должно быть задано значение NULL. В Windows XP это можно применить только к фиксированным столбцам (бит, байт, целое число и т. д.).</td>
</tr>
<tr class="odd">
<td></td>
<td>колумнверсион</td>
<td>Столбец представляет собой столбец версии, указывающий версию строки. Значение этого столбца начинается с нуля и будет автоматически увеличиваться для каждого обновления в строке. Этот параметр можно применить только к JET_coltyp. Столбцы типа long. Этот параметр нельзя использовать с Колумнаутоинкремент, Колумнескровупдате или Колумнтагжед.</td>
</tr>
<tr class="even">
<td></td>
<td>колумнаутоинкремент</td>
<td>Столбец будет автоматически увеличиваться. Число является увеличивающимся числом и гарантированно уникально в пределах таблицы. Однако числа могут не быть непрерывными. Например, если в таблицу вставляются пять строк, &quot; &quot; столбец AutoIncrement может содержать значения {1, 2, 6, 7, 8}. Этот бит можно использовать только для столбцов типа JET_coltyp. Long или JET_coltyp. Режиме.</td>
</tr>
<tr class="odd">
<td></td>
<td>колумнмултивалуед</td>
<td>Столбец может иметь несколько значений. Столбец с несколькими значениями может иметь ноль, одно или несколько связанных с ним значений. Различные значения в столбце с несколькими значениями идентифицируются по числу, называемому элементом Итагсекуенце, который относится к различным структурам, включая: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN и JET_ENUMCOLUMNVALUE. Столбцы с несколькими значениями должны быть помечены как столбцы. Это значит, что они не могут быть столбцами фиксированной длины или переменной длины.</td>
</tr>
<tr class="even">
<td></td>
<td>колумнескровупдате</td>
<td>Указывает, что столбец является столбцом депонирования обновлений. Столбец депонированного обновления может обновляться параллельно разными сеансами с Жетескровупдате и поддерживать согласованность транзакций. Столбец депонированного обновления должен также соответствовать следующим условиям: столбец депонированного обновления может быть создан только в том случае, если таблица пуста. Столбец депонированного обновления должен иметь тип JET_coltypLong. Столбец депонированного обновления должен иметь значение по умолчанию. JET_bitColumnEscrowUpdate нельзя использовать в сочетании с Колумнтагжед, Колумнверсион или Колумнаутоинкремент.</td>
</tr>
<tr class="odd">
<td></td>
<td>колумнунверсионед</td>
<td>Столбец будет создан в без сведений о версии. Это означает, что другие транзакции, пытающиеся добавить столбец с тем же именем, завершатся ошибкой. Этот бит удобен только для Жетаддколумн. Его нельзя использовать в транзакции.</td>
</tr>
<tr class="even">
<td></td>
<td>колумнмайбенулл</td>
<td>При выполнении внешнего объединения операция получения столбца может не иметь соответствия во внутренней таблице.</td>
</tr>
<tr class="odd">
<td></td>
<td>колумнусердефинеддефаулт</td>
<td>Значение по умолчанию для столбца будет предоставлено функцией обратного вызова. Столбец, содержащий определяемое пользователем значение по умолчанию, должен быть столбцом с тегами. Указание JET_bitColumnUserDefinedDefault означает, что Пвдефаулт должен указывать на структуру JET_USERDEFINEDDEFAULT, а для Кбдефаулт должно быть задано значение sizeof (JET_USERDEFINEDDEFAULT).</td>
</tr>
<tr class="even">
<td></td>
<td>тткэй</td>
<td>Столбец будет ключевым столбцом для временной таблицы. Порядок определений столбцов с этим параметром, указанным во входном массиве, определяет приоритет каждого ключевого столбца для временной таблицы. Первое определение столбца в массиве, для которого задан этот параметр, будет наиболее значимым ключевым столбцом и т. д. Если запрошено больше ключевых столбцов, чем может поддерживать ядро СУБД, этот параметр игнорируется для неподдерживаемых ключевых столбцов.</td>
</tr>
<tr class="odd">
<td></td>
<td>ттдесцендинг</td>
<td>Порядок сортировки ключевого столбца для временной таблицы должен быть по убыванию, а не по возрастанию. Если этот параметр указан без Тткэй, этот параметр игнорируется.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[колумнкомпрессед](./windows7grbits.columncompressed-field.md)
