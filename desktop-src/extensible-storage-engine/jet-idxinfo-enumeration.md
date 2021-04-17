---
description: 'Дополнительные сведения: перечисление JET_IdxInfo'
title: Перечисление JET_IdxInfo
TOCTitle: JET_IdxInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_IdxInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_idxinfo(v=EXCHG.10)
ms:contentKeyID: 39512789
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.IndexId
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_IdxInfo
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.List
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.VarSegMac
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.KeyMost
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.OLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.ResetOLC
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.SysTabCursor
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Count
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Default
- Microsoft.Isam.Esent.Interop.JET_IdxInfo.Langid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1f2cb50537ed492a428c82fd9a6f6541c5fad2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712883"
---
# <a name="jet_idxinfo-enumeration"></a><span data-ttu-id="cb1b3-103">Перечисление JET_IdxInfo</span><span class="sxs-lookup"><span data-stu-id="cb1b3-103">JET_IdxInfo enumeration</span></span>

<span data-ttu-id="cb1b3-104">Информационные уровни для получения сведений об индексе с помощью Жетжетиндексинфо.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-104">Info levels for retrieve index information with JetGetIndexInfo.</span></span> <span data-ttu-id="cb1b3-105">и Жетжеттаблеиндексинфо.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-105">and JetGetTableIndexInfo.</span></span>

<span data-ttu-id="cb1b3-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cb1b3-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cb1b3-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cb1b3-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cb1b3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb1b3-108">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_IdxInfo
'Usage
Dim instance As JET_IdxInfo
```

``` csharp
public enum JET_IdxInfo
```

## <a name="members"></a><span data-ttu-id="cb1b3-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cb1b3-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="cb1b3-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="cb1b3-110">Member name</span></span></th>
<th><span data-ttu-id="cb1b3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="cb1b3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb1b3-112">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cb1b3-112">Default</span></span></td>
<td><span data-ttu-id="cb1b3-113">Возвращает структуру <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> со сведениями об индексе.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-113">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb1b3-114">Список</span><span class="sxs-lookup"><span data-stu-id="cb1b3-114">List</span></span></td>
<td><span data-ttu-id="cb1b3-115">Возвращает структуру <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> со сведениями об индексе.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-115">Returns a <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a> structure with information about the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb1b3-116">систабкурсор</span><span class="sxs-lookup"><span data-stu-id="cb1b3-116">SysTabCursor</span></span></td>
<td><span data-ttu-id="cb1b3-117"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="cb1b3-117"><strong>Obsolete.</strong></span></span> <span data-ttu-id="cb1b3-118">Систабкурсор устарел.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-118">SysTabCursor is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb1b3-119">олк</span><span class="sxs-lookup"><span data-stu-id="cb1b3-119">OLC</span></span></td>
<td><span data-ttu-id="cb1b3-120"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="cb1b3-120"><strong>Obsolete.</strong></span></span> <span data-ttu-id="cb1b3-121">ОЛК устарел.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-121">OLC is obsolete.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb1b3-122">ресетолк</span><span class="sxs-lookup"><span data-stu-id="cb1b3-122">ResetOLC</span></span></td>
<td><span data-ttu-id="cb1b3-123"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="cb1b3-123"><strong>Obsolete.</strong></span></span> <span data-ttu-id="cb1b3-124">Сброс ОЛК устарел.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-124">Reset OLC is obsolete.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb1b3-125">спацеаллок</span><span class="sxs-lookup"><span data-stu-id="cb1b3-125">SpaceAlloc</span></span></td>
<td><span data-ttu-id="cb1b3-126">Возвращает целое число с использованием пространства индекса.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-126">Returns an integer with the space usage of the index.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb1b3-127">LCID</span><span class="sxs-lookup"><span data-stu-id="cb1b3-127">LCID</span></span></td>
<td><span data-ttu-id="cb1b3-128">Возвращает целое число с идентификатором LCID индекса.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-128">Returns an integer with the LCID of the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb1b3-129">Надежно</span><span class="sxs-lookup"><span data-stu-id="cb1b3-129">Langid</span></span></td>
<td><span data-ttu-id="cb1b3-130"><strong>Устарело.</strong></span><span class="sxs-lookup"><span data-stu-id="cb1b3-130"><strong>Obsolete.</strong></span></span> <span data-ttu-id="cb1b3-131">LangID устарел.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-131">Langid is obsolete.</span></span> <span data-ttu-id="cb1b3-132">Вместо этого используйте LCID.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-132">Use LCID instead.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb1b3-133">Count</span><span class="sxs-lookup"><span data-stu-id="cb1b3-133">Count</span></span></td>
<td><span data-ttu-id="cb1b3-134">Возвращает целое число с числом индексов в таблице.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-134">Returns an integer with the count of indexes in the table.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb1b3-135">варсегмак</span><span class="sxs-lookup"><span data-stu-id="cb1b3-135">VarSegMac</span></span></td>
<td><span data-ttu-id="cb1b3-136">Возвращает значение ushort со значением Кбварсегмак, с которым был создан индекс.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-136">Returns a ushort with the value of cbVarSegMac the index was created with.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="cb1b3-137">IndexId</span><span class="sxs-lookup"><span data-stu-id="cb1b3-137">IndexId</span></span></td>
<td><span data-ttu-id="cb1b3-138">Возвращает <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> , определяющую индекс.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-138">Returns a <a href="hh557060(v=exchg.10).md">JET_INDEXID</a> identifying the index.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="cb1b3-139">кэймост</span><span class="sxs-lookup"><span data-stu-id="cb1b3-139">KeyMost</span></span></td>
<td><span data-ttu-id="cb1b3-140">Впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-140">Introduced in Windows Vista.</span></span> <span data-ttu-id="cb1b3-141">Возвращает значение ushort со значением Кбкэймост, с которым был создан индекс.</span><span class="sxs-lookup"><span data-stu-id="cb1b3-141">Returns a ushort with the value of cbKeyMost the index was created with.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cb1b3-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb1b3-142">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cb1b3-143">Справочник</span><span class="sxs-lookup"><span data-stu-id="cb1b3-143">Reference</span></span>

[<span data-ttu-id="cb1b3-144">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cb1b3-144">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
