---
description: 'Дополнительные сведения: метод API. Десериализеобжектфромколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)'
title: Метод API. Десериализеобжектфромколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100669
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe2bb9757216dc4b0a671ae9d5da6cdf4bd5eb7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710858"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="4454c-103">Метод API. Десериализеобжектфромколумн (JET_SESID, JET_TABLEID, JET_COLUMNID, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="4454c-103">Api.DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="4454c-104">Десериализация объекта из столбца.</span><span class="sxs-lookup"><span data-stu-id="4454c-104">Deserialize an object from a column.</span></span>

<span data-ttu-id="4454c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4454c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4454c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4454c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4454c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4454c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="4454c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4454c-108">Parameters</span></span>

  - <span data-ttu-id="4454c-109">сесид</span><span class="sxs-lookup"><span data-stu-id="4454c-109">sesid</span></span>  
    <span data-ttu-id="4454c-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4454c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4454c-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4454c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4454c-112">TableID</span><span class="sxs-lookup"><span data-stu-id="4454c-112">tableid</span></span>  
    <span data-ttu-id="4454c-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4454c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4454c-114">Таблица, из которой производится чтение.</span><span class="sxs-lookup"><span data-stu-id="4454c-114">The table to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4454c-115">columnid</span><span class="sxs-lookup"><span data-stu-id="4454c-115">columnid</span></span>  
    <span data-ttu-id="4454c-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4454c-116">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="4454c-117">Столбец, из которого производится чтение.</span><span class="sxs-lookup"><span data-stu-id="4454c-117">The column to read from.</span></span>

<!-- end list -->

  - <span data-ttu-id="4454c-118">грбит</span><span class="sxs-lookup"><span data-stu-id="4454c-118">grbit</span></span>  
    <span data-ttu-id="4454c-119">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4454c-119">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4454c-120">Используемые параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="4454c-120">The retrieval options to use.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4454c-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4454c-121">Return value</span></span>

<span data-ttu-id="4454c-122">Тип: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="4454c-122">Type: [System.Object](/dotnet/api/system.object)</span></span>  
<span data-ttu-id="4454c-123">Десериализованный объект.</span><span class="sxs-lookup"><span data-stu-id="4454c-123">The deserialized object.</span></span> <span data-ttu-id="4454c-124">Значение null, если столбец имел значение null.</span><span class="sxs-lookup"><span data-stu-id="4454c-124">Null if the column was null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4454c-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4454c-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4454c-126">Справочник</span><span class="sxs-lookup"><span data-stu-id="4454c-126">Reference</span></span>

[<span data-ttu-id="4454c-127">Класс API</span><span class="sxs-lookup"><span data-stu-id="4454c-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4454c-128">Члены API</span><span class="sxs-lookup"><span data-stu-id="4454c-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4454c-129">Перегрузка Десериализеобжектфромколумн</span><span class="sxs-lookup"><span data-stu-id="4454c-129">DeserializeObjectFromColumn overload</span></span>](./api.deserializeobjectfromcolumn-method.md)

[<span data-ttu-id="4454c-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4454c-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
