---
description: 'Дополнительные сведения о: Есентонедатабасеперсессионексцептион Class'
title: Класс Есентонедатабасеперсессионексцептион
TOCTitle: EsentOneDatabasePerSessionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentonedatabasepersessionexception(v=EXCHG.10)
ms:contentKeyID: 55102432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b5f8c69397c9105eed8b0788faf3fe24af744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711813"
---
# <a name="esentonedatabasepersessionexception-class"></a><span data-ttu-id="40e66-103">Класс Есентонедатабасеперсессионексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-103">EsentOneDatabasePerSessionException class</span></span>

<span data-ttu-id="40e66-104">Базовый класс для JET_err. Исключения Онедатабасеперсессион.</span><span class="sxs-lookup"><span data-stu-id="40e66-104">Base class for JET_err.OneDatabasePerSession exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="40e66-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="40e66-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="40e66-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="40e66-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="40e66-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="40e66-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="40e66-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="40e66-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="40e66-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="40e66-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="40e66-112">Microsoft. ISAM. ESENT. Interop. Есентонедатабасеперсессионексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-112">Microsoft.Isam.Esent.Interop.EsentOneDatabasePerSessionException</span></span>  

<span data-ttu-id="40e66-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40e66-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40e66-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40e66-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40e66-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40e66-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOneDatabasePerSessionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentOneDatabasePerSessionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOneDatabasePerSessionException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="40e66-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="40e66-116">Thread safety</span></span>

<span data-ttu-id="40e66-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="40e66-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="40e66-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="40e66-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="40e66-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40e66-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40e66-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="40e66-120">Reference</span></span>

[<span data-ttu-id="40e66-121">Элементы Есентонедатабасеперсессионексцептион</span><span class="sxs-lookup"><span data-stu-id="40e66-121">EsentOneDatabasePerSessionException members</span></span>](./esentonedatabasepersessionexception-members.md)

[<span data-ttu-id="40e66-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="40e66-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
