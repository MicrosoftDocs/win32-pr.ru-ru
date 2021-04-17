---
description: Дополнительные сведения о перечислении Темптаблегрбит
title: Перечисление Темптаблегрбит
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682666"
---
# <a name="temptablegrbit-enumeration"></a>Перечисление Темптаблегрбит

Параметры для создания временной таблицы.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
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
<td>Индексированного</td>
<td>Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы позволить использовать Жетсик для поиска записей по ключу индекса. Если эта функция не требуется, то лучше не запрашивать ее. Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</td>
</tr>
<tr class="odd">
<td></td>
<td>Уникальная идентификация</td>
<td>Этот параметр запрашивает удаление записей с повторяющимися ключами индекса из окончательного набора записей во временной таблице. До Windows Server 2003 в ядре СУБД всегда предполагается, что этот параметр действует из-за того факта, что все кластеризованные индексы также должны быть первичным ключом и, таким же, должны быть уникальными. Начиная с Windows Server 2003, теперь можно создать временную таблицу, которая не удаляет дубликаты при указании параметра <a href="dn351284(v=exchg.10).md">форвардонли</a> . Невозможно понять, какие дубликаты будут выдаваться, и какие дубликаты будут отменены в целом. Однако при запросе параметра Ерророндупликатеинсертион первая запись с заданным ключом индекса для вставки во временную таблицу всегда будет выдаваться.</td>
</tr>
<tr class="even">
<td></td>
<td>Обновляется</td>
<td>Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить впоследствии изменять записи, которые были вставлены. Если эта функция не требуется, то лучше не запрашивать ее. Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</td>
</tr>
<tr class="odd">
<td></td>
<td>Прокручиваемые курсоры</td>
<td>Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы можно было просматривать записи в произвольном порядке и в направлении с помощью <a href="dn292217(v=exchg.10).md">жетмове (JET_SESID, JET_TABLEID, Int32, мовегрбит)</a>. Если эта функция не требуется, то лучше не запрашивать ее. Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</td>
</tr>
<tr class="even">
<td></td>
<td>сортнуллшигх</td>
<td>При выборе этого варианта значения ключевого столбца NULL сортируются ближе к концу индекса, чем значения ключевого столбца, отличные от NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>форцематериализатион</td>
<td>Этот параметр заставляет диспетчер временных таблиц отказаться от любой попытки выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</td>
</tr>
<tr class="even">
<td></td>
<td>ерророндупликатеинсертион</td>
<td>Этот параметр запрашивает, что любая попытка вставить запись с тем же ключом индекса, что и ранее вставленная запись, сразу же завершится с <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>. Если этот параметр не запрошен, то дубликат может быть обнаружен немедленно, с ошибкой или автоматически удален позже в зависимости от стратегии, выбранной ядром СУБД для реализации временной таблицы на основе запрошенной функциональности. Если эта функция не требуется, то лучше не запрашивать ее. Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

[форвардонли](./server2003grbits.forwardonly-field.md)

[интринсиклвсонли](./windows7grbits.intrinsiclvsonly-field.md)
