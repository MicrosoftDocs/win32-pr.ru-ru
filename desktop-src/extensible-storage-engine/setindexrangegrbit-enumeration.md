---
description: Дополнительные сведения о перечислении Сетиндексранжегрбит
title: Перечисление Сетиндексранжегрбит
TOCTitle: SetIndexRangeGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setindexrangegrbit(v=EXCHG.10)
ms:contentKeyID: 39515181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInstantDuration
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeUpperLimit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.None
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeInclusive
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit
- Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit.RangeRemove
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cda73597f88d2c8fca911ebb96d7a3c6399ed9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682885"
---
# <a name="setindexrangegrbit-enumeration"></a><span data-ttu-id="0e1f1-103">Перечисление Сетиндексранжегрбит</span><span class="sxs-lookup"><span data-stu-id="0e1f1-103">SetIndexRangeGrbit enumeration</span></span>

<span data-ttu-id="0e1f1-104">Параметры для Жетсетиндексранже.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-104">Options for JetSetIndexRange.</span></span>

<span data-ttu-id="0e1f1-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="0e1f1-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e1f1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e1f1-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e1f1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e1f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e1f1-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetIndexRangeGrbit
'Usage
Dim instance As SetIndexRangeGrbit
```

``` csharp
[FlagsAttribute]
public enum SetIndexRangeGrbit
```

## <a name="members"></a><span data-ttu-id="0e1f1-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0e1f1-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="0e1f1-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="0e1f1-110">Member name</span></span></th>
<th><span data-ttu-id="0e1f1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0e1f1-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0e1f1-112">Нет</span><span class="sxs-lookup"><span data-stu-id="0e1f1-112">None</span></span></td>
<td><span data-ttu-id="0e1f1-113">Параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0e1f1-114">ранжеинклусиве</span><span class="sxs-lookup"><span data-stu-id="0e1f1-114">RangeInclusive</span></span></td>
<td><span data-ttu-id="0e1f1-115">Этот параметр указывает, что предел диапазона индекса является инклюзивным.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-115">This option indicates that the limit of the index range is inclusive.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0e1f1-116">ранжеупперлимит</span><span class="sxs-lookup"><span data-stu-id="0e1f1-116">RangeUpperLimit</span></span></td>
<td><span data-ttu-id="0e1f1-117">Ключ поиска в курсоре представляет критерий поиска для элемента индекса, ближайшего к концу индекса, который будет соответствовать диапазону индексов.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-117">The search key in the cursor represents the search criteria for the index entry closest to the end of the index that will match the index range.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="0e1f1-118">ранжеинстантдуратион</span><span class="sxs-lookup"><span data-stu-id="0e1f1-118">RangeInstantDuration</span></span></td>
<td><span data-ttu-id="0e1f1-119">Диапазон индексов должен быть удален сразу после его установки.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-119">The index range should be removed as soon as it has been established.</span></span> <span data-ttu-id="0e1f1-120">Это полезно для проверки существования записей индекса, соответствующих условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-120">This is useful for testing for the existence of index entries that match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="0e1f1-121">ранжеремове</span><span class="sxs-lookup"><span data-stu-id="0e1f1-121">RangeRemove</span></span></td>
<td><span data-ttu-id="0e1f1-122">Отмена и существующий диапазон индекса.</span><span class="sxs-lookup"><span data-stu-id="0e1f1-122">Cancel and existing index range.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="0e1f1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e1f1-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e1f1-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="0e1f1-124">Reference</span></span>

[<span data-ttu-id="0e1f1-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0e1f1-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
