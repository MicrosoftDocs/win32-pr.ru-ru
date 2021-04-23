---
description: 'Дополнительные сведения о: Есентверсионстореаутофмеморексцептион Class'
title: Класс Есентверсионстореаутофмеморексцептион
TOCTitle: EsentVersionStoreOutOfMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversionstoreoutofmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55103197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1780826cb9b4578a4acfd14c53a38589eca42d84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713087"
---
# <a name="esentversionstoreoutofmemoryexception-class"></a><span data-ttu-id="8bc84-103">Класс Есентверсионстореаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-103">EsentVersionStoreOutOfMemoryException class</span></span>

<span data-ttu-id="8bc84-104">Базовый класс для JET_err. Исключения Версионстореаутофмемори.</span><span class="sxs-lookup"><span data-stu-id="8bc84-104">Base class for JET_err.VersionStoreOutOfMemory exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8bc84-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="8bc84-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8bc84-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8bc84-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8bc84-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8bc84-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8bc84-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8bc84-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8bc84-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="8bc84-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="8bc84-112">Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="8bc84-113">Microsoft. ISAM. ESENT. Interop. Есентверсионстореаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-113">Microsoft.Isam.Esent.Interop.EsentVersionStoreOutOfMemoryException</span></span>  

<span data-ttu-id="8bc84-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8bc84-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8bc84-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8bc84-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc84-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bc84-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentVersionStoreOutOfMemoryException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentVersionStoreOutOfMemoryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentVersionStoreOutOfMemoryException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="8bc84-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="8bc84-117">Thread safety</span></span>

<span data-ttu-id="8bc84-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="8bc84-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8bc84-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="8bc84-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8bc84-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bc84-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8bc84-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="8bc84-121">Reference</span></span>

[<span data-ttu-id="8bc84-122">Элементы Есентверсионстореаутофмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="8bc84-122">EsentVersionStoreOutOfMemoryException members</span></span>](./esentversionstoreoutofmemoryexception-members.md)

[<span data-ttu-id="8bc84-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8bc84-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
