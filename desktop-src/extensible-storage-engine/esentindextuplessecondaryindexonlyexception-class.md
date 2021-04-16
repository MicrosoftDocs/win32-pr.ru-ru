---
description: 'Дополнительные сведения о: Есентиндекступлессекондариндексонлексцептион Class'
title: Класс Есентиндекступлессекондариндексонлексцептион
TOCTitle: EsentIndexTuplesSecondaryIndexOnlyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindextuplessecondaryindexonlyexception(v=EXCHG.10)
ms:contentKeyID: 55101794
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8dcba7dee44e1645f1ba934a6440f2ab69adc79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542639"
---
# <a name="esentindextuplessecondaryindexonlyexception-class"></a><span data-ttu-id="6f1b0-103">Класс Есентиндекступлессекондариндексонлексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-103">EsentIndexTuplesSecondaryIndexOnlyException class</span></span>

<span data-ttu-id="6f1b0-104">Базовый класс для JET_err. Исключения Индекступлессекондариндексонли.</span><span class="sxs-lookup"><span data-stu-id="6f1b0-104">Base class for JET_err.IndexTuplesSecondaryIndexOnly exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6f1b0-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="6f1b0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6f1b0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6f1b0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6f1b0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="6f1b0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6f1b0-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6f1b0-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6f1b0-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6f1b0-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="6f1b0-112">Microsoft. ISAM. ESENT. Interop. Есентиндекступлессекондариндексонлексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-112">Microsoft.Isam.Esent.Interop.EsentIndexTuplesSecondaryIndexOnlyException</span></span>  

<span data-ttu-id="6f1b0-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6f1b0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6f1b0-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6f1b0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1b0-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f1b0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexTuplesSecondaryIndexOnlyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexTuplesSecondaryIndexOnlyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexTuplesSecondaryIndexOnlyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="6f1b0-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="6f1b0-116">Thread safety</span></span>

<span data-ttu-id="6f1b0-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="6f1b0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6f1b0-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="6f1b0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f1b0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f1b0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6f1b0-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="6f1b0-120">Reference</span></span>

[<span data-ttu-id="6f1b0-121">Элементы Есентиндекступлессекондариндексонлексцептион</span><span class="sxs-lookup"><span data-stu-id="6f1b0-121">EsentIndexTuplesSecondaryIndexOnlyException members</span></span>](./esentindextuplessecondaryindexonlyexception-members.md)

[<span data-ttu-id="6f1b0-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6f1b0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
