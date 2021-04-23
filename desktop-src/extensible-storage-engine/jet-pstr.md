---
description: 'Дополнительные сведения: JET_PSTR'
title: JET_PSTR
TOCTitle: JET_PSTR
ms:assetid: acb1143f-a5ee-4088-9f05-cc2aeef23442
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294056(v=EXCHG.10)
ms:contentKeyID: 32765667
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
ms.openlocfilehash: 6bbed2cad9f9c7816d010a429b1db8eb5306fc1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693526"
---
# <a name="jet_pstr"></a><span data-ttu-id="6c8b3-103">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="6c8b3-103">JET_PSTR</span></span>


<span data-ttu-id="6c8b3-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="6c8b3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pstr"></a><span data-ttu-id="6c8b3-105">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="6c8b3-105">JET_PSTR</span></span>

<span data-ttu-id="6c8b3-106">Тип данных JET_PSTR содержит строку ASCII, завершающуюся нулем (char \* ).</span><span class="sxs-lookup"><span data-stu-id="6c8b3-106">The JET_PSTR data type contains a null-terminated ASCII string (char \*).</span></span>

<span data-ttu-id="6c8b3-107">**Windows Vista: JET_PSTR** впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-107">**Windows Vista:  JET_PSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated char *  JET_PSTR;
```

### <a name="data-types"></a><span data-ttu-id="6c8b3-108">Типы данных</span><span class="sxs-lookup"><span data-stu-id="6c8b3-108">Data Types</span></span>

<span data-ttu-id="6c8b3-109">JET_PSTR</span><span class="sxs-lookup"><span data-stu-id="6c8b3-109">JET_PSTR</span></span>

<span data-ttu-id="6c8b3-110">Строка ASCII, заканчивающаяся символом NULL \* .</span><span class="sxs-lookup"><span data-stu-id="6c8b3-110">Null-terminated, ASCII string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="6c8b3-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6c8b3-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c8b3-112"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="6c8b3-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="6c8b3-113">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c8b3-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="6c8b3-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="6c8b3-115">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c8b3-116"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="6c8b3-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="6c8b3-117">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="6c8b3-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

