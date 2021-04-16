---
description: 'Дополнительные сведения о: Есенттуманимемпулентриесексцептион Class'
title: Класс Есенттуманимемпулентриесексцептион
TOCTitle: EsentTooManyMempoolEntriesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanymempoolentriesexception(v=EXCHG.10)
ms:contentKeyID: 55103097
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 454abe6d19fedb2f318696b80d166f181e19fb0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684304"
---
# <a name="esenttoomanymempoolentriesexception-class"></a><span data-ttu-id="dda29-103">Класс Есенттуманимемпулентриесексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-103">EsentTooManyMempoolEntriesException class</span></span>

<span data-ttu-id="dda29-104">Базовый класс для JET_err. Исключения Туманимемпулентриес.</span><span class="sxs-lookup"><span data-stu-id="dda29-104">Base class for JET_err.TooManyMempoolEntries exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dda29-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="dda29-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dda29-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dda29-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dda29-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="dda29-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dda29-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dda29-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dda29-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="dda29-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="dda29-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="dda29-113">Microsoft. ISAM. ESENT. Interop. Есенттуманимемпулентриесексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-113">Microsoft.Isam.Esent.Interop.EsentTooManyMempoolEntriesException</span></span>  

<span data-ttu-id="dda29-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dda29-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dda29-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dda29-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dda29-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dda29-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyMempoolEntriesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyMempoolEntriesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyMempoolEntriesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="dda29-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="dda29-117">Thread safety</span></span>

<span data-ttu-id="dda29-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="dda29-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dda29-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="dda29-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dda29-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dda29-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dda29-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="dda29-121">Reference</span></span>

[<span data-ttu-id="dda29-122">Элементы Есенттуманимемпулентриесексцептион</span><span class="sxs-lookup"><span data-stu-id="dda29-122">EsentTooManyMempoolEntriesException members</span></span>](./esenttoomanymempoolentriesexception-members.md)

[<span data-ttu-id="dda29-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="dda29-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
