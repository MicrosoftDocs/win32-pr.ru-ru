---
description: 'Дополнительные сведения: перечисление JET_DbInfo'
title: Перечисление JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701488"
---
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="42891-103">Перечисление JET_DbInfo</span><span class="sxs-lookup"><span data-stu-id="42891-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="42891-104">Информационные уровни для получения сведений о базе данных.</span><span class="sxs-lookup"><span data-stu-id="42891-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="42891-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42891-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42891-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42891-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42891-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42891-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="42891-108">Члены</span><span class="sxs-lookup"><span data-stu-id="42891-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="42891-109">Имя участника</span><span class="sxs-lookup"><span data-stu-id="42891-109">Member name</span></span></th>
<th><span data-ttu-id="42891-110">Описание</span><span class="sxs-lookup"><span data-stu-id="42891-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42891-111">Имя файла</span><span class="sxs-lookup"><span data-stu-id="42891-111">Filename</span></span></td>
<td><span data-ttu-id="42891-112">Возвращает путь к файлу базы данных (строка).</span><span class="sxs-lookup"><span data-stu-id="42891-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42891-113">LCID</span><span class="sxs-lookup"><span data-stu-id="42891-113">LCID</span></span></td>
<td><span data-ttu-id="42891-114">Возвращает код локали (LCID), связанный с этой базой данных (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42891-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="42891-115">Options</span></span></td>
<td><span data-ttu-id="42891-116">Возвращает <a href="hh579532(v=exchg.10).md">опендатабасегрбит</a>.</span><span class="sxs-lookup"><span data-stu-id="42891-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="42891-117">Указывает, открыта ли база данных в монопольном режиме.</span><span class="sxs-lookup"><span data-stu-id="42891-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="42891-118">Если база данных находится в монопольном режиме, будет возвращен <a href="hh579532(v=exchg.10).md">монопольный</a> режим, в противном случае возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="42891-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="42891-119">Другие параметры грбит базы данных для Жетаттачдатабасе и Жетопендатабасе не возвращаются.</span><span class="sxs-lookup"><span data-stu-id="42891-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42891-120">Transactions</span><span class="sxs-lookup"><span data-stu-id="42891-120">Transactions</span></span></td>
<td><span data-ttu-id="42891-121">Возвращает число, которое больше, чем максимальный уровень, до которого транзакции могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="42891-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="42891-122">Если вызывается <a href="dn292105(v=exchg.10).md">жетбегинтрансактион (JET_SESID)</a> (во вложенном режиме, то есть в том же сеансе без фиксации или отката), то при последнем вызове <a href="hh564840(v=exchg.10).md">транстудип</a> будет возвращено значение (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42891-123">Версия</span><span class="sxs-lookup"><span data-stu-id="42891-123">Version</span></span></td>
<td><span data-ttu-id="42891-124">Возвращает основной номер версии ядра СУБД (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42891-125">Размер файла</span><span class="sxs-lookup"><span data-stu-id="42891-125">Filesize</span></span></td>
<td><span data-ttu-id="42891-126">Возвращает размер файла базы данных на страницах (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42891-127">спацеовнед</span><span class="sxs-lookup"><span data-stu-id="42891-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="42891-128">Возвращает пространство, принадлежащее базе данных, на страницах (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42891-129">спацеаваилабле</span><span class="sxs-lookup"><span data-stu-id="42891-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="42891-130">Возвращает доступное пространство в базе данных на страницах (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42891-131">Разное</span><span class="sxs-lookup"><span data-stu-id="42891-131">Misc</span></span></td>
<td><span data-ttu-id="42891-132">Возвращает объект <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</span><span class="sxs-lookup"><span data-stu-id="42891-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42891-133">дбинусе</span><span class="sxs-lookup"><span data-stu-id="42891-133">DBInUse</span></span></td>
<td><span data-ttu-id="42891-134">Возвращает логическое значение, указывающее, присоединена ли база данных (логический).</span><span class="sxs-lookup"><span data-stu-id="42891-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="42891-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="42891-135">PageSize</span></span></td>
<td><span data-ttu-id="42891-136">Возвращает размер страницы базы данных (Int32).</span><span class="sxs-lookup"><span data-stu-id="42891-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="42891-137">FileType</span><span class="sxs-lookup"><span data-stu-id="42891-137">FileType</span></span></td>
<td><span data-ttu-id="42891-138">Возвращает тип базы данных (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span><span class="sxs-lookup"><span data-stu-id="42891-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="42891-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42891-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42891-140">Справочник</span><span class="sxs-lookup"><span data-stu-id="42891-140">Reference</span></span>

[<span data-ttu-id="42891-141">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="42891-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
