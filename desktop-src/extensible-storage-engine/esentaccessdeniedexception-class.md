---
description: 'Дополнительные сведения о: Есентакцессдениедексцептион Class'
title: Класс Есентакцессдениедексцептион
TOCTitle: EsentAccessDeniedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentaccessdeniedexception(v=EXCHG.10)
ms:contentKeyID: 55101035
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentAccessDeniedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7d81979a93bfa2ad3801047e5ec5cac9796bcda8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684212"
---
# <a name="esentaccessdeniedexception-class"></a><span data-ttu-id="2b8e1-103">Класс Есентакцессдениедексцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-103">EsentAccessDeniedException class</span></span>

<span data-ttu-id="2b8e1-104">Базовый класс для JET_err. Исключения AccessDenied.</span><span class="sxs-lookup"><span data-stu-id="2b8e1-104">Base class for JET_err.AccessDenied exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2b8e1-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="2b8e1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2b8e1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2b8e1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2b8e1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2b8e1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2b8e1-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2b8e1-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2b8e1-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2b8e1-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="2b8e1-112">Microsoft. ISAM. ESENT. Interop. Есентакцессдениедексцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-112">Microsoft.Isam.Esent.Interop.EsentAccessDeniedException</span></span>  

<span data-ttu-id="2b8e1-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2b8e1-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2b8e1-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2b8e1-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2b8e1-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b8e1-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentAccessDeniedException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentAccessDeniedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentAccessDeniedException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="2b8e1-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="2b8e1-116">Thread safety</span></span>

<span data-ttu-id="2b8e1-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="2b8e1-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2b8e1-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="2b8e1-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b8e1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b8e1-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2b8e1-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="2b8e1-120">Reference</span></span>

[<span data-ttu-id="2b8e1-121">Элементы Есентакцессдениедексцептион</span><span class="sxs-lookup"><span data-stu-id="2b8e1-121">EsentAccessDeniedException members</span></span>](./esentaccessdeniedexception-members.md)

[<span data-ttu-id="2b8e1-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2b8e1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
