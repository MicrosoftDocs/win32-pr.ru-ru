---
description: 'Дополнительные сведения о: Есентрекорднокопексцептион Class'
title: Класс Есентрекорднокопексцептион
TOCTitle: EsentRecordNoCopyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnocopyexception(v=EXCHG.10)
ms:contentKeyID: 55102583
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cca22790cc7cc45199be939a9acad944ab2f613e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264963"
---
# <a name="esentrecordnocopyexception-class"></a><span data-ttu-id="3ed17-103">Класс Есентрекорднокопексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-103">EsentRecordNoCopyException class</span></span>

<span data-ttu-id="3ed17-104">Базовый класс для JET_err. Исключения Рекорднокопи.</span><span class="sxs-lookup"><span data-stu-id="3ed17-104">Base class for JET_err.RecordNoCopy exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="3ed17-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="3ed17-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="3ed17-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="3ed17-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="3ed17-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="3ed17-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="3ed17-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="3ed17-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="3ed17-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="3ed17-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="3ed17-112">Microsoft. ISAM. ESENT. Interop. Есентрекорднокопексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-112">Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException</span></span>  

<span data-ttu-id="3ed17-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3ed17-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3ed17-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3ed17-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed17-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ed17-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNoCopyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRecordNoCopyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNoCopyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="3ed17-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="3ed17-116">Thread safety</span></span>

<span data-ttu-id="3ed17-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="3ed17-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="3ed17-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="3ed17-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ed17-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ed17-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3ed17-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="3ed17-120">Reference</span></span>

[<span data-ttu-id="3ed17-121">Элементы Есентрекорднокопексцептион</span><span class="sxs-lookup"><span data-stu-id="3ed17-121">EsentRecordNoCopyException members</span></span>](./esentrecordnocopyexception-members.md)

[<span data-ttu-id="3ed17-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3ed17-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
