---
description: 'Дополнительные сведения о: Есентдатабасеалреадируннингмаинтенанцеексцептион Class'
title: Класс Есентдатабасеалреадируннингмаинтенанцеексцептион
TOCTitle: EsentDatabaseAlreadyRunningMaintenanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasealreadyrunningmaintenanceexception(v=EXCHG.10)
ms:contentKeyID: 55101317
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8c9f9f65df8db69762f6ec6bca72ad3903cd72ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143660"
---
# <a name="esentdatabasealreadyrunningmaintenanceexception-class"></a><span data-ttu-id="00756-103">Класс Есентдатабасеалреадируннингмаинтенанцеексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-103">EsentDatabaseAlreadyRunningMaintenanceException class</span></span>

<span data-ttu-id="00756-104">Базовый класс для JET_err. Исключения Датабасеалреадируннингмаинтенанце.</span><span class="sxs-lookup"><span data-stu-id="00756-104">Base class for JET_err.DatabaseAlreadyRunningMaintenance exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="00756-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="00756-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="00756-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="00756-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="00756-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="00756-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="00756-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="00756-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="00756-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="00756-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="00756-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеалреадируннингмаинтенанцеексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-112">Microsoft.Isam.Esent.Interop.EsentDatabaseAlreadyRunningMaintenanceException</span></span>  

<span data-ttu-id="00756-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="00756-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="00756-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="00756-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="00756-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00756-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseAlreadyRunningMaintenanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseAlreadyRunningMaintenanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseAlreadyRunningMaintenanceException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="00756-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="00756-116">Thread safety</span></span>

<span data-ttu-id="00756-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="00756-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="00756-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="00756-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="00756-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00756-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="00756-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="00756-120">Reference</span></span>

[<span data-ttu-id="00756-121">Элементы Есентдатабасеалреадируннингмаинтенанцеексцептион</span><span class="sxs-lookup"><span data-stu-id="00756-121">EsentDatabaseAlreadyRunningMaintenanceException members</span></span>](./esentdatabasealreadyrunningmaintenanceexception-members.md)

[<span data-ttu-id="00756-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="00756-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
