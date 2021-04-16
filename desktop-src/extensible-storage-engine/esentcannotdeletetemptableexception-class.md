---
description: 'Дополнительные сведения о: Есентканнотделететемптабликсцептион Class'
title: Класс Есентканнотделететемптабликсцептион
TOCTitle: EsentCannotDeleteTempTableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdeletetemptableexception(v=EXCHG.10)
ms:contentKeyID: 55101145
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f333798a6b151b63cbd40c69fab438ecdff68ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712655"
---
# <a name="esentcannotdeletetemptableexception-class"></a><span data-ttu-id="f73b9-103">Класс Есентканнотделететемптабликсцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-103">EsentCannotDeleteTempTableException class</span></span>

<span data-ttu-id="f73b9-104">Базовый класс для JET_err. Исключения Каннотделететемптабле.</span><span class="sxs-lookup"><span data-stu-id="f73b9-104">Base class for JET_err.CannotDeleteTempTable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f73b9-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="f73b9-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f73b9-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f73b9-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f73b9-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f73b9-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f73b9-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f73b9-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f73b9-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f73b9-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="f73b9-112">Microsoft. ISAM. ESENT. Interop. Есентканнотделететемптабликсцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-112">Microsoft.Isam.Esent.Interop.EsentCannotDeleteTempTableException</span></span>  

<span data-ttu-id="f73b9-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f73b9-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f73b9-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f73b9-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f73b9-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f73b9-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDeleteTempTableException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDeleteTempTableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDeleteTempTableException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="f73b9-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="f73b9-116">Thread safety</span></span>

<span data-ttu-id="f73b9-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="f73b9-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f73b9-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="f73b9-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f73b9-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f73b9-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f73b9-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="f73b9-120">Reference</span></span>

[<span data-ttu-id="f73b9-121">Элементы Есентканнотделететемптабликсцептион</span><span class="sxs-lookup"><span data-stu-id="f73b9-121">EsentCannotDeleteTempTableException members</span></span>](./esentcannotdeletetemptableexception-members.md)

[<span data-ttu-id="f73b9-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f73b9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
