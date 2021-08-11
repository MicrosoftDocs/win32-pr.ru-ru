---
description: 'Дополнительные сведения: структура JET_SPACEHINTS'
title: Структура JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
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
ms.openlocfilehash: f829e78ff54e77011346ae1bfd39f909411cbee12c18d19781f8fe5d62865097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252259"
---
# <a name="jet_spacehints-structure"></a>Структура JET_SPACEHINTS


_**Применимо к:** Windows | Windows Сервером_

## <a name="jet_spacehints-structure"></a>Структура JET_SPACEHINTS

Структура **JET_SPACEHINTS** содержит сведения о шаблонах выделения пространства, когда сбалансированное дерево растет через разбиение или хотпоинт. Разбиение на страницы происходит, когда записи добавляются в конец сбалансированного дерева, а разбиение хотпоинт происходит, когда несколько записей добавляются в одну и ту же виртуальную точку вставки (например, при добавлении "Марие", "Mark", "Мартин'", "Mary" в середину сбалансированного дерева, отсортированного в алфавитном порядке).

**Windows 7:** структура **JET_SPACEHINTS** введена в Windows 7.

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер данной структуры (в байтах). Присвойте этому элементу значение sizeof (JET_SPACEHINTS).

**улинитиалденсити**

Схема плотности в (добавление).

**кбинитиал**

Начальный размер создаваемого объекта (в байтах). Это должен быть кратный размер страницы базы данных.

**грбит**

Группа битов, содержащая параметры, которые должны использоваться для этой структуры, включая ноль или более следующих элементов.

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
<td><p>JET_bitSpaceHintsUtilizeParentSpace<br />
0x00000001</p></td>
<td><p>Изменяет внутреннюю политику выделения для получения хеирарчикалли пространства от непосредственного родителя сбалансированного дерева.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateHintAppendSequential<br />
0x00000002</p></td>
<td><p>Включает поведение раздельного разбиения для увеличения в соответствии с Dynamics of таблицы (задается Кбминекстент, Улгровс, Кбмаксекстент).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitCreateHintHotpointSequential<br />
0x00000004</p></td>
<td><p>Обеспечивает увеличение поведения хотпоинт Split в соответствии с Dynamics of в таблице (устанавливается параметрами Кбминекстент, Улгровс, Кбмаксекстент).</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveHintTableScanForward<br />
0x00000010</p></td>
<td><p>Если этот параметр задан, клиент указывает, что в качестве основного шаблона использования этой таблицы используется прямая последовательная проверка.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveHintTableScanBackward<br />
0x00000020</p></td>
<td><p>Если задано значение, клиент указывает, что для этой таблицы используется обратная последовательная проверка.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDeleteHintTableSequential<br />
0x00000100</p></td>
<td><p>Если задано, приложение ждет, что эта таблица будет очищена в последовательном порядке, от наименьшего ключа к наибольшему.</p></td>
</tr>
</tbody>
</table>


**улмаинтденсити**

плотность к Мулмаинтденсити

Плотность для обслуживания в. Если в указаниях по пространству указано JET_bitRetrieveHintTableScanForward или JET_bitRetrieveHintTableScanBackward, Дефрагментация таблицы будет срабатывать, когда используемое место в таблице станет меньше этого порогового значения. Дефрагментацию таблицы можно отключить, установив для этого члена значение 0. Если установить этот элемент в значение 100, Дефрагментация таблицы будет выполняться сразу после высвобождения страницы.

**улгровс**

Процент роста с последнего роста или исходного размера, округленный до ближайшего размера выделения для собственного модуля JET.

**Кбминекстент слишком мал**

Это переопределяет Улгровс, если слишком мал.

**кбмаксекстент**

Максимальное значение для увеличения в байтах. Эти политики Улгровс.

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>При увеличении сбалансированного дерева с помощью операций Append или хотпоинт (в отличие от вставки случайных записей) объем пространства, на который будет расти таблица, вычисляется следующим образом:

1.  При создании мы дадим сбалансированное дерево Кбинитиал, всегда.

2.  При первом выделении данной области мы выделим: Кбинитиал \* улгровс/100 (округленный до размера страницы базы данных) или кбминекстент, если больше.

3.  При следующем выделении Кбласталлок \* улгровс/100 (округленный до размера страницы базы данных) или кбминекстент, если больше.

4.  При выделении (которое может быть первым выделением) Вычисленный размер будет превысить Кбмаксекстент, а это будет размер роста.

### <a name="requirements"></a>Требования

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
<td><p><strong>Server</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также:

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
