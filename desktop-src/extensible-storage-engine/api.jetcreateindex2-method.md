---
description: Дополнительные сведения о методе API. JetCreateIndex2
title: API. JetCreateIndex2, метод
TOCTitle: 'JetCreateIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_INDEXCREATE[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex2(v=EXCHG.10)
ms:contentKeyID: 55100673
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b5fa690ed127c41b8a84f5d8aa012510f3a9c3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897014"
---
# <a name="apijetcreateindex2-method"></a><span data-ttu-id="0bc4b-103">API. JetCreateIndex2, метод</span><span class="sxs-lookup"><span data-stu-id="0bc4b-103">Api.JetCreateIndex2 method</span></span>

<span data-ttu-id="0bc4b-104">Создает индексы для данных в базе данных ESE.</span><span class="sxs-lookup"><span data-stu-id="0bc4b-104">Creates indexes over data in an ESE database.</span></span>

<span data-ttu-id="0bc4b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0bc4b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0bc4b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0bc4b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc4b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bc4b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexcreates As JET_INDEXCREATE(), _
    numIndexCreates As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexcreates As JET_INDEXCREATE()
Dim numIndexCreates As IntegerApi.JetCreateIndex2(sesid, tableid, _
    indexcreates, numIndexCreates)
```

``` csharp
public static void JetCreateIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEXCREATE[] indexcreates,
    int numIndexCreates
)
```

#### <a name="parameters"></a><span data-ttu-id="0bc4b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bc4b-108">Parameters</span></span>

  - <span data-ttu-id="0bc4b-109">сесид</span><span class="sxs-lookup"><span data-stu-id="0bc4b-109">sesid</span></span>  
    <span data-ttu-id="0bc4b-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0bc4b-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0bc4b-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="0bc4b-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0bc4b-112">TableID</span><span class="sxs-lookup"><span data-stu-id="0bc4b-112">tableid</span></span>  
    <span data-ttu-id="0bc4b-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0bc4b-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0bc4b-114">Таблица, в которой создается индекс.</span><span class="sxs-lookup"><span data-stu-id="0bc4b-114">The table to create the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="0bc4b-115">индекскреатес</span><span class="sxs-lookup"><span data-stu-id="0bc4b-115">indexcreates</span></span>  
    <span data-ttu-id="0bc4b-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="0bc4b-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="0bc4b-117">Массив объектов, описывающих создаваемые индексы.</span><span class="sxs-lookup"><span data-stu-id="0bc4b-117">Array of objects describing the indexes to be created.</span></span>

<!-- end list -->

  - <span data-ttu-id="0bc4b-118">нуминдекскреатес</span><span class="sxs-lookup"><span data-stu-id="0bc4b-118">numIndexCreates</span></span>  
    <span data-ttu-id="0bc4b-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0bc4b-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0bc4b-120">Число объектов описания индекса.</span><span class="sxs-lookup"><span data-stu-id="0bc4b-120">Number of index description objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc4b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0bc4b-121">Remarks</span></span>

<span data-ttu-id="0bc4b-122">При создании нескольких индексов (т. е. с Нуминдекскреатес больше 1) Этот метод должен вызываться за пределами транзакций и с монопольным доступом к таблице.</span><span class="sxs-lookup"><span data-stu-id="0bc4b-122">When creating multiple indexes (i.e. with numIndexCreates greater than 1) this method MUST be called outside of any transactions and with exclusive access to the table.</span></span> <span data-ttu-id="0bc4b-123">JET_TABLEID, возвращаемый "Жеткреатетабле", будет иметь доступ только, или таблицу можно открыть для монопольного доступа, передав [дениреад](./opentablegrbit-enumeration.md) в [жетопентабле (JET_SESID, JET_DBID, String, \[ \] , Int32, опентаблегрбит, JET_TABLEID)](./api.jetopentable-method.md).</span><span class="sxs-lookup"><span data-stu-id="0bc4b-123">The JET_TABLEID returned by "JetCreateTable" will have exlusive access or the table can be opened for exclusive access by passing [DenyRead](./opentablegrbit-enumeration.md) to [JetOpenTable(JET_SESID, JET_DBID, String, \[\], Int32, OpenTableGrbit, JET_TABLEID)](./api.jetopentable-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0bc4b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bc4b-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0bc4b-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="0bc4b-125">Reference</span></span>

[<span data-ttu-id="0bc4b-126">Класс API</span><span class="sxs-lookup"><span data-stu-id="0bc4b-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0bc4b-127">Члены API</span><span class="sxs-lookup"><span data-stu-id="0bc4b-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0bc4b-128">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0bc4b-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
