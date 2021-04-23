---
description: 'Дополнительные сведения о: Есентмултивалуединдексвиолатионексцептион Class'
title: Класс Есентмултивалуединдексвиолатионексцептион
TOCTitle: EsentMultiValuedIndexViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedindexviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102266
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cafb4ce44f3b0600997e9d715f882e95869f65b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692530"
---
# <a name="esentmultivaluedindexviolationexception-class"></a><span data-ttu-id="fd40f-103">Класс Есентмултивалуединдексвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-103">EsentMultiValuedIndexViolationException class</span></span>

<span data-ttu-id="fd40f-104">Базовый класс для JET_err. Исключения Мултивалуединдексвиолатион.</span><span class="sxs-lookup"><span data-stu-id="fd40f-104">Base class for JET_err.MultiValuedIndexViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fd40f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="fd40f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fd40f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fd40f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fd40f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="fd40f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fd40f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fd40f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fd40f-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="fd40f-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="fd40f-112">Microsoft. ISAM. ESENT. Interop. Есентмултивалуединдексвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedIndexViolationException</span></span>  

<span data-ttu-id="fd40f-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fd40f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fd40f-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fd40f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fd40f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd40f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedIndexViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedIndexViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedIndexViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="fd40f-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="fd40f-116">Thread safety</span></span>

<span data-ttu-id="fd40f-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="fd40f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fd40f-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="fd40f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd40f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd40f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fd40f-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="fd40f-120">Reference</span></span>

[<span data-ttu-id="fd40f-121">Элементы Есентмултивалуединдексвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="fd40f-121">EsentMultiValuedIndexViolationException members</span></span>](./esentmultivaluedindexviolationexception-members.md)

[<span data-ttu-id="fd40f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fd40f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
