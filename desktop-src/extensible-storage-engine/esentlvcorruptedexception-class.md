---
description: 'Дополнительные сведения о: Есентлвкорруптедексцептион Class'
title: Класс Есентлвкорруптедексцептион
TOCTitle: EsentLVCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlvcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b075aa72b7ddbece409ab49e4e36bea86489de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908963"
---
# <a name="esentlvcorruptedexception-class"></a><span data-ttu-id="bacf0-103">Класс Есентлвкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-103">EsentLVCorruptedException class</span></span>

<span data-ttu-id="bacf0-104">Базовый класс для JET_err. Исключения Лвкорруптед.</span><span class="sxs-lookup"><span data-stu-id="bacf0-104">Base class for JET_err.LVCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="bacf0-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="bacf0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="bacf0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="bacf0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="bacf0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="bacf0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="bacf0-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="bacf0-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="bacf0-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="bacf0-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="bacf0-112">Microsoft. ISAM. ESENT. Interop. Есентлвкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-112">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>  

<span data-ttu-id="bacf0-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bacf0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bacf0-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bacf0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bacf0-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bacf0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLVCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLVCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLVCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="bacf0-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="bacf0-116">Thread safety</span></span>

<span data-ttu-id="bacf0-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="bacf0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="bacf0-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="bacf0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="bacf0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bacf0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bacf0-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="bacf0-120">Reference</span></span>

[<span data-ttu-id="bacf0-121">Элементы Есентлвкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="bacf0-121">EsentLVCorruptedException members</span></span>](./esentlvcorruptedexception-members.md)

[<span data-ttu-id="bacf0-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="bacf0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
