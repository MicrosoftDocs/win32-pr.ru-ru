---
description: Дополнительные сведения о перечислении Сикгрбит
title: Перечисление Сикгрбит
TOCTitle: SeekGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SeekGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.seekgrbit(v=EXCHG.10)
ms:contentKeyID: 39515862
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLT
- Microsoft.Isam.Esent.Interop.SeekGrbit.SetIndexRange
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekGE
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekLE
- Microsoft.Isam.Esent.Interop.SeekGrbit
- Microsoft.Isam.Esent.Interop.SeekGrbit.SeekEQ
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e59072055710676f5f7647130f42ad5acf50527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683578"
---
# <a name="seekgrbit-enumeration"></a><span data-ttu-id="cc3a4-103">Перечисление Сикгрбит</span><span class="sxs-lookup"><span data-stu-id="cc3a4-103">SeekGrbit enumeration</span></span>

<span data-ttu-id="cc3a4-104">Параметры для Жетсик.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-104">Options for JetSeek.</span></span>

<span data-ttu-id="cc3a4-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="cc3a4-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cc3a4-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cc3a4-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cc3a4-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3a4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc3a4-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SeekGrbit
'Usage
Dim instance As SeekGrbit
```

``` csharp
[FlagsAttribute]
public enum SeekGrbit
```

## <a name="members"></a><span data-ttu-id="cc3a4-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cc3a4-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="cc3a4-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="cc3a4-110">Member name</span></span></th>
<th><span data-ttu-id="cc3a4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cc3a4-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cc3a4-112">сикек</span><span class="sxs-lookup"><span data-stu-id="cc3a4-112">SeekEQ</span></span></td>
<td><span data-ttu-id="cc3a4-113">Курсор будет располагаться на записи индекса, ближайшей к началу индекса, точно совпадающему с ключом поиска.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-113">The cursor will be positioned at the index entry closest to the start of the index that exactly matches the search key.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cc3a4-114">сиклт</span><span class="sxs-lookup"><span data-stu-id="cc3a4-114">SeekLT</span></span></td>
<td><span data-ttu-id="cc3a4-115">Курсор будет расположен в позиции индекса, ближайшей к концу индекса, который меньше, чем элемент индекса, который в точности соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-115">The cursor will be positioned at the index entry closest to the end of the index that is less than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cc3a4-116">сикле</span><span class="sxs-lookup"><span data-stu-id="cc3a4-116">SeekLE</span></span></td>
<td><span data-ttu-id="cc3a4-117">Курсор будет расположен на позиции индекса, ближайшей к концу индекса, который меньше или равен элементу индекса, который в точности соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-117">The cursor will be positioned at the index entry closest to the end of the index that is less than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cc3a4-118">сикже</span><span class="sxs-lookup"><span data-stu-id="cc3a4-118">SeekGE</span></span></td>
<td><span data-ttu-id="cc3a4-119">Курсор будет расположен на позиции индекса, ближайшей к началу индекса, который больше или равен элементу индекса, который в точности соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-119">The cursor will be positioned at the index entry closest to the start of the index that is greater than or equal to an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cc3a4-120">сикгт</span><span class="sxs-lookup"><span data-stu-id="cc3a4-120">SeekGT</span></span></td>
<td><span data-ttu-id="cc3a4-121">Курсор будет расположен на позиции индекса, ближайшей к началу индекса, который больше, чем элемент индекса, который точно соответствует условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-121">The cursor will be positioned at the index entry closest to the start of the index that is greater than an index entry that would exactly match the search criteria.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cc3a4-122">сетиндексранже</span><span class="sxs-lookup"><span data-stu-id="cc3a4-122">SetIndexRange</span></span></td>
<td><span data-ttu-id="cc3a4-123">Диапазон индексов будет автоматически настроен для всех ключей, точно соответствующих ключу поиска.</span><span class="sxs-lookup"><span data-stu-id="cc3a4-123">An index range will automatically be setup for all keys that exactly match the search key.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cc3a4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc3a4-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cc3a4-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="cc3a4-125">Reference</span></span>

[<span data-ttu-id="cc3a4-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cc3a4-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
