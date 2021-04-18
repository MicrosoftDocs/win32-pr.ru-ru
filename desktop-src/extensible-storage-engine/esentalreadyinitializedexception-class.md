---
description: 'Дополнительные сведения о: Есенталреадинитиализедексцептион Class'
title: Класс Есенталреадинитиализедексцептион
TOCTitle: EsentAlreadyInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentalreadyinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55101047
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffc1cb0a1de8b3e7873ec48fce26507cfc45dd3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719620"
---
# <a name="esentalreadyinitializedexception-class"></a><span data-ttu-id="094fb-103">Класс Есенталреадинитиализедексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-103">EsentAlreadyInitializedException class</span></span>

<span data-ttu-id="094fb-104">Базовый класс для JET_err. Исключения Алреадинитиализед.</span><span class="sxs-lookup"><span data-stu-id="094fb-104">Base class for JET_err.AlreadyInitialized exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="094fb-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="094fb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="094fb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="094fb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="094fb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="094fb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="094fb-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="094fb-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="094fb-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="094fb-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="094fb-112">Microsoft. ISAM. ESENT. Interop. Есенталреадинитиализедексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-112">Microsoft.Isam.Esent.Interop.EsentAlreadyInitializedException</span></span>  

<span data-ttu-id="094fb-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="094fb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="094fb-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="094fb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="094fb-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="094fb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAlreadyInitializedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentAlreadyInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAlreadyInitializedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="094fb-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="094fb-116">Thread safety</span></span>

<span data-ttu-id="094fb-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="094fb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="094fb-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="094fb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="094fb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="094fb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="094fb-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="094fb-120">Reference</span></span>

[<span data-ttu-id="094fb-121">Элементы Есенталреадинитиализедексцептион</span><span class="sxs-lookup"><span data-stu-id="094fb-121">EsentAlreadyInitializedException members</span></span>](./esentalreadyinitializedexception-members.md)

[<span data-ttu-id="094fb-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="094fb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
