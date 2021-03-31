---
description: 'Дополнительные сведения о: Есентрекордтубигфорбакквардкомпатибилитексцептион Class'
title: Класс Есентрекордтубигфорбакквардкомпатибилитексцептион
TOCTitle: EsentRecordTooBigForBackwardCompatibilityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordtoobigforbackwardcompatibilityexception(v=EXCHG.10)
ms:contentKeyID: 55102602
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3d56e87678daf465f3f303d649e8c554fbb0c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809173"
---
# <a name="esentrecordtoobigforbackwardcompatibilityexception-class"></a><span data-ttu-id="6e4ae-103">Класс Есентрекордтубигфорбакквардкомпатибилитексцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-103">EsentRecordTooBigForBackwardCompatibilityException class</span></span>

<span data-ttu-id="6e4ae-104">Базовый класс для JET_err. Исключения Рекордтубигфорбакквардкомпатибилити.</span><span class="sxs-lookup"><span data-stu-id="6e4ae-104">Base class for JET_err.RecordTooBigForBackwardCompatibility exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6e4ae-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="6e4ae-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6e4ae-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6e4ae-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6e4ae-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="6e4ae-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6e4ae-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6e4ae-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6e4ae-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="6e4ae-111">Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="6e4ae-112">Microsoft. ISAM. ESENT. Interop. Есентрекордтубигфорбакквардкомпатибилитексцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-112">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>  

<span data-ttu-id="6e4ae-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e4ae-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e4ae-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e4ae-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4ae-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e4ae-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordTooBigForBackwardCompatibilityException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordTooBigForBackwardCompatibilityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordTooBigForBackwardCompatibilityException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="6e4ae-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="6e4ae-116">Thread safety</span></span>

<span data-ttu-id="6e4ae-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="6e4ae-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6e4ae-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="6e4ae-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e4ae-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e4ae-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e4ae-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="6e4ae-120">Reference</span></span>

[<span data-ttu-id="6e4ae-121">Элементы Есентрекордтубигфорбакквардкомпатибилитексцептион</span><span class="sxs-lookup"><span data-stu-id="6e4ae-121">EsentRecordTooBigForBackwardCompatibilityException members</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-members.md)

[<span data-ttu-id="6e4ae-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="6e4ae-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
