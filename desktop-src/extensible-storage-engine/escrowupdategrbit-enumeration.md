---
description: Дополнительные сведения о перечислении Ескровупдатегрбит
title: Перечисление Ескровупдатегрбит
TOCTitle: EscrowUpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.escrowupdategrbit(v=EXCHG.10)
ms:contentKeyID: 39514160
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.None
- Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit.NoRollback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d301ef801a5685057a9e33beb794f3b6cf13e646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999543"
---
# <a name="escrowupdategrbit-enumeration"></a><span data-ttu-id="b5864-103">Перечисление Ескровупдатегрбит</span><span class="sxs-lookup"><span data-stu-id="b5864-103">EscrowUpdateGrbit enumeration</span></span>

<span data-ttu-id="b5864-104">Параметры для Жетескровупдате.</span><span class="sxs-lookup"><span data-stu-id="b5864-104">Options for JetEscrowUpdate.</span></span>

<span data-ttu-id="b5864-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="b5864-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="b5864-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b5864-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b5864-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b5864-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b5864-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5864-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EscrowUpdateGrbit
'Usage
Dim instance As EscrowUpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum EscrowUpdateGrbit
```

## <a name="members"></a><span data-ttu-id="b5864-109">Члены</span><span class="sxs-lookup"><span data-stu-id="b5864-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b5864-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="b5864-110">Member name</span></span></th>
<th><span data-ttu-id="b5864-111">Описание</span><span class="sxs-lookup"><span data-stu-id="b5864-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b5864-112">Нет</span><span class="sxs-lookup"><span data-stu-id="b5864-112">None</span></span></td>
<td><span data-ttu-id="b5864-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5864-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b5864-114">Откат</span><span class="sxs-lookup"><span data-stu-id="b5864-114">NoRollback</span></span></td>
<td><span data-ttu-id="b5864-115">Даже если в сеансе, выполняющем Депонированное обновление, выполняется откат транзакций, это обновление не будет отменено.</span><span class="sxs-lookup"><span data-stu-id="b5864-115">Even if the session performing the escrow update has its transaction rollback this update will not be undone.</span></span> <span data-ttu-id="b5864-116">Поскольку записи журнала не могут быть записаны на диск, последние депонированные обновления, выполненные с помощью этого флага, могут быть утрачены в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="b5864-116">As the log records may not be flushed to disk, recent escrow updates done with this flag may be lost if there is a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b5864-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5864-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b5864-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="b5864-118">Reference</span></span>

[<span data-ttu-id="b5864-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b5864-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
