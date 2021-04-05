---
description: 'Дополнительные сведения о: Есентдатабасеинусиксцептион Class'
title: Класс Есентдатабасеинусиксцептион
TOCTitle: EsentDatabaseInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101372
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97ce4cc0a02b322a0abfc882ee0fce398fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897546"
---
# <a name="esentdatabaseinuseexception-class"></a><span data-ttu-id="75daa-103">Класс Есентдатабасеинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-103">EsentDatabaseInUseException class</span></span>

<span data-ttu-id="75daa-104">Базовый класс для JET_err. Исключения Датабасеинусе.</span><span class="sxs-lookup"><span data-stu-id="75daa-104">Base class for JET_err.DatabaseInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="75daa-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="75daa-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="75daa-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="75daa-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="75daa-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="75daa-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="75daa-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="75daa-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="75daa-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="75daa-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="75daa-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException</span></span>  

<span data-ttu-id="75daa-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75daa-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75daa-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="75daa-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75daa-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75daa-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="75daa-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="75daa-116">Thread safety</span></span>

<span data-ttu-id="75daa-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="75daa-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="75daa-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="75daa-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="75daa-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75daa-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75daa-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="75daa-120">Reference</span></span>

[<span data-ttu-id="75daa-121">Элементы Есентдатабасеинусиксцептион</span><span class="sxs-lookup"><span data-stu-id="75daa-121">EsentDatabaseInUseException members</span></span>](./esentdatabaseinuseexception-members.md)

[<span data-ttu-id="75daa-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="75daa-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
