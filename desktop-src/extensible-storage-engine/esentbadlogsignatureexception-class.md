---
description: 'Дополнительные сведения о: Есентбадлогсигнатуриксцептион Class'
title: Класс Есентбадлогсигнатуриксцептион
TOCTitle: EsentBadLogSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101128
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a77f5ae2b8c7148e80f2ea3163837dc9028e5510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702983"
---
# <a name="esentbadlogsignatureexception-class"></a><span data-ttu-id="c417f-103">Класс Есентбадлогсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-103">EsentBadLogSignatureException class</span></span>

<span data-ttu-id="c417f-104">Базовый класс для JET_err. Исключения Бадлогсигнатуре.</span><span class="sxs-lookup"><span data-stu-id="c417f-104">Base class for JET_err.BadLogSignature exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c417f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="c417f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c417f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c417f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c417f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c417f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c417f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c417f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c417f-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="c417f-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="c417f-112">Microsoft. ISAM. ESENT. Interop. Есентбадлогсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-112">Microsoft.Isam.Esent.Interop.EsentBadLogSignatureException</span></span>  

<span data-ttu-id="c417f-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c417f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c417f-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c417f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c417f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c417f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="c417f-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="c417f-116">Thread safety</span></span>

<span data-ttu-id="c417f-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="c417f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c417f-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="c417f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c417f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c417f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c417f-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="c417f-120">Reference</span></span>

[<span data-ttu-id="c417f-121">Элементы Есентбадлогсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="c417f-121">EsentBadLogSignatureException members</span></span>](./esentbadlogsignatureexception-members.md)

[<span data-ttu-id="c417f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c417f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
