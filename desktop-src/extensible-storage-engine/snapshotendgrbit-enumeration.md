---
description: Дополнительные сведения о перечислении Снапшотендгрбит
title: Перечисление Снапшотендгрбит (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: SnapshotEndGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.snapshotendgrbit(v=EXCHG.10)
ms:contentKeyID: 39510894
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit
- Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit.AbortSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit.AbortSnapshot
- Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit.None
- Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc813f4931a3b5a1d03cb5640e06d48d83e9aa07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154662"
---
# <a name="snapshotendgrbit-enumeration"></a><span data-ttu-id="7b72e-103">Перечисление Снапшотендгрбит</span><span class="sxs-lookup"><span data-stu-id="7b72e-103">SnapshotEndGrbit enumeration</span></span>

<span data-ttu-id="7b72e-104">Параметры для [жетосснапшотенд (JET_OSSNAPID, снапшотендгрбит)](./vistaapi.jetossnapshotend-method.md).</span><span class="sxs-lookup"><span data-stu-id="7b72e-104">Options for [JetOSSnapshotEnd(JET_OSSNAPID, SnapshotEndGrbit)](./vistaapi.jetossnapshotend-method.md).</span></span>

<span data-ttu-id="7b72e-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="7b72e-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="7b72e-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7b72e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7b72e-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7b72e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7b72e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b72e-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SnapshotEndGrbit
'Usage
Dim instance As SnapshotEndGrbit
```

``` csharp
[FlagsAttribute]
public enum SnapshotEndGrbit
```

## <a name="members"></a><span data-ttu-id="7b72e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7b72e-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="7b72e-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="7b72e-110">Member name</span></span></th>
<th><span data-ttu-id="7b72e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7b72e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="7b72e-112">Нет</span><span class="sxs-lookup"><span data-stu-id="7b72e-112">None</span></span></td>
<td><span data-ttu-id="7b72e-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b72e-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="7b72e-114">абортснапшот</span><span class="sxs-lookup"><span data-stu-id="7b72e-114">AbortSnapshot</span></span></td>
<td><span data-ttu-id="7b72e-115">Сеанс моментального снимка прерван.</span><span class="sxs-lookup"><span data-stu-id="7b72e-115">The snapshot session aborted.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="7b72e-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b72e-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7b72e-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="7b72e-117">Reference</span></span>

[<span data-ttu-id="7b72e-118">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="7b72e-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
