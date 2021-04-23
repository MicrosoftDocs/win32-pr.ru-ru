---
description: 'Дополнительные сведения: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262868"
---
# <a name="jet_snt"></a><span data-ttu-id="20ead-103">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="20ead-103">JET_SNT</span></span>


<span data-ttu-id="20ead-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="20ead-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_snt"></a><span data-ttu-id="20ead-105">JET_SNT</span><span class="sxs-lookup"><span data-stu-id="20ead-105">JET_SNT</span></span>

<span data-ttu-id="20ead-106">[JET_SNT]() группа констант описывает точки выполнения операции, сведения о которой запрашиваются при вызове функции обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .</span><span class="sxs-lookup"><span data-stu-id="20ead-106">The [JET_SNT]() group of constants describe the points of the progress of an operation about which information is requested in a call to the [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) callback function.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20ead-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="20ead-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="20ead-108">Описание</span><span class="sxs-lookup"><span data-stu-id="20ead-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20ead-109">JET_sntBegin</span><span class="sxs-lookup"><span data-stu-id="20ead-109">JET_sntBegin</span></span><br />
<span data-ttu-id="20ead-110">5</span><span class="sxs-lookup"><span data-stu-id="20ead-110">5</span></span></p></td>
<td><p><span data-ttu-id="20ead-111">Начало операции</span><span class="sxs-lookup"><span data-stu-id="20ead-111">The beginning of an operation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20ead-112">JET_sntRequirements</span><span class="sxs-lookup"><span data-stu-id="20ead-112">JET_sntRequirements</span></span><br />
<span data-ttu-id="20ead-113">7</span><span class="sxs-lookup"><span data-stu-id="20ead-113">7</span></span></p></td>
<td><p><span data-ttu-id="20ead-114">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="20ead-114">Not supported.</span></span></p>
<p><span data-ttu-id="20ead-115"><strong>Сервер Windows 2000:</strong>  Операция запущена.</span><span class="sxs-lookup"><span data-stu-id="20ead-115"><strong>Windows 2000 Server:</strong>  The operation is started.</span></span> <span data-ttu-id="20ead-116">В этом случае последний параметр функции обратного вызова должен быть допустимым указателем на <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> структуру, указывающую общее количество единиц для выполнения.</span><span class="sxs-lookup"><span data-stu-id="20ead-116">In this case, the last parameter of the callback function should be a valid pointer to a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure indicating the total number of units to be executed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20ead-117">JET_sntProgress</span><span class="sxs-lookup"><span data-stu-id="20ead-117">JET_sntProgress</span></span><br />
<span data-ttu-id="20ead-118">0</span><span class="sxs-lookup"><span data-stu-id="20ead-118">0</span></span></p></td>
<td><p><span data-ttu-id="20ead-119">Число завершенных единиц и количество единиц, которые еще не были выполнены.</span><span class="sxs-lookup"><span data-stu-id="20ead-119">The number of units completed and number of units yet to be done.</span></span> <span data-ttu-id="20ead-120">Эти сведения возвращаются в элементах структуры <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</span><span class="sxs-lookup"><span data-stu-id="20ead-120">This information is returned in the members of a <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> structure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20ead-121">JET_sntComplete</span><span class="sxs-lookup"><span data-stu-id="20ead-121">JET_sntComplete</span></span><br />
<span data-ttu-id="20ead-122">6</span><span class="sxs-lookup"><span data-stu-id="20ead-122">6</span></span></p></td>
<td><p><span data-ttu-id="20ead-123">Завершение операции.</span><span class="sxs-lookup"><span data-stu-id="20ead-123">The completion of an operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20ead-124">JET_sntFail</span><span class="sxs-lookup"><span data-stu-id="20ead-124">JET_sntFail</span></span><br />
<span data-ttu-id="20ead-125">3</span><span class="sxs-lookup"><span data-stu-id="20ead-125">3</span></span></p></td>
<td><p><span data-ttu-id="20ead-126">Сбой операции.</span><span class="sxs-lookup"><span data-stu-id="20ead-126">The failure of an operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20ead-127">JET_sntRecoveryStep</span><span class="sxs-lookup"><span data-stu-id="20ead-127">JET_sntRecoveryStep</span></span><br />
<span data-ttu-id="20ead-128">8</span><span class="sxs-lookup"><span data-stu-id="20ead-128">8</span></span></p></td>
<td><p><span data-ttu-id="20ead-129">Управление восстановлением операции.</span><span class="sxs-lookup"><span data-stu-id="20ead-129">The recovery control of an operation.</span></span></p>
<div class="alert">

> [!NOTE]
> <P><span data-ttu-id="20ead-130">Это значение неприменимо к версиям операционной системы Windows, начиная с Windows 8.</span><span class="sxs-lookup"><span data-stu-id="20ead-130">This value is not applicable to versions of the Windows operating system starting with Windows 8.</span></span></P>


</div></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="20ead-131">Требования</span><span class="sxs-lookup"><span data-stu-id="20ead-131">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20ead-132"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="20ead-132"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="20ead-133">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="20ead-133">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20ead-134"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="20ead-134"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="20ead-135">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="20ead-135">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20ead-136"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="20ead-136"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="20ead-137">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="20ead-137">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="20ead-138">См. также:</span><span class="sxs-lookup"><span data-stu-id="20ead-138">See Also</span></span>

[<span data-ttu-id="20ead-139">JET_PFNSTATUS</span><span class="sxs-lookup"><span data-stu-id="20ead-139">JET_PFNSTATUS</span></span>](./jet-pfnstatus-callback-function.md)  
[<span data-ttu-id="20ead-140">JET_SNP</span><span class="sxs-lookup"><span data-stu-id="20ead-140">JET_SNP</span></span>](./jet-snp.md)  
[<span data-ttu-id="20ead-141">JET_SNPROG</span><span class="sxs-lookup"><span data-stu-id="20ead-141">JET_SNPROG</span></span>](./jet-snprog-structure.md)
