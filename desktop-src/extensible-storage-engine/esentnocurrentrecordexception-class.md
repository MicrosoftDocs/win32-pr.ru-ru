---
description: 'Дополнительные сведения о: Есентнокуррентрекордексцептион Class'
title: Класс Есентнокуррентрекордексцептион
TOCTitle: EsentNoCurrentRecordException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentrecordexception(v=EXCHG.10)
ms:contentKeyID: 55102290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed58890ccd410101ecc6e6f38fafa0d254f4c2d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713091"
---
# <a name="esentnocurrentrecordexception-class"></a><span data-ttu-id="43e8f-103">Класс Есентнокуррентрекордексцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-103">EsentNoCurrentRecordException class</span></span>

<span data-ttu-id="43e8f-104">Базовый класс для JET_err. Исключения Нокуррентрекорд.</span><span class="sxs-lookup"><span data-stu-id="43e8f-104">Base class for JET_err.NoCurrentRecord exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="43e8f-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="43e8f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="43e8f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="43e8f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="43e8f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="43e8f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="43e8f-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="43e8f-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="43e8f-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="43e8f-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="43e8f-112">Microsoft. ISAM. ESENT. Interop. Есентнокуррентрекордексцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-112">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>  

<span data-ttu-id="43e8f-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43e8f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="43e8f-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43e8f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43e8f-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43e8f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentRecordException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoCurrentRecordException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentRecordException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="43e8f-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="43e8f-116">Thread safety</span></span>

<span data-ttu-id="43e8f-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="43e8f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="43e8f-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="43e8f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="43e8f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43e8f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43e8f-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="43e8f-120">Reference</span></span>

[<span data-ttu-id="43e8f-121">Элементы Есентнокуррентрекордексцептион</span><span class="sxs-lookup"><span data-stu-id="43e8f-121">EsentNoCurrentRecordException members</span></span>](./esentnocurrentrecordexception-members.md)

[<span data-ttu-id="43e8f-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="43e8f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
