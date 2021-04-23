---
description: 'Дополнительные сведения о: Есентколумнредундантексцептион Class'
title: Класс Есентколумнредундантексцептион
TOCTitle: EsentColumnRedundantException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumnredundantexception(v=EXCHG.10)
ms:contentKeyID: 55101247
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18b2fdd850e26c5a435841110a4e1ac5c0c7c640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710891"
---
# <a name="esentcolumnredundantexception-class"></a><span data-ttu-id="846da-103">Класс Есентколумнредундантексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-103">EsentColumnRedundantException class</span></span>

<span data-ttu-id="846da-104">Базовый класс для JET_err. Исключения Колумнредундант.</span><span class="sxs-lookup"><span data-stu-id="846da-104">Base class for JET_err.ColumnRedundant exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="846da-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="846da-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="846da-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="846da-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="846da-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="846da-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="846da-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="846da-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="846da-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="846da-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="846da-112">Microsoft. ISAM. ESENT. Interop. Есентколумнредундантексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-112">Microsoft.Isam.Esent.Interop.EsentColumnRedundantException</span></span>  

<span data-ttu-id="846da-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="846da-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="846da-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="846da-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="846da-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="846da-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnRedundantException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnRedundantException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnRedundantException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="846da-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="846da-116">Thread safety</span></span>

<span data-ttu-id="846da-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="846da-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="846da-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="846da-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="846da-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="846da-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="846da-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="846da-120">Reference</span></span>

[<span data-ttu-id="846da-121">Элементы Есентколумнредундантексцептион</span><span class="sxs-lookup"><span data-stu-id="846da-121">EsentColumnRedundantException members</span></span>](./esentcolumnredundantexception-members.md)

[<span data-ttu-id="846da-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="846da-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
