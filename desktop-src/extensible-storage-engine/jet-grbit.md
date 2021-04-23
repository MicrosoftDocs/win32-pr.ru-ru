---
description: 'Дополнительные сведения: JET_GRBIT'
title: JET_GRBIT
TOCTitle: JET_GRBIT
ms:assetid: b72548cf-3ca2-4ba5-b07a-35eb7e85ed2b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294066(v=EXCHG.10)
ms:contentKeyID: 32765681
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
ms.openlocfilehash: b050aaa844ea814c0c24a62ccfb5ab332c611107
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105674761"
---
# <a name="jet_grbit"></a><span data-ttu-id="703cd-103">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="703cd-103">JET_GRBIT</span></span>


<span data-ttu-id="703cd-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="703cd-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_grbit"></a><span data-ttu-id="703cd-105">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="703cd-105">JET_GRBIT</span></span>

<span data-ttu-id="703cd-106">**JET_GRBIT** тип данных — это группа битов, которая содержит константы, характерные для функций и структур, в которых она используется.</span><span class="sxs-lookup"><span data-stu-id="703cd-106">The **JET_GRBIT** data type is a group of bits that contain constants that are specific to the functions and structures in which it is used.</span></span>

```cpp
typedef unsigned long JET_GRBIT;
```

### <a name="data-types"></a><span data-ttu-id="703cd-107">Типы данных</span><span class="sxs-lookup"><span data-stu-id="703cd-107">Data Types</span></span>

<span data-ttu-id="703cd-108">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="703cd-108">JET_GRBIT</span></span>

<span data-ttu-id="703cd-109">Как правило, константы, используемые в качестве значений для этого типа данных, соответствуют имени элемента API, в котором они используются.</span><span class="sxs-lookup"><span data-stu-id="703cd-109">In general, the constants that are used as values for this data type reflect the name of the API element in which they are used.</span></span> <span data-ttu-id="703cd-110">Например, все константы, передаваемые в [жетретриевеколумн](./jetretrievecolumn-function.md) , начинаются с "JET_bitRetrieve".</span><span class="sxs-lookup"><span data-stu-id="703cd-110">For example, all constants passed to [JetRetrieveColumn](./jetretrievecolumn-function.md) begin with "JET_bitRetrieve".</span></span> <span data-ttu-id="703cd-111">Аналогичным образом все константы, передаваемые в [жетсетколумн](./jetsetcolumn-function.md) , начинаются с "JET_bitSet".</span><span class="sxs-lookup"><span data-stu-id="703cd-111">Similarly, all constants passed to [JetSetColumn](./jetsetcolumn-function.md) begin with "JET_bitSet".</span></span>

<span data-ttu-id="703cd-112">Нулевое значение приводит к тому, что параметр игнорируется.</span><span class="sxs-lookup"><span data-stu-id="703cd-112">A value of zero causes the parameter to be ignored.</span></span>

### <a name="remarks"></a><span data-ttu-id="703cd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="703cd-113">Remarks</span></span>

<span data-ttu-id="703cd-114">Дополнительные сведения см. в описании конкретной функции или структуры.</span><span class="sxs-lookup"><span data-stu-id="703cd-114">For more information, see the specific function or structure.</span></span> <span data-ttu-id="703cd-115">Параметры обычно передаются в виде набора флагов, которые можно комбинировать.</span><span class="sxs-lookup"><span data-stu-id="703cd-115">The options are usually passed as a set of flags that can be combined.</span></span>

### <a name="requirements"></a><span data-ttu-id="703cd-116">Требования</span><span class="sxs-lookup"><span data-stu-id="703cd-116">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="703cd-117"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="703cd-117"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="703cd-118">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="703cd-118">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="703cd-119"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="703cd-119"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="703cd-120">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="703cd-120">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="703cd-121"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="703cd-121"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="703cd-122">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="703cd-122">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="703cd-123">См. также:</span><span class="sxs-lookup"><span data-stu-id="703cd-123">See Also</span></span>

[<span data-ttu-id="703cd-124">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="703cd-124">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)  
[<span data-ttu-id="703cd-125">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="703cd-125">JetSetColumn</span></span>](./jetsetcolumn-function.md)
