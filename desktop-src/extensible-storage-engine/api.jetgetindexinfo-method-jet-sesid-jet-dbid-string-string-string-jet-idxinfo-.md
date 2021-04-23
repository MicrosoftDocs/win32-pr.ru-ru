---
description: Дополнительные сведения см. в статье метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, строка, JET_IdxInfo).
title: Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, строка, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.String@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55100769
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
ms.openlocfilehash: eed2ba4a3f578dda966b2b4530f26de25089681e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692216"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-string-jet_idxinfo"></a><span data-ttu-id="09235-103">Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, строка, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="09235-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</span></span>

<span data-ttu-id="09235-104">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="09235-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="09235-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="09235-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="09235-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="09235-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="09235-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09235-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As String
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out string result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="09235-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="09235-108">Parameters</span></span>

  - <span data-ttu-id="09235-109">сесид</span><span class="sxs-lookup"><span data-stu-id="09235-109">sesid</span></span>  
    <span data-ttu-id="09235-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09235-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="09235-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="09235-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="09235-112">dbid</span><span class="sxs-lookup"><span data-stu-id="09235-112">dbid</span></span>  
    <span data-ttu-id="09235-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="09235-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="09235-114">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="09235-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="09235-115">tablename</span><span class="sxs-lookup"><span data-stu-id="09235-115">tablename</span></span>  
    <span data-ttu-id="09235-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="09235-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="09235-117">Имя таблицы, о которой необходимо получить сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="09235-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="09235-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="09235-118">indexname</span></span>  
    <span data-ttu-id="09235-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="09235-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="09235-120">Имя индекса, сведения о котором необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="09235-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="09235-121">result</span><span class="sxs-lookup"><span data-stu-id="09235-121">result</span></span>  
    <span data-ttu-id="09235-122">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="09235-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="09235-123">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="09235-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="09235-124">инфолевел</span><span class="sxs-lookup"><span data-stu-id="09235-124">infoLevel</span></span>  
    <span data-ttu-id="09235-125">Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="09235-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="09235-126">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="09235-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="09235-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09235-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="09235-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="09235-128">Reference</span></span>

[<span data-ttu-id="09235-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="09235-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="09235-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="09235-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="09235-131">Перегрузка Жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="09235-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="09235-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="09235-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
