---
description: 'Дополнительные сведения о: Есентапиексцептион Class'
title: Класс Есентапиексцептион
TOCTitle: EsentApiException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentApiException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101032
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentApiException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b01747d2ecb197ce99617b8c9206d4fada8c2a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272533"
---
# <a name="esentapiexception-class"></a><span data-ttu-id="e33a0-103">Класс Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-103">EsentApiException class</span></span>

<span data-ttu-id="e33a0-104">Базовый класс для исключений API.</span><span class="sxs-lookup"><span data-stu-id="e33a0-104">Base class for API exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e33a0-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e33a0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e33a0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e33a0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e33a0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e33a0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e33a0-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e33a0-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="e33a0-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>  
          [<span data-ttu-id="e33a0-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
          [<span data-ttu-id="e33a0-112">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-112">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
          [<span data-ttu-id="e33a0-113">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-113">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  

<span data-ttu-id="e33a0-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e33a0-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e33a0-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e33a0-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e33a0-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e33a0-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentApiException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentApiException
```

``` csharp
[SerializableAttribute]
public abstract class EsentApiException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="e33a0-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e33a0-117">Thread safety</span></span>

<span data-ttu-id="e33a0-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e33a0-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e33a0-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e33a0-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e33a0-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e33a0-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e33a0-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="e33a0-121">Reference</span></span>

[<span data-ttu-id="e33a0-122">Элементы Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e33a0-122">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="e33a0-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e33a0-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
