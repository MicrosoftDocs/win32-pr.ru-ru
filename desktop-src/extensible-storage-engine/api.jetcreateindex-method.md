---
description: Дополнительные сведения о методе API. Жеткреатеиндекс
title: API. Жеткреатеиндекс, метод
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9b3549461324f396408bb7d370531907248e8c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710960"
---
# <a name="apijetcreateindex-method"></a><span data-ttu-id="477e0-103">API. Жеткреатеиндекс, метод</span><span class="sxs-lookup"><span data-stu-id="477e0-103">Api.JetCreateIndex method</span></span>

<span data-ttu-id="477e0-104">Создает индекс для данных в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="477e0-104">Creates an index over data in an ESE database.</span></span> <span data-ttu-id="477e0-105">Индекс можно использовать для быстрого выявления конкретных данных.</span><span class="sxs-lookup"><span data-stu-id="477e0-105">An index can be used to locate specific data quickly.</span></span>

<span data-ttu-id="477e0-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="477e0-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="477e0-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="477e0-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="477e0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="477e0-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a><span data-ttu-id="477e0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="477e0-109">Parameters</span></span>

  - <span data-ttu-id="477e0-110">сесид</span><span class="sxs-lookup"><span data-stu-id="477e0-110">sesid</span></span>  
    <span data-ttu-id="477e0-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="477e0-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="477e0-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="477e0-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="477e0-113">TableID</span><span class="sxs-lookup"><span data-stu-id="477e0-113">tableid</span></span>  
    <span data-ttu-id="477e0-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="477e0-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="477e0-115">Таблица, в которой создается индекс.</span><span class="sxs-lookup"><span data-stu-id="477e0-115">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="477e0-116">indexName</span><span class="sxs-lookup"><span data-stu-id="477e0-116">indexName</span></span>  
    <span data-ttu-id="477e0-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="477e0-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="477e0-118">Указатель на строку, завершающуюся нулем, которая указывает имя создаваемого индекса.</span><span class="sxs-lookup"><span data-stu-id="477e0-118">Pointer to a null-terminated string that specifies the name of the index to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="477e0-119">грбит</span><span class="sxs-lookup"><span data-stu-id="477e0-119">grbit</span></span>  
    <span data-ttu-id="477e0-120">Тип: [Microsoft. ISAM. ESENT. Interop. креатеиндексгрбит](./createindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="477e0-120">Type: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="477e0-121">Параметры создания индекса.</span><span class="sxs-lookup"><span data-stu-id="477e0-121">Index creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="477e0-122">кэйдескриптион</span><span class="sxs-lookup"><span data-stu-id="477e0-122">keyDescription</span></span>  
    <span data-ttu-id="477e0-123">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="477e0-123">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="477e0-124">Указатель на строку, завершающуюся двойной нулем и заканчивающуюся токеном с разделителями null.</span><span class="sxs-lookup"><span data-stu-id="477e0-124">Pointer to a double null-terminated string of null-delimited tokens.</span></span>

<!-- end list -->

  - <span data-ttu-id="477e0-125">кэйдескриптионленгс</span><span class="sxs-lookup"><span data-stu-id="477e0-125">keyDescriptionLength</span></span>  
    <span data-ttu-id="477e0-126">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="477e0-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="477e0-127">Длина в символах Сзкэй, включая два завершающих значения NULL.</span><span class="sxs-lookup"><span data-stu-id="477e0-127">The length, in characters, of szKey including the two terminating nulls.</span></span>

<!-- end list -->

  - <span data-ttu-id="477e0-128">плотность</span><span class="sxs-lookup"><span data-stu-id="477e0-128">density</span></span>  
    <span data-ttu-id="477e0-129">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="477e0-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="477e0-130">Начальная плотность дерева B +.</span><span class="sxs-lookup"><span data-stu-id="477e0-130">Initial B+ tree density.</span></span>

## <a name="see-also"></a><span data-ttu-id="477e0-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="477e0-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="477e0-132">Справочник</span><span class="sxs-lookup"><span data-stu-id="477e0-132">Reference</span></span>

[<span data-ttu-id="477e0-133">Класс API</span><span class="sxs-lookup"><span data-stu-id="477e0-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="477e0-134">Члены API</span><span class="sxs-lookup"><span data-stu-id="477e0-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="477e0-135">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="477e0-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
