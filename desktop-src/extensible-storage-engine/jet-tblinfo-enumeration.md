---
description: 'Дополнительные сведения: перечисление JET_TblInfo'
title: Перечисление JET_TblInfo
TOCTitle: JET_TblInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_TblInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tblinfo(v=EXCHG.10)
ms:contentKeyID: 39512198
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TblInfo
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Dbid
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Default
- Microsoft.Isam.Esent.Interop.JET_TblInfo.TemplateTableName
- Microsoft.Isam.Esent.Interop.JET_TblInfo.Name
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceUsage
- Microsoft.Isam.Esent.Interop.JET_TblInfo.SpaceAlloc
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad43dcecf65fdc9fb8dd53bdf686a077e6bdfa8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693149"
---
# <a name="jet_tblinfo-enumeration"></a><span data-ttu-id="9a6c5-103">Перечисление JET_TblInfo</span><span class="sxs-lookup"><span data-stu-id="9a6c5-103">JET_TblInfo enumeration</span></span>

<span data-ttu-id="9a6c5-104">Информационные уровни для получения сведений о таблице с помощью Жетжеттаблеинфо.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-104">Info levels for retrieving table info with JetGetTableInfo.</span></span>

<span data-ttu-id="9a6c5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a6c5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9a6c5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9a6c5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6c5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a6c5-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_TblInfo
'Usage
Dim instance As JET_TblInfo
```

``` csharp
public enum JET_TblInfo
```

## <a name="members"></a><span data-ttu-id="9a6c5-108">Члены</span><span class="sxs-lookup"><span data-stu-id="9a6c5-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="9a6c5-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="9a6c5-109">Member name</span></span></th>
<th><span data-ttu-id="9a6c5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9a6c5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9a6c5-111">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="9a6c5-111">Default</span></span></td>
<td><span data-ttu-id="9a6c5-112">Параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-112">Default option.</span></span> <span data-ttu-id="9a6c5-113">Извлекает <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> , содержащий сведения о таблице.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-113">Retrieves a <a href="dn335219(v=exchg.10).md">JET_OBJECTINFO</a> containing information about the table.</span></span> <span data-ttu-id="9a6c5-114">Используйте этот параметр с <a href="dn292198(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-114">Use this option with <a href="dn292198(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9a6c5-115">Имя</span><span class="sxs-lookup"><span data-stu-id="9a6c5-115">Name</span></span></td>
<td><span data-ttu-id="9a6c5-116">Возвращает имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-116">Retrieves the name of the table.</span></span> <span data-ttu-id="9a6c5-117">Используйте этот параметр с <a href="dn292204(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-117">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9a6c5-118">Dbid</span><span class="sxs-lookup"><span data-stu-id="9a6c5-118">Dbid</span></span></td>
<td><span data-ttu-id="9a6c5-119">Возвращает <a href="hh596176(v=exchg.10).md">JET_DBID</a> базы данных, содержащей таблицу.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-119">Retrieves the <a href="hh596176(v=exchg.10).md">JET_DBID</a> of the database containing the table.</span></span> <span data-ttu-id="9a6c5-120">Используйте этот параметр с <a href="dn292197(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-120">Use this option with <a href="dn292197(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9a6c5-121">спацеусаже</span><span class="sxs-lookup"><span data-stu-id="9a6c5-121">SpaceUsage</span></span></td>
<td><span data-ttu-id="9a6c5-122">Поведение метода зависит от того, насколько велик массив, передаваемый в метод.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-122">The behavior of the method depends on how large the array that is passed to the method is.</span></span> <span data-ttu-id="9a6c5-123">Массив должен содержать по крайней мере две записи.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-123">The array must have at least two entries.</span></span> <span data-ttu-id="9a6c5-124">Первая запись будет содержать число принадлежащих ей экстентов в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-124">The first entry will contain the number of Owned Extents in the table.</span></span> <span data-ttu-id="9a6c5-125">Вторая запись будет содержать количество доступных экстентов в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-125">The second entry will contain the number of Available Extents in the table.</span></span> <span data-ttu-id="9a6c5-126">Если массив содержит более двух записей, остальные байты буфера будут состоять из массива структур, представляющих список экстентов.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-126">If the array has more than two entries then the remaining bytes of the buffer will consist of an array of structures that represent a list of extents.</span></span> <span data-ttu-id="9a6c5-127">Эта структура содержит два члена: номер последней страницы в экстенте и количество страниц в экстенте.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-127">This structure contains two members: the last page number in the extent and the number of pages in the extent.</span></span> <span data-ttu-id="9a6c5-128">Используйте этот параметр с <a href="dn292202(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-128">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9a6c5-129">спацеаллок</span><span class="sxs-lookup"><span data-stu-id="9a6c5-129">SpaceAlloc</span></span></td>
<td><span data-ttu-id="9a6c5-130">Массив, переданный в Жетжеттаблеинфо, должен содержать две записи.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-130">The array passed to JetGetTableInfo must have two entries.</span></span> <span data-ttu-id="9a6c5-131">В первой записи будет задано количество страниц в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-131">The first entry will be set to the number of pages in the table.</span></span> <span data-ttu-id="9a6c5-132">Для второй записи будет задана Целевая плотность страниц таблицы.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-132">The second entry will be set to the target density of pages for the table.</span></span> <span data-ttu-id="9a6c5-133">Используйте этот параметр с <a href="dn292202(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-133">Use this option with <a href="dn292202(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, [], JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9a6c5-134">спацеовнед</span><span class="sxs-lookup"><span data-stu-id="9a6c5-134">SpaceOwned</span></span></td>
<td><span data-ttu-id="9a6c5-135">Возвращает число принадлежащих страниц в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-135">Gets the number of owned pages in the table.</span></span> <span data-ttu-id="9a6c5-136">Используйте этот параметр с <a href="dn292201(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-136">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="9a6c5-137">спацеаваилабле</span><span class="sxs-lookup"><span data-stu-id="9a6c5-137">SpaceAvailable</span></span></td>
<td><span data-ttu-id="9a6c5-138">Возвращает количество доступных страниц в таблице.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-138">Gets the number of available pages in the table.</span></span> <span data-ttu-id="9a6c5-139">Используйте этот параметр с <a href="dn292201(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-139">Use this option with <a href="dn292201(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a>.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="9a6c5-140">темплатетабленаме</span><span class="sxs-lookup"><span data-stu-id="9a6c5-140">TemplateTableName</span></span></td>
<td><span data-ttu-id="9a6c5-141">Если таблица является производной, то результат будет заполняться именем таблицы, из которой производная таблица наследовала ее DDL.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-141">If the table is a derived table, the result will be filled in with the name of the table from which the derived table inherited its DDL.</span></span> <span data-ttu-id="9a6c5-142">Если таблица не является производной, буфер будет пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-142">If the table is not a derived table, the buffer will an empty string.</span></span> <span data-ttu-id="9a6c5-143">Используйте этот параметр с <a href="dn292204(v=exchg.10).md">жетжеттаблеинфо (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span><span class="sxs-lookup"><span data-stu-id="9a6c5-143">Use this option with <a href="dn292204(v=exchg.10).md">JetGetTableInfo(JET_SESID, JET_TABLEID, String, JET_TblInfo)</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="9a6c5-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a6c5-144">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a6c5-145">Справочник</span><span class="sxs-lookup"><span data-stu-id="9a6c5-145">Reference</span></span>

[<span data-ttu-id="9a6c5-146">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9a6c5-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
