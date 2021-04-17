---
description: 'Дополнительные сведения о: Есентмултивалуеддупликатиксцептион Class'
title: Класс Есентмултивалуеддупликатиксцептион
TOCTitle: EsentMultiValuedDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55102340
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fddfac316bb8ad13ff5c42abc8041e4a18c85321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673583"
---
# <a name="esentmultivaluedduplicateexception-class"></a><span data-ttu-id="7d2ba-103">Класс Есентмултивалуеддупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-103">EsentMultiValuedDuplicateException class</span></span>

<span data-ttu-id="7d2ba-104">Базовый класс для JET_err. Исключения Мултивалуеддупликате.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-104">Base class for JET_err.MultiValuedDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7d2ba-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="7d2ba-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7d2ba-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7d2ba-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7d2ba-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7d2ba-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7d2ba-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7d2ba-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7d2ba-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7d2ba-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="7d2ba-112">Microsoft. ISAM. ESENT. Interop. Есентмултивалуеддупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedDuplicateException</span></span>  

<span data-ttu-id="7d2ba-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d2ba-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d2ba-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d2ba-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d2ba-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d2ba-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedDuplicateException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMultiValuedDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedDuplicateException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="7d2ba-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="7d2ba-116">Thread safety</span></span>

<span data-ttu-id="7d2ba-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7d2ba-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7d2ba-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d2ba-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d2ba-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d2ba-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="7d2ba-120">Reference</span></span>

[<span data-ttu-id="7d2ba-121">Элементы Есентмултивалуеддупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="7d2ba-121">EsentMultiValuedDuplicateException members</span></span>](./esentmultivaluedduplicateexception-members.md)

[<span data-ttu-id="7d2ba-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7d2ba-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
