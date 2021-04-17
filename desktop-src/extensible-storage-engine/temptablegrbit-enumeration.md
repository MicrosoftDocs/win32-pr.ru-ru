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
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="4d6b1-103">Перечисление Темптаблегрбит</span><span class="sxs-lookup"><span data-stu-id="4d6b1-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="4d6b1-104">Параметры для создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-104">Options for temporary table creation.</span></span>

<span data-ttu-id="4d6b1-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="4d6b1-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d6b1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d6b1-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d6b1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d6b1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d6b1-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="4d6b1-109">Члены</span><span class="sxs-lookup"><span data-stu-id="4d6b1-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="4d6b1-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="4d6b1-110">Member name</span></span></th>
<th><span data-ttu-id="4d6b1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4d6b1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4d6b1-112">Нет</span><span class="sxs-lookup"><span data-stu-id="4d6b1-112">None</span></span></td>
<td><span data-ttu-id="4d6b1-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4d6b1-114">Индексированного</span><span class="sxs-lookup"><span data-stu-id="4d6b1-114">Indexed</span></span></td>
<td><span data-ttu-id="4d6b1-115">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы позволить использовать Жетсик для поиска записей по ключу индекса.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="4d6b1-116">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="4d6b1-117">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4d6b1-118">Уникальная идентификация</span><span class="sxs-lookup"><span data-stu-id="4d6b1-118">Unique</span></span></td>
<td><span data-ttu-id="4d6b1-119">Этот параметр запрашивает удаление записей с повторяющимися ключами индекса из окончательного набора записей во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="4d6b1-120">До Windows Server 2003 в ядре СУБД всегда предполагается, что этот параметр действует из-за того факта, что все кластеризованные индексы также должны быть первичным ключом и, таким же, должны быть уникальными.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="4d6b1-121">Начиная с Windows Server 2003, теперь можно создать временную таблицу, которая не удаляет дубликаты при указании параметра <a href="dn351284(v=exchg.10).md">форвардонли</a> .</span><span class="sxs-lookup"><span data-stu-id="4d6b1-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="4d6b1-122">Невозможно понять, какие дубликаты будут выдаваться, и какие дубликаты будут отменены в целом.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="4d6b1-123">Однако при запросе параметра Ерророндупликатеинсертион первая запись с заданным ключом индекса для вставки во временную таблицу всегда будет выдаваться.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4d6b1-124">Обновляется</span><span class="sxs-lookup"><span data-stu-id="4d6b1-124">Updatable</span></span></td>
<td><span data-ttu-id="4d6b1-125">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы разрешить впоследствии изменять записи, которые были вставлены.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="4d6b1-126">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="4d6b1-127">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4d6b1-128">Прокручиваемые курсоры</span><span class="sxs-lookup"><span data-stu-id="4d6b1-128">Scrollable</span></span></td>
<td><span data-ttu-id="4d6b1-129">Этот параметр требует, чтобы временная таблица была достаточно гибкой, чтобы можно было просматривать записи в произвольном порядке и в направлении с помощью <a href="dn292217(v=exchg.10).md">жетмове (JET_SESID, JET_TABLEID, Int32, мовегрбит)</a>.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="4d6b1-130">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="4d6b1-131">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4d6b1-132">сортнуллшигх</span><span class="sxs-lookup"><span data-stu-id="4d6b1-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="4d6b1-133">При выборе этого варианта значения ключевого столбца NULL сортируются ближе к концу индекса, чем значения ключевого столбца, отличные от NULL.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="4d6b1-134">форцематериализатион</span><span class="sxs-lookup"><span data-stu-id="4d6b1-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="4d6b1-135">Этот параметр заставляет диспетчер временных таблиц отказаться от любой попытки выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="4d6b1-136">ерророндупликатеинсертион</span><span class="sxs-lookup"><span data-stu-id="4d6b1-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="4d6b1-137">Этот параметр запрашивает, что любая попытка вставить запись с тем же ключом индекса, что и ранее вставленная запись, сразу же завершится с <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="4d6b1-138">Если этот параметр не запрошен, то дубликат может быть обнаружен немедленно, с ошибкой или автоматически удален позже в зависимости от стратегии, выбранной ядром СУБД для реализации временной таблицы на основе запрошенной функциональности.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="4d6b1-139">Если эта функция не требуется, то лучше не запрашивать ее.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="4d6b1-140">Если эта функция не запрошена, то диспетчер временных таблиц может выбрать стратегию для управления временной таблицей, что приведет к повышению производительности.</span><span class="sxs-lookup"><span data-stu-id="4d6b1-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="4d6b1-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d6b1-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d6b1-142">Справочник</span><span class="sxs-lookup"><span data-stu-id="4d6b1-142">Reference</span></span>

[<span data-ttu-id="4d6b1-143">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4d6b1-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="4d6b1-144">форвардонли</span><span class="sxs-lookup"><span data-stu-id="4d6b1-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="4d6b1-145">интринсиклвсонли</span><span class="sxs-lookup"><span data-stu-id="4d6b1-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)
