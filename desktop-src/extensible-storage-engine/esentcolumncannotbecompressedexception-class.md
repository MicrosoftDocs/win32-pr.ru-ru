---
description: 'Дополнительные сведения о: Есентколумнканнотбекомпресседексцептион Class'
title: Класс Есентколумнканнотбекомпресседексцептион
TOCTitle: EsentColumnCannotBeCompressedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumncannotbecompressedexception(v=EXCHG.10)
ms:contentKeyID: 55101403
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1159125aaa9f1c522e3e3d1374bda772ce6c5db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081516"
---
# <a name="esentcolumncannotbecompressedexception-class"></a><span data-ttu-id="c89c3-103">Класс Есентколумнканнотбекомпресседексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-103">EsentColumnCannotBeCompressedException class</span></span>

<span data-ttu-id="c89c3-104">Базовый класс для JET_err. Исключения Колумнканнотбекомпрессед.</span><span class="sxs-lookup"><span data-stu-id="c89c3-104">Base class for JET_err.ColumnCannotBeCompressed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c89c3-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="c89c3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c89c3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c89c3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c89c3-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c89c3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c89c3-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c89c3-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c89c3-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="c89c3-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="c89c3-112">Microsoft. ISAM. ESENT. Interop. Есентколумнканнотбекомпресседексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-112">Microsoft.Isam.Esent.Interop.EsentColumnCannotBeCompressedException</span></span>  

<span data-ttu-id="c89c3-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c89c3-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c89c3-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c89c3-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c89c3-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c89c3-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnCannotBeCompressedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnCannotBeCompressedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnCannotBeCompressedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="c89c3-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="c89c3-116">Thread safety</span></span>

<span data-ttu-id="c89c3-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="c89c3-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c89c3-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="c89c3-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c89c3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c89c3-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c89c3-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="c89c3-120">Reference</span></span>

[<span data-ttu-id="c89c3-121">Элементы Есентколумнканнотбекомпресседексцептион</span><span class="sxs-lookup"><span data-stu-id="c89c3-121">EsentColumnCannotBeCompressedException members</span></span>](./esentcolumncannotbecompressedexception-members.md)

[<span data-ttu-id="c89c3-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c89c3-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
