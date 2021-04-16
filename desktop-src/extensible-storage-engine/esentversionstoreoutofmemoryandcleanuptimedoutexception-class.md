---
description: 'Дополнительные сведения о: Есентверсионстореаутофмеморяндклеануптимедаутексцептион Class'
title: Класс Есентверсионстореаутофмеморяндклеануптимедаутексцептион
TOCTitle: EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryandcleanuptimedoutexception(v=EXCHG.10)
ms:contentKeyID: 55103240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 58cfb5343bd4de471dc73cb0fa5a57729dde5b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712169"
---
# <a name="esentversionstoreoutofmemoryandcleanuptimedoutexception-class"></a><span data-ttu-id="b4c70-103">Класс Есентверсионстореаутофмеморяндклеануптимедаутексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-103">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException class</span></span>

<span data-ttu-id="b4c70-104">Базовый класс для JET_err. Исключения Версионстореаутофмеморяндклеануптимедаут.</span><span class="sxs-lookup"><span data-stu-id="b4c70-104">Base class for JET_err.VersionStoreOutOfMemoryAndCleanupTimedOut exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b4c70-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b4c70-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b4c70-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b4c70-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b4c70-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b4c70-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b4c70-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b4c70-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b4c70-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b4c70-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b4c70-112">Microsoft. ISAM. ESENT. Interop. Есентверсионстореаутофмеморяндклеануптимедаутексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-112">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryAndCleanupTimedOutException</span></span>  

<span data-ttu-id="b4c70-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4c70-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4c70-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4c70-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4c70-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4c70-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryAndCleanupTimedOutException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryAndCleanupTimedOutException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b4c70-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b4c70-116">Thread safety</span></span>

<span data-ttu-id="b4c70-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b4c70-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b4c70-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b4c70-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4c70-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4c70-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4c70-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="b4c70-120">Reference</span></span>

[<span data-ttu-id="b4c70-121">Элементы Есентверсионстореаутофмеморяндклеануптимедаутексцептион</span><span class="sxs-lookup"><span data-stu-id="b4c70-121">EsentVersionStoreOutOfMemoryAndCleanupTimedOutException members</span></span>](./esentversionstoreoutofmemoryandcleanuptimedoutexception-members.md)

[<span data-ttu-id="b4c70-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b4c70-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
