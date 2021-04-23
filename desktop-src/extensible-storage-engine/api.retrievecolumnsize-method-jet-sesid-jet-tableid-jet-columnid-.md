---
description: 'Дополнительные сведения: метод API. Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
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
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693624"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="cae8d-103">Метод API. Ретриевеколумнсизе (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="cae8d-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="cae8d-104">Получает размер значения одного столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="cae8d-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="cae8d-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="cae8d-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="cae8d-106">Кроме того, эта функция может извлекать столбец из записи, создаваемой в буфере копирования курсора.</span><span class="sxs-lookup"><span data-stu-id="cae8d-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="cae8d-107">Эта функция также может получать данные столбца из записи индекса, которая ссылается на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="cae8d-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="cae8d-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cae8d-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cae8d-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cae8d-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cae8d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cae8d-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="cae8d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="cae8d-111">Parameters</span></span>

  - <span data-ttu-id="cae8d-112">сесид</span><span class="sxs-lookup"><span data-stu-id="cae8d-112">sesid</span></span>  
    <span data-ttu-id="cae8d-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cae8d-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="cae8d-114">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="cae8d-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="cae8d-115">TableID</span><span class="sxs-lookup"><span data-stu-id="cae8d-115">tableid</span></span>  
    <span data-ttu-id="cae8d-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cae8d-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="cae8d-117">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="cae8d-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="cae8d-118">columnid</span><span class="sxs-lookup"><span data-stu-id="cae8d-118">columnid</span></span>  
    <span data-ttu-id="cae8d-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cae8d-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="cae8d-120">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="cae8d-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cae8d-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cae8d-121">Return value</span></span>

<span data-ttu-id="cae8d-122">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="cae8d-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="cae8d-123">Размер столбца.</span><span class="sxs-lookup"><span data-stu-id="cae8d-123">The size of the column.</span></span> <span data-ttu-id="cae8d-124">0, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="cae8d-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cae8d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cae8d-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cae8d-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="cae8d-126">Reference</span></span>

[<span data-ttu-id="cae8d-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="cae8d-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cae8d-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="cae8d-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cae8d-129">Перегрузка Ретриевеколумнсизе</span><span class="sxs-lookup"><span data-stu-id="cae8d-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="cae8d-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cae8d-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
