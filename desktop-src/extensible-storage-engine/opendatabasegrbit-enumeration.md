---
description: Дополнительные сведения о перечислении Опендатабасегрбит
title: Перечисление Опендатабасегрбит
TOCTitle: OpenDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opendatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39514563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit.Exclusive
- Microsoft.Isam.Esent.Interop.OpenDatabaseGrbit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d14fb779ec02137f6a4fce1cfdd92f46dedcb832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264771"
---
# <a name="opendatabasegrbit-enumeration"></a><span data-ttu-id="ecbc9-103">Перечисление Опендатабасегрбит</span><span class="sxs-lookup"><span data-stu-id="ecbc9-103">OpenDatabaseGrbit enumeration</span></span>

<span data-ttu-id="ecbc9-104">Параметры для [жетопендатабасе (JET_SESID, String, String, JET_DBID, опендатабасегрбит)](./api.jetopendatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="ecbc9-104">Options for [JetOpenDatabase(JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).</span></span>

<span data-ttu-id="ecbc9-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="ecbc9-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="ecbc9-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ecbc9-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ecbc9-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ecbc9-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ecbc9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ecbc9-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenDatabaseGrbit
'Usage
Dim instance As OpenDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="ecbc9-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ecbc9-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="ecbc9-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="ecbc9-110">Member name</span></span></th>
<th><span data-ttu-id="ecbc9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ecbc9-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ecbc9-112">Нет</span><span class="sxs-lookup"><span data-stu-id="ecbc9-112">None</span></span></td>
<td><span data-ttu-id="ecbc9-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ecbc9-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="ecbc9-114">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ecbc9-114">ReadOnly</span></span></td>
<td><span data-ttu-id="ecbc9-115">Предотвращает изменения в базе данных.</span><span class="sxs-lookup"><span data-stu-id="ecbc9-115">Prevents modifications to the database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="ecbc9-116">Монопольная блокировка</span><span class="sxs-lookup"><span data-stu-id="ecbc9-116">Exclusive</span></span></td>
<td><span data-ttu-id="ecbc9-117">Разрешает присоединение базы данных только одному сеансу.</span><span class="sxs-lookup"><span data-stu-id="ecbc9-117">Allows only a single session to attach a database.</span></span> <span data-ttu-id="ecbc9-118">Как правило, база данных может быть открыта несколькими сеансами.</span><span class="sxs-lookup"><span data-stu-id="ecbc9-118">Normally, several sessions can open a database.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="ecbc9-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecbc9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ecbc9-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ecbc9-120">Reference</span></span>

[<span data-ttu-id="ecbc9-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ecbc9-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
