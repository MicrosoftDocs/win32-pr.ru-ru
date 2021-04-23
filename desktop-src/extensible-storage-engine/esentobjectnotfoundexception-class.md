---
description: 'Дополнительные сведения о: Есентобжектнотфаундексцептион Class'
title: Класс Есентобжектнотфаундексцептион
TOCTitle: EsentObjectNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentobjectnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55102350
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d30eb09898142b25549ff4318059b4a373c31d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263324"
---
# <a name="esentobjectnotfoundexception-class"></a><span data-ttu-id="fe00d-103">Класс Есентобжектнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-103">EsentObjectNotFoundException class</span></span>

<span data-ttu-id="fe00d-104">Базовый класс для JET_err. Исключения ObjectNotFound.</span><span class="sxs-lookup"><span data-stu-id="fe00d-104">Base class for JET_err.ObjectNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fe00d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="fe00d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fe00d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fe00d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fe00d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="fe00d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="fe00d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="fe00d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="fe00d-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="fe00d-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="fe00d-112">Microsoft. ISAM. ESENT. Interop. Есентобжектнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-112">Microsoft.Isam.Esent.Interop.EsentObjectNotFoundException</span></span>  

<span data-ttu-id="fe00d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fe00d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fe00d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fe00d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fe00d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe00d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentObjectNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentObjectNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentObjectNotFoundException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="fe00d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="fe00d-116">Thread safety</span></span>

<span data-ttu-id="fe00d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="fe00d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fe00d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="fe00d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fe00d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe00d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fe00d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="fe00d-120">Reference</span></span>

[<span data-ttu-id="fe00d-121">Элементы Есентобжектнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="fe00d-121">EsentObjectNotFoundException members</span></span>](./esentobjectnotfoundexception-members.md)

[<span data-ttu-id="fe00d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fe00d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
