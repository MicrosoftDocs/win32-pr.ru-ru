---
description: 'Дополнительные сведения: JET_PWSTR'
title: JET_PWSTR
TOCTitle: JET_PWSTR
ms:assetid: 6575f0f0-d022-4e70-9f17-c1d884d9e226
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269271(v=EXCHG.10)
ms:contentKeyID: 32765573
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
ms.openlocfilehash: 536ef3bba465f6d152e3483436c1dc1e82277339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693360"
---
# <a name="jet_pwstr"></a><span data-ttu-id="9322d-103">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="9322d-103">JET_PWSTR</span></span>


<span data-ttu-id="9322d-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="9322d-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_pwstr"></a><span data-ttu-id="9322d-105">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="9322d-105">JET_PWSTR</span></span>

<span data-ttu-id="9322d-106">Тип данных **JET_PWSTR** содержит строку в **Юникоде** , заканчивающуюся символом NULL \* .</span><span class="sxs-lookup"><span data-stu-id="9322d-106">The **JET_PWSTR** data type contains a null-terminated **Unicode** string (char \*).</span></span>

<span data-ttu-id="9322d-107">**Windows Vista: JET_PWSTR** впервые появился в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9322d-107">**Windows Vista:  JET_PWSTR** is introduced in Windows Vista.</span></span>

```cpp
    typedef __nullterminated WCHAR * JET_PWSTR;
```

### <a name="data-types"></a><span data-ttu-id="9322d-108">Типы данных</span><span class="sxs-lookup"><span data-stu-id="9322d-108">Data Types</span></span>

<span data-ttu-id="9322d-109">JET_PWSTR</span><span class="sxs-lookup"><span data-stu-id="9322d-109">JET_PWSTR</span></span>

<span data-ttu-id="9322d-110">Заканчивающийся нулем, строка в Юникоде (char \* ).</span><span class="sxs-lookup"><span data-stu-id="9322d-110">Null-terminated, Unicode string (char \*).</span></span>

### <a name="requirements"></a><span data-ttu-id="9322d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="9322d-111">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9322d-112"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="9322d-112"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="9322d-113">Требуется Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9322d-113">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9322d-114"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="9322d-114"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="9322d-115">Требуется Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9322d-115">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9322d-116"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="9322d-116"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="9322d-117">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="9322d-117">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

