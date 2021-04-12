---
description: 'Дополнительные сведения о: Есентфорцедетачноталловедексцептион Class'
title: Класс Есентфорцедетачноталловедексцептион
TOCTitle: EsentForceDetachNotAllowedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentforcedetachnotallowedexception(v=EXCHG.10)
ms:contentKeyID: 55101772
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 28a1987b82c4233302bbd3c2e8ffc928f4b55ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155750"
---
# <a name="esentforcedetachnotallowedexception-class"></a><span data-ttu-id="0e6d2-103">Класс Есентфорцедетачноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-103">EsentForceDetachNotAllowedException class</span></span>

<span data-ttu-id="0e6d2-104">Базовый класс для JET_err. Исключения Форцедетачноталловед.</span><span class="sxs-lookup"><span data-stu-id="0e6d2-104">Base class for JET_err.ForceDetachNotAllowed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0e6d2-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="0e6d2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0e6d2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0e6d2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0e6d2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0e6d2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0e6d2-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0e6d2-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0e6d2-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0e6d2-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0e6d2-112">Microsoft. ISAM. ESENT. Interop. Есентфорцедетачноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-112">Microsoft.Isam.Esent.Interop.EsentForceDetachNotAllowedException</span></span>  

<span data-ttu-id="0e6d2-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0e6d2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0e6d2-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0e6d2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0e6d2-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0e6d2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentForceDetachNotAllowedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentForceDetachNotAllowedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentForceDetachNotAllowedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0e6d2-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="0e6d2-116">Thread safety</span></span>

<span data-ttu-id="0e6d2-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="0e6d2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0e6d2-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="0e6d2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e6d2-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e6d2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e6d2-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="0e6d2-120">Reference</span></span>

[<span data-ttu-id="0e6d2-121">Элементы Есентфорцедетачноталловедексцептион</span><span class="sxs-lookup"><span data-stu-id="0e6d2-121">EsentForceDetachNotAllowedException members</span></span>](./esentforcedetachnotallowedexception-members.md)

[<span data-ttu-id="0e6d2-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0e6d2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
