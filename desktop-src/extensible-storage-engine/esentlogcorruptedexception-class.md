---
description: 'Дополнительные сведения о: Есентлогкорруптедексцептион Class'
title: Класс Есентлогкорруптедексцептион
TOCTitle: EsentLogCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55107292
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 962f27ee891434691531f44e400e39a19bfc98ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693534"
---
# <a name="esentlogcorruptedexception-class"></a><span data-ttu-id="22863-103">Класс Есентлогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-103">EsentLogCorruptedException class</span></span>

<span data-ttu-id="22863-104">Базовый класс для JET_err. Исключения Логкорруптед.</span><span class="sxs-lookup"><span data-stu-id="22863-104">Base class for JET_err.LogCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="22863-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="22863-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="22863-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="22863-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="22863-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="22863-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="22863-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="22863-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="22863-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="22863-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="22863-112">Microsoft. ISAM. ESENT. Interop. Есентлогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptedException</span></span>  

<span data-ttu-id="22863-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="22863-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="22863-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="22863-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="22863-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22863-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="22863-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="22863-116">Thread safety</span></span>

<span data-ttu-id="22863-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="22863-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="22863-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="22863-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="22863-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22863-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="22863-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="22863-120">Reference</span></span>

[<span data-ttu-id="22863-121">Элементы Есентлогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="22863-121">EsentLogCorruptedException members</span></span>](./esentlogcorruptedexception-members.md)

[<span data-ttu-id="22863-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="22863-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
