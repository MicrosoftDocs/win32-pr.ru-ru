---
description: 'Дополнительные сведения: метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)'
title: Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55107227
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cc7c110c139c66fdd5d8baee4ebb102922adf7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673220"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist-jet_idxinfo"></a><span data-ttu-id="d80c3-103">Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)</span><span class="sxs-lookup"><span data-stu-id="d80c3-103">Api.JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</span></span>

<span data-ttu-id="d80c3-104">Извлекает сведения о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="d80c3-104">Retrieves information about indexes on a table.</span></span>

<span data-ttu-id="d80c3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d80c3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d80c3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d80c3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d80c3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d80c3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXLIST, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXLIST
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXLIST result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="d80c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d80c3-108">Parameters</span></span>

  - <span data-ttu-id="d80c3-109">сесид</span><span class="sxs-lookup"><span data-stu-id="d80c3-109">sesid</span></span>  
    <span data-ttu-id="d80c3-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d80c3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d80c3-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="d80c3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d80c3-112">dbid</span><span class="sxs-lookup"><span data-stu-id="d80c3-112">dbid</span></span>  
    <span data-ttu-id="d80c3-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d80c3-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="d80c3-114">Используемая база данных.</span><span class="sxs-lookup"><span data-stu-id="d80c3-114">The database to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d80c3-115">tablename</span><span class="sxs-lookup"><span data-stu-id="d80c3-115">tablename</span></span>  
    <span data-ttu-id="d80c3-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d80c3-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d80c3-117">Имя таблицы, о которой необходимо получить сведения об индексе.</span><span class="sxs-lookup"><span data-stu-id="d80c3-117">The name of the table to retrieve index information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="d80c3-118">IndexName</span><span class="sxs-lookup"><span data-stu-id="d80c3-118">indexname</span></span>  
    <span data-ttu-id="d80c3-119">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d80c3-119">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d80c3-120">Имя индекса, сведения о котором необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="d80c3-120">The name of the index to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="d80c3-121">result</span><span class="sxs-lookup"><span data-stu-id="d80c3-121">result</span></span>  
    <span data-ttu-id="d80c3-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span><span class="sxs-lookup"><span data-stu-id="d80c3-122">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXLIST](./jet-indexlist-class.md)</span></span>  
    
    <span data-ttu-id="d80c3-123">Заполняется сведениями о индексах в таблице.</span><span class="sxs-lookup"><span data-stu-id="d80c3-123">Filled in with information about indexes on the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="d80c3-124">инфолевел</span><span class="sxs-lookup"><span data-stu-id="d80c3-124">infoLevel</span></span>  
    <span data-ttu-id="d80c3-125">Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d80c3-125">Type: [Microsoft.Isam.Esent.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="d80c3-126">Тип извлекаемых данных.</span><span class="sxs-lookup"><span data-stu-id="d80c3-126">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="d80c3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d80c3-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d80c3-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="d80c3-128">Reference</span></span>

[<span data-ttu-id="d80c3-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="d80c3-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d80c3-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="d80c3-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d80c3-131">Перегрузка Жетжетиндексинфо</span><span class="sxs-lookup"><span data-stu-id="d80c3-131">JetGetIndexInfo overload</span></span>](./api.jetgetindexinfo-method.md)

[<span data-ttu-id="d80c3-132">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d80c3-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
