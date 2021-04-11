---
description: 'Дополнительные сведения о: Есентбадпажелинкексцептион Class'
title: Класс Есентбадпажелинкексцептион
TOCTitle: EsentBadPageLinkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadPageLinkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadpagelinkexception(v=EXCHG.10)
ms:contentKeyID: 55101138
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadPageLinkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadPageLinkException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308d0e220e2c39411d22622f907db6ce46013842
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272194"
---
# <a name="esentbadpagelinkexception-class"></a><span data-ttu-id="52ac4-103">Класс Есентбадпажелинкексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-103">EsentBadPageLinkException class</span></span>

<span data-ttu-id="52ac4-104">Базовый класс для JET_err. Исключения Бадпажелинк.</span><span class="sxs-lookup"><span data-stu-id="52ac4-104">Base class for JET_err.BadPageLink exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="52ac4-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="52ac4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="52ac4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="52ac4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="52ac4-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="52ac4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="52ac4-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="52ac4-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="52ac4-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="52ac4-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="52ac4-112">Microsoft. ISAM. ESENT. Interop. Есентбадпажелинкексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-112">Microsoft.Isam.Esent.Interop.EsentBadPageLinkException</span></span>  

<span data-ttu-id="52ac4-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="52ac4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="52ac4-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="52ac4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="52ac4-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52ac4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadPageLinkException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadPageLinkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadPageLinkException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="52ac4-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="52ac4-116">Thread safety</span></span>

<span data-ttu-id="52ac4-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="52ac4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="52ac4-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="52ac4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="52ac4-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52ac4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="52ac4-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="52ac4-120">Reference</span></span>

[<span data-ttu-id="52ac4-121">Элементы Есентбадпажелинкексцептион</span><span class="sxs-lookup"><span data-stu-id="52ac4-121">EsentBadPageLinkException members</span></span>](./esentbadpagelinkexception-members.md)

[<span data-ttu-id="52ac4-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="52ac4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
