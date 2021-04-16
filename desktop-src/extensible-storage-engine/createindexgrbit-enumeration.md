---
description: Дополнительные сведения о перечислении Креатеиндексгрбит
title: Перечисление Креатеиндексгрбит
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713009"
---
# <a name="createindexgrbit-enumeration"></a>Перечисление Креатеиндексгрбит

Параметры для Жеткреатеиндекс.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
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
<td>индексуникуе</td>
<td>Дублирующиеся записи индекса (ключи) запрещены. Это применяется при вызове Жетупдате, а не при вызове Жетсетколумн.</td>
</tr>
<tr class="odd">
<td></td>
<td>индекспримари</td>
<td>Индекс является первичным (кластеризованным) индексом. Каждая таблица должна иметь ровно один первичный индекс. Если первичный индекс явно не определен в таблице, то ядро СУБД создаст собственный первичный индекс.</td>
</tr>
<tr class="even">
<td></td>
<td>индексдисалловнулл</td>
<td>Ни один из столбцов, по которым создается индекс, может содержать значение NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>индексигноренулл</td>
<td>Не добавляйте элемент индекса для строки, если все индексируемые столбцы имеют значение NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>индексигнореанинулл</td>
<td>Не добавляйте элемент индекса для строки, если какие-либо индексируемые столбцы имеют значение NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>индексигнорефирстнулл</td>
<td>Не добавляйте элемент индекса для строки, если первый индексируемый столбец имеет значение NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>индекслазифлуш</td>
<td>Указывает, что операции с индексами будут регистрироваться неактивно. JET_bitIndexLazyFlush не влияет на отложенность обновлений данных. Если операции индексирования прерываются завершением процесса, то при мягком восстановлении все равно смогут получить целостное состояние базы данных, но индекс может отсутствовать.</td>
</tr>
<tr class="odd">
<td></td>
<td>индексемпти</td>
<td>Не пытайтесь построить индекс, так как все записи будут иметь значение NULL. грбит также должен указывать JET_bitIgnoreAnyNull при передаче JET_bitIndexEmpty. Это улучшение производительности. Например, если в таблицу добавляется новый столбец, то для него создается индекс, а все записи в таблице просматриваются, даже если они никогда не добавляются в индекс. При указании JET_bitIndexEmpty пропускается сканирование таблицы, что может занять длительное время.</td>
</tr>
<tr class="even">
<td></td>
<td>индексунверсионед</td>
<td>Приводит к тому, что создание индекса станет видимым для других транзакций. Обычно сеанс в транзакции не сможет увидеть операцию создания индекса в другом сеансе. Этот флаг может быть полезен, если другая транзакция, скорее всего, создаст тот же индекс, так что второй индекс-Create просто завершится ошибкой, а не может вызвать множество ненужных операций с базой данных. Вторая транзакция может не иметь возможности немедленно использовать индекс. Операция создания индекса должна быть завершена, прежде чем ее можно будет использовать. В настоящее время сеанс не должен находиться в транзакции, чтобы создать индекс без сведений о версии.</td>
</tr>
<tr class="odd">
<td></td>
<td>индекссортнуллшигх</td>
<td>Задание этого флага приводит к сортировке значений NULL после данных для всех столбцов в индексе.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
