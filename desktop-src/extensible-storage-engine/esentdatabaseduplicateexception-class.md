---
description: 'Дополнительные сведения о: Есентдатабаседупликатиксцептион Class'
title: Класс Есентдатабаседупликатиксцептион
TOCTitle: EsentDatabaseDuplicateException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseDuplicateException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseduplicateexception(v=EXCHG.10)
ms:contentKeyID: 55101346
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDuplicateException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseDuplicateException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e469604b6c68aa7a54c17c086ae8474ccf03079d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145679"
---
# <a name="esentdatabaseduplicateexception-class"></a><span data-ttu-id="ebc93-103">Класс Есентдатабаседупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-103">EsentDatabaseDuplicateException class</span></span>

<span data-ttu-id="ebc93-104">Базовый класс для JET_err. Исключения Датабаседупликате.</span><span class="sxs-lookup"><span data-stu-id="ebc93-104">Base class for JET_err.DatabaseDuplicate exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ebc93-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ebc93-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ebc93-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ebc93-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ebc93-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ebc93-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ebc93-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ebc93-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ebc93-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ebc93-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ebc93-112">Microsoft. ISAM. ESENT. Interop. Есентдатабаседупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-112">Microsoft.Isam.Esent.Interop.EsentDatabaseDuplicateException</span></span>  

<span data-ttu-id="ebc93-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebc93-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ebc93-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebc93-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc93-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebc93-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseDuplicateException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseDuplicateException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseDuplicateException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ebc93-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ebc93-116">Thread safety</span></span>

<span data-ttu-id="ebc93-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ebc93-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ebc93-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ebc93-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebc93-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebc93-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebc93-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ebc93-120">Reference</span></span>

[<span data-ttu-id="ebc93-121">Элементы Есентдатабаседупликатиксцептион</span><span class="sxs-lookup"><span data-stu-id="ebc93-121">EsentDatabaseDuplicateException members</span></span>](./esentdatabaseduplicateexception-members.md)

[<span data-ttu-id="ebc93-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ebc93-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
