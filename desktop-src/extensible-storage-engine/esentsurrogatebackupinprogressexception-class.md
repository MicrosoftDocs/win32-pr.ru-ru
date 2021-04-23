---
description: 'Дополнительные сведения о: Есентсуррогатебаккупинпрогрессексцептион Class'
title: Класс Есентсуррогатебаккупинпрогрессексцептион
TOCTitle: EsentSurrogateBackupInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsurrogatebackupinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55102946
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 545d23eefb547089244a43e24646324dd5551b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693191"
---
# <a name="esentsurrogatebackupinprogressexception-class"></a><span data-ttu-id="3fc3b-103">Класс Есентсуррогатебаккупинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-103">EsentSurrogateBackupInProgressException class</span></span>

<span data-ttu-id="3fc3b-104">Базовый класс для JET_err. Исключения Суррогатебаккупинпрогресс.</span><span class="sxs-lookup"><span data-stu-id="3fc3b-104">Base class for JET_err.SurrogateBackupInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3fc3b-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="3fc3b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3fc3b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3fc3b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3fc3b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3fc3b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3fc3b-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3fc3b-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3fc3b-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3fc3b-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="3fc3b-112">Microsoft. ISAM. ESENT. Interop. Есентсуррогатебаккупинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-112">Microsoft.Isam.Esent.Interop.EsentSurrogateBackupInProgressException</span></span>  

<span data-ttu-id="3fc3b-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3fc3b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3fc3b-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3fc3b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc3b-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fc3b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSurrogateBackupInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentSurrogateBackupInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSurrogateBackupInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="3fc3b-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="3fc3b-116">Thread safety</span></span>

<span data-ttu-id="3fc3b-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="3fc3b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3fc3b-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3fc3b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3fc3b-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fc3b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3fc3b-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="3fc3b-120">Reference</span></span>

[<span data-ttu-id="3fc3b-121">Элементы Есентсуррогатебаккупинпрогрессексцептион</span><span class="sxs-lookup"><span data-stu-id="3fc3b-121">EsentSurrogateBackupInProgressException members</span></span>](./esentsurrogatebackupinprogressexception-members.md)

[<span data-ttu-id="3fc3b-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3fc3b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
