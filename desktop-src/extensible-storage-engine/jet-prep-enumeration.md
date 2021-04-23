---
description: 'Дополнительные сведения: перечисление JET_prep'
title: Перечисление JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693434"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="728d3-103">Перечисление JET_prep</span><span class="sxs-lookup"><span data-stu-id="728d3-103">JET_prep enumeration</span></span>

<span data-ttu-id="728d3-104">Типы обновления для Жетпрепареупдате.</span><span class="sxs-lookup"><span data-stu-id="728d3-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="728d3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="728d3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="728d3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="728d3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="728d3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="728d3-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="728d3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="728d3-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="728d3-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="728d3-109">Member name</span></span></th>
<th><span data-ttu-id="728d3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="728d3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="728d3-111">Вставить</span><span class="sxs-lookup"><span data-stu-id="728d3-111">Insert</span></span></td>
<td><span data-ttu-id="728d3-112">Этот флаг заставляет курсор подготовиться к вставке новой записи.</span><span class="sxs-lookup"><span data-stu-id="728d3-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="728d3-113">Все данные инициализируются в состояние по умолчанию для записи.</span><span class="sxs-lookup"><span data-stu-id="728d3-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="728d3-114">Если в таблице есть столбец с автоматическим приращением, то эта запись назначается новому значению независимо от того, завершилось ли обновление в конечном итоге успешно, завершается сбоем или отменяется.</span><span class="sxs-lookup"><span data-stu-id="728d3-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="728d3-115">Заменить</span><span class="sxs-lookup"><span data-stu-id="728d3-115">Replace</span></span></td>
<td><span data-ttu-id="728d3-116">Этот флаг заставляет курсор подготовиться к замене текущей записи.</span><span class="sxs-lookup"><span data-stu-id="728d3-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="728d3-117">Если таблица имеет столбец Version, то для столбца Version устанавливается следующее значение в последовательности.</span><span class="sxs-lookup"><span data-stu-id="728d3-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="728d3-118">Если это обновление не завершено, то значение версии в записи не изменится.</span><span class="sxs-lookup"><span data-stu-id="728d3-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="728d3-119">Для записи была снята блокировка обновления, чтобы другие сеансы не обновляли эту запись до завершения этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="728d3-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="728d3-120">Отменить</span><span class="sxs-lookup"><span data-stu-id="728d3-120">Cancel</span></span></td>
<td><span data-ttu-id="728d3-121">Этот флаг приводит к тому, что Жетпрепареупдате отменяет обновление для данного курсора.</span><span class="sxs-lookup"><span data-stu-id="728d3-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="728d3-122">реплаценолокк</span><span class="sxs-lookup"><span data-stu-id="728d3-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="728d3-123">Этот флаг аналогичен JET_prepReplace, но блокировка не предпринимается, чтобы другие сеансы не обновляли эту запись.</span><span class="sxs-lookup"><span data-stu-id="728d3-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="728d3-124">Вместо этого этот сеанс может получить JET_errWriteConflict при вызове Жетупдате для завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="728d3-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="728d3-125">инсерткопи</span><span class="sxs-lookup"><span data-stu-id="728d3-125">InsertCopy</span></span></td>
<td><span data-ttu-id="728d3-126">Этот флаг заставляет курсор подготовиться к вставке копии существующей записи.</span><span class="sxs-lookup"><span data-stu-id="728d3-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="728d3-127">При использовании этого параметра должна существовать текущая запись.</span><span class="sxs-lookup"><span data-stu-id="728d3-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="728d3-128">Начальное состояние новой записи копируется из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="728d3-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="728d3-129">Длинные значения, хранящиеся за пределами записи, практически копируются.</span><span class="sxs-lookup"><span data-stu-id="728d3-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="728d3-130">инсерткопиделетеоригинал</span><span class="sxs-lookup"><span data-stu-id="728d3-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="728d3-131">Этот флаг заставляет курсор подготовиться к вставке той же записи, а также к удалению или исходной записи.</span><span class="sxs-lookup"><span data-stu-id="728d3-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="728d3-132">Он используется в случаях, когда первичный ключ изменился.</span><span class="sxs-lookup"><span data-stu-id="728d3-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="728d3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="728d3-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="728d3-134">Справочник</span><span class="sxs-lookup"><span data-stu-id="728d3-134">Reference</span></span>

[<span data-ttu-id="728d3-135">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="728d3-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
