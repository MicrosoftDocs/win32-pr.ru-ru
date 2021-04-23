---
description: 'Дополнительные сведения: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662163"
---
# <a name="jet_snp"></a><span data-ttu-id="0bacf-103">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="0bacf-103">JET_SNP</span></span>


<span data-ttu-id="0bacf-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="0bacf-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snp"></a><span data-ttu-id="0bacf-105">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="0bacf-105">JET_SNP</span></span>

<span data-ttu-id="0bacf-106">**JET_SNP** группа констант описывает тип операции, для которой необходимо получить сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="0bacf-106">The **JET_SNP** group of constants describe the type of the operation for which progress information is to be obtained.</span></span> <span data-ttu-id="0bacf-107">Эти константы используются в качестве параметра *SNP* функции обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="0bacf-107">These constants are used as the *snp* parameter of the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0bacf-108">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="0bacf-108">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="0bacf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0bacf-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bacf-110">JET_snpRepair</span><span class="sxs-lookup"><span data-stu-id="0bacf-110">JET_snpRepair</span></span><br />
<span data-ttu-id="0bacf-111">2</span><span class="sxs-lookup"><span data-stu-id="0bacf-111">2</span></span></p></td>
<td><p><span data-ttu-id="0bacf-112">Обратный вызов предназначен для операции исправления.</span><span class="sxs-lookup"><span data-stu-id="0bacf-112">The callback is for a repair operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bacf-113">JET_snpCompact</span><span class="sxs-lookup"><span data-stu-id="0bacf-113">JET_snpCompact</span></span><br />
<span data-ttu-id="0bacf-114">4</span><span class="sxs-lookup"><span data-stu-id="0bacf-114">4</span></span></p></td>
<td><p><span data-ttu-id="0bacf-115">Обратный вызов предназначен для дефрагментации базы данных.</span><span class="sxs-lookup"><span data-stu-id="0bacf-115">The callback is for database defragmentation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bacf-116">JET_snpRestore</span><span class="sxs-lookup"><span data-stu-id="0bacf-116">JET_snpRestore</span></span><br />
<span data-ttu-id="0bacf-117">8</span><span class="sxs-lookup"><span data-stu-id="0bacf-117">8</span></span></p></td>
<td><p><span data-ttu-id="0bacf-118">Обратный вызов предназначен для операции восстановления.</span><span class="sxs-lookup"><span data-stu-id="0bacf-118">The callback is for a restore operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bacf-119">JET_snpBackup</span><span class="sxs-lookup"><span data-stu-id="0bacf-119">JET_snpBackup</span></span><br />
<span data-ttu-id="0bacf-120">9</span><span class="sxs-lookup"><span data-stu-id="0bacf-120">9</span></span></p></td>
<td><p><span data-ttu-id="0bacf-121">Обратный вызов предназначен для операции резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="0bacf-121">The callback is for a backup operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bacf-122">JET_snpUpgrade</span><span class="sxs-lookup"><span data-stu-id="0bacf-122">JET_snpUpgrade</span></span><br />
<span data-ttu-id="0bacf-123">10</span><span class="sxs-lookup"><span data-stu-id="0bacf-123">10</span></span></p></td>
<td><p><span data-ttu-id="0bacf-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bacf-124">Not supported.</span></span></p>
<p><span data-ttu-id="0bacf-125"><strong>Windows 2000:</strong>  Обратный вызов предназначен для операции обновления формата базы данных.</span><span class="sxs-lookup"><span data-stu-id="0bacf-125"><strong>Windows 2000:</strong>  The callback is for the database format upgrade operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bacf-126">JET_snpScrub</span><span class="sxs-lookup"><span data-stu-id="0bacf-126">JET_snpScrub</span></span><br />
<span data-ttu-id="0bacf-127">11</span><span class="sxs-lookup"><span data-stu-id="0bacf-127">11</span></span></p></td>
<td><p><span data-ttu-id="0bacf-128">Обратный вызов предназначен для операции обнуления (т. е. очистки) базы данных.</span><span class="sxs-lookup"><span data-stu-id="0bacf-128">The callback is for a database zeroing (that is, scrubbing) operation.</span></span></p>
<p><span data-ttu-id="0bacf-129"><strong>Windows server 2003 и windows 2000 Server:</strong>  Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bacf-129"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bacf-130">JET_snpUpgradeRecordFormat</span><span class="sxs-lookup"><span data-stu-id="0bacf-130">JET_snpUpgradeRecordFormat</span></span><br />
<span data-ttu-id="0bacf-131">12</span><span class="sxs-lookup"><span data-stu-id="0bacf-131">12</span></span></p></td>
<td><p><span data-ttu-id="0bacf-132">Обратный вызов предназначен для процесса обновления формата записей всех страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="0bacf-132">The callback is for the process of upgrading the record format of all database pages.</span></span></p>
<p><span data-ttu-id="0bacf-133"><strong>Windows server 2003 и windows 2000 Server:</strong>  Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0bacf-133"><strong>Windows Server 2003 and Windows 2000 Server:</strong>  Not supported.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="0bacf-134">Требования</span><span class="sxs-lookup"><span data-stu-id="0bacf-134">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0bacf-135"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="0bacf-135"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="0bacf-136">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="0bacf-136">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0bacf-137"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="0bacf-137"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="0bacf-138">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="0bacf-138">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0bacf-139"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="0bacf-139"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="0bacf-140">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="0bacf-140">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="0bacf-141">См. также:</span><span class="sxs-lookup"><span data-stu-id="0bacf-141">See Also</span></span>

[<span data-ttu-id="0bacf-142">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="0bacf-142">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="0bacf-143">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="0bacf-143">JET_SNPROG</span></span>](./jet-snprog-structure.md)  
[<span data-ttu-id="0bacf-144">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="0bacf-144">JET_SNT</span></span>](./jet-snt.md)
