---
description: 'Дополнительные сведения о: Есенттуманинстанцесексцептион Class'
title: Класс Есенттуманинстанцесексцептион
TOCTitle: EsentTooManyInstancesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyinstancesexception(v=EXCHG.10)
ms:contentKeyID: 55103084
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ecd20f6a05a17d4bd21623732a4e716e82c9b1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712597"
---
# <a name="esenttoomanyinstancesexception-class"></a><span data-ttu-id="5ead9-103">Класс Есенттуманинстанцесексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-103">EsentTooManyInstancesException class</span></span>

<span data-ttu-id="5ead9-104">Базовый класс для JET_err. Исключения Туманинстанцес.</span><span class="sxs-lookup"><span data-stu-id="5ead9-104">Base class for JET_err.TooManyInstances exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5ead9-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="5ead9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5ead9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5ead9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5ead9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5ead9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5ead9-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5ead9-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5ead9-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="5ead9-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="5ead9-112">Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="5ead9-113">Microsoft. ISAM. ESENT. Interop. Есенттуманинстанцесексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-113">Microsoft.Isam.Esent.Interop.EsentTooManyInstancesException</span></span>  

<span data-ttu-id="5ead9-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ead9-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ead9-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5ead9-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ead9-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ead9-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyInstancesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyInstancesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyInstancesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="5ead9-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="5ead9-117">Thread safety</span></span>

<span data-ttu-id="5ead9-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="5ead9-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5ead9-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="5ead9-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5ead9-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ead9-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ead9-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="5ead9-121">Reference</span></span>

[<span data-ttu-id="5ead9-122">Элементы Есенттуманинстанцесексцептион</span><span class="sxs-lookup"><span data-stu-id="5ead9-122">EsentTooManyInstancesException members</span></span>](./esenttoomanyinstancesexception-members.md)

[<span data-ttu-id="5ead9-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5ead9-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
