---
description: 'Дополнительные сведения о: Есентвритеконфликтексцептион Class'
title: Класс Есентвритеконфликтексцептион
TOCTitle: EsentWriteConflictException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentWriteConflictException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentwriteconflictexception(v=EXCHG.10)
ms:contentKeyID: 55103199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentWriteConflictException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fffcb0b2bb07e12dc4dd9f86de5c22b13aca66b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703356"
---
# <a name="esentwriteconflictexception-class"></a><span data-ttu-id="ac2e0-103">Класс Есентвритеконфликтексцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-103">EsentWriteConflictException class</span></span>

<span data-ttu-id="ac2e0-104">Базовый класс для JET_err. Исключения Вритеконфликт.</span><span class="sxs-lookup"><span data-stu-id="ac2e0-104">Base class for JET_err.WriteConflict exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ac2e0-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ac2e0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ac2e0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ac2e0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ac2e0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ac2e0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ac2e0-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ac2e0-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ac2e0-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ac2e0-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="ac2e0-112">Microsoft. ISAM. ESENT. Interop. Есентвритеконфликтексцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-112">Microsoft.Isam.Esent.Interop.EsentWriteConflictException</span></span>  

<span data-ttu-id="ac2e0-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac2e0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac2e0-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ac2e0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2e0-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac2e0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentWriteConflictException _
    Inherits EsentStateException
'Usage
Dim instance As EsentWriteConflictException
```

``` csharp
[SerializableAttribute]
public sealed class EsentWriteConflictException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="ac2e0-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ac2e0-116">Thread safety</span></span>

<span data-ttu-id="ac2e0-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ac2e0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ac2e0-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ac2e0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac2e0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac2e0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac2e0-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ac2e0-120">Reference</span></span>

[<span data-ttu-id="ac2e0-121">Элементы Есентвритеконфликтексцептион</span><span class="sxs-lookup"><span data-stu-id="ac2e0-121">EsentWriteConflictException members</span></span>](./esentwriteconflictexception-members.md)

[<span data-ttu-id="ac2e0-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ac2e0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
