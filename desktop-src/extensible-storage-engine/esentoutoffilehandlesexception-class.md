---
description: 'Дополнительные сведения о: Есентаутоффилехандлесексцептион Class'
title: Класс Есентаутоффилехандлесексцептион
TOCTitle: EsentOutOfFileHandlesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoffilehandlesexception(v=EXCHG.10)
ms:contentKeyID: 55102419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24d8dec9de0cb4149835766222348dc037f54c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712751"
---
# <a name="esentoutoffilehandlesexception-class"></a><span data-ttu-id="53605-103">Класс Есентаутоффилехандлесексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-103">EsentOutOfFileHandlesException class</span></span>

<span data-ttu-id="53605-104">Базовый класс для JET_err. Исключения Аутоффилехандлес.</span><span class="sxs-lookup"><span data-stu-id="53605-104">Base class for JET_err.OutOfFileHandles exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="53605-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="53605-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="53605-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="53605-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="53605-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="53605-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="53605-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="53605-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="53605-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="53605-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="53605-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="53605-113">Microsoft. ISAM. ESENT. Interop. Есентаутоффилехандлесексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-113">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>  

<span data-ttu-id="53605-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53605-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53605-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53605-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53605-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53605-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfFileHandlesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfFileHandlesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfFileHandlesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="53605-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="53605-117">Thread safety</span></span>

<span data-ttu-id="53605-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="53605-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="53605-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="53605-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="53605-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53605-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53605-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="53605-121">Reference</span></span>

[<span data-ttu-id="53605-122">Элементы Есентаутоффилехандлесексцептион</span><span class="sxs-lookup"><span data-stu-id="53605-122">EsentOutOfFileHandlesException members</span></span>](./esentoutoffilehandlesexception-members.md)

[<span data-ttu-id="53605-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="53605-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
