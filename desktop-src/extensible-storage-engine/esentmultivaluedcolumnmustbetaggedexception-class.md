---
description: 'Дополнительные сведения о: Есентмултивалуедколумнмустбетагжедексцептион Class'
title: Класс Есентмултивалуедколумнмустбетагжедексцептион
TOCTitle: EsentMultiValuedColumnMustBeTaggedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmultivaluedcolumnmustbetaggedexception(v=EXCHG.10)
ms:contentKeyID: 55102318
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 300b3b74aaf8277dd014256685b4ad375abe2ccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702129"
---
# <a name="esentmultivaluedcolumnmustbetaggedexception-class"></a><span data-ttu-id="b3d9c-103">Класс Есентмултивалуедколумнмустбетагжедексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-103">EsentMultiValuedColumnMustBeTaggedException class</span></span>

<span data-ttu-id="b3d9c-104">Базовый класс для JET_err. Исключения Мултивалуедколумнмустбетагжед.</span><span class="sxs-lookup"><span data-stu-id="b3d9c-104">Base class for JET_err.MultiValuedColumnMustBeTagged exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b3d9c-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b3d9c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b3d9c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b3d9c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b3d9c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b3d9c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b3d9c-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b3d9c-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b3d9c-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b3d9c-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b3d9c-112">Microsoft. ISAM. ESENT. Interop. Есентмултивалуедколумнмустбетагжедексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-112">Microsoft.Isam.Esent.Interop.EsentMultiValuedColumnMustBeTaggedException</span></span>  

<span data-ttu-id="b3d9c-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3d9c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b3d9c-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b3d9c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d9c-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3d9c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMultiValuedColumnMustBeTaggedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentMultiValuedColumnMustBeTaggedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMultiValuedColumnMustBeTaggedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b3d9c-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b3d9c-116">Thread safety</span></span>

<span data-ttu-id="b3d9c-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b3d9c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b3d9c-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b3d9c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3d9c-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3d9c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3d9c-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="b3d9c-120">Reference</span></span>

[<span data-ttu-id="b3d9c-121">Элементы Есентмултивалуедколумнмустбетагжедексцептион</span><span class="sxs-lookup"><span data-stu-id="b3d9c-121">EsentMultiValuedColumnMustBeTaggedException members</span></span>](./esentmultivaluedcolumnmustbetaggedexception-members.md)

[<span data-ttu-id="b3d9c-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b3d9c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
