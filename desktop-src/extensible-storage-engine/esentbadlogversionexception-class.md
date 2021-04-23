---
description: 'Дополнительные сведения о: Есентбадлогверсионексцептион Class'
title: Класс Есентбадлогверсионексцептион
TOCTitle: EsentBadLogVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadlogversionexception(v=EXCHG.10)
ms:contentKeyID: 55101079
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadLogVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e1bdf96dd46fdd16a566c2a6cc5047f4a74fef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498045"
---
# <a name="esentbadlogversionexception-class"></a><span data-ttu-id="4c76d-103">Класс Есентбадлогверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-103">EsentBadLogVersionException class</span></span>

<span data-ttu-id="4c76d-104">Базовый класс для JET_err. Исключения Бадлогверсион.</span><span class="sxs-lookup"><span data-stu-id="4c76d-104">Base class for JET_err.BadLogVersion exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4c76d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4c76d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4c76d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4c76d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4c76d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4c76d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4c76d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4c76d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4c76d-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="4c76d-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="4c76d-112">Microsoft. ISAM. ESENT. Interop. Есентбадлогверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-112">Microsoft.Isam.Esent.Interop.EsentBadLogVersionException</span></span>  

<span data-ttu-id="4c76d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4c76d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4c76d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4c76d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4c76d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c76d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadLogVersionException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentBadLogVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadLogVersionException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="4c76d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4c76d-116">Thread safety</span></span>

<span data-ttu-id="4c76d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4c76d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4c76d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4c76d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4c76d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c76d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4c76d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4c76d-120">Reference</span></span>

[<span data-ttu-id="4c76d-121">Элементы Есентбадлогверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="4c76d-121">EsentBadLogVersionException members</span></span>](./esentbadlogversionexception-members.md)

[<span data-ttu-id="4c76d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4c76d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
