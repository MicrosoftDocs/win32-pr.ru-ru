---
description: 'Дополнительные сведения о: Есентрестореинпрогрессексцептион Class'
title: Класс Есентрестореинпрогрессексцептион
TOCTitle: EsentRestoreInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrestoreinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102631
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0906d1ee8c196260d36da8d385a0e48e12f31018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693792"
---
# <a name="esentrestoreinprogressexception-class"></a><span data-ttu-id="aa5b1-103">Класс Есентрестореинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-103">EsentRestoreInProgressException class</span></span>

<span data-ttu-id="aa5b1-104">Базовый класс для JET_err. Исключения Рестореинпрогресс.</span><span class="sxs-lookup"><span data-stu-id="aa5b1-104">Base class for JET_err.RestoreInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="aa5b1-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="aa5b1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="aa5b1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="aa5b1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="aa5b1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="aa5b1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="aa5b1-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="aa5b1-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="aa5b1-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="aa5b1-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="aa5b1-112">Microsoft. ISAM. ESENT. Interop. Есентрестореинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-112">Microsoft.Isam.Esent.Interop.EsentRestoreInProgressException</span></span>  

<span data-ttu-id="aa5b1-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aa5b1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="aa5b1-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aa5b1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5b1-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa5b1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRestoreInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRestoreInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRestoreInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="aa5b1-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="aa5b1-116">Thread safety</span></span>

<span data-ttu-id="aa5b1-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="aa5b1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="aa5b1-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="aa5b1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa5b1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa5b1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aa5b1-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="aa5b1-120">Reference</span></span>

[<span data-ttu-id="aa5b1-121">Элементы Есентрестореинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="aa5b1-121">EsentRestoreInProgressException members</span></span>](./esentrestoreinprogressexception-members.md)

[<span data-ttu-id="aa5b1-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="aa5b1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
