---
description: 'Дополнительные сведения о: Есентсессионконтекстнотсетбисиссреадексцептион Class'
title: Класс Есентсессионконтекстнотсетбисиссреадексцептион
TOCTitle: EsentSessionContextNotSetByThisThreadException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextnotsetbythisthreadexception(v=EXCHG.10)
ms:contentKeyID: 55102698
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 097712353336a9a412dd4255781a42c74eac1782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647647"
---
# <a name="esentsessioncontextnotsetbythisthreadexception-class"></a><span data-ttu-id="4eae6-103">Класс Есентсессионконтекстнотсетбисиссреадексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-103">EsentSessionContextNotSetByThisThreadException class</span></span>

<span data-ttu-id="4eae6-104">Базовый класс для JET_err. Исключения Сессионконтекстнотсетбисиссреад.</span><span class="sxs-lookup"><span data-stu-id="4eae6-104">Base class for JET_err.SessionContextNotSetByThisThread exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4eae6-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="4eae6-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4eae6-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4eae6-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4eae6-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4eae6-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4eae6-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4eae6-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4eae6-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4eae6-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="4eae6-112">Microsoft. ISAM. ESENT. Interop. Есентсессионконтекстнотсетбисиссреадексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-112">Microsoft.Isam.Esent.Interop.EsentSessionContextNotSetByThisThreadException</span></span>  

<span data-ttu-id="4eae6-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4eae6-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4eae6-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4eae6-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4eae6-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4eae6-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextNotSetByThisThreadException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextNotSetByThisThreadException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextNotSetByThisThreadException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="4eae6-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="4eae6-116">Thread safety</span></span>

<span data-ttu-id="4eae6-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="4eae6-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4eae6-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="4eae6-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4eae6-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4eae6-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4eae6-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="4eae6-120">Reference</span></span>

[<span data-ttu-id="4eae6-121">Элементы Есентсессионконтекстнотсетбисиссреадексцептион</span><span class="sxs-lookup"><span data-stu-id="4eae6-121">EsentSessionContextNotSetByThisThreadException members</span></span>](./esentsessioncontextnotsetbythisthreadexception-members.md)

[<span data-ttu-id="4eae6-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4eae6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
