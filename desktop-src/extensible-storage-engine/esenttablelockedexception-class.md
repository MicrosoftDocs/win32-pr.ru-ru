---
description: 'Дополнительные сведения о: Есенттаблелоккедексцептион Class'
title: Класс Есенттаблелоккедексцептион
TOCTitle: EsentTableLockedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTableLockedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttablelockedexception(v=EXCHG.10)
ms:contentKeyID: 55102975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTableLockedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTableLockedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 427aae831534f25ab8df974eb60dbdf5f6e692e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702263"
---
# <a name="esenttablelockedexception-class"></a><span data-ttu-id="6b4af-103">Класс Есенттаблелоккедексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-103">EsentTableLockedException class</span></span>

<span data-ttu-id="6b4af-104">Базовый класс для JET_err. Исключения Таблелоккед.</span><span class="sxs-lookup"><span data-stu-id="6b4af-104">Base class for JET_err.TableLocked exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6b4af-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="6b4af-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6b4af-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6b4af-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6b4af-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="6b4af-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6b4af-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6b4af-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6b4af-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6b4af-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="6b4af-112">Microsoft. ISAM. ESENT. Interop. Есенттаблелоккедексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-112">Microsoft.Isam.Esent.Interop.EsentTableLockedException</span></span>  

<span data-ttu-id="6b4af-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b4af-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6b4af-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6b4af-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b4af-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b4af-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTableLockedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTableLockedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTableLockedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="6b4af-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="6b4af-116">Thread safety</span></span>

<span data-ttu-id="6b4af-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="6b4af-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6b4af-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="6b4af-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b4af-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b4af-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b4af-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="6b4af-120">Reference</span></span>

[<span data-ttu-id="6b4af-121">Элементы Есенттаблелоккедексцептион</span><span class="sxs-lookup"><span data-stu-id="6b4af-121">EsentTableLockedException members</span></span>](./esenttablelockedexception-members.md)

[<span data-ttu-id="6b4af-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6b4af-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
