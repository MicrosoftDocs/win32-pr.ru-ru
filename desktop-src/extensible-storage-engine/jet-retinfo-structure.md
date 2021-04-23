---
description: 'Дополнительные сведения: структура JET_RETINFO'
title: Структура JET_RETINFO
TOCTitle: JET_RETINFO Structure
ms:assetid: a47a7902-3ecd-4d42-941f-89d25d78eb4c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294049(v=EXCHG.10)
ms:contentKeyID: 32765648
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
ms.openlocfilehash: 3452c4fab7155ea33b556ac7aa2c777b11a3f954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897734"
---
# <a name="jet_retinfo-structure"></a><span data-ttu-id="85224-103">Структура JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="85224-103">JET_RETINFO Structure</span></span>


<span data-ttu-id="85224-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="85224-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_retinfo-structure"></a><span data-ttu-id="85224-105">Структура JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="85224-105">JET_RETINFO Structure</span></span>

<span data-ttu-id="85224-106">Структура **JET_RETINFO** содержит необязательные входные и выходные параметры для [жетретриевеколумн](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="85224-106">The **JET_RETINFO** structure contains optional input and output parameters for [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span> <span data-ttu-id="85224-107">Указатель NULL можно передать, где в противном случае будет передан указатель на эту структуру.</span><span class="sxs-lookup"><span data-stu-id="85224-107">A null pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="85224-108">Передача пустого указателя аналогична передаче **JET_RETINFO** с параметром **кбструкт** , для которого задано значение sizeof (JET_RETINFO), **иблонгвалуе** имеет значение 0 (ноль), а **итагсекуенце** — значение 1.</span><span class="sxs-lookup"><span data-stu-id="85224-108">Passing a null pointer is the same as passing **JET_RETINFO** with **cbStruct** set to sizeof(JET_RETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
    } JET_RETINFO;
```

### <a name="members"></a><span data-ttu-id="85224-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="85224-109">Members</span></span>

<span data-ttu-id="85224-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="85224-110">**cbStruct**</span></span>

<span data-ttu-id="85224-111">Необходимо задать размер структуры **JET_RETINFO** (в байтах) и выполнить для подтверждения наличия следующих полей.</span><span class="sxs-lookup"><span data-stu-id="85224-111">Must be set to the size of the **JET_RETINFO** structure, in bytes, and serves to confirm the presence of the following fields.</span></span>

<span data-ttu-id="85224-112">**иблонгвалуе**</span><span class="sxs-lookup"><span data-stu-id="85224-112">**ibLongValue**</span></span>

<span data-ttu-id="85224-113">Смещение для первого байта, получаемого из столбца типа [JET_coltypLongBinary](./jet-coltyp.md)или [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="85224-113">The offset to the first byte to be retrieved from a column of type [JET_coltypLongBinary](./jet-coltyp.md), or [JET_coltypLongText](./jet-coltyp.md).</span></span> <span data-ttu-id="85224-114">Обратите внимание, что объем данных, извлекаемых с этого смещения, — это Нижняя часть размера выходного буфера и размер данных в фактическом значении после этого смещения.</span><span class="sxs-lookup"><span data-stu-id="85224-114">Note that the amount of data retrieved from this offset is the lower of the size of the output buffer and the size of data in the actual value after this offset.</span></span>

<span data-ttu-id="85224-115">**итагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="85224-115">**itagSequence**</span></span>

<span data-ttu-id="85224-116">Описывает порядковый номер значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="85224-116">Describes the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="85224-117">Обратите внимание, что массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="85224-117">Note that the array of values is one-based.</span></span> <span data-ttu-id="85224-118">Первое значение — Sequence 1, а не 0.</span><span class="sxs-lookup"><span data-stu-id="85224-118">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="85224-119">Если столбец записи имеет только одно значение, то в качестве **итагсекуенце** передается 1.</span><span class="sxs-lookup"><span data-stu-id="85224-119">If the record column has only one value then 1 should be passed as the **itagSequence**</span></span>

<span data-ttu-id="85224-120">При использовании столбца, который может содержать несколько значений, в [жетсетколумн](./jetsetcolumn-function.md)можно использовать только порядковый номер больше 1 в [жетсетколумн](./jetsetcolumn-function.md) и [жетретриевеколумн](./jetretrievecolumn-function.md) или 0.</span><span class="sxs-lookup"><span data-stu-id="85224-120">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="85224-121">В текущей реализации обработчика любой столбец, созданный с помощью JET_bitColumnTagged, может содержать несколько значений.</span><span class="sxs-lookup"><span data-stu-id="85224-121">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="85224-122">Столбцы, созданные JET_bitColumnMultiValued, отличаются от столбцов с многозначными тегами только тем способом, в котором они индексируются.</span><span class="sxs-lookup"><span data-stu-id="85224-122">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="85224-123">Дополнительные сведения см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="85224-123">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

<span data-ttu-id="85224-124">**колумниднексттагжед**</span><span class="sxs-lookup"><span data-stu-id="85224-124">**columnidNextTagged**</span></span>

<span data-ttu-id="85224-125">Возвращает значение columnid полученного помеченного, многозначного или разреженного столбца, если все отмеченные столбцы извлекаются путем передачи 0 в качестве значения columnid в [жетретриевеколумн](./jetretrievecolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="85224-125">Returns the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to [JetRetrieveColumn](./jetretrievecolumn-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="85224-126">Требования</span><span class="sxs-lookup"><span data-stu-id="85224-126">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85224-127"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="85224-127"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="85224-128">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="85224-128">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85224-129"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="85224-129"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="85224-130">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="85224-130">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85224-131"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="85224-131"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="85224-132">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="85224-132">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="85224-133">См. также:</span><span class="sxs-lookup"><span data-stu-id="85224-133">See Also</span></span>

[<span data-ttu-id="85224-134">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="85224-134">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="85224-135">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="85224-135">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="85224-136">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="85224-136">JET_RETINFO</span></span>]()  
[<span data-ttu-id="85224-137">жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="85224-137">JetRetrieveColumn</span></span>](./jetretrievecolumn-function.md)
