---
description: 'Дополнительные сведения: метод API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100907
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb4de0dc72493d0b28716b5a0859aa19adfe62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496878"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="4dd76-103">Метод API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="4dd76-103">Api.RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="4dd76-104">Извлекает значение столбца UInt64 из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4dd76-104">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="4dd76-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="4dd76-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="4dd76-106">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="4dd76-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="4dd76-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4dd76-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4dd76-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4dd76-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd76-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dd76-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4dd76-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dd76-110">Parameters</span></span>

  - <span data-ttu-id="4dd76-111">сесид</span><span class="sxs-lookup"><span data-stu-id="4dd76-111">sesid</span></span>  
    <span data-ttu-id="4dd76-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4dd76-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4dd76-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4dd76-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dd76-114">TableID</span><span class="sxs-lookup"><span data-stu-id="4dd76-114">tableid</span></span>  
    <span data-ttu-id="4dd76-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4dd76-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4dd76-116">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="4dd76-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dd76-117">columnid</span><span class="sxs-lookup"><span data-stu-id="4dd76-117">columnid</span></span>  
    <span data-ttu-id="4dd76-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4dd76-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4dd76-119">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="4dd76-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="4dd76-120">грбит</span><span class="sxs-lookup"><span data-stu-id="4dd76-120">grbit</span></span>  
    <span data-ttu-id="4dd76-121">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4dd76-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4dd76-122">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="4dd76-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4dd76-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dd76-123">Return value</span></span>

<span data-ttu-id="4dd76-124">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span><span class="sxs-lookup"><span data-stu-id="4dd76-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span></span>  
<span data-ttu-id="4dd76-125">Данные, полученные из столбца в виде UInt64.</span><span class="sxs-lookup"><span data-stu-id="4dd76-125">The data retrieved from the column as an UInt64.</span></span> <span data-ttu-id="4dd76-126">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="4dd76-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4dd76-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dd76-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4dd76-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="4dd76-128">Reference</span></span>

[<span data-ttu-id="4dd76-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="4dd76-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4dd76-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="4dd76-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4dd76-131">Перегрузка RetrieveColumnAsUInt64</span><span class="sxs-lookup"><span data-stu-id="4dd76-131">RetrieveColumnAsUInt64 overload</span></span>](./api.retrievecolumnasuint64-method.md)

[<span data-ttu-id="4dd76-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4dd76-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
