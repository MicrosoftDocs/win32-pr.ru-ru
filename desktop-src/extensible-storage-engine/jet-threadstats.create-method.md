---
description: 'Дополнительные сведения о: JET_THREADSTATS. Создать метод'
title: JET_THREADSTATS. Метод Create (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816345"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="4acb7-103">JET_THREADSTATS. Создать метод</span><span class="sxs-lookup"><span data-stu-id="4acb7-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="4acb7-104">Создать новую [JET_THREADSTATS](./jet-threadstats-structure2.md) структуру с указанным значением.</span><span class="sxs-lookup"><span data-stu-id="4acb7-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="4acb7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4acb7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4acb7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4acb7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4acb7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4acb7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="4acb7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4acb7-108">Parameters</span></span>

  - <span data-ttu-id="4acb7-109">кпажереференцед</span><span class="sxs-lookup"><span data-stu-id="4acb7-109">cPageReferenced</span></span>  
    <span data-ttu-id="4acb7-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-111">Количество посещенных страниц.</span><span class="sxs-lookup"><span data-stu-id="4acb7-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="4acb7-112">кпажереад</span><span class="sxs-lookup"><span data-stu-id="4acb7-112">cPageRead</span></span>  
    <span data-ttu-id="4acb7-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-114">Число прочитанных страниц.</span><span class="sxs-lookup"><span data-stu-id="4acb7-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="4acb7-115">кпажепререад</span><span class="sxs-lookup"><span data-stu-id="4acb7-115">cPagePreread</span></span>  
    <span data-ttu-id="4acb7-116">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-117">Число страниц, которые были считаны.</span><span class="sxs-lookup"><span data-stu-id="4acb7-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="4acb7-118">кпажедиртиед</span><span class="sxs-lookup"><span data-stu-id="4acb7-118">cPageDirtied</span></span>  
    <span data-ttu-id="4acb7-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-120">Тнумбер страниц изменялся.</span><span class="sxs-lookup"><span data-stu-id="4acb7-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="4acb7-121">кпажередиртиед</span><span class="sxs-lookup"><span data-stu-id="4acb7-121">cPageRedirtied</span></span>  
    <span data-ttu-id="4acb7-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-123">Число страниц редиртиед.</span><span class="sxs-lookup"><span data-stu-id="4acb7-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="4acb7-124">клогрекорд</span><span class="sxs-lookup"><span data-stu-id="4acb7-124">cLogRecord</span></span>  
    <span data-ttu-id="4acb7-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-126">Число созданных записей журнала.</span><span class="sxs-lookup"><span data-stu-id="4acb7-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="4acb7-127">кблогрекорд</span><span class="sxs-lookup"><span data-stu-id="4acb7-127">cbLogRecord</span></span>  
    <span data-ttu-id="4acb7-128">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4acb7-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4acb7-129">Байтов записанных записей журнала.</span><span class="sxs-lookup"><span data-stu-id="4acb7-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4acb7-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4acb7-130">Return value</span></span>

<span data-ttu-id="4acb7-131">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4acb7-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="4acb7-132">Новая [JET_THREADSTATS](./jet-threadstats-structure2.md) структура с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="4acb7-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4acb7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4acb7-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4acb7-134">Справочник</span><span class="sxs-lookup"><span data-stu-id="4acb7-134">Reference</span></span>

[<span data-ttu-id="4acb7-135">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4acb7-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="4acb7-136">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4acb7-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="4acb7-137">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="4acb7-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
