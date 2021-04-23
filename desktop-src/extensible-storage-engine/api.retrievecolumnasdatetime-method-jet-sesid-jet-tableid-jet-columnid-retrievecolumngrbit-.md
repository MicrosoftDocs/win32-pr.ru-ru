---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100843
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: befd4e7256c9d1ca52d6f0239f5e56c21842a85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713012"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="451b5-103">Метод API. Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="451b5-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="451b5-104">Извлекает значение столбца DateTime из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="451b5-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="451b5-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="451b5-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="451b5-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="451b5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="451b5-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="451b5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="451b5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="451b5-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="451b5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="451b5-109">Parameters</span></span>

  - <span data-ttu-id="451b5-110">сесид</span><span class="sxs-lookup"><span data-stu-id="451b5-110">sesid</span></span>  
    <span data-ttu-id="451b5-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="451b5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="451b5-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="451b5-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="451b5-113">TableID</span><span class="sxs-lookup"><span data-stu-id="451b5-113">tableid</span></span>  
    <span data-ttu-id="451b5-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="451b5-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="451b5-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="451b5-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="451b5-116">columnid</span><span class="sxs-lookup"><span data-stu-id="451b5-116">columnid</span></span>  
    <span data-ttu-id="451b5-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="451b5-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="451b5-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="451b5-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="451b5-119">грбит</span><span class="sxs-lookup"><span data-stu-id="451b5-119">grbit</span></span>  
    <span data-ttu-id="451b5-120">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="451b5-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="451b5-121">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="451b5-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="451b5-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="451b5-122">Return value</span></span>

<span data-ttu-id="451b5-123">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="451b5-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="451b5-124">Данные, полученные из столбца в виде даты и времени.</span><span class="sxs-lookup"><span data-stu-id="451b5-124">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="451b5-125">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="451b5-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="451b5-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="451b5-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="451b5-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="451b5-127">Reference</span></span>

[<span data-ttu-id="451b5-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="451b5-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="451b5-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="451b5-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="451b5-130">Перегрузка Ретриевеколумнасдатетиме</span><span class="sxs-lookup"><span data-stu-id="451b5-130">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="451b5-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="451b5-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
