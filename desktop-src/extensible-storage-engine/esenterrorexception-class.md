---
description: 'Дополнительные сведения о: Есентеррорексцептион Class'
title: Класс EsentErrorException
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb05197392c1d5c8798968254b24d2d0ae677bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081000"
---
# <a name="esenterrorexception-class"></a><span data-ttu-id="ed102-103">Класс EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ed102-103">EsentErrorException class</span></span>

<span data-ttu-id="ed102-104">Базовый класс для исключений ошибок ESENT.</span><span class="sxs-lookup"><span data-stu-id="ed102-104">Base class for ESENT error exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ed102-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ed102-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ed102-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ed102-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ed102-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ed102-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ed102-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      <span data-ttu-id="ed102-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>  
        [<span data-ttu-id="ed102-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
        [<span data-ttu-id="ed102-111">Microsoft. ISAM. ESENT. Interop. Есентканнотлогдурингрековериредоексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-111">Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException</span></span>](./esentcannotlogduringrecoveryredoexception-class.md)  
        [<span data-ttu-id="ed102-112">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-112">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
        [<span data-ttu-id="ed102-113">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-113">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
        [<span data-ttu-id="ed102-114">Microsoft. ISAM. ESENT. Interop. Есентпревиаусверсионексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-114">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>](./esentpreviousversionexception-class.md)  
        [<span data-ttu-id="ed102-115">Microsoft. ISAM. ESENT. Interop. Есентверсионсторинтритубижексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-115">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>](./esentversionstoreentrytoobigexception-class.md)  

<span data-ttu-id="ed102-116">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed102-116">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed102-117">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed102-117">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed102-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed102-118">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a><span data-ttu-id="ed102-119">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ed102-119">Thread safety</span></span>

<span data-ttu-id="ed102-120">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ed102-120">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ed102-121">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ed102-121">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed102-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed102-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed102-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="ed102-123">Reference</span></span>

[<span data-ttu-id="ed102-124">Элементы Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ed102-124">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="ed102-125">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ed102-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
