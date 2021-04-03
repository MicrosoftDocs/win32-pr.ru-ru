---
description: 'Дополнительные сведения: перечисление JET_dbstate'
title: Перечисление JET_dbstate
TOCTitle: JET_dbstate enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_dbstate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbstate(v=EXCHG.10)
ms:contentKeyID: 39511841
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_dbstate
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_dbstate.JustCreated
- Microsoft.Isam.Esent.Interop.JET_dbstate.BeingConverted
- Microsoft.Isam.Esent.Interop.JET_dbstate.CleanShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate.ForceDetach
- Microsoft.Isam.Esent.Interop.JET_dbstate.DirtyShutdown
- Microsoft.Isam.Esent.Interop.JET_dbstate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a83c8a4313e5e6f21ee885ee7936c90503bfbd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808561"
---
# <a name="jet_dbstate-enumeration"></a><span data-ttu-id="35530-103">Перечисление JET_dbstate</span><span class="sxs-lookup"><span data-stu-id="35530-103">JET_dbstate enumeration</span></span>

<span data-ttu-id="35530-104">Состояния базы данных (используется в [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span><span class="sxs-lookup"><span data-stu-id="35530-104">Database states (used in [JET_DBINFOMISC](./jet-dbinfomisc-class.md)).</span></span>

<span data-ttu-id="35530-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="35530-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="35530-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="35530-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="35530-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35530-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_dbstate
'Usage
Dim instance As JET_dbstate
```

``` csharp
public enum JET_dbstate
```

## <a name="members"></a><span data-ttu-id="35530-108">Члены</span><span class="sxs-lookup"><span data-stu-id="35530-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="35530-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="35530-109">Member name</span></span></th>
<th><span data-ttu-id="35530-110">Описание</span><span class="sxs-lookup"><span data-stu-id="35530-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="35530-111">жусткреатед</span><span class="sxs-lookup"><span data-stu-id="35530-111">JustCreated</span></span></td>
<td><span data-ttu-id="35530-112">База данных была только что создана.</span><span class="sxs-lookup"><span data-stu-id="35530-112">The database was just created.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="35530-113">диртишутдовн</span><span class="sxs-lookup"><span data-stu-id="35530-113">DirtyShutdown</span></span></td>
<td><span data-ttu-id="35530-114">"Грязное" завершение работы (несовместимость) базы данных.</span><span class="sxs-lookup"><span data-stu-id="35530-114">Dirty shutdown (inconsistent) database.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="35530-115">клеаншутдовн</span><span class="sxs-lookup"><span data-stu-id="35530-115">CleanShutdown</span></span></td>
<td><span data-ttu-id="35530-116">Очистка базы данных (с постоянным завершением работы).</span><span class="sxs-lookup"><span data-stu-id="35530-116">Clean shutdown (consistent) database.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="35530-117">беингконвертед</span><span class="sxs-lookup"><span data-stu-id="35530-117">BeingConverted</span></span></td>
<td><span data-ttu-id="35530-118">Выполняется преобразование базы данных.</span><span class="sxs-lookup"><span data-stu-id="35530-118">Database is being converted.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="35530-119">форцедетач</span><span class="sxs-lookup"><span data-stu-id="35530-119">ForceDetach</span></span></td>
<td><span data-ttu-id="35530-120">База данных была принудительно отключена.</span><span class="sxs-lookup"><span data-stu-id="35530-120">Database was force-detached.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="35530-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35530-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="35530-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="35530-122">Reference</span></span>

[<span data-ttu-id="35530-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="35530-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
