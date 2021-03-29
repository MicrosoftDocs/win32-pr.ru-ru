---
description: 'Дополнительные сведения о: Есентдатабасеснотфромсамеснапшотексцептион Class'
title: Класс Есентдатабасеснотфромсамеснапшотексцептион
TOCTitle: EsentDatabasesNotFromSameSnapshotException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesnotfromsamesnapshotexception(v=EXCHG.10)
ms:contentKeyID: 55101443
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6d26ecdab73517d1634bc6beb79dfc1249a2756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647245"
---
# <a name="esentdatabasesnotfromsamesnapshotexception-class"></a><span data-ttu-id="e2286-103">Класс Есентдатабасеснотфромсамеснапшотексцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-103">EsentDatabasesNotFromSameSnapshotException class</span></span>

<span data-ttu-id="e2286-104">Базовый класс для JET_err. Исключения Датабасеснотфромсамеснапшот.</span><span class="sxs-lookup"><span data-stu-id="e2286-104">Base class for JET_err.DatabasesNotFromSameSnapshot exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e2286-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e2286-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e2286-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e2286-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e2286-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e2286-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e2286-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e2286-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e2286-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e2286-111">Microsoft. ISAM. ESENT. Interop. Есентобсолетиксцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="e2286-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасеснотфромсамеснапшотексцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-112">Microsoft.Isam.Esent.Interop.EsentDatabasesNotFromSameSnapshotException</span></span>  

<span data-ttu-id="e2286-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e2286-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e2286-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e2286-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e2286-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2286-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabasesNotFromSameSnapshotException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabasesNotFromSameSnapshotException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabasesNotFromSameSnapshotException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="e2286-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e2286-116">Thread safety</span></span>

<span data-ttu-id="e2286-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e2286-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e2286-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e2286-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2286-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2286-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e2286-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e2286-120">Reference</span></span>

[<span data-ttu-id="e2286-121">Элементы Есентдатабасеснотфромсамеснапшотексцептион</span><span class="sxs-lookup"><span data-stu-id="e2286-121">EsentDatabasesNotFromSameSnapshotException members</span></span>](./esentdatabasesnotfromsamesnapshotexception-members.md)

[<span data-ttu-id="e2286-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e2286-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
