---
description: 'Дополнительные сведения: метод API. Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)'
title: Метод API. Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100790
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d417e188c72914f871df4b46dede204f6633a8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692210"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="c1067-103">Метод API. Жетретриевеколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte, Int32, Int32, Ретриевеколумнгрбит, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="c1067-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="c1067-104">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="c1067-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="c1067-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="c1067-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="c1067-106">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="c1067-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="c1067-107">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="c1067-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="c1067-108">Помимо получения фактического значения столбца, Жетретриевеколумн можно также использовать для получения размера столбца перед извлечением самих данных столбца, чтобы можно было соответствующим образом изменить размер буферов приложения.</span><span class="sxs-lookup"><span data-stu-id="c1067-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="c1067-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1067-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c1067-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1067-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1067-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    actualDataSize, grbit, retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="c1067-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1067-112">Parameters</span></span>

  - <span data-ttu-id="c1067-113">сесид</span><span class="sxs-lookup"><span data-stu-id="c1067-113">sesid</span></span>  
    <span data-ttu-id="c1067-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c1067-115">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c1067-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-116">TableID</span><span class="sxs-lookup"><span data-stu-id="c1067-116">tableid</span></span>  
    <span data-ttu-id="c1067-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c1067-118">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="c1067-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-119">columnid</span><span class="sxs-lookup"><span data-stu-id="c1067-119">columnid</span></span>  
    <span data-ttu-id="c1067-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c1067-121">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="c1067-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-122">.</span><span class="sxs-lookup"><span data-stu-id="c1067-122">data</span></span>  
    <span data-ttu-id="c1067-123">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="c1067-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="c1067-124">Буфер данных, в который будет получен объект.</span><span class="sxs-lookup"><span data-stu-id="c1067-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="c1067-125">dataSize</span></span>  
    <span data-ttu-id="c1067-126">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c1067-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c1067-127">Размер буфера данных.</span><span class="sxs-lookup"><span data-stu-id="c1067-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-128">актуалдатасизе</span><span class="sxs-lookup"><span data-stu-id="c1067-128">actualDataSize</span></span>  
    <span data-ttu-id="c1067-129">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c1067-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="c1067-130">Возвращает фактический размер буфера данных.</span><span class="sxs-lookup"><span data-stu-id="c1067-130">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-131">грбит</span><span class="sxs-lookup"><span data-stu-id="c1067-131">grbit</span></span>  
    <span data-ttu-id="c1067-132">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-132">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c1067-133">Получение параметров столбца.</span><span class="sxs-lookup"><span data-stu-id="c1067-133">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1067-134">ретинфо</span><span class="sxs-lookup"><span data-stu-id="c1067-134">retinfo</span></span>  
    <span data-ttu-id="c1067-135">Тип: [Microsoft.ISAM.ESENT.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-135">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="c1067-136">Если претинфо имеет значение NULL, функция ведет себя так, как будто Итагсекуенце равен 1 и Иблонгвалуе 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="c1067-136">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="c1067-137">Это приводит к извлечению столбца для получения первого значения многозначного столбца, а также для получения длинных данных со смещением 0 (нулем).</span><span class="sxs-lookup"><span data-stu-id="c1067-137">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="c1067-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1067-138">Return value</span></span>

<span data-ttu-id="c1067-139">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c1067-139">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="c1067-140">Код предупреждения ESENT.</span><span class="sxs-lookup"><span data-stu-id="c1067-140">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="c1067-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1067-141">Remarks</span></span>

<span data-ttu-id="c1067-142">Функции Ретриевеколумнас предоставляют функции извлечения, относящиеся к типу данных.</span><span class="sxs-lookup"><span data-stu-id="c1067-142">The RetrieveColumnAs functions provide datatype-specific retrieval functions.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1067-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1067-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1067-144">Справочник</span><span class="sxs-lookup"><span data-stu-id="c1067-144">Reference</span></span>

[<span data-ttu-id="c1067-145">Класс API</span><span class="sxs-lookup"><span data-stu-id="c1067-145">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c1067-146">Члены API</span><span class="sxs-lookup"><span data-stu-id="c1067-146">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c1067-147">Перегрузка Жетретриевеколумн</span><span class="sxs-lookup"><span data-stu-id="c1067-147">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="c1067-148">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c1067-148">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
