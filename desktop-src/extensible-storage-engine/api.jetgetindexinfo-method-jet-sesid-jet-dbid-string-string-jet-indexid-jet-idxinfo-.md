---
description: 'Дополнительные сведения: метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXID, JET_IdxInfo)'
title: Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXID, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100772
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac8a622f3b653885374888fa9fa6b2835ef8ede0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673221"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexid-jet_idxinfo"></a><span data-ttu-id="02baa-103">Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXID, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="02baa-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</span></span>

<span data-ttu-id="02baa-104">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="02baa-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="02baa-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02baa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02baa-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02baa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02baa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02baa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXID, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXID
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXID result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="02baa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="02baa-108">Parameters</span></span>

  - <span data-ttu-id="02baa-109">сесид</span><span class="sxs-lookup"><span data-stu-id="02baa-109">sesid</span></span>  
    <span data-ttu-id="02baa-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02baa-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="02baa-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="02baa-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="02baa-112">dbid</span><span class="sxs-lookup"><span data-stu-id="02baa-112">dbid</span></span>  
    <span data-ttu-id="02baa-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="02baa-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="02baa-114">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="02baa-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="02baa-115">tablename</span><span class="sxs-lookup"><span data-stu-id="02baa-115">tablename</span></span>  
    <span data-ttu-id="02baa-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02baa-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02baa-117">Имя таблицы, о которой необходимо получить сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="02baa-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="02baa-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="02baa-118">indexname</span></span>  
    <span data-ttu-id="02baa-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="02baa-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="02baa-120">Имя индекса, сведения о котором необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="02baa-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="02baa-121">result</span><span class="sxs-lookup"><span data-stu-id="02baa-121">result</span></span>  
    <span data-ttu-id="02baa-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="02baa-122">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="02baa-123">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="02baa-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="02baa-124">инфолевел</span><span class="sxs-lookup"><span data-stu-id="02baa-124">infoLevel</span></span>  
    <span data-ttu-id="02baa-125">Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="02baa-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="02baa-126">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="02baa-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="02baa-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02baa-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02baa-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="02baa-128">Reference</span></span>

[<span data-ttu-id="02baa-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="02baa-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="02baa-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="02baa-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="02baa-131">Перегрузка Жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="02baa-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="02baa-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="02baa-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
