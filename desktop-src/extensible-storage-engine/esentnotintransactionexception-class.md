---
description: 'Дополнительные сведения о: Есентнотинтрансактионексцептион Class'
title: Класс Есентнотинтрансактионексцептион
TOCTitle: EsentNotInTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotintransactionexception(v=EXCHG.10)
ms:contentKeyID: 55107294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1630ecc3cea33af09c0c81be69beb9a852609f32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712003"
---
# <a name="esentnotintransactionexception-class"></a><span data-ttu-id="e7459-103">Класс Есентнотинтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-103">EsentNotInTransactionException class</span></span>

<span data-ttu-id="e7459-104">Базовый класс для JET_err. Исключения Нотинтрансактион.</span><span class="sxs-lookup"><span data-stu-id="e7459-104">Base class for JET_err.NotInTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e7459-105">Иерархия наследования</span><span class="sxs-lookup"><span data-stu-id="e7459-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e7459-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e7459-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e7459-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e7459-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e7459-108">Microsoft. ISAM. ESENT. Есентексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e7459-109">Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e7459-110">Microsoft. ISAM. ESENT. Interop. Есентапиексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e7459-111">Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="e7459-112">Microsoft. ISAM. ESENT. Interop. Есентнотинтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-112">Microsoft.Isam.Esent.Interop.EsentNotInTransactionException</span></span>  

<span data-ttu-id="e7459-113">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7459-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7459-114">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7459-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7459-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7459-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInTransactionException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentNotInTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInTransactionException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="e7459-116">Потокобезопасность</span><span class="sxs-lookup"><span data-stu-id="e7459-116">Thread safety</span></span>

<span data-ttu-id="e7459-117">Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="e7459-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e7459-118">Потокобезопасная работа с членами экземпляров типа не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="e7459-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7459-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7459-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7459-120">Справочник</span><span class="sxs-lookup"><span data-stu-id="e7459-120">Reference</span></span>

[<span data-ttu-id="e7459-121">Элементы Есентнотинтрансактионексцептион</span><span class="sxs-lookup"><span data-stu-id="e7459-121">EsentNotInTransactionException members</span></span>](./esentnotintransactionexception-members.md)

[<span data-ttu-id="e7459-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e7459-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
