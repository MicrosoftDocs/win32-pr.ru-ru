---
description: 'Дополнительные сведения о: Есентгивенлогфилехасбадсигнатуриксцептион Class'
title: Класс Есентгивенлогфилехасбадсигнатуриксцептион
TOCTitle: EsentGivenLogFileHasBadSignatureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentgivenlogfilehasbadsignatureexception(v=EXCHG.10)
ms:contentKeyID: 55101732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2bcb1fa75eb5f6d14d86fc1e9249fbe4c34848c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719654"
---
# <a name="esentgivenlogfilehasbadsignatureexception-class"></a><span data-ttu-id="3d9cf-103">Класс Есентгивенлогфилехасбадсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-103">EsentGivenLogFileHasBadSignatureException class</span></span>

<span data-ttu-id="3d9cf-104">Базовый класс для JET_err. Исключения Гивенлогфилехасбадсигнатуре.</span><span class="sxs-lookup"><span data-stu-id="3d9cf-104">Base class for JET_err.GivenLogFileHasBadSignature exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3d9cf-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="3d9cf-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3d9cf-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3d9cf-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3d9cf-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3d9cf-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3d9cf-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3d9cf-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3d9cf-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="3d9cf-111">Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="3d9cf-112">Microsoft. ISAM. ESENT. Interop. Есентгивенлогфилехасбадсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-112">Microsoft.Isam.Esent.Interop.EsentGivenLogFileHasBadSignatureException</span></span>  

<span data-ttu-id="3d9cf-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3d9cf-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3d9cf-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3d9cf-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3d9cf-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d9cf-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentGivenLogFileHasBadSignatureException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentGivenLogFileHasBadSignatureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentGivenLogFileHasBadSignatureException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="3d9cf-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="3d9cf-116">Thread safety</span></span>

<span data-ttu-id="3d9cf-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="3d9cf-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3d9cf-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3d9cf-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3d9cf-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d9cf-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3d9cf-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="3d9cf-120">Reference</span></span>

[<span data-ttu-id="3d9cf-121">Элементы Есентгивенлогфилехасбадсигнатуриксцептион</span><span class="sxs-lookup"><span data-stu-id="3d9cf-121">EsentGivenLogFileHasBadSignatureException members</span></span>](./esentgivenlogfilehasbadsignatureexception-members.md)

[<span data-ttu-id="3d9cf-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3d9cf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
