---
description: 'Дополнительные сведения о: Есентдериведколумнкорруптионексцептион Class'
title: Класс Есентдериведколумнкорруптионексцептион
TOCTitle: EsentDerivedColumnCorruptionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentderivedcolumncorruptionexception(v=EXCHG.10)
ms:contentKeyID: 55101606
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 806a8b81383b63cd2ea7b0c0675504e30a7d4dd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703224"
---
# <a name="esentderivedcolumncorruptionexception-class"></a><span data-ttu-id="e5068-103">Класс Есентдериведколумнкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-103">EsentDerivedColumnCorruptionException class</span></span>

<span data-ttu-id="e5068-104">Базовый класс для JET_err. Исключения Дериведколумнкорруптион.</span><span class="sxs-lookup"><span data-stu-id="e5068-104">Base class for JET_err.DerivedColumnCorruption exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e5068-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e5068-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e5068-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e5068-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e5068-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e5068-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e5068-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e5068-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e5068-110">Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="e5068-111">Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="e5068-112">Microsoft. ISAM. ESENT. Interop. Есентдериведколумнкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-112">Microsoft.Isam.Esent.Interop.EsentDerivedColumnCorruptionException</span></span>  

<span data-ttu-id="e5068-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e5068-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e5068-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e5068-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e5068-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5068-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDerivedColumnCorruptionException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDerivedColumnCorruptionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDerivedColumnCorruptionException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="e5068-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e5068-116">Thread safety</span></span>

<span data-ttu-id="e5068-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e5068-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e5068-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e5068-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5068-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5068-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e5068-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e5068-120">Reference</span></span>

[<span data-ttu-id="e5068-121">Элементы Есентдериведколумнкорруптионексцептион</span><span class="sxs-lookup"><span data-stu-id="e5068-121">EsentDerivedColumnCorruptionException members</span></span>](./esentderivedcolumncorruptionexception-members.md)

[<span data-ttu-id="e5068-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e5068-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
