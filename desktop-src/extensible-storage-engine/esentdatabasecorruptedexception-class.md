---
description: 'Дополнительные сведения о: Есентдатабасекорруптедексцептион Class'
title: Класс Есентдатабасекорруптедексцептион
TOCTitle: EsentDatabaseCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasecorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a82a0ec101223bae64b39a4db2ca0779d671591c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897842"
---
# <a name="esentdatabasecorruptedexception-class"></a><span data-ttu-id="d2d14-103">Класс Есентдатабасекорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-103">EsentDatabaseCorruptedException class</span></span>

<span data-ttu-id="d2d14-104">Базовый класс для JET_err. Исключения Датабасекорруптед.</span><span class="sxs-lookup"><span data-stu-id="d2d14-104">Base class for JET_err.DatabaseCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d2d14-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="d2d14-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d2d14-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d2d14-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d2d14-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d2d14-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d2d14-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d2d14-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d2d14-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d2d14-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="d2d14-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасекорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-112">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>  

<span data-ttu-id="d2d14-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d2d14-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d2d14-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d2d14-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d14-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2d14-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDatabaseCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="d2d14-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="d2d14-116">Thread safety</span></span>

<span data-ttu-id="d2d14-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="d2d14-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d2d14-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="d2d14-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2d14-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2d14-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d2d14-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="d2d14-120">Reference</span></span>

[<span data-ttu-id="d2d14-121">Элементы Есентдатабасекорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="d2d14-121">EsentDatabaseCorruptedException members</span></span>](./esentdatabasecorruptedexception-members.md)

[<span data-ttu-id="d2d14-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d2d14-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
