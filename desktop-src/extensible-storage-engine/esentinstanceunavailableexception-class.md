---
description: 'Дополнительные сведения о: Есентинстанцеунаваилабликсцептион Class'
title: Класс Есентинстанцеунаваилабликсцептион
TOCTitle: EsentInstanceUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinstanceunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101879
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c3761965a836182480ec934be344322f5b5c6a1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711593"
---
# <a name="esentinstanceunavailableexception-class"></a><span data-ttu-id="50188-103">Класс Есентинстанцеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="50188-103">EsentInstanceUnavailableException class</span></span>

<span data-ttu-id="50188-104">Базовый класс для JET_err. Исключения Инстанцеунаваилабле.</span><span class="sxs-lookup"><span data-stu-id="50188-104">Base class for JET_err.InstanceUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="50188-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="50188-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="50188-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="50188-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="50188-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="50188-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="50188-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="50188-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="50188-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="50188-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="50188-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="50188-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="50188-111">Microsoft. ISAM. ESENT. Interop. Есентфаталексцептион</span><span class="sxs-lookup"><span data-stu-id="50188-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="50188-112">Microsoft. ISAM. ESENT. Interop. Есентинстанцеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="50188-112">Microsoft.Isam.Esent.Interop.EsentInstanceUnavailableException</span></span>  

<span data-ttu-id="50188-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="50188-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="50188-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="50188-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="50188-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50188-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInstanceUnavailableException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentInstanceUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInstanceUnavailableException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="50188-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="50188-116">Thread safety</span></span>

<span data-ttu-id="50188-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="50188-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="50188-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="50188-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="50188-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50188-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="50188-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="50188-120">Reference</span></span>

[<span data-ttu-id="50188-121">Элементы Есентинстанцеунаваилабликсцептион</span><span class="sxs-lookup"><span data-stu-id="50188-121">EsentInstanceUnavailableException members</span></span>](./esentinstanceunavailableexception-members.md)

[<span data-ttu-id="50188-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="50188-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
