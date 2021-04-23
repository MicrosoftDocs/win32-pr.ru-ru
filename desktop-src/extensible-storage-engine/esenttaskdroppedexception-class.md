---
description: 'Дополнительные сведения о: Есенттаскдроппедексцептион Class'
title: Класс Есенттаскдроппедексцептион
TOCTitle: EsentTaskDroppedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttaskdroppedexception(v=EXCHG.10)
ms:contentKeyID: 55103022
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTaskDroppedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4770f405ff7ca8875e3e2a960dea846e2f34ff6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545607"
---
# <a name="esenttaskdroppedexception-class"></a><span data-ttu-id="07e5d-103">Класс Есенттаскдроппедексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-103">EsentTaskDroppedException class</span></span>

<span data-ttu-id="07e5d-104">Базовый класс для JET_err. Исключения Таскдроппед.</span><span class="sxs-lookup"><span data-stu-id="07e5d-104">Base class for JET_err.TaskDropped exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="07e5d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="07e5d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="07e5d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="07e5d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="07e5d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="07e5d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="07e5d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="07e5d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="07e5d-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="07e5d-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="07e5d-112">Microsoft. ISAM. ESENT. Interop. Есенттаскдроппедексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-112">Microsoft.Isam.Esent.Interop.EsentTaskDroppedException</span></span>  

<span data-ttu-id="07e5d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07e5d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07e5d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07e5d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07e5d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07e5d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTaskDroppedException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentTaskDroppedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTaskDroppedException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="07e5d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="07e5d-116">Thread safety</span></span>

<span data-ttu-id="07e5d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="07e5d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="07e5d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="07e5d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="07e5d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07e5d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07e5d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="07e5d-120">Reference</span></span>

[<span data-ttu-id="07e5d-121">Элементы Есенттаскдроппедексцептион</span><span class="sxs-lookup"><span data-stu-id="07e5d-121">EsentTaskDroppedException members</span></span>](./esenttaskdroppedexception-members.md)

[<span data-ttu-id="07e5d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="07e5d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
