---
description: 'Дополнительные сведения о: Есентиндекснотфаундексцептион Class'
title: Класс Есентиндекснотфаундексцептион
TOCTitle: EsentIndexNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101767
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 559716b8d579f8293f09f0e328ef63e813067eef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702503"
---
# <a name="esentindexnotfoundexception-class"></a><span data-ttu-id="2d18b-103">Класс Есентиндекснотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-103">EsentIndexNotFoundException class</span></span>

<span data-ttu-id="2d18b-104">Базовый класс для JET_err. Исключения Индекснотфаунд.</span><span class="sxs-lookup"><span data-stu-id="2d18b-104">Base class for JET_err.IndexNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2d18b-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="2d18b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2d18b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2d18b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2d18b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2d18b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2d18b-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2d18b-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2d18b-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2d18b-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="2d18b-112">Microsoft. ISAM. ESENT. Interop. Есентиндекснотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-112">Microsoft.Isam.Esent.Interop.EsentIndexNotFoundException</span></span>  

<span data-ttu-id="2d18b-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d18b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d18b-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2d18b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d18b-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d18b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentIndexNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexNotFoundException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="2d18b-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="2d18b-116">Thread safety</span></span>

<span data-ttu-id="2d18b-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="2d18b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2d18b-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="2d18b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d18b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d18b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d18b-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="2d18b-120">Reference</span></span>

[<span data-ttu-id="2d18b-121">Элементы Есентиндекснотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="2d18b-121">EsentIndexNotFoundException members</span></span>](./esentindexnotfoundexception-members.md)

[<span data-ttu-id="2d18b-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2d18b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
