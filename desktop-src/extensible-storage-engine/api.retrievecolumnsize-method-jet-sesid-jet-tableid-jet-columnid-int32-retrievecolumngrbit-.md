---
description: 'Дополнительные сведения: метод API. Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, Ретриевеколумнгрбит)'
title: Метод API. Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990850"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="153a3-103">Метод API. Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="153a3-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="153a3-104">Получает размер значения одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="153a3-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="153a3-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="153a3-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="153a3-106">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="153a3-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="153a3-107">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="153a3-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="153a3-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="153a3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="153a3-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="153a3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="153a3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="153a3-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="153a3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="153a3-111">Parameters</span></span>

  - <span data-ttu-id="153a3-112">сесид</span><span class="sxs-lookup"><span data-stu-id="153a3-112">sesid</span></span>  
    <span data-ttu-id="153a3-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="153a3-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="153a3-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="153a3-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="153a3-115">TableID</span><span class="sxs-lookup"><span data-stu-id="153a3-115">tableid</span></span>  
    <span data-ttu-id="153a3-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="153a3-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="153a3-117">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="153a3-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="153a3-118">columnid</span><span class="sxs-lookup"><span data-stu-id="153a3-118">columnid</span></span>  
    <span data-ttu-id="153a3-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="153a3-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="153a3-120">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="153a3-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="153a3-121">итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="153a3-121">itagSequence</span></span>  
    <span data-ttu-id="153a3-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="153a3-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="153a3-123">Порядковый номер значения в столбце с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="153a3-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="153a3-124">Массив значений является исходным.</span><span class="sxs-lookup"><span data-stu-id="153a3-124">The array of values is one-based.</span></span> <span data-ttu-id="153a3-125">Первое значение — Sequence 1, а не 0.</span><span class="sxs-lookup"><span data-stu-id="153a3-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="153a3-126">Если столбец записи имеет только одно значение, то в качестве Итагсекуенце передается 1.</span><span class="sxs-lookup"><span data-stu-id="153a3-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="153a3-127">грбит</span><span class="sxs-lookup"><span data-stu-id="153a3-127">grbit</span></span>  
    <span data-ttu-id="153a3-128">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="153a3-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="153a3-129">Получение параметров столбца.</span><span class="sxs-lookup"><span data-stu-id="153a3-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="153a3-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="153a3-130">Return value</span></span>

<span data-ttu-id="153a3-131">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="153a3-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="153a3-132">Размер столбца.</span><span class="sxs-lookup"><span data-stu-id="153a3-132">The size of the column.</span></span> <span data-ttu-id="153a3-133">0, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="153a3-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="153a3-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="153a3-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="153a3-135">Справочник</span><span class="sxs-lookup"><span data-stu-id="153a3-135">Reference</span></span>

[<span data-ttu-id="153a3-136">Класс API</span><span class="sxs-lookup"><span data-stu-id="153a3-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="153a3-137">Члены API</span><span class="sxs-lookup"><span data-stu-id="153a3-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="153a3-138">Перегрузка Ретриевеколумнсизе</span><span class="sxs-lookup"><span data-stu-id="153a3-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="153a3-139">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="153a3-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
