---
description: 'Дополнительные сведения: метод API. Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)'
title: Метод API. Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701341"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="7e48f-103">Метод API. Ретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="7e48f-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="7e48f-104">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="7e48f-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="7e48f-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="7e48f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="7e48f-106">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="7e48f-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="7e48f-107">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="7e48f-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="7e48f-108">Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</span><span class="sxs-lookup"><span data-stu-id="7e48f-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="7e48f-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e48f-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e48f-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e48f-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e48f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e48f-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="7e48f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e48f-112">Parameters</span></span>

  - <span data-ttu-id="7e48f-113">сесид</span><span class="sxs-lookup"><span data-stu-id="7e48f-113">sesid</span></span>  
    <span data-ttu-id="7e48f-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e48f-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7e48f-115">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="7e48f-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e48f-116">TableID</span><span class="sxs-lookup"><span data-stu-id="7e48f-116">tableid</span></span>  
    <span data-ttu-id="7e48f-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e48f-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7e48f-118">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="7e48f-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e48f-119">columnid</span><span class="sxs-lookup"><span data-stu-id="7e48f-119">columnid</span></span>  
    <span data-ttu-id="7e48f-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e48f-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7e48f-121">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="7e48f-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e48f-122">грбит</span><span class="sxs-lookup"><span data-stu-id="7e48f-122">grbit</span></span>  
    <span data-ttu-id="7e48f-123">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7e48f-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7e48f-124">Получение параметров столбца.</span><span class="sxs-lookup"><span data-stu-id="7e48f-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e48f-125">ретинфо</span><span class="sxs-lookup"><span data-stu-id="7e48f-125">retinfo</span></span>  
    <span data-ttu-id="7e48f-126">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="7e48f-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="7e48f-127">Если претинфо имеет значение NULL, функция ведет себя так, как будто Итагсекуенце равен 1 и Иблонгвалуе 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="7e48f-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="7e48f-128">Это приводит к извлечению столбца для получения первого значения многозначного столбца, а также для получения длинных данных со смещением 0 (нулем).</span><span class="sxs-lookup"><span data-stu-id="7e48f-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="7e48f-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e48f-129">Return value</span></span>

<span data-ttu-id="7e48f-130">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="7e48f-130">Type: \[\]</span></span>  
<span data-ttu-id="7e48f-131">Данные, полученные из столбца.</span><span class="sxs-lookup"><span data-stu-id="7e48f-131">The data retrieved from the column.</span></span> <span data-ttu-id="7e48f-132">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="7e48f-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7e48f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7e48f-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e48f-134">Справочник</span><span class="sxs-lookup"><span data-stu-id="7e48f-134">Reference</span></span>

[<span data-ttu-id="7e48f-135">Класс API</span><span class="sxs-lookup"><span data-stu-id="7e48f-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7e48f-136">Члены API</span><span class="sxs-lookup"><span data-stu-id="7e48f-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7e48f-137">Перегрузка Ретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="7e48f-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="7e48f-138">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7e48f-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
