---
description: 'Дополнительные сведения: метод API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100859
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e9f963d298610fb36f6b1f9c9ff3a0bfbfa2501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539707"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="1ab78-103">Метод API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="1ab78-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="1ab78-104">Извлекает значение столбца Int32 из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="1ab78-104">Retrieves an int32 column value from the current record.</span></span> <span data-ttu-id="1ab78-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="1ab78-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="1ab78-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1ab78-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1ab78-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1ab78-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1ab78-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ab78-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1ab78-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ab78-109">Parameters</span></span>

  - <span data-ttu-id="1ab78-110">сесид</span><span class="sxs-lookup"><span data-stu-id="1ab78-110">sesid</span></span>  
    <span data-ttu-id="1ab78-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ab78-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1ab78-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1ab78-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ab78-113">TableID</span><span class="sxs-lookup"><span data-stu-id="1ab78-113">tableid</span></span>  
    <span data-ttu-id="1ab78-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ab78-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1ab78-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="1ab78-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ab78-116">columnid</span><span class="sxs-lookup"><span data-stu-id="1ab78-116">columnid</span></span>  
    <span data-ttu-id="1ab78-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1ab78-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1ab78-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="1ab78-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="1ab78-119">грбит</span><span class="sxs-lookup"><span data-stu-id="1ab78-119">grbit</span></span>  
    <span data-ttu-id="1ab78-120">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1ab78-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1ab78-121">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="1ab78-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1ab78-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ab78-122">Return value</span></span>

<span data-ttu-id="1ab78-123">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="1ab78-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="1ab78-124">Данные, полученные из столбца в виде целого числа. Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="1ab78-124">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ab78-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ab78-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1ab78-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="1ab78-126">Reference</span></span>

[<span data-ttu-id="1ab78-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="1ab78-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1ab78-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="1ab78-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1ab78-129">Перегрузка RetrieveColumnAsInt32</span><span class="sxs-lookup"><span data-stu-id="1ab78-129">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="1ab78-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1ab78-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
