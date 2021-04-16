---
description: 'Дополнительные сведения о: Есентдатабасешарингвиолатионексцептион Class'
title: Класс Есентдатабасешарингвиолатионексцептион
TOCTitle: EsentDatabaseSharingViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasesharingviolationexception(v=EXCHG.10)
ms:contentKeyID: 55101436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 03d168a0235cdc31cd8e4420924f5f8b2dae90dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263769"
---
# <a name="esentdatabasesharingviolationexception-class"></a><span data-ttu-id="25043-103">Класс Есентдатабасешарингвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-103">EsentDatabaseSharingViolationException class</span></span>

<span data-ttu-id="25043-104">Базовый класс для JET_err. Исключения Датабасешарингвиолатион.</span><span class="sxs-lookup"><span data-stu-id="25043-104">Base class for JET_err.DatabaseSharingViolation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="25043-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="25043-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="25043-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="25043-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="25043-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="25043-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="25043-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="25043-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="25043-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="25043-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="25043-112">Microsoft. ISAM. ESENT. Interop. Есентдатабасешарингвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-112">Microsoft.Isam.Esent.Interop.EsentDatabaseSharingViolationException</span></span>  

<span data-ttu-id="25043-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25043-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25043-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25043-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25043-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25043-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseSharingViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseSharingViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseSharingViolationException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="25043-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="25043-116">Thread safety</span></span>

<span data-ttu-id="25043-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="25043-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="25043-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="25043-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="25043-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25043-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25043-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="25043-120">Reference</span></span>

[<span data-ttu-id="25043-121">Элементы Есентдатабасешарингвиолатионексцептион</span><span class="sxs-lookup"><span data-stu-id="25043-121">EsentDatabaseSharingViolationException members</span></span>](./esentdatabasesharingviolationexception-members.md)

[<span data-ttu-id="25043-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="25043-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
