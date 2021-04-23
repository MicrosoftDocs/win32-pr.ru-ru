---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасбулеан (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. Ретриевеколумнасбулеан (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsBoolean method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsBoolean(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasboolean(v=EXCHG.10)
ms:contentKeyID: 55100837
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsBoolean
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a2f7f38841248910bd23dd15b6cec06a638640d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539722"
---
# <a name="apiretrievecolumnasboolean-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="4a5c1-103">Метод API. Ретриевеколумнасбулеан (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="4a5c1-103">Api.RetrieveColumnAsBoolean method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="4a5c1-104">Извлекает значение логического столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-104">Retrieves a boolean column value from the current record.</span></span> <span data-ttu-id="4a5c1-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="4a5c1-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4a5c1-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4a5c1-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4a5c1-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4a5c1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a5c1-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsBoolean ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Boolean)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Boolean)

returnValue = Api.RetrieveColumnAsBoolean(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<bool> RetrieveColumnAsBoolean(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="4a5c1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a5c1-109">Parameters</span></span>

  - <span data-ttu-id="4a5c1-110">сесид</span><span class="sxs-lookup"><span data-stu-id="4a5c1-110">sesid</span></span>  
    <span data-ttu-id="4a5c1-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a5c1-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4a5c1-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a5c1-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4a5c1-113">tableid</span></span>  
    <span data-ttu-id="4a5c1-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a5c1-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4a5c1-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4a5c1-116">columnid</span><span class="sxs-lookup"><span data-stu-id="4a5c1-116">columnid</span></span>  
    <span data-ttu-id="4a5c1-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4a5c1-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4a5c1-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4a5c1-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4a5c1-119">Return value</span></span>

<span data-ttu-id="4a5c1-120">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Boolean](/dotnet/api/system.boolean)\></span><span class="sxs-lookup"><span data-stu-id="4a5c1-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Boolean](/dotnet/api/system.boolean)\></span></span>  
<span data-ttu-id="4a5c1-121">Данные, полученные из столбца в виде логического значения.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-121">The data retrieved from the column as a boolean.</span></span> <span data-ttu-id="4a5c1-122">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="4a5c1-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4a5c1-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a5c1-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4a5c1-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="4a5c1-124">Reference</span></span>

[<span data-ttu-id="4a5c1-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="4a5c1-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4a5c1-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="4a5c1-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4a5c1-127">Перегрузка Ретриевеколумнасбулеан</span><span class="sxs-lookup"><span data-stu-id="4a5c1-127">RetrieveColumnAsBoolean overload</span></span>](./api.retrievecolumnasboolean-method.md)

[<span data-ttu-id="4a5c1-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4a5c1-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
