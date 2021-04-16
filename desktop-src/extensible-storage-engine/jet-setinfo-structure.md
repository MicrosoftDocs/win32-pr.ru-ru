---
description: 'Дополнительные сведения: структура JET_SETINFO'
title: Структура JET_SETINFO
TOCTitle: JET_SETINFO Structure
ms:assetid: cbc41175-e48f-46b0-aeb1-1120fa2cd981
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294090(v=EXCHG.10)
ms:contentKeyID: 32765705
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
ms.openlocfilehash: 69602aad89142d9f5dc202074ca54cf278767892
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548183"
---
# <a name="jet_setinfo-structure"></a><span data-ttu-id="2e5c8-103">Структура JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="2e5c8-103">JET_SETINFO Structure</span></span>


<span data-ttu-id="2e5c8-104">_**Применимо к:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2e5c8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_setinfo-structure"></a><span data-ttu-id="2e5c8-105">Структура JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="2e5c8-105">JET_SETINFO Structure</span></span>

<span data-ttu-id="2e5c8-106">Структура **JET_SETINFO** содержит необязательные входные параметры для [жетсетколумн](./jetsetcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c8-106">The **JET_SETINFO** structure contains optional input parameters for [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="2e5c8-107">Указатель **null** можно передать, где в противном случае будет передан указатель на эту структуру.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-107">A **NULL** pointer can be passed where a pointer to this structure would otherwise be passed.</span></span> <span data-ttu-id="2e5c8-108">Значение передачи **значения NULL** аналогично передаче **JET_SETINFO** с параметром **кбструкт** , равным sizeof (JET_SETINFO), **иблонгвалуе** имеет значение 0 (ноль), а **итагсекуенце** — значение 1.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-108">The meaning of passing a **NULL** is the same as passing **JET_SETINFO** with **cbStruct** set to sizeof(JET_SETINFO), **ibLongValue** set to 0 (zero) and **itagSequence** set to 1.</span></span>

```cpp
typedef struct {
  unsigned long cbStruct;
  unsigned long ibLongValue;
  unsigned long itagSequence;
} JET_SETINFO;
```

### <a name="members"></a><span data-ttu-id="2e5c8-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="2e5c8-109">Members</span></span>

<span data-ttu-id="2e5c8-110">**кбструкт**</span><span class="sxs-lookup"><span data-stu-id="2e5c8-110">**cbStruct**</span></span>

<span data-ttu-id="2e5c8-111">Размер **JET_SETINFO** в байтах.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-111">The size, in bytes, of the **JET_SETINFO**.</span></span> <span data-ttu-id="2e5c8-112">Это значение подтверждает наличие следующих полей.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-112">This value confirms the presence of the following fields.</span></span>

<span data-ttu-id="2e5c8-113">**иблонгвалуе**</span><span class="sxs-lookup"><span data-stu-id="2e5c8-113">**ibLongValue**</span></span>

<span data-ttu-id="2e5c8-114">Смещение к первому байту, заданному в столбце типа [JET_coltypLongBinary](./jet-coltyp.md) или [JET_coltypLongText](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="2e5c8-114">The offset to the first byte to be set in a column of type [JET_coltypLongBinary](./jet-coltyp.md) or [JET_coltypLongText](./jet-coltyp.md).</span></span>

<span data-ttu-id="2e5c8-115">**итагсекуенце**</span><span class="sxs-lookup"><span data-stu-id="2e5c8-115">**itagSequence**</span></span>

<span data-ttu-id="2e5c8-116">Описывает порядковый номер значения в столбце с несколькими значениями, который необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-116">Describes the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="2e5c8-117">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-117">The array of values is one-based.</span></span> <span data-ttu-id="2e5c8-118">Первое значение — Sequence 1, а не 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="2e5c8-118">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="2e5c8-119">Если столбец записи имеет только одно значение, то значение 1 должно передаваться как **итагсекуенце** при замене этого значения.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-119">If the record column has only one value then 1 should be passed as the **itagSequence** if that value is being replaced.</span></span> <span data-ttu-id="2e5c8-120">Значение 0 (ноль) означает, что новый экземпляр значения столбца добавляется в конец последовательности значений столбцов.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-120">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span>

<span data-ttu-id="2e5c8-121">При использовании столбца, который может содержать несколько значений, в [жетсетколумн](./jetsetcolumn-function.md)можно использовать только порядковый номер больше 1 в [жетсетколумн](./jetsetcolumn-function.md) и [жетретриевеколумн](./jetretrievecolumn-function.md) или 0.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-121">With a column that can contain multiple values, it is only possible to use a sequence number larger than 1 in [JetSetColumn](./jetsetcolumn-function.md) and [JetRetrieveColumn](./jetretrievecolumn-function.md) or 0 in [JetSetColumn](./jetsetcolumn-function.md).</span></span> <span data-ttu-id="2e5c8-122">В текущей реализации обработчика любой столбец, созданный с помощью JET_bitColumnTagged, может содержать несколько значений.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-122">In the current implementation of the engine, any column that was created with JET_bitColumnTagged can contain multiple values.</span></span> <span data-ttu-id="2e5c8-123">Столбцы, созданные JET_bitColumnMultiValued, отличаются от столбцов с многозначными тегами только тем способом, в котором они индексируются.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-123">Columns created with JET_bitColumnMultiValued differ from multi-valued tagged columns only in the way that they are indexed.</span></span> <span data-ttu-id="2e5c8-124">Дополнительные сведения см. в разделе [JET_INDEXCREATE](./jet-indexcreate-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="2e5c8-124">See [JET_INDEXCREATE](./jet-indexcreate-structure.md) for more information.</span></span>

### <a name="requirements"></a><span data-ttu-id="2e5c8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2e5c8-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e5c8-126"><strong>Клиент</strong></span><span class="sxs-lookup"><span data-stu-id="2e5c8-126"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5c8-127">Требуется Windows Vista, Windows XP или Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-127">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e5c8-128"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2e5c8-128"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5c8-129">Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-129">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e5c8-130"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2e5c8-130"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2e5c8-131">Объявлено в ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="2e5c8-131">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2e5c8-132">См. также:</span><span class="sxs-lookup"><span data-stu-id="2e5c8-132">See Also</span></span>

[<span data-ttu-id="2e5c8-133">жетсетколумн</span><span class="sxs-lookup"><span data-stu-id="2e5c8-133">JetSetColumn</span></span>](./jetsetcolumn-function.md)
