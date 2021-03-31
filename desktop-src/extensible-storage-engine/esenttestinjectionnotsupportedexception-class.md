---
description: 'Дополнительные сведения о: Есенттестинжектионнотсуппортедексцептион Class'
title: Класс Есенттестинжектионнотсуппортедексцептион
TOCTitle: EsentTestInjectionNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttestinjectionnotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55103041
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07d640aa0429ac6fce63b07f873a26ea536a6261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272654"
---
# <a name="esenttestinjectionnotsupportedexception-class"></a><span data-ttu-id="9b9e8-103">Класс Есенттестинжектионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-103">EsentTestInjectionNotSupportedException class</span></span>

<span data-ttu-id="9b9e8-104">Базовый класс для JET_err. Исключения Тестинжектионнотсуппортед.</span><span class="sxs-lookup"><span data-stu-id="9b9e8-104">Base class for JET_err.TestInjectionNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9b9e8-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="9b9e8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9b9e8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9b9e8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9b9e8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9b9e8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9b9e8-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9b9e8-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9b9e8-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="9b9e8-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="9b9e8-112">Microsoft. ISAM. ESENT. Interop. Есенттестинжектионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-112">Microsoft.Isam.Esent.Interop.EsentTestInjectionNotSupportedException</span></span>  

<span data-ttu-id="9b9e8-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9b9e8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9b9e8-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9b9e8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9e8-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b9e8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTestInjectionNotSupportedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentTestInjectionNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTestInjectionNotSupportedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="9b9e8-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="9b9e8-116">Thread safety</span></span>

<span data-ttu-id="9b9e8-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="9b9e8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9b9e8-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="9b9e8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9b9e8-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b9e8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9b9e8-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="9b9e8-120">Reference</span></span>

[<span data-ttu-id="9b9e8-121">Элементы Есенттестинжектионнотсуппортедексцептион</span><span class="sxs-lookup"><span data-stu-id="9b9e8-121">EsentTestInjectionNotSupportedException members</span></span>](./esenttestinjectionnotsupportedexception-members.md)

[<span data-ttu-id="9b9e8-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="9b9e8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
