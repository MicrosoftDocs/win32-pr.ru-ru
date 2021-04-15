---
description: 'Дополнительные сведения о: Есентаутофдатабасеспацеексцептион Class'
title: Класс Есентаутофдатабасеспацеексцептион
TOCTitle: EsentOutOfDatabaseSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdatabasespaceexception(v=EXCHG.10)
ms:contentKeyID: 55102410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ece3a81fa0687299edba0857b15f4c0abc50e403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662880"
---
# <a name="esentoutofdatabasespaceexception-class"></a><span data-ttu-id="ba9ad-103">Класс Есентаутофдатабасеспацеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-103">EsentOutOfDatabaseSpaceException class</span></span>

<span data-ttu-id="ba9ad-104">Базовый класс для JET_err. Исключения Аутофдатабасеспаце.</span><span class="sxs-lookup"><span data-stu-id="ba9ad-104">Base class for JET_err.OutOfDatabaseSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ba9ad-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ba9ad-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ba9ad-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ba9ad-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ba9ad-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ba9ad-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ba9ad-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ba9ad-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ba9ad-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="ba9ad-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="ba9ad-112">Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="ba9ad-113">Microsoft. ISAM. ESENT. Interop. Есентаутофдатабасеспацеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>  

<span data-ttu-id="ba9ad-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ba9ad-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ba9ad-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ba9ad-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ba9ad-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba9ad-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDatabaseSpaceException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentOutOfDatabaseSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDatabaseSpaceException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="ba9ad-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ba9ad-117">Thread safety</span></span>

<span data-ttu-id="ba9ad-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ba9ad-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ba9ad-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ba9ad-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba9ad-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba9ad-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ba9ad-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="ba9ad-121">Reference</span></span>

[<span data-ttu-id="ba9ad-122">Элементы Есентаутофдатабасеспацеексцептион</span><span class="sxs-lookup"><span data-stu-id="ba9ad-122">EsentOutOfDatabaseSpaceException members</span></span>](./esentoutofdatabasespaceexception-members.md)

[<span data-ttu-id="ba9ad-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ba9ad-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
