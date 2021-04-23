---
description: 'Дополнительные сведения о: Есенткоммиттедлогфилесмиссинжексцептион Class'
title: Класс Есенткоммиттедлогфилесмиссинжексцептион
TOCTitle: EsentCommittedLogFilesMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcommittedlogfilesmissingexception(v=EXCHG.10)
ms:contentKeyID: 55101361
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 937534d550ff13fce4240411ce486e6d789ef957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693372"
---
# <a name="esentcommittedlogfilesmissingexception-class"></a><span data-ttu-id="61e0d-103">Класс Есенткоммиттедлогфилесмиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-103">EsentCommittedLogFilesMissingException class</span></span>

<span data-ttu-id="61e0d-104">Базовый класс для исключений JET_err. Коммиттедлогфилесмиссинг.</span><span class="sxs-lookup"><span data-stu-id="61e0d-104">Base class for JET_err.CommittedLogFilesMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="61e0d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="61e0d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="61e0d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="61e0d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="61e0d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="61e0d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="61e0d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="61e0d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="61e0d-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="61e0d-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="61e0d-112">Microsoft. ISAM. ESENT. Interop. Есенткоммиттедлогфилесмиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-112">Microsoft.Isam.Esent.Interop.EsentCommittedLogFilesMissingException</span></span>  

<span data-ttu-id="61e0d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61e0d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61e0d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61e0d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61e0d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61e0d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCommittedLogFilesMissingException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCommittedLogFilesMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCommittedLogFilesMissingException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="61e0d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="61e0d-116">Thread safety</span></span>

<span data-ttu-id="61e0d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="61e0d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="61e0d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="61e0d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="61e0d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61e0d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61e0d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="61e0d-120">Reference</span></span>

[<span data-ttu-id="61e0d-121">Элементы Есенткоммиттедлогфилесмиссинжексцептион</span><span class="sxs-lookup"><span data-stu-id="61e0d-121">EsentCommittedLogFilesMissingException members</span></span>](./esentcommittedlogfilesmissingexception-members.md)

[<span data-ttu-id="61e0d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="61e0d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
