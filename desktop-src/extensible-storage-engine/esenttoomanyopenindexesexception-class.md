---
description: 'Дополнительные сведения о: Есенттуманйопениндексесексцептион Class'
title: Класс Есенттуманйопениндексесексцептион
TOCTitle: EsentTooManyOpenIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopenindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103106
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 681f9a8ec67b9b9c82babcc3814833a1a3dbb0d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272143"
---
# <a name="esenttoomanyopenindexesexception-class"></a><span data-ttu-id="38917-103">Класс Есенттуманйопениндексесексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-103">EsentTooManyOpenIndexesException class</span></span>

<span data-ttu-id="38917-104">Базовый класс для JET_err. Исключения Туманйопениндексес.</span><span class="sxs-lookup"><span data-stu-id="38917-104">Base class for JET_err.TooManyOpenIndexes exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="38917-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="38917-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="38917-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="38917-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="38917-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="38917-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="38917-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="38917-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="38917-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="38917-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="38917-112">Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="38917-113">Microsoft. ISAM. ESENT. Interop. Есенттуманйопениндексесексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>  

<span data-ttu-id="38917-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="38917-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="38917-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="38917-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="38917-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38917-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenIndexesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyOpenIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenIndexesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="38917-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="38917-117">Thread safety</span></span>

<span data-ttu-id="38917-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="38917-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="38917-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="38917-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="38917-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38917-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="38917-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="38917-121">Reference</span></span>

[<span data-ttu-id="38917-122">Элементы Есенттуманйопениндексесексцептион</span><span class="sxs-lookup"><span data-stu-id="38917-122">EsentTooManyOpenIndexesException members</span></span>](./esenttoomanyopenindexesexception-members.md)

[<span data-ttu-id="38917-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="38917-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
