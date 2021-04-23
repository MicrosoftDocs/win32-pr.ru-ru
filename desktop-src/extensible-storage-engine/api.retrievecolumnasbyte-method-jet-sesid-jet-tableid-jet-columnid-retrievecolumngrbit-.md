---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100865
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 68ea6a2b461799006edd0d82f69a20bc52d2c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539719"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="8c3ee-103">Метод API. Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-103">Api.RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="8c3ee-104">Извлекает значение байтового столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-104">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="8c3ee-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="8c3ee-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8c3ee-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8c3ee-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c3ee-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8c3ee-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c3ee-109">Parameters</span></span>

  - <span data-ttu-id="8c3ee-110">сесид</span><span class="sxs-lookup"><span data-stu-id="8c3ee-110">sesid</span></span>  
    <span data-ttu-id="8c3ee-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="8c3ee-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c3ee-113">TableID</span><span class="sxs-lookup"><span data-stu-id="8c3ee-113">tableid</span></span>  
    <span data-ttu-id="8c3ee-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="8c3ee-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c3ee-116">columnid</span><span class="sxs-lookup"><span data-stu-id="8c3ee-116">columnid</span></span>  
    <span data-ttu-id="8c3ee-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8c3ee-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="8c3ee-119">грбит</span><span class="sxs-lookup"><span data-stu-id="8c3ee-119">grbit</span></span>  
    <span data-ttu-id="8c3ee-120">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8c3ee-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8c3ee-121">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8c3ee-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c3ee-122">Return value</span></span>

<span data-ttu-id="8c3ee-123">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span><span class="sxs-lookup"><span data-stu-id="8c3ee-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span></span>  
<span data-ttu-id="8c3ee-124">Данные, полученные из столбца в виде байта.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-124">The data retrieved from the column as a byte.</span></span> <span data-ttu-id="8c3ee-125">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="8c3ee-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8c3ee-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8c3ee-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8c3ee-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="8c3ee-127">Reference</span></span>

[<span data-ttu-id="8c3ee-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="8c3ee-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8c3ee-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="8c3ee-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8c3ee-130">Перегрузка Ретриевеколумнасбите</span><span class="sxs-lookup"><span data-stu-id="8c3ee-130">RetrieveColumnAsByte overload</span></span>](./api.retrievecolumnasbyte-method.md)

[<span data-ttu-id="8c3ee-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8c3ee-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
