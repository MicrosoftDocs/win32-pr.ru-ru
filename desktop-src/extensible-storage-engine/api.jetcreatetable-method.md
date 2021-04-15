---
description: Дополнительные сведения о методе API. Жеткреатетабле
title: API. Жеткреатетабле, метод
TOCTitle: 'JetCreateTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.JET_TABLEID@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreatetable(v=EXCHG.10)
ms:contentKeyID: 55100676
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateTable
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8025e35746d921fda3b601d289a9b361aefefb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497157"
---
# <a name="apijetcreatetable-method"></a><span data-ttu-id="903fe-103">API. Жеткреатетабле, метод</span><span class="sxs-lookup"><span data-stu-id="903fe-103">Api.JetCreateTable method</span></span>

<span data-ttu-id="903fe-104">Создайте пустую таблицу.</span><span class="sxs-lookup"><span data-stu-id="903fe-104">Create an empty table.</span></span> <span data-ttu-id="903fe-105">Вновь созданная таблица открывается исключительно.</span><span class="sxs-lookup"><span data-stu-id="903fe-105">The newly created table is opened exclusively.</span></span>

<span data-ttu-id="903fe-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="903fe-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="903fe-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="903fe-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="903fe-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="903fe-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String, _
    pages As Integer, _
    density As Integer, _
    <OutAttribute> ByRef tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As String
Dim pages As Integer
Dim density As Integer
Dim tableid As JET_TABLEIDApi.JetCreateTable(sesid, dbid, _
    table, pages, density, tableid)
```

``` csharp
public static void JetCreateTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table,
    int pages,
    int density,
    out JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="903fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="903fe-109">Parameters</span></span>

  - <span data-ttu-id="903fe-110">сесид</span><span class="sxs-lookup"><span data-stu-id="903fe-110">sesid</span></span>  
    <span data-ttu-id="903fe-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="903fe-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="903fe-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="903fe-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="903fe-113">dbid</span><span class="sxs-lookup"><span data-stu-id="903fe-113">dbid</span></span>  
    <span data-ttu-id="903fe-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="903fe-114">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="903fe-115">База данных, в которой создается таблица.</span><span class="sxs-lookup"><span data-stu-id="903fe-115">The database to create the table in.</span></span>

<!-- end list -->

  - <span data-ttu-id="903fe-116">table</span><span class="sxs-lookup"><span data-stu-id="903fe-116">table</span></span>  
    <span data-ttu-id="903fe-117">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="903fe-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="903fe-118">Имя создаваемой таблицы.</span><span class="sxs-lookup"><span data-stu-id="903fe-118">The name of the table to create.</span></span>

<!-- end list -->

  - <span data-ttu-id="903fe-119">страницы</span><span class="sxs-lookup"><span data-stu-id="903fe-119">pages</span></span>  
    <span data-ttu-id="903fe-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="903fe-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="903fe-121">Начальное число страниц в таблице.</span><span class="sxs-lookup"><span data-stu-id="903fe-121">Initial number of pages in the table.</span></span>

<!-- end list -->

  - <span data-ttu-id="903fe-122">плотность</span><span class="sxs-lookup"><span data-stu-id="903fe-122">density</span></span>  
    <span data-ttu-id="903fe-123">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="903fe-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="903fe-124">Плотность таблицы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="903fe-124">The default density of the table.</span></span> <span data-ttu-id="903fe-125">Используется при выполнении последовательных вставок.</span><span class="sxs-lookup"><span data-stu-id="903fe-125">This is used when doing sequential inserts.</span></span>

<!-- end list -->

  - <span data-ttu-id="903fe-126">TableID</span><span class="sxs-lookup"><span data-stu-id="903fe-126">tableid</span></span>  
    <span data-ttu-id="903fe-127">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="903fe-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="903fe-128">Возвращает TableID новой таблицы.</span><span class="sxs-lookup"><span data-stu-id="903fe-128">Returns the tableid of the new table.</span></span>

## <a name="see-also"></a><span data-ttu-id="903fe-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="903fe-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="903fe-130">Справочник</span><span class="sxs-lookup"><span data-stu-id="903fe-130">Reference</span></span>

[<span data-ttu-id="903fe-131">Класс API</span><span class="sxs-lookup"><span data-stu-id="903fe-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="903fe-132">Члены API</span><span class="sxs-lookup"><span data-stu-id="903fe-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="903fe-133">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="903fe-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
