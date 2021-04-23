---
description: 'Дополнительные сведения о: Есентресаурцеексцептион Class'
title: Класс EsentResourceException
TOCTitle: EsentResourceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResourceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102627
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResourceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7d4964bb4ed9c1305652d9425170bd934c9274e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265135"
---
# <a name="esentresourceexception-class"></a><span data-ttu-id="b85dd-103">Класс EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="b85dd-103">EsentResourceException class</span></span>

<span data-ttu-id="b85dd-104">Базовый класс для исключений ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b85dd-104">Base class for Resource exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b85dd-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b85dd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b85dd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b85dd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b85dd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b85dd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b85dd-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b85dd-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b85dd-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="b85dd-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>  
            [<span data-ttu-id="b85dd-112">Microsoft. ISAM. ESENT. Interop. Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
            [<span data-ttu-id="b85dd-113">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-113">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
            [<span data-ttu-id="b85dd-114">Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-114">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
            [<span data-ttu-id="b85dd-115">Microsoft. ISAM. ESENT. Interop. Есенттаскдроппедексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-115">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>](./esenttaskdroppedexception-class.md)  
            [<span data-ttu-id="b85dd-116">Microsoft. ISAM. ESENT. Interop. Есенттуманиоексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-116">Microsoft.Isam.Esent.Interop.EsentTooManyIOException</span></span>](./esenttoomanyioexception-class.md)  

<span data-ttu-id="b85dd-117">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b85dd-117">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b85dd-118">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b85dd-118">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b85dd-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b85dd-119">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentResourceException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentResourceException
```

``` csharp
[SerializableAttribute]
public abstract class EsentResourceException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="b85dd-120">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b85dd-120">Thread safety</span></span>

<span data-ttu-id="b85dd-121">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b85dd-121">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b85dd-122">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b85dd-122">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b85dd-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b85dd-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b85dd-124">Справочник</span><span class="sxs-lookup"><span data-stu-id="b85dd-124">Reference</span></span>

[<span data-ttu-id="b85dd-125">Элементы Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b85dd-125">EsentResourceException members</span></span>](./esentresourceexception-members.md)

[<span data-ttu-id="b85dd-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b85dd-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
