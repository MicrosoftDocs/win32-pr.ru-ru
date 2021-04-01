---
description: 'Дополнительные сведения: недопустимые константы Handle'
title: Недопустимые константы Handle
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081416"
---
# <a name="invalid-handle-constants"></a><span data-ttu-id="8c5e3-103">Недопустимые константы Handle</span><span class="sxs-lookup"><span data-stu-id="8c5e3-103">Invalid Handle Constants</span></span>


<span data-ttu-id="8c5e3-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8c5e3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="invalid-handle-constants"></a><span data-ttu-id="8c5e3-105">Недопустимые константы Handle</span><span class="sxs-lookup"><span data-stu-id="8c5e3-105">Invalid Handle Constants</span></span>

<span data-ttu-id="8c5e3-106">Следующие константы указывают недопустимые дескрипторы для различных аспектов ESE.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-106">The following constants indicate invalid handles for different aspects of ESE.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c5e3-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="8c5e3-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="8c5e3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="8c5e3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c5e3-109">JET_instanceNil</span><span class="sxs-lookup"><span data-stu-id="8c5e3-109">JET_instanceNil</span></span><br />
<span data-ttu-id="8c5e3-110">(~ (JET_INSTANCE) 0)</span><span class="sxs-lookup"><span data-stu-id="8c5e3-110">(~(JET_INSTANCE)0)</span></span></p></td>
<td><p><span data-ttu-id="8c5e3-111">Недопустимый обработчик для экземпляра базы данных.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-111">An invalid handle for a database instance.</span></span><br /><span data-ttu-id="8c5e3-112">
<strong>Windows XP:</strong> Впервые появился в Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-112">
<strong>Windows XP:</strong> Introduced in Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5e3-113">JET_sesidNil</span><span class="sxs-lookup"><span data-stu-id="8c5e3-113">JET_sesidNil</span></span><br />
<span data-ttu-id="8c5e3-114">(~ (JET_SESID) 0)</span><span class="sxs-lookup"><span data-stu-id="8c5e3-114">(~(JET_SESID)0)</span></span></p></td>
<td><p><span data-ttu-id="8c5e3-115">Недопустимый обработчик для идентификатора сеанса.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-115">An invalid handle for a session ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5e3-116">JET_tableidNil</span><span class="sxs-lookup"><span data-stu-id="8c5e3-116">JET_tableidNil</span></span><br />
<span data-ttu-id="8c5e3-117">(~ (JET_TABLEID) 0)</span><span class="sxs-lookup"><span data-stu-id="8c5e3-117">(~(JET_TABLEID)0)</span></span></p></td>
<td><p><span data-ttu-id="8c5e3-118">Недопустимый обработчик для идентификатора таблицы.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-118">An invalid handle for a table ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5e3-119">JET_bitNil</span><span class="sxs-lookup"><span data-stu-id="8c5e3-119">JET_bitNil</span></span><br />
<span data-ttu-id="8c5e3-120">((JET_GRBIT) 0)</span><span class="sxs-lookup"><span data-stu-id="8c5e3-120">((JET_GRBIT)0)</span></span></p></td>
<td><p><span data-ttu-id="8c5e3-121">Недопустимый маркер для группы битов.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-121">An invalid handle for a group of bits.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5e3-122">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="8c5e3-122">JET_LSNil</span></span><br />
<span data-ttu-id="8c5e3-123">(~ (JET_LS) 0)</span><span class="sxs-lookup"><span data-stu-id="8c5e3-123">(~(JET_LS)0)</span></span></p></td>
<td><p><span data-ttu-id="8c5e3-124">Недопустимый обработчик для локального хранилища.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-124">An invalid handle for the Local Storage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5e3-125">JET_dbidNil</span><span class="sxs-lookup"><span data-stu-id="8c5e3-125">JET_dbidNil</span></span><br />
<span data-ttu-id="8c5e3-126">((JET_DBID) 0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="8c5e3-126">((JET_DBID) 0xFFFFFFFF)</span></span></p></td>
<td><p><span data-ttu-id="8c5e3-127">Недопустимый обработчик для идентификатора базы данных.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-127">An invalid handle for the database ID.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="8c5e3-128">Требования</span><span class="sxs-lookup"><span data-stu-id="8c5e3-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c5e3-129"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="8c5e3-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5e3-130">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c5e3-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8c5e3-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5e3-132">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c5e3-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8c5e3-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8c5e3-134">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="8c5e3-134">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

