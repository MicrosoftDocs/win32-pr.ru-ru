---
description: Дополнительные сведения о методе API. Трйопентабле
title: API. Трйопентабле, метод
TOCTitle: 'TryOpenTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TryOpenTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryopentable(v=EXCHG.10)
ms:contentKeyID: 55100889
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TryOpenTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 556d3f12f24229326a6b26f357e5b19801119b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423749"
---
# <a name="apitryopentable-method"></a><span data-ttu-id="04549-103">API. Трйопентабле, метод</span><span class="sxs-lookup"><span data-stu-id="04549-103">Api.TryOpenTable method</span></span>

<span data-ttu-id="04549-104">Попробуйте открыть таблицу.</span><span class="sxs-lookup"><span data-stu-id="04549-104">Try to open a table.</span></span>

<span data-ttu-id="04549-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="04549-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="04549-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="04549-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="04549-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04549-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TryOpenTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    grbit As OpenTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim grbit As OpenTableGrbit
Dim tableid As JET_TABLEID
Dim returnValue As Boolean

returnValue = Api.TryOpenTable(sesid, _
    dbid, tablename, grbit, tableid)
```

``` csharp
public static bool TryOpenTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    OpenTableGrbit grbit,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="04549-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="04549-108">Parameters</span></span>

  - <span data-ttu-id="04549-109">сесид</span><span class="sxs-lookup"><span data-stu-id="04549-109">sesid</span></span>  
    <span data-ttu-id="04549-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04549-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="04549-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="04549-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="04549-112">dbid</span><span class="sxs-lookup"><span data-stu-id="04549-112">dbid</span></span>  
    <span data-ttu-id="04549-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04549-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="04549-114">База данных для поиска таблицы в.</span><span class="sxs-lookup"><span data-stu-id="04549-114">The database to look for the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="04549-115">tablename</span><span class="sxs-lookup"><span data-stu-id="04549-115">tablename</span></span>  
    <span data-ttu-id="04549-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="04549-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="04549-117">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="04549-117">The name of the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="04549-118">грбит</span><span class="sxs-lookup"><span data-stu-id="04549-118">grbit</span></span>  
    <span data-ttu-id="04549-119">Тип: [Microsoft. ISAM. ESENT. Interop. опентаблегрбит](./opentablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="04549-119">Type: [Microsoft.Isam.Esent.Interop.OpenTableGrbit](./opentablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="04549-120">Параметры открытия таблицы.</span><span class="sxs-lookup"><span data-stu-id="04549-120">Table open options.</span></span>

<!-- end list -->

  - <span data-ttu-id="04549-121">TableID</span><span class="sxs-lookup"><span data-stu-id="04549-121">tableid</span></span>  
    <span data-ttu-id="04549-122">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="04549-122">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="04549-123">Возвращает открытый TableID.</span><span class="sxs-lookup"><span data-stu-id="04549-123">Returns the opened tableid.</span></span>

#### <a name="return-value"></a><span data-ttu-id="04549-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04549-124">Return value</span></span>

<span data-ttu-id="04549-125">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="04549-125">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="04549-126">Значение true, если таблица была открыта, и значение false, если таблица не существует.</span><span class="sxs-lookup"><span data-stu-id="04549-126">True if the table was opened, false if the table doesn't exist.</span></span>  

## <a name="see-also"></a><span data-ttu-id="04549-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04549-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="04549-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="04549-128">Reference</span></span>

[<span data-ttu-id="04549-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="04549-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="04549-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="04549-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="04549-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="04549-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
