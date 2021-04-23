---
description: 'Дополнительные сведения: JET_PCSTR'
title: JET_PCSTR
TOCTitle: JET_PCSTR
ms:assetid: 5826e6b9-5297-421f-abaa-016708bf16f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269254(v=EXCHG.10)
ms:contentKeyID: 32765556
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
ms.openlocfilehash: 2786435822fefb56b09c3bb434612dc1fbf13f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272861"
---
# <a name="jet_pcstr"></a><span data-ttu-id="5f4b4-103">JET_PCSTR</span><span class="sxs-lookup"><span data-stu-id="5f4b4-103">JET_PCSTR</span></span>


<span data-ttu-id="5f4b4-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="5f4b4-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pcstr"></a><span data-ttu-id="5f4b4-105">JET_PCSTR</span><span class="sxs-lookup"><span data-stu-id="5f4b4-105">JET_PCSTR</span></span>

<span data-ttu-id="5f4b4-106">Тип данных **JET_PCSTR** содержит константную строку **ASCII** с завершающим нулем (символ \* ).</span><span class="sxs-lookup"><span data-stu-id="5f4b4-106">The **JET_PCSTR** data type contains a null-terminated, constant **ASCII** string (char \*).</span></span>

<span data-ttu-id="5f4b4-107">**Windows Vista: JET_PCSTR** впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-107">**Windows Vista:  JET_PCSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated const char *  JET_PCSTR;
```

### <a name="data-types"></a><span data-ttu-id="5f4b4-108">Типы данных</span><span class="sxs-lookup"><span data-stu-id="5f4b4-108">Data Types</span></span>

<span data-ttu-id="5f4b4-109">JET_PCSTR</span><span class="sxs-lookup"><span data-stu-id="5f4b4-109">JET_PCSTR</span></span>

<span data-ttu-id="5f4b4-110">Строка константы ASCII с завершающим нулем (символ \* ).</span><span class="sxs-lookup"><span data-stu-id="5f4b4-110">Null-terminated, constant ASCII string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="5f4b4-111">Требования</span><span class="sxs-lookup"><span data-stu-id="5f4b4-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f4b4-112"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="5f4b4-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5f4b4-113">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f4b4-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="5f4b4-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5f4b4-115">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f4b4-116"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="5f4b4-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5f4b4-117">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="5f4b4-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

