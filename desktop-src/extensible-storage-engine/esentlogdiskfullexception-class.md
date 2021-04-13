---
description: 'Дополнительные сведения о: Есентлогдискфуллексцептион Class'
title: Класс Есентлогдискфуллексцептион
TOCTitle: EsentLogDiskFullException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogdiskfullexception(v=EXCHG.10)
ms:contentKeyID: 55102101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogDiskFullException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a237a8d21aab32114708a5cb59545ed827e05bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345992"
---
# <a name="esentlogdiskfullexception-class"></a><span data-ttu-id="f8f42-103">Класс Есентлогдискфуллексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-103">EsentLogDiskFullException class</span></span>

<span data-ttu-id="f8f42-104">Базовый класс для JET_err. Исключения Логдискфулл.</span><span class="sxs-lookup"><span data-stu-id="f8f42-104">Base class for JET_err.LogDiskFull exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f8f42-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="f8f42-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f8f42-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f8f42-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f8f42-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f8f42-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f8f42-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f8f42-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f8f42-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="f8f42-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="f8f42-112">Microsoft. ISAM. ESENT. Interop. Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>](./esentdiskexception-class.md)  
              <span data-ttu-id="f8f42-113">Microsoft. ISAM. ESENT. Interop. Есентлогдискфуллексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-113">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>  

<span data-ttu-id="f8f42-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f8f42-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f8f42-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f8f42-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f8f42-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8f42-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogDiskFullException _
    Inherits EsentDiskException
'Usage
Dim instance As EsentLogDiskFullException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogDiskFullException : EsentDiskException
```

## <a name="thread-safety"></a><span data-ttu-id="f8f42-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="f8f42-117">Thread safety</span></span>

<span data-ttu-id="f8f42-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="f8f42-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f8f42-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="f8f42-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8f42-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8f42-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f8f42-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="f8f42-121">Reference</span></span>

[<span data-ttu-id="f8f42-122">Элементы Есентлогдискфуллексцептион</span><span class="sxs-lookup"><span data-stu-id="f8f42-122">EsentLogDiskFullException members</span></span>](./esentlogdiskfullexception-members.md)

[<span data-ttu-id="f8f42-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f8f42-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
