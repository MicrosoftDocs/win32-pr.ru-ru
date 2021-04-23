---
description: 'Дополнительные сведения о: Есентроллбаккрекуиредексцептион Class'
title: Класс Есентроллбаккрекуиредексцептион
TOCTitle: EsentRollbackRequiredException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackrequiredexception(v=EXCHG.10)
ms:contentKeyID: 55107325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 12baa9d69400cfd84c54184132c45aba4095b427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812041"
---
# <a name="esentrollbackrequiredexception-class"></a><span data-ttu-id="ace08-103">Класс Есентроллбаккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-103">EsentRollbackRequiredException class</span></span>

<span data-ttu-id="ace08-104">Базовый класс для JET_err. Исключения Роллбаккрекуиред.</span><span class="sxs-lookup"><span data-stu-id="ace08-104">Base class for JET_err.RollbackRequired exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ace08-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ace08-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ace08-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ace08-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ace08-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ace08-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ace08-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ace08-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ace08-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ace08-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="ace08-112">Microsoft. ISAM. ESENT. Interop. Есентроллбаккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-112">Microsoft.Isam.Esent.Interop.EsentRollbackRequiredException</span></span>  

<span data-ttu-id="ace08-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ace08-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ace08-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ace08-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ace08-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ace08-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackRequiredException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentRollbackRequiredException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackRequiredException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="ace08-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ace08-116">Thread safety</span></span>

<span data-ttu-id="ace08-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ace08-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ace08-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ace08-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ace08-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ace08-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ace08-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ace08-120">Reference</span></span>

[<span data-ttu-id="ace08-121">Элементы Есентроллбаккрекуиредексцептион</span><span class="sxs-lookup"><span data-stu-id="ace08-121">EsentRollbackRequiredException members</span></span>](./esentrollbackrequiredexception-members.md)

[<span data-ttu-id="ace08-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ace08-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
