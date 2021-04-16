---
description: Дополнительные сведения о перечислении Компактгрбит
title: Перечисление Компактгрбит
TOCTitle: CompactGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CompactGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.compactgrbit(v=EXCHG.10)
ms:contentKeyID: 39509676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CompactGrbit.Repair
- Microsoft.Isam.Esent.Interop.CompactGrbit.Stats
- Microsoft.Isam.Esent.Interop.CompactGrbit
- Microsoft.Isam.Esent.Interop.CompactGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7bbe6c88a0a52ab852e3cde9af8871833948949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650600"
---
# <a name="compactgrbit-enumeration"></a><span data-ttu-id="115e7-103">Перечисление Компактгрбит</span><span class="sxs-lookup"><span data-stu-id="115e7-103">CompactGrbit enumeration</span></span>

<span data-ttu-id="115e7-104">Параметры для [жеткомпакт (JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, компактгрбит)](./api.jetcompact-method.md).</span><span class="sxs-lookup"><span data-stu-id="115e7-104">Options for [JetCompact(JET_SESID, String, String, JET_PFNSTATUS, JET_CONVERT, CompactGrbit)](./api.jetcompact-method.md).</span></span>

<span data-ttu-id="115e7-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="115e7-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="115e7-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="115e7-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="115e7-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="115e7-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="115e7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="115e7-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CompactGrbit
'Usage
Dim instance As CompactGrbit
```

``` csharp
[FlagsAttribute]
public enum CompactGrbit
```

## <a name="members"></a><span data-ttu-id="115e7-109">Члены</span><span class="sxs-lookup"><span data-stu-id="115e7-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="115e7-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="115e7-110">Member name</span></span></th>
<th><span data-ttu-id="115e7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="115e7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="115e7-112">Нет</span><span class="sxs-lookup"><span data-stu-id="115e7-112">None</span></span></td>
<td><span data-ttu-id="115e7-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="115e7-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="115e7-114">Статистика</span><span class="sxs-lookup"><span data-stu-id="115e7-114">Stats</span></span></td>
<td><span data-ttu-id="115e7-115">Вызывает Жеткомпакт для дампа статистики в базе данных-источнике в файл с именем DFRGINFO.TXT.</span><span class="sxs-lookup"><span data-stu-id="115e7-115">Causes JetCompact to dump statistics on the source database to a file named DFRGINFO.TXT.</span></span> <span data-ttu-id="115e7-116">Статистика включает в себя имя каждой таблицы в базе данных источника, число строк в каждой таблице, общий размер в байтах всех строк в каждой таблице, общий размер в байтах всех столбцов типа <a href="hh577895(v=exchg.10).md">LongText</a> или <a href="hh577895(v=exchg.10).md">лонгбинари</a> , которые достаточно велики для хранения отдельно от записи, число конечных страниц кластеризованного индекса и количество конечных страниц с длинными значениями.</span><span class="sxs-lookup"><span data-stu-id="115e7-116">Statistics include the name of each table in source database, number of rows in each table, total size in bytes of all rows in each table, total size in bytes of all columns of type <a href="hh577895(v=exchg.10).md">LongText</a> or <a href="hh577895(v=exchg.10).md">LongBinary</a> that were large enough to be stored separate from the record, number of clustered index leaf pages, and the number of long value leaf pages.</span></span> <span data-ttu-id="115e7-117">Кроме того, сводные статистические данные, включая размер базы данных-источника, целевую базу данных, время, необходимое для сжатия базы данных, также сохраняются в дампе временной базы данных.</span><span class="sxs-lookup"><span data-stu-id="115e7-117">In addition, summary statistics including the size of the source database, destination database, time required for database compaction, temporary database space are all dumped as well.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="115e7-118">Восстановить</span><span class="sxs-lookup"><span data-stu-id="115e7-118">Repair</span></span></td>
<td><span data-ttu-id="115e7-119"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="115e7-119"><strong>Obsolete.</strong></span></span> <span data-ttu-id="115e7-120">Используется, если база данных-источник повреждена.</span><span class="sxs-lookup"><span data-stu-id="115e7-120">Used when the source database is known to be corrupt.</span></span> <span data-ttu-id="115e7-121">Она обеспечивает целый набор новых поведений, предназначенных для восстановления максимально возможного объема данных из базы данных-источника.</span><span class="sxs-lookup"><span data-stu-id="115e7-121">It enables a whole set of new behaviors intended to salvage as much data as possible from the source database.</span></span> <span data-ttu-id="115e7-122">Жеткомпакт с этим набором параметров может вернуть значение <a href="hh564840(v=exchg.10).md">Success</a> , но не скопировать все данные, созданные в базе данных источника.</span><span class="sxs-lookup"><span data-stu-id="115e7-122">JetCompact with this option set may return <a href="hh564840(v=exchg.10).md">Success</a> but not copy all of the data created in the source database.</span></span> <span data-ttu-id="115e7-123">Данные, которые находятся в поврежденных частях базы данных источника, будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="115e7-123">Data that was in damaged portions of the source database will be skipped.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="115e7-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="115e7-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="115e7-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="115e7-125">Reference</span></span>

[<span data-ttu-id="115e7-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="115e7-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
