---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Метод API. Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100870
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7176fa1c78b9910b68d0b3c9e7ce4f7e46519020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719278"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="c27e5-103">Метод API. Ретриевеколумнасдатетиме (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="c27e5-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="c27e5-104">Извлекает значение столбца DateTime из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="c27e5-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="c27e5-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="c27e5-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="c27e5-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c27e5-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c27e5-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c27e5-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c27e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c27e5-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="c27e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c27e5-109">Parameters</span></span>

  - <span data-ttu-id="c27e5-110">сесид</span><span class="sxs-lookup"><span data-stu-id="c27e5-110">sesid</span></span>  
    <span data-ttu-id="c27e5-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c27e5-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c27e5-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="c27e5-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c27e5-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c27e5-113">tableid</span></span>  
    <span data-ttu-id="c27e5-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c27e5-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c27e5-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="c27e5-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c27e5-116">columnid</span><span class="sxs-lookup"><span data-stu-id="c27e5-116">columnid</span></span>  
    <span data-ttu-id="c27e5-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c27e5-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c27e5-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="c27e5-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c27e5-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c27e5-119">Return value</span></span>

<span data-ttu-id="c27e5-120">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="c27e5-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="c27e5-121">Данные, полученные из столбца в виде даты и времени.</span><span class="sxs-lookup"><span data-stu-id="c27e5-121">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="c27e5-122">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="c27e5-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c27e5-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c27e5-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c27e5-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="c27e5-124">Reference</span></span>

[<span data-ttu-id="c27e5-125">Класс API</span><span class="sxs-lookup"><span data-stu-id="c27e5-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c27e5-126">Члены API</span><span class="sxs-lookup"><span data-stu-id="c27e5-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c27e5-127">Перегрузка Ретриевеколумнасдатетиме</span><span class="sxs-lookup"><span data-stu-id="c27e5-127">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="c27e5-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c27e5-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
