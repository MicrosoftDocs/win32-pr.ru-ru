---
description: 'Дополнительные сведения о: Есентаутофсессионсексцептион Class'
title: Класс Есентаутофсессионсексцептион
TOCTitle: EsentOutOfSessionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsessionsexception(v=EXCHG.10)
ms:contentKeyID: 55102494
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70b3c466586551f67f451d8ecc6ad108da52089a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423917"
---
# <a name="esentoutofsessionsexception-class"></a><span data-ttu-id="a01f0-103">Класс Есентаутофсессионсексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-103">EsentOutOfSessionsException class</span></span>

<span data-ttu-id="a01f0-104">Базовый класс для JET_err. Исключения Аутофсессионс.</span><span class="sxs-lookup"><span data-stu-id="a01f0-104">Base class for JET_err.OutOfSessions exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a01f0-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="a01f0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a01f0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a01f0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a01f0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a01f0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a01f0-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a01f0-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a01f0-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="a01f0-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="a01f0-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="a01f0-113">Microsoft. ISAM. ESENT. Interop. Есентаутофсессионсексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-113">Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException</span></span>  

<span data-ttu-id="a01f0-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a01f0-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a01f0-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a01f0-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a01f0-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a01f0-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSessionsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfSessionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSessionsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="a01f0-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="a01f0-117">Thread safety</span></span>

<span data-ttu-id="a01f0-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="a01f0-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a01f0-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="a01f0-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a01f0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a01f0-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a01f0-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="a01f0-121">Reference</span></span>

[<span data-ttu-id="a01f0-122">Элементы Есентаутофсессионсексцептион</span><span class="sxs-lookup"><span data-stu-id="a01f0-122">EsentOutOfSessionsException members</span></span>](./esentoutofsessionsexception-members.md)

[<span data-ttu-id="a01f0-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a01f0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
