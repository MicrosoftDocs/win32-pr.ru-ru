---
description: 'Дополнительные сведения: JET_OSSNAPID'
title: JET_OSSNAPID
TOCTitle: JET_OSSNAPID
ms:assetid: 89b15492-674a-46e4-8aea-991df4f22a6f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269325(v=EXCHG.10)
ms:contentKeyID: 32765615
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
ms.openlocfilehash: b0ca1bb5e2e5a80c9166574708efc7875ed95446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702803"
---
# <a name="jet_ossnapid"></a><span data-ttu-id="38786-103">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="38786-103">JET_OSSNAPID</span></span>


<span data-ttu-id="38786-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="38786-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ossnapid"></a><span data-ttu-id="38786-105">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="38786-105">JET_OSSNAPID</span></span>

<span data-ttu-id="38786-106">**JET_OSSNAPID** тип данных содержит маркер моментального снимка базы данных.</span><span class="sxs-lookup"><span data-stu-id="38786-106">The **JET_OSSNAPID** data type contains a handle to a snapshot of the database.</span></span>

```cpp
    typedef JET_API_PTR JET_OSSNAPID;
```

### <a name="data-types"></a><span data-ttu-id="38786-107">Типы данных</span><span class="sxs-lookup"><span data-stu-id="38786-107">Data Types</span></span>

<span data-ttu-id="38786-108">JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="38786-108">JET_OSSNAPID</span></span>

<span data-ttu-id="38786-109">Маркер моментального снимка базы данных.</span><span class="sxs-lookup"><span data-stu-id="38786-109">A handle to a snapshot of the database.</span></span> <span data-ttu-id="38786-110">Этот маркер используется в элементах API JET, которые участвуют в резервном копировании моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="38786-110">This handle is used in JET API elements that are involved with snapshot backup.</span></span>

<span data-ttu-id="38786-111">**Null** можно использовать для указания недопустимого маркера.</span><span class="sxs-lookup"><span data-stu-id="38786-111">**NULL** can be used to indicate an invalid handle.</span></span>

### <a name="requirements"></a><span data-ttu-id="38786-112">Требования</span><span class="sxs-lookup"><span data-stu-id="38786-112">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38786-113"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="38786-113"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="38786-114">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="38786-114">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38786-115"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="38786-115"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="38786-116">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="38786-116">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38786-117"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="38786-117"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="38786-118">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="38786-118">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

