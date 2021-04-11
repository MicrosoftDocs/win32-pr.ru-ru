---
description: 'Дополнительные сведения о: Есентаутофсреадсексцептион Class'
title: Класс Есентаутофсреадсексцептион
TOCTitle: EsentOutOfThreadsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofthreadsexception(v=EXCHG.10)
ms:contentKeyID: 55102450
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05a1427383a12c286ba37eee6f4ddfcd0b655350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999644"
---
# <a name="esentoutofthreadsexception-class"></a><span data-ttu-id="8a27f-103">Класс Есентаутофсреадсексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-103">EsentOutOfThreadsException class</span></span>

<span data-ttu-id="8a27f-104">Базовый класс для JET_err. Исключения Аутофсреадс.</span><span class="sxs-lookup"><span data-stu-id="8a27f-104">Base class for JET_err.OutOfThreads exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8a27f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="8a27f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8a27f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8a27f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8a27f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8a27f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8a27f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8a27f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8a27f-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="8a27f-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="8a27f-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="8a27f-113">Microsoft. ISAM. ESENT. Interop. Есентаутофсреадсексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-113">Microsoft.Isam.Esent.Interop.EsentOutOfThreadsException</span></span>  

<span data-ttu-id="8a27f-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8a27f-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8a27f-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8a27f-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8a27f-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8a27f-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfThreadsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfThreadsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfThreadsException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="8a27f-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="8a27f-117">Thread safety</span></span>

<span data-ttu-id="8a27f-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="8a27f-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8a27f-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="8a27f-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a27f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a27f-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8a27f-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="8a27f-121">Reference</span></span>

[<span data-ttu-id="8a27f-122">Элементы Есентаутофсреадсексцептион</span><span class="sxs-lookup"><span data-stu-id="8a27f-122">EsentOutOfThreadsException members</span></span>](./esentoutofthreadsexception-members.md)

[<span data-ttu-id="8a27f-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8a27f-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
