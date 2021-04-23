---
description: 'Дополнительные сведения о: Есентфаталексцептион Class'
title: Класс EsentFatalException
TOCTitle: EsentFatalException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFatalException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfatalexception(v=EXCHG.10)
ms:contentKeyID: 55101653
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFatalException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFatalException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c38df447f2eb816772713ba930204e75aa38a88c
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "104273202"
---
# <a name="esentfatalexception-class"></a><span data-ttu-id="68fd5-103">Класс EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="68fd5-103">EsentFatalException class</span></span>

<span data-ttu-id="68fd5-104">Базовый класс для неустранимых исключений.</span><span class="sxs-lookup"><span data-stu-id="68fd5-104">Base class for Fatal exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="68fd5-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="68fd5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="68fd5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="68fd5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="68fd5-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="68fd5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="68fd5-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="68fd5-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="68fd5-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="68fd5-111">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            

<span data-ttu-id="68fd5-112">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="68fd5-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="68fd5-113">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="68fd5-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="68fd5-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68fd5-114">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFatalException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentFatalException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFatalException : EsentOperationException
```

## <a name="thread-safety"></a><span data-ttu-id="68fd5-115">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="68fd5-115">Thread safety</span></span>

<span data-ttu-id="68fd5-116">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="68fd5-116">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="68fd5-117">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="68fd5-117">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="68fd5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68fd5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="68fd5-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="68fd5-119">Reference</span></span>

[<span data-ttu-id="68fd5-120">Элементы Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-120">EsentFatalException members</span></span>](./esentfatalexception-members.md)

[<span data-ttu-id="68fd5-121">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="68fd5-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="68fd5-122">Производные типы</span><span class="sxs-lookup"><span data-stu-id="68fd5-122">Derived types</span></span>

[<span data-ttu-id="68fd5-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="68fd5-123">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="68fd5-124">System. Exception</span><span class="sxs-lookup"><span data-stu-id="68fd5-124">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="68fd5-125">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-125">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="68fd5-126">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-126">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="68fd5-127">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-127">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          <span data-ttu-id="68fd5-128">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-128">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>  
            [<span data-ttu-id="68fd5-129">Microsoft. ISAM. ESENT. Interop. Есентинстанцеунаваилабледуетофаталлогдискфуллексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-129">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableDueToFatalLogDiskFullException</span></span>](./esentinstanceunavailableduetofatallogdiskfullexception-class.md)  
            [<span data-ttu-id="68fd5-130">Microsoft. ISAM. ESENT. Interop. Есентинстанцеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-130">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>](./esentinstanceunavailableexception-class.md)  
            [<span data-ttu-id="68fd5-131">Microsoft. ISAM. ESENT. Interop. Есентлогдисабледдуеторековерифаилуриксцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-131">Microsoft.Isam.Esent.Interop.EsentLogDisabledDueToRecoveryFailureException</span></span>](./esentlogdisabledduetorecoveryfailureexception-class.md)  
            [<span data-ttu-id="68fd5-132">Microsoft. ISAM. ESENT. Interop. Есентроллбаккеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-132">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>](./esentrollbackerrorexception-class.md)  
            [<span data-ttu-id="68fd5-133">Microsoft. ISAM. ESENT. Interop. Есентсекторсизенотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-133">Microsoft.Isam.Esent.Interop.EsentSectorSizeNotSupportedException</span></span>](./esentsectorsizenotsupportedexception-class.md)  
            [<span data-ttu-id="68fd5-134">Microsoft. ISAM. ESENT. Interop. Есентунлоадаблеосфунктионалитексцептион</span><span class="sxs-lookup"><span data-stu-id="68fd5-134">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>](./esentunloadableosfunctionalityexception-class.md)