---
description: 'Дополнительные сведения о: Есентаутофбуфферсексцептион Class'
title: Класс Есентаутофбуфферсексцептион
TOCTitle: EsentOutOfBuffersException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofbuffersexception(v=EXCHG.10)
ms:contentKeyID: 55102398
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fc8c5d22a6dc4d33d855d6d98a78e8ce7d33ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711807"
---
# <a name="esentoutofbuffersexception-class"></a><span data-ttu-id="b7434-103">Класс Есентаутофбуфферсексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-103">EsentOutOfBuffersException class</span></span>

<span data-ttu-id="b7434-104">Базовый класс для JET_err. Исключения Аутофбуфферс.</span><span class="sxs-lookup"><span data-stu-id="b7434-104">Base class for JET_err.OutOfBuffers exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b7434-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="b7434-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b7434-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b7434-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b7434-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b7434-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b7434-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b7434-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b7434-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="b7434-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="b7434-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="b7434-113">Microsoft. ISAM. ESENT. Interop. Есентаутофбуфферсексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-113">Microsoft.Isam.Esent.Interop.EsentOutOfBuffersException</span></span>  

<span data-ttu-id="b7434-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7434-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7434-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7434-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7434-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7434-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfBuffersException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfBuffersException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfBuffersException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="b7434-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="b7434-117">Thread safety</span></span>

<span data-ttu-id="b7434-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="b7434-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b7434-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="b7434-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7434-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7434-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7434-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="b7434-121">Reference</span></span>

[<span data-ttu-id="b7434-122">Элементы Есентаутофбуфферсексцептион</span><span class="sxs-lookup"><span data-stu-id="b7434-122">EsentOutOfBuffersException members</span></span>](./esentoutofbuffersexception-members.md)

[<span data-ttu-id="b7434-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b7434-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
