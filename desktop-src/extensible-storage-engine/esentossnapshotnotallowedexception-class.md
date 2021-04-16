---
description: 'Дополнительные сведения о: Есентосснапшотноталловедексцептион Class'
title: Класс Есентосснапшотноталловедексцептион
TOCTitle: EsentOSSnapshotNotAllowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentossnapshotnotallowedexception(v=EXCHG.10)
ms:contentKeyID: 55102388
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d2c11340f937e7622d1740061a1b7eac2e7887a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692935"
---
# <a name="esentossnapshotnotallowedexception-class"></a><span data-ttu-id="7c6bc-103">Класс Есентосснапшотноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-103">EsentOSSnapshotNotAllowedException class</span></span>

<span data-ttu-id="7c6bc-104">Базовый класс для JET_err. Исключения Осснапшотноталловед.</span><span class="sxs-lookup"><span data-stu-id="7c6bc-104">Base class for JET_err.OSSnapshotNotAllowed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7c6bc-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="7c6bc-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7c6bc-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7c6bc-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7c6bc-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7c6bc-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7c6bc-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7c6bc-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7c6bc-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7c6bc-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="7c6bc-112">Microsoft. ISAM. ESENT. Interop. Есентосснапшотноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-112">Microsoft.Isam.Esent.Interop.EsentOSSnapshotNotAllowedException</span></span>  

<span data-ttu-id="7c6bc-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7c6bc-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7c6bc-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7c6bc-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6bc-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c6bc-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOSSnapshotNotAllowedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentOSSnapshotNotAllowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOSSnapshotNotAllowedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="7c6bc-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="7c6bc-116">Thread safety</span></span>

<span data-ttu-id="7c6bc-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="7c6bc-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7c6bc-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7c6bc-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c6bc-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c6bc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7c6bc-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="7c6bc-120">Reference</span></span>

[<span data-ttu-id="7c6bc-121">Элементы Есентосснапшотноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="7c6bc-121">EsentOSSnapshotNotAllowedException members</span></span>](./esentossnapshotnotallowedexception-members.md)

[<span data-ttu-id="7c6bc-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7c6bc-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
