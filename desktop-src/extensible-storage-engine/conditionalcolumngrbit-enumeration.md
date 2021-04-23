---
description: Дополнительные сведения о перечислении Кондитионалколумнгрбит
title: Перечисление Кондитионалколумнгрбит
TOCTitle: ConditionalColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conditionalcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39513009
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNull
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit
- Microsoft.Isam.Esent.Interop.ConditionalColumnGrbit.ColumnMustBeNonNull
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82828df5d5a25dac08a2a8ab560225456f075a34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991340"
---
# <a name="conditionalcolumngrbit-enumeration"></a><span data-ttu-id="9f193-103">Перечисление Кондитионалколумнгрбит</span><span class="sxs-lookup"><span data-stu-id="9f193-103">ConditionalColumnGrbit enumeration</span></span>

<span data-ttu-id="9f193-104">Параметры структуры JET_CONDITIONALCOLUMN.</span><span class="sxs-lookup"><span data-stu-id="9f193-104">Options for the JET_CONDITIONALCOLUMN structure.</span></span>

<span data-ttu-id="9f193-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="9f193-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="9f193-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9f193-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9f193-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9f193-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9f193-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9f193-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ConditionalColumnGrbit
'Usage
Dim instance As ConditionalColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum ConditionalColumnGrbit
```

## <a name="members"></a><span data-ttu-id="9f193-109">Члены</span><span class="sxs-lookup"><span data-stu-id="9f193-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9f193-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="9f193-110">Member name</span></span></th>
<th><span data-ttu-id="9f193-111">Описание</span><span class="sxs-lookup"><span data-stu-id="9f193-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9f193-112">колумнмустбенулл</span><span class="sxs-lookup"><span data-stu-id="9f193-112">ColumnMustBeNull</span></span></td>
<td><span data-ttu-id="9f193-113">Чтобы запись индекса отображалась в индексе, столбец должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="9f193-113">The column must be null for an index entry to appear in the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9f193-114">колумнмустбеноннулл</span><span class="sxs-lookup"><span data-stu-id="9f193-114">ColumnMustBeNonNull</span></span></td>
<td><span data-ttu-id="9f193-115">Столбец не должен иметь значение null, чтобы запись индекса отображалась в индексе.</span><span class="sxs-lookup"><span data-stu-id="9f193-115">The column must be non-null for an index entry to appear in the index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9f193-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9f193-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9f193-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="9f193-117">Reference</span></span>

[<span data-ttu-id="9f193-118">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9f193-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
