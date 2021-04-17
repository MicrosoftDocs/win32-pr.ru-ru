---
description: 'Дополнительные сведения о: Есентексклусиветаблелоккрекуиредексцептион Class'
title: Класс Есентексклусиветаблелоккрекуиредексцептион
TOCTitle: EsentExclusiveTableLockRequiredException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentexclusivetablelockrequiredexception(v=EXCHG.10)
ms:contentKeyID: 55101593
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c167ab3910b3ba3ce69bc4f946ba7d315256b17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702506"
---
# <a name="esentexclusivetablelockrequiredexception-class"></a><span data-ttu-id="58fc5-103">Класс Есентексклусиветаблелоккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-103">EsentExclusiveTableLockRequiredException class</span></span>

<span data-ttu-id="58fc5-104">Базовый класс для JET_err. Исключения Ексклусиветаблелоккрекуиред.</span><span class="sxs-lookup"><span data-stu-id="58fc5-104">Base class for JET_err.ExclusiveTableLockRequired exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="58fc5-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="58fc5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="58fc5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="58fc5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="58fc5-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="58fc5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="58fc5-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="58fc5-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="58fc5-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="58fc5-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="58fc5-112">Microsoft. ISAM. ESENT. Interop. Есентексклусиветаблелоккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-112">Microsoft.Isam.Esent.Interop.EsentExclusiveTableLockRequiredException</span></span>  

<span data-ttu-id="58fc5-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="58fc5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="58fc5-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="58fc5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="58fc5-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58fc5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentExclusiveTableLockRequiredException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentExclusiveTableLockRequiredException
```

``` csharp
[SerializableAttribute]
public sealed class EsentExclusiveTableLockRequiredException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="58fc5-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="58fc5-116">Thread safety</span></span>

<span data-ttu-id="58fc5-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="58fc5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="58fc5-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="58fc5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="58fc5-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58fc5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="58fc5-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="58fc5-120">Reference</span></span>

[<span data-ttu-id="58fc5-121">Элементы Есентексклусиветаблелоккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="58fc5-121">EsentExclusiveTableLockRequiredException members</span></span>](./esentexclusivetablelockrequiredexception-members.md)

[<span data-ttu-id="58fc5-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="58fc5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
