---
description: 'Дополнительные сведения о: Есентентрипоинтнотфаундексцептион Class'
title: Класс Есентентрипоинтнотфаундексцептион
TOCTitle: EsentEntryPointNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esententrypointnotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101642
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7bbc8d66af82c5f232ccc94f14b81f2987748e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712603"
---
# <a name="esententrypointnotfoundexception-class"></a><span data-ttu-id="e7f6d-103">Класс Есентентрипоинтнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-103">EsentEntryPointNotFoundException class</span></span>

<span data-ttu-id="e7f6d-104">Базовый класс для JET_err. Исключения Ентрипоинтнотфаунд.</span><span class="sxs-lookup"><span data-stu-id="e7f6d-104">Base class for JET_err.EntryPointNotFound exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e7f6d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e7f6d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e7f6d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e7f6d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e7f6d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e7f6d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e7f6d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e7f6d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e7f6d-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e7f6d-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e7f6d-112">Microsoft. ISAM. ESENT. Interop. Есентентрипоинтнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-112">Microsoft.Isam.Esent.Interop.EsentEntryPointNotFoundException</span></span>  

<span data-ttu-id="e7f6d-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7f6d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7f6d-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7f6d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f6d-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7f6d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentEntryPointNotFoundException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentEntryPointNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentEntryPointNotFoundException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e7f6d-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e7f6d-116">Thread safety</span></span>

<span data-ttu-id="e7f6d-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e7f6d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e7f6d-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e7f6d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7f6d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7f6d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7f6d-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e7f6d-120">Reference</span></span>

[<span data-ttu-id="e7f6d-121">Элементы Есентентрипоинтнотфаундексцептион</span><span class="sxs-lookup"><span data-stu-id="e7f6d-121">EsentEntryPointNotFoundException members</span></span>](./esententrypointnotfoundexception-members.md)

[<span data-ttu-id="e7f6d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e7f6d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
