---
description: Дополнительные сведения о перечислении Снапшоттрункателоггрбит
title: Перечисление Снапшоттрункателоггрбит (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: SnapshotTruncateLogGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshottruncateloggrbit(v=EXCHG.10)
ms:contentKeyID: 39516474
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.AllDatabasesSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8baf9f9ec15e91183d2b01a07da9aeda0c7fec18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701657"
---
# <a name="snapshottruncateloggrbit-enumeration"></a><span data-ttu-id="164bc-103">Перечисление Снапшоттрункателоггрбит</span><span class="sxs-lookup"><span data-stu-id="164bc-103">SnapshotTruncateLogGrbit enumeration</span></span>

<span data-ttu-id="164bc-104">Параметры для [жетосснапшоттрункателог (JET_OSSNAPID, снапшоттрункателоггрбит)](./vistaapi.jetossnapshottruncatelog-method.md) и [жетосснапшоттрункателогинстанце (JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="164bc-104">Options for [JetOSSnapshotTruncateLog(JET_OSSNAPID, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncatelog-method.md) and [JetOSSnapshotTruncateLogInstance(JET_OSSNAPID, JET_INSTANCE, SnapshotTruncateLogGrbit)](./vistaapi.jetossnapshottruncateloginstance-method.md).</span></span>

<span data-ttu-id="164bc-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="164bc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="164bc-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="164bc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="164bc-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="164bc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="164bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="164bc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotTruncateLogGrbit
'Usage
Dim instance As SnapshotTruncateLogGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotTruncateLogGrbit
```

## <a name="members"></a><span data-ttu-id="164bc-109">Члены</span><span class="sxs-lookup"><span data-stu-id="164bc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="164bc-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="164bc-110">Member name</span></span></th>
<th><span data-ttu-id="164bc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="164bc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="164bc-112">Нет</span><span class="sxs-lookup"><span data-stu-id="164bc-112">None</span></span></td>
<td><span data-ttu-id="164bc-113">Усечение не выполняется.</span><span class="sxs-lookup"><span data-stu-id="164bc-113">No truncation will occur.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="164bc-114">аллдатабасесснапшот</span><span class="sxs-lookup"><span data-stu-id="164bc-114">AllDatabasesSnapshot</span></span></td>
<td><span data-ttu-id="164bc-115">Все базы данных подключены, поэтому подсистема хранилища может вычислять и выполнять усечение журнала.</span><span class="sxs-lookup"><span data-stu-id="164bc-115">All the databases are attached so the storage engine can compute and do the log truncation.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="164bc-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="164bc-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="164bc-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="164bc-117">Reference</span></span>

[<span data-ttu-id="164bc-118">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="164bc-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
