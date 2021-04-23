---
description: Дополнительные сведения о перечислении Детачдатабасегрбит
title: Перечисление Детачдатабасегрбит
TOCTitle: DetachDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.detachdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 55100985
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceClose
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceCloseAndDetach
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit
- Microsoft.Isam.Esent.Interop.DetachDatabaseGrbit.ForceDetach
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e67962420ee0179571da8262f17ea5279f59016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272534"
---
# <a name="detachdatabasegrbit-enumeration"></a><span data-ttu-id="c2e1f-103">Перечисление Детачдатабасегрбит</span><span class="sxs-lookup"><span data-stu-id="c2e1f-103">DetachDatabaseGrbit enumeration</span></span>

<span data-ttu-id="c2e1f-104">Параметры для [JetDetachDatabase2 (JET_SESID, String, детачдатабасегрбит)](./api.jetdetachdatabase2-method.md).</span><span class="sxs-lookup"><span data-stu-id="c2e1f-104">Options for [JetDetachDatabase2(JET_SESID, String, DetachDatabaseGrbit)](./api.jetdetachdatabase2-method.md).</span></span>

<span data-ttu-id="c2e1f-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c2e1f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c2e1f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c2e1f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c2e1f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e1f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2e1f-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration DetachDatabaseGrbit
'Usage
Dim instance As DetachDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum DetachDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="c2e1f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c2e1f-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c2e1f-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="c2e1f-110">Member name</span></span></th>
<th><span data-ttu-id="c2e1f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c2e1f-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c2e1f-112">Нет</span><span class="sxs-lookup"><span data-stu-id="c2e1f-112">None</span></span></td>
<td><span data-ttu-id="c2e1f-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c2e1f-114">форцедетач</span><span class="sxs-lookup"><span data-stu-id="c2e1f-114">ForceDetach</span></span></td>
<td><span data-ttu-id="c2e1f-115"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="c2e1f-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="c2e1f-116">Если используется Форцедетач, будет возвращено <a href="dn350463(v=exchg.10).md">есентфорцедетачноталловедексцептион</a> .</span><span class="sxs-lookup"><span data-stu-id="c2e1f-116">If ForceDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c2e1f-117">Принудительное закрытие</span><span class="sxs-lookup"><span data-stu-id="c2e1f-117">ForceClose</span></span></td>
<td><span data-ttu-id="c2e1f-118"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="c2e1f-118"><strong>Obsolete.</strong></span></span> <span data-ttu-id="c2e1f-119">Принудительное закрытие больше не используется.</span><span class="sxs-lookup"><span data-stu-id="c2e1f-119">ForceClose is no longer used.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c2e1f-120">форцеклосеанддетач</span><span class="sxs-lookup"><span data-stu-id="c2e1f-120">ForceCloseAndDetach</span></span></td>
<td><span data-ttu-id="c2e1f-121"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="c2e1f-121"><strong>Obsolete.</strong></span></span> <span data-ttu-id="c2e1f-122">Если используется Форцеклосеанддетач, будет возвращено <a href="dn350463(v=exchg.10).md">есентфорцедетачноталловедексцептион</a> .</span><span class="sxs-lookup"><span data-stu-id="c2e1f-122">If ForceCloseAndDetach is used, <a href="dn350463(v=exchg.10).md">EsentForceDetachNotAllowedException</a> will be returned.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c2e1f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2e1f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c2e1f-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="c2e1f-124">Reference</span></span>

[<span data-ttu-id="c2e1f-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c2e1f-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
