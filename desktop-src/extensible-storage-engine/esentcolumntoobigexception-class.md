---
description: 'Дополнительные сведения о: Есентколумнтубижексцептион Class'
title: Класс Есентколумнтубижексцептион
TOCTitle: EsentColumnTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumntoobigexception(v=EXCHG.10)
ms:contentKeyID: 55101348
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a72ef8849dcbb8854786d126899924f0d835dcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713193"
---
# <a name="esentcolumntoobigexception-class"></a><span data-ttu-id="ebd98-103">Класс Есентколумнтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-103">EsentColumnTooBigException class</span></span>

<span data-ttu-id="ebd98-104">Базовый класс для JET_err. Исключения Колумнтубиг.</span><span class="sxs-lookup"><span data-stu-id="ebd98-104">Base class for JET_err.ColumnTooBig exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ebd98-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="ebd98-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ebd98-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ebd98-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ebd98-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ebd98-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ebd98-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ebd98-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ebd98-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ebd98-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ebd98-112">Microsoft. ISAM. ESENT. Interop. Есентколумнтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-112">Microsoft.Isam.Esent.Interop.EsentColumnTooBigException</span></span>  

<span data-ttu-id="ebd98-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ebd98-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ebd98-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ebd98-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ebd98-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebd98-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnTooBigException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnTooBigException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ebd98-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="ebd98-116">Thread safety</span></span>

<span data-ttu-id="ebd98-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="ebd98-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ebd98-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="ebd98-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebd98-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebd98-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ebd98-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="ebd98-120">Reference</span></span>

[<span data-ttu-id="ebd98-121">Элементы Есентколумнтубижексцептион</span><span class="sxs-lookup"><span data-stu-id="ebd98-121">EsentColumnTooBigException members</span></span>](./esentcolumntoobigexception-members.md)

[<span data-ttu-id="ebd98-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ebd98-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
