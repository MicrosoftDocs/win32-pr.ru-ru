---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасгуид (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. Ретриевеколумнасгуид (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasguid(v=EXCHG.10)
ms:contentKeyID: 55100854
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsGuid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5945cbedca8e628829fa8283a576913a641f6378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710849"
---
# <a name="apiretrievecolumnasguid-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="f8a53-103">Метод API. Ретриевеколумнасгуид (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="f8a53-103">Api.RetrieveColumnAsGuid method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="f8a53-104">Извлекает значение столбца GUID из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="f8a53-104">Retrieves a guid column value from the current record.</span></span> <span data-ttu-id="f8a53-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="f8a53-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="f8a53-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8a53-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8a53-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8a53-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a53-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8a53-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsGuid ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Guid)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Guid)

returnValue = Api.RetrieveColumnAsGuid(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<Guid> RetrieveColumnAsGuid(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f8a53-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8a53-109">Parameters</span></span>

  - <span data-ttu-id="f8a53-110">сесид</span><span class="sxs-lookup"><span data-stu-id="f8a53-110">sesid</span></span>  
    <span data-ttu-id="f8a53-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8a53-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f8a53-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="f8a53-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8a53-113">TableID</span><span class="sxs-lookup"><span data-stu-id="f8a53-113">tableid</span></span>  
    <span data-ttu-id="f8a53-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8a53-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f8a53-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="f8a53-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8a53-116">columnid</span><span class="sxs-lookup"><span data-stu-id="f8a53-116">columnid</span></span>  
    <span data-ttu-id="f8a53-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f8a53-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="f8a53-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="f8a53-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="f8a53-119">грбит</span><span class="sxs-lookup"><span data-stu-id="f8a53-119">grbit</span></span>  
    <span data-ttu-id="f8a53-120">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f8a53-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f8a53-121">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="f8a53-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f8a53-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8a53-122">Return value</span></span>

<span data-ttu-id="f8a53-123">Тип: [System. Nullable](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\></span><span class="sxs-lookup"><span data-stu-id="f8a53-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Guid](/dotnet/api/system.guid)\></span></span>  
<span data-ttu-id="f8a53-124">Данные, полученные из столбца в виде идентификатора GUID.</span><span class="sxs-lookup"><span data-stu-id="f8a53-124">The data retrieved from the column as a guid.</span></span> <span data-ttu-id="f8a53-125">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="f8a53-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8a53-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8a53-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8a53-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="f8a53-127">Reference</span></span>

[<span data-ttu-id="f8a53-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="f8a53-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f8a53-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="f8a53-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f8a53-130">Перегрузка Ретриевеколумнасгуид</span><span class="sxs-lookup"><span data-stu-id="f8a53-130">RetrieveColumnAsGuid overload</span></span>](./api.retrievecolumnasguid-method.md)

[<span data-ttu-id="f8a53-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f8a53-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
