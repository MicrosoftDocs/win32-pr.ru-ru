---
description: 'Дополнительные сведения о: Есентколумнночункексцептион Class'
title: Класс Есентколумнночункексцептион
TOCTitle: EsentColumnNoChunkException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumnnochunkexception(v=EXCHG.10)
ms:contentKeyID: 55101234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57ff408b4d45debc3af98aabc70be2d56ad712ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081053"
---
# <a name="esentcolumnnochunkexception-class"></a><span data-ttu-id="7bc50-103">Класс Есентколумнночункексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-103">EsentColumnNoChunkException class</span></span>

<span data-ttu-id="7bc50-104">Базовый класс для JET_err. Исключения Колумнночунк.</span><span class="sxs-lookup"><span data-stu-id="7bc50-104">Base class for JET_err.ColumnNoChunk exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7bc50-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="7bc50-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7bc50-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7bc50-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7bc50-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7bc50-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7bc50-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7bc50-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7bc50-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="7bc50-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="7bc50-112">Microsoft. ISAM. ESENT. Interop. Есентколумнночункексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-112">Microsoft.Isam.Esent.Interop.EsentColumnNoChunkException</span></span>  

<span data-ttu-id="7bc50-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7bc50-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7bc50-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7bc50-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc50-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bc50-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnNoChunkException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnNoChunkException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnNoChunkException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="7bc50-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="7bc50-116">Thread safety</span></span>

<span data-ttu-id="7bc50-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="7bc50-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7bc50-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="7bc50-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bc50-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bc50-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7bc50-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="7bc50-120">Reference</span></span>

[<span data-ttu-id="7bc50-121">Элементы Есентколумнночункексцептион</span><span class="sxs-lookup"><span data-stu-id="7bc50-121">EsentColumnNoChunkException members</span></span>](./esentcolumnnochunkexception-members.md)

[<span data-ttu-id="7bc50-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7bc50-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
