---
description: 'Дополнительные сведения: метод API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100858
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edd9c8a8495a56e14c655357397c5a693239062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896602"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="5c8db-103">Метод API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="5c8db-103">Api.RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="5c8db-104">Извлекает значение одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="5c8db-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="5c8db-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="5c8db-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="5c8db-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5c8db-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5c8db-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5c8db-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5c8db-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c8db-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="5c8db-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c8db-109">Parameters</span></span>

  - <span data-ttu-id="5c8db-110">сесид</span><span class="sxs-lookup"><span data-stu-id="5c8db-110">sesid</span></span>  
    <span data-ttu-id="5c8db-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c8db-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5c8db-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="5c8db-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c8db-113">TableID</span><span class="sxs-lookup"><span data-stu-id="5c8db-113">tableid</span></span>  
    <span data-ttu-id="5c8db-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c8db-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5c8db-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="5c8db-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5c8db-116">columnid</span><span class="sxs-lookup"><span data-stu-id="5c8db-116">columnid</span></span>  
    <span data-ttu-id="5c8db-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5c8db-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5c8db-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="5c8db-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5c8db-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c8db-119">Return value</span></span>

<span data-ttu-id="5c8db-120">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span><span class="sxs-lookup"><span data-stu-id="5c8db-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span></span>  
<span data-ttu-id="5c8db-121">Данные, полученные из столбца как длинные.</span><span class="sxs-lookup"><span data-stu-id="5c8db-121">The data retrieved from the column as a long.</span></span> <span data-ttu-id="5c8db-122">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="5c8db-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5c8db-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c8db-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5c8db-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="5c8db-124">Reference</span></span>

[<span data-ttu-id="5c8db-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="5c8db-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5c8db-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="5c8db-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5c8db-127">Перегрузка RetrieveColumnAsInt64</span><span class="sxs-lookup"><span data-stu-id="5c8db-127">RetrieveColumnAsInt64 overload</span></span>](./api.retrievecolumnasint64-method.md)

[<span data-ttu-id="5c8db-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5c8db-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
