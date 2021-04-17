---
description: 'Дополнительные сведения: метод API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint32(v=EXCHG.10)
ms:contentKeyID: 55100866
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt32
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 17babe091d4ae6a2c0219d97b240ee3198260147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693493"
---
# <a name="apiretrievecolumnasuint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="b3ce7-103">Метод API. RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-103">Api.RetrieveColumnAsUInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="b3ce7-104">Извлекает значение столбца UInt32 из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-104">Retrieves a uint32 column value from the current record.</span></span> <span data-ttu-id="b3ce7-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="b3ce7-106">Этот API несовместим с CLS.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="b3ce7-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b3ce7-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ce7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3ce7-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of UInteger)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of UInteger)

returnValue = Api.RetrieveColumnAsUInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<uint> RetrieveColumnAsUInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b3ce7-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3ce7-110">Parameters</span></span>

  - <span data-ttu-id="b3ce7-111">сесид</span><span class="sxs-lookup"><span data-stu-id="b3ce7-111">sesid</span></span>  
    <span data-ttu-id="b3ce7-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b3ce7-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3ce7-114">TableID</span><span class="sxs-lookup"><span data-stu-id="b3ce7-114">tableid</span></span>  
    <span data-ttu-id="b3ce7-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b3ce7-116">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3ce7-117">columnid</span><span class="sxs-lookup"><span data-stu-id="b3ce7-117">columnid</span></span>  
    <span data-ttu-id="b3ce7-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b3ce7-119">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="b3ce7-120">грбит</span><span class="sxs-lookup"><span data-stu-id="b3ce7-120">grbit</span></span>  
    <span data-ttu-id="b3ce7-121">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b3ce7-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b3ce7-122">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b3ce7-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3ce7-123">Return value</span></span>

<span data-ttu-id="b3ce7-124">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span><span class="sxs-lookup"><span data-stu-id="b3ce7-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt32](/dotnet/api/system.uint32)\></span></span>  
<span data-ttu-id="b3ce7-125">Данные, полученные из столбца как UInt32.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-125">The data retrieved from the column as an UInt32.</span></span> <span data-ttu-id="b3ce7-126">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="b3ce7-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b3ce7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3ce7-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3ce7-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="b3ce7-128">Reference</span></span>

[<span data-ttu-id="b3ce7-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="b3ce7-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b3ce7-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="b3ce7-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b3ce7-131">Перегрузка RetrieveColumnAsUInt32</span><span class="sxs-lookup"><span data-stu-id="b3ce7-131">RetrieveColumnAsUInt32 overload</span></span>](./api.retrievecolumnasuint32-method.md)

[<span data-ttu-id="b3ce7-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b3ce7-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
