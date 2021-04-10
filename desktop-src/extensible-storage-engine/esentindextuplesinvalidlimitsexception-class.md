---
description: 'Дополнительные сведения о: Есентиндекступлесинвалидлимитсексцептион Class'
title: Класс Есентиндекступлесинвалидлимитсексцептион
TOCTitle: EsentIndexTuplesInvalidLimitsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexTuplesInvalidLimitsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindextuplesinvalidlimitsexception(v=EXCHG.10)
ms:contentKeyID: 55101849
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesInvalidLimitsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexTuplesInvalidLimitsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdc5f8e8466b6339d6bfce5f97ac33032c0e6a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265158"
---
# <a name="esentindextuplesinvalidlimitsexception-class"></a><span data-ttu-id="08b4e-103">Класс Есентиндекступлесинвалидлимитсексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-103">EsentIndexTuplesInvalidLimitsException class</span></span>

<span data-ttu-id="08b4e-104">Базовый класс для JET_err. Исключения Индекступлесинвалидлимитс.</span><span class="sxs-lookup"><span data-stu-id="08b4e-104">Base class for JET_err.IndexTuplesInvalidLimits exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="08b4e-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="08b4e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="08b4e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="08b4e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="08b4e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="08b4e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="08b4e-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="08b4e-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="08b4e-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="08b4e-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="08b4e-112">Microsoft. ISAM. ESENT. Interop. Есентиндекступлесинвалидлимитсексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-112">Microsoft.Isam.Esent.Interop.EsentIndexTuplesInvalidLimitsException</span></span>  

<span data-ttu-id="08b4e-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08b4e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08b4e-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08b4e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08b4e-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08b4e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexTuplesInvalidLimitsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentIndexTuplesInvalidLimitsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexTuplesInvalidLimitsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="08b4e-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="08b4e-116">Thread safety</span></span>

<span data-ttu-id="08b4e-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="08b4e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="08b4e-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="08b4e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="08b4e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08b4e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08b4e-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="08b4e-120">Reference</span></span>

[<span data-ttu-id="08b4e-121">Элементы Есентиндекступлесинвалидлимитсексцептион</span><span class="sxs-lookup"><span data-stu-id="08b4e-121">EsentIndexTuplesInvalidLimitsException members</span></span>](./esentindextuplesinvalidlimitsexception-members.md)

[<span data-ttu-id="08b4e-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="08b4e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
