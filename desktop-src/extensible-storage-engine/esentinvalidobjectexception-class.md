---
description: 'Дополнительные сведения о: Есентинвалидобжектексцептион Class'
title: Класс Есентинвалидобжектексцептион
TOCTitle: EsentInvalidObjectException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidobjectexception(v=EXCHG.10)
ms:contentKeyID: 55107288
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidObjectException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86cf06f1f291ca6f2637e652a61b27319b4fa7c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693674"
---
# <a name="esentinvalidobjectexception-class"></a><span data-ttu-id="02af7-103">Класс Есентинвалидобжектексцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-103">EsentInvalidObjectException class</span></span>

<span data-ttu-id="02af7-104">Базовый класс для JET_err. Исключения Инвалидобжект.</span><span class="sxs-lookup"><span data-stu-id="02af7-104">Base class for JET_err.InvalidObject exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="02af7-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="02af7-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="02af7-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="02af7-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="02af7-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="02af7-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="02af7-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="02af7-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="02af7-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="02af7-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="02af7-112">Microsoft. ISAM. ESENT. Interop. Есентинвалидобжектексцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-112">Microsoft.Isam.Esent.Interop.EsentInvalidObjectException</span></span>  

<span data-ttu-id="02af7-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02af7-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02af7-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02af7-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02af7-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02af7-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidObjectException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentInvalidObjectException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidObjectException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="02af7-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="02af7-116">Thread safety</span></span>

<span data-ttu-id="02af7-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="02af7-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="02af7-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="02af7-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="02af7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02af7-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02af7-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="02af7-120">Reference</span></span>

[<span data-ttu-id="02af7-121">Элементы Есентинвалидобжектексцептион</span><span class="sxs-lookup"><span data-stu-id="02af7-121">EsentInvalidObjectException members</span></span>](./esentinvalidobjectexception-members.md)

[<span data-ttu-id="02af7-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="02af7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
