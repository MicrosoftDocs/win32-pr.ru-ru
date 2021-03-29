---
description: 'Дополнительные сведения: класс экземпляра'
title: Класс экземпляра
TOCTitle: Instance class
ms:assetid: T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance(v=EXCHG.10)
ms:contentKeyID: 55103260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Instance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Instance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b717286a9d07b7eb17b87354cbe0896cf182f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811135"
---
# <a name="instance-class"></a><span data-ttu-id="12c7d-103">Класс экземпляра</span><span class="sxs-lookup"><span data-stu-id="12c7d-103">Instance class</span></span>

<span data-ttu-id="12c7d-104">Класс, инкапсулирующий [JET_INSTANCE](./jet-instance-structure.md) в удаляемом объекте.</span><span class="sxs-lookup"><span data-stu-id="12c7d-104">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="12c7d-105">Экземпляр должен быть закрыт последним, а закрытие экземпляра освобождает все остальные ресурсы для экземпляра.</span><span class="sxs-lookup"><span data-stu-id="12c7d-105">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="12c7d-106">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="12c7d-106">Inheritance hierarchy</span></span>

[<span data-ttu-id="12c7d-107">System.Object</span><span class="sxs-lookup"><span data-stu-id="12c7d-107">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="12c7d-108">System. Runtime. Констраинедексекутион. CriticalFinalizerObject</span><span class="sxs-lookup"><span data-stu-id="12c7d-108">System.Runtime.ConstrainedExecution.CriticalFinalizerObject</span></span>](/dotnet/api/system.runtime.constrainedexecution.criticalfinalizerobject)  
    [<span data-ttu-id="12c7d-109">System.Runtime.InteropServices.SafeHandle</span><span class="sxs-lookup"><span data-stu-id="12c7d-109">System.Runtime.InteropServices.SafeHandle</span></span>](/dotnet/api/system.runtime.interopservices.safehandle)  
      [<span data-ttu-id="12c7d-110">Microsoft. Win32. SafeHandle. Сафехандлезерурминусонеисинвалид</span><span class="sxs-lookup"><span data-stu-id="12c7d-110">Microsoft.Win32.SafeHandles.SafeHandleZeroOrMinusOneIsInvalid</span></span>](/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid)  
        <span data-ttu-id="12c7d-111">Microsoft. ISAM. ESENT. Interop. instance</span><span class="sxs-lookup"><span data-stu-id="12c7d-111">Microsoft.Isam.Esent.Interop.Instance</span></span>  

<span data-ttu-id="12c7d-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="12c7d-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="12c7d-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="12c7d-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="12c7d-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12c7d-114">Syntax</span></span>

``` vb
'Declaration
Public Class Instance _
    Inherits SafeHandleZeroOrMinusOneIsInvalid
'Usage
Dim instance As Instance
```

``` csharp
public class Instance : SafeHandleZeroOrMinusOneIsInvalid
```

## <a name="thread-safety"></a><span data-ttu-id="12c7d-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="12c7d-115">Thread safety</span></span>

<span data-ttu-id="12c7d-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="12c7d-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="12c7d-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="12c7d-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="12c7d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12c7d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="12c7d-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="12c7d-119">Reference</span></span>

[<span data-ttu-id="12c7d-120">Члены экземпляра</span><span class="sxs-lookup"><span data-stu-id="12c7d-120">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="12c7d-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="12c7d-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
