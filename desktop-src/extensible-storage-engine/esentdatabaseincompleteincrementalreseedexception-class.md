---
description: 'Дополнительные сведения о: Есентдатабасеинкомплетеинкременталресидексцептион Class'
title: Класс Есентдатабасеинкомплетеинкременталресидексцептион
TOCTitle: EsentDatabaseIncompleteIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseincompleteincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101478
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 65d660c28f9b876e0cb2016631a4a8108a52b6dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542215"
---
# <a name="esentdatabaseincompleteincrementalreseedexception-class"></a><span data-ttu-id="8ea79-103">Класс Есентдатабасеинкомплетеинкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-103">EsentDatabaseIncompleteIncrementalReseedException class</span></span>

<span data-ttu-id="8ea79-104">Базовый класс для JET_err. Исключения Датабасеинкомплетеинкременталресид.</span><span class="sxs-lookup"><span data-stu-id="8ea79-104">Base class for JET_err.DatabaseIncompleteIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8ea79-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="8ea79-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8ea79-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8ea79-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8ea79-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8ea79-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8ea79-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8ea79-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8ea79-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="8ea79-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="8ea79-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеинкомплетеинкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-112">Microsoft.Isam.Esent.Interop.EsentDatabaseIncompleteIncrementalReseedException</span></span>  

<span data-ttu-id="8ea79-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ea79-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ea79-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8ea79-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea79-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ea79-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseIncompleteIncrementalReseedException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDatabaseIncompleteIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseIncompleteIncrementalReseedException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="8ea79-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="8ea79-116">Thread safety</span></span>

<span data-ttu-id="8ea79-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="8ea79-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8ea79-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="8ea79-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ea79-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ea79-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ea79-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="8ea79-120">Reference</span></span>

[<span data-ttu-id="8ea79-121">Элементы Есентдатабасеинкомплетеинкременталресидексцептион</span><span class="sxs-lookup"><span data-stu-id="8ea79-121">EsentDatabaseIncompleteIncrementalReseedException members</span></span>](./esentdatabaseincompleteincrementalreseedexception-members.md)

[<span data-ttu-id="8ea79-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="8ea79-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
