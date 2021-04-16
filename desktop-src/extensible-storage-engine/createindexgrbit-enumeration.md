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
# <a name="createindexgrbit-enumeration"></a><span data-ttu-id="069cc-103">Перечисление Креатеиндексгрбит</span><span class="sxs-lookup"><span data-stu-id="069cc-103">CreateIndexGrbit enumeration</span></span>

<span data-ttu-id="069cc-104">Параметры для Жеткреатеиндекс.</span><span class="sxs-lookup"><span data-stu-id="069cc-104">Options for JetCreateIndex.</span></span>

<span data-ttu-id="069cc-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="069cc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="069cc-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="069cc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="069cc-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="069cc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="069cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="069cc-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="069cc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="069cc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="069cc-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="069cc-110">Member name</span></span></th>
<th><span data-ttu-id="069cc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="069cc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="069cc-112">Нет</span><span class="sxs-lookup"><span data-stu-id="069cc-112">None</span></span></td>
<td><span data-ttu-id="069cc-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="069cc-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="069cc-114">индексуникуе</span><span class="sxs-lookup"><span data-stu-id="069cc-114">IndexUnique</span></span></td>
<td><span data-ttu-id="069cc-115">Дублирующиеся записи индекса (ключи) запрещены.</span><span class="sxs-lookup"><span data-stu-id="069cc-115">Duplicate index entries (keys) are disallowed.</span></span> <span data-ttu-id="069cc-116">Это применяется при вызове Жетупдате, а не при вызове Жетсетколумн.</span><span class="sxs-lookup"><span data-stu-id="069cc-116">This is enforced when JetUpdate is called, not when JetSetColumn is called.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="069cc-117">индекспримари</span><span class="sxs-lookup"><span data-stu-id="069cc-117">IndexPrimary</span></span></td>
<td><span data-ttu-id="069cc-118">Индекс является первичным (кластеризованным) индексом.</span><span class="sxs-lookup"><span data-stu-id="069cc-118">The index is a primary (clustered) index.</span></span> <span data-ttu-id="069cc-119">Каждая таблица должна иметь ровно один первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="069cc-119">Every table must have exactly one primary index.</span></span> <span data-ttu-id="069cc-120">Если первичный индекс явно не определен в таблице, то ядро СУБД создаст собственный первичный индекс.</span><span class="sxs-lookup"><span data-stu-id="069cc-120">If no primary index is explicitly defined over a table, then the database engine will create its own primary index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="069cc-121">индексдисалловнулл</span><span class="sxs-lookup"><span data-stu-id="069cc-121">IndexDisallowNull</span></span></td>
<td><span data-ttu-id="069cc-122">Ни один из столбцов, по которым создается индекс, может содержать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="069cc-122">None of the columns over which the index is created may contain a NULL value.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="069cc-123">индексигноренулл</span><span class="sxs-lookup"><span data-stu-id="069cc-123">IndexIgnoreNull</span></span></td>
<td><span data-ttu-id="069cc-124">Не добавляйте элемент индекса для строки, если все индексируемые столбцы имеют значение NULL.</span><span class="sxs-lookup"><span data-stu-id="069cc-124">Do not add an index entry for a row if all of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="069cc-125">индексигнореанинулл</span><span class="sxs-lookup"><span data-stu-id="069cc-125">IndexIgnoreAnyNull</span></span></td>
<td><span data-ttu-id="069cc-126">Не добавляйте элемент индекса для строки, если какие-либо индексируемые столбцы имеют значение NULL.</span><span class="sxs-lookup"><span data-stu-id="069cc-126">Do not add an index entry for a row if any of the columns being indexed are NULL.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="069cc-127">индексигнорефирстнулл</span><span class="sxs-lookup"><span data-stu-id="069cc-127">IndexIgnoreFirstNull</span></span></td>
<td><span data-ttu-id="069cc-128">Не добавляйте элемент индекса для строки, если первый индексируемый столбец имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="069cc-128">Do not add an index entry for a row if the first column being indexed is NULL.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="069cc-129">индекслазифлуш</span><span class="sxs-lookup"><span data-stu-id="069cc-129">IndexLazyFlush</span></span></td>
<td><span data-ttu-id="069cc-130">Указывает, что операции с индексами будут регистрироваться неактивно.</span><span class="sxs-lookup"><span data-stu-id="069cc-130">Specifies that the index operations will be logged lazily.</span></span> <span data-ttu-id="069cc-131">JET_bitIndexLazyFlush не влияет на отложенность обновлений данных.</span><span class="sxs-lookup"><span data-stu-id="069cc-131">JET_bitIndexLazyFlush does not affect the laziness of data updates.</span></span> <span data-ttu-id="069cc-132">Если операции индексирования прерываются завершением процесса, то при мягком восстановлении все равно смогут получить целостное состояние базы данных, но индекс может отсутствовать.</span><span class="sxs-lookup"><span data-stu-id="069cc-132">If the indexing operations is interrupted by process termination, Soft Recovery will still be able to able to get the database to a consistent state, but the index may not be present.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="069cc-133">индексемпти</span><span class="sxs-lookup"><span data-stu-id="069cc-133">IndexEmpty</span></span></td>
<td><span data-ttu-id="069cc-134">Не пытайтесь построить индекс, так как все записи будут иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="069cc-134">Do not attempt to build the index, because all entries would evaluate to NULL.</span></span> <span data-ttu-id="069cc-135">грбит также должен указывать JET_bitIgnoreAnyNull при передаче JET_bitIndexEmpty.</span><span class="sxs-lookup"><span data-stu-id="069cc-135">grbit MUST also specify JET_bitIgnoreAnyNull when JET_bitIndexEmpty is passed.</span></span> <span data-ttu-id="069cc-136">Это улучшение производительности.</span><span class="sxs-lookup"><span data-stu-id="069cc-136">This is a performance enhancement.</span></span> <span data-ttu-id="069cc-137">Например, если в таблицу добавляется новый столбец, то для него создается индекс, а все записи в таблице просматриваются, даже если они никогда не добавляются в индекс.</span><span class="sxs-lookup"><span data-stu-id="069cc-137">For example if a new column is added to a table, then an index is created over this newly added column, all of the records in the table would be scanned even though they would never get added to the index anyway.</span></span> <span data-ttu-id="069cc-138">При указании JET_bitIndexEmpty пропускается сканирование таблицы, что может занять длительное время.</span><span class="sxs-lookup"><span data-stu-id="069cc-138">Specifying JET_bitIndexEmpty skips the scanning of the table, which could potentially take a long time.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="069cc-139">индексунверсионед</span><span class="sxs-lookup"><span data-stu-id="069cc-139">IndexUnversioned</span></span></td>
<td><span data-ttu-id="069cc-140">Приводит к тому, что создание индекса станет видимым для других транзакций.</span><span class="sxs-lookup"><span data-stu-id="069cc-140">Causes index creation to be visible to other transactions.</span></span> <span data-ttu-id="069cc-141">Обычно сеанс в транзакции не сможет увидеть операцию создания индекса в другом сеансе.</span><span class="sxs-lookup"><span data-stu-id="069cc-141">Normally a session in a transaction will not be able to see an index creation operation in another session.</span></span> <span data-ttu-id="069cc-142">Этот флаг может быть полезен, если другая транзакция, скорее всего, создаст тот же индекс, так что второй индекс-Create просто завершится ошибкой, а не может вызвать множество ненужных операций с базой данных.</span><span class="sxs-lookup"><span data-stu-id="069cc-142">This flag can be useful if another transaction is likely to create the same index, so that the second index-create will simply fail instead of potentially causing many unnecessary database operations.</span></span> <span data-ttu-id="069cc-143">Вторая транзакция может не иметь возможности немедленно использовать индекс.</span><span class="sxs-lookup"><span data-stu-id="069cc-143">The second transaction may not be able to use the index immediately.</span></span> <span data-ttu-id="069cc-144">Операция создания индекса должна быть завершена, прежде чем ее можно будет использовать.</span><span class="sxs-lookup"><span data-stu-id="069cc-144">The index creation operation needs to complete before it is usable.</span></span> <span data-ttu-id="069cc-145">В настоящее время сеанс не должен находиться в транзакции, чтобы создать индекс без сведений о версии.</span><span class="sxs-lookup"><span data-stu-id="069cc-145">The session must not currently be in a transaction to create an index without version information.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="069cc-146">индекссортнуллшигх</span><span class="sxs-lookup"><span data-stu-id="069cc-146">IndexSortNullsHigh</span></span></td>
<td><span data-ttu-id="069cc-147">Задание этого флага приводит к сортировке значений NULL после данных для всех столбцов в индексе.</span><span class="sxs-lookup"><span data-stu-id="069cc-147">Specifying this flag causes NULL values to be sorted after data for all columns in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="069cc-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="069cc-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="069cc-149">Справочник</span><span class="sxs-lookup"><span data-stu-id="069cc-149">Reference</span></span>

[<span data-ttu-id="069cc-150">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="069cc-150">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
