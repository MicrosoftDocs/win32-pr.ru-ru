---
description: 'Дополнительные сведения о: Есентрекордтубижексцептион Class'
title: Класс Есентрекордтубижексцептион
TOCTitle: EsentRecordTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordtoobigexception(v=EXCHG.10)
ms:contentKeyID: 55107350
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c252b8c3c5fdf8a78a0a971b24065d1cb8c92152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144302"
---
# <a name="esentrecordtoobigexception-class"></a><span data-ttu-id="85504-103">Класс Есентрекордтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="85504-103">EsentRecordTooBigException class</span></span>

<span data-ttu-id="85504-104">Базовый класс для JET_err. Исключения Рекордтубиг.</span><span class="sxs-lookup"><span data-stu-id="85504-104">Base class for JET_err.RecordTooBig exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="85504-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="85504-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="85504-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="85504-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="85504-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="85504-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="85504-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="85504-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="85504-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="85504-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="85504-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="85504-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="85504-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="85504-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="85504-112">Microsoft. ISAM. ESENT. Interop. Есентрекордтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="85504-112">Microsoft.Isam.Esent.Interop.EsentRecordTooBigException</span></span>  

<span data-ttu-id="85504-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="85504-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="85504-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="85504-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="85504-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85504-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordTooBigException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordTooBigException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="85504-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="85504-116">Thread safety</span></span>

<span data-ttu-id="85504-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="85504-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="85504-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="85504-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="85504-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85504-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="85504-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="85504-120">Reference</span></span>

[<span data-ttu-id="85504-121">Элементы Есентрекордтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="85504-121">EsentRecordTooBigException members</span></span>](./esentrecordtoobigexception-members.md)

[<span data-ttu-id="85504-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="85504-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
