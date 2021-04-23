---
description: 'Дополнительные сведения о: Есентнуллкэйдисалловедексцептион Class'
title: Класс Есентнуллкэйдисалловедексцептион
TOCTitle: EsentNullKeyDisallowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnullkeydisallowedexception(v=EXCHG.10)
ms:contentKeyID: 55102391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3b38e043572b1182cd099664cf09dfc229efc8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702447"
---
# <a name="esentnullkeydisallowedexception-class"></a><span data-ttu-id="7a089-103">Класс Есентнуллкэйдисалловедексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-103">EsentNullKeyDisallowedException class</span></span>

<span data-ttu-id="7a089-104">Базовый класс для JET_err. Исключения Нуллкэйдисалловед.</span><span class="sxs-lookup"><span data-stu-id="7a089-104">Base class for JET_err.NullKeyDisallowed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7a089-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="7a089-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7a089-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7a089-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7a089-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7a089-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7a089-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7a089-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7a089-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7a089-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="7a089-112">Microsoft. ISAM. ESENT. Interop. Есентнуллкэйдисалловедексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-112">Microsoft.Isam.Esent.Interop.EsentNullKeyDisallowedException</span></span>  

<span data-ttu-id="7a089-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a089-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a089-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a089-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a089-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a089-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNullKeyDisallowedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNullKeyDisallowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNullKeyDisallowedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="7a089-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="7a089-116">Thread safety</span></span>

<span data-ttu-id="7a089-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="7a089-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7a089-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7a089-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a089-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a089-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a089-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="7a089-120">Reference</span></span>

[<span data-ttu-id="7a089-121">Элементы Есентнуллкэйдисалловедексцептион</span><span class="sxs-lookup"><span data-stu-id="7a089-121">EsentNullKeyDisallowedException members</span></span>](./esentnullkeydisallowedexception-members.md)

[<span data-ttu-id="7a089-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7a089-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
