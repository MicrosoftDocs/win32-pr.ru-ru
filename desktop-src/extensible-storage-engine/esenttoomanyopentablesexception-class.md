---
description: 'Дополнительные сведения о: Есенттуманйопентаблесексцептион Class'
title: Класс Есенттуманйопентаблесексцептион
TOCTitle: EsentTooManyOpenTablesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesexception(v=EXCHG.10)
ms:contentKeyID: 55107362
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 066191af07aab606731f98a16369b2500d24cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155415"
---
# <a name="esenttoomanyopentablesexception-class"></a><span data-ttu-id="94c9d-103">Класс Есенттуманйопентаблесексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-103">EsentTooManyOpenTablesException class</span></span>

<span data-ttu-id="94c9d-104">Базовый класс для JET_err. Исключения Туманйопентаблес.</span><span class="sxs-lookup"><span data-stu-id="94c9d-104">Base class for JET_err.TooManyOpenTables exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="94c9d-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="94c9d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="94c9d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="94c9d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="94c9d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="94c9d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="94c9d-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="94c9d-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="94c9d-110">Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="94c9d-111">Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="94c9d-112">Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="94c9d-113">Microsoft. ISAM. ESENT. Interop. Есенттуманйопентаблесексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>  

<span data-ttu-id="94c9d-114">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="94c9d-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="94c9d-115">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="94c9d-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="94c9d-116">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94c9d-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyOpenTablesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="94c9d-117">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="94c9d-117">Thread safety</span></span>

<span data-ttu-id="94c9d-118">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="94c9d-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="94c9d-119">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="94c9d-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="94c9d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94c9d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="94c9d-121">Справочник</span><span class="sxs-lookup"><span data-stu-id="94c9d-121">Reference</span></span>

[<span data-ttu-id="94c9d-122">Элементы Есенттуманйопентаблесексцептион</span><span class="sxs-lookup"><span data-stu-id="94c9d-122">EsentTooManyOpenTablesException members</span></span>](./esenttoomanyopentablesexception-members.md)

[<span data-ttu-id="94c9d-123">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="94c9d-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
