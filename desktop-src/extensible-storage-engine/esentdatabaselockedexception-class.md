---
description: 'Дополнительные сведения о: Есентдатабаселоккедексцептион Class'
title: Класс Есентдатабаселоккедексцептион
TOCTitle: EsentDatabaseLockedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaselockedexception(v=EXCHG.10)
ms:contentKeyID: 55101527
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97001b234c845d6453818aeeb5a930d090382278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692466"
---
# <a name="esentdatabaselockedexception-class"></a><span data-ttu-id="78750-103">Класс Есентдатабаселоккедексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-103">EsentDatabaseLockedException class</span></span>

<span data-ttu-id="78750-104">Базовый класс для JET_err. Исключения Датабаселоккед.</span><span class="sxs-lookup"><span data-stu-id="78750-104">Base class for JET_err.DatabaseLocked exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="78750-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="78750-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="78750-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="78750-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="78750-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="78750-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="78750-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="78750-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="78750-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="78750-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="78750-112">Microsoft. ISAM. ESENT. Interop. Есентдатабаселоккедексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-112">Microsoft.Isam.Esent.Interop.EsentDatabaseLockedException</span></span>  

<span data-ttu-id="78750-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="78750-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="78750-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="78750-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="78750-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78750-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseLockedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseLockedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseLockedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="78750-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="78750-116">Thread safety</span></span>

<span data-ttu-id="78750-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="78750-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="78750-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="78750-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="78750-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78750-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="78750-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="78750-120">Reference</span></span>

[<span data-ttu-id="78750-121">Элементы Есентдатабаселоккедексцептион</span><span class="sxs-lookup"><span data-stu-id="78750-121">EsentDatabaseLockedException members</span></span>](./esentdatabaselockedexception-members.md)

[<span data-ttu-id="78750-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="78750-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
