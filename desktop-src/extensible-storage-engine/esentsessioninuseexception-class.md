---
description: 'Дополнительные сведения о: Есентсессионинусиксцептион Class'
title: Класс Есентсессионинусиксцептион
TOCTitle: EsentSessionInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioninuseexception(v=EXCHG.10)
ms:contentKeyID: 55102709
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b956d88e1a8c59f23bedc25fadcacd234841572b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719528"
---
# <a name="esentsessioninuseexception-class"></a><span data-ttu-id="4e6cd-103">Класс Есентсессионинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-103">EsentSessionInUseException class</span></span>

<span data-ttu-id="4e6cd-104">Базовый класс для JET_err. Исключения Сессионинусе.</span><span class="sxs-lookup"><span data-stu-id="4e6cd-104">Base class for JET_err.SessionInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4e6cd-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4e6cd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4e6cd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4e6cd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4e6cd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4e6cd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4e6cd-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4e6cd-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4e6cd-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4e6cd-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="4e6cd-112">Microsoft. ISAM. ESENT. Interop. Есентсессионинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-112">Microsoft.Isam.Esent.Interop.EsentSessionInUseException</span></span>  

<span data-ttu-id="4e6cd-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4e6cd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4e6cd-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4e6cd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6cd-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e6cd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="4e6cd-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4e6cd-116">Thread safety</span></span>

<span data-ttu-id="4e6cd-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4e6cd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4e6cd-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4e6cd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e6cd-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e6cd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4e6cd-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4e6cd-120">Reference</span></span>

[<span data-ttu-id="4e6cd-121">Элементы Есентсессионинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="4e6cd-121">EsentSessionInUseException members</span></span>](./esentsessioninuseexception-members.md)

[<span data-ttu-id="4e6cd-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4e6cd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
