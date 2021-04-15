---
description: 'Дополнительные сведения о: Есентфилеиоретрексцептион Class'
title: Класс Есентфилеиоретрексцептион
TOCTitle: EsentFileIORetryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileIORetryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfileioretryexception(v=EXCHG.10)
ms:contentKeyID: 55107269
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileIORetryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileIORetryException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6077d77096061b584adc106fceeecf02c9d6953
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701677"
---
# <a name="esentfileioretryexception-class"></a><span data-ttu-id="383ef-103">Класс Есентфилеиоретрексцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-103">EsentFileIORetryException class</span></span>

<span data-ttu-id="383ef-104">Базовый класс для JET_err. Исключения Филеиоретри.</span><span class="sxs-lookup"><span data-stu-id="383ef-104">Base class for JET_err.FileIORetry exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="383ef-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="383ef-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="383ef-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="383ef-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="383ef-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="383ef-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="383ef-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="383ef-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="383ef-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="383ef-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="383ef-112">Microsoft. ISAM. ESENT. Interop. Есентфилеиоретрексцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-112">Microsoft.Isam.Esent.Interop.EsentFileIORetryException</span></span>  

<span data-ttu-id="383ef-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="383ef-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="383ef-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="383ef-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="383ef-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="383ef-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileIORetryException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentFileIORetryException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileIORetryException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="383ef-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="383ef-116">Thread safety</span></span>

<span data-ttu-id="383ef-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="383ef-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="383ef-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="383ef-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="383ef-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="383ef-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="383ef-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="383ef-120">Reference</span></span>

[<span data-ttu-id="383ef-121">Элементы Есентфилеиоретрексцептион</span><span class="sxs-lookup"><span data-stu-id="383ef-121">EsentFileIORetryException members</span></span>](./esentfileioretryexception-members.md)

[<span data-ttu-id="383ef-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="383ef-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
