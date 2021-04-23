---
description: 'Дополнительные сведения о: Есенттранстудипексцептион Class'
title: Класс Есенттранстудипексцептион
TOCTitle: EsentTransTooDeepException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTransTooDeepException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttranstoodeepexception(v=EXCHG.10)
ms:contentKeyID: 55107315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTransTooDeepException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTransTooDeepException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7b56840a053c6f3ea0106700447986d8b706877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693112"
---
# <a name="esenttranstoodeepexception-class"></a><span data-ttu-id="89dc9-103">Класс Есенттранстудипексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-103">EsentTransTooDeepException class</span></span>

<span data-ttu-id="89dc9-104">Базовый класс для JET_err. Исключения Транстудип.</span><span class="sxs-lookup"><span data-stu-id="89dc9-104">Base class for JET_err.TransTooDeep exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="89dc9-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="89dc9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="89dc9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="89dc9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="89dc9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="89dc9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="89dc9-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="89dc9-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="89dc9-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="89dc9-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="89dc9-112">Microsoft. ISAM. ESENT. Interop. Есенттранстудипексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-112">Microsoft.Isam.Esent.Interop.EsentTransTooDeepException</span></span>  

<span data-ttu-id="89dc9-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89dc9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89dc9-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89dc9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89dc9-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89dc9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTransTooDeepException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTransTooDeepException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTransTooDeepException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="89dc9-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="89dc9-116">Thread safety</span></span>

<span data-ttu-id="89dc9-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="89dc9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="89dc9-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="89dc9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="89dc9-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89dc9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89dc9-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="89dc9-120">Reference</span></span>

[<span data-ttu-id="89dc9-121">Элементы Есенттранстудипексцептион</span><span class="sxs-lookup"><span data-stu-id="89dc9-121">EsentTransTooDeepException members</span></span>](./esenttranstoodeepexception-members.md)

[<span data-ttu-id="89dc9-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="89dc9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
