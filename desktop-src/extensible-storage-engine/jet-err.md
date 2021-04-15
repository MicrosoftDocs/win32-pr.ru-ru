---
description: 'Дополнительные сведения: JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105714059"
---
# <a name="jet_err"></a><span data-ttu-id="60912-103">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60912-103">JET_ERR</span></span>


<span data-ttu-id="60912-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="60912-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_err"></a><span data-ttu-id="60912-105">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60912-105">JET_ERR</span></span>

<span data-ttu-id="60912-106">Тип данных **JET_ERR** содержит [Расширенный код ошибки подсистемы хранилища](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="60912-106">The **JET_ERR** data type contains an [Extensible Storage Engine error code](./extensible-storage-engine-error-codes.md).</span></span>

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a><span data-ttu-id="60912-107">Типы данных</span><span class="sxs-lookup"><span data-stu-id="60912-107">Data Types</span></span>

<span data-ttu-id="60912-108">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="60912-108">JET_ERR</span></span>

<span data-ttu-id="60912-109">Нулевое значение (соответствующее JET_errSuccess) указывает на Успешный вызов.</span><span class="sxs-lookup"><span data-stu-id="60912-109">A zero value (corresponding to JET_errSuccess) indicates that the call succeeded.</span></span> <span data-ttu-id="60912-110">Положительное значение предупреждает о некритическом условии, произошедшем при успешном вызове по ошибке.</span><span class="sxs-lookup"><span data-stu-id="60912-110">A positive value warns of a non-fatal condition that occurred during an otherwise successful call.</span></span> <span data-ttu-id="60912-111">Отрицательное значение указывает на сбой вызова.</span><span class="sxs-lookup"><span data-stu-id="60912-111">A negative value indicates that the call failed.</span></span>

### <a name="remarks"></a><span data-ttu-id="60912-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60912-112">Remarks</span></span>

<span data-ttu-id="60912-113">Сведения об возврате ошибок в виде значений HRESULT см. в разделе [ошибки расширенного подсистемы хранилища](./extensible-storage-engine-errors.md).</span><span class="sxs-lookup"><span data-stu-id="60912-113">For information about returning errors as HRESULTs, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md).</span></span> <span data-ttu-id="60912-114">Дополнительные сведения о флагах настройки базы данных для обработки ошибок см. в разделе [Параметры обработки ошибок](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="60912-114">For information about flags for configuring the database to handle errors, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="60912-115">Требования</span><span class="sxs-lookup"><span data-stu-id="60912-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60912-116"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="60912-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="60912-117">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="60912-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60912-118"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="60912-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="60912-119">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="60912-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60912-120"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="60912-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="60912-121">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="60912-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="60912-122">См. также:</span><span class="sxs-lookup"><span data-stu-id="60912-122">See Also</span></span>

[<span data-ttu-id="60912-123">Ошибки расширяемого подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="60912-123">Extensible Storage Engine Errors</span></span>](./extensible-storage-engine-errors.md)  
[<span data-ttu-id="60912-124">Коды ошибок расширенного подсистемы хранилища</span><span class="sxs-lookup"><span data-stu-id="60912-124">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)  
[<span data-ttu-id="60912-125">Параметры обработки ошибок</span><span class="sxs-lookup"><span data-stu-id="60912-125">Error Handling Parameters</span></span>](./error-handling-parameters.md)
