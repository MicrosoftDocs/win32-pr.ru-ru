---
description: 'Дополнительные сведения о: Есентаутофмеморексцептион Class'
title: Класс Есентаутофмеморексцептион
TOCTitle: EsentOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d766bdfa115db7e43cbee6242e41a5c7cdb281b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263277"
---
# <a name="esentoutofmemoryexception-class"></a><span data-ttu-id="9fecb-103">Класс Есентаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-103">EsentOutOfMemoryException class</span></span>

<span data-ttu-id="9fecb-104">Базовый класс для JET_err. Исключения OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="9fecb-104">Base class for JET_err.OutOfMemory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9fecb-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="9fecb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9fecb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9fecb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9fecb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9fecb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9fecb-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9fecb-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9fecb-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="9fecb-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="9fecb-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="9fecb-113">Microsoft. ISAM. ESENT. Interop. Есентаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-113">Microsoft.Isam.Esent.Interop.EsentOutOfMemoryException</span></span>  

<span data-ttu-id="9fecb-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9fecb-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9fecb-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9fecb-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9fecb-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9fecb-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfMemoryException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfMemoryException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="9fecb-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="9fecb-117">Thread safety</span></span>

<span data-ttu-id="9fecb-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="9fecb-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9fecb-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="9fecb-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9fecb-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9fecb-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9fecb-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="9fecb-121">Reference</span></span>

[<span data-ttu-id="9fecb-122">Элементы Есентаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="9fecb-122">EsentOutOfMemoryException members</span></span>](./esentoutofmemoryexception-members.md)

[<span data-ttu-id="9fecb-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9fecb-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
