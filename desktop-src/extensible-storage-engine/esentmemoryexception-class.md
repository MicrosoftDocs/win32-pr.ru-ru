---
description: 'Дополнительные сведения о: Есентмеморексцептион Class'
title: Класс EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a7090fdedee2969e5dd3658b7068fd8739e9365
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "103913992"
---
# <a name="esentmemoryexception-class"></a><span data-ttu-id="4f842-103">Класс EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="4f842-103">EsentMemoryException class</span></span>

<span data-ttu-id="4f842-104">Базовый класс для исключений памяти.</span><span class="sxs-lookup"><span data-stu-id="4f842-104">Base class for Memory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4f842-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4f842-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4f842-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4f842-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4f842-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4f842-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4f842-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4f842-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4f842-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4f842-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="4f842-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              

<span data-ttu-id="4f842-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f842-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f842-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f842-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f842-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f842-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="4f842-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4f842-116">Thread safety</span></span>

<span data-ttu-id="4f842-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4f842-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4f842-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4f842-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f842-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f842-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f842-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4f842-120">Reference</span></span>

[<span data-ttu-id="4f842-121">Элементы Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-121">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="4f842-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4f842-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="4f842-123">Производные типы</span><span class="sxs-lookup"><span data-stu-id="4f842-123">Derived types</span></span>

[<span data-ttu-id="4f842-124">System.Object</span><span class="sxs-lookup"><span data-stu-id="4f842-124">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4f842-125">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4f842-125">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4f842-126">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-126">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4f842-127">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-127">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4f842-128">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-128">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="4f842-129">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-129">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="4f842-130">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-130">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>  
              [<span data-ttu-id="4f842-131">Microsoft. ISAM. ESENT. Interop. Есентаутофбуфферсексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-131">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>](./esentoutofbuffersexception-class.md)  
              [<span data-ttu-id="4f842-132">Microsoft. ISAM. ESENT. Interop. Есентаутофкурсорсексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-132">Microsoft.Isam.Esent.Interop.EsentOutOfCursorsException</span></span>](./esentoutofcursorsexception-class.md)  
              [<span data-ttu-id="4f842-133">Microsoft. ISAM. ESENT. Interop. Есентаутоффилехандлесексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-133">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>](./esentoutoffilehandlesexception-class.md)  
              [<span data-ttu-id="4f842-134">Microsoft. ISAM. ESENT. Interop. Есентаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-134">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>](./esentoutofmemoryexception-class.md)  
              [<span data-ttu-id="4f842-135">Microsoft. ISAM. ESENT. Interop. Есентаутофсессионсексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-135">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>](./esentoutofsessionsexception-class.md)  
              [<span data-ttu-id="4f842-136">Microsoft. ISAM. ESENT. Interop. Есентаутофсреадсексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-136">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>](./esentoutofthreadsexception-class.md)  
              [<span data-ttu-id="4f842-137">Microsoft. ISAM. ESENT. Interop. Есенттуманимемпулентриесексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-137">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>](./esenttoomanymempoolentriesexception-class.md)  
              [<span data-ttu-id="4f842-138">Microsoft. ISAM. ESENT. Interop. Есенттуманйопениндексесексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-138">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>](./esenttoomanyopenindexesexception-class.md)  
              [<span data-ttu-id="4f842-139">Microsoft. ISAM. ESENT. Interop. Есенттуманисортсексцептион</span><span class="sxs-lookup"><span data-stu-id="4f842-139">Microsoft.Isam.Esent.Interop.EsentTooManySortsException</span></span>](./esenttoomanysortsexception-class.md)