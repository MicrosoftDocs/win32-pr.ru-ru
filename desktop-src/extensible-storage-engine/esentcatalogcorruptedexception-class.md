---
description: 'Дополнительные сведения о: Есенткаталогкорруптедексцептион Class'
title: Класс Есенткаталогкорруптедексцептион
TOCTitle: EsentCatalogCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcatalogcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01b6e9859920ff9e85dff59b1cf71dd5903d7e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544639"
---
# <a name="esentcatalogcorruptedexception-class"></a><span data-ttu-id="394ca-103">Класс Есенткаталогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-103">EsentCatalogCorruptedException class</span></span>

<span data-ttu-id="394ca-104">Базовый класс для JET_err. Исключения Каталогкорруптед.</span><span class="sxs-lookup"><span data-stu-id="394ca-104">Base class for JET_err.CatalogCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="394ca-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="394ca-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="394ca-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="394ca-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="394ca-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="394ca-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="394ca-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="394ca-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="394ca-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="394ca-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="394ca-112">Microsoft. ISAM. ESENT. Interop. Есенткаталогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-112">Microsoft.Isam.Esent.Interop.EsentCatalogCorruptedException</span></span>  

<span data-ttu-id="394ca-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="394ca-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="394ca-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="394ca-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="394ca-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="394ca-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCatalogCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCatalogCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCatalogCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="394ca-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="394ca-116">Thread safety</span></span>

<span data-ttu-id="394ca-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="394ca-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="394ca-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="394ca-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="394ca-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="394ca-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="394ca-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="394ca-120">Reference</span></span>

[<span data-ttu-id="394ca-121">Элементы Есенткаталогкорруптедексцептион</span><span class="sxs-lookup"><span data-stu-id="394ca-121">EsentCatalogCorruptedException members</span></span>](./esentcatalogcorruptedexception-members.md)

[<span data-ttu-id="394ca-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="394ca-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
