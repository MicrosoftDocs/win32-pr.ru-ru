---
description: 'Дополнительные сведения о: Есентдискексцептион Class'
title: Класс Есентдискексцептион
TOCTitle: EsentDiskException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskexception(v=EXCHG.10)
ms:contentKeyID: 55101517
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22c2e2e2f829b6fcc6967e6e58692613243549c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424001"
---
# <a name="esentdiskexception-class"></a><span data-ttu-id="2ac9a-103">Класс Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-103">EsentDiskException class</span></span>

<span data-ttu-id="2ac9a-104">Базовый класс для исключений диска.</span><span class="sxs-lookup"><span data-stu-id="2ac9a-104">Base class for Disk exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2ac9a-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="2ac9a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2ac9a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2ac9a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2ac9a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2ac9a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2ac9a-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2ac9a-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2ac9a-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="2ac9a-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            <span data-ttu-id="2ac9a-112">Microsoft. ISAM. ESENT. Interop. Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-112">Microsoft.Isam.Esent.Interop.EsentDiskException</span></span>  
              [<span data-ttu-id="2ac9a-113">Microsoft. ISAM. ESENT. Interop. Есентдискфуллексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-113">Microsoft.Isam.Esent.Interop.EsentDiskFullException</span></span>](./esentdiskfullexception-class.md)  
              [<span data-ttu-id="2ac9a-114">Microsoft. ISAM. ESENT. Interop. Есентлогдискфуллексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-114">Microsoft.Isam.Esent.Interop.EsentLogDiskFullException</span></span>](./esentlogdiskfullexception-class.md)  

<span data-ttu-id="2ac9a-115">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ac9a-115">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ac9a-116">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2ac9a-116">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac9a-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ac9a-117">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentDiskException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentDiskException
```

``` csharp
[SerializableAttribute]
public abstract class EsentDiskException : EsentResourceException
```

## <a name="thread-safety"></a><span data-ttu-id="2ac9a-118">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="2ac9a-118">Thread safety</span></span>

<span data-ttu-id="2ac9a-119">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="2ac9a-119">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2ac9a-120">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="2ac9a-120">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ac9a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ac9a-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ac9a-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="2ac9a-122">Reference</span></span>

[<span data-ttu-id="2ac9a-123">Элементы Есентдискексцептион</span><span class="sxs-lookup"><span data-stu-id="2ac9a-123">EsentDiskException members</span></span>](./esentdiskexception-members.md)

[<span data-ttu-id="2ac9a-124">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2ac9a-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
