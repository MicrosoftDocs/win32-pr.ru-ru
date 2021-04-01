---
description: 'Дополнительные сведения о: Есентмустбесепарателонгвалуиксцептион Class'
title: Класс Есентмустбесепарателонгвалуиксцептион
TOCTitle: EsentMustBeSeparateLongValueException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmustbeseparatelongvalueexception(v=EXCHG.10)
ms:contentKeyID: 55102269
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07e9ddb913450e8c3e974c07fd3ad13ed09bfc38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263718"
---
# <a name="esentmustbeseparatelongvalueexception-class"></a><span data-ttu-id="3825c-103">Класс Есентмустбесепарателонгвалуиксцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-103">EsentMustBeSeparateLongValueException class</span></span>

<span data-ttu-id="3825c-104">Базовый класс для JET_err. Исключения Мустбесепарателонгвалуе.</span><span class="sxs-lookup"><span data-stu-id="3825c-104">Base class for JET_err.MustBeSeparateLongValue exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3825c-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="3825c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3825c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3825c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3825c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3825c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3825c-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3825c-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3825c-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3825c-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="3825c-112">Microsoft. ISAM. ESENT. Interop. Есентмустбесепарателонгвалуиксцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-112">Microsoft.Isam.Esent.Interop.EsentMustBeSeparateLongValueException</span></span>  

<span data-ttu-id="3825c-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3825c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3825c-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3825c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3825c-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3825c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMustBeSeparateLongValueException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMustBeSeparateLongValueException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMustBeSeparateLongValueException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="3825c-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="3825c-116">Thread safety</span></span>

<span data-ttu-id="3825c-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="3825c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3825c-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3825c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3825c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3825c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3825c-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="3825c-120">Reference</span></span>

[<span data-ttu-id="3825c-121">Элементы Есентмустбесепарателонгвалуиксцептион</span><span class="sxs-lookup"><span data-stu-id="3825c-121">EsentMustBeSeparateLongValueException members</span></span>](./esentmustbeseparatelongvalueexception-members.md)

[<span data-ttu-id="3825c-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3825c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
