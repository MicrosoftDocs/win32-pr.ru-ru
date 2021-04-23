---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasbyte(v=EXCHG.10)
ms:contentKeyID: 55100838
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsByte
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e3bc5db8aa14f3cabf05f15f8e1ecb41256496b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999547"
---
# <a name="apiretrievecolumnasbyte-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="1f37f-103">Метод API. Ретриевеколумнасбите (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="1f37f-103">Api.RetrieveColumnAsByte method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="1f37f-104">Извлекает значение байтового столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1f37f-104">Retrieves a byte column value from the current record.</span></span> <span data-ttu-id="1f37f-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="1f37f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="1f37f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f37f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f37f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f37f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f37f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1f37f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsByte ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Byte)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Byte)

returnValue = Api.RetrieveColumnAsByte(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<byte> RetrieveColumnAsByte(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="1f37f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1f37f-109">Parameters</span></span>

  - <span data-ttu-id="1f37f-110">сесид</span><span class="sxs-lookup"><span data-stu-id="1f37f-110">sesid</span></span>  
    <span data-ttu-id="1f37f-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f37f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1f37f-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1f37f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f37f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="1f37f-113">tableid</span></span>  
    <span data-ttu-id="1f37f-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f37f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1f37f-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="1f37f-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1f37f-116">columnid</span><span class="sxs-lookup"><span data-stu-id="1f37f-116">columnid</span></span>  
    <span data-ttu-id="1f37f-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1f37f-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1f37f-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="1f37f-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1f37f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1f37f-119">Return value</span></span>

<span data-ttu-id="1f37f-120">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span><span class="sxs-lookup"><span data-stu-id="1f37f-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Byte](/dotnet/api/system.byte)\></span></span>  
<span data-ttu-id="1f37f-121">Данные, полученные из столбца в виде байта.</span><span class="sxs-lookup"><span data-stu-id="1f37f-121">The data retrieved from the column as a byte.</span></span> <span data-ttu-id="1f37f-122">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="1f37f-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f37f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f37f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f37f-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="1f37f-124">Reference</span></span>

[<span data-ttu-id="1f37f-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="1f37f-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1f37f-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="1f37f-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1f37f-127">Перегрузка Ретриевеколумнасбите</span><span class="sxs-lookup"><span data-stu-id="1f37f-127">RetrieveColumnAsByte overload</span></span>](./api.retrievecolumnasbyte-method.md)

[<span data-ttu-id="1f37f-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1f37f-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
